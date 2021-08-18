---
title: TEXT.cursor
description: Das Cursorattribut gibt einen Wert an, der angibt, welcher Cursor angezeigt wird, wenn sich der Mauszeiger über dem Text-Steuerelement befindet, oder ruft einen Wert ab.
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- TEXT.cursor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72dc904371333dcdf3b9c80e441fb1d8254285bcd6193150ecd3df4032afd22d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134653"
---
# <a name="textcursor"></a>TEXT.cursor

Das  Cursorattribut gibt einen Wert an, der angibt, welcher Cursor angezeigt wird, wenn sich der Mauszeiger über dem Text-Steuerelement befindet, oder ruft einen Wert ab.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff.



| Wert            | Beschreibung                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| System           | Standard. Plattformabhängiger Cursor (normalerweise ein Pfeil).                                      |
| Hand             | Hand.                                                                                       |
| Hilfe             | Pfeil mit Fragezeichen, das angibt, dass die Hilfe verfügbar ist.                                      |
| sizeall          | Vierzeilige Pfeile, die nach Norden, Süden, Osten und Westen zeigen.                                   |
| sizenesw         | Doppelpfeil, der nach Nordosten und Südosten zeigt.                                      |
| sizens           | Doppelpfeil, der nach Norden und Süden zeigt.                                              |
| sizenwse         | Pfeil mit doppelter Spitze, der auf den Nordosten und südosten zeigt.                                      |
| sizewe           | Doppelt gezeigter Pfeil, der nach Westen und Osten zeigt.                                                |
| uparrow          | Vertikaler Pfeil, der nach oben zeigt.                                                             |
| \*.ani oder \* .cur | Eine BELIEBIGE ANI- oder CUR-Datei (muss sich im selben Verzeichnis wie die WMS-Datei oder in der WMZ-Datei befinden). |



 

Ein Beispiel, das veranschaulicht, wie die Attribute des **TEXT-Elements** verwendet werden, finden Sie im [Value-Attribut.](text-value.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TEXT-Element**](text-element.md)
</dt> </dl>

 

 





