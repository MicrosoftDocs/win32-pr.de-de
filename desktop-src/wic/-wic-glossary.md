---
description: Definiert Begriffe, die in WIC verwendet werden.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Glossar der Windows Imaging-Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6812024571727c8f769df88f8233119eed13ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368859"
---
# <a name="windows-imaging-component-glossary"></a>Glossar der Windows Imaging-Komponente

## <a name="b"></a>B

<dl> <dt>

**Bittiefe**
</dt> <dd>

Die Anzahl der Farbwerte, die einem einzelnen Pixel in einem Bild zugewiesen werden können. Die Farbtiefe kann zwischen 1 Bit (schwarz und weiß) und 32 Bits (über 16,7 Millionen Farben) liegen. Siehe auch: Farbtiefe

</dd> <dt>

**Bits pro Pixel (BPP)**
</dt> <dd>

Die Anzahl der Bits, die den Farbwert der einzelnen Pixel in einem digitalisierten Bild darstellen. Siehe auch: BPP

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Clipper**
</dt> <dd>

Ein iwicbitmapclipperobjekt.

</dd> <dt>

**Codec**
</dt> <dd>

Ein Filter, der einen Datenstrom komprimiert (codiert) oder dekomprimiert (decodiert).

</dd> <dt>

**Farb Kontext**
</dt> <dd>

Eine Abstraktion für ein Farbprofil. Das Profil kann aus einer Datei geladen werden (d.h. "sRGB Color Space Profile. ICM") oder aus einem Arbeitsspeicher Puffer, der durchlesen abgerufen wird. Farb Kontextinformationen werden von der IWICColorContext-Schnittstelle für WIC definiert und mit der GetColorContext-Methode abgerufen.

</dd> <dt>

**Farb Transformation**
</dt> <dd>

Zuordnung von Farben aus dem Quell Farb Kontext zum Ziel Farb Kontext in einem vorgegebenen Ausgabe Pixel Format.

</dd> <dt>

**CYMK-Farbmodell**
</dt> <dd>

Mehrdimensionaler farbiger farbiger Bereich, der aus den Intensitäten Cyan, Magenta, gelb und schwarz besteht, die eine bestimmte Farbe bilden.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**der**
</dt> <dd>

Siehe anderen Begriff: Codec

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**ASA**
</dt> <dd>

Siehe anderen Begriff: Codec

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**verlustfreie**
</dt> <dd>

Ein Komprimierungstyp, mit dem sichergestellt wird, dass die ursprünglichen Daten genau wieder hergestellt werden können, ohne dass die Bildqualität verloren geht.

</dd> <dt>

**verlustbehafteten**
</dt> <dd>

Ein Prozess zum Komprimieren von Daten, bei denen Informationen, die als unnötig erachtet werden, entfernt und bei der Dekomprimierung nicht wieder hergestellt werden können Wird in der Regel mit Audiodaten und visuellen Daten verwendet, bei denen eine geringfügige Verschlechterung der Qualität akzeptabel ist.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**Multithread-Apartment (MTA)**
</dt> <dd>

Eine Form von Multithreading, die von Component Object Model (com) unterstützt wird. In einem Multithread-Apartment Modell befinden sich alle Threads im Prozess, die als "freigegeben" initialisiert wurden, in einem einzigen Apartment.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**Natives Pixel Format**
</dt> <dd>

Eines der Pixel Formate, die von WIC bereitgestellt werden, wobei das Speicher Layout der einzelnen Pixel in einer Bitmap beschrieben wird.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**Messer**
</dt> <dd>

Ein Satz von Farben, die von einem Objekt oder einer Anwendung verwendet werden.

</dd> <dt>

**Foto-metadatenrichtlinie**
</dt> <dd>

Die Windows-Richtlinie zum Lesen, schreiben und Entfernen von Bild Metadaten.

</dd> <dt>

**Pixelformat**
</dt> <dd>

Größe und Anordnung von Pixel Farbkomponenten im Arbeitsspeicher. Sie wird durch die Gesamtzahl der pro Pixel verwendeten Bits und die Anzahl der Bits angegeben, die zum Speichern der roten, grünen, blauen und Alpha Komponenten der Farbe verwendet werden. Beispielsweise verwendet das RGB24-Pixel-Format 24 Bits zum Speichern einer Pixelfarbe mit jeweils acht Bits für Rot, grün und blau. Das ARGB32-Pixel Format verwendet 32 Bits mit 24 Bits an Farbinformationen und 8 Bits von Alphakanal Informationen.

</dd> <dt>

**Progressive Decodierung**
</dt> <dd>

Der Prozess für das Decodieren von Bildern, die mit Informationen über die verschiedenen Decodierungs Ebenen codiert wurden.

</dd> </dl>

## <a name="s"></a>E

<dl> <dt>

**Streich**
</dt> <dd>

Bezieht sich auf eine IStream-com-Schnittstelle, die zum sequenziellen lesen oder Schreiben von Daten in Dateien, Arbeitsspeicher oder Netzwerkspeicher Orte verwendet werden kann.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**Tonkurve**
</dt> <dd>

Ein in digitaler Fotografie verwendetes Diagramm, das den klanglichen Bereich des Bilds anzeigt.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Windows Imaging-Komponente (WIC)**
</dt> <dd>

Eine erweiterbare Plattform, die eine Low-Level-API für digitale Images bereitstellt.

</dd> </dl>

 

 



