---
description: Andere Quellobjekte
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Andere Quellobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8bbc1618cb7a76e87a4837fce3905a7c9ba7455b13297e779b8be8e80c40732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790910"
---
# <a name="other-source-objects"></a>Andere Quellobjekte

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Zusätzlich zu Video- und Audioquellen unterstützt [DirectShow Editing Services](directshow-editing-services.md) (DES) die folgenden Quellobjekte.

**Still Images**

DES unterstützt die folgenden Dateiformate für Still-Bilder:

-   Bitmap (.bmp)
-   GIF (Graphics Interchange Format)
-   JPEG (Joint Photographic Experts Group)
-   Targa oder Truevision-Grafikadapter (TGA): Modus 2 (unkomprimiertes RGB) im 16-Bit-, 24-Bit- oder 32-Bit-Format.

Diese Dateien können als Noch-Bilder oder zum Erstellen von Animationen verwendet werden. Wenn Sie für Bitmap-, JPEG- und Targa-Dateien die Datei als Stillbild verwenden, rufen Sie die [**IAMTimelineSrc::SetDefaultFPS-Methode**](iamtimelinesrc-setdefaultfps.md) auf, um die Bildfrequenz auf 0 (null) zu setzen.

**DIB-Sequenzen**

Bei einer Reihe von Bitmap-, JPEG- oder Targa-Dateien kann die Render-Engine eine DIB-Sequenz erstellen. Um eine DIB-Sequenz zu erstellen, geben Sie den Dateien numerisch sequenzielle Namen wie Image001.bmp, Image002.bmp, Image003.bmp und so weiter. Verwenden Sie die erste Datei in der Sequenz als Quelle. Legen Sie die Framerate für die Sequenz fest, indem [**Sie IAMTimelineSrc::SetDefaultFPS aufrufen.**](iamtimelinesrc-setdefaultfps.md) Die Render-Engine durchfing die Bilder in der Sequenz mit der angegebenen Bildfrequenz.

Wenn die Sequenz zu kurz ist, um die Dauer bei der Framerate zu füllen, ist der Rest der Dauer voll schwarz. Während des Renderings tritt kein Fehler auf.

**GIF-Quellen**

DES unterstützt GIF-Quellen, einschließlich animierter und transparenter GIFs, mithilfe der GIF89a-Spezifikation. Bei einem animierten GIF müssen Sie im Gegensatz zu den anderen Dateitypen die Bildfrequenz nicht festlegen. Die GIF-Datei gibt die Verzögerung zwischen den einzelnen Bildern in der Animation an.

Um transparente GIFs zu unterstützen, konvertiert DES transparente Bereiche im Bild in das RGB-Triplet RGB(0,0,0). Sie können dann den Schlüsselübergang [zum](key-transition.md) Schlüssel für RGB(0,0,0) verwenden.

DES konvertiert auch alle schwarzen Bereiche, die innerhalb des Bereichs RGB(0–7,0–7,0–7) liegen, in den Wert RGB(8,8,8) – mit Ausnahme des Transparenzindexes, wenn er in diesen Bereich fällt. Diese Konvertierung ist für die Augen nicht erkennbar.

**Videofarbquelle**

Das [Video Color Source-Objekt](video-color-source.md) erstellt ein fortlaufendes Videobild einer Volltonfarbe. Eine Verwendung für dieses Objekt besteht im Erstellen einer Ebene in einem Übergang. Verwenden Sie sie z. B. in einem Ein- oder Ausblenden eines Videos.

**Benutzerdefinierte Quellfilter**

DES kann einen DirectShow-Quellfilter als Zeitachsenquelle verwenden, wenn der Filter die folgenden Bedingungen erfüllt:

-   Es unterstützt such-
-   Es erzeugt ein Format, das DES unterstützt. Das Format kann komprimiert werden, solange das System des Benutzers über einen DirectShow-Filter verfügt, der es decodieren kann.

Um eine benutzerdefinierte Quelle zu verwenden, geben Sie die CLSID des Filters als Unterobjekt-GUID des Quellobjekts an. Weitere Informationen finden Sie unter [Unterobjekte.](subobjects.md) Um benutzerdefinierte Eigenschaften zu unterstützen, implementieren Sie sie als "put"-Eigenschaften von **IDispatch.** Nur statische Eigenschaften werden für Quellobjekte unterstützt. dynamische Eigenschaften werden nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Quellen](working-with-sources.md)
</dt> </dl>

 

 



