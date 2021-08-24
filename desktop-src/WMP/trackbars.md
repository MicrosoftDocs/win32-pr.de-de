---
title: Trackbars
description: Trackbars
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Windows Media Player Mobile Skins, Trackbars
- Skins, Trackbars
- Referenz für Skins, Trackbars
- Trackbars in Skins,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb311994ccdfb48eb1ea9e010b268cdef13fd1fc8a2154d491f6e4103a91ec3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762670"
---
# <a name="trackbars"></a>Trackbars

Eine Trackleiste zeigt ein Bild an, das sich in kleinen Schritten ändert. Trackbars werden für Lautstärke- und Wiedergabepositionssteuerelemente verwendet. Sie können Trackleisten verwenden, um Informationen zum aktuellen Medienelement anzuzeigen oder dem Benutzer das Ändern von Einstellungen oder der Wiedergabeposition zu ermöglichen. Beispielsweise können Sie eine Trackleiste verwenden, um dem Benutzer das Anpassen des Volumes zu ermöglichen, und eine andere Trackleiste, die dem Benutzer die aktuelle Wiedergabeposition anzeigen kann. Trackleisten verfügen über ein Fingerabdruckbild, das die aktuelle Einstellung des Trackbarwerts definiert.

Der Abschnitt Trackbars der Skindefinitionsdatei muss mit dieser Zeile beginnen:


```C++
[ Trackbars ]

```



Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen zu den einzelnen Trackbars in Ihrer Skin enthalten.


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



Sie können die folgende Vorlage für den Abschnitt Trackbars Ihrer Skindefinitionsdatei verwenden:


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



Sie müssen die folgende Reihenfolge für Trackbarinformationen für jede Zeile im Abschnitt Trackbars verwenden (jeder Teil der Zeile ist erforderlich):

1.  [Trackbar-Typ](trackbar-type.md)
2.  [Trackbar-Position](trackbar-location.md)
3.  [Bildquelle für deaktivierte Trackleiste](image-source-for-disabled-trackbar.md)
4.  [Thumb Image Source](thumb-image-source.md)
5.  [Thumb Size](thumb-size.md)

Ein Beispiel für Trackbars-Code finden Sie im [Abschnitt "Beispiel-Trackleisten".](sample-trackbars-section.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




