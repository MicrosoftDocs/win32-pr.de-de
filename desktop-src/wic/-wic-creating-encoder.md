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
# <a name="encoding-overview"></a><span data-ttu-id="038aa-104">Übersicht über die Codierung</span><span class="sxs-lookup"><span data-stu-id="038aa-104">Encoding Overview</span></span>

<span data-ttu-id="038aa-105">Ein Encoder schreibt Bilddaten in einen Stream.</span><span class="sxs-lookup"><span data-stu-id="038aa-105">An encoder writes image data to a stream.</span></span> <span data-ttu-id="038aa-106">Encoder können die Bildpixel auf verschiedene Weise komprimieren, verschlüsseln und ändern, bevor sie in den Stream geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="038aa-106">Encoders can compress, encrypt, and alter the image pixels in a number of ways prior to writing them to the stream.</span></span> <span data-ttu-id="038aa-107">Die Verwendung einiger Encoder führt zu Kompromissen, z. B. JPEG, bei dem Farbinformationen für eine bessere Komprimierung abgehandelt werden.</span><span class="sxs-lookup"><span data-stu-id="038aa-107">Using some encoders results in tradeoffs—for example, JPEG, which trades off color information for better compression.</span></span> <span data-ttu-id="038aa-108">Andere Encoder führen nicht zu solchen Verlusten, z. B. Bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="038aa-108">Other encoders do not result in such losses—for example, bitmap (BMP).</span></span> <span data-ttu-id="038aa-109">Da viele Codecs proprietäre Technologie verwenden, um eine bessere Komprimierung und Bildgenauigkeit zu erzielen, sind die Details zur Codierung eines Bilds vom Codecentwickler selbst zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="038aa-109">Because many codecs use proprietary technology to achieve better compression and image fidelity, the details on how an image gets encoded are up to the codec developer.</span></span>

