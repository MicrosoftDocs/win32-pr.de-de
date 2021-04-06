---
description: Die WPD-Daten \_ Strom \_ Einheiten-Enumeration gibt die Einheiten Typen an, die für iportabledeviceunitsstream-Vorgänge verwendet werden sollen.
ms.assetid: BE668696-7AF3-44AA-891A-9BFF67FB5544
title: WPD_STREAM_UNITS-Enumeration (portabletvicetypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STREAM_UNITS
api_type:
- HeaderDef
api_location:
- PortableDeviceTypes.h
ms.openlocfilehash: 8e70455402a49673b574a0c696b6dda30cc6a884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758838"
---
# <a name="wpd_stream_units-enumeration"></a>WPD \_ - \_ streamingeinheiten-Enumeration

Die **WPD-Daten \_ Strom \_ Einheiten** -Enumeration gibt die Einheiten Typen an, die für [**iportabledeviceunitsstream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) -Vorgänge verwendet werden sollen.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WPD_STREAM_UNITS { 
  WPD_STREAM_UNITS_BYTES         = 0,
  WPD_STREAM_UNITS_FRAMES        = 1,
  WPD_STREAM_UNITS_ROWS          = 2,
  WPD_STREAM_UNITS_MILLISECONDS  = 3,
  WPD_STREAM_UNITS_MICROSECONDS  = 4
} WPD_STREAM_UNITS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**WPD \_ - \_ streameinheiten ( \_ Bytes)**
</dt> <dd>

Die streameinheiten werden in Bytes angegeben.

</dd> <dt>

<span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**Rahmen für WPD- \_ \_ streamingeinheiten \_**
</dt> <dd>

Die streameinheiten werden in Frames angegeben.

</dd> <dt>

<span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**Zeilen für WPD- \_ \_ streameinheiten \_**
</dt> <dd>

Die streameinheiten werden in Zeilen angegeben.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**WPD \_ - \_ streameinheiten ( \_ Millisekunden)**
</dt> <dd>

Die streameinheiten werden in Millisekunden angegeben.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**WPD \_ - \_ streamingeinheiten ( \_ Mikrosekunden)**
</dt> <dd>

Die streameinheiten werden in Mikrosekunden angegeben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                        |
| Header<br/>                   | <dl> <dt>Portablede vicetypes. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledeviceunitsstream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[**Iportabledeviceunitsstream:: seekinunits**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




