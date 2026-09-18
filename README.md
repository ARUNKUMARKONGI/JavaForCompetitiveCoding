<details>
<summary><h2 style="display:inline;">🔣 Data Types, Conditional Stmts, Operators and Loops</h2></summary>
  <br>
<p>Data types are important because they determine what kind of data you can store, how much memory it uses, and what range of values it can handle.</p>
<p>For competitive coding, choosing the correct data type helps you:</p>
<ul style="margin-top:0; margin-bottom:12px; padding-left:20px;">
  <li style="margin-bottom:4px;">⚡ <strong>Avoid overflow</strong> — e.g., use <code>long</code> for very large numbers.</li>
  <li style="margin-bottom:4px;">💾 <strong>Manage memory efficiently</strong> — important for large arrays.</li>
  <li style="margin-bottom:4px;">🎯 <strong>Get correct results</strong> — especially in integer division and arithmetic.</li>
  <li style="margin-bottom:4px;">🧩 <strong>Match problem constraints</strong> — choose based on the maximum possible input value.</li>
</ul>
<p><strong>Example:</strong> If a problem says <em>n ≤ 10⁹</em>, <code>int</code> may be enough, but calculations like <em>n × n</em> can reach <em>10¹⁸</em>, so <code>long</code> is safer.</p>
<p>👉 <strong>Rule:</strong> In competitive coding, always check constraints before choosing a data type.</p>
<h3>Reference Diagram <em>(Click image to view/download full resolution)</em></h3>
<a href="./images/JavaDataTypes.png" target="_blank">
  <img src="./images/JavaDataTypes.png" alt="Java Data Types Diagram" style="max-width:100%; height:auto; display:block; margin:10px 0;"/>
</a>
</details>

<hr>

<details>
<summary><h2 style="display:inline;">🔄 Typecasting & Data Conversions</h2></summary>
  <br>
<p>In Java, <strong>Typecasting</strong> is the process of converting a value from one data type to another. Mastering both <strong>Implicit (Widening)</strong> and <strong>Explicit (Narrowing)</strong> conversions is essential for mathematical accuracy, preventing hidden logic bugs, and avoiding runtime errors.</p>
<h3>Why Data Conversions Matter in Competitive Coding & Math</h3>
<ul style="margin-top:0; margin-bottom:12px; padding-left:20px;">
  <li style="margin-bottom:8px;">
    <strong>Preventing Loss of Precision in Integer Division:</strong><br>
    In Java, dividing two integers always yields an integer (e.g., <code>5 / 2</code> evaluates to <code>2</code>, not <code>2.5</code>). In competitive programming math problems (like computing averages or probabilities), failing to cast at least one operand to <code>double</code> (e.g., <code>(double) 5 / 2</code>) causes truncation errors.
  </li>
  <li style="margin-bottom:8px;">
    <strong>Avoiding Intermediate Overflow During Arithmetic:</strong><br>
    When multiplying two large <code>int</code> values, the result is calculated as an <code>int</code> <em>before</em> being assigned to a destination variable. If the product exceeds 2 × 10⁹, it silently overflows into a negative value—even if assigned to a <code>long</code>.
    <ul style="margin-top:4px; margin-bottom:4px; padding-left:20px;">
      <li style="margin-bottom:2px;">❌ <strong>Incorrect:</strong> <code>long total = a * b;</code> <em>(overflow occurs during multiplication)</em></li>
      <li style="margin-bottom:2px;">✅ <strong>Correct:</strong> <code>long total = (long) a * b;</code> <em>(forces 64-bit precision)</em></li>
    </ul>
  </li>
  <li style="margin-bottom:8px;">
    <strong>Safe Downcasting & Range Truncation:</strong><br>
    Explicitly casting a larger type to a smaller type (e.g., <code>long</code> to <code>int</code>) clips high-order bits via modulo arithmetic. While useful in bitwise optimizations, unintended narrowing leads to unexpected negative numbers.
  </li>
</ul>
<h3>Reference Diagram <em>(Click image to view/download full resolution)</em></h3>
<a href="./images/typecasting.png" target="_blank">
  <img src="./images/typecasting.png" alt="Java Typecasting Diagram" style="max-width:100%; height:auto; display:block; margin:10px 0;"/>
</a>
</details>

---

<details>
<summary><h2 style="display:inline;">🛠️ Java Important Library Functions (Math, Strings, Arrays & Collections)</h2></summary>
<br>

<p>Java library functions provide pre-built, optimized methods for common tasks, allowing you to solve problems faster and write cleaner code.</p>
<ul>
  <li>⚡ <strong>Save Time</strong> — Avoid implementing common operations from scratch.</li>
  <li>🧩 <strong>Simplify Code</strong> — Functions like <code>sort()</code>, <code>max()</code>, <code>min()</code>, and <code>binarySearch()</code> reduce complexity.</li>
  <li>🚀 <strong>Improve Efficiency</strong> — Built-in library methods are well-tested and highly optimized.</li>
  <li>🛠️ <strong>Reduce Bugs</strong> — Using reliable built-in methods minimizes implementation errors.</li>
  <li>📚 <strong>Useful Data Structures</strong> — Includes <code>Math</code>, <code>String</code>, <code>Character</code>, <code>Arrays</code>, <code>ArrayList</code>, <code>HashMap</code>, <code>HashSet</code>, etc.</li>
  <li>🎯 <strong>Competitive Advantage</strong> — Allows you to focus on core algorithms rather than low-level implementations.</li>
