---
description: Ruft das FourCC&\# 160; DWORD aus dem fourccmap-Objekt ab.
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: 'Fourccmap:: getfourcc-Methode (FourCC. h)'
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
ms.openlocfilehash: c76493ff172f7a5611367fd50aa3b7957cf5441b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369448"
---
# <a name="fourccmapgetfourcc-method"></a>Fourccmap:: getfourcc-Methode

Ruft das **FourCC** **DWORD** aus dem [**fourccmap**](fourccmap.md) -Objekt ab.

## <a name="syntax"></a>Syntax


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den **FourCC** **DWORD** -Wert zurück. Beachten Sie Folgendes: Wenn Sie eine **GUID** erstellen, die ursprünglich nicht von einem **FourCC** abgeleitet wurde, ist der Rückgabewert im Grunde zufällig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>FourCC. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Fourccmap-Klasse**](fourccmap.md)
</dt> </dl>

 

 




