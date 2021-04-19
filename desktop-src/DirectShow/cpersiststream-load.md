---
description: Lädt die Filterdaten aus einem angegebenen Datenstrom.
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: Cpersiststream. Load-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Load
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83b16c3fe7bf905d1ade6b7f38cf27c61b44e4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367066"
---
# <a name="cpersiststreamload-method"></a>Cpersiststream. Load-Methode

Lädt die Filterdaten aus einem angegebenen Datenstrom.

## <a name="syntax"></a>Syntax


```C++
HRESULT Load(
   LPSTREAM pStm
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstm* 
</dt> <dd>

Zeiger auf den Stream, aus dem geladen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die **IPersistStream:: Load** -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PStream. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpersiststream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




