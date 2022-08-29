``` solidity
// before
function addressInternalBalance() public returns (uint256) {
        return address(this).balance;
}

// after
returns (uint256) {
  assembly {
      let c := selfbalance()
      mstore(0x00, c)
      return(0x00, 0x20)
  }
}


// before
function addressExternalBalance(address addr) public {
      uint256 bal = address(addr).balance;
}
   
// after
function assemblyExternalBalance(address addr) public {
    uint256 bal;
    assembly {
        bal := balance(addr)
    }
}
```
