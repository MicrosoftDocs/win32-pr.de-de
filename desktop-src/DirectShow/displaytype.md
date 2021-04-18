---
description: Die DisplayType-Funktion sendet Informationen über einen Medientyp an den debugausgabespeicherort. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: DisplayType-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DisplayType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3d83bbe7a24463fc4cfaed4ace3adec9d6fcf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364728"
---
# <a name="displaytype-function"></a>DisplayType-Funktion

Die- `DisplayType` Funktion sendet Informationen über einen Medientyp an den debugausgabespeicherort. Wird in Einzelhandels Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DisplayType(
         LPTSTR        label,
   const AM_MEDIA_TYPE *pmtIn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*label* 
</dt> <dd>

Eine Zeichenfolge, die eine Meldung enthält, die mit den Medientyp Informationen angezeigt werden soll.

</dd> <dt>

*pmtin* 
</dt> <dd>

unterliegt [**der Medientyp Struktur, die \_ \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) den Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion generiert mehrere Protokoll-Ablauf \_ Verfolgungs Meldungen. Bei der Protokollierung 2 oder höher zeigt die Funktion den Haupttyp, den Untertyp und den Formattyp sowie die Daten aus dem Format Block an. Bei der Protokollierung 5 oder höher zeigt die Funktion zusätzliche Informationen an, z. b. die Quell-und Ziel Rechtecke für Video Typen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Debug-Ausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




