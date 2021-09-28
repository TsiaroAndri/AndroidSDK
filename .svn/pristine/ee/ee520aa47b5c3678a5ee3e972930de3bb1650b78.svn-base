function getSearchParameters() {
    var prmstr = window.location.search.substr(1);
    return prmstr != null && prmstr != "" ? transformToAssocArray(prmstr) : {};
}

function transformToAssocArray( prmstr ) {
    var params = {};
    var prmarr = prmstr.split("&");
    for ( var i = 0; i < prmarr.length; i++) {
        var tmparr = prmarr[i].split("=");
        params[tmparr[0]] = decodeURIComponent(tmparr[1]);
    }
    return params;
}

(function(){
    var params = getSearchParameters()
    //var src = "https://www.ultimedia.com/deliver/generic/iframe/mdtk/{mdtk}/src/{src}/zone/{zone}/showtitle/1/gdprconsentstring/{gdprconsentstring}/urlfacebook=[URL_REFERER]&tagparamdecoded={tagparamdecoded}";
    var src = "https://www.ultimedia.com/deliver/generic/iframe/mdtk/{mdtk}/src/{src}/zone/{zone}/showtitle/1/gdprconsentstring/BOj8iv4Oj8iwYAHABAlxCS-AAAAnF7_______9______9uz_Ov_v_f__33e87_9v_l_7_-___u_-3zd4-_1vf99yfm1-7etr3tp_87ues2_Xur__59__3z3_9phPrsk89r633A/urlfacebook=[URL_REFERER]&tagparamdecoded=video_app&sa=D&ust=1586938702508000&usg=AOvVaw0EoSE28fXl4HfVg-fQrA4n";
    
    var url = src.replace(/\{([\w]+)\}/g, function(match, val){
      if(val == 'src' && !params[val]) return 'default';
  
      return params[val];
    })
    var node = document.getElementById("frame");
    var source = document.createAttribute("src");
    source.value = url;
    node.setAttributeNode(source);
    console.log(node.getAttribute("src"))
  })()
