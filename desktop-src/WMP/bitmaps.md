---
title: Bitmaps (Windows Media Player SDK)
description: Bitmaps
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Windows Media Player Mobile Skins, Bitmaps
- Skins, Bitmaps
- Referenz für Skins,Bitmaps
- Bitmaps in Skins,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ff4689c052162d8addfb9a66aeb6b227916f0e22e21de3e3572ea265380664
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123860"
---
# <a name="bitmaps-windows-media-player-sdk"></a>Bitmaps (Windows Media Player SDK)

Sie müssen ein oder mehrere Bilder in Ihrer Skin verwenden, und jedes Bild muss in der Skindefinitionsdatei definiert werden. Wenn Sie in diesem Abschnitt kein Bild definieren, kann Ihr Skin es nicht verwenden.

Der Begriff "Bitmap" wird in der gesamten Referenz allgemein verwendet und bezieht sich auf Bitmapbilder mit einer .bmp-Erweiterung, GIF-Bilder mit einer .gif-Erweiterung, JPEG-Bilder mit einer .jpg-Erweiterung und PNG-Bilder mit einer .png-Erweiterung.

Der Abschnitt Bitmaps der Skindefinitionsdatei beginnt mit dieser Zeile:


```C++
[ Bitmaps ]

```



Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen zu den einzelnen Bildern in Ihrer Skin enthalten.

Eine typische Zeile kann sein:


```C++
    Background  Background.bmp  0,0

```



Sie können die folgende Vorlage für den Abschnitt Bitmaps Ihrer Skindefinitionsdatei verwenden:


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



Sie müssen die folgende Reihenfolge für Bitmapinformationen für jede Zeile im Abschnitt Bitmap verwenden. Jeder Teil der Zeile ist erforderlich.

1.  [Bitmaptyp](bitmap-type.md)
2.  [Dateiname](file-name.md)
3.  [Koordinaten](coordinates.md)

Ein Beispiel für Bitmapcode finden Sie im [Abschnitt Beispielbitmap](sample-bitmap-section.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




