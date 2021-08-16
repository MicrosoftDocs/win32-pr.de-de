---
description: Eine Konstruktormethode, die die Zuordnung zwischen alten Multimediaformat-DWORD-Typen und GUID-Untertypen ermöglicht. Diese Methode verwendet keine Parameter.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: FOURCCMap::FOURCCMap-Konstruktor (Fourcc.h) – Keine Parameter
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
ms.openlocfilehash: d856589146103e599a1cf67d2090dd64af7107d1c221c46b9c93852f989ade9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015728"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a>FOURCCMap::FOURCCMap-Konstruktor (Fourcc.h) – Keine Parameter

Konstruktormethode. Der Constuctor stellt die Zuordnung zwischen alten **Multimediaformat-DWORD-Typen** und **GUID-Untertypen** zur Verfügung.

## <a name="syntax"></a>Syntax


```C++
FOURCCMap();
```



## <a name="parameters"></a>Parameter

Dieser Konstruktor verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Wenn dieses Objekt mit dem **FOURCC-Code erstellt** wird, wird eine **GUID** erstellt, um ihn zu finden. Wenn dieses Objekt mit einer vorhandenen **GUID** erstellt wird, wird der **FOURCC-Wert** des -Objekts auf 0 (null) festgelegt. Danach kann der **FOURCC-Wert** mithilfe der [**Memberfunktionen SetFOURCC**](fourccmap-setfourcc.md) bzw. [**GetFOURCC**](fourccmap-getfourcc.md) festgelegt oder abgerufen werden.

## <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|-|-|
| Header  | Fourcc.h (include Streams.h) |
| Bibliothek | Strmbase.lib (Einzelhandels-Builds); Strmbasd.lib (Debugbuilds) |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FOURCCMap-Klasse**](fourccmap.md)
</dt> </dl>

 

 




