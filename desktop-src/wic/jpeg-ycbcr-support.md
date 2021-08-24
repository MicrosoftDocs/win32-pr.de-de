---
description: Ab Windows 8.1 unterstützt der JPEG-Codec Windows Imaging Component (WIC) das Lesen und Schreiben von Bilddaten in seiner nativen YCbCr-Form.
ms.assetid: 50B89A96-72E8-4771-9109-207F4CDD06CB
title: JPEG-YCbCr-Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f8548a458f70265d248e1d686ad3bc300d7cfee2bc1e0ab2262ee652f0d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086804"
---
# <a name="jpeg-ycbcr-support"></a>JPEG-YCbCr-Unterstützung

Ab Windows 8.1 unterstützt der [JPEG-Codec Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) das Lesen und Schreiben von Bilddaten in seiner nativen YC<sub>b</sub>C<sub>r-Form.</sub> WIC YC<sub>b</sub>C<sub>r-Unterstützung</sub> kann in Verbindung mit [Direct2D](../direct2d/direct2d-portal.md) verwendet werden, um YC<sub>b</sub>C<sub>r Pixeldaten</sub> mit einem Bildeffekt zu rendern. Darüber hinaus kann der WIC JPEG-Codec YC<sub>b</sub>C<sub>r Pixeldaten</sub> verarbeiten, die von bestimmten Kameratreibern über Media Foundation.

YC<sub>b</sub>C<sub>r Pixel-Daten</sub> verbrauchen deutlich weniger Arbeitsspeicher als BGRA-Standardpixelformate. Darüber hinaus können Sie durch den Zugriff auf YC<sub>b</sub>C<sub>r-Daten</sub> einige Phasen der JPEG-Decodierungs-/Codierungspipeline in Direct2D auslasten, das durch GPU beschleunigt wird. Mithilfe von YC<sub>b</sub>C<sub>r</sub>kann Ihre App den JPEG-Arbeitsspeicherverbrauch und die Ladezeiten für Bilder mit der gleichen Größe und Qualität reduzieren. Oder Ihre App kann mehr JPEG-Bilder mit höherer Auflösung verwenden, ohne dass die Leistung darunter zu beeinträchtigen ist.

In diesem Thema wird beschrieben, wie YC<sub>b</sub>C<sub>r-Daten</sub> funktionieren und wie sie in WIC und Direct2D verwendet werden.

