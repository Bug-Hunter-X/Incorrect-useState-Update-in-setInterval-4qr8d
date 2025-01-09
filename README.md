# Incorrect useState Update in setInterval

This repository demonstrates a common error in React applications involving the `useState` hook and `setInterval`. The problem arises when attempting to directly manipulate the state variable from within the `setInterval` callback without using the setter function provided by `useState`.

## Bug Description
The component intends to increment a counter every second. However, the counter value will not always update correctly or may even fail to update at all in certain scenarios due to improper use of the state update function.

## Bug Solution
The solution involves correctly utilizing the state update function (the second element returned by `useState`) to modify the state variable. The state update function ensures that React's rendering process is correctly triggered after each change. The updated code directly modifies the state using the setter function within the `setInterval` callback, ensuring accurate state updates and correct rendering.