<template>
  <app-navigation></app-navigation>
</template>

<script>
import { StackNavigator } from "vue-native-router";
import { DrawerNavigator } from "vue-native-router";
import MainScreen from "./Vue/Main";
import LoginScreen from "./Vue/Login";
import SignupScreen from "./Vue/Signup";
import GuestSUScreen from "./Vue/GuestSU";
import BTSignUpScreen from "./Vue/BTSignUp";
import GuestLoginScreen from "./Vue/GuestLogin";
import BTLoginScreen from "./Vue/BTLogin";
import YourGuestsScreen from "./Vue/YourGuests";
import YourBartendersScreen from "./Vue/YourBartenders";
import UserScreen from "./Vue/User";
import AccountScreen from "./Vue/Account";
import EditInfoScreen from "./Vue/EditInfo";
import PlaceOfWorkScreen from "./Vue/PlaceOfWork";

const Drawer = DrawerNavigator(
  {
    Main: MainScreen,
    User: UserScreen,
    Account: AccountScreen,
    Signout: MainScreen
  },
  {
    initialRouteName: "Main",
  }
);

const AppNavigation = StackNavigator(
  {
    Drawer: Drawer,
    Main: MainScreen,
    Login: LoginScreen,
    Signup: SignupScreen,
    GuestSU: GuestSUScreen,
    BTSignUp: BTSignUpScreen,
    GuestLogin: GuestLoginScreen,
    BTLogin: BTLoginScreen,
    User: UserScreen,
    YourGuests: YourGuestsScreen,
    YourBartenders: YourBartendersScreen,
    EditInfo: EditInfoScreen,
    PlaceOfWork: PlaceOfWorkScreen
  },
  {
    initialRouteName: "Drawer"
  }
);
export default {
    components: { AppNavigation }
}
</script>