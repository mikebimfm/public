# public

# 01 .Net 472 MVC JSON ViewBag to View:
## Controller.cs: 
ViewBag.ImageQuerystr = JsonConvert.SerializeObject(forgeDataList, Formatting.Indented);
ViewBag.ImageQuerystr2 = (JsonConvert.SerializeObject(forgeDataList, Formatting.Indented)).ToString();

## View.cshtml:
var DataItemA = @Html.Raw(Newtonsoft.Json.JsonConvert.SerializeObject(ViewBag.ImageQuerystr2));
var DataItemB = @Html.Raw(Newtonsoft.Json.JsonConvert.DeserializeObject(ViewBag.ImageQuerystr2));
let ImageQuery = @Html.Raw(ViewBag.ImageQuerystr2);

console.log("DataItemA");
alert(DataItemA);
console.log(DataItemA);

Reference: https://blog.darkthread.net/blog/escape-script-in-json/
