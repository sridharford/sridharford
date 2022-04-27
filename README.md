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
