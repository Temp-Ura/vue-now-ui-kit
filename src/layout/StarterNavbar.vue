<template>
  <navbar position="fixed" type="primary"   menu-classes="ml-auto">
    <template>
      <a class="navbar-brand" to="#">
        PRENDIAMOLA CON FILOSOFIA 
      </a>
      <!--<a class="navbar-brand" href="#">
        
      </a>-->
      <!--<el-popover
        ref="popover1"
        popper-class="popover"
        placement="bottom"
        width="200"
        trigger="hover"
      >
        <div class="popover-body">
          Designed by Invision. Coded by Creative Tim
        </div>
      </el-popover>-->
    </template>
    <template slot="navbar-menu">
      <li class="nav-item hover">
           <a class="nav-link" href="#manif">
             
             <p>Manifesto</p>
           </a>
         </li>
         <li class="nav-item hover">
           <a class="nav-link" href="#tito">
             
             <p>Programma</p>
           </a>
         </li>
         <li class="nav-item hover">
           <a class="nav-link" href="#partner">
             
             <p>Partner</p>
           </a>
         </li>
         <li class="nav-item hover">
           <a class="nav-link" href="#pablo">
             <i class="fab fa-instagram"></i>
           </a>
         </li>
         <li class="nav-item hover">
           <a class="nav-link" href="#pablo">
             <i class="fab fa-facebook"></i>
           </a>
         </li>
         <li class="nav-item hover">
           <a class="nav-link" href="#pablo">
             <i class="fab fa-youtube"></i>
           </a>
         </li>
    </template>
  </navbar>
</template>

<script>
import { DropDown, NavbarToggleButton, Navbar, NavLink } from '@/components';
import { Popover } from 'element-ui';

export default {
  name: 'main-navbar',
  components: {
    DropDown,
    Navbar,
    NavbarToggleButton,
    NavLink,
    [Popover.name]: Popover
  }
};
</script>

<style scoped></style>
