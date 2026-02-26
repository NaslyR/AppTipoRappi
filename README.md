# AppTipoRappi

Aplicación tipo **Rappi** para la **gestión de domicilios**, orientada a facilitar el proceso de pedidos, asignación de repartidores y seguimiento de entregas en tiempo real.

---

## 📱 Descripción general

**AppTipoRappi** es una aplicación diseñada para simular y gestionar un sistema de domicilios similar a plataformas de delivery. Permite administrar pedidos desde su creación hasta la entrega final, involucrando a clientes, repartidores y administradores.

La app está pensada como base para aprendizaje, prototipos o evolución hacia un producto real.

---

## 🚀 Funcionalidades principales

- 📦 **Gestión de pedidos**
  - Creación y seguimiento de pedidos
  - Estados del pedido (pendiente, en preparación, en camino, entregado)

- 👤 **Gestión de usuarios**
  - Clientes
  - Repartidores
  - Administradores

- 🛵 **Asignación de repartidores**
  - Asignación manual o automática
  - Visualización de pedidos activos

- 📍 **Seguimiento de domicilios**
  - Estado en tiempo real
  - Historial de pedidos

- 📊 **Panel administrativo**
  - Control de pedidos
  - Gestión de usuarios
  - Reportes básicos

---}

Nombre del proyecto: DeliveryApp tipo Rappi

**¿Qué problema resuelve el sistema?**
El sistema busca facilitar la compra de productos y alimentos a domicilio mediante una aplicación móvil, permitiendo que los usuarios realicen pedidos de manera rápida y segura sin necesidad de desplazarse físicamente.

**¿Quién lo usará?**
Será utilizado por clientes que realizan pedidos, repartidores encargados de las entregas, negocios afiliados que ofrecen productos y administradores que supervisan el funcionamiento general del sistema.

**¿Qué pasaría si no existiera?**
Los usuarios tendrían menos opciones para comprar desde casa y los negocios perderían una oportunidad importante de ampliar su alcance y aumentar sus ventas.

2 **¿Qué funciones principales tiene el sistema?**
El sistema permite el registro e inicio de sesión de usuarios, la visualización de productos, la creación y gestión de pedidos, el procesamiento de pagos, el control de inventario y el envío de notificaciones.

**¿Qué partes pueden trabajar por separado?**
Los módulos de autenticación, pedidos, pagos, inventario y notificaciones pueden funcionar de manera independiente, ya que cada uno cumple una responsabilidad específica dentro del sistema.

**¿Qué procesos son independientes?**
El inicio de sesión, la consulta de productos, la validación de pagos y el envío de notificaciones pueden ejecutarse sin depender directamente del funcionamiento simultáneo de todos los demás servicios.

3 **¿Qué servicio necesita información de otro?**
El servicio de Pedidos necesita información del servicio de Inventario para verificar la disponibilidad de los productos seleccionados.

**Quien solicita datos**
Autenticación solicita datos a Usuarios
Pedidos solicita datos a Inventario.
Pedidos solicita validación a Pagos
Pagos solicita actualización a Pedidos
Pedidos solicita envío de mensaje a Notificaciones

**¿Quién responde?**
Usuarios responde a Autenticación
Inventario responde a Pedidos
Pagos responde a Pedidos
Pedidos responde a Pagos (actualizando estado)
Notificaciones responde enviando el mensaje correspondiente
