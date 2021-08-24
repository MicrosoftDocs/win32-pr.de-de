---
description: Eine Konstruktormethode, die die Zuordnung zwischen DWORD-Typen im alten Multimediaformat und GUID-Untertypen bereitstellt. Diese Methode verwendet den Fourcc-Parameter.
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: FOURCCMap::FOURCCMap-Konstruktor (Fourcc.h) – Fourcc-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cfd9cbb93a4d517391be0afe591d3378d9ecef32a0013ab452d31b9eecb6d59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043210"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a>FOURCCMap::FOURCCMap-Konstruktor (Fourcc.h) – Fourcc-Parameter

Konstruktormethode. Der Constuctor stellt die Zuordnung zwischen **DWORD-Typen** im alten Multimediaformat und **GUID-Untertypen** bereit.

## <a name="syntax"></a>Syntax


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fourcc* 
</dt> <dd>

**DWORD,** das fourcc angibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn dieses Objekt mit dem **FOURCC-Code** erstellt wird, wird eine **GUID** für den Abgleich erstellt. Wenn dieses Objekt mit einer vorhandenen **GUID** erstellt wird, wird der **FOURCC-Wert** des Objekts auf 0 (null) festgelegt. Danach kann der **FOURCC-Wert** mithilfe der [**Memberfunktionen SetFOURCC**](fourccmap-setfourcc.md) bzw. [**GetFOURCC**](fourccmap-getfourcc.md) festgelegt oder abgerufen werden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header  | Fourcc.h (include Streams.h) |
| Bibliothek | Strmbase.lib (Verkaufsbuilds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FOURCCMap-Klasse**](fourccmap.md)
</dt> </dl>

 

 




