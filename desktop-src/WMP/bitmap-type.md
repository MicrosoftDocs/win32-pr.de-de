---
title: Bitmaptyp
description: Bitmaptyp
ms.assetid: 208df4b9-d1be-49ff-bc0b-2e000608e9c7
keywords:
- Windows Media Player Mobile Skins, Bitmaps
- Skins, Bitmaps
- Verweis für Skins, Bitmaps
- Bitmaps in Skins, Typen
- Bitmaps in Skins, Werte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602a436b5f4428b897672607265098104a9c1b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856111"
---
# <a name="bitmap-type"></a>Bitmaptyp

In der folgenden Tabelle sind die Werte aufgeführt, die für den Bitmaptyp gültig sind. Nur der Hintergrundtyp ist erforderlich. andere sind optional und beziehen sich auf verschiedene Verwendungsmöglichkeiten von Bildern.



| Wert       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hintergrund  | Erforderlich. Das Bild, auf dem alle Schaltflächen Bilder überlagert werden. Die Dimensionen des Basis Hintergrund Bilds enthalten die vollständige Breite und Höhe des Bildschirms. Dies ist auch die Datei, in der Bilder für die natürlichen Zustände von Schaltflächen und trackbars angezeigt werden. (Die Schaltflächen per pushübertragung und deaktiviert sind nicht Teil dieses Bilds.)                                                                                                                                                                                                                                                                                           |
| Disabled    | Erforderlich. Gibt an, dass das Drücken der Schaltfläche keine Auswirkung hat. Definiert ein Bild, das angezeigt wird, wenn für den Benutzer eine bestimmte Player-Funktionalität nicht verfügbar ist. Sie müssen einen Koordinaten Wert angeben, um die linke obere Ecke dieses Bilds in Relation zum Hintergrundbild anzugeben.                                                                                                                                                                                                                                                                                                                |
| Übertragen      | Erforderlich. Definiert ein Bild, das angezeigt wird, wenn der Benutzer eine Schaltfläche drückt. Verwenden Sie pushübertragung, um dem Benutzer visuelles Feedback zu geben, wenn er auf eine Schaltfläche tippt. Sie müssen einen Koordinaten Wert angeben, um die linke obere Ecke dieses Bilds in Relation zum Hintergrundbild anzugeben.                                                                                                                                                                                                                                                                                                                              |
| Region      | Definiert Bilder, die farbige Bereiche verwenden, um den Tap-Response-Bereich für die Treffer Typen-Schaltflächen darzustellen: pushhit, togglehit, 2pushhit. Wenn Sie die Schaltflächen für den Treffer-Typ verwenden, müssen Sie ein Regions Bild bereitstellen. Diese Bilddatei verwendet für jedes Steuerelement bestimmte Windows-Palettenfarben. Die Farben werden durch Zahlen definiert, die den Wert von rot, grün und blau für den Bereich darstellen. Dieses Bild wird dem Benutzer nie angezeigt. Sie müssen auch einen Koordinaten Wert angeben, um die linke obere Ecke dieses Bilds in Relation zum Hintergrundbild anzugeben.                                                      |
| Seekthumb   | Definiert ein Bild, das in Verbindung mit einer TrackBar verwendet wird, um die aktuelle Position im Medien Element anzugeben. Wenn ein Titel z. b. die Hälfte der Wiedergabe hat, wird das seekthumb-Bild in der Mitte der TrackBar angezeigt. Durch Tippen und ziehen des seekthumb-Bilds kann der Benutzer das Medien Element an jeder beliebigen Position neu starten, die als " *Suchen*" bezeichnet wird. Das Bild der TrackBar selbst wird im Hintergrundbild definiert. Das seekthumb-Bild ist nicht im Bitmaps-Abschnitt der Skin-Definitionsdatei enthalten, sondern wird im Abschnitt trackbars als Teil der TrackBar-Definition angegeben. |
| Super       | Definiert das deaktivierte Bild für eine TrackBar. Sie kann auch alternative Bilder für die stumm Schaltfläche enthalten.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Volumethumkehr | Definiert ein Bild, das in Verbindung mit einer TrackBar verwendet werden soll, um die volumeposition anzugeben. Wenn Sie das volumethumb-Image tippen und ziehen, kann der Benutzer die Volumeebene ändern. Das Bild der TrackBar selbst wird im Hintergrundbild definiert. Das volumethbib-Image ist nicht im Bitmaps-Abschnitt der Skin-Definitionsdatei enthalten, sondern wird im Abschnitt trackbars als Teil der TrackBar-Definition angegeben.                                                                                                                                                                                      |



 

> [!Note]  
> Die Typen "Region" und "Super Bitmap" sind in Skins für Windows Media Player 10 Mobile oder höher veraltet.

 

Beachten Sie, dass der Dateiname und der Dateityp nicht notwendigerweise identisch sind. Sie können die gepushte Datei beliebig angleichen, aber Sie wird immer noch an anderen Stellen als per Pushvorgang bezeichnet. Im Schaltflächen Abschnitt haben Sie z. b. ein Element wie z. b.:


```C++
Pushed @ 50,60

```



Dies bezieht sich auf den Typ der Datei, nicht auf den Dateinamen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Bitmaps**](bitmaps.md)
</dt> </dl>

 

 




