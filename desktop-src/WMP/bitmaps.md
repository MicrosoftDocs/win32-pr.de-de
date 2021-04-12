---
title: Bitmaps (Windows Media Player SDK)
description: Bitmaps
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Windows Media Player Mobile Skins, Bitmaps
- Skins, Bitmaps
- Verweis für Skins, Bitmaps
- Bitmaps in Skins, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad690b691c22154bad4db0981e2b5ab760400b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474763"
---
# <a name="bitmaps-windows-media-player-sdk"></a>Bitmaps (Windows Media Player SDK)

Sie müssen ein oder mehrere Bilder in der Skin verwenden, und jedes Image muss in der Skin-Definitionsdatei definiert werden. Wenn Sie in diesem Abschnitt kein Bild definieren, kann es von der Skin nicht verwendet werden.

Der Begriff "Bitmap" wird in einem generischen Sinn in der gesamten Referenz verwendet und bezieht sich auf Bitmap-Bilder mit der Erweiterung. BMP, GIF-Bilder mit der Erweiterung GIF, JPEG-Bilder mit der Erweiterung JPG und PNG-Bilder mit der Erweiterung PNG.

Der Bitmaps-Abschnitt der Skin-Definitionsdatei beginnt mit der folgenden Zeile:


```C++
[ Bitmaps ]

```



Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen zu den einzelnen Bildern in der Skin enthalten.

Eine typische Zeile könnte wie folgt lauten:


```C++
    Background  Background.bmp  0,0

```



Sie können die folgende Vorlage für den Bitmaps-Abschnitt Ihrer Skin-Definitionsdatei verwenden:


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



Sie müssen die folgende Reihenfolge für Bitmapinformationen für jede Zeile im Bitmap-Abschnitt verwenden. Jeder Teil der Zeile ist erforderlich.

1.  [Bitmaptyp](bitmap-type.md)
2.  [Dateiname](file-name.md)
3.  [Koordinaten](coordinates.md)

Ein Beispiel für einen bitmapcode finden Sie unter [Sample Bitmap section](sample-bitmap-section.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




