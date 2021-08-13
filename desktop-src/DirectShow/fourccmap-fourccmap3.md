---
description: Eine Konstruktormethode, die die Zuordnung zwischen alten Multimediaformat-DWORD-Typen und GUID-Untertypen ermöglicht. Diese Methode verwendet den Parameter "pguid".
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: FOURCCMap::FOURCCMap-Konstruktor (Fourcc.h) – pguid-Parameter
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
ms.openlocfilehash: 2c674791418a7668d7c7597e951e9a89613b9c8150865ff123263e9d0ef9ded2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330440"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a>FOURCCMap::FOURCCMap-Konstruktor (Fourcc.h) – pguid-Parameter

Konstruktormethode. Der Constuctor stellt die Zuordnung zwischen alten **Multimediaformat-DWORD-Typen** und **GUID-Untertypen** zur Verfügung.

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

Zeiger auf den global eindeutigen Bezeichner (**GUID**).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn dieses Objekt mit dem **FOURCC-Code erstellt** wird, wird eine **GUID** erstellt, um ihn zu finden. Wenn dieses Objekt mit einer vorhandenen **GUID erstellt** wird, wird der **FOURCC-Wert** des -Objekts auf 0 (null) festgelegt. Danach kann der **FOURCC-Wert** mithilfe der [**Memberfunktionen SetFOURCC**](fourccmap-setfourcc.md) bzw. [**GetFOURCC**](fourccmap-getfourcc.md) festgelegt oder abgerufen werden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header  | Fourcc.h (include Streams.h) |
| Bibliothek | Strmbase.lib (Einzelhandels-Builds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FOURCCMap-Klasse**](fourccmap.md)
</dt> </dl>

 

 




