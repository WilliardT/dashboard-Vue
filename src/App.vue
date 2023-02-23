<template>
  <div class="appWrapper">
    <header>
      <div class="logoD">
        <div class="d">D</div>
        <div class="textLogo">Dashboard</div>
        <div class="rightControls">
          <div class="help">
            <span>Help</span>
            <img src="./assets/icons/que.png" alt="arrow" />
          </div>
          <div class="buttonHeader">
            <span>Upgrade</span>
          </div>
          <img src="./assets/icons/avatar.png" alt="avatar" />
        </div>
      </div>
    </header>
    <div class="marksWrapper">
      <div class="marks">
        <div class="marksActive">Analyze</div>
        <div class="marksDisable">My campaigns</div>
        <div class="marksDisable">Configure</div>
      </div>
    </div>
    <div class="content">
      <div class="leftMenuWrapper">
        <div class="buttonNew">
          <img src="./assets/icons/plus.png" alt="plus" />
          <span>Create new</span>
        </div>
        <div class="sortWrapper">
          <div class="typeSortDisable">
            <img src="./assets/icons/round.png" alt="round" />
            <span>Even rows of data</span>
            <p>Display rows 2,4,6 etc</p>
          </div>
          <div class="typeSortDisable">
            <img src="./assets/icons/check.png" alt="check" />
            <span>Odd rows of data</span><br>
            <p>Display rows 1,3,5 etc</p>
          </div>
          <div class="typeSortActive">
            <img src="./assets/icons/print.png" alt="print" />
            <span>All data</span>
            <p>Display all data</p>
          </div>
        </div>
      </div>
      <div class="rightTableWrapper">
        <div class="headerTableWrapper">
          <div class="headerTable">
            <h4>Dashboard</h4>
            <div class="itemsWrapper">
              <div class="dateWrapper">
                <p>Aug 21, 2021 · Sep 21 2021</p>
                <img src="./assets/icons/down.png" alt="down" />
              </div>
              <div class="iconsHeaderTable">
                <img src="./assets/icons/print.png" alt="print" />
              </div>
              <div class="iconsHeaderTable">
                <img src="./assets/icons/arrow.png" alt="download" />
              </div>
            </div>
          </div>
        </div>
        <div class="tableWrapper">
          <section>
            <Table />
          </section>
        </div>
        <input type="text" placeholder="search..." v-model="searchValue">
      </div>
    </div>
  </div>
</template>

<script>
import Table from "@/components/Table.vue";

