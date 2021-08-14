---
description: In diesem Thema wird die progressive Decodierung und die Verwendung der progressiven Decodierung in Anwendungen beschrieben.
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

In diesem Thema wird die progressive Decodierung und die Verwendung der progressiven Decodierung in Anwendungen beschrieben. Außerdem enthält er Richtlinien zum Erstellen von Codecs, die die progressive Decodierung unterstützen.

Dieses Thema enthält folgende Abschnitte:

-   [Introduction (Einführung)](#introduction)
-   [Was ist progressive Decodierung?](#what-is-progressive-decoding)
-   [Unterstützung für progressive Decodierung in Windows 7](#progressive-decoding-support-in-windows-7)
-   [PROGRESSIVE JPEG-Decodierung](#jpeg-progressive-decoding)
-   [Progressive PNG/GIF-Decodierung](#pnggif-progressive-decoding)
    -   [Progressive PNG-Decodierung](#png-progressive-decoding)
    -   [Progressive GIF-Decodierung](#gif-progressive-decoding)
-   [Progressive Decodierung in Anwendungen](#progressive-decoding-in-applications)
-   [Unterstützung benutzerdefinierter Codecs für die progressive Decodierung](#custom-codec-support-for-progressive-decoding)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Die progressive Decodierung bietet die Möglichkeit, Teile eines Bilds inkrementell zu decodieren und zu rendern, bevor das gesamte Bild heruntergeladen wurde. Dieses Feature verbessert die Benutzerfreundlichkeit beim Anzeigen von Bildern aus dem Internet erheblich, da der Benutzer nicht warten muss, bis das gesamte Bild heruntergeladen wird, bevor die Decodierung beginnen kann. Benutzer können eine Imagevorschau mit verfügbaren Daten sehen, lange bevor das gesamte Image heruntergeladen wird. Dieses Feature ist wichtig für jede Anwendung, die zum Anzeigen von Bildern aus dem Internet oder aus Datenquellen mit begrenzter Bandbreite verwendet wird.

Die Windows Imaging Component (WIC) in Windows 7 unterstützt die progressive Decodierung beliebter Bildformate wie JPEG, PNG und GIF. WIC unterstützt auch alle WIC-fähigen Nicht-Microsoft-Codecs, die progressive Decodierung implementieren. Progressive Codierung wird in der aktuellen Version von WIC nicht unterstützt. In diesem Thema werden die progressive Decodierung in Windows 7 und das Verfahren zum Aktivieren der progressiven Decodierung in Ihren Anwendungen beschrieben.

## <a name="what-is-progressive-decoding"></a>Was ist progressive Decodierung?

Die progressive Decodierung ist die Möglichkeit, Teile eines Bilds inkrementell aus einer unvollständigen Bilddatei zu decodieren. Die herkömmliche Decodierung erfordert eine vollständige Bilddatei, bevor die Decodierung beginnen kann. Die progressive Decodierung beginnt, nachdem das Herunterladen einer progressiven Ebene eines Images abgeschlossen wurde. Der Decoder führt einen Decodierungspass auf der aktuellen progressiven Ebene des Bilds aus. Anschließend werden mehrere Decodierungsüberläufe für das Image beim Herunterladen der einzelnen progressiven Ebenen durchführt. Bei jedem Decodierungspass werden weitere Bilder angezeigt, bis das Bild vollständig heruntergeladen und decodiert wurde. Die Anzahl der zum Decodieren eines vollständigen Bilds erforderlichen Durchläufe hängt vom Bilddateiformat und dem Codierungsprozess ab, der zum Erstellen des Bilds verwendet wird.

Bilder müssen speziell codiert werden, um die progressive Decodierung zu implementieren, aber nicht alle Bildformate unterstützen sie. In der folgenden Liste sind die Anforderungen für die Verwendung der progressiven Decodierung zusammengefasst.

-   Die Bilddatei muss die progressive Decodierung unterstützen. Die meisten Bildformate unterstützen keine progressive Decodierung, obwohl die gängigen Bildformate JPEG, PNG und GIF dies tun.
-   Die Bilddatei muss als progressives Image codiert werden. Bilddateien, die nicht mit der progressiven Bildcodierung erstellt wurden, können keine progressive Decodierung implementieren, selbst wenn das Dateiformat dies andernfalls unterstützen würde.
-   Ein Codec, der die progressive Decodierung unterstützt, muss verfügbar sein. Wenn ein Codec keine progressive Decodierung unterstützt, wird ein als progressives Bild codiertes Bild als herkömmliches Bild decodiert.

## <a name="progressive-decoding-support-in-windows-7"></a>Unterstützung für progressive Decodierung in Windows 7

Windows 7 bietet integrierte Codecs, die die progressive Decodierung für JPEG-, PNG- und GIF-Bildformate unterstützen. Jeder dieser Windows 7 Codecs führt mehrere Decodierungsüberläufe für ein Bild aus. Jeder Durchgang entspricht einer bestimmten Ebene und einem Teil des Bilds, der decodiert wird, was schließlich zu einem vollständig decodierten Bild führt.

Jedes Bildformat behandelt die progressive Decodierung auf unterschiedliche Weise. Die folgende Tabelle enthält Informationen zur Anzahl der progressiven Ebenen und zur Decodierungsmethode, die von den Windows 7 progressiven Decodierungsformaten unterstützt wird. 

| Bildformat | Anzahl der unterstützten progressiven Ebenen | Progressive Decodierungsmethode |
|--------------|----------------------------------------|-----------------------------|
| JPEG         | Definiert durch Image                       | Erhöhen der Auflösung       |
| PNG          | 7                                      | Interlacing                 |
| GIF          | 4                                      | Interlacing                 |



 

Darüber hinaus kann die progressive Decodierung in Codecs implementiert werden, indem unterstützung für progressive Schnittstellen und Methoden zur Verfügung steht. Wenn die progressive Decodierung in einem Codec nicht unterstützt wird, sollten entsprechende Fehlermeldungen zurückgegeben werden, wenn diese Methoden aufgerufen werden.

## <a name="jpeg-progressive-decoding"></a>PROGRESSIVE JPEG-Decodierung

Die progressive JPEG-Decodierung stellt Bilddaten mit immer höheren Auflösungen für jede Ebene bereit, bis das Bild mit voller Auflösung verfügbar ist. Jede Ebene des Images wird so festgelegt, dass sie eine andere Auflösungsebene bietet. Wenn progressivere Ebenen verfügbar werden, wird das Bild mit höheren Auflösungen angezeigt, bis das Bild mit voller Auflösung aufgelöst wird.

Die Anzahl der verfügbaren Ebenen und die auf jeder Ebene festgelegten Auflösung hängen vollständig von der codierten JPEG-Datei ab. Die folgenden beiden Abbildungen zeigen ein Beispiel für die progressive JPEG-Decodierung auf zwei progressiven Ebenen.

![Beispiele für die progressive JPEG-Decodierung](graphics/Progressive_JPEG_Comparison.jpg)

Das Bild auf der linken Seite wird auf progressiver Ebene 0 decodiert. Das Bild auf der rechten Seite wird nach fünf progressiven Ebenen vollständig decodiert.

## <a name="pnggif-progressive-decoding"></a>Progressive PNG/GIF-Decodierung

Für die progressive PNG- und GIF-Decodierung wird eine progressive Decodierungsmethode mit Interlacing verwendet. Der Decodierungsprozess für beide Formate ist sehr ähnlich.

### <a name="png-progressive-decoding"></a>Progressive PNG-Decodierung

PNG-Bilddateien bieten sieben progressive Ebenen für die Decodierung, wie in der PNG-Spezifikation beschrieben. Die progressive PNG-Decodierung wird implementiert, indem bei jedem Durchgang des Decoders ein angegebenes Pixelmuster decodiert wird. Das Muster in der folgenden Tabelle aus der PNG-Spezifikation wird über das gesamte Bild repliziert. Jede Zahl stellt die progressive Ebene dar, in der das entsprechende Pixel decodiert wird.



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



 

In der obigen Tabelle können Sie die Pixel bestimmen, die bei jedem Durchgang des Decoders decodiert werden. Im Gegensatz zum Windows 7-GIF-Codec repliziert der Windows 7-PNG-Codec das am linken Ende verfügbare Pixel auf einer Scanzeile, um leere Pixel zu füllen.

Die folgenden Abbildungen zeigen ein Beispiel für den Windows 7 PNG-Codec für die progressive Decodierung auf drei progressiven Ebenen.

![Beispiele für die progressive PNG-Decodierung](graphics/PNG_Progressive_Comparison.jpg)

Das Bild oben links zeigt ein PNG-Bild, das auf progressiver Ebene 0 decodiert ist. Das bild oben rechts zeigt das gleiche PNG-Bild, das auf progressiver Ebene 3 decodiert wurde. Das untere Bild zeigt das gleiche Bild, das nach sieben progressiven Ebenen vollständig decodiert wurde.

### <a name="gif-progressive-decoding"></a>Progressive GIF-Decodierung

GIF-Bilddateien bieten vier progressive Ebenen für die Decodierung, wie in der GIF-Spezifikation beschrieben. Jeder Durchgang füllt bestimmte Zeilen innerhalb eines Bilds auf und erzeugt nach dem vierten Durchgang ein vollständiges Bild. Die folgende Tabelle aus der GIF-Spezifikation zeigt, welche Scanzeilen bei jedem Durchgang des Decoders decodiert werden. 

| Levelnummer/Passnummer | Aufgefüllte Scanzeilen   | Starten der Scanzeile |
|---------------------------|------------------------|--------------------|
| 1                         | Jede achte Scanzeile | 0                  |
| 2                         | Jede achte Scanzeile | 4                  |
| 3                         | Jede vierte Scanzeile | 2                  |
| 4                         | Jede zweite Scanzeile | 1                  |



 

Obwohl Codecs den Inhalt leerer Pixel auf einer bestimmten Ebene angeben können, füllt der Windows GIF-Codec leere Scanzeilen auf, indem er aufgefüllte Scanzeilen über der leeren Scanzeile repliziert.

## <a name="progressive-decoding-in-applications"></a>Progressive Decodierung in Anwendungen

Die wichtigste Schnittstelle für die progressive Decodierung ist [**die IWICProgressiveLevelControl-Schnittstelle.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) Um einen Verweis auf die Schnittstelle zu erhalten, fragen Sie einen Bildrahmen ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) für **IWICProgressiveLevelControl ab.** Auf progressive Methoden kann dann über die -Schnittstelle zugegriffen werden.

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



Der vorangehende Code stellt die grundlegende Funktionalität zur Verfügung, die für die Implementierung der progressiven Decodierung in den meisten Anwendungen erforderlich ist. Mithilfe des Codes kann auf progressive Ebenen zugegriffen werden, wenn Bildpixeldaten verfügbar werden. Die [**SetCurrentLevel-Funktion**](/windows/desktop/api/Wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel) blockiert die Ausführung, bis die angeforderte Ebene verfügbar ist.

## <a name="custom-codec-support-for-progressive-decoding"></a>Unterstützung benutzerdefinierter Codecs für die progressive Decodierung

Codec-Entwickler können sich für die Implementierung [**von IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) entscheiden, wenn ihre Bildformate die progressive Decodierung unterstützen. Die Unterstützung der progressiven Decodierung ist keine Voraussetzung für die Ermittlung und Vermittlung durch WIC. Die progressive Decodierung verbessert jedoch die Benutzerfreundlichkeit stark, und die Implementierung sollte nach Möglichkeit berücksichtigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Digitale Komprimierung und Codierung Continuous-Tone Still Images – Anforderungen und Richtlinien](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)
</dt> <dt>

[JPEG-Dateiaustauschformat](https://www.w3.org/Graphics/JPEG/jfif3.pdf)
</dt> <dt>

[GIF89a-Spezifikation](https://www.w3.org/Graphics/GIF/spec-gif89a.txt)
</dt> <dt>

[Portable Network Graphics (PNG) – Spezifikation und Erweiterungen](http://www.libpng.org/pub/png/spec/)
</dt> </dl>

 

 



