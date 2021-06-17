---
title: Dateiformate für Die Bildart
description: Erfahren Sie mehr über die Dateiformate, Windows Media Player für Skins erkannt werden. Dazu gehören Bitmap, GIF, JPEG und PNG.
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
ms.openlocfilehash: 2b525bc316d6a9901e32e51a54b6fb938fa91208
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262212"
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

 

 




