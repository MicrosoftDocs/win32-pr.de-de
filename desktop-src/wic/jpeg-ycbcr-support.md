---
description: Ab Windows 8.1 unterstützt der JPEG-Codec der Windows Imaging Component (WIC) das Lesen und Schreiben von Bilddaten in der nativen YCbCr-Form.
ms.assetid: 50B89A96-72E8-4771-9109-207F4CDD06CB
title: JPEG YCbCr-Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a8f05fe55e724a12513f24fc7401d277ebf097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959816"
---
# <a name="jpeg-ycbcr-support"></a>JPEG YCbCr-Unterstützung

Ab Windows 8.1 unterstützt der JPEG-Codec der [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) das Lesen und Schreiben von Bilddaten in der nativen Yc<sub>b</sub>c<sub>r</sub> -Form. WIC Yc<sub>b</sub>c<sub>r</sub> -Unterstützung kann zusammen mit [Direct2D](../direct2d/direct2d-portal.md) verwendet werden, um Yc<sub>b</sub>c<sub>r</sub> -Pixeldaten mit einem Bildeffekt zu rendern. Außerdem kann der WIC-JPEG-Codec Yc<sub>b</sub>C<sub>r</sub> Pixel-Daten verarbeiten, die von bestimmten Kamera Treibern über Media Foundation erzeugt werden.

Yc<sub>b</sub>C-Pixeldaten verbrauchen erheblich weniger Arbeitsspeicher als die standardmäßigen BGRA<sub>-Pixel Formate</sub> . Außerdem ermöglicht der Zugriff auf Yc<sub>b</sub>C<sub>r</sub> -Daten das Auslagern einiger Phasen der JPEG-Decodierung/-Codierungs Pipeline in Direct2D. Dies ist eine GPU-Beschleunigung. Wenn Sie Yc<sub>b</sub>C<sub>r</sub>verwenden, kann Ihre APP die JPEG-Speichernutzung und Ladezeiten für dieselben Größen-und Qualitäts Images reduzieren. Oder Ihre APP kann mehr Auflösung von JPEG-Images mit höherer Auflösung verwenden, ohne dass dies zu Leistungseinbußen führen kann.

In diesem Thema wird beschrieben, wie Yc<sub>b</sub>C<sub>r</sub> -Daten funktioniert und wie Sie in WIC und Direct2D verwendet werden.

