---
description: Ruft die maximale Bytegröße ab, die für den aktuellen Stream benötigt wird, ohne die Versionsnummer.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Cpersiststream. sizemax-Methode (pStream. h)
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
ms.openlocfilehash: afa29e2c81cc454a9e85b9038486221f6f44aaf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370740"
---
# <a name="cpersiststreamsizemax-method"></a>Cpersiststream. sizemax-Methode

Ruft die maximale Bytegröße ab, die für den aktuellen Stream benötigt wird, ohne die Versionsnummer.

## <a name="syntax"></a>Syntax


```C++
virtual int SizeMax();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl von Bytes zurück, die für Daten benötigt werden, ohne die Versionsnummer.

## <a name="remarks"></a>Bemerkungen

Die Standardversion gibt 0 (null) zurück. Er sollte überschrieben werden, um einen anderen passenden Wert bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PStream. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpersiststream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




