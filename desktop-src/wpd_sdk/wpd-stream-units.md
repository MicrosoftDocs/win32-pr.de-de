---
description: Die WPD STREAM UNITS-Enumeration gibt die Einheitentypen an, die \_ \_ für IPortableDeviceUnitsStream-Vorgänge verwendet werden sollen.
ms.assetid: BE668696-7AF3-44AA-891A-9BFF67FB5544
title: WPD_STREAM_UNITS -Enumeration (PortableDeviceTypes.h)
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
ms.openlocfilehash: d2419453beac6b493ddd1bbbe1281b1596ce00456599074b3872fecb003550c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440760"
---
# <a name="wpd_stream_units-enumeration"></a>WPD \_ STREAM \_ UNITS-Enumeration

Die **WPD \_ STREAM \_ UNITS-Enumeration** gibt die Einheitentypen an, die für [**IPortableDeviceUnitsStream-Vorgänge verwendet werden**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) sollen.

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

<span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**BYTES DER \_ \_ WPD-STREAMEINHEITEN \_**
</dt> <dd>

Die Streameinheiten werden in Bytes angegeben.

</dd> <dt>

<span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**WPD \_ STREAM \_ UNITS \_ FRAMES**
</dt> <dd>

Die Streameinheiten werden in Frames angegeben.

</dd> <dt>

<span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**\_ \_ WPD-STREAMEINHEITENZEILEN \_**
</dt> <dd>

Die Streameinheiten werden in Zeilen angegeben.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**\_WPD-STREAMEINHEITEN \_ \_ IN MILLISEKUNDEN**
</dt> <dd>

Die Streameinheiten werden in Millisekunden angegeben.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**WPD \_ STREAM \_ UNITS \_ MICROSECONDS**
</dt> <dd>

Die Streameinheiten werden in Mikrosekunden angegeben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                        |
| Header<br/>                   | <dl> <dt>PortableDeviceTypes.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[**IPortableDeviceUnitsStream::SeekInUnits**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




