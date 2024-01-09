<script>
    import './styles.css'; // Import the CSS file

    let text = '';
  
    // Function to check if the text is a palindrome
    function isPalindrome(str) {
      const cleaned = str.replace(/[\W_]/g, '').toLowerCase();
      const reversed = cleaned.split('').reverse().join('');
      return cleaned === reversed;
    }
  </script>
<div class="container">
  <!-- Input field for the user to enter text -->
  <input type="text" bind:value={text} class="input-field" placeholder="Enter text to check" />
  
  <!-- Display the result -->
  <p class="{text ? 'result-text' : ''}">
    {#if text}
      "{text}" is {isPalindrome(text) ? '' : 'not '}a palindrome.
    {/if}
  </p>
</div>
  