---
description: Andere Quell Objekte
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Andere Quell Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747049"
---
# <a name="other-source-objects"></a>Andere Quell Objekte

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Zusätzlich zu Video-und Audioquellen unterstützt [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) die folgenden Quell Objekte.

**Bilder**

Des unterstützt die folgenden Dateiformate für weiterhin Images:

-   Bitmap (.bmp)
-   GIF (Graphics Interchange Format)
-   JPEG (Joint Photographic Experts Group)
-   Targa-oder Truevision-Grafik Adapter (. TGA): Modus 2 (unkomprimiertes RGB) im 16-Bit-, 24-Bit-oder 32-Bit-Format.

Diese Dateien können als Bilder oder zum Erstellen von Animationen verwendet werden. Wenn Sie die Datei für Bitmap-, JPEG-und Targa-Dateien als Image verwenden, müssen Sie die [**iamtimelinesrc:: setdefaultfps**](iamtimelinesrc-setdefaultfps.md) -Methode aufrufen, um die Framerate auf 0 (null) festzulegen.

**DIB-Sequenzen**

Bei einer Reihe von Bitmap-, JPEG-oder Targa-Dateien kann die Renderingengine eine DIB-Sequenz erstellen. Zum Erstellen einer DIB-Sequenz müssen Sie den Dateien numerische sequenzielle Namen wie Image001.bmp, Image002.bmp, Image003.bmp usw. zuordnen. Verwenden Sie die erste Datei in der Sequenz als Quelle. Legen Sie die Framerate für die Sequenz fest, indem Sie [**iamtimelinesrc:: setdefaultfps**](iamtimelinesrc-setdefaultfps.md)aufrufen. Die Renderingengine durchläuft die Bilder in der Sequenz mit der angegebenen Framerate.

Wenn die Sequenz zu kurz ist, um die Dauer bei Angabe der Framerate auszufüllen, ist der Rest der Dauer solide schwarz. Während des Renderings tritt kein Fehler auf.

**GIF-Quellen**

Des unterstützt GIF-Quellen, einschließlich animierter und transparenter GIFs, mithilfe der GIF89a-Spezifikation. Bei einem animierten GIF müssen Sie im Gegensatz zu anderen Dateitypen die Framerate nicht festlegen. Die GIF-Datei gibt die Verzögerung zwischen den einzelnen Bildern in der Animation an.

Zur Unterstützung transparenter-GIFs konvertiert des die transparenten Bereiche im Bild in den RGB-triplergb (0,0). Anschließend können Sie den [Schlüssel Übergang](key-transition.md) zu Key auf RGB (0,0) verwenden.

Der konvertiert außerdem alle schwarzen Bereiche, die im Bereich RGB (0 – 7, 0 – 7, 0 – 7) liegen, in den Wert RGB (8, 8, 8) – mit Ausnahme des Transparenz Indexes, wenn er in diesen Bereich fällt. Diese Konvertierung ist im Augenblick nicht erkennbar.

**Video Farbquelle**

Das [Video Farb Quellen](video-color-source.md) -Objekt erstellt ein kontinuierliches Video Bild einer voll Tonfarbe. Eine Verwendung für dieses Objekt besteht darin, es zu einer Ebene in einem Übergang zu machen. Verwenden Sie diese z. b. in einem Video, das ein-oder ausgeblendet wird.

**Benutzerdefinierte Quell Filter**

Des kann einen DirectShow-Quell Filter als Zeitachsen Quelle verwenden, wenn der Filter die folgenden Bedingungen erfüllt:

-   Es unterstützt Suchvorgänge
-   Sie erzeugt ein Format, das von unterstützt wird. Das Format kann komprimiert werden, solange das System des Benutzers über einen DirectShow-Filter verfügt, der ihn decodieren kann.

Wenn Sie eine benutzerdefinierte Quelle verwenden möchten, geben Sie die CLSID des Filters als untergeordnete GUID des Quell Objekts an. Weitere Informationen finden Sie unter unter [geordnete Objekte](subobjects.md). Um benutzerdefinierte Eigenschaften zu unterstützen, implementieren Sie Sie als **IDispatch** -"Put"-Eigenschaften. Nur statische Eigenschaften werden für Quell Objekte unterstützt. dynamische Eigenschaften werden nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Quellen](working-with-sources.md)
</dt> </dl>

 

 



