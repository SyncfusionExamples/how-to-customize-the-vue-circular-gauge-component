<script setup>
import { CircularGaugeComponent as EjsCirculargauge, AxesDirective as EAxes,
         AxisDirective as EAxis, RangesDirective as ERanges,
         RangeDirective as ERange
 } from '@syncfusion/ej2-vue-circulargauge';
 const lineStyle = {
    color:'blue',width:3
}
const majorTicks={
  color:'blue',
  width:3,
  height:10,
  interval:20 ,
  offset:5,  
  position:'Outside'                     
}
const minorTicks={
  color:'red',
  width:2,
  height:5,
  interval:10 ,
  offset:5,  
  position:'Outside'               
}
const  labelStyle={
              autoAngle:true,
           format:'{value}°C',
             hiddenLabel:'First'
              }
</script>

<template>
<ejs-circulargauge>
    <e-axes>
        <e-axis :lineStyle='lineStyle' background='rgba(0, 128, 128, 0.3)'
        minimum="50" maximum="250" :majorTicks='majorTicks' :minorTicks='minorTicks'
        :labelStyle="labelStyle" startAngle="0" endAngle="360" direction='AntiClockWise'
       >
       <e-ranges>
        <e-range start="210" end="250" radius='70%' color='blue' opacity='0.2'
          roundedCornerRadius="5"></e-range>
          <e-range start="70" end="90" radius='70%'></e-range>
          <e-range start="110" end="150" radius='70%'></e-range>
          </e-ranges>
        </e-axis>
        <e-axis background="rgba(0, 256,64,0.3)" minimum="-20" maximum="60"></e-axis>
       </e-axes>
</ejs-circulargauge>
</template>

<style>

</style>
