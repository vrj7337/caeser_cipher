# caeser_cipher
function rot13(str){
     let decodeRes = "";
     let alStart = "abcdefghijklm".toUpperCase;
     let alEnd   = "nopqrstuvwxyz".toUpperCase;
   
   for(let i = 0; i < str.length ; i++){
     let letterToCode = str[i];
   if(alStart.indexOf(letterToCode) >= 0){
      decodeRes += alEnd[alStart.indexOf(letterToCode)];   
    }else if (alEnd.indexOf(letterToCode) >= 0){
      decodeRes += alStart[alEnd.indexOf(letterToCode)];
    }else{
      decodeRes += letterToCode;
    } 
  }
  return decodeRes;
}

let Res = rot13("SERR PBQR PNZC");
console.log(res);
