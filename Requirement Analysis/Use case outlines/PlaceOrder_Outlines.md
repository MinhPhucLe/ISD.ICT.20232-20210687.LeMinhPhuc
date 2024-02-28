<table>
<colgroup>
<col style="width: 22%" />
<col style="width: 28%" />
<col style="width: 24%" />
<col style="width: 24%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Use case code</strong> </th>
<th>UC003 </th>
<th><strong>Use case name</strong> </th>
<th>Place order </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Actor</strong> </td>
<td colspan="3">Customer, administrator, VNPay</td>
</tr>
<tr class="even">
<td><strong>Description</strong> </td>
<td colspan="3">Customer is permitted to place order</td>
</tr>
<tr class="odd">
<td><strong>Precondition</strong> </td>
<td colspan="3">Need at least one item in the cart </td>
</tr>
<tr class="even">
<td><p><strong>Flow of events</strong> </p>
<p><strong>(Success)</strong> </p></td>
<td colspan="3"><p> </p>
<table>
<colgroup>
<col style="width: 16%" />
<col style="width: 41%" />
<col style="width: 41%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>No</strong> </th>
<th><strong>Actor</strong> </th>
<th><strong>Action</strong> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.                  </td>
<td>Customer </td>
<td>Choose product to place order in the cart view </td>
</tr>
<tr class="even">
<td>2. </td>
<td>software </td>
<td>Check the availability of products in cart </td>
</tr>
<tr class="odd">
<td>3.                  </td>
<td>softare </td>
<td>Ask customer to set up delivery information</td>
</tr>
<tr class="even">
<td>4.                  </td>
<td>Customer </td>
<td>Set up delivery information</td>
</tr>
<tr class="odd">
<td>5.                  </td>
<td>software </td>
<td><p>Calculate (or</p>
<p>recalculate) the delivery fee, total product price including delivery
fee.</p></td>
</tr>
<tr class="even">
<td>6.                  </td>
<td>software </td>
<td>Display and temporarily save invoice information,</td>
</tr>
<tr class="odd">
<td>7.                  </td>
<td>software </td>
<td>Check the input information</td>
</tr>
<tr class="even">
<td>8.                  </td>
<td>Customer </td>
<td>Have the option to select rush order delivery</td>
</tr>
<tr class="odd">
<td>9.</td>
<td>Customer</td>
<td>Fill in the delivery information</td>
</tr>
<tr class="even">
<td>10. </td>
<td>Software </td>
<td>Check whether the delivery address supports this service and if any
products are eligible.</td>
</tr>
<tr class="odd">
<td>11. </td>
<td>Customer </td>
<td>Adjust the delivery method or the items they wish to purchase if
necessary.</td>
</tr>
<tr class="even">
<td>12. </td>
<td>Software </td>
<td>Recalculates the delivery fees and updates the corresponding
invoice.</td>
</tr>
<tr class="odd">
<td>13.</td>
<td>Software</td>
<td>Display information and ask customer to choose the payment
method</td>
</tr>
<tr class="even">
<td>14.</td>
<td>Customer</td>
<td>Choose the payment method</td>
</tr>
<tr class="odd">
<td>15.</td>
<td>Customer</td>
<td>Pay the order</td>
</tr>
<tr class="even">
<td>16.</td>
<td>VNPay</td>
<td>Request information for customer to fill in</td>
</tr>
<tr class="odd">
<td>17.</td>
<td>Software</td>
<td>Check if the payment is successful or not</td>
</tr>
<tr class="even">
<td>18.</td>
<td>Administrator</td>
<td>Approve the order</td>
</tr>
<tr class="odd">
<td>18.</td>
<td>Software</td>
<td>Display transaction information</td>
</tr>
<tr class="even">
<td>19.</td>
<td>Software</td>
<td><p>Send all order and transaction information to the</p>
<p>customer's email</p></td>
</tr>
<tr class="odd">
<td>20.</td>
<td>Customer</td>
<td><p>Go back to any step or exit the software during the</p>
<p>ordering process</p></td>
</tr>
</tbody>
</table>
<p> <br />
 </p></td>
</tr>
<tr class="odd">
<td><strong>Alternative flow</strong> </td>
<td colspan="3"><p> </p>
<table>
<colgroup>
<col style="width: 32%" />
<col style="width: 32%" />
<col style="width: 34%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>No</strong> </th>
<th><strong>Actor</strong> </th>
<th><strong>Action</strong> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>2a. </td>
<td>software</td>
<td>Notify error: The cart is empty or notify that the inventory
quantity is insufficient and will display the inventory quantity for
each unmet product.</td>
</tr>
<tr class="even">
<td>2a.1</td>
<td>Customer</td>
<td>Update the cart</td>
</tr>
<tr class="odd">
<td>7a</td>
<td>software </td>
<td>Notify error: there are some required fields left blank or invalid
information.</td>
</tr>
<tr class="even">
<td>7a.1</td>
<td>Customer</td>
<td>Fill in the information</td>
</tr>
<tr class="odd">
<td>10a</td>
<td>Software</td>
<td><p>Notify error: no products are eligible or the delivery address
doesn't support rush order</p>
<p>delivery</p></td>
</tr>
<tr class="even">
<td>10a.1</td>
<td>Customer</td>
<td>Update the address or choose another delivery method</td>
</tr>
<tr class="odd">
<td>17a</td>
<td>Software</td>
<td>Notify error: the payment is unsucess</td>
</tr>
<tr class="even">
<td>17a.1</td>
<td>Customer</td>
<td>Complete the transaction</td>
</tr>
<tr class="odd">
<td>18a</td>
<td>Software</td>
<td>Notify that the order is not approved</td>
</tr>
<tr class="even">
<td>18b</td>
<td>Customer</td>
<td>Cancel order</td>
</tr>
<tr class="odd">
<td>18b.1</td>
<td>Software</td>
<td>Set up refund process</td>
</tr>
<tr class="even">
<td>18b.2</td>
<td>VNPay</td>
<td>Confirm refunding transaction</td>
</tr>
<tr class="odd">
<td>18b.3</td>
<td>Software</td>
<td>Notify that customer has been refunded</td>
</tr>
</tbody>
</table>
<p> <br />
 </p></td>
</tr>
<tr class="even">
<td><strong>Post condition</strong> </td>
<td colspan="3">No </td>
</tr>
</tbody>
</table>
