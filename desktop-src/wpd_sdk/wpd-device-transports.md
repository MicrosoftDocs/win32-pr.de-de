---
description: Der \_ Enumerationstyp der WPD-Geräte \_ Transporte gibt die Vererbungs Beziehung für einen Dienst an. Diese Enumeration wird von der WPD- \_ Geräte \_ Transport Eigenschaft verwendet.
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: WPD_DEVICE_TRANSPORTS-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TRANSPORTS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 574c6b0b00980d110f2374e7426dd101c9122854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358205"
---
# <a name="wpd_device_transports-enumeration"></a>WPD- \_ Geräte \_ Transport-Enumeration

Der Enumerationstyp der [**WPD- \_ Geräte \_ Transporte**](/windows/desktop/wpd_sdk/wpd-device-transports) gibt die Vererbungs Beziehung für einen Dienst an. Diese Enumeration wird von der **WPD- \_ Geräte \_ Transport** Eigenschaft verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**der WPD- \_ Geräte \_ Transport ist \_ nicht angegeben.**
</dt> <dd>

Der Transporttyp wurde nicht angegeben.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD \_ \_ -Geräte Transport \_ -USB**
</dt> <dd>

Das Gerät ist über USB verbunden.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**WPD \_ \_ -Geräte Transport \_ -IP**
</dt> <dd>

Das Gerät ist über das Internet Protokoll (IP) verbunden.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**WPD- \_ Geräte \_ Transport \_ Bluetooth**
</dt> <dd>

Das Gerät ist über Bluetooth verbunden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



 

