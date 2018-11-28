# assignment3

//Text input or the user to key in - ariffah
//Button to perform analysis - ariffah
//Display vowels – aminah 
//Display Consonants - aminah
//Display words - aminah
//Display number of letters - ariffah
//we try our best sir 

import React, {Component} from 'react';
import {StyleSheet, Text, View, Button, TextInput} from 'react-native';

export default class App extends Component{
  constructor(){
    super();
    this.state = {
        text: '',
        counterV : 0,
        counterC : 0,
        counterL : 0
    }
  }


//reset = () =>{
//     this.setState({counterV: this.state.counterV}, {counterC: this.state.counterC},{counterL: this.state.counterL});
//}


countVowelsIterative = () => {
// var pieces = text.toLowerCase();
// this.setState({this.state.text.split()})
  
vowels = ["a", "e", "i", "o", "u"]

  // Loop through text to test if each character is a vowel
  for (var i=0; i<this.text.length; i++){
      if (vowels.includes(text)) {
         this.setState({counterV: this.state.counterV+1})
      }
      else{
        this.setState({counterC: this.state.counterC+1})
     }
  }
  this.setState({counterL: this.setState.length}); 
//   return counterV, counterC, counterL
  }

  render() {
    return (
      <View style={styles.container}>
        <View style={styles.container}>
        <Text style={styles.welcome}>Word Analyzer</Text>
        </View>

        <View style={styles.container}>
        <TextInput onChangeText={(word)  => this.setState({word})} style={styles.instructions} placeholder= "Enter a word"/>
        </View>
        
        <View style={styles.container}>
        <Button color="#841584" onPress={this.countVowelsIterative} title="Analyze"/>
        <Text style={styles.instructions}>vowel(s): {this.state.counterV}</Text>
        <Text style={styles.instructions}>consonant(s): {this.state.counterC}</Text>
        <Text style={styles.instructions}>alphabet(s): {this.state.counterL}</Text>
        </View>
    </View>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    backgroundColor: '#F5FCFF',
  },
  welcome: {
    fontSize: 20,
    textAlign: 'center',
    margin: 10,
  },
  instructions: {
    textAlign: 'center',
    color: '#333333',
    marginBottom: 5,
  },
});