-   [Informationen zu JPEG Yc<sub>b</sub>C<sub>r</sub> -Daten](#about-jpeg-ycbcr-data)
    -   [Yc<sub>b</sub>C<sub>r</sub> -Farbmodell](#ycbcr-color-model)
    -   [Planar im Vergleich zu verschachtelten Speicher Layouts](#planar-versus-interleaved-memory-layouts)
    -   [Chroma-Unterstichprobe](#chroma-subsampling)
    -   [JPEG-Verwendung von Yc<sub>b</sub>C<sub>r</sub>](#jpeg-usage-of-ycbcr)
-   [Verwenden von JPEG Yc<sub>b</sub>c<sub>r</sub> -Daten](#using-jpeg-ycbcr-data)
    -   [Verwenden von Yc<sub>b</sub>C<sub>r</sub> JPEG-Images](#using-ycbcr-jpeg-images)
    -   [Windows Imaging-Komponenten-APIs](#windows-imaging-component-apis)
    -   [Direct2D-APIs](#direct2d-apis)
    -   [Ermitteln, ob die JC<sub>b</sub><sub>-C-</sub> Konfiguration unterstützt wird](#determining-if-the-ycbcr-configuration-is-supported)
    -   [Decodieren von Yc<sub>b</sub>C<sub>r</sub> -Pixel Daten](#decoding-ycbcr-pixel-data)
    -   [Transformieren von Yc<sub>b</sub>C<sub>r</sub> -Pixel Daten](#transforming-ycbcr-pixel-data)
    -   [Codieren von Yc<sub>b</sub>C<sub>r</sub> -Pixel Daten](#encoding-ycbcr-pixel-data)
    -   [Decodieren von Yc<sub>b</sub>C<sub>r</sub> Pixel-Daten in Windows 10](#decoding-ycbcr-pixel-data-in-windows-10)
-   [Zugehörige Themen](#related-topics)

## <a name="about-jpeg-ycsubbsubcsubrsub-data"></a>Informationen zu JPEG Yc<sub>b</sub>C<sub>r</sub> -Daten

In diesem Abschnitt werden einige wichtige Konzepte erläutert, die erforderlich sind, um zu verstehen, wie Yc<sub>b</sub>C<sub>r</sub> -Unterstützung in WIC funktioniert und welche Hauptvorteile

### <a name="ycsubbsubcsubrsub-color-model"></a>Yc<sub>b</sub>C<sub>r</sub> -Farbmodell

WIC in Windows 8 und früheren Versionen unterstützt vier verschiedene [Farbmodelle](-wic-codec-native-pixel-formats.md), bei denen es sich am häufigsten um RGB/BGR handelt. Mit diesem Farbmodell werden Farbdaten mithilfe von roten, grünen und blauen Komponenten definiert. Es kann auch eine vierte Alpha Komponente verwendet werden.

Hier ist ein Bild, das in seine roten, grünen und blauen Komponenten zerlegt wird.

![ein Bild, das in seine roten, grünen und blauen Komponenten zerlegt wird.](graphics/ycbcr1.png)

Yc<sub>b</sub>C<sub>r</sub> ist ein alternatives Farbmodell, das Farbdaten mit einer Leuchtkraft Komponente (Y) und zwei Chrominanz-Komponenten (c<sub>b</sub> und c<sub>r</sub>) definiert. Sie wird häufig in digitalen Abbild-und Video Szenarios verwendet. Der Begriff Yc<sub>b</sub>C<sub>r</sub> wird häufig austauschbar mit YUV verwendet, obwohl beide technisch unterschiedlich sind.

Es gibt mehrere Variationen von Yc<sub>b</sub>c<sub>r</sub> , die sich in Farbraum und dynamischen Bereichs Definitionen unterscheiden – WIC unterstützt speziell JPEG JFI-Yc<sub>b</sub>c<sub>r</sub> -Daten. Weitere Informationen finden Sie in der [JPEG-Spezifikation "ITU-T81](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)".

Hier ist ein Bild, das in seine Y-, C<sub>b</sub>-und c<sub>r</sub> -Komponenten zerlegt wird.

![ein Bild, das in seine y-, CB-und CR-Komponenten zerlegt wird.](graphics/ycbcr2.png)

### <a name="planar-versus-interleaved-memory-layouts"></a>Planar im Vergleich zu verschachtelten Speicher Layouts

In diesem Abschnitt werden einige Unterschiede zwischen dem Zugriff auf und dem Speichern von RGB-Pixeldaten im Arbeitsspeicher im Vergleich zu Yc<sub>b</sub>C<sub>r</sub>

RGB-Pixeldaten werden in der Regel mit einem verschachtelten Speicher Layout gespeichert. Dies bedeutet, dass sich die Daten für eine einzelne Farbkomponente zwischen Pixeln überlappen und jedes Pixel im Arbeitsspeicher zusammenhängend gespeichert wird.

Es folgt eine Abbildung, in der die in einem verschachtelten Speicher Layout gespeicherten RGBA-Pixeldaten angezeigt werden.

![eine Abbildung, die RGBA-Pixeldaten anzeigt, die in einem verschachtelten Speicher Layout gespeichert sind.](graphics/ycbcr3.png)

Yc<sub>b</sub>C<sub>r</sub> -Daten werden in der Regel mit einem planaren Speicher Layout gespeichert. Dies bedeutet, dass jede Farbkomponente separat in einer eigenen zusammenhängenden Ebene gespeichert wird, sodass insgesamt drei Ebenen zur Auswahl stehen. In einer anderen allgemeinen Konfiguration werden die Komponenten c<sub>b</sub> und c<sub>r</sub> zusammengefasst und zusammen gespeichert, während die Y-Komponente auf der eigenen Ebene bleibt, um insgesamt zwei Ebenen zu erhalten.

Im folgenden finden Sie eine Abbildung der planaren Y-und verschachtelten c<sub>b</sub><sub>-c-Pixeldaten</sub> , einem gemeinsamen Speicher Layout für Yc<sub>b</sub>c<sub>r</sub> .

![eine Abbildung, die planare y und verschachtelte CbCr-Pixeldaten zeigt, ein gängiges YCbCr-Speicher Layout.](graphics/ycbcr4.png)

Sowohl in WIC als auch in Direct2D wird jede Farb Ebene als eigenes, eindeutiges Objekt behandelt (entweder [IWICBitmapSource](-wic-imp-iwicbitmapsource.md) oder [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)), und diese Ebenen bilden zusammen die Unterstützungs Daten für ein Yc <sub>b</sub>C <sub>r</sub> -Image.

Obwohl WIC den Zugriff auf Yc<sub>b</sub>c<sub>r</sub> -Daten in den Konfigurationen der Konfigurationen 2 und 3 unterstützt, unterstützt Direct2D nur das erste (Y und c<sub>b</sub>c<sub>r</sub>). Wenn Sie WIC und Direct2D verwenden, sollten Sie daher immer die 2-Zc<sub>b</sub>C<sub>r</sub> -Konfiguration verwenden.

### <a name="chroma-subsampling"></a>Chroma-Unterstichprobe

Das Yc<sub>b</sub>C<sub>r</sub> Color-Modell eignet sich gut für Szenarien mit digitaler Abbild Erstellung, da es bestimmte Aspekte des menschlichen visuellen Systems nutzen kann. Insbesondere sind die Änderungen an der Leuchtkraft (Helligkeit) eines Bilds sensibler und weniger sensibel für Chrominanz (Farbe). Durch Aufteilen der Farbdaten in separate "Leuchtdichte"-und "Chrominanz"-Komponenten können wir nur die Chrominanz-Komponenten selektiv komprimieren, um Speicherplatz Einsparungen mit minimalem Qualitätsverlust zu erzielen.

Eine solche Vorgehensweise wird als Chroma-Unterstichprobe bezeichnet. Die c<sub>b</sub> -und c<sub>r</sub> -Ebenen werden in einer oder beiden horizontalen und vertikalen Dimensionen als Stichprobe (herabgestuft) untersucht. Aus historischen Gründen wird jeder Chroma-unter Samplingmodus häufig mit einem dreiteiligen j:a: b-Verhältnis bezeichnet.



| Untersamplingmodus | Horizontale downscale | Vertikale downscale | Bits pro Pixel\* |
|------------------|----------------------|--------------------|------------------|
| 4:4:4            | 1x                   | 1x                 | 24               |
| 4:2:2            | 2x                   | 1x                 | 16               |
| 4:4:0            | 1x                   | 2x                 | 16               |
| 4:2:0            | 2x                   | 2x                 | 12               |



 

\* Schließt Y-Daten ein.

Wenn Sie in der obigen Tabelle Yc<sub>b</sub>C<sub>r</sub> verwenden, um unkomprimierte Bilddaten zu speichern, können Sie eine Arbeitsspeicher Einsparung von 25% bis 62,5% im Vergleich zu 32 Bit pro Pixel-RGBA-Daten erzielen, je nachdem, welcher Chroma-subsamplingmodus verwendet wird.

### <a name="jpeg-usage-of-ycsubbsubcsubrsub"></a>JPEG-Verwendung von Yc<sub>b</sub>C<sub>r</sub>

Im großen Umfang besteht die JPEG-Komprimierungs Pipeline aus den folgenden Stufen:

1.  Entropie (z. b. Huffman)-Komprimierung ausführen
2.  Ausführen von "Debug"
3.  Ausführen umgekehrter diskreter Kosinus-Transformation
4.  Ausführen von Chroma-Upsampling für c<sub>b</sub>c<sub>r</sub> -Daten
5.  Konvertieren von Yc<sub>b</sub>C<sub>r</sub> -Daten in RGBA (falls erforderlich)

Wenn der JPEG-Codec Yc<sub>b</sub>C<sub>r</sub> -Daten erzeugt, können wir die letzten beiden Schritte des Decodierungsprozesses vermeiden oder Sie auf die GPU verschieben. Zusätzlich zu den im vorherigen Abschnitt aufgeführten Speicher Einsparungen reduziert dies die Gesamtzeit, die zum Decodieren des Images benötigt wird. Beim Codieren von Yc<sub>b</sub>C<sub>r</sub> -Daten gelten die gleichen Einsparungen.

## <a name="using-jpeg-ycsubbsubcsubrsub-data"></a>Verwenden von JPEG Yc<sub>b</sub>c<sub>r</sub> -Daten

In diesem Abschnitt wird erläutert, wie Sie WIC und Direct2D verwenden, um mit Yc<sub>b</sub>C<sub>r</sub> -Daten zu arbeiten.

Informationen zu den in diesem Dokument verwendeten Anleitungen finden Sie im [Beispiel JPEG YCbCr Optimierungen in Direct2D und WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample) , in dem alle Schritte veranschaulicht werden, die zum Decodieren und Rendering von Yc<sub>b</sub>C<sub>r</sub> -Inhalt in einer Direct2D-App erforderlich sind.

### <a name="using-ycsubbsubcsubrsub-jpeg-images"></a>Verwenden von Yc<sub>b</sub>C<sub>r</sub> JPEG-Images

Die meisten JPEG-Images werden als Yc<sub>b</sub>C<sub>r</sub>gespeichert. Einige jggs enthalten CMYK-oder Graustufen-Daten und verwenden nicht Yc<sub>b</sub>C<sub>r</sub>. Dies bedeutet, dass Sie in der Regel, aber nicht immer, bereits vorhandenen JPEG-Inhalt ohne Änderungen direkt verwenden können.

WIC und Direct2D unterstützen nicht jede mögliche Yc<sub>b</sub>c<sub>r</sub> -Konfiguration, und die Unterstützung von Yc<sub>b</sub>c<sub>r</sub> in Direct2D hängt von der zugrunde liegenden Grafikhardware und dem Treiber ab. Aus diesem Grund muss eine allgemeine Abbild Pipeline für Images robust sein, die nicht Yc<sub>b</sub>c<sub>r</sub> verwenden (einschließlich anderer allgemeiner Bildformate wie PNG oder BMP), oder für Fälle, in denen die Unterstützung von Yc<sub>b</sub>c<sub>r</sub> nicht verfügbar ist. Es wird empfohlen, dass Sie Ihre vorhandene BGRA-basierte Abbild Erstellungs Pipeline beibehalten und Yc<sub>b</sub>C<sub>r</sub> als Leistungsoptimierung aktivieren, falls verfügbar.

### <a name="windows-imaging-component-apis"></a>Windows Imaging-Komponenten-APIs

Mit WIC in Windows 8.1 werden drei neue Schnittstellen hinzugefügt, um den Zugriff auf JPEG Yc<sub>b</sub>C<sub>r</sub> -Daten bereitzustellen.

### <a name="iwicplanarbitmapsourcetransform"></a>Iwicplanarbitmapsourcetransform

[**Iwicplanarbitmapsourcetransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) ist analog zu [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), mit dem Unterschied, dass es Pixel in einer planaren Konfiguration erzeugt, einschließlich Yc <sub>b</sub>C <sub>r</sub> -Daten. Sie können diese Schnittstelle abrufen, indem Sie QueryInterface für eine Implementierung von [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) aufrufen, die planaren Zugriff unterstützt. Dies umfasst die Implementierung von [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) des JPEG-Codecs sowie [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)und [**iwiccolortransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform).

### <a name="iwicplanarbitmapframeencode"></a>Iwicplanarbitmapframecocode

[**Iwicplanarbitmapframeencode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) bietet die Möglichkeit, planare Pixeldaten, einschließlich Yc <sub>b</sub>C <sub>r</sub> -Daten, zu codieren. Sie können diese Schnittstelle abrufen, indem Sie QueryInterface in der Implementierung von [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)des JPEG-Codecs aufrufen.

### <a name="iwicplanarformatconverter"></a>Iwicplanarformatconverter

[**Iwicplanarformatconverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) ermöglicht [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) das Verarbeiten von planaren Pixeldaten, einschließlich Yc <sub>b</sub>C <sub>r</sub>, und das Konvertieren in ein verschachtelter Pixel Format. Es macht nicht die Möglichkeit verfügbar, verschachtelte Pixeldaten in ein planare-Format zu konvertieren. Sie können diese Schnittstelle abrufen, indem Sie QueryInterface in der von Windows bereitgestellten Implementierung von **IWICFormatConverter** aufrufen.

### <a name="direct2d-apis"></a>Direct2D-APIs

Direct2D in Windows 8.1 unterstützt Yc<sub>b</sub>c<sub>r</sub> -planare Pixeldaten mit dem neuen Yc<sub>b</sub>c<sub>r</sub> -Image Effekt. Dieser Effekt bietet die Möglichkeit zum Rendering von Yc<sub>b</sub>C<sub>r</sub> -Daten. Der Effekt nimmt als Eingabe zwei [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Schnittstellen an: eine mit planaren Y-Daten im unorm-Format des DXGI- \_ Formats \_ \_ und eine mit verschachtelten CbCr-Daten im DXGI- \_ Format \_ R8G8 \_ unorm-Format. Normalerweise verwenden Sie diesen Effekt anstelle der **ID2D1Bitmap** , die BGRA-Pixeldaten enthalten würden.

Der JC<sub>b</sub>c<sub>r</sub> -Image Effekt ist für die Verwendung in Verbindung mit den WIC Yc<sub>b</sub>c<sub>r</sub> -APIs vorgesehen, die die Yc<sub>b</sub>c<sub>r</sub> -Daten bereitstellen. Dies verhält sich effektiv, um einige der Decodierungs Arbeiten von der CPU auf die GPU auszulagern, wo Sie viel schneller und parallel verarbeitet werden kann.

### <a name="determining-if-the-ycsubbsubcsubrsub-configuration-is-supported"></a>Ermitteln, ob die JC<sub>b</sub><sub>-C-</sub> Konfiguration unterstützt wird

Wie bereits erwähnt, sollte Ihre APP für Fälle, in denen die Unterstützung von Yc<sub>b</sub>C<sub>r</sub> nicht verfügbar ist, robust sein. In diesem Abschnitt werden die Bedingungen erläutert, die von Ihrer APP überprüft werden sollten. Wenn eine der folgenden Überprüfungen fehlschlägt, sollte Ihre APP auf eine standardmäßige BGRA-basierte Pipeline zurückgreifen.

### <a name="does-the-wic-component-support-ycsubbsubcsubrsub-data-access"></a>Unterstützt die WIC-Komponente den Yc<sub>b</sub>C<sub>r</sub> -Datenzugriff?

Nur der von Windows bereitgestellte JPEG-Codec und bestimmte WIC-Transformationen unterstützen den JC<sub>b</sub>C<sub>r</sub> -Datenzugriff. Eine umfassende Liste finden Sie im Abschnitt APIs für die [Windows Imaging-Komponente](#windows-imaging-component-apis) .

Rufen Sie QueryInterface in der ursprünglichen-Schnittstelle auf, um eine der planaren Yc<sub>b</sub>-c-<sub>Schnittstellen zu</sub> erhalten. Dies schlägt fehl, wenn die Komponente den Yc<sub>b</sub>C<sub>r</sub> -Datenzugriff nicht unterstützt.

### <a name="is-the-requested-wic-transform-supported-for-ycsubbsubcsubrsub"></a>Wird die angeforderte WIC-Transformation für Yc<sub>b</sub>C<sub>r</sub>unterstützt?

Nachdem Sie eine [**iwicplanarbitmapsourcetransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)erhalten haben, sollten Sie zuerst [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform)aufrufen. Diese Methode verwendet als Eingabeparameter den gesamten Satz von Transformationen, die auf die planaren Yc<sub>b</sub>C<sub>r</sub> -Daten angewendet werden sollen, und gibt einen booleschen Wert zurück, der die Unterstützung angibt, sowie die nächstgelegenen Dimensionen der angeforderten Größe, die zurückgegeben werden können. Überprüfen Sie alle drei Werte, bevor Sie auf die Pixeldaten mit [**iwicplanarbitmapsourcetransform:: CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels)zugreifen.

Dieses Muster ähnelt der Verwendung von [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) .

### <a name="does-the-graphics-driver-support-the-features-necessary-to-use-ycsubbsubcsubrsub-with-direct2d"></a>Unterstützt der Grafiktreiber die Features, die für die Verwendung von Yc<sub>b</sub>C<sub>r</sub> mit Direct2D erforderlich sind?

Diese Überprüfung ist nur erforderlich, wenn Sie den Direct2D Yc<sub>b</sub>c<sub>r</sub> -Effekt zum Rendering von Yc<sub>b</sub>c<sub>r</sub> -Inhalt verwenden. Direct2D speichert Yc<sub>b</sub>c<sub>r</sub> -Daten mit dem DXGI \_ \_ -Format R8 \_ unorm und DXGI \_ Format \_ R8G8 \_ unorm Pixel Formats, die nicht für alle Grafiktreiber verfügbar sind.

Vor der Verwendung des JC <sub>b</sub>C <sub>r</sub> -Image Effekts sollte [**ID2D1DeviceContext:: isdxgiformatsupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) aufgerufen werden, um sicherzustellen, dass beide Formate vom Treiber unterstützt werden.

### <a name="sample-code"></a>Beispielcode

Im folgenden finden Sie ein Codebeispiel, das die empfohlenen Überprüfungen veranschaulicht. Dieses Beispiel stammt aus den [JPEG YCbCr-Optimierungen in Direct2D und WIC Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


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



### <a name="decoding-ycsubbsubcsubrsub-pixel-data"></a>Decodieren von Yc<sub>b</sub>C<sub>r</sub> -Pixel Daten

Wenn Sie Yc <sub>b</sub>C <sub>r</sub> -Pixeldaten abrufen möchten, sollten Sie [**iwicplanarbitmapsourcetransform:: CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels)aufrufen. Diese Methode kopiert Pixeldaten in ein Array von ausgefüllten [**wicbitmapplane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) -Strukturen, eines für jede gewünschte Datenebene (z. b. Y und c <sub>b</sub>c <sub>r</sub>). Eine **wicbitmapplane** enthält Informationen über die Pixeldaten und verweist auf den Speicherpuffer, der die Daten empfängt.

Wenn Sie die Yc <sub>b</sub>C-<sub>r</sub> -Pixeldaten mit anderen WIC-APIs verwenden möchten, sollten Sie eine ordnungsgemäß konfigurierte [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)erstellen, die "Lock"- [**Sperre**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) zum Abrufen des zugrunde liegenden Speicherpuffers verwenden und den Puffer der [**wicbitmapplane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) zuordnen, die zum Empfangen der YC <sub>b</sub>-c <sub>-Pixeldaten</sub> verwendet wird. Anschließend können Sie die [IWICBitmap](-wic-imp-iwicbitmapdecoder.md) normal verwenden.

Wenn Sie schließlich die Yc <sub>b</sub>c <sub>r</sub> -Daten in Direct2D Rendering möchten, sollten Sie ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Element aus jeder [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) erstellen und als Quelle für den JC <sub>b</sub>c <sub>r</sub> -Image Effekt verwenden. Mit WIC können Sie mehrere planare Konfigurationen anfordern. Bei der Interaktion mit Direct2D sollten Sie zwei Ebenen anfordern, eine mit GUID \_ WICPixelFormat8bppY und die andere mit GUID \_ WICPixelFormat16bppCbCr, da dies die von Direct2D erwartete Konfiguration ist.

### <a name="code-sample"></a>Codebeispiel

Im folgenden finden Sie ein Codebeispiel, in dem die Schritte zum Decodieren und Rendering von Yc<sub>b</sub>C<sub>r</sub> -Daten in Direct2D veranschaulicht werden. Dieses Beispiel stammt aus den [JPEG YCbCr-Optimierungen in Direct2D und WIC Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


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



### <a name="transforming-ycsubbsubcsubrsub-pixel-data"></a>Transformieren von Yc<sub>b</sub>C<sub>r</sub> -Pixel Daten

Das Transformieren von Yc <sub>b</sub>C <sub>r</sub> -Daten ist nahezu identisch mit der Decodierung, da beide [**iwicplanarbitmapsourcetransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)betreffen. Der einzige Unterschied ist der WIC-Objekt, von dem Sie die Schnittstelle abgerufen haben. Die von Windows bereitgestellten Scaler, Flip Rotator und Color Transform unterstützen alle Yc<sub>b</sub>C<sub>r</sub> -Zugriff.

### <a name="chaining-transforms-together"></a>Verketten von Transformationen

WIC unterstützt das Konzept der Verkettung mehrerer Transformationen. Beispielsweise können Sie die folgende WIC-Pipeline erstellen:

![ein Diagramm einer WIC-Pipeline, beginnend mit einem JPEG-Decoder.](graphics/ycbcr5.png)

Sie können dann QueryInterface für [**iwiccolortransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) aufrufen, um [**iwicplanarbitmapsourcetransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)zu erhalten. Die Farb Transformation kann mit den vorangehenden Transformationen kommunizieren und die Aggregatfunktionen jeder Phase in der Pipeline verfügbar machen. WIC stellt sicher, dass die Yc<sub>b</sub>C<sub>r</sub> -Daten durch den gesamten Prozess beibehalten werden. Diese Verkettung funktioniert nur bei Verwendung von Komponenten, die Yc<sub>b</sub>C<sub>r</sub> -Zugriff unterstützen.

### <a name="jpeg-codec-optimizations"></a>JPEG-Codec-Optimierungen

Ähnlich wie bei der Implementierung der JPEG-Frame-Decodierung von [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)unterstützt die JPEG-Frame-Decodierung von [**iwicplanarbitmapsourcetransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) das Skalieren und Drehen von systemeigenen JPEG-DCT-Domänen. Sie können eine Potenz von zwei downscale oder Drehung direkt vom JPEG-Decoder anfordern. Dies führt in der Regel zu einer höheren Qualität und Leistung als bei der Verwendung der diskreten Transformationen.

Wenn Sie eine oder mehrere WIC-Transformationen nach dem JPEG-Decoder verketten, können Sie außerdem die systemeigene JPEG-Skalierung und-Rotation nutzen, um den angeforderten Vorgang zu erfüllen.

### <a name="format-conversions"></a>Format Konvertierungen

Verwenden Sie [**iwicplanarformatconverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) zum Konvertieren von planaren <sub>Yc b-C-</sub> Daten in ein überlappendes Pixel Format, z.<sub>b</sub>. GUID \_ WICPixelFormat32bppPBGRA. WIC in Windows 8.1 bietet keine Möglichkeit, in ein planare Yc<sub>b</sub>C-<sub>r</sub> -Pixel-Format zu konvertieren.

### <a name="encoding-ycsubbsubcsubrsub-pixel-data"></a>Codieren von Yc<sub>b</sub>C<sub>r</sub> -Pixel Daten

Verwenden Sie [**iwicplanarbitmapframeencode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) zum Codieren von Yc <sub>b</sub>-C-<sub>r</sub> -Pixeldaten in den JPEG-Encoder. Encoding Yc <sub>b</sub>C <sub>r</sub> Data **iwicplanarbitmapframeencode** ist ähnlich, aber nicht identisch mit der Codierung überlappenden Daten mithilfe von [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). Die planare-Schnittstelle macht nur die Möglichkeit verfügbar, planare Frame Bilddaten zu schreiben, und Sie sollten die Frame Codierungs Schnittstelle weiterhin verwenden, um Metadaten oder eine Miniaturansicht festzulegen und am Ende des Vorgangs einen Commit durchzuführen.

In den üblichen Fällen sollten Sie die folgenden Schritte ausführen:

1.  Rufen Sie [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) wie gewohnt ab. Wenn Sie die Chroma-Unterstichprobe konfigurieren möchten, legen Sie beim Erstellen des Frames die Option [**jpeer**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) -Encoder-Encoder fest.
2.  Wenn Sie Metadaten oder eine Miniaturansicht festlegen müssen, verwenden Sie hierfür [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .
3.  QueryInterface für [**iwicplanarbitmapframeencode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode).
4.  Legen Sie die Yc <sub>b</sub><sub>-C-</sub> Pixeldaten mithilfe von [**iwicplanarbitmapframeencode:: Beschreib tesource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writesource) oder [**iwicplanarbitmapframeencode:: schreitepixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writepixels)fest. Anders als bei Ihren [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Entsprechungen stellen Sie diese Methoden mit einem Array von [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) oder [**wicbitmapplane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) bereit, das die Yc <sub>b</sub>C <sub>r</sub> -Pixel Ebenen enthält.
5.  Wenn Sie fertig sind, wenden Sie sich an [**iwicbitmapframecocode:: Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).

### <a name="decoding-ycsubbsubcsubrsub-pixel-data-in-windows-10"></a>Decodieren von Yc<sub>b</sub>C<sub>r</sub> Pixel-Daten in Windows 10

Ab Windows 10 Build [**1507 bietet Direct2D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)eine einfachere Möglichkeit zum Decodieren von jppgs in Direct2D während der Nutzung von Yc <sub>b</sub>C <sub>r</sub> -Optimierungen. **ID2D1ImageSourceFromWic** führt automatisch alle erforderlichen Überprüfungen von Yc <sub>b</sub>C <sub>r</sub> -Funktionen für Sie durch. Er verwendet den optimierten Codepfad, wenn möglich, und verwendet andernfalls ein Fall Back. Außerdem werden neue Optimierungen ermöglicht, wie z. b. nur das Zwischenspeichern von Unterbereichen des Bilds, die jeweils benötigt werden.

Weitere Informationen zur Verwendung von [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)finden Sie im [Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)für das Direct2D Photo-Anpassungs-SDK.

## <a name="related-topics"></a>Zugehörige Themen

* [JPEG YCbCr-Optimierungen in Direct2D und WIC Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)
