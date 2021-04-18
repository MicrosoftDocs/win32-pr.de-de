---
title: Video. Cursor
description: Das Cursor Attribut gibt den Cursor Wert an, der verwendet wird, wenn sich der Mauszeiger über einem klickbaren Bereich des Videos befindet, oder ruft ihn ab.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- Video. Cursor-Fenster Media Player
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c23ab90b974ad5a7f9cfaf9fcc598371cd0697f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371227"
---
# <a name="videocursor"></a>Video. Cursor

Das **Cursor** Attribut gibt den Cursor Wert an, der verwendet wird, wenn sich der Mauszeiger über einem klickbaren Bereich des Videos befindet, oder ruft ihn ab.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.



| Wert            | Beschreibung                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| System           | Platt Form abhängiger Cursor (in der Regel ein Pfeil).                                               |
| linken             | Linken.                                                                                       |
| help             | Pfeil mit Fragezeichen, das angibt, dass Hilfe verfügbar ist.                                      |
| SizeAll          | Vierstufige Pfeil, der nach Norden, Süden, Osten und Westen zeigt.                                   |
| sizenesw         | Ein Pfeil mit zwei Spitzen, der auf Nordost und Südwest zeigt.                                      |
| SizeNS           | Ein Pfeil mit zwei Spitzen, der nach Norden und Süden zeigt.                                              |
| sizenwse         | Ein Pfeil mit zwei Spitzen, der auf Nordwest und Südost zeigt.                                      |
| SizeWE           | Ein Pfeil mit zwei Spitzen, der nach Westen und Osten zeigt.                                                |
| oben          | Vertikaler Pfeil nach oben.                                                             |
| \*. ani oder \* . cur | Alle. ani-oder. cur-Dateien (müssen sich in demselben Verzeichnis wie die WMS-Datei oder in der WMZ-Datei befinden). |



 

## <a name="remarks"></a>Bemerkungen

Zu Renderingzwecken ist System der Standard Cursor. Der Standardwert, der von diesem Attribut abgerufen wird, ist "" (leere Zeichenfolge).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Video-Element**](video-element.md)
</dt> </dl>

 

 





