---
description: Das Thema enthält eine Einführung in den Bitmap-Decoder, eine Windows Imaging Component-Kernkomponente (WIC), die zum Decodieren von Bilddateien aus einem Stream verwendet wird.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: 'Decodierung: Übersicht'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a15e6a9c914cfa220e1aad5bff4badeb8fc8cc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349869"
---
# <a name="decoding-overview"></a>Decodierung: Übersicht

Das Thema enthält eine Einführung in den Bitmap-Decoder, eine Windows Imaging Component-Kernkomponente (WIC), die zum Decodieren von Bilddateien aus einem Stream verwendet wird.

Dieses Thema enthält folgende Abschnitte:

-   [Introduction (Einführung)](#introduction)
-   [Native Bitmap-decoderer](#native-bitmap-decoders)
-   [Erstellen eines Bitmap-Decoders](#creating-a-bitmap-decoder)
-   [Decodererweiterbarkeit](#decoder-extensibility)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

BitmapDecoder können als äußerer Container eines digitalen Bilds angezeigt werden und bieten Zugriff auf globale Eigenschaften und Bild Frames. Einige Bildformate unterstützen globale Miniaturansichten, Vorschau Versionen, Farb Kontexte oder Metadaten, während andere diese Eigenschaften nur auf Frame-Ebene bereitstellen. Beachten Sie jedoch, dass viele der Standardbild Formate diese globalen Eigenschaften nicht unterstützen. Daher unterstützen viele der systemeigenen Codec-Implementierungen, die von WIC bereitgestellt werden, nicht die Mehrzahl dieser globalen Eigenschaften. Weitere Informationen zur Unterstützung von globalen Eigenschaften finden Sie in der Tabelle im Abschnitt Native Bitmap-Decoders dieses Themas.

In WIC werden Bitmap-Decoder durch die [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Schnittstelle dargestellt und ermöglichen den Zugriff auf diese globalen Eigenschaften der Bitmap und, was noch wichtiger ist, die darin enthaltenen Frames. Die [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Schnittstelle stellt einen einzelnen BitmapFrame dar und wird in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md)ausführlich erläutert.

## <a name="native-bitmap-decoders"></a>Native Bitmap-decoderer

WIC stellt mehrere systemeigene Implementierungen der [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Schnittstelle für die Standardweb Bildformate und das High Dynamic Range HD Photo-Format bereit. In der folgenden Tabelle sind die verfügbaren systemeigenen Decoders, der Klassen Bezeichnername und die Unterstützung für globale Eigenschaften aufgelistet. Obwohl eine Funktion eine Eigenschaft, z. b. Miniaturansichten auf globaler Ebene, nicht unterstützt, kann das Bildformat solche Eigenschaften auf der einzelnen Frame Ebene unterstützen.



| Bildformat | CLSID-Name            | Miniaturbilder | Vorschau | Farb Kontexte | Metadaten |
|--------------|-----------------------|------------|----------|----------------|----------|
| BMP          | CLSID \_ wicbmpdecoder  | Nein         | Nein       | Nein             | Nein       |
| GIF          | CLSID- \_ wicgifdecoder  | Nein         | Nein       | Nein             | Ja      |
| ICO          | CLSID- \_ wicikodecoder  | Nein         | Nein       | Nein             | Nein       |
| JPEG         | CLSID \_ wicjpgdecoder | Nein         | Nein       | Nein             | Nein       |
| PNG          | CLSID- \_ wicpngdecoder  | Nein         | Nein       | Nein             | Nein       |
| TIFF         | CLSID \_ wictiffdecoder | Nein         | Nein       | Nein             | Nein       |
| HD-Foto     | CLSID \_ wicwmpdecoder  | Nein         | Ja      | Nein             | Nein       |



 

## <a name="creating-a-bitmap-decoder"></a>Erstellen eines Bitmap-Decoders

Zum Decodieren eines Bilds mit WIC müssen Sie zunächst eine Instanz des [**iwicbitmapdecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) für das Ziel Bildformat erstellen. Die decoderinstanz ermöglicht Ihnen den Zugriff auf die globalen Eigenschaften und Metadaten, sofern dies unterstützt wird, sowie auf die Bildframes. Die WIC Imaging Factory, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), bietet verschiedene Methoden zum Erstellen von bitmapdecodern. Die folgenden Factorymethoden werden zum Erstellen von Bitmap-Decodern bereitgestellt.

-   [**Bilderstellungsfactory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [**"Kreatedecoderfromfilehandle"**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [**"Kreatedecoderfromfilename"**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [**"Kreatedecoderfromstream"**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

Der folgende Code veranschaulicht, wie ein Bitmap-Decoder mit einem Bilddateinamen erstellt und der erste Frame des Bilds abgerufen wird.


```C++
   // Create a decoder
   IWICBitmapDecoder *pDecoder = NULL;

   hr = m_pIWICFactory->CreateDecoderFromFilename(
       szFileName,                      // Image to be decoded
       NULL,                            // Do not prefer a particular vendor
       GENERIC_READ,                    // Desired read access to the file
       WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
       &pDecoder                        // Pointer to the decoder
       );

   // Retrieve the first frame of the image from the decoder
   IWICBitmapFrameDecode *pFrame = NULL;

   if (SUCCEEDED(hr))
   {
       hr = pDecoder->GetFrame(0, &pFrame);
   }
```



## <a name="decoder-extensibility"></a>Decodererweiterbarkeit

Eines der wichtigsten Features von WIC ist ein Erweiterbarkeits Framework, mit dem Codec-Entwickler ihre eigenen Bild Codecs entwickeln und die gleiche Platt Form Unterstützung wie die systemeigenen Implementierungen von Bild Codecs erhalten können. Für alle Bildverarbeitung wird unabhängig vom Bildformat ein einzelner, einheitlicher Satz von Schnittstellen verwendet. Jede Anwendung, die WIC verwendet, erhält automatische Unterstützung für neue Bildformate, sobald der Codec installiert ist. Weitere Informationen zur Codec-Entwicklung finden Sie in den Themen unter [Komponentenentwicklung](-wic-component-development.md). Weitere Informationen zur decoderentwicklung finden Sie unter [Implementieren eines WIC-Enabled Decoders](-wic-implementingwicdecoder.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über die Codierung](-wic-creating-encoder.md)
</dt> <dt>

[Komponentenentwicklung](-wic-component-development.md)
</dt> </dl>

 

 