</ul>
<p>👉 <strong>Rule:</strong> In competitive coding, know commonly used Java library functions and their asymptotic time complexities.</p>


<h3>Reference Diagram <em>(Click image to view/download full resolution)</em></h3>

<a href="./images/JavaLibraryFunctions.png" target="_blank">
  <img src="./images/JavaLibraryFunctions.png" alt="Java Built-in Libraries and Methods Cheat Sheet" style="max-width:100%; height:auto; display:block; margin:10px 0;"/>
</a>

</details>

---

<details>
<summary><h2 style="display:inline;">📊 Java Arrays</h2></summary>
<br>
<p>Arrays are one of the most fundamental data structures in competitive coding. They allow you to store and efficiently access multiple values using an index.
</p>
  
<ul>
  <li>⚡ <strong>Fast Access</strong> — Elements can be accessed directly using an index in <code>O(1)</code> time.</li>
  <li>💾 <strong>Efficient Storage</strong> — Stores multiple values of the same data type in contiguous memory locations.</li>
  <li>🔄 <strong>Easy Traversal</strong> — Ideal for processing sequential data using standard loops.</li>
  <li>🧩 <strong>Foundation for Algorithms</strong> — Search, sort, prefix sums, and two pointers rely heavily on arrays.</li>
  <li>🚀 <strong>Better Performance</strong> — Arrays provide predictable memory layout and fast cache access.</li>
  <li>🎯 <strong>Versatile Application</strong> — Commonly used for strings, matrices, frequency counting, and dynamic programming.</li>
</ul>

<p>👉 <strong>Rule:</strong> In competitive coding, master array indexing, traversal, searching, sorting, and common multi-pointer techniques thoroughly.</p>

<br>
<h3>Reference Diagram <em>(Click image to view/download full resolution)</em></h3>

---

<a href="./images/JavaArray.png" target="_blank">
  <img src="./images/JavaArray.png" alt="Java Typecasting Diagram" style="max-width:100%; height:auto; display:block; margin:10px 0;"/>
</a>

</details>

---

<details>
<summary><h2 style="display:inline;">Java Collections Framework</h2></summary>
<br>

<p>
The Java Collections Framework provides a set of interfaces and classes for storing, organizing, and manipulating groups of objects efficiently. It is essential for competitive coding because it provides ready-to-use data structures with optimized operations.
</p>

<ul>
  <li>⚡ <strong>Dynamic Storage</strong> — Collections can grow and shrink dynamically, unlike fixed-size arrays.</li>

  <li>🔑 <strong>Fast Data Access</strong> — Hash-based collections such as <code>HashSet</code> and <code>HashMap</code> provide average <code>O(1)</code> time for common operations.</li>

  <li>🔄 <strong>Maintain Order</strong> — <code>ArrayList</code> and <code>LinkedHashSet</code>/<code>LinkedHashMap</code> can maintain insertion order.</li>

  <li>🎯 <strong>Unique Elements</strong> — <code>HashSet</code>, <code>LinkedHashSet</code>, and <code>TreeSet</code> automatically prevent duplicate elements.</li>

  <li>🔢 <strong>Key-Value Storage</strong> — <code>HashMap</code>, <code>LinkedHashMap</code>, and <code>TreeMap</code> store data in key-value pairs with unique keys.</li>

  <li>📈 <strong>Sorted Data</strong> — <code>TreeSet</code> and <code>TreeMap</code> maintain elements/keys in sorted order using a Red-Black Tree.</li>

  <li>🧩 <strong>Ready-to-Use Methods</strong> — Methods such as <code>add()</code>, <code>remove()</code>, <code>contains()</code>, <code>put()</code>, <code>get()</code>, and <code>containsKey()</code> simplify problem solving.</li>

  <li>🚀 <strong>Efficient Problem Solving</strong> — Collections are widely used for frequency counting, duplicate detection, grouping, searching, sorting, and maintaining relationships between data.</li>
</ul>

<p>
👉 <strong>Rule:</strong> In competitive coding, understand when to use <code>ArrayList</code>, <code>HashSet</code>, <code>LinkedHashSet</code>, <code>TreeSet</code>, <code>HashMap</code>, <code>LinkedHashMap</code>, and <code>TreeMap</code> based on ordering, uniqueness, sorting, and time-complexity requirements.
</p>

<br>

<h3>Key Collections at a Glance</h3>

<ul>
  <li><strong>ArrayList</strong> → Ordered + duplicates allowed + index-based access</li>
  <li><strong>HashSet</strong> → Unique elements + no guaranteed order</li>
  <li><strong>LinkedHashSet</strong> → Unique elements + insertion order</li>
  <li><strong>TreeSet</strong> → Unique elements + sorted order+ <code>O(log n)</li>
  <li><strong>HashMap</strong> → Key-value pairs + no guaranteed order + average <code>O(1)</code></li>
  <li><strong>LinkedHashMap</strong> → Key-value pairs + insertion order</li>
  <li><strong>TreeMap</strong> → Key-value pairs + sorted keys + <code>O(log n)</code></li>
</ul>

<br>

<h3>Reference Diagram <em>(Click image to view/download full resolution)</em></h3>

---

<a href="./images/Collections.png" target="_blank">
  <img src="./images/Collections.png" alt="Java Collections Framework Important Classes" style="max-width:100%; height:auto; display:block; margin:10px 0;"/>
</a>

</details>




