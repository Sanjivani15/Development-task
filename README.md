# Development-task
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Interactive Boxes</title>
<style>
  .box {
    width: 300px;
    border: 2px solid pink;
    margin: 20px auto;
    padding: 20px;
    transition: height 0.3s ease;
  }
  h6{
    color:crimson;
    font-family: sans-serif;
    margin: 10px auto;
    text-align: center;
    font-size: 30px;
    max-width: 300px;
   position:sticky;
  }
  button{
    width: 200px;
  }

 .Delivery{
    text-align:center;
 }
 .box+input[type="radio"]{
    display: none;
 }
 .box+input[type="radio"]:checked{
    max-height: 400px;
 }
 


</style>
</head>
<body>
    <h6>YAY! It's BOGO</h6>
<div class="box" onclick="expandBox(1)">

  <table>
    <tr>
        <td><input type="radio" name="unit1" value="1unit" checked></td>

        <td><label for="first"> 1 Unit </label></td>
        <td id="item" bgcolor="pink"> 10% off </td>
        <td>     </td>
        <td>$10:00 USD</td>
    </tr>

    <tr>
        <td> </td>
        <td colspan="2" >Standard Price</td>
        <td> </td>
        <td> <del>$24:00 USD </del></td>
    </tr>
</table>
</div>


<div class="box" onclick="expandBox(2)">
    <table>
        <tr>
            <td><input type="radio" name="unit2" value="2unit"></td>
    
            <td><label for="first"> 2 Unit </label></td>
            <td bgcolor="pink"> 20% off </td>
            <td>     </td>
            <td>$18:00 USD</td>
        </tr>
    
        <tr>
            <td> </td>
            <td colspan="2" ></td>
            <td> </td>
            <td> <del>$24:00 USD </del></td>
        </tr>
    </table>
<br>
<Table>
    <tr>
    <th>   </th>
    <th> Size </th>
    <th> Color </th>
    </tr>
    <tr>
        <td>#1</td>
        <td>
<form>
    <select name="size" id="Size">
        <option value="S">S</option>
        <option value="L">L</option>
        <option value="XL">XL</option>
    </select>
</form>
</td>
<td>
    <form>
        <select name="Color" id="Color">
            <option value="B">Color</option>
            <option value="B">Black</option>
            <option value="w">White</option>
            <option value="G">Gray</option>
        </select>
    </form>
</td>
</tr>   
<tr>
<td>#2</td>
<td>
<form>
<select name="size" id="Size">
<option value="S">S</option>
<option value="L">L</option>
<option value="XL">XL</option>
</select>
</form>
</td>
<td>
<form>
<select name="Color" id="Color">
<option value="B">Black</option>
<option value="w">White</option>
<option value="G">Gray</option>
</select>
</form>
</td>
</tr>   
</table>
</div>
<div class="box" onclick="expandBox(3)">
    <table>
        <tr>
            <td><input type="radio" name="unit3" value="3unit"></td>
    
            <td><label for="first"> 3 Unit </label></td>
            <td bgcolor="pink"> 30% off </td>
            <td>     </td>
            <td>$24:00 USD</td>
        </tr>
    
        <tr>
            <td> </td>
            <td colspan="2" ></td>
            <td> </td>
            <td> $24:00 USD</td>
        </tr>
    </table>
</div>
<br> 
<div class="Delivery">
<p>Free Delivery.      Total:$18.00 USD   </p>
</div>
<div class="Delivery">
<button type="submit" id="btn"> Add to cart</button>

</div>
<script>
  function expandBox(boxNumber) {
    var box = document.getElementsByClassName('box')[boxNumber - 1];
    if (box.style.height === 'auto' || box.style.height === '') {
      box.style.height = box.scrollHeight + 'px';
    } else {
      box.style.height = 'auto';
    }
  }

  function addToCart(boxNumber) {
    var units = document.querySelector('input[name="unit' + boxNumber + '"]:checked').value;
    alert('Added ' + units + ' to cart!');
  }
</script>

</body>
</html>
