---
description: Die DisplayType-Funktion sendet Informationen zu einem Medientyp an den Debugausgabespeicherort. Wird in Einzelhandels-Builds ignoriert.
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: DisplayType-Funktion (Wxdebug.h)
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
ms.openlocfilehash: 4a48bc5f4afbfabc9bdc37ff2cfe8c5890629f3fcaacf135979b82523981ed66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906500"
---
# <a name="displaytype-function"></a>DisplayType-Funktion

Die `DisplayType` Funktion sendet Informationen zu einem Medientyp an den Debugausgabespeicherort. Wird in Einzelhandels-Builds ignoriert.

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

Eine Zeichenfolge, die eine Meldung enthält, die mit den Medientypinformationen angezeigt werden soll.

</dd> <dt>

*pmtIn* 
</dt> <dd>

Mit der [**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) die den Medientyp enthält, geintert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion generiert mehrere LOG \_ TRACE-Meldungen. Auf Protokollierungsebene 2 oder höher zeigt die Funktion den Haupttyp, Untertyp und Formattyp sowie Daten aus dem Formatblock an. Bei Protokollierungsebene 5 oder höher zeigt die Funktion zusätzliche Informationen an, z. B. die Quell- und Zielrechtecke für Videotypen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Debugausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




