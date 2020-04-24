# react-
Source code of Avatar.js



import React,{Component} from 'react';
//import ReactDOM from 'react-dom';
import './Avatar.css';
import Avatarlist from './Avatarlist'
import 'tachyons';
      class Avatar extends Component
      {
        constructor()
        {
          super();
          this.state =
          {
            name: "Welcome to Avatar World"
          }
        }
        namechange()
        {
          this.setState(
            {
              name: "Hope u like this!!"
            }
          )
        }
        render()
        {
          const avatarlistarray=[
            {
              id:1,
              name:"Utkarsh",
              work:"web designer"
            },

              {
                id:2,
                name:"Raj",
                work:"ethical hacker"
              },
                {
                  id:3,
                  name:"Harsh",
                  work:"web developer"
                },

                  {
                    id:4,
                    name:"Shrey",
                    work:"software developer"
                  }

          ]
          const arrayavatarcard = avatarlistarray.map((avatarcard,i) =>
          {
            return <Avatarlist key={i} id={avatarlistarray[i].name} name={avatarlistarray[i].name}
            work= {avatarlistarray[i].work}/>
          })
          return (
            <div class="mainpage">
            <h1> {this.state.name} </h1>
            {arrayavatarcard}
          <button id="ck" onClick={()=> this.namechange() }> Click here </button>
          </div>
       )

      }



}

export default Avatar;




