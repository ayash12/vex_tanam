<template>
  <mdb-container> 
  <mdb-modal v-if="show" centered  :show ="modal" @close="show = false" scrollable>
        <mdb-modal-header>
            <mdb-modal-title>Buy Seeds</mdb-modal-title>
        </mdb-modal-header>
        <mdb-modal-body>
          <div class="row">
            <div class="col-sm-6">
              <div class="card">
                <div class="card-body">
                <img src="@/assets/seedbag.png" alt="" style="width:100px">
                <div class="container">
                  vexamania
                  <br>
                  <h6> get 1120 vex </h6>
                </div>
                  <mdb-btn color="primary" size="sm" @click.native="buySeed()">1k vex</mdb-btn>
                </div>
              </div>
            </div>
            <div class="col-sm-6">
              <div class="card">
                <div class="card-body">
                  <img src="@/assets/seedbag.png" alt="" style="width:100px">
                <div class="container">
                  vexdefi
                  <br>
                  <h6> get 1100 vex </h6>
                </div>
                   <mdb-btn color="primary" size="sm" @click.native="buySeed()">1k vex</mdb-btn>
                </div>
              </div>
            </div>
          </div>            
         
        </mdb-modal-body>
        <mdb-modal-footer>
            <mdb-btn color="primary" size="sm" @click.native="show = false">Close</mdb-btn>
        </mdb-modal-footer>
    </mdb-modal>
    <div></div>
  </mdb-container>
</template>

<script>

import { mdbModal, mdbModalHeader, mdbModalTitle, mdbModalBody, mdbModalFooter, mdbBtn, mdbRow, mdbCol, mdbContainer } from 'mdbvue';

export default {
  name: "Modal",
   components: {
      mdbModal,
      mdbModalHeader,
      mdbModalTitle,
      mdbModalBody,
      mdbModalFooter,
      mdbBtn,
      mdbRow, 
      mdbCol,
      mdbContainer
    },
  data() {
    return {
      show: false,
      counter: 0
    };
    
  },
  methods: {
    openModal() {
      this.show = !this.show;
      },
    buySeed() {
     this.counter++;
      // this.show = false;
      console.log({counter});
      }
  }
};
</script>


<style >
.col-sm-6 {
  width: 50%;
  background-color: white;
  margin-bottom: 10px;
}

.container {
  text-align: center;
  padding: 10px 10px;
}

h6 {
  font-size: 13px;
}

</style>