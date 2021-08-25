---
description: Ruft die maximale Bytegröße ab, die für den aktuellen Stream benötigt wird, ohne die Versionsnummer.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: CPersistStream.SizeMax-Methode (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b8f2c547e75303e4c54a49651f2118a90768bc0f42161ee3dae0de9bec2dcad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813300"
---
# <a name="cpersiststreamsizemax-method"></a>CPersistStream.SizeMax-Methode

Ruft die maximale Bytegröße ab, die für den aktuellen Stream benötigt wird, ohne die Versionsnummer.

## <a name="syntax"></a>Syntax


```C++
virtual int SizeMax();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der bytes zurück, die für Daten benötigt werden, ohne die Versionsnummer.

## <a name="remarks"></a>Hinweise

Die Standardversion gibt 0 (null) zurück. sie sollte überschrieben werden, um einen anderen geeigneten Wert bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pstream.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPersistStream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




