<script>
  import {createEventDispatcher} from 'svelte'
  let value = 'select';

  const dispatch = createEventDispatcher()

  const onChange = (e) => {
    value = e.currentTarget.value
    dispatch('course-select', value)
  }
</script>

    <p>Give review for the course : {value || 'select'} </p>
    <ul class="course">
      <li>
        <input type="radio" id="num1" name="course" value="cs f211" on:change={onChange} checked={value===1} />
        <label for="num1">cs f211 - Object oriented Programming</label>
      </li>
      <li>
        <input type="radio" id="num2" name="course" value="cs f212" on:change={onChange} checked={value===2} />
        <label for="num2">cs f212 - Logic in CS</label>
      </li>
      <li>
        <input type="radio" id="num3" name="course" value="cs f213" on:change={onChange} checked={value===3} />
        <label for="num3">cs f213 - Discrete Structures for CS</label>
      </li>
   
    </ul>
    
