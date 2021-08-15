---
description: In diesem Thema werden die progressive Decodierung und die Verwendung der progressiven Decodierung in Anwendungen vorgestellt.
ms.assetid: d22c2c59-0fa1-4452-93f1-dbf151033714
title: Übersicht über die progressive Decodierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a409a337ecd3852a50cb5ca1a410ebd32c7f3226c79aacca20b10733e214fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710043"
---
# <a name="progressive-decoding-overview"></a>Übersicht über die progressive Decodierung

In diesem Thema werden die progressive Decodierung und die Verwendung der progressiven Decodierung in Anwendungen vorgestellt. Außerdem enthält sie Richtlinien zum Erstellen von Codecs, die die progressive Decodierung unterstützen.

Dieses Thema enthält folgende Abschnitte:

-   [Introduction (Einführung)](#introduction)
-   [Was ist progressive Decodierung?](#what-is-progressive-decoding)
-   [Unterstützung der progressiven Decodierung in Windows 7](#progressive-decoding-support-in-windows-7)
-   [PROGRESSIVE JPEG-Decodierung](#jpeg-progressive-decoding)
-   [Png-/GIF-Progressive Decodierung](#pnggif-progressive-decoding)
    -   [Progressive PNG-Decodierung](#png-progressive-decoding)
    -   [Progressive GIF-Decodierung](#gif-progressive-decoding)
-   [Progressive Decodierung in Anwendungen](#progressive-decoding-in-applications)
-   [Unterstützung benutzerdefinierter Codecs für die progressive Decodierung](#custom-codec-support-for-progressive-decoding)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Die progressive Decodierung bietet die Möglichkeit, Teile eines Bilds inkrementell zu decodieren und zu rendern, bevor der Download des gesamten Bilds abgeschlossen ist. Dieses Feature verbessert die Benutzerfreundlichkeit beim Anzeigen von Bildern aus dem Internet erheblich, da der Benutzer nicht warten muss, bis das gesamte Bild heruntergeladen wurde, bevor die Decodierung beginnen kann. Benutzer können eine Imagevorschau mit verfügbaren Daten anzeigen, lange bevor das gesamte Image heruntergeladen wird. Dieses Feature ist für jede Anwendung wichtig, die zum Anzeigen von Bildern aus dem Internet oder aus Datenquellen mit eingeschränkter Bandbreite verwendet wird.

Die Windows Imaging Component (WIC) in Windows 7 unterstützt die progressive Decodierung gängiger Bildformate wie JPEG, PNG und GIF. WIC unterstützt auch alle WIC-fähigen Nicht-Microsoft-Codecs, die progressive Decodierung implementieren. Die progressive Codierung wird in der aktuellen Version von WIC nicht unterstützt. In diesem Thema werden die progressive Decodierung in Windows 7 und das Verfahren zum Aktivieren der progressiven Decodierung in Ihren Anwendungen beschrieben.

## <a name="what-is-progressive-decoding"></a>Was ist progressive Decodierung?

Die progressive Decodierung ist die Möglichkeit, Teile eines Bilds inkrementell aus einer unvollständigen Bilddatei zu decodieren. Die herkömmliche Decodierung erfordert eine vollständige Bilddatei, bevor die Decodierung beginnen kann. Die progressive Decodierung beginnt, nachdem das Herunterladen einer progressiven Ebene eines Bilds abgeschlossen wurde. Der Decoder führt einen Decodierungsdurchlauf auf der aktuellen progressiven Ebene des Bilds aus. Anschließend werden mehrere Decodierungsdurchläufe für das Bild ausgeführt, während jede progressive Ebene heruntergeladen wird. Jeder Decodierungsdurchlauf zeigt einen größeren Teil des Bilds an, bis das Bild vollständig heruntergeladen und decodiert wurde. Die Anzahl von Durchläufen, die zum Decodieren eines vollständigen Bilds erforderlich sind, hängt vom Bilddateiformat und dem Codierungsprozess ab, der zum Erstellen des Bilds verwendet wird.

Bilder müssen speziell codiert werden, um die progressive Decodierung zu implementieren, aber nicht alle Bildformate unterstützen sie. In der folgenden Liste sind die Anforderungen für die Verwendung der progressiven Decodierung zusammengefasst.

-   Die Bilddatei muss die progressive Decodierung unterstützen. Die meisten Bildformate unterstützen keine progressive Decodierung, obwohl die gängigen Bildformate JPEG, PNG und GIF dies tun.
-   Die Bilddatei muss als progressives Bild codiert werden. Bilddateien, die nicht mit der progressiven Bildcodierung erstellt wurden, können keine progressive Decodierung implementieren, selbst wenn das Dateiformat dies andernfalls unterstützen würde.
-   Ein Codec, der die progressive Decodierung unterstützt, muss verfügbar sein. Wenn ein Codec keine progressive Decodierung unterstützt, wird ein als progressives Bild codiertes Bild als herkömmliches Bild decodiert.

## <a name="progressive-decoding-support-in-windows-7"></a>Unterstützung der progressiven Decodierung in Windows 7

Windows 7 bietet integrierte Codecs, die die progressive Decodierung für JPEG-, PNG- und GIF-Bildformate unterstützen. Jeder dieser Windows 7 Codecs führt mehrere Decodierungsdurchläufe für ein Bild durch. Jeder Durchlauf entspricht einer bestimmten Ebene und einem Teil des Bilds, das decodiert wird, was schließlich zu einem vollständig decodierten Bild führt.

Jedes Bildformat verarbeitet die progressive Decodierung auf andere Weise. Die folgende Tabelle enthält Informationen zur Anzahl der progressiven Ebenen und zur Decodierungsmethode, die von den Windows 7 Progressive Decoding-Formaten unterstützt wird. 

| Bildformat | Anzahl der unterstützten progressiven Ebenen | Progressive Decodierungsmethode |
|--------------|----------------------------------------|-----------------------------|
| JPEG         | Definiert durch Bild                       | Erhöhen der Auflösung       |
| PNG          | 7                                      | Interlacing                 |
| GIF          | 4                                      | Interlacing                 |



 

Darüber hinaus kann die progressive Decodierung in Codecs implementiert werden, indem unterstützung für progressive Schnittstellen und Methoden geboten wird. Wenn die progressive Decodierung in einem Codec nicht unterstützt wird, sollten entsprechende Fehlermeldungen zurückgegeben werden, wenn diese Methoden aufgerufen werden.

## <a name="jpeg-progressive-decoding"></a>PROGRESSIVE JPEG-Decodierung

Bei der progressiven JPEG-Decodierung werden Bilddaten in immer höheren Auflösungen für jede Ebene angezeigt, bis das Bild mit voller Auflösung verfügbar ist. Jede Ebene des Bilds wird so festgelegt, dass sie eine andere Auflösungsebene bereitstellt. Sobald mehr progressive Ebenen verfügbar sind, wird das Bild mit höheren Auflösungen angezeigt, bis das Bild mit vollständiger Auflösung aufgelöst wird.

Die Anzahl der verfügbaren Ebenen und die auf jeder Ebene festgelegte Auflösung hängen vollständig vom codierten JPEG ab. Die folgenden beiden Bilder zeigen ein Beispiel für die progressive JPEG-Decodierung auf zwei progressiven Ebenen.

![Beispiele für die progressive Jpeg-Decodierung](graphics/Progressive_JPEG_Comparison.jpg)

Das Bild auf der linken Seite wird auf progressiver Ebene 0 decodiert. Das Bild auf der rechten Seite wird nach fünf progressiven Ebenen vollständig decodiert.

## <a name="pnggif-progressive-decoding"></a>Png-/GIF-Progressive Decodierung

Sowohl die progressive PNG- als auch die GIF-Decodierung verwenden eine progressive Decodierungsmethode mit Zeilensprung. Der Decodierungsprozess für beide Formate ist sehr ähnlich.

### <a name="png-progressive-decoding"></a>Progressive PNG-Decodierung

PNG-Bilddateien bieten sieben progressive Ebenen für die Decodierung, wie in der PNG-Spezifikation beschrieben. Die progressive PNG-Decodierung wird implementiert, indem bei jedem Durchlauf des Decoders ein angegebenes Pixelmuster decodiert wird. Das Muster in der folgenden Tabelle aus der PNG-Spezifikation wird über das gesamte Bild repliziert. Jede Zahl stellt die progressive Ebene dar, in der das entsprechende Pixel decodiert wird.



|  &nbsp;  |  &nbsp;   |  &nbsp;   |  &nbsp;   |   &nbsp;  |  &nbsp;   |  &nbsp;   | &nbsp;    |
|-----|-----|-----|-----|-----|-----|-----|-----|
| 1   | 6   | 4   | 6   | 2   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 3   | 6   | 4   | 6   | 3   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |



 

In der obigen Tabelle können Sie die Pixel bestimmen, die mit jedem Durchlauf des Decoders decodiert werden. Im Gegensatz zum Windows 7 GIF-Codec repliziert der Windows 7 PNG-Codec das am weitesten links verfügbare Pixel in einer Scanzeile, um leere Pixel aufzufüllen.

Die folgenden Bilder zeigen ein Beispiel für den progressiven Decodierungscodec Windows 7 PNG auf drei progressiven Ebenen.

![Beispiele für die progressive PNG-Decodierung](graphics/PNG_Progressive_Comparison.jpg)

Das Bild oben links zeigt ein PNG-Bild, das auf progressiver Ebene 0 decodiert ist. Das Bild oben rechts zeigt das gleiche PNG-Bild, das auf progressiver Ebene 3 decodiert wurde. Das untere Bild zeigt das gleiche Bild, das nach 7 progressiven Ebenen vollständig decodiert wurde.

### <a name="gif-progressive-decoding"></a>Progressive GIF-Decodierung

GIF-Bilddateien bieten vier progressive Ebenen für die Decodierung, wie in der GIF-Spezifikation beschrieben. Jeder Durchlauf füllt bestimmte Zeilen innerhalb eines Bilds auf und erzeugt nach dem vierten Durchlauf ein vollständiges Bild. Die folgende Tabelle aus der GIF-Spezifikation zeigt, welche Scanzeilen durch jeden Durchlauf des Decoders decodiert werden. 

| Ebenennummer/Durchlaufnummer | Aufgefüllte Scanzeilen   | Starten der Scanzeile |
|---------------------------|------------------------|--------------------|
| 1                         | Jede achte Scanzeile | 0                  |
| 2                         | Jede achte Scanzeile | 4                  |
| 3                         | Jede vierte Scanzeile | 2                  |
| 4                         | Jede zweite Scanzeile | 1                  |



 

Obwohl Codecs den Inhalt leerer Pixel auf einer bestimmten Ebene angeben können, füllt der Windows GIF-Codec leere Scanzeilen auf, indem aufgefüllte Scanzeilen über der leeren Scanzeile repliziert werden.

## <a name="progressive-decoding-in-applications"></a>Progressive Decodierung in Anwendungen

Die wichtigste schnittstelle für die progressive Decodierung ist die [**IWICProgressiveLevelControl-Schnittstelle.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) Um einen Verweis auf die Schnittstelle abzurufen, fragen Sie einen Bildrahmen ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) nach **IWICProgressiveLevelControl** ab. Auf progressive Methoden kann dann über die -Schnittstelle zugegriffen werden.

Der folgende Code enthält ein Beispiel für die Verwendung der progressiven Decodierung in Anwendungen.


```
IWICProgressiveLevelControl *pProgressive = NULL;

HRESULT hr = (pBitmapFrame->QueryInterface(
   IID_IWICProgressiveLevelControl, 
   (void**) &pProgressive));
                
if (SUCCEEDED(hr))
{
   for (UINT uCurrentLevel = 0; SUCCEEDED(hr); uCurrentLevel++)
   {
      hr = pProgressive->SetCurrentLevel(uCurrentLevel);
               if (WINCODEC_ERR_INVALIDPROGRESSIVELEVEL == hr)
      {
         // No more levels
         break;
      }

      if (SUCCEEDED(hr))
      {
         // Output the current level
         hr = pBitmapFrame->CopyPixels(...);
      }                      
   }
}

if (pProgressive)
{
   pProgressive->Release();
}
```



Der vorangehende Code stellt die grundlegende Funktionalität bereit, die für die Implementierung der progressiven Decodierung in den meisten Anwendungen erforderlich ist. Mithilfe des Codes kann auf progressive Ebenen zugegriffen werden, sobald Bildpixeldaten verfügbar werden. Die [**SetCurrentLevel-Funktion**](/windows/desktop/api/Wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel) blockiert die Ausführung, bis die angeforderte Ebene verfügbar ist.

## <a name="custom-codec-support-for-progressive-decoding"></a>Unterstützung benutzerdefinierter Codecs für die progressive Decodierung

Codecentwickler können [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) implementieren, wenn ihre Bildformate die progressive Decodierung unterstützen. Die Unterstützung der progressiven Decodierung ist keine Voraussetzung für die Ermittlung und Vermittlung durch WIC. Die progressive Decodierung verbessert jedoch die Benutzerfreundlichkeit erheblich, und die Implementierung sollte nach Möglichkeit berücksichtigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Digitale Komprimierung und Codierung von Continuous-Tone Standbildern – Anforderungen und Richtlinien](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)
</dt> <dt>

[JPEG-Dateiaustauschformat](https://www.w3.org/Graphics/JPEG/jfif3.pdf)
</dt> <dt>

[GIF89a-Spezifikation](https://www.w3.org/Graphics/GIF/spec-gif89a.txt)
</dt> <dt>

[png-Spezifikation und -Erweiterungen (Portable Network Graphics)](http://www.libpng.org/pub/png/spec/)
</dt> </dl>

 

 



