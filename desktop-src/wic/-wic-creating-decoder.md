---
description: In diesem Thema wird der Bitmapdecoder vorgestellt, eine Kerncodeckomponente Windows Imaging Component (WIC), die zum Decodieren von Bilddateien aus einem Stream verwendet wird.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: Übersicht über die Decodierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14300c9857702ceff5f07fcc127a4ef4182f9e77ad46f0598edc12abf91f240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711403"
---
# <a name="decoding-overview"></a>Übersicht über die Decodierung

In diesem Thema wird der Bitmapdecoder vorgestellt, eine Kerncodeckomponente Windows Imaging Component (WIC), die zum Decodieren von Bilddateien aus einem Stream verwendet wird.

Dieses Thema enthält folgende Abschnitte:

-   [Introduction (Einführung)](#introduction)
-   [Native Bitmap-Decoder](#native-bitmap-decoders)
-   [Erstellen eines Bitmap-Decoders](#creating-a-bitmap-decoder)
-   [Decodererweiterbarkeit](#decoder-extensibility)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Bitmapdecoder können als äußerer Container eines digitalen Bilds angezeigt werden und bieten Zugriff auf globale Eigenschaften und Bildrahmen. Einige Bildformate unterstützen globale Miniaturansichten, Vorschauen, Farbkontexte oder Metadaten, während andere diese Eigenschaften nur auf Frameebene bereitstellen. Beachten Sie jedoch, dass viele der Standardbildformate diese globalen Eigenschaften nicht unterstützen. Daher unterstützen viele der nativen Codecimplementierungen, die von WIC bereitgestellt werden, den Großteil dieser globalen Eigenschaften nicht. Informationen zur Unterstützung globaler Eigenschaften finden Sie in der Tabelle im Abschnitt Native Bitmap Decoder dieses Themas.

In WIC werden Bitmapdecoder durch die [**IWICBitmapDecoder-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) dargestellt und bieten Zugriff auf diese globalen Eigenschaften der Bitmap und vor allem auf die darin enthaltenen Frames. Die [**IWICBitmapFrameDecode-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) stellt einen einzelnen Bitmaprahmen dar und wird in der [Übersicht über Bitmapquellen](-wic-bitmapsources.md)ausführlich erläutert.

## <a name="native-bitmap-decoders"></a>Native Bitmap-Decoder

WIC bietet mehrere native Implementierungen der [**IWICBitmapDecoder-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) für die Standard-Webbildformate und das HD Photo-Format mit hohem dynamischen Bereich. In der folgenden Tabelle sind die verfügbaren nativen Decoder, der Klassenbezeichnername und die Unterstützung für globale Eigenschaften aufgeführt. Obwohl ein Feature eine Eigenschaft wie Miniaturansichten auf globaler Ebene möglicherweise nicht unterstützt, unterstützt das Bildformat diese Eigenschaften möglicherweise auf einzelner Frameebene.



| Bildformat | CLSID-Name            | Miniaturbilder | Vorschau | Farbkontexte | Metadaten |
|--------------|-----------------------|------------|----------|----------------|----------|
| BMP          | CLSID \_ WICBmpDecoder  | Nein         | Nein       | Nein             | Nein       |
| GIF          | CLSID \_ WICGifDecoder  | Nein         | Nein       | Nein             | Ja      |
| ICO          | CLSID \_ WICIcoDecoder  | Nein         | Nein       | Nein             | Nein       |
| JPEG         | CLSID \_ WICJpegDecoder | Nein         | Nein       | Nein             | Nein       |
| PNG          | CLSID \_ WICPngDecoder  | Nein         | Nein       | Nein             | Nein       |
| TIFF         | CLSID \_ WICTiffDecoder | Nein         | Nein       | Nein             | Nein       |
| HD-Foto     | CLSID \_ WICWmpDecoder  | Nein         | Ja      | Nein             | Nein       |



 

## <a name="creating-a-bitmap-decoder"></a>Erstellen eines Bitmap-Decoders

Um ein Bild mit WIC zu decodieren, müssen Sie zunächst eine Instanz von [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) für das Zielbildformat erstellen. Mit der Decoderinstanz können Sie auf die globalen Eigenschaften und Metadaten zugreifen, sofern unterstützt, sowie auf die Bildframes. Die WIC Imaging Factory, [**IWICImagingFactory,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)stellt mehrere Methoden zum Erstellen von Bitmapdecodern bereit. Die folgenden Factorymethoden werden zum Erstellen von Bitmapdecodern bereitgestellt.

-   [**CreateDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

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

Eines der Kernfeatures von WIC ist ein Erweiterbarkeitsframework, mit dem Codecentwickler ihre eigenen Bildcodecs entwickeln und die gleiche Plattformunterstützung wie die nativen Implementierungen von Bildcodecs erhalten können. Ein einzelner, konsistenter Satz von Schnittstellen wird unabhängig vom Bildformat für die gesamte Bildverarbeitung verwendet. Jede Anwendung, die WIC verwendet, erhält automatische Unterstützung für neue Bildformate, sobald der Codec installiert ist. Weitere Informationen zur Codecentwicklung finden Sie in den Themen unter [Komponentenentwicklung.](-wic-component-development.md) Weitere Informationen zur Decoderentwicklung finden Sie unter [Implementieren eines WIC-Enabled Decoders.](-wic-implementingwicdecoder.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über die Codierung](-wic-creating-encoder.md)
</dt> <dt>

[Komponentenentwicklung](-wic-component-development.md)
</dt> </dl>

 

 



