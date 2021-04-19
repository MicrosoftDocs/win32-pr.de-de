---
description: Der \_ \_ Enumerationstyp WPD-Power Sources beschreibt die Stromquelle, die von einem Gerät verwendet wird.
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: WPD_POWER_SOURCES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_POWER_SOURCES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bf9a153d4d41a64b639f796ea2ba0eeb9e567a32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369591"
---
# <a name="wpd_power_sources-enumeration"></a>WPD- \_ Power \_ Sources-Enumeration

Der Enumerationstyp **WPD- \_ Power \_ Sources** beschreibt die Stromquelle, die von einem Gerät verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**Akku für WPD- \_ Strom \_ Quelle \_**
</dt> <dd>

Die Stromquelle des Geräts ist ein Akku.

</dd> <dt>

<span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**externe WPD- \_ Strom \_ Quelle \_**
</dt> <dd>

Vom Gerät wird eine externe Stromquelle verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird von der [WPD- \_ Geräte \_ Energie \_ Quellen](device-properties.md) -Eigenschaft verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




