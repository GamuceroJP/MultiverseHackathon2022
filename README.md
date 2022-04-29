# Intento de Markdown

1. Open the file.
2. Find the following code block on line 21:
```{.python .numberLines .lineAnchors}
def partition(my_arr, start, end):
   pivot = my_arr[end] 
   i = start -1
   for j in range(start, end):
    if my_arr[j]<=pivot:
     i=i+1
     my_arr[i], my_arr[j] = my_arr[j], my_arr[i] my_arr[i+1], my_arr[end] = my_arr[end], my_arr[i+1] return i+1
   def quicksort(my_arr, start, end):
    if start<end:
     q = partition(my_arr, start, end)
     quicksort(my_arr, start, q-1)
     quicksort(my_arr, q+1, end)
  arr = [15, 9, 11, 2 ,21,12]
  quicksort(arr, 0, 5)
  print(arr)
```
3. Update the title to match the name of your website.


> First, order the elements of `S` in any manner. We write any subset of `S` in 
the format `{γ1, γ2, ..., γn}` where `γi , 1 ≤ i ≤ n`, can take the value 
of `0` or `1`. If `γi = 1`, the `i`-th element of `S` is in the subset;
otherwise, the `i`-th element is not in the subset. Clearly the number of 
distinct subsets that can be constructed this way is `2^n` as `γi ∈ {0, 1}`.


<div id="adobe-dc-view" style="height: 360px; width: 500px;"></div>
<script src="https://documentcloud.adobe.com/view-sdk/main.js"></script>
<script type="text/javascript">
  document.addEventListener("adobe_dc_view_sdk.ready", function(){
    var adobeDCView = new AdobeDC.View({clientId: "<YOUR_CLIENT_ID>", divId: "adobe-dc-view"});
    adobeDCView.previewFile({
      content:{ location:
        { url: "https://documentcloud.adobe.com/view-sdk-demo/PDFs/Bodea%20Brochure.pdf"}},
      metaData:{fileName: "Bodea Brochure.pdf"}
    },
    {
      embedMode: "SIZED_CONTAINER"
    });
  });
</script>

