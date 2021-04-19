---
description: Die SetFormat-Methode initialisiert den Format Block.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Cmediatype. SetFormat-Methode (mtype. h)
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
ms.openlocfilehash: 08dd05faf514581a3325f4922076ba2053cd0c95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359624"
---
# <a name="cmediatypesetformat-method"></a>Cmediatype. SetFormat-Methode

Die- `SetFormat` Methode initialisiert den Format Block.

## <a name="syntax"></a>Syntax


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pformat* 
</dt> <dd>

Ein Zeiger auf einen Speicherblock, der den Format Block enthält.

</dd> <dt>

*length* 
</dt> <dd>

Länge des Format Blocks in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, oder **false** , wenn ein Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode ordnet Speicher für den Format Block zu und kopiert den durch *pformat* angegebenen Puffer in den neuen Format Block. Wenn der Medientyp bereits einen Format Block enthält, wird der alte freigegeben. Die-Methode legt auch den **cbformat** -Member **der \_ \_ Medientyp** Struktur "am" fest.

Um den Formattyp festzulegen, rufen Sie die [**cmediatype:: setformattype**](cmediatype-setformattype.md) -Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 




