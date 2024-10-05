<h1 align="center">Proyecto 2</h1>

<p align="center"></p>

<div align="center">
🙍‍♂️ Joab Israel Ajsivinac Ajsivinac 🆔 202200135
</div>
<div align="center">
📕 REDES DE COMPUTADORAS 1
</div>
<div align="center"> 🏛 Universidad San Carlos de Guatemala</div>
<div align="center"> 📆 Segundo Semestre 2024</div>

<br/> 
<h1 align="center">📍 Manual Técnico</h1>
<br/> 

# 🛠 Configuración de Routers
## R1

```
Router>en
Router#conf t
Router (config) #ip domain—lookup
Router (config) #hostname R1
R1 (config) #do wr

R1>en
R1#conf t
R1 (config) #int f0/0
R1 (config) #ip add 152.168.1.2 255.255.255.248
R1 (config—if) #no shutdown

R1 (config—if) #exit
R1 (config) # int f0/1
R1 (config-if) #ip add 152.168.2.2 255.255.255.248
R1 (config—if) #no sh
R1 (config—if) #exit
```

## R2

```
Router>en
Router#conf t
Router (config) #ip domain—lookup
Router (config) #hostname R2
R2 (config) #do wr

R2>en
R2#conf t
R2 (config) #int f0/1
R2 (config) #ip add 152.168.0.2 255.255.255.0
R2 (config—if) #standby 1 ip 152.168.0.1
R2 (config—if) #standby 1 priority 150
R2 (config—if) #standby 1 preempt
R2 (config—if) #no shutdown

R2 (config—if) #exit
R2 (config) # int f0/0
R2 (config-if) #ip add 152.168.1.1 255.255.255.248
R2 (config—if) #no shutdown
R2 (config—if) #exit
```

## R6

# 🔧 Configuración de Switches

## SW1
```
Switch>en
Switch#conf t
Switch (config) #int range f0/21—22
Switch # channel—protocol pagp
Switch # channel—group 1 mode desirable
Switch 1 mode desirable
```

## SW3


# 💻 Configuración de VPC
## VPC11

## VPC14


# ⌨ Creación Rutas Estáticas

## R1

```
R1>en
R1#conf t
R1 (config) route
R1 (config) #ip route 152.178.0.0 255.255.255.0 10.0.0 2
R1 (config) #ip route 152.178.1.0 255.255.255.0 10.0.0 2
R1 (config) #ip route 152.178.2.0 255.255.255.0 10.0.0 2
```

# ↔ Creación de PortChannel con PAGP

# ↔ Creación de PortChannel con LACP

# 🔰 HSRP

# ⌨ Resumen de Comandos