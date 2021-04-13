---
title: Kunst Dateiformate
description: Kunst Dateiformate
ms.assetid: 803479e8-0e00-4724-80b7-9d86709c43db
keywords:
- Windows Media Player Skins, Grafikdateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, Dateiformate
- Windows Media Player Skins, Dateiformate für Kunst
- Skins, Dateiformate für Kunst
- Dateiformate für Skin Art
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a35af72fd502cb23e81063fe9513b4a9311f9557
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311357"
---
# <a name="art-file-formats"></a>Kunst Dateiformate

Die folgenden Kunst Dateiformate werden von Windows Media Player für Skins erkannt:



| Format                                  | Durchwahl   | BESCHREIBUNG                                                                                        |
|-----------------------------------------|-------------|----------------------------------------------------------------------------------------------------|
| Bitmap                                  | BMP        | Bitmapbilder werden empfohlen, da Sie die höchste Kontrolle über das exakte Bild und die Farben bieten. |
| GIF (Graphics Interchange Format)       | .gif        | Für Webseiten verwendetes komprimiertes Bildformat. Animierte Gifs werden unterstützt.                            |
| JPEG (Joint Photographic Experts Group) | JPEG, JPG | Für Webseiten verwendetes komprimiertes Bildformat.                                                         |
| PNG (Portable Network Graphics)         | .png        | Für Webseiten verwendetes komprimiertes Bildformat.                                                         |



 

Wenn Sie eines der komprimierten Dateiformate verwenden, das eine Farbe für einen Webbrowser als transparent definiert, definieren Sie in der Bilddatei keine Farbe als transparent. Verwenden Sie eine sichtbare Farbe, um transparente Bereiche im Bild darzustellen, und definieren Sie dann diese Farbe in der Skin-Definitionsdatei als transparent. Wenn Sie z. b. eine GIF-Datei mit einigen Bereichen transparent erstellen, sind Sie in ihrem endgültigen Bild nicht transparent, und Sie können die Farbe, die Sie in ihrer GIF-Datei als transparent festgelegt haben, nicht als Transparenz Farbe in der Skin verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Kunstdateien**](art-files.md)
</dt> </dl>

 

 




