## Details


This function adds user data "preorder" to vertices of a connected tree.
It starts by marking vertex `root` with integer `initialRank`, and proceeds
so that the children nodes are marked with values higher than the parent.
Return value is the highest preorder rank (which is the initial preorder value
plus the number of vertices in the tree minus one).

## Notes

This function *should not* be called on graphs with cycles, it will be
caught in an infinite loop.

If called on a non-connected tree, only the connected component of the
`root` will be marked.

## Examples

```js
cy.elements().preorder(cy.$('a'), 1);

console.log('preorder rank of vertice "b": ' + cy.$('b').data('preorder'));
```
