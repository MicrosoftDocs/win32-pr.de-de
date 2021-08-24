---
description: Ruft die maximale Bytegröße ab, die für den aktuellen Stream benötigt wird, einschließlich der Versionsnummer.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: CPersistStream.GetSizeMax-Methode (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 746fb01102642f2d3e6b254ac741c284143aaecfd401fc220bf7a9d97d93e64e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813370"
---
# <a name="cpersiststreamgetsizemax-method"></a>CPersistStream.GetSizeMax-Methode

Ruft die maximale Bytegröße ab, die für den aktuellen Stream benötigt wird, einschließlich der Versionsnummer.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*layoutSize* 
</dt> <dd>

Zeiger auf die Größe in Bytes, die zum Speichern dieses Streams erforderlich ist, einschließlich der Versionsnummer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die **IPersistStream::GetSizeMax-Methode.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pstream.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPersistStream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




