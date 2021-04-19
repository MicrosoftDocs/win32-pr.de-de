---
description: Eine Konstruktormethode, die die Zuordnung zwischen den DWORD-Typen für das Format "im Stil" und "GUID" im alten Stil ermöglicht. Diese Methode verwendet keine Parameter.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: 'Fourccmap:: fourccmap-Konstruktor (FourCC. h)-keine Parameter'
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
ms.openlocfilehash: cd37ac842ab46c0d46fb3db1567d42274a026c47
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106360250"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a>Fourccmap:: fourccmap-Konstruktor (FourCC. h)-keine Parameter

Konstruktormethode. Der-konstuktor stellt die Zuordnung zwischen den **DWORD** -Typen für das Multimedia-Format im alten Stil und **GUID** -Untertypen bereit.

## <a name="syntax"></a>Syntax


```C++
FOURCCMap();
```



## <a name="parameters"></a>Parameter

Dieser Konstruktor weist keine Parameter auf.

## <a name="remarks"></a>Bemerkungen

Wenn dieses Objekt mit dem **FourCC** -Code erstellt wird, wird eine **GUID** erstellt, um Sie abzugleichen. Wenn dieses Objekt mit einer vorhandenen **GUID** erstellt wird, wird der **FourCC** -Wert des-Objekts auf 0 (null) festgelegt. Danach kann der **FourCC** -Wert mit den Element Funktionen [**setfourcc**](fourccmap-setfourcc.md) und [**getfourcc**](fourccmap-getfourcc.md) festgelegt oder abgerufen werden.

## <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|-|-|
| Header  | FourCC. h (Include Streams. h) |
| Bibliothek | "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Fourccmap-Klasse**](fourccmap.md)
</dt> </dl>

 

 




