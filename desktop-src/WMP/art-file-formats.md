---
title: Dateiformate für Die Bildart
description: Erfahren Sie mehr über die Dateiformate für Windows Media Player, die für Skins erkannt werden. Dazu gehören Bitmap, GIF, JPEG und PNG.
ms.assetid: 803479e8-0e00-4724-80b7-9d86709c43db
keywords:
- Windows Media Player skins,art files
- Skins,Art-Dateien
- Dateien für Skins,Art
- Artdateien für Skins,Dateiformate
- Windows Media Player Skins,Dateiformate für Die Technik
- Skins,Dateiformate für Die Technik
- Dateiformate für Skinart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95872ef6bf98f690841372471c8170439c2b44ac7d8ee8027e91f0372b4b4437
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573811"
---
# <a name="art-file-formats"></a>Dateiformate für Die Bildart

Die folgenden Dateiformate werden von der -Windows Media Player für Skins erkannt:



| Format                                  | Durchwahl   | BESCHREIBUNG                                                                                        |
|-----------------------------------------|-------------|----------------------------------------------------------------------------------------------------|
| Bitmap                                  | BMP        | Bitmapbilder werden empfohlen, da sie die größte Kontrolle über das genaue Bild und die Farben bieten. |
| GIF (Graphics Interchange Format)       | .gif        | Komprimiertes Bildformat, das für Webseiten verwendet wird. Animierte GIFs werden unterstützt.                            |
| JPEG (Joint Photographic Experts Group) | JPEG, JPG | Komprimiertes Bildformat, das für Webseiten verwendet wird.                                                         |
| PNG (Portable Network Graphics)         | .png        | Komprimiertes Bildformat, das für Webseiten verwendet wird.                                                         |



 

Wenn Sie eines der komprimierten Dateiformate verwenden, das eine Farbe als für einen Webbrowser transparent definiert, definieren Sie eine Farbe in der Bilddatei nicht als transparent. Verwenden Sie eine sichtbare Farbe, um transparente Bereiche im Bild zu darstellen, und definieren Sie diese Farbe dann in der Skindefinitionsdatei als transparent. Wenn Sie beispielsweise eine GIF-Datei mit einigen transparenten Bereichen erstellen, sind diese in Ihrem endgültigen Bild nicht transparent, und Sie können die Farbe, die Sie in Ihrer GIF-Datei als transparent festgelegt haben, nicht für die Transparenzfarbe in Ihrer Skin verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Art-Dateien**](art-files.md)
</dt> </dl>

 

 




