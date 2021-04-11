---
description: Unterstützung für IWICDevelopRaw
ms.assetid: 8e8ff65b-0849-42e0-924e-2a7c61d4b1bb
title: Unterstützung für IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa39aa339a3cd21c7ffa848a5ab1fe2dd6426981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217370"
---
# <a name="support-for-iwicdevelopraw"></a>Unterstützung für IWICDevelopRaw

Um es Anwendungen zu ermöglichen, die Rohverarbeitung zu unterstützen, werden Codec-Autoren dringend empfohlen, alle Parameter von [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)zu implementieren. Für Windows 7 benötigt Windows Imaging Component (WIC) Unterstützung für alle [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)-Komponenten. Wenn das Dateiformat nicht alle diese Parameter unterstützt, sollten Sie das Bild Dateiformat überarbeiten.

Um die grundlegende Rohverarbeitung in-Anwendungen zu ermöglichen, müssen Codecs Anpassungen an der verfügbar machung (exposurecompensationsupport) und Farbe (z. b. kelvinwhitepointsupport und tintsupport) unterstützen. Darüber hinaus wird die Ausgabe an bestimmte Farb-und Pixel Formate dringend empfohlen. Die Unterstützung für andere Anpassungen ist natürlich empfehlenswert und für Windows 7 erforderlich.

Der unformatierte Codec muss grundlegende Unterstützung für die Bilddrehung und die schnelle Vorschau bereitstellen. Die Drehung kann auf zwei verschiedene Arten angegeben werden:

-   [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**abtrotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) -Methode. Diese Methode legt den gewünschten Drehungs Winkel für die Ausgabe von nachfolgenden Aufrufen an [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)fest.
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) -Methode. Der Aufrufer kann die dsttransform-Option festlegen, um den gewünschten Drehungs Winkel anzugeben.

Diese beiden Ansätze unterscheiden sich wie folgt:

-   Nur [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Einstellungen können über Instanzen des Decoder-Objekts hinweg beibehalten werden.
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) gilt nur für diesen speziellen-Befehl. Es gibt keine Persistenz jeglicher Art.
-   [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) bietet eine wesentlich präzisere Steuerung der Drehung. [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) ist auf 90-Grad-Inkremente beschränkt.

Wenn Drehung sowohl in [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) als auch in [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)angegeben ist, ist der Drehungs Effekt kumulativ. Wenn [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) z. b. eine 25-Grad-Rotation angibt und [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) eine 90-Grad-Drehung angibt, sollte Folgendes geschehen:

-   Aufrufe von [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) sollten eine 25-Grad-Drehung anwenden (d. h. nur die in [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)angegebene Menge).
-   Aufrufe von [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) mit einem dsttransform-Betrag von 90 führen dann zu einer Rotation von 115 Grad (25 + 90).
-   Auch hier kann nur die über [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**abkultation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) angegebene 25-Grad-Drehung persistent gespeichert werden.

In Windows Vista können Aufrufer durch die [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) -und [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) -Methode eingebettete Miniaturansichten bzw. Vorschau Bilder erhalten. Diese sollen vorab berechnete Vorschauen und Miniaturansichten aus dem Bilddatei-Stream zurückgeben. Das dynamische Erstellen von Vorschauen oder Miniaturansichten führt zu einer schlechten Leistung in Windows-Explorer und Foto-Viewer. Der Codec muss auch eine Möglichkeit bieten, ein aktualisiertes Bildschirm Auflösungs Bild schnell zurückzugeben, wenn Benutzer die Verarbeitungseinstellungen interaktiv steuern.

Aufrufe von [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**setrendermode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) bestimmen, welche nachfolgenden Aufrufe von [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) zurückgeben (positiv oder Qualität). Darüber hinaus kann die IWICBitmapSourceTransform-Schnittstelle verwendet werden, um zu bestimmen, ob ein Verkleinerung notwendig ist, und kann die Leistung erhöhen, wenn Sie angewendet werden kann. Die Farb Treue aller Bilder sollte vergleichbar sein. Wenn Änderungen an den Verarbeitungseinstellungen vorgenommen werden, sollten alle diese Renderings die Änderungen widerspiegeln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC-Richtlinien für Kamera Rohbild Formate](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



