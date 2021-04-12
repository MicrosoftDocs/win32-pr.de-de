---
description: Ein Encoder schreibt Bilddaten in einen Stream. Encoder können die Bild Pixel auf verschiedene Weise komprimieren, verschlüsseln und ändern, bevor Sie Sie in den Stream schreiben.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Übersicht über die Codierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be46aa73082071deb69fdd402f42866b18ef0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218038"
---
# <a name="encoding-overview"></a>Übersicht über die Codierung

Ein Encoder schreibt Bilddaten in einen Stream. Encoder können die Bild Pixel auf verschiedene Weise komprimieren, verschlüsseln und ändern, bevor Sie Sie in den Stream schreiben. Die Verwendung einiger Encoder führt zu den vor-und Nachteile – z. b. JPEG, die Farbinformationen für eine bessere Komprimierung abwickelt. Andere Encoder führen nicht zu solchen Verlusten – z. b. Bitmap (BMP). Da viele Codecs proprietäre Technologien verwenden, um eine bessere Komprimierung und Bild Treue zu erzielen, werden die Details zur Codierung eines Bilds dem Codec-Entwickler angezeigt.

Das Thema enthält folgende Abschnitte:

-   [Iwicbitmapcoder](#iwicbitmapencoder)
-   [IWICBitmapFrameEncode](#iwicbitmapframeencode)
-   [Beispiel für TIFF-Codierung](#tiff-encoding-example)
-   [Verwendung von Encoder-Optionen](#encoder-options-usage)
-   [Codierungsoptionen](#encoder-options-usage)
-   [Beispiele für Codierungsoptionen](#encoder-options-examples)
-   [Zugehörige Themen](#related-topics)

## <a name="iwicbitmapencoder"></a>Iwicbitmapcoder

[**Iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) ist die Hauptschnittstelle zum Codieren eines Bilds in das Zielformat und wird zum Serialisieren der Komponenten eines Bilds, z. b. Miniaturansicht ([**setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) und Frames ("[**kreatenewframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe))", in die Bilddatei verwendet.

Wie und wann die Serialisierung stattfindet, wird dem Codec-Entwickler überlassen. Jeder einzelne Datenblock innerhalb des Ziel Datei Formats sollte in der Lage sein, unabhängig von der Reihenfolge festzulegen, aber dies ist die Entscheidung des Codec-Entwicklers. Nachdem die [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) -Methode aufgerufen wurde, sollten Änderungen am Bild nicht zulässig sein, und der Stream sollte geschlossen werden.

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**Iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) ist die Schnittstelle zum Codieren der einzelnen Frames eines Bilds. Es stellt Methoden zum Festlegen einzelner Frame-Imaging-Komponenten wie Miniaturansichten und Frames sowie Bild Dimensionen, dpi-und Pixel Formate bereit.

Einzelne Frames können mit Frame-spezifischen Metadaten codiert werden, damit [**iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) über die [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) -Methode Zugriff auf einen metadatenwriter bietet.

Die Commit-Methode des Frames führt einen [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) für alle Änderungen an den einzelnen Frame durch und gibt an, dass Änderungen an diesem Frame nicht mehr akzeptiert werden sollen.

## <a name="tiff-encoding-example"></a>Beispiel für TIFF-Codierung

Im folgenden Beispiel wird ein Tagged Image File Format-Bild (TIFF) mit [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) und einem [**iwicbitmapframecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)-Element codiert. Die TIFF-Ausgabe wird mithilfe von [**wictiffcompressionoption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) angepasst, und der BitmapFrame wird mithilfe der angegebenen Optionen initialisiert. Nachdem das Image mit " [**Write Pixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)" erstellt wurde, wird der Frame per [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) committet, und das Image wird mithilfe von [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)gespeichert.


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
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride**_/;
    UINT cbBufferSize = uiHeight _ cbStride;

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



## <a name="encoder-options-usage"></a>Verwendung von Encoder-Optionen

Verschiedene Encoder für verschiedene Formate müssen unterschiedliche Optionen für die Codierung eines Bilds verfügbar machen. Windows Imaging Component (WIC) stellt einen konsistenten Mechanismus dar, mit dem ausgedrückt werden soll, ob Codierungsoptionen erforderlich sind, während Anwendungen weiterhin mit mehreren Encodern arbeiten können, ohne dass ein bestimmtes Format erforderlich ist. Dies erfolgt durch Bereitstellen eines [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) -Parameters für die Methode "| [**atenewframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) " und die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) -Methode.

Die komponentenfactory bietet einen einfachen Erstellungs Punkt zum Erstellen eines Eigenschaften Behälters für Codierungsoptionen. Codecs können diesen Dienst verwenden, wenn Sie einen einfachen, intuitiven und nicht in Konflikt stehenden Satz von Codierungsoptionen bereitstellen müssen. Der Bild Verarbeitungseigenschaften Behälter muss während der Erstellung mit allen für diesen Codec relevanten Codierungsoptionen initialisiert werden. Bei Encoderoptionen aus der kanonischen Menge wird der Wertebereich beim Schreiben erzwungen. Für erweiterte Anforderungen sollten Codecs eine eigene Implementierung der Eigenschaften Behälter schreiben.

Einer Anwendung wird während der Frame Erstellung der Codierungsoptionen-Behälter zugewiesen, und vor dem Initialisieren des encoderframes müssen alle Werte konfiguriert werden. Für eine UI-gesteuerte Anwendung kann Sie eine Benutzeroberfläche für kanonische Codierungsoptionen und eine erweiterte Ansicht für verbleibende Optionen bieten. Änderungen können jeweils nacheinander durch die Write-Methode vorgenommen werden, und alle Fehler werden über IErrorLog gemeldet. Die Benutzeroberflächen Anwendung sollte immer erneut lesen und alle Optionen anzeigen, nachdem eine Änderung vorgenommen wurde, falls die Änderung zu einem kaskadierenden Effekt geführt hat. Eine Anwendung sollte darauf vorbereitet sein, die fehlgeschlagene Frame Initialisierung für Codecs zu behandeln, die nur minimale Fehlerberichterstattung über ihren Eigenschaften Behälter bereitstellen.

## <a name="encoder-options"></a>Codierungsoptionen

Eine Anwendung kann die folgenden Codierungsoptionen erwarten. Die Codierungsoptionen spiegeln die Funktionen eines Encoders und des zugrunde liegenden Container Formats wider und sind daher von Natur aus nicht wirklich Codec-agnostisch. Wenn möglich, sollten neue Optionen normalisiert werden, damit Sie auf neue Codecs angewendet werden können, die sich ergeben.



| Eigenschaftsname      | VARTYPE  | Wert                                                                     | Anwendbare Codecs |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| ImageQuality       | VT \_ R4   | 0-1.0                                                                     | JPEG, HDPhoto     |
| CompressionQuality | VT \_ R4   | 0-1.0                                                                     | TIFF              |
| Lossless           | VT \_ bool | **true**, **false**                                                       | HDPhoto           |
| BitmapTransform    | VT \_ UI1  | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | JPEG              |



 

Imagequalty von 0,0 bedeutet, dass die niedrigste mögliche Treue Gabe und 1,0 die höchste Genauigkeit bedeuten. Dies kann je nach Codec auch Verluste bedeuten.

CompressionQuality von 0,0 bedeutet das am wenigsten effiziente Komprimierungs Schema, das in der Regel eine schnelle Codierung, aber eine größere Ausgabe ergibt. Der Wert 1,0 ist das effizienteste verfügbare Schema, das in der Regel mehr Zeit in Anspruch nimmt, um eine geringere Ausgabe zu erzeugen. Abhängig von den Funktionen des Codecs kann dieser Bereich einem diskreten Satz verfügbarer Komprimierungs Methoden zugeordnet werden.

Verlust lose bedeutet, dass der Codec das Image als verlustfreie Methode ohne Bild Datenverlust codiert. Wenn Lossless aktiviert ist, wird ImageQuality ignoriert.

Zusätzlich zu den oben genannten generischen Codierungsoptionen unterstützen mit WIC bereitgestellte Codecs die folgenden Optionen. Wenn ein Codec eine Option unterstützen muss, die mit der Verwendung in den angegebenen Codecs konsistent ist, wird es empfohlen, dies zu tun.



| Eigenschaftsname           | VARTYPE           | Wert                                                                             | Anwendbare Codecs |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| InterlaceOption         | VT \_ bool          | Ein/Aus                                                                            | PNG               |
| FilterOption            | VT \_ UI1           | [**Wicpngfilteroption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | PNG               |
| TiffCompressionMethod   | VT \_ UI1           | [**Wictiffcompressionoption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | TIFF              |
| Luminance               | VT \_ UI4/VT- \_ Array | 64 Einträge (DCT)                                                                  | JPEG              |
| Chrominance             | VT \_ UI4/VT- \_ Array | 64 Einträge (DCT)                                                                  | JPEG              |
| JpegYCrCbSubsampling    | VT \_ UI1           | [**Wicjppfgycrcbsubsamplingoption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | JPEG              |
| SuppressApp0            | VT \_ bool          |                                                                                   | JPEG              |
| EnableV5Header32bppBGRA | VT \_ bool          | Ein/Aus                                                                            | BMP               |



 

Verwenden Sie **VT \_ empty** , um anzugeben, dass nicht als Standard **\* \* festgelegt** ist. Wenn zusätzliche Eigenschaften festgelegt, aber nicht unterstützt werden, sollte der Encoder diese ignorieren. Dadurch können Anwendungen weniger Logik codieren, wenn Sie eine Funktion benötigen, die möglicherweise vorhanden ist oder nicht.

## <a name="encoder-options-examples"></a>Beispiele für Codierungsoptionen

Im obigen [Beispiel](#tiff-encoding-example) für die TIFF-Codierung wird eine bestimmte Encoder-Option festgelegt. Der *pstrinname* -Member der PROPBAG2-Struktur wird auf den entsprechenden Eigenschaftsnamen festgelegt, und der Variant-Wert wird auf den entsprechenden VarType und den gewünschten Wert festgelegt – in diesem Fall ein Member der [**wictiffcompressionoption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) -Enumeration.


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



Um die standardmäßigen Codierungsoptionen zu verwenden, initialisieren Sie einfach den BitmapFrame mit dem Eigenschaften Behälter, der beim Erstellen des Frames zurückgegeben wurde.


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



Es ist auch möglich, den Eigenschaften Behälter zu entfernen, wenn keine Codierungsoptionen berücksichtigt werden.


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

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Decodierung: Übersicht](-wic-creating-decoder.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
