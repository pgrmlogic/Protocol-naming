<!DOCTYPE html>
<html>
<body>

<h1>Protocol Manager Naming</h1>
<h3>Non R0</h3>

<function NonR0()>


    <form id="myForm" class="form">
  

        <label for="WorkFlow">Choose A WorkFlow:</label>
            <select name="WorkFlow" id="WorkFlow">
                <option value=""></option>
                <option value="RC_">Rapid Cycle</option>
                <option value="eSDI_">eSDI</option>
                <option value="SS_">Standard Short Day</option>
                <option value="ST_">Standard Seed Production</option>
                <option value="FL_">Fly Protocol</option>
                <option value="NF_">No Flies</option>
                <option value="EXP_">Expirimental Protocol</option>
                <option value="BIO_"> Bioassay</option>
                <option value="PROP_">Propagation Only</option>
            </select>

    <br><br>

        <label for="Project">Choose A Project:</label>
            <select name="Project" id="Project">
                <option value=""></option>
                <option value="LEP-">Any Lep Project</option>
                <option value="CRW-">Any CRW Project</option>
                <option value="COL-">Any Coleop</option>
                <option value="HT-">Any Ht Project</option>
                <option value="GE-">Gene Editing</option>
                <option value="YLD-">Any Yield Project</option>
                <option value="BG-">Any Bollgard Project</option>
                <option value="HD-">Any Hemipteran Project</option>
                <option value="DT-">Disease Traits</option>
                <option value="SIP-">Any Soy Insect Protection Projects</option>
                <option value="MIC-">Any Microbial Project</option>
                <option value="SI-">System Improvements</option>
                <option value="TST-">Trait Stacking Technologies</option>
            </select>

    <br><br>

        <label for="VCR">VCR Number:</label>
        <input type="number" id="VCR" name="VCR" required>

    <br><br>

        <label for="ChipScar">Chipped Or Scarified?:</label>
            <select name="ChipScar" id="ChipScar">
                <option value="">None</option>
                <option value="_CH">Chipped</option>
                <option value="_SC">Scarified</option>
      
            </select>

    <br><br>

        <input type="submit" name="Non R0" id="nonR0Btn">
        <input type="reset" value="Reset">
    

    </form>
        <div class="overlay-bg1"> 
            <div>     
        
                <h3>Your Protocol Name:</h3>
                <p id="nonR0content"></p>
                <button class="close-btn1">Close</button>
        
            </div>
        </div>
 <br><br>

    <script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>
  <script>

    $(document).ready(function(){

        $(".overlay-bg1").hide();

        $("#nonR0Btn").on("click", function(even){
            even.preventDefault();
            var workInfo = $("#WorkFlow").val();
            var proInfo = $("#Project").val();
            var vcrInfo = $("#VCR").val();
            var csInfo = $("#ChipScar").val();
            $("#nonR0content").text("");
            $("#nonR0content").append( workInfo + proInfo + vcrInfo + csInfo);
            $(".overlay-bg1").show();
        });

            $(".close-btn1").on("click", function(){
            $(".overlay-bg1").hide();
            });

    });

  </script>

</function>

<function R0()>
<h3>R0</h3>

<form id="nyForm" class="form">
    <label for="crop">Choose A Crop</label>
    <select name="crop" id="crop">
        <option value=""></option>
        <option value="TA">Wheat</option>
        <option value="ZM">Corn</option>
        <option value="GH">Cotton</option>
        <option value="GM">Soy</option>
        <option value="BN">Canola</option>
    </select>
    
    <br><br>

    <label for="site">Enter The First Letter Of The Site:</label>
    <input type="text" id="site" name="site" pattern="[A-Z]{1}" title="Two Letter Code" required>

    <br><br>

    <label for="year">Enter The Calendar Year:</label>
    <input type="number" id="year" name="year" pattern=".{2,}" title="Two Digit Number" required>

    <br><br>

    <label for="control">Is It A Control:</label>
    <select name="control" id="control">
        <option value="">No</option>
        <option value="Control">Yes</option>
    </select>

    <br><br>

    <input type="submit" name="submit" id="r0Btn">
    <input type="reset" value="Reset">

</form>
    <div class="overlay-bg2"> 
     <div>     
      
      <h3>Your Protocol Name:</h3>
      <p id="r0Content"></p>
      <button class="close-btn2">Close</button>
      
     </div>
    </div>

<br><br>

    <script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>
    <script>

        $(document).ready(function(){

        $(".overlay-bg2").hide();

        $("#r0Btn").on("click", function(even){
            even.preventDefault();
            var cropInfo = $("#crop").val();
            var siteInfo = $("#site").val();
            var yearInfo = $("#year").val();
            var conInfo = $("#control").val();
    
            $("#r0Content").text("");
            $("#r0Content").append( cropInfo + siteInfo + yearInfo + conInfo);
            $(".overlay-bg2").show();
        });

            $(".close-btn2").on("click", function(){
            $(".overlay-bg2").hide();
            
            });
        });


</script>

</function>

<function Donor()>

    <h3>Donor/Female</h3>

    <form id="xzForm" class="form">

        <label for="donFem">Donor Or Female</label>
        <select name="donFem" id="donFem">
            <option value=""></option>
            <option value="DM">Donor</option>
            <option value="FS">Female</option>
        </select>

    <br><br>

        <label for="year">Enter The Calendar Year:</label>
        <input type="number" id="year2" name="year2" pattern=".{2,}" title="Two Digit Number" required>

    <br><br>

        <label for="pedigree">Enter The Pedigree</label>
        <input type="text" id="pedigree" name="pedigree"></input>

    <br><br>

        <input type="submit" name="submit" id="submitBtn3">
        <input type="reset" value="Reset">

    </form>
    <div class="overlay-bg3"> 
        <div>     
         
         <h3>Your Protocol Name:</h3>
         <p id="doncontent"></p>
         <button class="close-btn3">Close</button>
         
        </div>
    </div>

    <br><br>

    <script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>
    <script>

        $(document).ready(function(){

        $(".overlay-bg3").hide();

        $("#submitBtn3").on("click", function(even){
            even.preventDefault();
            var dFInfo = $("#donFem").val();
            var pedInfo = $("#pedigree").val();
            var year2Info = $("#year2").val();
    
            $("#doncontent").text("");
            $("#doncontent").append( dFInfo +"CE"+ year2Info + "_" + pedInfo);
            $(".overlay-bg3").show();
        });

            $(".close-btn3").on("click", function(){
            $(".overlay-bg3").hide();
            
            });
        });


    </script>


    
</function>

</body>
<h6>If there are any revisions or questions please contact me at brandon.schmidt@bayer.com</h6>
</html>

<!-- Created by Brandon Schmidt 1/6/2021 If there are any revisions or questions please contact me at brandon.schmidt@bayer.com -->