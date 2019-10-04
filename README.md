# switch-button-react-native
Customisable switch button in react native ( e.g: change view after change  switch button )

![switchbutton](https://user-images.githubusercontent.com/33284430/32404024-3d02ba94-c15d-11e7-8e76-87276dd2ee1a.gif)


how to use:

1) import component
2) set

        activeSwitch=1
to state

3) use:

        <SwitchButton  
              onValueChange={(val) => this.setState({ activeSwitch: val })} 
        /> 
in your code

4) use:

        { this.state.activeSwitch === 1 ? view1 : view2 }





small example: ...
    
    import React, { Component } from 'react'; 
    import { View } from 'react-native'; 
    import SwitchButton from 'switch-button-react-native';
    
    constructor () {
        super();

        this.state = {
          activeSwitch: 1
        };
    }


    render () {

        return (

            <View>
                <SwitchButton
                    onValueChange={(val) => this.setState({ activeSwitch: val })}      // this is necessary for this component
                    text1 = 'ON'                        // optional: first text in switch button --- default ON
                    text2 = 'OFF'                       // optional: second text in switch button --- default OFF
                    switchWidth = {100}                 // optional: switch width --- default 44
                    switchHeight = {44}                 // optional: switch height --- default 100
                    switchdirection = 'rtl'             // optional: switch button direction ( ltr and rtl ) --- default ltr
                    switchBorderRadius = {100}          // optional: switch border radius --- default oval
                    switchSpeedChange = {500}           // optional: button change speed --- default 100
                    switchBorderColor = '#d4d4d4'       // optional: switch border color --- default #d4d4d4
                    switchBackgroundColor = '#fff'      // optional: switch background color --- default #fff
                    btnBorderColor = '#00a4b9'          // optional: button border color --- default #00a4b9
                    btnBackgroundColor = '#00bcd4'      // optional: button background color --- default #00bcd4
                    fontColor = '#b1b1b1'               // optional: text font color --- default #b1b1b1
                    activeFontColor = '#fff'            // optional: active font color --- default #fff
                />
                
                { this.state.activeSwitch === 1 ? console.log('view1') : console.log('view2') }
                
            </View>

        );
    }
