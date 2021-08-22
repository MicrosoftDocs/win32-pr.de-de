---
description: Unterstützung für IWICDevelopRaw
ms.assetid: 8e8ff65b-0849-42e0-924e-2a7c61d4b1bb
title: Unterstützung für IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6436eb9d9422da6f5a29c196df10c97014df6beff178bb584b70e45d207dd50d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709730"
---
# <a name="support-for-iwicdevelopraw"></a>Unterstützung für IWICDevelopRaw

Um Anwendungen die Unterstützung der RAW-Verarbeitung zu ermöglichen, wird Codecautoren dringend empfohlen, alle Parameter von [**IWICDevelopRaw zu implementieren.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Für Windows 7 erfordert Windows Imaging Component (WIC) Unterstützung für [**alle IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)- . Wenn Ihr Dateiformat nicht alle diese Parameter unterstützt, sollten Sie das Bilddateiformat überarbeiten.

Um die grundlegende RAW-Verarbeitung in Anwendungen zu ermöglichen, müssen Codecs Anpassungen an der Belichtung (ExposureCompensationSupport) und der Farbe (z. B. KelvinWhitePointSupport und TintSupport) unterstützen. Darüber hinaus wird die Ausgabe in bestimmte Farbräume und Pixelformate dringend empfohlen. Unterstützung für andere Anpassungen wird natürlich empfohlen und ist für Windows 7 erforderlich.

Der RAW-Codec muss grundlegende Unterstützung für die Bildrotation und schnelle Vorschau bereitstellen. Die Drehung kann auf zwei unterschiedliche Arten angegeben werden:

-   [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) Diese Methode legt den gewünschten Drehwinkel für die Ausgabe nachfolgender Aufrufe von [**CopyPixels fest.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) Der Aufrufer kann die Option dstTransform festlegen, um den gewünschten Drehwinkel anzugeben.

Diese beiden Ansätze unterscheiden sich auf folgende Weise:

-   Nur [**IWICDevelopRaw-Einstellungen**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) können über Instanzen des Decoderobjekts hinweg beibehalten werden.
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) gilt nur für diesen bestimmten Aufruf; es gibt keineRlei Persistenz.
-   [**IWICDevelopRaw ermöglicht**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) eine wesentlich feiner abgrenzende Steuerung der Drehung. [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) ist auf 90-Grad-Inkremente beschränkt.

Wenn rotation sowohl in [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) als auch [**in IWICBitmapSourceTransform angegeben**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)ist, ist der Rotationseffekt kumulativ. Wenn [**ALSOICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) beispielsweise eine Drehung um 25 Grad angibt und [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) eine Drehung um 90 Grad angibt, sollte Folgendes geschehen:

-   Aufrufe [**von IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) sollten eine Drehung um 25 Grad anwenden (d. h. nur den in [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)angegebenen Betrag).
-   Aufrufe [**von IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) mit einer dstTransform-Menge von 90 führen dann zu einer Drehung um 115 Grad (25 + 90).
-   Auch hier kann nur die über [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) angegebene Drehung um 25 Grad beibehalten werden.

In Windows Vista können Aufrufer mit den [**METHODEN IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) und [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) eingebettete Miniaturansichten bzw. Vorschaubilder erhalten. Diese sollen vorab berechnete Vorschauen und Miniaturansichten aus dem Bilddateistream zurückgeben. Das Generieren von Vorschauversionen oder Miniaturansichten "on the fly" führt zu einer schlechten Leistung im Windows Explorer und Bildanzeige. Der Codec muss auch eine Möglichkeit bieten, ein aktualisiertes Bild mit Bildschirmauflösung schnell zurück zu geben, wenn Benutzer die Verarbeitungseinstellungen interaktiv steuern.

Aufrufe [**von IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) bestimmt, welche nachfolgenden Aufrufe von [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) zurückgeben (entweder durch Geschwindigkeit oder Qualität). Darüber hinaus kann die IWICBitmapSourceTransform-Schnittstelle verwendet werden, um zu bestimmen, ob downsampling erforderlich ist, und kann die Leistung erhöhen, wenn es angewendet werden kann. Die Farbgenauigkeit aller Bilder sollte vergleichbar sein. Wenn Änderungen an den Verarbeitungseinstellungen vorgenommen werden, sollten alle diese Renderings die Änderungen widerspiegeln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC Guidelines for Camera RAW Image Formats](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



