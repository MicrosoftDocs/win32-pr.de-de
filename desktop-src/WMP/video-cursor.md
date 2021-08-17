---
title: VIDEO.cursor
description: Das Cursorattribut gibt den Cursorwert an, der verwendet wird, wenn sich der Mauszeiger über einem klickbaren Bereich des Videos befindet, oder ruft diesen ab.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- VIDEO.cursor Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c39b40412a02e145b8063f473272184e1d7cf03caaa170de19bde7fad37a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134243"
---
# <a name="videocursor"></a>VIDEO.cursor

Das  Cursorattribut gibt den Cursorwert an, der verwendet wird, wenn sich der Mauszeiger über einem klickbaren Bereich des Videos befindet, oder ruft diesen ab.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff.



| Wert            | Beschreibung                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| System           | Plattformabhängiger Cursor (normalerweise ein Pfeil).                                               |
| Hand             | Hand.                                                                                       |
| Hilfe             | Pfeil mit Fragezeichen, das angibt, dass die Hilfe verfügbar ist.                                      |
| sizeall          | Vierzeilige Pfeile, die nach Norden, Süden, Osten und Westen zeigen.                                   |
| sizenesw         | Doppelpfeil, der nach Nordosten und Südosten zeigt.                                      |
| sizens           | Doppelpfeil, der nach Norden und Süden zeigt.                                              |
| sizenwse         | Pfeil mit doppelter Spitze, der auf den Nordosten und südosten zeigt.                                      |
| sizewe           | Doppelt gezeigter Pfeil, der nach Westen und Osten zeigt.                                                |
| uparrow          | Vertikaler Pfeil, der nach oben zeigt.                                                             |
| \*.ani oder \* .cur | Eine BELIEBIGE ANI- oder CUR-Datei (muss sich im selben Verzeichnis wie die WMS-Datei oder in der WMZ-Datei befinden). |



 

## <a name="remarks"></a>Hinweise

Zu Renderingzwecken ist system der Standardcursor. Der Standardwert, der von diesem Attribut abgerufen wird, ist "" (leere Zeichenfolge).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**VIDEO-Element**](video-element.md)
</dt> </dl>

 

 