-   [Informationen zu JPEG YC<sub>b</sub>C<sub>r</sub> Data](#about-jpeg-ycbcr-data)
    -   [YC<sub>b</sub>C<sub>r Farbmodell</sub>](#ycbcr-color-model)
    -   [Planar im Vergleich zu überlappten Speicherlayouts](#planar-versus-interleaved-memory-layouts)
    -   [Subsampling von Subsampling](#chroma-subsampling)
    -   [JPEG-Verwendung von YC<sub>b</sub>C<sub>r</sub>](#jpeg-usage-of-ycbcr)
-   [Verwenden von JPEG YC<sub>b</sub>C<sub>r</sub> Data](#using-jpeg-ycbcr-data)
    -   [Verwenden von YC<sub>b</sub>C<sub>r</sub> JPEG-Bildern](#using-ycbcr-jpeg-images)
    -   [Windows Imaging-Komponenten-APIs](#windows-imaging-component-apis)
    -   [Direct2D-APIs](#direct2d-apis)
    -   [Bestimmen, ob die YC<sub>b</sub>C<sub>r-Konfiguration</sub> unterstützt wird](#determining-if-the-ycbcr-configuration-is-supported)
    -   [Decodieren von YC<sub>b</sub>C<sub>r</sub> Pixel-Daten](#decoding-ycbcr-pixel-data)
    -   [Transformieren von YC<sub>b</sub>C<sub>r</sub> Pixel-Daten](#transforming-ycbcr-pixel-data)
    -   [Codieren von YC<sub>b</sub>C<sub>r</sub> Pixel-Daten](#encoding-ycbcr-pixel-data)
    -   [Decodieren von YC<sub>b</sub>C<sub>r Pixeldaten</sub> in Windows 10](#decoding-ycbcr-pixel-data-in-windows-10)
-   [Zugehörige Themen](#related-topics)

## <a name="about-jpeg-ycsubbsubcsubrsub-data"></a>Informationen zu JPEG YC<sub>b</sub>C<sub>r</sub> Data

In diesem Abschnitt werden einige wichtige Konzepte erläutert, die erforderlich sind, um zu verstehen, wie die Unterstützung von YC<sub>b</sub>C<sub>r</sub> in WIC funktioniert, und die wichtigsten Vorteile.

### <a name="ycsubbsubcsubrsub-color-model"></a>YC<sub>b</sub>C<sub>r Farbmodell</sub>

WIC in Windows 8 und früher unterstützt [](-wic-codec-native-pixel-formats.md)vier verschiedene Farbmodelle, von denen RGB/BGR am häufigsten verwendet wird. Dieses Farbmodell definiert Farbdaten mithilfe roter, grüner und blauer Komponenten. Eine vierte Alphakomponente kann ebenfalls verwendet werden.

Hier sehen Sie ein Bild, das in seine roten, grünen und blauen Komponenten zersetzt ist.

![ein Bild, das in seine roten, grünen und blauen Komponenten zersetzt ist.](graphics/ycbcr1.png)

YC<sub>b</sub>C<sub>r</sub> ist ein alternatives Farbmodell, das Farbdaten mithilfe einer Leuchtdichtekomponente (Y) und zwei Chrominancekomponenten (C<sub>b</sub> und C<sub>r) definiert.</sub> Sie wird häufig in Szenarien mit digitaler Bildverarbeitung und Video verwendet. Der Begriff YC<sub>b</sub>C<sub>r</sub> wird häufig synonym mit YUV verwendet, obwohl die beiden technisch eindeutig sind.

Es gibt mehrere Variationen von YC<sub>b</sub>C<sub>r,</sub> die sich im Farbraum und in dynamischen Bereichsdefinitionen unterscheiden– WIC unterstützt speziell JPEG JFIF YC<sub>b</sub>C<sub>r-Daten.</sub> Weitere Informationen finden Sie in der [JPEG ITU-T81-Spezifikation.](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)

Hier sehen Sie ein Image, das in seine Y-, C<sub>b-</sub>und C<sub>r-Komponenten zersetzt</sub> ist.

![ein Image, das in seine y-, cb- und cr-Komponenten zersetzt ist.](graphics/ycbcr2.png)

### <a name="planar-versus-interleaved-memory-layouts"></a>Planar im Vergleich zu überlappten Speicherlayouts

In diesem Abschnitt werden einige Unterschiede zwischen dem Zugreifen auf und Speichern von RGB-Pixeldaten im Arbeitsspeicher und YC<sub>b</sub>C<sub>r-Daten</sub> beschrieben.

RGB-Pixeldaten werden in der Regel mithilfe eines überlappten Speicherlayouts gespeichert. Dies bedeutet, dass Daten für eine einzelne Farbkomponente zwischen Pixeln übereinander liegen und jedes Pixel zusammenhängend im Arbeitsspeicher gespeichert wird.

Die folgende Abbildung zeigt RGBA-Pixeldaten, die in einem überlappten Speicherlayout gespeichert sind.

![Eine Abbildung, die rgba-Pixeldaten zeigt, die in einem überlappten Speicherlayout gespeichert sind.](graphics/ycbcr3.png)

YC<sub>b</sub>C<sub>r-Daten</sub> werden in der Regel mit einem planaren Speicherlayout gespeichert. Dies bedeutet, dass jede Farbkomponente separat in einer eigenen zusammenhängenden Ebene für insgesamt drei Ebenen gespeichert wird. In einer anderen allgemeinen Konfiguration werden die C<sub>b-</sub> und C<sub>r-Komponenten</sub> übereinander verwebt und gespeichert, während die Y-Komponente auf ihrer eigenen Ebene verbleibt, für insgesamt zwei Ebenen.

Die folgende Abbildung zeigt planare Y- und überlappte C<sub>b</sub>C<sub>r Pixel-Daten,</sub> ein gemeinsames YC<sub>b</sub>C<sub>r-Speicherlayout.</sub>

![Eine Abbildung, die planare y- und überlappte Cbcr-Pixeldaten zeigt, ein gemeinsames ycbcr-Speicherlayout.](graphics/ycbcr4.png)

Sowohl in WIC als auch in Direct2D wird jede Farbebene als eigenes eindeutiges Objekt [(entweder EINE IWICBitmapSource](-wic-imp-iwicbitmapsource.md) oder [**ID2D1Bitmap)**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)behandelt, und zusammen bilden diese Ebenen die Hintergrunddaten für ein YC <sub>b</sub>C <sub>r-Bild.</sub>

WIC unterstützt den Zugriff auf YC<sub>b</sub>C<sub>r-Daten</sub> sowohl in den Konfigurationen der 2- als auch der 3-Ebene, Direct2D unterstützt jedoch nur den ersten (Y und C<sub>b</sub>C<sub>r</sub>). Wenn Sie WIC und Direct2D zusammen verwenden, sollten Sie daher immer die 2-Ebenen-YC<sub>b</sub>C<sub>r-Konfiguration</sub> verwenden.

### <a name="chroma-subsampling"></a>Subsampling von Subsampling

Das YC<sub>b</sub>C<sub>r-Farbmodell</sub> eignet sich gut für Szenarien mit digitaler Bildverarbeitung, da es bestimmte Aspekte des menschlichen visuellen Systems nutzen kann. Insbesondere menschen sind anfälliger für Änderungen der Leuchtdichte (Helligkeit) eines Bilds und weniger empfindlich gegenüber Chrominance (Farbe). Indem die Farbdaten in separate Leuchtdichte- und Chrominancekomponenten aufgeteilt werden, können wir selektiv nur die Chrominancekomponenten komprimieren, um Platzeinsparungen mit minimalem Qualitätsverlust zu erzielen.

Eine Technik dafür wird als "untergeordnetes Subsampling" bezeichnet. Die Ebenen C<sub>b</sub> und C<sub>r</sub> werden in einer oder beiden horizontalen und vertikalen Dimensionen subsampelt (herunterskaliert). Aus historischen Gründen wird auf jeden Untergeordneten Subsamplingmodus mit einem Dreiteil-J:a:b-Verhältnis verwiesen.



| Subsamplingmodus | Horizontales Herunterskalieren | Vertikales Herunterskalieren | Bits pro Pixel\* |
|------------------|----------------------|--------------------|------------------|
| 4:4:4            | 1x                   | 1x                 | 24               |
| 4:2:2            | 2x                   | 1x                 | 16               |
| 4:4:0            | 1x                   | 2x                 | 16               |
| 4:2:0            | 2x                   | 2x                 | 12               |



 

\* Schließt Y-Daten ein.

Wenn Sie in der obigen Tabelle YC<sub>b</sub>C<sub>r</sub> verwenden, um unkomprimierte Bilddaten zu speichern, können Sie eine Speichereinsparung von 25 % bis 62,5 % im Vergleich zu RGBA-Daten mit 32 Bit pro Pixel erzielen, je nachdem, welcher Subsamplingmodus verwendet wird.

### <a name="jpeg-usage-of-ycsubbsubcsubrsub"></a>JPEG-Verwendung von YC<sub>b</sub>C<sub>r</sub>

Auf hoher Ebene besteht die JPEG-Dekomprimierungspipeline aus den folgenden Phasen:

1.  Durchführen der Entropiedekomprimierung (z. B. Huffman)
2.  Durchführen der Dequantisierung
3.  Durchführen einer inversen diskreten Kosinustransformation
4.  Durchführen eines upsampling-Upsamplings für C<sub>b</sub>C<sub>r-Daten</sub>
5.  Konvertieren von YC<sub>b</sub>C<sub>r-Daten</sub> in RGBA (falls erforderlich)

Wenn der JPEG-Codec YC<sub>b</sub>C<sub>r-Daten</sub> erzeugt, können wir die letzten beiden Schritte des Decodierungsprozesses vermeiden oder sie auf die GPU zurückstufen. Zusätzlich zu den im vorherigen Abschnitt aufgeführten Speichereinsparungen reduziert dies die Gesamtzeit, die zum Decodieren des Bilds benötigt wird, erheblich. Beim Codieren von YC<sub>b</sub>C r-Daten gelten die<sub>gleichen Einsparungen.</sub>

## <a name="using-jpeg-ycsubbsubcsubrsub-data"></a>Verwenden von JPEG YC<sub>b</sub>C<sub>r</sub> Data

In diesem Abschnitt wird erläutert, wie WIC und Direct2D zum Verarbeiten von YC<sub>b</sub>C<sub>r-Daten verwendet</sub> werden.

Die Anleitungen aus diesem Dokument, die in der Praxis verwendet werden, finden Sie im [Beispiel JPEG YCbCr optimizations in Direct2D and WIC (JPEG-YCbCr-Optimierungen in Direct2D und WIC),](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample) das alle Schritte veranschaulicht, die zum Decodieren und Rendern von YC<sub>b</sub>C<sub>r-Inhalten</sub> in einer Direct2D-App erforderlich sind.

### <a name="using-ycsubbsubcsubrsub-jpeg-images"></a>Verwenden von YC<sub>b</sub>C<sub>r</sub> JPEG-Bildern

Die überwiegende Mehrheit der JPEG-Bilder wird als YC<sub>b</sub>C<sub>r gespeichert.</sub> Einige JPEGs enthalten C JPEG- oder Graustufendaten und verwenden YC<sub>b</sub>C<sub>r nicht.</sub> Dies bedeutet, dass Sie in der Regel, aber nicht immer, bereits vorhandene JPEG-Inhalte ohne Änderungen direkt verwenden können.

WIC und Direct2D unterstützen nicht jede mögliche YC<sub>b</sub>C<sub>r-Konfiguration,</sub> und die Unterstützung von YC<sub>b</sub>C<sub>r</sub> in Direct2D ist von der zugrunde liegenden Grafikhardware und dem Treiber abhängig. Aus diesem Grund muss eine allgemeine Bildverarbeitungspipeline stabil für Bilder sein, die YC<sub>b</sub>C<sub>r</sub> nicht verwenden (einschließlich anderer gängiger Bildformate wie PNG oder BMP) oder für Fälle, in denen YC<sub>b</sub>C<sub>r</sub> nicht unterstützt wird. Es wird empfohlen, ihre vorhandene BGRA-basierte Bildverarbeitungspipeline beizubehalten und YC<sub>b</sub>C<sub>r</sub> als Leistungsoptimierung zu aktivieren, sofern verfügbar.

### <a name="windows-imaging-component-apis"></a>Windows APIs für Bildverarbeitungskomponenten

WIC in Windows 8.1 fügt drei neue Schnittstellen hinzu, um Zugriff auf JPEG YC<sub>b</sub>C<sub>r-Daten</sub> zu ermöglichen.

### <a name="iwicplanarbitmapsourcetransform"></a>IWICPlanarBitmapSourceTransform

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) ist analog zu [**IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)mit der Ausnahme, dass pixel in einer planaren Konfiguration erzeugt wird, einschließlich YC <sub>b</sub>C <sub>r-Daten.</sub> Sie können diese Schnittstelle abrufen, indem Sie QueryInterface für eine Implementierung von [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) aufrufen, die planaren Zugriff unterstützt. Dies schließt die Implementierung des JPEG-Codecs [**von IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) sowie [**IWICBitmapScaler,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)und [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)ein.

### <a name="iwicplanarbitmapframeencode"></a>IWICPlanarBitmapFrameEncode

[**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) bietet die Möglichkeit, planare Pixeldaten zu codieren, einschließlich YC <sub>b</sub>C <sub>r-Daten.</sub> Sie können diese Schnittstelle abrufen, indem Sie QueryInterface für die Implementierung des JPEG-Codecs von [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)aufrufen.

### <a name="iwicplanarformatconverter"></a>IWICPlanarFormatConverter

[**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) ermöglicht [**IWICFormatConverter,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) planare Pixeldaten zu nutzen, einschließlich YC <sub>b</sub>C <sub>r</sub>, und konvertiert sie in ein verschachteltes Pixelformat. Es bietet keine Möglichkeit, überlappende Pixeldaten in ein planares Format zu konvertieren. Sie können diese Schnittstelle abrufen, indem Sie QueryInterface für die Windows bereitgestellte Implementierung von **IWICFormatConverter** aufrufen.

### <a name="direct2d-apis"></a>Direct2D-APIs

Direct2D in Windows 8.1 unterstützt YC<sub>b</sub>C<sub>r</sub> planare Pixeldaten mit dem neuen Bildeffekt YC<sub>b</sub>C<sub>r.</sub> Dieser Effekt bietet die Möglichkeit, YC<sub>b</sub>C r-Daten zu<sub>rendern.</sub> Der Effekt nimmt als Eingabe zwei [**ID2D1Bitmap-Schnittstellen**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) an: eine mit planaren Y-Daten im \_ DXGI FORMAT \_ R8 \_ UNORM-Format und eine mit verschachtelten CbCr-Daten im DXGI \_ FORMAT \_ R8G8 \_ UNORM-Format. In der Regel verwenden Sie diesen Effekt anstelle der **ID2D1Bitmap,** die BGRA-Pixeldaten enthalten hätte.

Der Imageeffekt YC<sub>b</sub><sub>C r</sub> ist für die Verwendung in Verbindung mit den WIC YC<sub>b</sub>C<sub>r-APIs</sub> vorgesehen, die die YC<sub>b</sub>C<sub>r-Daten</sub> bereitstellen. Dadurch wird effektiv ein Teil der Decodierungsarbeit von der CPU auf die GPU ausgelagert, wo sie viel schneller und parallel verarbeitet werden kann.

### <a name="determining-if-the-ycsubbsubcsubrsub-configuration-is-supported"></a>Bestimmen, ob die YC<sub>b</sub>C<sub>r-Konfiguration</sub> unterstützt wird

Wie bereits erwähnt, sollte Ihre App in Fällen robust sein, in denen die Unterstützung von YC<sub>b</sub>C<sub>r</sub> nicht verfügbar ist. In diesem Abschnitt werden die Bedingungen erläutert, die Ihre App überprüfen sollte. Wenn eine der folgenden Überprüfungen fehlschlägt, sollte Ihre App auf eine BGRA-basierte Standardpipeline zurückgreifen.

### <a name="does-the-wic-component-support-ycsubbsubcsubrsub-data-access"></a>Unterstützt die WIC-Komponente den Datenzugriff auf YC<sub>b</sub><sub>C r?</sub>

Nur die Windows JPEG-Codec und bestimmte WIC-Transformationen unterstützen den YC<sub>b</sub>C r-Datenzugriff.<sub></sub> Eine vollständige Liste finden Sie im Abschnitt [Windows Imaging Component-APIs.](#windows-imaging-component-apis)

Um eine der planaren YC<sub>b</sub>C<sub>r-Schnittstellen</sub> abzurufen, rufen Sie QueryInterface für die ursprüngliche Schnittstelle auf. Dies schlägt fehl, wenn die Komponente keinen YC<sub>b</sub>C<sub>r-Datenzugriff</sub> unterstützt.

### <a name="is-the-requested-wic-transform-supported-for-ycsubbsubcsubrsub"></a>Wird die angeforderte WIC-Transformation für YC<sub>b</sub>C<sub>r</sub>unterstützt?

Nachdem Sie eine [**IWICPlanarBitmapSourceTransform-Datei**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)erhalten haben, sollten Sie zuerst [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform)aufrufen. Diese Methode verwendet als Eingabeparameter den vollständigen Satz von Transformationen, die Sie auf die planaren YC<sub>b</sub>C<sub>r-Daten</sub> anwenden möchten, und gibt einen booleschen Wert zurück, der die Unterstützung angibt, sowie die dimensionen, die der angeforderten Größe am nächsten sind, die zurückgegeben werden kann. Überprüfen Sie alle drei Werte, bevor Sie mit [**IWICPlanarBitmapSourceTransform::CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels)auf die Pixeldaten zugreifen.

Dieses Muster ähnelt der Verwendung von [**IWICBitmapSourceTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)

### <a name="does-the-graphics-driver-support-the-features-necessary-to-use-ycsubbsubcsubrsub-with-direct2d"></a>Unterstützt der Grafiktreiber die Features, die für die Verwendung von YC<sub>b</sub>C<sub>r</sub> mit Direct2D erforderlich sind?

Diese Überprüfung ist nur erforderlich, wenn Sie den Direct2D YC<sub>b</sub>C<sub>r-Effekt</sub> verwenden, um YC<sub>b</sub>C r-Inhalt zu<sub>rendern.</sub> Direct2D speichert YC<sub>b</sub>C<sub>r-Daten</sub> mithilfe der \_ UNORM-Formate DXGI FORMAT \_ R8 und \_ DXGI FORMAT \_ \_ R8G8 \_ UNORM, die nicht von allen Grafiktreibern verfügbar sind.

Bevor Sie den Imageeffekt YC <sub>b</sub>C <sub>r</sub> verwenden, sollten Sie [**ID2D1DeviceContext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) aufrufen, um sicherzustellen, dass beide Formate vom Treiber unterstützt werden.

### <a name="sample-code"></a>Beispielcode

Im Folgenden finden Sie ein Codebeispiel, in dem die empfohlenen Überprüfungen veranschaulicht werden. Dieses Beispiel stammt aus den [JPEG-YCbCr-Optimierungen im Direct2D- und WIC-Beispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


```C++
bool DirectXSampleRenderer::DoesWicSupportRequestedYCbCr()
{
    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    HRESULT hr = m_wicScaler.As(&wicPlanarSource);
    if (SUCCEEDED(hr))
    {
        BOOL isTransformSupported;
        uint32 supportedWidth = m_cachedBitmapPixelWidth;
        uint32 supportedHeight = m_cachedBitmapPixelHeight;
        DX::ThrowIfFailed(
            wicPlanarSource->DoesSupportTransform(
                &supportedWidth,
                &supportedHeight,
                WICBitmapTransformRotate0,
                WICPlanarOptionsDefault,
                SampleConstants::WicYCbCrFormats,
                m_planeDescriptions,
                SampleConstants::NumPlanes,
                &isTransformSupported
                )
            );

        // The returned width and height may be larger if IWICPlanarBitmapSourceTransform does not
        // exactly support what is requested.
        if ((isTransformSupported == TRUE) &&
            (supportedWidth == m_cachedBitmapPixelWidth) &&
            (supportedHeight == m_cachedBitmapPixelHeight))
        {
            return true;
        }
    }

    return false;
}

bool DirectXSampleRenderer::DoesDriverSupportYCbCr()
{
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    return (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8_UNORM)) &&
        (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8G8_UNORM));
}
```



### <a name="decoding-ycsubbsubcsubrsub-pixel-data"></a>Decodieren von YC<sub>b</sub><sub>C r</sub> Pixel-Daten

Wenn Sie YC <sub>b</sub>C <sub>r</sub> Pixeldaten abrufen möchten, sollten Sie [**IWICPlanarBitmapSourceTransform::CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels)aufrufen. Diese Methode kopiert Pixeldaten in ein Array ausgefüllter [**WICBitmapPlane-Strukturen,**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) eine für jede gewünschte Datenebene (z. B. Y und C <sub>b</sub>C <sub>r).</sub> Ein **WICBitmapPlane** enthält Informationen zu den Pixeldaten und zeigt auf den Speicherpuffer, der die Daten empfängt.

Wenn Sie die YC <sub>b</sub>C <sub>r-Pixeldaten</sub> mit anderen WIC-APIs verwenden möchten, sollten Sie eine entsprechend konfigurierte [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)erstellen, [**lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) aufrufen, um den zugrunde liegenden Speicherpuffer abzurufen, und den Puffer dem [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) zuordnen, der zum Empfangen der YC <sub>b</sub>C <sub>r-Pixeldaten</sub> verwendet wird. Anschließend können Sie [IWICBitmap](-wic-imp-iwicbitmapdecoder.md) normal verwenden.

Wenn Sie schließlich die YC <sub>b</sub>C <sub>r-Daten</sub> in Direct2D rendern möchten, sollten Sie eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) aus jeder [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) erstellen und diese als Quelle für den YC <sub>b</sub>C <sub>r-Imageeffekt</sub> verwenden. Mit WIC können Sie mehrere planare Konfigurationen anfordern. Bei der Zusammenarbeit mit Direct2D sollten Sie zwei Ebenen anfordern: eine mit guid \_ WICPixelFormat8bppY und die andere mit guid \_ WICPixelFormat16bppCbCr, da dies die von Direct2D erwartete Konfiguration ist.

### <a name="code-sample"></a>Codebeispiel

Im Folgenden finden Sie ein Codebeispiel, das die Schritte zum Decodieren und Rendern von YC<sub>b</sub>C<sub>r-Daten</sub> in Direct2D veranschaulicht. Dieses Beispiel stammt aus den [JPEG-YCbCr-Optimierungen im Direct2D- und WIC-Beispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


```C++
void DirectXSampleRenderer::CreateYCbCrDeviceResources()
{
    auto wicFactory = m_deviceResources->GetWicImagingFactory();
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    DX::ThrowIfFailed(
        m_wicScaler.As(&wicPlanarSource)
        );

    ComPtr<IWICBitmap> bitmaps[SampleConstants::NumPlanes];
    ComPtr<IWICBitmapLock> locks[SampleConstants::NumPlanes];
    WICBitmapPlane planes[SampleConstants::NumPlanes];

    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        DX::ThrowIfFailed(
            wicFactory->CreateBitmap(
                m_planeDescriptions[i].Width,
                m_planeDescriptions[i].Height,
                m_planeDescriptions[i].Format,
                WICBitmapCacheOnLoad,
                &bitmaps[i]
                )
            );

        LockBitmap(bitmaps[i].Get(), WICBitmapLockWrite, nullptr, &locks[i], &planes[i]);
    }

    DX::ThrowIfFailed(
        wicPlanarSource->CopyPixels(
            nullptr, // Copy the entire source region.
            m_cachedBitmapPixelWidth,
            m_cachedBitmapPixelHeight,
            WICBitmapTransformRotate0,
            WICPlanarOptionsDefault,
            planes,
            SampleConstants::NumPlanes
            )
        );

    DX::ThrowIfFailed(d2dContext->CreateEffect(CLSID_D2D1YCbCr, &m_d2dYCbCrEffect));

    ComPtr<ID2D1Bitmap1> d2dBitmaps[SampleConstants::NumPlanes];
    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        // IWICBitmapLock must be released before using the IWICBitmap.
        locks[i] = nullptr;

        // First ID2D1Bitmap1 is DXGI_FORMAT_R8 (Y), second is DXGI_FORMAT_R8G8 (CbCr).
        DX::ThrowIfFailed(d2dContext->CreateBitmapFromWicBitmap(bitmaps[i].Get(), &d2dBitmaps[i]));
        m_d2dYCbCrEffect->SetInput(i, d2dBitmaps[i].Get());
    }
}

void DirectXSampleRenderer::LockBitmap(
    _In_ IWICBitmap *pBitmap,
    DWORD bitmapLockFlags,
    _In_opt_ const WICRect *prcSource,
    _Outptr_ IWICBitmapLock **ppBitmapLock,
    _Out_ WICBitmapPlane *pPlane
    )
{
    // ComPtr guarantees the IWICBitmapLock is released if an exception is thrown.
    ComPtr<IWICBitmapLock> lock;
    DX::ThrowIfFailed(pBitmap->Lock(prcSource, bitmapLockFlags, &lock));
    DX::ThrowIfFailed(lock->GetStride(&pPlane->cbStride));
    DX::ThrowIfFailed(lock->GetDataPointer(&pPlane->cbBufferSize, &pPlane->pbBuffer));
    DX::ThrowIfFailed(lock->GetPixelFormat(&pPlane->Format));
    *ppBitmapLock = lock.Detach();
}
```



### <a name="transforming-ycsubbsubcsubrsub-pixel-data"></a>Transformieren von YC<sub>b</sub>C<sub>r</sub> Pixel-Daten

Das Transformieren von YC <sub>b</sub>C <sub>r-Daten</sub> ist nahezu identisch mit der Decodierung, da beide [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)beinhalten. Der einzige Unterschied besteht darin, von welchem WIC-Objekt Sie die Schnittstelle erhalten haben. Die Windows bereitgestellten Scaler, Flip-Rotator und Farbtransformation unterstützen alle YC<sub>b</sub>C<sub>r-Zugriff.</sub>

### <a name="chaining-transforms-together"></a>Verketten von Transformationen

WIC unterstützt das Konzept der Verkettung mehrerer Transformationen. Beispielsweise können Sie die folgende WIC-Pipeline erstellen:

![Ein Diagramm einer wic-Pipeline, die mit einem JPEG-Decoder beginnt.](graphics/ycbcr5.png)

Anschließend können Sie QueryInterface für [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) aufrufen, um [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)abzurufen. Die Farbtransformation kann mit den vorherigen Transformationen kommunizieren und die Aggregatfunktionen jeder Phase in der Pipeline verfügbar machen. WIC stellt sicher, dass die YC<sub>b</sub>C<sub>r-Daten</sub> während des gesamten Prozesses beibehalten werden. Diese Verkettung funktioniert nur, wenn Komponenten verwendet werden, die YC<sub>b</sub>C<sub>r-Zugriff</sub> unterstützen.

### <a name="jpeg-codec-optimizations"></a>JPEG-Codecoptimierungen

Ähnlich wie bei der Implementierung der JPEG-Framedecodierung von [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)unterstützt die JPEG-Framedecodierungsimplementierung von [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) die native Skalierung und Drehung von JPEG-DCT-Domänen. Sie können eine Leistung von zwei Herunterskalierungs- oder Drehungen direkt vom JPEG-Decoder anfordern. Dies führt in der Regel zu einer höheren Qualität und Leistung als bei der Verwendung der diskreten Transformationen.

Wenn Sie eine oder mehrere WIC-Transformationen nach dem JPEG-Decoder verketten, kann außerdem die native JPEG-Skalierung und -Drehung genutzt werden, um den angeforderten Aggregatvorgang zu erfüllen.

### <a name="format-conversions"></a>Formatkonvertierungen

Verwenden Sie [**IWICPlanarFormatConverter,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) um planare YC <sub>b</sub>C <sub>r-Pixeldaten</sub> in ein verschachteltes Pixelformat wie GUID \_ WICPixelFormat32bppPBGRA zu konvertieren. WIC in Windows 8.1 bietet nicht die Möglichkeit, in ein planares YC<sub>b</sub>C<sub>r-Pixelformat</sub> zu konvertieren.

### <a name="encoding-ycsubbsubcsubrsub-pixel-data"></a>Codierung von YC<sub>b</sub>C<sub>r</sub> Pixeldaten

Verwenden Sie [**IWICPlanarBitmapFrameEncode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) um YC <sub>b</sub>C <sub>r</sub> Pixeldaten im JPEG-Encoder zu codieren. Encoding YC <sub>b</sub>C <sub>r</sub> data **IWICPlanarBitmapFrameEncode** is similar but not identical to encoding interleaved data using [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). Die planare Schnittstelle bietet nur die Möglichkeit, planare Framebilddaten zu schreiben, und Sie sollten weiterhin die Framecodierungsschnittstelle verwenden, um Metadaten oder eine Miniaturansicht festzulegen und am Ende des Vorgangs einen Commit zu committen.

Für den typischen Fall sollten Sie die folgenden Schritte ausführen:

1.  Rufen Sie [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) wie gewohnt ab. Wenn Sie die Subsamplingoption [**"JpegYCrCbSubsampling"**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) konfigurieren möchten, legen Sie beim Erstellen des Frames die Option JpegYCrCbSubsampling fest.
2.  Wenn Sie Metadaten oder eine Miniaturansicht festlegen müssen, verwenden Sie [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) wie gewohnt.
3.  QueryInterface für [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode).
4.  Legen Sie die YC <sub>b</sub>C <sub>r-Pixeldaten</sub> mithilfe von [**IWICPlanarBitmapFrameEncode::WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writesource) oder [**IWICPlanarBitmapFrameEncode::WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writepixels)fest. Im Gegensatz zu ihren [**IWICBitmapFrameEncode-Entsprechungen**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) stellen Sie diese Methoden mit einem Array von [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) oder [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) bereit, das die YC <sub>b</sub>C r-Pixelebenen enthält.<sub></sub>
5.  Wenn Sie fertig sind, rufen Sie [**IWICBitmapFrameEncode::Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit)auf.

### <a name="decoding-ycsubbsubcsubrsub-pixel-data-in-windows-10"></a>Decodieren von YC<sub>b</sub>C<sub>r-Pixeldaten</sub> in Windows 10

Ab Windows 10 Build 1507 bietet Direct2D [**ID2D1ImageSourceFromWic,**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)eine einfachere Möglichkeit, JPEGs in Direct2D zu decodieren, während YC <sub>b</sub>C <sub>r-Optimierungen</sub> genutzt werden. **ID2D1ImageSourceFromWic** führt automatisch alle erforderlichen YC <sub>b</sub>C r-Funktionsüberprüfungen für Sie aus.<sub></sub> er verwendet nach Möglichkeit den optimierten Codepfad und andernfalls einen Fallback. Außerdem werden neue Optimierungen ermöglicht, z. B. das Zwischenspeichern von Teilregionen des Images, die gleichzeitig benötigt werden.

Weitere Informationen zur Verwendung von [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)finden Sie im Direct2D Photo Adjustment [SDK-Beispiel.](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)

## <a name="related-topics"></a>Zugehörige Themen

* [JPEG-YCbCr-Optimierungen in Direct2D- und WIC-Beispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)
