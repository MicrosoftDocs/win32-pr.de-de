---
description: Der \_ \_ Enumerationstyp der WPD-Bitrate-Typen beschreibt einen Komprimierungstyp für Audiodateien.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: WPD_BITRATE_TYPES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2597af21c5655c3c12c0ca29f097d0eba2bb8d54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370285"
---
# <a name="wpd_bitrate_types-enumeration"></a>WPD \_ Bitrate \_ types-Enumeration

Der Enumerationstyp der **WPD- \_ Bitrate- \_ Typen** beschreibt den Komprimierungstyp einer Audiodatei.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**nicht verwendeter WPD- \_ Bitrate- \_ Typ \_**
</dt> <dd>

Dieser Wert wurde nicht angegeben.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**diskreter WPD- \_ Bitrate- \_ Typ \_**
</dt> <dd>

Komprimierung konstanter Bitrate.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**WPD- \_ Bitrate- \_ \_ Typvariable**
</dt> <dd>

Komprimierung der Variablen Bitrate.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD- \_ Bitrate ( \_ \_ Free)**
</dt> <dd>

Kostenlose formatbitrate. Dies ist eine Konstante Bitrate, die niedriger als die maximal zulässige Bitrate ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




