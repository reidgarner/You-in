<template>
    <view class="container">
        <image-background :source="bartenderImg" class="imageContainer">
            <view class="logo-container">
                <image :source="logo" class="logo"></image>
                <image :source="logo2" class="logo2"></image>
            </view>
            <view class="barguest-container">
                <image :source="BarGuest1" class="BarGuest1"></image>
                <image :source="BarGuest2" class="BarGuest2"></image>
            </view>
            <view class="input-container">
                <text-input class="input" auto-capitalize="none" v-model="first_name" placeholder="First Name"/>
                <text-input class="input" auto-capitalize="none" v-model="last_name" placeholder="Last Name"/>
                <text-input class="input" auto-capitalize="none" v-model="email" placeholder="Email"/>
                <text-input class="input" auto-capitalize="none" v-model="password" placeholder="Password"/>
            </view>
            <touchable-opacity class="button" :on-press="handleUser">
                <text class="button-text">Login</text>
            </touchable-opacity>
        </image-background>
    </view>
</template>

<script>
import bartenderImg from "/Users/reidgarner/Galv-Projects/CAPSTONE/You-In-Frontend/assets/Bartender3-Background.png";
import logo from "/Users/reidgarner/Galv-Projects/CAPSTONE/You-In-Frontend/assets/red_cream_ud_logo_transparent.png";
import logo2 from "/Users/reidgarner/Galv-Projects/CAPSTONE/You-In-Frontend/assets/YouIn_transparent.png";
import BarGuest1 from "/Users/reidgarner/Galv-Projects/CAPSTONE/You-In-Frontend/assets/BarGuest_Tan.png";
import BarGuest2 from "/Users/reidgarner/Galv-Projects/CAPSTONE/You-In-Frontend/assets/BarGuest_Black.png";

export default {
    props: {
        navigation: {
            type: Object
        }
    },

    data() {
        return {
            first_name: '',
            last_name: '',
            email: '',
            password: '',
            logo: logo,
            logo2: logo2,
            bartenderImg: bartenderImg,
            BarGuest1: BarGuest1,
            BarGuest2: BarGuest2
    }
    },

    methods: {
        handleUser() {
            this.navigation.navigate("User");
        }
    }
}
</script>

<style>
.container {
    background-color: rgb(99, 99, 99);
    align-items: center;
    justify-content: center;
    flex: 1;
}

.imageContainer {
    flex: 1;
    align-items: center;
    justify-content: center;
    width: 130%;
    position: relative; left: 46;
}

.logo-container {
    height: 300;
    width: 200;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative; top: 30;
}

.logo {
    height: 120%;
    width: 120%;
    position: relative; top: 163; right: 45;
    opacity: .78;
}

.logo2 {
    height: 124%;
    width: 120%;
    position: relative; right: 45; bottom: 171;
    opacity: 1;
}

.button {
    background-color: #8D1B33;
    width: 170;
    height: 60;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 10;
    opacity: .85;
    position: relative; bottom: 40; right: 47;
}

.button-text {
    color: #F7C7AA;
    font-size: 30;
    font-family: Helvetica;
}

.input-container {
    display: flex;
    justify-content: space-evenly;
    height: 250;
    width: 300;
    position: relative; bottom: 50; right: 47;
    opacity: .85;
}

.input {
    height: 50; 
    width: 300; 
    border-radius: 10; 
    border-color: gray; 
    border-width: 1;
    background-color: whitesmoke;
}

.barguest-container {
    height: 100;
    width: 300;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative; top: 205;
}

.BarGuest1 {
    height: 200%;
    width: 200%;
    position: relative; bottom: 104; right: 47;
}

.BarGuest2 {
    height: 205%;
    width: 203%;
    position: relative; bottom: 305; right: 47;
}
</style>