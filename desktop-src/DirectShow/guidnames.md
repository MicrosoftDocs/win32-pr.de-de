---
description: Guidnames ist ein globales Array in der DirectShow-Basisklassen Bibliothek, das Zeichen folgen enthält, die die in UUIDs. h definierten GUIDs darstellen. Dieses Array ist hilfreich beim Erzeugen der Debugausgabe.
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: Guidnames (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GuidNames
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359294d0cf3ab4e2074db5935cbbd604dcc1b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358089"
---
# <a name="guidnames"></a>Guidnames

`GuidNames` bei handelt es sich um ein globales Array in der DirectShow-Basisklassen Bibliothek, das Zeichen folgen enthält, die die in UUIDs. h definierten GUIDs darstellen. Dieses Array ist hilfreich beim Erzeugen der Debugausgabe.

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="guid"></span><span id="GUID"></span>*GUID*
</dt> <dd>

Gibt jeden GUID-Wert an, der in der Header Datei "UUIDs. h" definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses globale Array, um GUID-Konstanten als Zeichen folgen auszugeben. Der folgende Code gibt z. b. die Zeichenfolge "MediaType \_ Video" in der Konsole aus:


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



Wenn die GUID nicht übereinstimmt, wird die Zeichenfolge "Unbekannter GUID-Name" zurückgegeben. Nicht alle DirectShow-GUIDs sind in "UUIDs. h" definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Debug-Ausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




