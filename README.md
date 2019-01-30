# Data-Transaction
Data transaction by using struct array
pragma solidity >=0.4.2;
contract Struct {
    struct pardhu {
        uint number;
        string name;
        uint age;
    }
    mapping (uint=>pardhu) c;
    
    uint[] public accounts;
    function setStruct(uint indx,uint x, string memory a, uint y) public {
     pardhu storage prd= c[indx]; 
     prd.number = x;
     prd.name = a;
     prd.age = y;
     accounts.push(indx)-1;
     }
     function getStruct(uint indx) public view returns(uint,string memory,uint) {
         return(c[indx].number,c[indx].name,c[indx].age);
     }
          function membersLength() public view returns(uint){
              return accounts.length;
          }
   }
