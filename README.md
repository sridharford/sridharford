- 👋 Hi, I’m @sridharford
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
sridharford/sridharford is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
/*
This is the script which can find cost spent on Zomato.com
Step 1: Visit Zomato.com, 'Profile' and click on 'Order History'
Step 2: Load all the orders by scrolling down and clicking on 'Load more' until it appears
Step 3: Run below script in Console (CTRL + SHIFT + I or CTRL + ALT + I) by copying/pasting after '>>' and press ENTER
*/

costs = $('.cost b').get()
cost_regex = /\d+.\d*/g
total_cost = 0
for (cost in costs) {
    if (costs[cost].innerHTML.match(cost_regex)) {
        cost_in_int = parseInt(costs[cost].innerHTML.match(cost_regex)[0])
        total_cost += cost_in_int
    }
}
console.log('Total ', total_cost, ' spent on Zomato!')
