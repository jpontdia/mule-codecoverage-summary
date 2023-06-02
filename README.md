# mule-codecoverage-summary

Lets crate a test:

<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title>MUnit Coverage Report</title>
    <link rel="stylesheet" type="text/css" href="assets/styles/mulesoft-styles.css">
    <link rel="stylesheet" type="text/css" href="assets/styles/tsorter.css">
</head>
<body>
<div class="mulesoft-topbar">
    <div class="mulesoft-appbar">
        <div class="muleicon muleicon-logo"></div>
        <div class="anypoint-brand">MUnit Coverage Report - Mule Configuration Files</div>
    </div>
</div>
<div class="col-md-8 col-md-offset-2">
    <h2 class="text-bold">Application Coverage*</h2>
    <div class="progress">
        <span>100%</span>
        <div class="progress-bar progress-bar-success" role="progressbar" aria-valuenow="100" aria-valuemin="0"
             aria-valuemax="100" style="width: 100%;">
        </div>
    </div>
    <ul class="list-unstyled">
        <li>
            <h4><b>Required Application Coverage :</b>
            80%
            </h4>
        </li>
    </ul>
    <h2 class="text-bold">Mule Configuration Files</h2>
    <table id="resources_table" class="table table-featured table-hover sortable">
        <thead>
        <tr>
            <th colspan="2" data-tsorter="link">Resource</th>
            <th data-tsorter="numeric">#Containers</th>
            <th data-tsorter="numeric">Weight%**</th>
            <th data-tsorter="coverage">Coverage*</th>
        </tr>
        </thead>
        <tbody id="table-body">
        <tr>
            <td colspan="2"><a href=implementations/get-report.html>implementations/get.xml</a></td>
            <td>3</td>
            <td>35.14</td>
            <td>
                    <div class="progress">
                        <span>100%</span>
                        <div class="progress-bar progress-bar-success" role="progressbar" aria-valuenow="100"
                             aria-valuemin="0" aria-valuemax="100" style="width: 100%;">
                        </div>
                    </div>
            </td>
        </tr>
        <tr>
            <td colspan="2"><a href=api-report.html>api.xml</a></td>
            <td>6</td>
            <td>16.22</td>
            <td>
                    <div class="progress">
                        <span>100%</span>
                        <div class="progress-bar progress-bar-success" role="progressbar" aria-valuenow="100"
                             aria-valuemin="0" aria-valuemax="100" style="width: 100%;">
                        </div>
                    </div>
            </td>
        </tr>
        <tr>
            <td colspan="2"><a href=implementations/post-report.html>implementations/post.xml</a></td>
            <td>2</td>
            <td>35.14</td>
            <td>
                    <div class="progress">
                        <span>100%</span>
                        <div class="progress-bar progress-bar-success" role="progressbar" aria-valuenow="100"
                             aria-valuemin="0" aria-valuemax="100" style="width: 100%;">
                        </div>
                    </div>
            </td>
        </tr>
        <tr>
            <td colspan="2"><a href=implementations/delete-report.html>implementations/delete.xml</a></td>
            <td>1</td>
            <td>13.51</td>
            <td>
                    <div class="progress">
                        <span>100%</span>
                        <div class="progress-bar progress-bar-success" role="progressbar" aria-valuenow="100"
                             aria-valuemin="0" aria-valuemax="100" style="width: 100%;">
                        </div>
                    </div>
            </td>
        </tr>
        </tbody>
    </table>
    <h4>(*) Number of processors executed during test</h4>
    <h4>(**) Number of processors inside the resource over the total number of processors in the application</h4>
</div>
<script type="text/javascript" src="assets/js/tsorter.min.js"></script>
<script type="text/javascript">
    function init() {
        var sorter = tsorter.create('resources_table', 0, {
            coverage: function (row) {
                var cov = this.getCell(row).childNodes[1].childNodes[3].attributes['aria-valuenow'].textContent;
                return parseFloat(cov.substring(cov[0].length - 1), 10);
            }
        });
    }

    window.onload = init;

</script>
</body>
</html>
