---
description: Implementieren von IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: Implementieren von IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88e2f7dfd073405f9de8c82b2ce6d9592b241a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758299"
---
# <a name="implementing-iwicbitmapsource"></a>Implementieren von IWICBitmapSource

## <a name="iwicbitmapsource"></a>IWICBitmapSource

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) ist wichtig für das Arbeiten mit Bildern aus Anwendungs Sicht. Es stellt die Abstraktion der höchsten Ebene für eine Bildquelle dar. alle Windows Imaging Component-Schnittstellen (WIC), die ein Bild darstellen, einschließlich [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)und alle Transformations Schnittstellen ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)und [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)), werden davon abgeleitet. Ein **IWICBitmapSource** -Objekt kann zu einem bestimmten Zeitpunkt von einer tatsächlichen Bitmap im Arbeitsspeicher unterstützt werden. Dies ermöglicht eine sehr effiziente Verarbeitung durch eine Anwendung, da ein Bild als Abstraktion behandelt werden kann. Transformations Vorgänge können in einer Transformations Pipeline verkettet werden, ohne Arbeitsspeicher Ressourcen zu beanspruchen, bis die Anwendung zum Renderingvorgang oder Drucken des Bilds bereit ist. zu diesem Zeitpunkt wird die [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) -Methode für die endgültige Transformation aufgerufen, um mit den ausgewählten Transformationen eine Bitmap im Speicher des Bilds zu erhalten.

``` syntax
interface IWICBitmapSource : IUnknown
{
   // Required methods
   HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
   HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
   HRESULT GetResolution ( double *pDpiX, double *pDpiY );
   HRESULT CopyPixels ( const WICRect *prc,
      UINT cbStride,
      UINT cbBufferSize, 
      BYTE *pbBuffer );
   // Optional method
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

Aus Codec-Sicht werden die [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Methoden auf dem Frame-Decoderobjekt implementiert. Diese Methoden werden unter Implementieren von IWICBitmapSource und den anderen Methoden in [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)beschrieben, die von **IWICBitmapSource** abgeleitet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Licher**
</dt> <dt>

[Implementieren von IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Implementieren von IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



