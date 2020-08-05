####implement node list

```
function Node(value) {
  this.value = value;
  this.next = null;
}
class Nodelist {
  constructor(value) {
    this.head = new Node(value);
  }
  get last() {
    var current = this.head;
    while (current.next !== null) {
      current = current.next;
    }
    return current;
  }
  get size() {
    var len = 1;
    var current = this.head;
    while (current.next !== null) {
      current = current.next;
      len += 1;
    }
    return len;
  }
  find(value) {
    var current = this.head;
    while (current !== value && current.next !== null) {
      current = current.next;
    }
    return current;
  }
  insert(value, indexValue) {
    var node = this.find(indexValue);
    var newNode = new Node(value);
    var currentNext = node.next;
    node.next = newNode;
    newNode.next = currentNext;
  }
  append(value) {
    this.last.next = new Node(value);
  }
}

```
