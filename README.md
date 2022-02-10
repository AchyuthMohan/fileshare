# competition card/cardflip.css
.card-container2 {
   cursor: pointer;
   height: 250px;
   perspective: 600;
   position: relative;
   /* width: 140%; */
}
.card {
   height: 100%;
   position: absolute;
   transform-style: preserve-3d;
   transition: all 1s ease-in-out;
   width: 100%;
   background: transparent;
}
.card:hover {
   transform: rotateY(180deg);
}
.card .side {
   backface-visibility: hidden;
   border-radius: 6px;
   height: 94%;
   position: absolute;
   overflow: hidden;
   width: 100%;
  
   background: #251b419d;

   /* background-image: linear-gradient(60deg, #191629, #231831); */
}
.card .back {
   background: transparent;
   padding: 15%;
   text-align: center;
   transform: rotateY(180deg);
}
@media screen and (max-width: 600px) {
   .card {
      width: 110%;
     
   }
   .title {
      font-size: 1rem;
   }
}
@media (min-width: 1800px) and (max-width: 2070px) {
   .card-container2 {
      cursor: pointer;
      height: 300px !important;
      perspective: 600;
      position: relative;
      
   }
  
   
 
}





# competition grid/index.css

.competition-grid {
  position: relative;
  z-index: 0;
  margin-top: 4rem;
}

.category-div {
   display: none;
}
@media only screen and (max-width: 601px) {
   .competition-title {
      font-size: 41px !important;
   }
   .competition-sort-1 {
      display: flex;
      flex-direction: column !important;
   }
   .competition-sort-2 {
      display: flex;
      flex-direction: column !important;
   }
}
.competition-sort-1 {
   display: flex;
   flex-direction: row;
}
.competition-sort-2 {
   display: flex;
   flex-direction: row;
}
.sort-filter-box {
   display: grid;
   grid-template-columns: auto auto;
   justify-content: space-around;
   padding: 0.8rem 5px;
   gap: 5rem;
   margin-left: 0.5%;
   margin-right: 0.5%;
}
.drop-down-div {
   text-align: center;
   appearance: none !important;
}
.competition-grid .sort-filter-box .drop-down {
   border: 2px solid #adb5bd;
   border-radius: 5px;
   padding: 0.4rem;
   padding-right: 0.3rem;
   background-color: #100f16;
   color: white;
   float: center;
   font-size: 1rem;
}

.competition-grid .sort-filter-box .drop-down .is-selected {
   background-color: transparent !important;
   color: white !important;
}
.competition-grid .sort-filter-box .drop-down .Dropdown-option {
   text-overflow: ellipsis;
   white-space: nowrap;
   overflow: hidden;
   color: white;
}
.competition-grid .sort-filter-box .drop-down .Dropdown-option .is-selected {
   background-color: rgba(224, 173, 247, 0.637) !important;
   color: #333 !important;
}

.competition-cards-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 3rem;
  text-align: center;
  padding: 1.5rem 0;
  
}
.loading-container {
   text-align: center;
   margin-top: 8rem;
}
.loading-container .image-circle {
   opacity: 0.15;
   background-color: white;
   width: fit-content;
   margin: auto;
   padding: 1rem;
   border-radius: 9999px;
   border: 2px solid #000;
   box-shadow: 6px 6px 24px #05334e, 6px -6px 24px #7ff;
}
.loading-container .image-circle svg {
   margin: auto;
   width: 10rem;
   height: auto;
   filter: drop-shadow(10px 3px 2px rgba(0, 0, 0, 0.397));
   animation: rocket 2s ease-in-out infinite;
}
@keyframes rocket {
   0% {
      transform: translate(10px, -10px);
   }
   25% {
      transform: translate(50px, -50px);
   }
   50% {
      transform: translate(-15px, 15px);
   }
   75% {
      transform: translate(30px, -30px);
   }
   100% {
      transform: translate(10px, -10px);
   }
}
.drop-down .Dropdown-control {
   background: rgba(195, 138, 221, 0.233) !important;
   box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
   -webkit-backdrop-filter: blur(10.5px);
   backdrop-filter: blur(10.5px);
   border-radius: 10px;
   color: white;
   border: none;
   transform: scale(1.3);
   z-index: 2;
   transition: none;
   cursor: pointer;
}

@media screen and (max-width: 1700px) {
  .competition-cards-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr) !important;
   
  }
  .competition-grid {
    padding: 0 6vw;
    padding-bottom: 70px;
    
  }
}
@media screen and (max-width: 1400px) {
  .competition-cards-container {
    display: grid;
    grid-template-columns: repeat(4, 1fr) !important;
    gap: 1rem !important;
   
  }
  .competition-grid {
    padding: 0 6vw;
    padding-bottom: 70px;
  }
}
@media screen and (max-width: 1150px) {
   .competition-cards-container {
      display: grid;
      grid-template-columns: repeat(4, 1fr) !important;
   }
   .sort-filter-box {
      font-size: 0.75rem;
      display: flex;
      justify-content: center;
   }
}
@media screen and (max-width: 850px) {
   .competition-cards-container {
      display: grid;
      grid-template-columns: repeat(2, 1fr) !important;
   }
   .sort-filter-box {
      font-size: 0.75rem;
      display: flex;
      justify-content: center;
   }
   .drop-down {
      max-width: 7rem;
   }
   .competitionfilterbtn {
      display: none !important;
   }
   .category-row {
      display: flex;
      justify-content: space-around;
   }
   .category-div {
      display: flex;
      justify-content: space-around;
      margin-right: 5%;
   }
   .competition-cards-container {
      grid-template-columns: repeat(2, 1fr);
   }
}
@media screen and (max-width: 580px) {
   .competition-grid {
      padding: 0;
      padding-bottom: 70px;
   }
   .competition-cards-container {
      display: grid;
      margin-top: -5%;
      grid-template-columns: repeat(2, 1fr) !important;
      padding: 15px;
      padding-right: 24px;
   }
   .competition-card-container {
      margin-left: 10%;
      margin-right: 14%;
   }
   .sort-filter-box {
      gap: 0rem;

      margin-left: 0px;
      font-size: 11px;
      display: flex;
      justify-content: space-between;
   }
   .drop-down {
      max-width: 7rem;
      margin: 0 30px;
   }
   .compDropDown {
      margin-left: 1%;
      display: flex;
      justify-content: space-between !important;
   }
   .sort-filter-box {
      padding-left: 3%;
      padding-right: 3%;
   }
   .Dropdown-control {
      padding: 10px;
   }
   .drop-down-div {
      padding-top: 5%;
      margin-top: 3rem;
   }
}

