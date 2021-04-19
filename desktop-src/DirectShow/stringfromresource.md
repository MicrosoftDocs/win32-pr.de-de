---
description: Die stringfromresource-Funktion lädt eine Zeichenfolge aus einer Ressourcen Datei mit dem angegebenen Ressourcen Bezeichner.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: Stringfromresource-Funktion (wxutil. h)
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
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371723"
---
# <a name="stringfromresource-function"></a>Stringfromresource-Funktion

Die- `StringFromResource` Funktion lädt eine Zeichenfolge aus einer Ressourcen Datei mit dem angegebenen Ressourcen Bezeichner.

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

Ein Zeiger auf die Zeichenfolge, die " *iResourceID*" entspricht.

</dd> <dt>

*iResourceID* 
</dt> <dd>

Der Ressourcen Bezeichner der abzurufenden Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die gleiche Zeichenfolge wie *pbuffer* zurück. Wenn die Funktion nicht erfolgreich ist, wird eine NULL-Zeichenfolge zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Der *pbuffer* -Puffer muss mindestens Str \_ Maximale \_ Länge aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hilfsfunktionen für Eigenschaften Seiten](property-page-helper-functions.md)
</dt> </dl>

 

 




