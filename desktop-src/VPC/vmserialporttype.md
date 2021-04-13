---
title: Vmserialporttype-Enumeration (vpccominterfaces. h)
description: Gibt den Typ des seriellen Anschlusses an.
ms.assetid: 1385292b-ee3c-41f0-805a-df126f33cabb
keywords:
- Vmserialporttype-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMSerialPortType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9b6171053e980f1f5dbdc52ef28deed177edba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518371"
---
# <a name="vmserialporttype-enumeration"></a>Vmserialporttype-Enumeration

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Gibt den Typ des seriellen Anschlusses an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmSerialPort_HostPort   = 0,
  vmSerialPort_TextFile   = 1,
  vmSerialPort_NamedPipe  = 2,
  vmSerialPort_Null       = 3
} VMSerialPortType;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**vmserialport- \_ hostport**
</dt> <dd>

Einen seriellen Port für den Host.

</dd> <dt>

<span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**vmserialport- \_ Textdatei**
</dt> <dd>

Eine Host Textdatei.

</dd> <dt>

<span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**vmserialport- \_ NamedPipe**
</dt> <dd>

Eine Named Pipe.

</dd> <dt>

<span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmserialport \_ null**
</dt> <dd>

Ein serieller **null** -Anschluss (verwirft alle an ihn gesendeten Bits).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmserialport**](ivmserialport.md)
</dt> </dl>

 

