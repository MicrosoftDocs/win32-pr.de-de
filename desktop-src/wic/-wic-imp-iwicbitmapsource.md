---
description: Implementieren von IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: Implementieren von IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7ffd73271e8e159eea825ed40c24347ec2af98f0edbfa9ecc0d5ac584df23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965019"
---
# <a name="implementing-iwicbitmapsource"></a>Implementieren von IWICBitmapSource

## <a name="iwicbitmapsource"></a>Iwicbitmapsource

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) ist wichtig für die Arbeit mit Bildern aus Der Anwendungsperspektive. Sie stellt die Abstraktion auf der höchsten Ebene für eine Bildquelle dar, und alle Windows Imaging Component (WIC)-Schnittstellen, die ein Bild darstellen, einschließlich [**IWICBitmapFrameDecode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)und alle Transformationsschnittstellen ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)und [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) werden davon abgeleitet. Zu einem bestimmten Zeitpunkt kann ein **IWICBitmapSource-Objekt** durch eine tatsächliche Bitmap im Arbeitsspeicher gesichert werden. Dies ermöglicht eine sehr effiziente Verarbeitung durch eine Anwendung, da ein Bild als Abstraktion behandelt werden kann. Transformationsvorgänge können in einer Transformationspipeline verkettet werden, ohne Speicherressourcen zu verbrauchen, bis die Anwendung bereit ist, das Bild zu rendern oder zu drucken. Zu diesem Zeitpunkt ruft sie die [**CopyPixels-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) für die endgültige Transformation auf, um eine Bitmap im Speicher des Bilds mit den angewendeten ausgewählten Transformationen abzurufen.

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

Aus Codecperspektive werden die [**IWICBitmapSource-Methoden**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) für das Framedecoderobjekt implementiert. Diese Methoden werden unter Implementieren von IWICBitmapSource zusammen mit den anderen Methoden für [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)beschrieben, die von **IWICBitmapSource** abgeleitet sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Iwicbitmapdecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**Iwicbitmapsource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**Iwicbitmapframedecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Implementieren von IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Implementieren von IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



