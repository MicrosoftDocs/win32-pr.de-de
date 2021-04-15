---
description: In diesem Thema werden bitmapquellen, eine Windows Imaging Component-Kernkomponente (WIC) vorgestellt, die die Bitmap-Pixel eines Bilds darstellt.
ms.assetid: cff0c088-ca22-4d55-9cf0-9cbe9803923e
title: Übersicht über Bitmap-Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910bfc253798058639b98a1d1beaacec9bd4d1bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484779"
---
# <a name="bitmap-sources-overview"></a>Übersicht über Bitmap-Quellen

In diesem Thema werden bitmapquellen, eine Windows Imaging Component-Kernkomponente (WIC) vorgestellt, die die Bitmap-Pixel eines Bilds darstellt.

Dieses Thema enthält folgende Abschnitte:

-   [Bitmapquellen](#bitmap-sources-overview)
-   [Bitmapframes](#bitmap-frames)
-   [Bitmaps](#bitmap-sources-overview)
-   [Transformieren von bitmapquellen](#transform-bitmap-sources)
-   [Pixel Format-und Farb Kontext Konverter](#pixel-format-and-color-context-converters)
-   [Zeichnen von bitmapquellen](#drawing-bitmap-sources)
-   [Zugehörige Themen](#related-topics)

## <a name="bitmap-sources"></a>Bitmapquellen

Die [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Komponente ist der grundlegende Baustein von WIC und stellt einen einzelnen Satz von Pixeln dar. Bei einer Bitmap-Quelle kann es sich um einen einzelnen Frame eines Szene-Bilds handeln, oder es kann sich um das Ergebnis einer Transformation handeln, die für eine Bitmapquelle ausgeführt wird. Die **IWICBitmapSource** -Schnittstelle ist die Basis von vielen der primären WIC-Schnittstellen, wie z. b. dem Decoder-Frame [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) und Transformieren von bitmapquellen, z. b. [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).

In der folgenden Tabelle werden die verschiedenen Bitmap-Quell Komponenten beschrieben, die von WIC bereitgestellt werden.



| Bitmapquellen                                                    | BESCHREIBUNG                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) | Stellt einen decoderbildindex dar.                                    |
| [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                       | Stellt beschreiblichkeit und in-Memory-Darstellung für bitmapquellen bereit. |
| [**Iwicbitmapclipperdatei**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)         | Schneidet eine Bitmap-Quelle mit einem gewünschten Rechteck ab.                        |
| [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) | Flippt und/oder dreht eine Bitmap-Quelle in eine gewünschte Ausrichtung.       |
| [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)           | Skaliert eine Bitmapquelle auf die gewünschte Größe.                            |
| [**Iwiccolortransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)       | Transformiert den Farb Kontext einer Bitmap-Quelle.                     |
| [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)     | Konvertiert das Pixel Format einer Bitmap-Quelle.                        |



 

## <a name="bitmap-frames"></a>Bitmapframes

Die gängigste [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) ist [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode). Diese Schnittstelle wird verwendet, um auf die eigentlichen Bitmapdaten eines Bildformats zuzugreifen. Viele Bildformate unterstützen nur einen einzelnen BitmapFrame, während andere Formate, wie z. b. gif und TIFF, mehrere Frames pro Bild unterstützen.

Ein Beispiel zum Abrufen von bitmapframes aus einem Bild finden Sie im Thema [Abrufen der Frames eines Bilds](https://www.bing.com/search?q=How+to+Retrieve+the+Frames+of+an+Image) .

## <a name="bitmaps"></a>Bitmaps

Eine [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) fügt die Konzepte der beschreiblichkeit und des statischen Speicher internen Speichers zu bitmapquellen hinzu. Mit WIC-Bitmaps können Benutzer direkt auf die Pixel einer Bitmapquelle zugreifen. Dieser direkte Zugriff wird von der [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) -Methode bereitgestellt und unterstützt jede beliebige Kombination aus Lese-und/oder Schreibzugriff auf die bitmappixel. Die **Lock** -Methode sperrt das angegebene [**bitmaprechteck und stellt ein iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) -Objekt für den Zugriff auf die Pixel bereit.

Ein Beispiel für die Verwendung von [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) -und [**iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) -Objekten finden Sie im Thema Gewusst [wie: Ändern des Pixels einer Bitmap-Quelle](-wic-bitmapsources-howto-modifypixels.md) .

## <a name="transform-bitmap-sources"></a>Transformieren von bitmapquellen

WIC stellt mehrere [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Schnittstellen bereit, mit denen die Pixeldaten transformiert werden. WIC bietet speziell Bitmap-Quell Transformationen für das Skalieren, Clipping, drehen und Kippen von Pixeldaten. Diese Bitmap-Quell Transformationen sind [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)und [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator). Jede dieser bitmapquellen verfügt über eine-Methode, um eine neue transformierte Bitmapquelle zu initialisieren und zu erstellen. Beispielsweise enthält die **iwicbitmapclippermethode** die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) -Methode. Diese Methode initialisiert die Clipper Bitmap-Quelle mit den abgeschnittenen Pixeldaten der Eingabe Bitmap-Quelle bei der angegebenen [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect).

In den folgenden Vorgehensweisen wird veranschaulicht, wie die bitmapquellen der Transformation unterschiedlich verwendet werden.

-   [Skalieren einer Bitmap-Quelle](-wic-bitmapsources-howto-scale.md)
-   [Vorgehensweise beim Abschneiden einer Bitmap-Quelle](-wic-bitmapsources-howto-clip.md)
-   [Vorgehensweise beim Kippen und Drehen einer Bitmap-Quelle](-wic-bitmapsources-howto-flipandrotate.md)

## <a name="pixel-format-and-color-context-converters"></a>Pixel Format-und Farb Kontext Konverter

WIC stellt auch bitmapquellen zur Verfügung, die das Pixel Format und den Farb Kontext einer Bitmap-Quelle umrechnen. WIC stellt [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) und [**iwiccolortransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) für diese Vorgänge bereit.

[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) konvertiert eine angegebene Bitmapquelle von einem Pixel Format in ein anderes.

Ein Beispiel für die Verwendung von [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)finden Sie im Thema [How to draw a Bitmap Source using Direct2D](-wic-bitmapsources-howto-drawusingd2d.md) .

## <a name="drawing-bitmap-sources"></a>Zeichnen von bitmapquellen

WIC ist eine immer noch Abbild-Codec-Technologie und wird zum Verwalten von Bilddaten und Metadaten verwendet und stellt nicht grundsätzlich eine Möglichkeit zum Rendering von Bildern bereit. Bitmapquellen können jedoch mithilfe verschiedener Windows-Grafik Technologien wie Direct2D, Windows Graphics Device Interface (GDI) und Windows GDI+ gezeichnet werden. Jede dieser Technologien hat eine andere Ebene der Interoperabilität mit WIC. Direct2D ermöglicht die direkte Interoperabilität über die [ID2D1Bitmap](../direct2d/render-targets-overview.md) -Schnittstelle und die [ID2D1RenderTarget::](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) -Methode, während GDI und GDI+ erfordern, dass Benutzer die Bitmap-Quell Pixel in [Bitmaps](../gdi/bitmaps.md)kopieren müssen.

Im folgenden Beispiel wird veranschaulicht, wie bitmapquellen mithilfe von Direct2D gezeichnet werden.

-   [Zeichnen einer Bitmap-Quelle mithilfe von Direct2D](-wic-bitmapsources-howto-drawusingd2d.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über die Codierung](-wic-creating-encoder.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
