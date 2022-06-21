<script>
  let result = "0";

  function display(value) {
    result += value;
  }

  function calculate() {
    var p = result.replace(/^0+/, "");
    var q = eval(p);
    result = q;
  }
</script>

<main>
  <table class="calculator">
    <tr>
      <td colspan="5">
        <div class="display-box">{result}</div>
      </td>
    </tr>

    <tr>
      <td>
        <input
          class="button"
          type="button"
          value="7"
          on:click={(e) => display("7")}
        />
      </td>
      <td>
        <input
          class="button"
          type="button"
          value="8"
          on:click={(e) => display("8")}
        />
      </td>
      <td>
        <input
          class="button"
          type="button"
          value="9"
          on:click={(e) => display("9")}
        />
      </td>
      <td>
        <input
          class="button"
          type="button"
          value="+"
          on:click={(e) => display("+")}
        />
      </td>
    </tr>
    <tr>
      <td>
        <input
          class="button"
          type="button"
          value="4"
          on:click={(e) => display("4")}
        />
      </td>
      <td>
        <input
          class="button"
          type="button"
          value="5"
          on:click={(e) => display("5")}
        />
      </td>
      <td>
        <input
          class="button"
          type="button"
          value="6"
          on:click={(e) => display("6")}
        />
      </td>
      <td>
        <input
          class="button"
          type="button"
          value="-"
          on:click={(e) => display("-")}
        />
      </td>
    </tr>
    <tr>
      <td>
        <input
          class="button"
          type="button"
          value="1"
          on:click={(e) => display("1")}
        />
      </td>
      <td>
        <input
          class="button"
          type="button"
          value="2"
          on:click={(e) => display("2")}
        />
      </td>
      <td>
        <input
          class="button"
          type="button"
          value="3"
          on:click={(e) => display("3")}
        />
      </td>
      <td>
        <input
          class="button"
          type="button"
          value="*"
          on:click={(e) => display("*")}
        />
      </td>
    </tr>
    <tr>
      <td>
        <input
          class="button"
          type="button"
          value="0"
          on:click={(e) => display("0")}
        />
      </td>
      <td>
        <input
          class="button"
          type="button"
          value="."
          on:click={(e) => display(".")}
        />
      </td>
      <td>
        <input
          class="button"
          type="button"
          value="/"
          on:click={(e) => display("/")}
        />
      </td>
      <td>
        <input
          class="button"
          type="button"
          value="="
          on:click={(e) => calculate()}
          style="background-color: #FF0509;"
        />
      </td>
    </tr>
  </table>
</main>

<style>
  .calculator {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background: #fff;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.2);
    border-radius: 14px;
    padding-bottom: 20px;
    width: 320px;
  }
  .display-box {
    width: 100%;
    height: 60px;
    padding: 40px 0;
    background: #ff0509;
    border-top-left-radius: 14px;
    border-top-right-radius: 14px;
  }

  .button {
    width: 60px;
    height: 60px;
    float: left;
    padding: 0;
    margin: 5px;
    box-sizing: border-box;
    background: #ecedef;
    border: none;
    font-size: 30px;
    line-height: 30px;
    border-radius: 50%;
    font-weight: 700;
    color: #5e5858;
    cursor: pointer;
  }
</style>
