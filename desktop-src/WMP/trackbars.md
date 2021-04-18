---
title: Trackbars
description: Trackbars
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Windows Media Player Mobile Skins, trackbars
- Skins, trackbars
- Verweis für Skins, trackbars
- trackbars in Skins, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb7b64f7bada6f927b25aeecb71d584aa1ec2a68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340230"
---
# <a name="trackbars"></a>Trackbars

Eine TrackBar zeigt ein Bild an, das in kleinen Schritten geändert wird. Trackbars werden für volumensteuerelemente und Wiedergabe Positions Steuerelemente verwendet. Mithilfe von trackbars können Sie Informationen zum aktuellen Medien Element anzeigen oder den Benutzern die Möglichkeit geben, Einstellungen oder Wiedergabe Positionen zu ändern. Beispielsweise können Sie eine TrackBar verwenden, um dem Benutzer das Anpassen des Volumes und eine weitere TrackBar zu ermöglichen, die dem Benutzer die aktuelle Wiedergabe Position anzeigen kann. Trackbars verfügen über ein Thumb-Bild, das die aktuelle Einstellung des TrackBar-Werts definiert.

Der trackbars-Abschnitt der Skin-Definitionsdatei muss mit der folgenden Zeile beginnen:


```C++
[ Trackbars ]

```



Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen zu den einzelnen trackbars in der Skin enthalten.


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



Sie können die folgende Vorlage für den trackbars-Abschnitt Ihrer Skin-Definitionsdatei verwenden:


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



Sie müssen die folgende Reihenfolge für die TrackBar-Informationen für jede Zeile im Abschnitt trackbars verwenden (jeder Teil der Zeile ist erforderlich):

1.  [TrackBar-Typ](trackbar-type.md)
2.  [Position der TrackBar](trackbar-location.md)
3.  [Bildquelle für deaktivierte TrackBar](image-source-for-disabled-trackbar.md)
4.  [Ziehpunkt Bildquelle](thumb-image-source.md)
5.  [Thumb-Größe](thumb-size.md)

Ein Beispiel für trackbars-Code finden Sie im [Abschnitt "Beispiel trackbars](sample-trackbars-section.md)".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




