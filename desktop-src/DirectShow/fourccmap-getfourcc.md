---
description: Ruft den FOURCC-&\# 160;DWORD aus dem FOURCCMap-Objekt ab.
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: FOURCCMap::GetFOURCC-Methode (Fourcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.GetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 381625f5d0a585f212c8f7b076d1cd58ea5215958bf09025e1db864ce2f624b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015718"
---
# <a name="fourccmapgetfourcc-method"></a>FOURCCMap::GetFOURCC-Methode

Ruft das **FOURCC** **DWORD** aus dem [**FOURCCMap-Objekt**](fourccmap.md) ab.

## <a name="syntax"></a>Syntax


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den **FOURCC** **DWORD-Wert** zurück. Beachten Sie Folgendes: Wenn Sie eine **GUID** erstellen, die ursprünglich nicht von **einer FOURCC** abgeleitet wurde, ist der Rückgabewert im Wesentlichen zufällig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Fourcc.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FOURCCMap-Klasse**](fourccmap.md)
</dt> </dl>

 

 