export default {
  name: "table",
  components: {
    Table,
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Racing+Sans+One&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Racing+Sans+One&family=Roboto&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@500&family=Racing+Sans+One&family=Roboto&display=swap");

* {
  margin: 0;
  padding: 0;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.appWrapper {
  position: absolute;
  margin-top: 5%;
  width: 1440px;
  height: 574px;
  background-color: #e2f0f0;
  box-shadow: 0px 33px 43px rgba(0, 0, 0, 0.1),
    0px 9.94853px 12.9632px rgba(0, 0, 0, 0.0651589),
    0px 4.13211px 5.38427px rgba(0, 0, 0, 0.05),
    0px 1.4945px 1.94738px rgba(0, 0, 0, 0.0348411);
  border-radius: 20px;
}

header {
  background: #ffffff;
  width: 1440px;
  height: 64px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logoD {
  width: 40px;
  height: 40px;
  background: #ffffff;
  box-shadow: 0px 2px 6px rgba(8, 35, 48, 0.16),
    0px 1px 2px rgba(8, 35, 48, 0.24);
  border-radius: 10px;
  display: flex;
  margin-left: 12px;
}

.d {
  font-family: "Racing Sans One";
  font-style: normal;
  font-weight: 400;
  font-size: 24px;
  line-height: 28px;
  display: flex;
  align-items: center;
  text-align: center;
  letter-spacing: 0.15px;
  color: #367bf5;
  text-shadow: 0px 16px 24px rgba(54, 123, 245, 0.16),
    0px 6px 12px rgba(54, 123, 245, 0.16);
  margin-left: 30%;
}

.textLogo {
  font-family: "Racing Sans One";
  font-style: normal;
  font-weight: 400;
  font-size: 24px;
  line-height: 28px;
  display: flex;
  align-items: center;
  letter-spacing: 0.15px;
  color: #5e6366;
  margin-left: 60%;
}

.help {
  background: #f7f9fa;
  border-radius: 10px;
  width: 96px;
  height: 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  cursor: pointer;
}

.help > span {
  font-family: "Roboto";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  display: flex;
  align-items: center;
  letter-spacing: 0.44px;
  color: #5e6366;
  margin-left: 8px;
}

.help > img {
  width: 20px;
  height: 20px;
  margin-right: 8px;
}

.rightControls {
  width: 320px;
  height: 40px;
  left: 1048px;
  top: 12px;
  display: flex;
  margin-left: 975px;
}

.buttonHeader {
  background: #ffffff;
  box-shadow: 0px 4px 8px rgba(54, 123, 245, 0.16),
    0px 2px 4px rgba(54, 123, 245, 0.24);
  border-radius: 10px;
  width: 96px;
  height: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 16px;
  margin-right: 16px;
  cursor: pointer;
}

.buttonHeader > span {
  font-family: "Roboto";
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 16px;
  display: flex;
  align-items: center;
  text-align: center;
  letter-spacing: 0.75px;
  text-transform: uppercase;
  color: #367bf5;
}

.marksWrapper {
  background: #ffffff;
  height: 56px;
  width: 100%;
  position: absolute;
}

.marks {
  display: flex;
  justify-content: center;
  align-items: center;
}

.marks > div {
  margin-right: 6px;
  padding: 8px;
  margin-top: 15.5px;
  cursor: pointer;
}

.marksActive {
  border: 1px solid #c6cacc;
  border-bottom: 0;
  border-radius: 4px 4px 0px 0px;
  font-family: "Roboto";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  display: flex;
  align-items: center;
  text-align: center;
  letter-spacing: 0.44px;
  color: rgba(0, 0, 0, 0.87);
}

.marksDisable {
  font-family: "Roboto";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  display: flex;
  align-items: center;
  text-align: center;
  letter-spacing: 0.44px;
  color: #5e6366;
}

.content {
  display: flex;
}

.leftMenuWrapper {
  width: 30%;
  height: 455px;
  margin-top: 56px;
}

.rightTableWrapper {
  width: 70%;
  height: 455px;
  margin-top: 56px;
}

.headerTableWrapper {
  display: flex;
  align-items: center;
  height: 60px;
}

.headerTable {
  display: flex;
}

.headerTable > h4 {
  font-family: "Quicksand";
  font-style: normal;
  font-weight: 500;
  font-size: 34px;
  line-height: 42px;
  display: flex;
  align-items: center;
  letter-spacing: 0.25px;
  color: rgba(0, 0, 0, 0.87);
  margin-left: 10px;
}

.itemsWrapper {
  display: flex;
  margin-top: 7px;
  margin-left: 393px;
}

.dateWrapper {
  border: 1px solid #c6cacc;
  border-radius: 10px;
  height: 32px;
  width: 232px;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  cursor: pointer;
}

.dateWrapper > p {
  font-family: "Roboto";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  display: flex;
  align-items: center;
  letter-spacing: 0.25px;
  color: rgba(0, 0, 0, 0.87);
}

.dateWrapper > img {
  width: 10px;
  height: 5px;
}

.iconsHeaderTable {
  background: #f7f9fa;
  border-radius: 4px;
  width: 32px;
  height: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-left: 8px;
  cursor: pointer;
}

.tableWrapper {
  width: 100%;
  height: 87%;
}

.buttonNew {
  position: absolute;
  left: 85px;
  right: 0.43px;
  top: 142px;
  bottom: 0px;
  background: #ffffff;
  box-shadow: 0px 16px 24px rgba(54, 123, 245, 0.16),
    0px 6px 12px rgba(54, 123, 245, 0.16);
  border-radius: 99px;
  width: 213px;
  height: 58px;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  cursor: pointer;
}

.buttonNew > span {
  font-family: "Quicksand";
  font-style: normal;
  font-weight: 500;
  font-size: 20px;
  line-height: 28px;
  display: flex;
  align-items: center;
  letter-spacing: 0.15px;
  color: #367bf5;
  margin-left: -25px;
}

.sortWrapper {
  position: absolute;
  top: 236px;
  left: 102px;
}

.typeSortActive > span, .typeSortDisable > span {
  font-family: 'Quicksand';
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 24px;
  letter-spacing: 0.44px;
  color: rgba(0, 0, 0, 0.87);
}

.typeSortActive > p, .typeSortDisable > p {
  font-family: 'Roboto';
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 16px;
  display: flex;
  align-items: flex-end;
  letter-spacing: 0.4px;
  color: #5E6366;
}

.typeSortActive > img, .typeSortDisable > img {
  margin-right: 5px;
  width: 15px;
}

.typeSortDisable {
  border-radius: 10px;
  width: 280px;
  height: 56px;
  cursor: pointer;
}

.typeSortActive {
  background: #e6efff;
  border-radius: 10px;
  width: 280px;
  height: 56px;
  cursor: pointer;
}

input {
  border: 1px solid #C6CACC;
  border-radius: 10px;
  width: 330px;
  height: 32px;
  font-family: 'Roboto';
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.25px;
  position: absolute;
  top: 500px;
  background: none;
  padding-left: 10px;
}

</style>
