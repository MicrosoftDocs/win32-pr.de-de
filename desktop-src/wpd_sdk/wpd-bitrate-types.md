---
description: Der WPD \_ BITRATE \_ TYPES-Enumerationstyp beschreibt einen Komprimierungstyp für Audiodateien.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: WPD_BITRATE_TYPES -Enumeration (PortableDevice.h)
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
ms.openlocfilehash: 5b50b56222014119a50c9d4ecb0fd7eb96694b30f35fbcbb72dc6550fdf88606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704050"
---
# <a name="wpd_bitrate_types-enumeration"></a>WPD \_ BITRATE \_ TYPES-Enumeration

Der **WPD \_ BITRATE TYPES-Enumerationstyp \_** beschreibt den Komprimierungstyp einer Audiodatei.

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

<span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**\_WPD-BITRATETYP \_ \_ NICHT VERWENDET**
</dt> <dd>

Dieser Wert wurde nicht angegeben.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**\_WPD-BITRATETYP \_ \_ DISKRET**
</dt> <dd>

Komprimierung der konstanten Bitrate.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**\_ \_ WPD-BITRATE-TYPVARIABLE \_**
</dt> <dd>

Komprimierung variabler Bitraten.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD \_ BITRATE \_ TYPE \_ FREE**
</dt> <dd>

Bitrate im Free-Format. Dies ist eine konstante Bitrate, die niedriger als die maximal zulässige Bitrate ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




