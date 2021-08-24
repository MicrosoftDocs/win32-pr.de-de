---
description: Der WPD \_ DEVICE \_ TRANSPORTS-Enumerationstyp gibt die Vererbungsbeziehung für einen Dienst an. Diese Enumeration wird von der WPD \_ DEVICE \_ TRANSPORT-Eigenschaft verwendet.
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: WPD_DEVICE_TRANSPORTS -Enumeration (PortableDevice.h)
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
ms.openlocfilehash: 5f091a84c573038c7d74cf5c2760c298a2542f70f06bdb45d1e72954c9dd5f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703820"
---
# <a name="wpd_device_transports-enumeration"></a>WPD \_ DEVICE \_ TRANSPORTS-Enumeration

Der [**WPD \_ DEVICE \_ TRANSPORTS-Enumerationstyp**](/windows/desktop/wpd_sdk/wpd-device-transports) gibt die Vererbungsbeziehung für einen Dienst an. Diese Enumeration wird von der **WPD \_ DEVICE \_ TRANSPORT-Eigenschaft** verwendet.

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

<span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**\_ \_ WPD-GERÄTETRANSPORT \_ NICHT ANGEGEBEN**
</dt> <dd>

Der Transporttyp wurde nicht angegeben.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD \_ DEVICE \_ TRANSPORT \_ USB**
</dt> <dd>

Das Gerät ist über USB verbunden.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**\_ \_ WPD-GERÄTETRANSPORT-IP \_**
</dt> <dd>

Das Gerät ist über das Internetprotokoll (INTERNET PROTOCOL, IP) verbunden.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**WPD \_ DEVICE \_ TRANSPORT \_ BLUETOOTH**
</dt> <dd>

Das Gerät ist über eine Bluetooth.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

