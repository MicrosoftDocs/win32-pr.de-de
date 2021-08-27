---
description: Die SetFormat-Methode initialisiert den Formatblock.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: CMediaType.SetFormat-Methode (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99726a466b6bf273b654a5d459fa2391a75882f1adee64b981d91a514a988b88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108450"
---
# <a name="cmediatypesetformat-method"></a>CMediaType.SetFormat-Methode

Die `SetFormat` -Methode initialisiert den Formatblock.

## <a name="syntax"></a>Syntax


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFormat* 
</dt> <dd>

Zeiger auf einen Speicherblock, der den Formatblock enthält.

</dd> <dt>

*length* 
</dt> <dd>

Länge des Formatblocks in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, oder **FALSE,** wenn ein Fehler aufgetreten ist.

## <a name="remarks"></a>Hinweise

Diese Methode belegt Arbeitsspeicher für den Formatblock und kopiert den von *pFormat* angegebenen Puffer in den neuen Formatblock. Wenn der Medientyp bereits einen Formatblock enthält, wird der alte freigegeben. Die -Methode legt auch den **cbFormat-Member** der **AM MEDIA \_ \_ TYPE-Struktur** fest.

Um den Formattyp festzulegen, rufen Sie die [**CMediaType::SetFormatType-Methode**](cmediatype-setformattype.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




