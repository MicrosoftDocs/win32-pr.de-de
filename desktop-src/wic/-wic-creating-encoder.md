---
description: Ein Encoder schreibt Bilddaten in einen Stream. Encoder können die Bildpixel auf verschiedene Weise komprimieren, verschlüsseln und ändern, bevor sie in den Stream geschrieben werden.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Übersicht über die Codierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f938e184dee7fd9b3e5348365550615ee28de70d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549485"
---
# <a name="encoding-overview"></a>Übersicht über die Codierung

Ein Encoder schreibt Bilddaten in einen Stream. Encoder können die Bildpixel auf verschiedene Weise komprimieren, verschlüsseln und ändern, bevor sie in den Stream geschrieben werden. Die Verwendung einiger Encoder führt zu Kompromissen, z. B. JPEG, bei dem Farbinformationen für eine bessere Komprimierung abgehandelt werden. Andere Encoder führen nicht zu solchen Verlusten, z. B. Bitmap (BMP). Da viele Codecs proprietäre Technologie verwenden, um eine bessere Komprimierung und Bildgenauigkeit zu erzielen, sind die Details zur Codierung eines Bilds vom Codecentwickler selbst zu erhalten.

Das Thema enthält folgende Abschnitte:

-   [IWICBitmapEncoder](#iwicbitmapencoder)
-   [IWICBitmapFrameEncode](#iwicbitmapframeencode)
-   [TIFF-Codierungsbeispiel](#tiff-encoding-example)
-   [Verwendung von Encoderoptionen](#encoder-options-usage)
-   [Encoderoptionen](#encoder-options-usage)
-   [Beispiele für Encoderoptionen](#encoder-options-examples)
-   [Verwandte Themen](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) ist die Hauptschnittstelle zum Codieren eines Bilds in das Zielformat und wird verwendet, um die Komponenten eines Bilds, z. B. Miniaturansicht ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) und Frames ([**CreateNewFrame),**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)in die Bilddatei zu serialisieren.

Wie und wann die Serialisierung erfolgt, bleibt dem Codecentwickler übrig. Jeder einzelne Datenblock im Zieldateiformat sollte unabhängig von der Reihenfolge festgelegt werden können. Dies ist jedoch auch hier die Entscheidung des Codecentwicklers. Nachdem die [**Commit-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) aufgerufen wurde, sollten Änderungen am Image jedoch nicht zulässig sein, und der Stream sollte geschlossen werden.

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) ist die Schnittstelle zum Codieren der einzelnen Frames eines Bilds. Es stellt Methoden zum Festlegen einzelner Bildbildkomponenten für Frames bereit, z. B. Miniaturansichten und Frames, sowie Bilddimensionen, DPI- und Pixelformate.

Einzelne Frames können mit framespezifischen Metadaten codiert werden, sodass [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) über die [**GetMetadataQueryWriter-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) Zugriff auf einen Metadatenwriter bietet.

Die [**Commit-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) des Frames committet alle Änderungen am einzelnen Frame und gibt an, dass Änderungen an diesem Frame nicht mehr akzeptiert werden sollen.

## <a name="tiff-encoding-example"></a>TIFF-Codierungsbeispiel

Im folgenden Beispiel wird ein Tagged Image File Format -Image (TIFF) mithilfe von [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) und einem [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)codiert. Die TIFF-Ausgabe wird mithilfe von [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) angepasst, und der Bitmapframe wird mit den angegebenen Optionen initialisiert. Nachdem das Image mit [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)erstellt wurde, wird für den Frame ein Commit über [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) ausgeführt, und das Image wird mit [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)gespeichert.


```C++
IWICImagingFactory *piFactory = NULL;
IWICBitmapEncoder *piEncoder = NULL;
IWICBitmapFrameEncode *piBitmapFrame = NULL;
IPropertyBag2 *pPropertybag = NULL;

IWICStream *piStream = NULL;
UINT uiWidth = 640;
UINT uiHeight = 480;

HRESULT hr = CoCreateInstance(
                CLSID_WICImagingFactory,
                NULL,
                CLSCTX_INPROC_SERVER,
                IID_IWICImagingFactory,
                (LPVOID*) &piFactory);

if (SUCCEEDED(hr))
{
    hr = piFactory->CreateStream(&piStream);
}

if (SUCCEEDED(hr))
{
    hr = piStream->InitializeFromFilename(L"output.tif", GENERIC_WRITE);
}

if (SUCCEEDED(hr))
{
   hr = piFactory->CreateEncoder(GUID_ContainerFormatTiff, NULL, &piEncoder);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->Initialize(piStream, WICBitmapEncoderNoCache);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetSize(uiWidth, uiHeight);
}

WICPixelFormatGUID formatGUID = GUID_WICPixelFormat24bppBGR;
if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetPixelFormat(&formatGUID);
}

if (SUCCEEDED(hr))
{
    // We're expecting to write out 24bppRGB. Fail if the encoder cannot do it.
    hr = IsEqualGUID(formatGUID, GUID_WICPixelFormat24bppBGR) ? S_OK : E_FAIL;
}

if (SUCCEEDED(hr))
{
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride***/;
    UINT cbBufferSize = uiHeight * cbStride;

    BYTE *pbBuffer = new BYTE[cbBufferSize];

    if (pbBuffer != NULL)
    {
        for (UINT i = 0; i < cbBufferSize; i++)
        {
            pbBuffer[i] = static_cast<BYTE>(rand());
        }

        hr = piBitmapFrame->WritePixels(uiHeight, cbStride, cbBufferSize, pbBuffer);

        delete[] pbBuffer;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->Commit();
}    

if (SUCCEEDED(hr))
{
    hr = piEncoder->Commit();
}

if (piFactory)
    piFactory->Release();

if (piEncoder)
    piEncoder->Release();

if (piBitmapFrame)
    piBitmapFrame->Release();

if (pPropertybag)
    pPropertybag->Release();

if (piStream)
    piStream->Release();

return hr;
```



## <a name="encoder-options-usage"></a>Verwendung von Encoderoptionen

Verschiedene Encoder für verschiedene Formate müssen unterschiedliche Optionen für die Codierung eines Bilds verfügbar machen. Windows-Bilderstellungskomponente (WIC) bietet einen konsistenten Mechanismus zum Ausdrücken, ob Codierungsoptionen erforderlich sind, während Anwendungen weiterhin mit mehreren Encodern arbeiten können, ohne dass ein bestimmtes Format bekannt sein muss. Dies wird erreicht, indem ein [IPropertyBag-Parameter](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) für die [**CreateNewFrame-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) und die [**Initialize-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) zur Verfügung gestellt wird.

Die Komponentenfactory bietet einen einfachen Erstellungspunkt zum Erstellen eines Eigenschaftenbehälters für Encoderoptionen. Codecs können diesen Dienst verwenden, wenn sie einen einfachen, intuitiven und nicht in Konflikt stehenden Satz von Encoderoptionen bereitstellen müssen. Die Imaging-Eigenschaftenerfassung muss während der Erstellung mit allen Encoderoptionen initialisiert werden, die für diesen Codec relevant sind. Für Encoderoptionen aus dem kanonischen Satz wird der Wertbereich beim Schreiben erzwungen. Für erweiterte Anforderungen sollten Codecs ihre eigene Implementierung von Eigenschaftentüten schreiben.

Eine Anwendung erhält während der Frameerstellung den Encoderoptionen-Bag und muss vor der Initialisierung des Encoderframes alle Werte konfigurieren. Für eine benutzeroberflächengesteuerte Anwendung kann sie eine feste Benutzeroberfläche für die kanonischen Encoderoptionen und eine erweiterte Ansicht für die verbleibenden Optionen anbieten. Änderungen können nach und nach über die Write-Methode vorgenommen werden, und alle Fehler werden über IErrorLog gemeldet. Die Benutzeroberflächenanwendung sollte nach einer Änderung immer erneut lesen und alle Optionen anzeigen, falls die Änderung einen kaskadierten Effekt verursacht hat. Eine Anwendung sollte darauf vorbereitet sein, die fehlgeschlagene Framein initialisierung für Codecs zu verarbeiten, die nur minimale Fehlerberichte über ihre Eigenschaftentüte bereitstellen.

## <a name="encoder-options"></a>Encoderoptionen

Eine Anwendung kann die folgenden Encoderoptionen erwarten. Encoderoptionen spiegeln die Funktionen eines Encoders und des zugrunde liegenden Containerformats wider und sind daher von Natur aus nicht wirklich codecunabhängig. Nach Möglichkeit sollten neue Optionen normalisiert werden, damit sie auf neue Codecs angewendet werden können, die entstehen.



| Eigenschaftsname      | VARTYPE  | Wert                                                                     | Anwendbare Codecs |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| ImageQuality       | VT \_ R4   | 0-1.0                                                                     | JPEG, HDPhoto     |
| CompressionQuality | VT \_ R4   | 0-1.0                                                                     | TIFF              |
| Lossless           | VT \_ BOOL | **TRUE,** **FALSE**                                                       | HDPhoto           |
| BitmapTransform    | VT \_ UI1  | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | JPEG              |



 

ImageQualty von 0.0 bedeutet die kleinstmögliche Wiedergabegenauigkeit und 1.0 die höchste Genauigkeit, was je nach Codec auch verlustfrei bedeuten kann.

CompressionQuality von 0.0 bedeutet, dass das am wenigsten effiziente Komprimierungsschema verfügbar ist, was in der Regel zu einer schnellen Codierung, aber einer größeren Ausgabe führt. Der Wert 1.0 bedeutet, dass das effizienteste verfügbare Schema verfügbar ist. In der Regel dauert die Codierung mehr Zeit, erzeugt aber eine kleinere Ausgabe. Abhängig von den Funktionen des Codecs kann dieser Bereich einem diskreten Satz verfügbarer Komprimierungsmethoden zugeordnet werden.

Verlustfrei bedeutet, dass der Codec das Bild als verlustfrei codiert, ohne dass Bilddaten verloren sind. Wenn Lossless aktiviert ist, wird ImageQuality ignoriert.

Zusätzlich zu den oben genannten generischen Encoderoptionen unterstützen die mit WIC bereitgestellten Codecs die folgenden Optionen. Wenn ein Codec eine Option unterstützen muss, die mit der Verwendung in diesen bereitgestellten Codecs konsistent ist, wird empfohlen, dies zu tun.



| Eigenschaftsname           | VARTYPE           | Wert                                                                             | Anwendbare Codecs |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| InterlaceOption         | VT \_ BOOL          | Ein/Aus                                                                            | PNG               |
| FilterOption            | VT \_ UI1           | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | PNG               |
| TiffCompressionMethod   | VT \_ UI1           | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | TIFF              |
| Luminance               | VT \_ UI4/VT \_ ARRAY | 64 Einträge (DCT)                                                                  | JPEG              |
| Chrominance             | VT \_ UI4/VT \_ ARRAY | 64 Einträge (DCT)                                                                  | JPEG              |
| JpegYCrCbSubsampling    | VT \_ UI1           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | JPEG              |
| SuppressApp0            | VT \_ BOOL          |                                                                                   | JPEG              |
| EnableV5Header32bppBGRA | VT \_ BOOL          | Ein/Aus                                                                            | BMP               |



 

Verwenden **Sie VT \_ EMPTY,** um **\* anzugeben, dass nicht als \*** Standard festgelegt ist. Wenn zusätzliche Eigenschaften festgelegt, aber nicht unterstützt werden, sollte der Encoder sie ignorieren. Dadurch können Anwendungen weniger Logik codieren, wenn sie eine Funktion wünschen, die möglicherweise vorhanden ist oder nicht.

## <a name="encoder-options-examples"></a>Beispiele für Encoderoptionen

Im [obigen TIFF-Codierungsbeispiel](#tiff-encoding-example) ist eine bestimmte Encoderoption festgelegt. Der *pstrName-Member* der PROPBAG2-Struktur wird auf den entsprechenden Eigenschaftsnamen und variant auf den entsprechenden VARTYPE und den gewünschten Wert festgelegt – in diesem Fall ein Member der [**WICTiffCompressionOption-Enumeration.**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



Um die Standardencoderoptionen zu verwenden, initialisieren Sie einfach den Bitmapframe mit dem Eigenschaftentüt, der beim Erstellen des Frames zurückgegeben wurde.


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // Accept the default encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



Es ist auch möglich, die Eigenschaftentüte zu beseitigen, wenn keine Encoderoptionen berücksichtigt werden.


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, 0);
}

if (SUCCEEDED(hr))
{        
    // No encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(0);
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows-Bilderstellungskomponente Übersicht](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über die Decodierung](-wic-creating-decoder.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
