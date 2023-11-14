// import React, { useState } from 'react'
// import "./App.css"


// function App() {
//   const [result,setResult] = useState(null)
//   const [num1,setNum1] = useState()
//   const [num2,setNum2] = useState()

//   const handlePlus = () => {
//     const sum = num1 + num2;
//     setResult(sum);
//   };
//   const handleMinus = ()=>{
//     const sum = num1 - num2
//     setResult(sum)
//   }
//   const handleVurma = ()=>{
//     const sum = num1 * num2
//     setResult(sum);
//   }
//   const handleBolme = ()=>{
//     const sum = num1 / num2
//     setResult(sum);
//   }


//   return (
//     <div>
//       <input value={num1} type="text" onChange={(e) => setNum1(Number(e.target.value))} />
//       <input value={num2} type="text" onChange={(e) => setNum2(Number(e.target.value))}/>

//       <button onClick={handlePlus}>+</button>
//       <button onClick={handleMinus}>-</button>
//       <button onClick={handleVurma}>*</button>
//       <button onClick={handleBolme}>/</button>
//       <p>{result}</p>
//     </div>
//   )
// }

// export default App







import React from 'react'
import Card from './components/Card'

const App = () => {
  return (
    <div>
      <Card />
    </div>
  )
}

export default App



import React from 'react'
import "./rehim.css"

const MiniCard = ({ data }) => {
  return (
    <div key={data?.id}>
        <img src={data?.image}  />
        <h2>{data?.title}</h2>
        <h3>{data?.price}</h3>
        <p>{data?.star}</p>
    </div>
  )
}

export default MiniCard


import React from 'react'
import MiniCard from './MiniCard';
const imageAPI = [
  {
    id: 1,
    title: "Audi RS7",
    image: "https://images.pistonheads.com/nimg/47454/blobid0.jpg",
    price: 210000,
    star: 5
  },
  {
    id: 2,
    title: "BMW M8 Competition",
    image: "https://cdn.motor1.com/images/mgl/y2gxLG/s3/2022-bmw-m8-competition-coupe.jpg",
    price: 220000,
    star: 4.7
  },
  {
    id: 3,
    title: "Mercedes GT63s AMG",
    image: "https://a4d540d8508d4f8a94eefc64d221e3d5.objectstore.eu/lot-19129712/1000x0/84834e6bf6529451420bbb094a0be6a0.jpg",
    price: 240000,
    star: 4.5
  },
  {
    id: 4,
    title: "Porsche Panamera Turbo S",
    image: "https://www.topgear.com/sites/default/files/images/cars-road-test/carousel/2018/01/2e841e679fd98ddfd7bca486b6044ba8/29r9139-1.jpg",
    price: 250000, 
    star: 4.8
  }
];
function Card() {
  return (
    <>
      {imageAPI.map((data)=>(
        <MiniCard key={data?.id} data={data}/>
      ))}   
    </>
  )
}

export default Card