<span data-ttu-id="038aa-110">Das Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="038aa-110">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="038aa-111">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="038aa-111">IWICBitmapEncoder</span></span>](#iwicbitmapencoder)
-   [<span data-ttu-id="038aa-112">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="038aa-112">IWICBitmapFrameEncode</span></span>](#iwicbitmapframeencode)
-   [<span data-ttu-id="038aa-113">TIFF-Codierungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="038aa-113">TIFF Encoding Example</span></span>](#tiff-encoding-example)
-   [<span data-ttu-id="038aa-114">Verwendung von Encoderoptionen</span><span class="sxs-lookup"><span data-stu-id="038aa-114">Encoder Options Usage</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="038aa-115">Encoderoptionen</span><span class="sxs-lookup"><span data-stu-id="038aa-115">Encoder Options</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="038aa-116">Beispiele für Encoderoptionen</span><span class="sxs-lookup"><span data-stu-id="038aa-116">Encoder Options Examples</span></span>](#encoder-options-examples)
-   [<span data-ttu-id="038aa-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="038aa-117">Related topics</span></span>](#related-topics)

## <a name="iwicbitmapencoder"></a><span data-ttu-id="038aa-118">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="038aa-118">IWICBitmapEncoder</span></span>

<span data-ttu-id="038aa-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) ist die Hauptschnittstelle zum Codieren eines Bilds in das Zielformat und wird verwendet, um die Komponenten eines Bilds, z. B. Miniaturansicht ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) und Frames ([**CreateNewFrame),**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)in die Bilddatei zu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="038aa-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) is the main interface for encoding an image to the target format and used to serialize an image's components, such as thumbnail ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) and frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), to the image file.</span></span>

<span data-ttu-id="038aa-120">Wie und wann die Serialisierung erfolgt, bleibt dem Codecentwickler übrig.</span><span class="sxs-lookup"><span data-stu-id="038aa-120">How and when serialization occurs is left up to the codec developer.</span></span> <span data-ttu-id="038aa-121">Jeder einzelne Datenblock im Zieldateiformat sollte unabhängig von der Reihenfolge festgelegt werden können. Dies ist jedoch auch hier die Entscheidung des Codecentwicklers.</span><span class="sxs-lookup"><span data-stu-id="038aa-121">Each individual block of data within the target file format should be able to set independent of order, but again, this is the codec developer's decision.</span></span> <span data-ttu-id="038aa-122">Nachdem die [**Commit-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) aufgerufen wurde, sollten Änderungen am Image jedoch nicht zulässig sein, und der Stream sollte geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="038aa-122">Once the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method is called however, changes to the image should not be allowed and the stream should be closed.</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="038aa-123">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="038aa-123">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="038aa-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) ist die Schnittstelle zum Codieren der einzelnen Frames eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="038aa-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the interface for encoding the individual frames of an image.</span></span> <span data-ttu-id="038aa-125">Es stellt Methoden zum Festlegen einzelner Bildbildkomponenten für Frames bereit, z. B. Miniaturansichten und Frames, sowie Bilddimensionen, DPI- und Pixelformate.</span><span class="sxs-lookup"><span data-stu-id="038aa-125">It provides methods for setting individual frame imaging components, such as thumbnails and frames, as well as image dimensions, DPI, and pixel formats.</span></span>

<span data-ttu-id="038aa-126">Einzelne Frames können mit framespezifischen Metadaten codiert werden, sodass [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) über die [**GetMetadataQueryWriter-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) Zugriff auf einen Metadatenwriter bietet.</span><span class="sxs-lookup"><span data-stu-id="038aa-126">Individual frames may be encoded with frame-specific metadata so [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) provides access to a metadata writer through the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

<span data-ttu-id="038aa-127">Die [**Commit-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) des Frames committet alle Änderungen am einzelnen Frame und gibt an, dass Änderungen an diesem Frame nicht mehr akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="038aa-127">The frame's [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method commits all changes to the individual frame and indicates that changes to that frame should no longer be accepted.</span></span>

## <a name="tiff-encoding-example"></a><span data-ttu-id="038aa-128">TIFF-Codierungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="038aa-128">TIFF Encoding Example</span></span>

<span data-ttu-id="038aa-129">Im folgenden Beispiel wird ein Tagged Image File Format -Image (TIFF) mithilfe von [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) und einem [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)codiert.</span><span class="sxs-lookup"><span data-stu-id="038aa-129">In the following example, a Tagged Image File Format (TIFF) image is encoded using [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span> <span data-ttu-id="038aa-130">Die TIFF-Ausgabe wird mithilfe von [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) angepasst, und der Bitmapframe wird mit den angegebenen Optionen initialisiert.</span><span class="sxs-lookup"><span data-stu-id="038aa-130">The TIFF output is customized using the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) and the bitmap frame is initialized using the given options.</span></span> <span data-ttu-id="038aa-131">Nachdem das Image mit [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)erstellt wurde, wird für den Frame ein Commit über [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) ausgeführt, und das Image wird mit [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)gespeichert.</span><span class="sxs-lookup"><span data-stu-id="038aa-131">Once the image has been created using [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), the frame is committed by way of [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) and the image is saved using [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span></span>


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



## <a name="encoder-options-usage"></a><span data-ttu-id="038aa-132">Verwendung von Encoderoptionen</span><span class="sxs-lookup"><span data-stu-id="038aa-132">Encoder Options Usage</span></span>

<span data-ttu-id="038aa-133">Verschiedene Encoder für verschiedene Formate müssen unterschiedliche Optionen für die Codierung eines Bilds verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="038aa-133">Different encoders for different formats need to expose different options for how an image is encoded.</span></span> <span data-ttu-id="038aa-134">Windows-Bilderstellungskomponente (WIC) bietet einen konsistenten Mechanismus zum Ausdrücken, ob Codierungsoptionen erforderlich sind, während Anwendungen weiterhin mit mehreren Encodern arbeiten können, ohne dass ein bestimmtes Format bekannt sein muss.</span><span class="sxs-lookup"><span data-stu-id="038aa-134">Windows Imaging Component (WIC) provides a consistent mechanism for expressing whether encoding options are required while still enabling applications to work with multiple encoders without requiring knowledge of a particular format.</span></span> <span data-ttu-id="038aa-135">Dies wird erreicht, indem ein [IPropertyBag-Parameter](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) für die [**CreateNewFrame-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) und die [**Initialize-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="038aa-135">This is accomplished by providing an [IPropertyBag](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) parameter on the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method and the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

<span data-ttu-id="038aa-136">Die Komponentenfactory bietet einen einfachen Erstellungspunkt zum Erstellen eines Eigenschaftenbehälters für Encoderoptionen.</span><span class="sxs-lookup"><span data-stu-id="038aa-136">The component factory provides an easy creation point for creating an encoder options property bag.</span></span> <span data-ttu-id="038aa-137">Codecs können diesen Dienst verwenden, wenn sie einen einfachen, intuitiven und nicht in Konflikt stehenden Satz von Encoderoptionen bereitstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="038aa-137">Codecs can use this service if they need to provide a simple, intuitive and non-conflicting set of encoder options.</span></span> <span data-ttu-id="038aa-138">Die Imaging-Eigenschaftenerfassung muss während der Erstellung mit allen Encoderoptionen initialisiert werden, die für diesen Codec relevant sind.</span><span class="sxs-lookup"><span data-stu-id="038aa-138">The imaging property bag must be initialized during creation with all the encoder options relevant to that codec.</span></span> <span data-ttu-id="038aa-139">Für Encoderoptionen aus dem kanonischen Satz wird der Wertbereich beim Schreiben erzwungen.</span><span class="sxs-lookup"><span data-stu-id="038aa-139">For encoder options from the canonical set, the value range will be enforced on Write.</span></span> <span data-ttu-id="038aa-140">Für erweiterte Anforderungen sollten Codecs ihre eigene Implementierung von Eigenschaftentüten schreiben.</span><span class="sxs-lookup"><span data-stu-id="038aa-140">For more advanced needs, codecs should write their own property bag implementation.</span></span>

<span data-ttu-id="038aa-141">Eine Anwendung erhält während der Frameerstellung den Encoderoptionen-Bag und muss vor der Initialisierung des Encoderframes alle Werte konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="038aa-141">An application is given the encoder options bag during frame creation and must configure any values prior to initializing the encoder frame.</span></span> <span data-ttu-id="038aa-142">Für eine benutzeroberflächengesteuerte Anwendung kann sie eine feste Benutzeroberfläche für die kanonischen Encoderoptionen und eine erweiterte Ansicht für die verbleibenden Optionen anbieten.</span><span class="sxs-lookup"><span data-stu-id="038aa-142">For a UI-driven application, it can offer a fixed UI for the canonical encoder options and an advanced view for remaining options.</span></span> <span data-ttu-id="038aa-143">Änderungen können nach und nach über die Write-Methode vorgenommen werden, und alle Fehler werden über IErrorLog gemeldet.</span><span class="sxs-lookup"><span data-stu-id="038aa-143">Changes can be made one at a time through the Write method and any error will be reported through IErrorLog.</span></span> <span data-ttu-id="038aa-144">Die Benutzeroberflächenanwendung sollte nach einer Änderung immer erneut lesen und alle Optionen anzeigen, falls die Änderung einen kaskadierten Effekt verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="038aa-144">The UI application should always re-read and display all options after making a change in case the change caused a cascade effect.</span></span> <span data-ttu-id="038aa-145">Eine Anwendung sollte darauf vorbereitet sein, die fehlgeschlagene Framein initialisierung für Codecs zu verarbeiten, die nur minimale Fehlerberichte über ihre Eigenschaftentüte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="038aa-145">An application should be prepared to handle failed frame initialization for codecs that only provide minimal error reporting through their property bag.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="038aa-146">Encoderoptionen</span><span class="sxs-lookup"><span data-stu-id="038aa-146">Encoder Options</span></span>

<span data-ttu-id="038aa-147">Eine Anwendung kann die folgenden Encoderoptionen erwarten.</span><span class="sxs-lookup"><span data-stu-id="038aa-147">An application can expect to encounter the following set of encoder options.</span></span> <span data-ttu-id="038aa-148">Encoderoptionen spiegeln die Funktionen eines Encoders und des zugrunde liegenden Containerformats wider und sind daher von Natur aus nicht wirklich codecunabhängig.</span><span class="sxs-lookup"><span data-stu-id="038aa-148">Encoder options reflect the capabilities of an encoder and the underlying container format, and therefore are by their nature not really codec-agnostic.</span></span> <span data-ttu-id="038aa-149">Nach Möglichkeit sollten neue Optionen normalisiert werden, damit sie auf neue Codecs angewendet werden können, die entstehen.</span><span class="sxs-lookup"><span data-stu-id="038aa-149">When possible, new options should be normalized so they can be applied to new codecs that emerge.</span></span>



| <span data-ttu-id="038aa-150">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="038aa-150">Property Name</span></span>      | <span data-ttu-id="038aa-151">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="038aa-151">VARTYPE</span></span>  | <span data-ttu-id="038aa-152">Wert</span><span class="sxs-lookup"><span data-stu-id="038aa-152">Value</span></span>                                                                     | <span data-ttu-id="038aa-153">Anwendbare Codecs</span><span class="sxs-lookup"><span data-stu-id="038aa-153">Applicable Codecs</span></span> |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="038aa-154">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="038aa-154">ImageQuality</span></span>       | <span data-ttu-id="038aa-155">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="038aa-155">VT\_R4</span></span>   | <span data-ttu-id="038aa-156">0-1.0</span><span class="sxs-lookup"><span data-stu-id="038aa-156">0-1.0</span></span>                                                                     | <span data-ttu-id="038aa-157">JPEG, HDPhoto</span><span class="sxs-lookup"><span data-stu-id="038aa-157">JPEG, HDPhoto</span></span>     |
| <span data-ttu-id="038aa-158">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="038aa-158">CompressionQuality</span></span> | <span data-ttu-id="038aa-159">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="038aa-159">VT\_R4</span></span>   | <span data-ttu-id="038aa-160">0-1.0</span><span class="sxs-lookup"><span data-stu-id="038aa-160">0-1.0</span></span>                                                                     | <span data-ttu-id="038aa-161">TIFF</span><span class="sxs-lookup"><span data-stu-id="038aa-161">TIFF</span></span>              |
| <span data-ttu-id="038aa-162">Lossless</span><span class="sxs-lookup"><span data-stu-id="038aa-162">Lossless</span></span>           | <span data-ttu-id="038aa-163">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="038aa-163">VT\_BOOL</span></span> | <span data-ttu-id="038aa-164">**TRUE,** **FALSE**</span><span class="sxs-lookup"><span data-stu-id="038aa-164">**TRUE**, **FALSE**</span></span>                                                       | <span data-ttu-id="038aa-165">HDPhoto</span><span class="sxs-lookup"><span data-stu-id="038aa-165">HDPhoto</span></span>           |
| <span data-ttu-id="038aa-166">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="038aa-166">BitmapTransform</span></span>    | <span data-ttu-id="038aa-167">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="038aa-167">VT\_UI1</span></span>  | [<span data-ttu-id="038aa-168">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="038aa-168">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="038aa-169">JPEG</span><span class="sxs-lookup"><span data-stu-id="038aa-169">JPEG</span></span>              |



 

<span data-ttu-id="038aa-170">ImageQualty von 0.0 bedeutet die kleinstmögliche Wiedergabegenauigkeit und 1.0 die höchste Genauigkeit, was je nach Codec auch verlustfrei bedeuten kann.</span><span class="sxs-lookup"><span data-stu-id="038aa-170">ImageQualty of 0.0 means the lowest possible fidelity rendition and 1.0 means the highest fidelity, which may also imply lossless depending on the codec.</span></span>

<span data-ttu-id="038aa-171">CompressionQuality von 0.0 bedeutet, dass das am wenigsten effiziente Komprimierungsschema verfügbar ist, was in der Regel zu einer schnellen Codierung, aber einer größeren Ausgabe führt.</span><span class="sxs-lookup"><span data-stu-id="038aa-171">CompressionQuality of 0.0 means the least efficient compression scheme available, typically resulting in a fast encode but larger output.</span></span> <span data-ttu-id="038aa-172">Der Wert 1.0 bedeutet, dass das effizienteste verfügbare Schema verfügbar ist. In der Regel dauert die Codierung mehr Zeit, erzeugt aber eine kleinere Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="038aa-172">A value of 1.0 means the most efficient scheme available, typically taking more time to encode but producing smaller output.</span></span> <span data-ttu-id="038aa-173">Abhängig von den Funktionen des Codecs kann dieser Bereich einem diskreten Satz verfügbarer Komprimierungsmethoden zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="038aa-173">Depending on the capabilities of the codec, this range may be mapped onto a discrete set of available compression methods.</span></span>

<span data-ttu-id="038aa-174">Verlustfrei bedeutet, dass der Codec das Bild als verlustfrei codiert, ohne dass Bilddaten verloren sind.</span><span class="sxs-lookup"><span data-stu-id="038aa-174">Lossless means that the codec encodes the image as lossless with no image data loss.</span></span> <span data-ttu-id="038aa-175">Wenn Lossless aktiviert ist, wird ImageQuality ignoriert.</span><span class="sxs-lookup"><span data-stu-id="038aa-175">If Lossless is enabled, ImageQuality is ignored.</span></span>

<span data-ttu-id="038aa-176">Zusätzlich zu den oben genannten generischen Encoderoptionen unterstützen die mit WIC bereitgestellten Codecs die folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="038aa-176">In addition to the above generic encoder options, codecs supplied with WIC support the following options.</span></span> <span data-ttu-id="038aa-177">Wenn ein Codec eine Option unterstützen muss, die mit der Verwendung in diesen bereitgestellten Codecs konsistent ist, wird empfohlen, dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="038aa-177">If a codec has a need to support an option that is consistent with the usage in these supplied codecs, it is encouraged to do so.</span></span>



| <span data-ttu-id="038aa-178">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="038aa-178">Property Name</span></span>           | <span data-ttu-id="038aa-179">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="038aa-179">VARTYPE</span></span>           | <span data-ttu-id="038aa-180">Wert</span><span class="sxs-lookup"><span data-stu-id="038aa-180">Value</span></span>                                                                             | <span data-ttu-id="038aa-181">Anwendbare Codecs</span><span class="sxs-lookup"><span data-stu-id="038aa-181">Applicable Codecs</span></span> |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="038aa-182">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="038aa-182">InterlaceOption</span></span>         | <span data-ttu-id="038aa-183">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="038aa-183">VT\_BOOL</span></span>          | <span data-ttu-id="038aa-184">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="038aa-184">On/Off</span></span>                                                                            | <span data-ttu-id="038aa-185">PNG</span><span class="sxs-lookup"><span data-stu-id="038aa-185">PNG</span></span>               |
| <span data-ttu-id="038aa-186">FilterOption</span><span class="sxs-lookup"><span data-stu-id="038aa-186">FilterOption</span></span>            | <span data-ttu-id="038aa-187">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="038aa-187">VT\_UI1</span></span>           | [<span data-ttu-id="038aa-188">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="038aa-188">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | <span data-ttu-id="038aa-189">PNG</span><span class="sxs-lookup"><span data-stu-id="038aa-189">PNG</span></span>               |
| <span data-ttu-id="038aa-190">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="038aa-190">TiffCompressionMethod</span></span>   | <span data-ttu-id="038aa-191">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="038aa-191">VT\_UI1</span></span>           | [<span data-ttu-id="038aa-192">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="038aa-192">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | <span data-ttu-id="038aa-193">TIFF</span><span class="sxs-lookup"><span data-stu-id="038aa-193">TIFF</span></span>              |
| <span data-ttu-id="038aa-194">Luminance</span><span class="sxs-lookup"><span data-stu-id="038aa-194">Luminance</span></span>               | <span data-ttu-id="038aa-195">VT \_ UI4/VT \_ ARRAY</span><span class="sxs-lookup"><span data-stu-id="038aa-195">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="038aa-196">64 Einträge (DCT)</span><span class="sxs-lookup"><span data-stu-id="038aa-196">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="038aa-197">JPEG</span><span class="sxs-lookup"><span data-stu-id="038aa-197">JPEG</span></span>              |
| <span data-ttu-id="038aa-198">Chrominance</span><span class="sxs-lookup"><span data-stu-id="038aa-198">Chrominance</span></span>             | <span data-ttu-id="038aa-199">VT \_ UI4/VT \_ ARRAY</span><span class="sxs-lookup"><span data-stu-id="038aa-199">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="038aa-200">64 Einträge (DCT)</span><span class="sxs-lookup"><span data-stu-id="038aa-200">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="038aa-201">JPEG</span><span class="sxs-lookup"><span data-stu-id="038aa-201">JPEG</span></span>              |
| <span data-ttu-id="038aa-202">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="038aa-202">JpegYCrCbSubsampling</span></span>    | <span data-ttu-id="038aa-203">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="038aa-203">VT\_UI1</span></span>           | [<span data-ttu-id="038aa-204">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="038aa-204">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | <span data-ttu-id="038aa-205">JPEG</span><span class="sxs-lookup"><span data-stu-id="038aa-205">JPEG</span></span>              |
| <span data-ttu-id="038aa-206">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="038aa-206">SuppressApp0</span></span>            | <span data-ttu-id="038aa-207">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="038aa-207">VT\_BOOL</span></span>          |                                                                                   | <span data-ttu-id="038aa-208">JPEG</span><span class="sxs-lookup"><span data-stu-id="038aa-208">JPEG</span></span>              |
| <span data-ttu-id="038aa-209">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="038aa-209">EnableV5Header32bppBGRA</span></span> | <span data-ttu-id="038aa-210">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="038aa-210">VT\_BOOL</span></span>          | <span data-ttu-id="038aa-211">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="038aa-211">On/Off</span></span>                                                                            | <span data-ttu-id="038aa-212">BMP</span><span class="sxs-lookup"><span data-stu-id="038aa-212">BMP</span></span>               |



 

<span data-ttu-id="038aa-213">Verwenden **Sie VT \_ EMPTY,** um **\* anzugeben, dass nicht als \*** Standard festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="038aa-213">Use **VT\_EMPTY** to indicate **\*not set\*** as the default.</span></span> <span data-ttu-id="038aa-214">Wenn zusätzliche Eigenschaften festgelegt, aber nicht unterstützt werden, sollte der Encoder sie ignorieren. Dadurch können Anwendungen weniger Logik codieren, wenn sie eine Funktion wünschen, die möglicherweise vorhanden ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="038aa-214">If additional properties are set but not supported, the encoder should ignore them; this allows applications to code less logic if they want a capability that may or may not be present.</span></span>

## <a name="encoder-options-examples"></a><span data-ttu-id="038aa-215">Beispiele für Encoderoptionen</span><span class="sxs-lookup"><span data-stu-id="038aa-215">Encoder Options Examples</span></span>

<span data-ttu-id="038aa-216">Im [obigen TIFF-Codierungsbeispiel](#tiff-encoding-example) ist eine bestimmte Encoderoption festgelegt.</span><span class="sxs-lookup"><span data-stu-id="038aa-216">In the [TIFF Encoding Example](#tiff-encoding-example) above, a specific encoder option is set.</span></span> <span data-ttu-id="038aa-217">Der *pstrName-Member* der PROPBAG2-Struktur wird auf den entsprechenden Eigenschaftsnamen und variant auf den entsprechenden VARTYPE und den gewünschten Wert festgelegt – in diesem Fall ein Member der [**WICTiffCompressionOption-Enumeration.**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)</span><span class="sxs-lookup"><span data-stu-id="038aa-217">The *pstrName* member of the PROPBAG2 structure is set to the appropriate property name, and the VARIANT is set to the corresponding VARTYPE and the desired value—in this case, a member of the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) enumeration.</span></span>


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



<span data-ttu-id="038aa-218">Um die Standardencoderoptionen zu verwenden, initialisieren Sie einfach den Bitmapframe mit dem Eigenschaftentüt, der beim Erstellen des Frames zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="038aa-218">To use the default encoder options, simply initialize the bitmap frame with the property bag returned when the frame was created.</span></span>


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



<span data-ttu-id="038aa-219">Es ist auch möglich, die Eigenschaftentüte zu beseitigen, wenn keine Encoderoptionen berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="038aa-219">It is also possible to eliminate the property bag when no encoder options are being considered.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="038aa-220">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="038aa-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="038aa-221">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="038aa-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="038aa-222">Windows-Bilderstellungskomponente Übersicht</span><span class="sxs-lookup"><span data-stu-id="038aa-222">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="038aa-223">Übersicht über die Decodierung</span><span class="sxs-lookup"><span data-stu-id="038aa-223">Decoding Overview</span></span>](-wic-creating-decoder.md)
</dt> <dt>

<span data-ttu-id="038aa-224">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="038aa-224">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="038aa-225">Schreiben eines WIC-Enabled CODEC</span><span class="sxs-lookup"><span data-stu-id="038aa-225">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
