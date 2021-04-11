---
description: In diesem Thema wird die Progressive Decodierung und die Verwendung progressiver Decodierung in-Anwendungen vorgestellt.
ms.assetid: d22c2c59-0fa1-4452-93f1-dbf151033714
title: Übersicht über Progressive Decodierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf005dfb5b4cf5a69ca45020776fee9f0641eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217376"
---
# <a name="progressive-decoding-overview"></a>Übersicht über Progressive Decodierung

In diesem Thema wird die Progressive Decodierung und die Verwendung progressiver Decodierung in-Anwendungen vorgestellt. Außerdem enthält es Richtlinien zum Erstellen von Codecs, die eine progressive Decodierung unterstützen.

Dieses Thema enthält folgende Abschnitte:

-   [Introduction (Einführung)](#introduction)
-   [Was ist progressiv-Decodierung?](#what-is-progressive-decoding)
-   [Unterstützung progressiver Decodierung in Windows 7](#progressive-decoding-support-in-windows-7)
-   [Progressive JPEG-Decodierung](#jpeg-progressive-decoding)
-   [Fortschreitende PNG/GIF-Decodierung](#pnggif-progressive-decoding)
    -   [PNG-Progressive Decodierung](#png-progressive-decoding)
    -   [Progressive GIF-Decodierung](#gif-progressive-decoding)
-   [Progressive Decodierung in Anwendungen](#progressive-decoding-in-applications)
-   [Unterstützung für die benutzerdefinierte Codec-Unterstützung](#custom-codec-support-for-progressive-decoding)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Die Progressive Decodierung bietet die Möglichkeit, Teile eines Bilds inkrementell zu decodieren und zu Rendering, bevor das gesamte Bild heruntergeladen wird. Diese Funktion verbessert die Benutzer Funktionalität beim Anzeigen von Images aus dem Internet erheblich, da der Benutzer nicht warten muss, bis das gesamte Image heruntergeladen wird, bevor die Decodierung beginnen kann. Benutzern kann eine Bildvorschau mit verfügbaren Daten angezeigt werden, bevor das gesamte Image heruntergeladen wird. Diese Funktion ist für alle Anwendungen, die zum Anzeigen von Images aus dem Internet oder für Datenquellen mit eingeschränkter Bandbreite verwendet werden, von entscheidender Bedeutung.

Die Windows Imaging Component (WIC) in Windows 7 unterstützt das Progressive decodieren beliebter Bildformate, wie z. b. JPEG, PNG und GIF. WIC unterstützt auch alle WIC-aktivierten nicht-Microsoft-Codecs, die eine progressive Decodierung implementieren. Progressive Codierung wird in der aktuellen Version von WIC nicht unterstützt. In diesem Thema wird das Progressive decodieren in Windows 7 und das Verfahren zum Aktivieren der progressiven Decodierung in Ihren Anwendungen erläutert.

## <a name="what-is-progressive-decoding"></a>Was ist progressiv-Decodierung?

Progressives decodieren ist die Möglichkeit, Teile eines Bilds inkrementell aus einer unvollständigen Bilddatei zu decodieren. Herkömmliche Decodierung erfordert eine komplette Bilddatei, bevor die Decodierung beginnen kann. Die Progressive Decodierung startet, nachdem eine progressive Ebene eines Bilds den Download abgeschlossen hat. Der Decoder führt einen Decodierungs Durchlauf für die aktuelle Progressive Ebene des Bilds durch. Anschließend werden mehrere Decodierungs Durchgänge für das Bild durchführt, wenn jede Progressive Ebene heruntergeladen wird. Jeder Decodierungs Durchlauf zeigt mehr von dem Bild an, bis das Bild vollständig heruntergeladen und decodiert wurde. Die Anzahl der zum Decodieren eines vollständigen Bilds erforderlichen Schritte hängt vom Bild Dateiformat und dem Codierungsprozess ab, der zum Erstellen des Images verwendet wurde.

Bilder müssen speziell codiert werden, um eine progressive Decodierung zu implementieren, aber nicht alle Bildformate unterstützen Sie. In der folgenden Liste sind die Anforderungen für die Verwendung der progressiven Decodierung zusammengefasst

-   Die Bilddatei muss die Progressive Decodierung unterstützen. Die meisten Bildformate unterstützen keine Progressive Decodierung, obwohl das beliebte Bildformat JPEG, PNG und GIF tut.
-   Die Bilddatei muss als progressives Bild codiert werden. Bilddateien, die nicht mit der progressiven Bildcodierung erstellt wurden, können keine Progressive Decodierung implementieren, auch wenn das Dateiformat Sie andernfalls unterstützen würde.
-   Ein Codec, der die Progressive Decodierung unterstützt, muss verfügbar sein. Wenn ein Codec keine Progressive Decodierung unterstützt, wird ein als progressives Bild codiertes Bild als herkömmliches Bild decodiert.

## <a name="progressive-decoding-support-in-windows-7"></a>Unterstützung progressiver Decodierung in Windows 7

Windows 7 bietet integrierte Codecs, die eine progressive Decodierung für Bildformate von JPEG, PNG und GIF unterstützen. Jede dieser Windows 7-Codecs führt mehrere Decodierung für ein Abbild aus. Jeder Durchlauf entspricht einer bestimmten Ebene und einem Teil des Bilds, das decodiert wird, was schließlich zu einem vollständig decodierten Bild führt.

Jedes Bildformat behandelt die Progressive Decodierung auf andere Weise. In der folgenden Tabelle finden Sie Informationen zur Anzahl der progressiven Ebenen und der Decodierungs Methode, die von den progressiven Windows 7-Decodierung unterstützt wird. 

| Bildformat | Anzahl unterstützter Stufen | Progressive Decodierungs Methode |
|--------------|----------------------------------------|-----------------------------|
| JPEG         | Definiert durch Image                       | Erhöhen der Auflösung       |
| PNG          | 7                                      | Zeilen Sprung                 |
| GIF          | 4                                      | Zeilen Sprung                 |



 

Außerdem kann die Progressive Decodierung in Codecs implementiert werden, indem Unterstützung für Progressive Schnittstellen und Methoden bereitgestellt wird. Wenn eine progressive Decodierung nicht in einem Codec unterstützt wird, sollten entsprechende Fehlermeldungen zurückgegeben werden, wenn diese Methoden aufgerufen werden.

## <a name="jpeg-progressive-decoding"></a>Progressive JPEG-Decodierung

Die Progressive JPEG-Decodierung stellt Bilddaten in immer höheren Auflösungen für jede Ebene dar, bis das voll auflösende Image verfügbar ist. Jede Ebene des Bilds wird so festgelegt, dass eine andere Auflösungsebene bereitgestellt wird. Wenn progressivere Ebenen verfügbar werden, wird das Bild bei einer höheren Auflösung angezeigt, bis das Bild der vollständigen Auflösung aufgelöst ist.

Die Anzahl der verfügbaren Ebenen und die auf jeder Ebene festgelegte Auflösung hängen vollständig vom codierten JPEG ab. Die beiden folgenden Abbildungen zeigen ein Beispiel für eine progressive JPEG-Decodierung auf zwei progressiven Ebenen.

![Beispiele für die Progressive JPEG-Decodierung](graphics/Progressive_JPEG_Comparison.jpg)

Das Bild auf der linken Seite wird auf progressiver Ebene 0 decodiert. Das Bild auf der rechten Seite wird nach fünf progressiven Ebenen vollständig decodiert.

## <a name="pnggif-progressive-decoding"></a>Fortschreitende PNG/GIF-Decodierung

Sowohl PNG-als auch GIF-, Progressive Der Decodierungs Prozess für beide Formate ist sehr ähnlich.

### <a name="png-progressive-decoding"></a>PNG-Progressive Decodierung

PNG-Bilddateien bieten sieben Progressive Ebenen für die Decodierung, wie in der PNG-Spezifikation beschrieben. Die demokratische PNG-Decodierung wird implementiert, indem ein angegebenes Pixelmuster bei jedem Durchlauf des Decoders decodiert wird. Das Muster in der folgenden Tabelle aus der PNG-Spezifikation wird über das gesamte Image repliziert. Jede Zahl stellt die Progressive Ebene dar, in der das entsprechende Pixel decodiert wird.



|     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|
| 1   | 6   | 4   | 6   | 2   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 3   | 6   | 4   | 6   | 3   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |



 

In der obigen Tabelle können Sie die Pixel ermitteln, die bei jedem Durchlauf des Decoders decodiert werden. Im Gegensatz zum Windows 7-GIF-Codec repliziert der Windows 7 PNG-Codec das auf der linken Seite Verfügbare Pixel in einer Überprüfungs Zeile, um leere Pixel aufzufüllen.

Die folgenden Abbildungen zeigen ein Beispiel für den Windows 7 PNG-Codec für die Progressive Decodierung auf drei progressiven Ebenen.

![Beispiele für die Progressive PNG-Decodierung](graphics/PNG_Progressive_Comparison.jpg)

Das Bild oben links zeigt ein PNG-Bild, das auf progressiv Ebene 0 decodiert wurde. Das Bild oben rechts zeigt das gleiche PNG-Bild an, das auf progressiv Ebene 3 decodiert wurde. Das untere Bild zeigt das Bild, das nach 7 progressiven Ebenen vollständig decodiert wurde.

### <a name="gif-progressive-decoding"></a>Progressive GIF-Decodierung

GIF-Bilddateien bieten vier Progressive Ebenen für die Decodierung, wie in der GIF-Spezifikation beschrieben. Jeder Durchlauf füllt bestimmte Zeilen innerhalb eines Bilds auf und erzeugt nach dem vierten Durchlauf ein vollständiges Bild. Die folgende Tabelle der GIF-Spezifikation zeigt, welche Scan Zeilen von jedem Durchlauf des Decoders decodiert werden. 

| Anzahl der Ebenen/Passnummern | Ausgefüllten Zeilen überprüfen   | Scan Zeile wird gestartet |
|---------------------------|------------------------|--------------------|
| 1                         | Jede achte Überprüfungs Zeile | 0                  |
| 2                         | Jede achte Überprüfungs Zeile | 4                  |
| 3                         | Jede vierte Scanzeile | 2                  |
| 4                         | Jede zweite Scan Zeile | 1                  |



 

Obwohl Codecs den Inhalt von leeren Pixeln auf einer bestimmten Ebene angeben kann, füllt der Windows GIF-Codec leere Überprüfungs Zeilen durch Replizieren von gefüllten Scan Zeilen oberhalb der leeren Überprüfungs Linie auf.

## <a name="progressive-decoding-in-applications"></a>Progressive Decodierung in Anwendungen

Die wichtigste Progressive Decodierungs Schnittstelle ist die [**iwicprogressivelevelcontrol**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) -Schnittstelle. Um einen Verweis auf die-Schnittstelle zu erhalten, Fragen Sie einen Bildframe ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) für **iwicprogressivelevelcontrol** ab. Auf Progressive Methoden kann dann über die-Schnittstelle zugegriffen werden.

Der folgende Code enthält ein Beispiel für die Verwendung von progressiver Decodierung in-Anwendungen.


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



Der vorangehende Code stellt die grundlegenden Funktionen bereit, die für die Implementierung progressiver Decodierung in den meisten Anwendungen Mit dem Code können Sie auf Progressive Ebenen zugreifen, wenn Bildpixeldaten verfügbar werden. Die [**setcurrentlevel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel) -Funktion blockiert die Ausführung, bis die angeforderte Ebene verfügbar ist.

## <a name="custom-codec-support-for-progressive-decoding"></a>Unterstützung für die benutzerdefinierte Codec-Unterstützung

Codec-Entwickler können das [**iwicprogressivelevelcontrol**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) -Element implementieren, wenn Ihre Bildformate eine progressive Decodierung unterstützen. Die Unterstützung für die Progressive Decodierung ist keine Voraussetzung für die Ermittlung und die Schiedsgerichtsbarkeit durch WIC. Durch die Progressive Decodierung wird jedoch die Benutzer Leistung erheblich gesteigert, und die Implementierung sollte nach Möglichkeit in Erwägung gezogen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Digitale Komprimierung und Codierung von Continuous-Tone weiterhin Images: Anforderungen und Richtlinien](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)
</dt> <dt>

[JPEG-Dateiaustausch Format](https://www.w3.org/Graphics/JPEG/jfif3.pdf)
</dt> <dt>

[GIF89a-Spezifikation](https://www.w3.org/Graphics/GIF/spec-gif89a.txt)
</dt> <dt>

[Spezifikation und Erweiterungen für Portable Network Graphics (PNG)](http://www.libpng.org/pub/png/spec/)
</dt> </dl>

 

 



