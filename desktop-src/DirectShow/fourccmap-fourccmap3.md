---
description: Eine Konstruktormethode, die die Zuordnung zwischen den DWORD-Typen für das Format "im Stil" und "GUID" im alten Stil ermöglicht. Diese Methode verwendet den pguid-Parameter.
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: 'Fourccmap:: fourccmap-Konstruktor (FourCC. h)-pguid-Parameter'
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
ms.openlocfilehash: 3e36f0ea58c99930d4c6c2e0929f27a43184c6be
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106357294"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a>Fourccmap:: fourccmap-Konstruktor (FourCC. h)-pguid-Parameter

Konstruktormethode. Der-konstuktor stellt die Zuordnung zwischen den **DWORD** -Typen für das Multimedia-Format im alten Stil und **GUID** -Untertypen bereit.

## <a name="syntax"></a>Syntax


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguid* 
</dt> <dd>

Zeiger auf den Globally Unique Identifier (**GUID**).

</dd> </dl>

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

 

 




