---
description: Die StringFromResource-Funktion lädt eine Zeichenfolge aus einer Ressourcendatei mit dem angegebenen Ressourcenbezeichner.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: StringFromResource-Funktion (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a12bffb3659bd18f630ce3ff06435a701ed77f8fba2af79b20df6d6b2574ad8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329650"
---
# <a name="stringfromresource-function"></a>StringFromResource-Funktion

Die `StringFromResource` Funktion lädt eine Zeichenfolge aus einer Ressourcendatei mit dem angegebenen Ressourcenbezeichner.

## <a name="syntax"></a>Syntax


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBuffer* 
</dt> <dd>

Zeiger auf die Zeichenfolge, die *iResourceID entspricht.*

</dd> <dt>

*iResourceID* 
</dt> <dd>

Ressourcenbezeichner der abzurufenden Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt dieselbe Zeichenfolge wie *pBuffer zurück.* Wenn die Funktion nicht erfolgreich ist, gibt eine NULL-Zeichenfolge zurück.

## <a name="remarks"></a>Hinweise

Der *pBuffer-Puffer* muss mindestens STR \_ MAX LENGTH Bytes \_ sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Hilfsfunktionen für Eigenschaftenseiten](property-page-helper-functions.md)
</dt> </dl>

 

 




