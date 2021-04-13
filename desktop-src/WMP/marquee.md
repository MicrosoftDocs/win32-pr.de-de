---
title: Marquee
description: Marquee
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Windows Media Player Mobile Skins, marquees
- Skins, marquees
- Referenz für Skins, marquees
- marquees in Skins, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388541"
---
# <a name="marquee"></a>Marquee

Ein Marquee ist ein Bild Lauf Text-Anzeige Feld, in dem Informationen von einem oder mehreren Textanzeige Feldern angezeigt werden. Sie müssen kein Marquee hinzufügen, aber es kann sehr nützlich sein, wenn Sie ausführliche Informationen haben, die Sie dem Benutzer in begrenztem Raum anzeigen möchten.

Der Text im Marquee führt nur dann einen Bildlauf durch, wenn die beiden folgenden Bedingungen erfüllt sind:

-   Sie haben mehr Text, der im Marquee angezeigt werden soll als die Breite des Marquee-Anzeige Felds.
-   Das Medien Element wird entweder beendet oder angehalten.

Der Marquee-Abschnitt der Skin-Definitionsdatei muss mit der folgenden Zeile beginnen:


```C++
[ Marquee ]

```



> [!Note]  
> Um die Kompatibilität mit Versionen von Windows Media Player Mobile zu gewährleisten, die älter als Windows Media Player 10 Mobile sind, wird die Verwendung von "Marquis" in einer Skin-Definitionsdatei weiterhin als gültig betrachtet.

 

Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen zu jedem der Marquee-Anzeigefelder in der Skin enthalten.


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



Sie können die folgende Vorlage für den Marquee-Abschnitt Ihrer Skin-Definitionsdatei verwenden:


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



Sie müssen die folgende Reihenfolge für Informationen in den einzelnen Zeilen des Marquee-Abschnitts verwenden (jeder Teil der Zeile ist erforderlich):

1.  [Marquee-Speicherort](marquee-location.md)
2.  [Marquee-Schriftart](marquee-font.md)
3.  [Marquee-Farbe](marquee-color.md)
4.  [Text Kombinationen](text-combinations.md)

Ein Beispiel für einen Marquee-Code finden Sie unter [Sample Marquee section](sample-marquee-section.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




