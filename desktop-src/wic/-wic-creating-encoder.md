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
# <a name="encoding-overview"></a><span data-ttu-id="95a46-104">Übersicht über die Codierung</span><span class="sxs-lookup"><span data-stu-id="95a46-104">Encoding Overview</span></span>

<span data-ttu-id="95a46-105">Ein Encoder schreibt Bilddaten in einen Stream.</span><span class="sxs-lookup"><span data-stu-id="95a46-105">An encoder writes image data to a stream.</span></span> <span data-ttu-id="95a46-106">Encoder können die Bild Pixel auf verschiedene Weise komprimieren, verschlüsseln und ändern, bevor Sie Sie in den Stream schreiben.</span><span class="sxs-lookup"><span data-stu-id="95a46-106">Encoders can compress, encrypt, and alter the image pixels in a number of ways prior to writing them to the stream.</span></span> <span data-ttu-id="95a46-107">Die Verwendung einiger Encoder führt zu den vor-und Nachteile – z. b. JPEG, die Farbinformationen für eine bessere Komprimierung abwickelt.</span><span class="sxs-lookup"><span data-stu-id="95a46-107">Using some encoders results in tradeoffs—for example, JPEG, which trades off color information for better compression.</span></span> <span data-ttu-id="95a46-108">Andere Encoder führen nicht zu solchen Verlusten – z. b. Bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="95a46-108">Other encoders do not result in such losses—for example, bitmap (BMP).</span></span> <span data-ttu-id="95a46-109">Da viele Codecs proprietäre Technologien verwenden, um eine bessere Komprimierung und Bild Treue zu erzielen, werden die Details zur Codierung eines Bilds dem Codec-Entwickler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95a46-109">Because many codecs use proprietary technology to achieve better compression and image fidelity, the details on how an image gets encoded are up to the codec developer.</span></span>

<span data-ttu-id="95a46-110">Das Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="95a46-110">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="95a46-111">Iwicbitmapcoder</span><span class="sxs-lookup"><span data-stu-id="95a46-111">IWICBitmapEncoder</span></span>](#iwicbitmapencoder)
-   [<span data-ttu-id="95a46-112">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="95a46-112">IWICBitmapFrameEncode</span></span>](#iwicbitmapframeencode)
-   [<span data-ttu-id="95a46-113">Beispiel für TIFF-Codierung</span><span class="sxs-lookup"><span data-stu-id="95a46-113">TIFF Encoding Example</span></span>](#tiff-encoding-example)
-   [<span data-ttu-id="95a46-114">Verwendung von Encoder-Optionen</span><span class="sxs-lookup"><span data-stu-id="95a46-114">Encoder Options Usage</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="95a46-115">Codierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="95a46-115">Encoder Options</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="95a46-116">Beispiele für Codierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="95a46-116">Encoder Options Examples</span></span>](#encoder-options-examples)
-   [<span data-ttu-id="95a46-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95a46-117">Related topics</span></span>](#related-topics)

## <a name="iwicbitmapencoder"></a><span data-ttu-id="95a46-118">Iwicbitmapcoder</span><span class="sxs-lookup"><span data-stu-id="95a46-118">IWICBitmapEncoder</span></span>

<span data-ttu-id="95a46-119">[**Iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) ist die Hauptschnittstelle zum Codieren eines Bilds in das Zielformat und wird zum Serialisieren der Komponenten eines Bilds, z. b. Miniaturansicht ([**setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) und Frames ("[**kreatenewframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe))", in die Bilddatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="95a46-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) is the main interface for encoding an image to the target format and used to serialize an image's components, such as thumbnail ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) and frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), to the image file.</span></span>

<span data-ttu-id="95a46-120">Wie und wann die Serialisierung stattfindet, wird dem Codec-Entwickler überlassen.</span><span class="sxs-lookup"><span data-stu-id="95a46-120">How and when serialization occurs is left up to the codec developer.</span></span> <span data-ttu-id="95a46-121">Jeder einzelne Datenblock innerhalb des Ziel Datei Formats sollte in der Lage sein, unabhängig von der Reihenfolge festzulegen, aber dies ist die Entscheidung des Codec-Entwicklers.</span><span class="sxs-lookup"><span data-stu-id="95a46-121">Each individual block of data within the target file format should be able to set independent of order, but again, this is the codec developer's decision.</span></span> <span data-ttu-id="95a46-122">Nachdem die [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) -Methode aufgerufen wurde, sollten Änderungen am Bild nicht zulässig sein, und der Stream sollte geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="95a46-122">Once the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method is called however, changes to the image should not be allowed and the stream should be closed.</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="95a46-123">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="95a46-123">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="95a46-124">[**Iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) ist die Schnittstelle zum Codieren der einzelnen Frames eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="95a46-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the interface for encoding the individual frames of an image.</span></span> <span data-ttu-id="95a46-125">Es stellt Methoden zum Festlegen einzelner Frame-Imaging-Komponenten wie Miniaturansichten und Frames sowie Bild Dimensionen, dpi-und Pixel Formate bereit.</span><span class="sxs-lookup"><span data-stu-id="95a46-125">It provides methods for setting individual frame imaging components, such as thumbnails and frames, as well as image dimensions, DPI, and pixel formats.</span></span>

<span data-ttu-id="95a46-126">Einzelne Frames können mit Frame-spezifischen Metadaten codiert werden, damit [**iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) über die [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) -Methode Zugriff auf einen metadatenwriter bietet.</span><span class="sxs-lookup"><span data-stu-id="95a46-126">Individual frames may be encoded with frame-specific metadata so [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) provides access to a metadata writer through the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

<span data-ttu-id="95a46-127">Die Commit-Methode des Frames führt einen [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) für alle Änderungen an den einzelnen Frame durch und gibt an, dass Änderungen an diesem Frame nicht mehr akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="95a46-127">The frame's [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method commits all changes to the individual frame and indicates that changes to that frame should no longer be accepted.</span></span>

## <a name="tiff-encoding-example"></a><span data-ttu-id="95a46-128">Beispiel für TIFF-Codierung</span><span class="sxs-lookup"><span data-stu-id="95a46-128">TIFF Encoding Example</span></span>

<span data-ttu-id="95a46-129">Im folgenden Beispiel wird ein Tagged Image File Format-Bild (TIFF) mit [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) und einem [**iwicbitmapframecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)-Element codiert.</span><span class="sxs-lookup"><span data-stu-id="95a46-129">In the following example, a Tagged Image File Format (TIFF) image is encoded using [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span> <span data-ttu-id="95a46-130">Die TIFF-Ausgabe wird mithilfe von [**wictiffcompressionoption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) angepasst, und der BitmapFrame wird mithilfe der angegebenen Optionen initialisiert.</span><span class="sxs-lookup"><span data-stu-id="95a46-130">The TIFF output is customized using the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) and the bitmap frame is initialized using the given options.</span></span> <span data-ttu-id="95a46-131">Nachdem das Image mit " [**Write Pixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)" erstellt wurde, wird der Frame per [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) committet, und das Image wird mithilfe von [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)gespeichert.</span><span class="sxs-lookup"><span data-stu-id="95a46-131">Once the image has been created using [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), the frame is committed by way of [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) and the image is saved using [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span></span>


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



## <a name="encoder-options-usage"></a><span data-ttu-id="95a46-132">Verwendung von Encoder-Optionen</span><span class="sxs-lookup"><span data-stu-id="95a46-132">Encoder Options Usage</span></span>

<span data-ttu-id="95a46-133">Verschiedene Encoder für verschiedene Formate müssen unterschiedliche Optionen für die Codierung eines Bilds verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="95a46-133">Different encoders for different formats need to expose different options for how an image is encoded.</span></span> <span data-ttu-id="95a46-134">Windows Imaging Component (WIC) stellt einen konsistenten Mechanismus dar, mit dem ausgedrückt werden soll, ob Codierungsoptionen erforderlich sind, während Anwendungen weiterhin mit mehreren Encodern arbeiten können, ohne dass ein bestimmtes Format erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="95a46-134">Windows Imaging Component (WIC) provides a consistent mechanism for expressing whether encoding options are required while still enabling applications to work with multiple encoders without requiring knowledge of a particular format.</span></span> <span data-ttu-id="95a46-135">Dies erfolgt durch Bereitstellen eines [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) -Parameters für die Methode "| [**atenewframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) " und die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) -Methode.</span><span class="sxs-lookup"><span data-stu-id="95a46-135">This is accomplished by providing an [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) parameter on the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method and the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

<span data-ttu-id="95a46-136">Die komponentenfactory bietet einen einfachen Erstellungs Punkt zum Erstellen eines Eigenschaften Behälters für Codierungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="95a46-136">The component factory provides an easy creation point for creating an encoder options property bag.</span></span> <span data-ttu-id="95a46-137">Codecs können diesen Dienst verwenden, wenn Sie einen einfachen, intuitiven und nicht in Konflikt stehenden Satz von Codierungsoptionen bereitstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="95a46-137">Codecs can use this service if they need to provide a simple, intuitive and non-conflicting set of encoder options.</span></span> <span data-ttu-id="95a46-138">Der Bild Verarbeitungseigenschaften Behälter muss während der Erstellung mit allen für diesen Codec relevanten Codierungsoptionen initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="95a46-138">The imaging property bag must be initialized during creation with all the encoder options relevant to that codec.</span></span> <span data-ttu-id="95a46-139">Bei Encoderoptionen aus der kanonischen Menge wird der Wertebereich beim Schreiben erzwungen.</span><span class="sxs-lookup"><span data-stu-id="95a46-139">For encoder options from the canonical set, the value range will be enforced on Write.</span></span> <span data-ttu-id="95a46-140">Für erweiterte Anforderungen sollten Codecs eine eigene Implementierung der Eigenschaften Behälter schreiben.</span><span class="sxs-lookup"><span data-stu-id="95a46-140">For more advanced needs, codecs should write their own property bag implementation.</span></span>

<span data-ttu-id="95a46-141">Einer Anwendung wird während der Frame Erstellung der Codierungsoptionen-Behälter zugewiesen, und vor dem Initialisieren des encoderframes müssen alle Werte konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="95a46-141">An application is given the encoder options bag during frame creation and must configure any values prior to initializing the encoder frame.</span></span> <span data-ttu-id="95a46-142">Für eine UI-gesteuerte Anwendung kann Sie eine Benutzeroberfläche für kanonische Codierungsoptionen und eine erweiterte Ansicht für verbleibende Optionen bieten.</span><span class="sxs-lookup"><span data-stu-id="95a46-142">For a UI-driven application, it can offer a fixed UI for the canonical encoder options and an advanced view for remaining options.</span></span> <span data-ttu-id="95a46-143">Änderungen können jeweils nacheinander durch die Write-Methode vorgenommen werden, und alle Fehler werden über IErrorLog gemeldet.</span><span class="sxs-lookup"><span data-stu-id="95a46-143">Changes can be made one at a time through the Write method and any error will be reported through IErrorLog.</span></span> <span data-ttu-id="95a46-144">Die Benutzeroberflächen Anwendung sollte immer erneut lesen und alle Optionen anzeigen, nachdem eine Änderung vorgenommen wurde, falls die Änderung zu einem kaskadierenden Effekt geführt hat.</span><span class="sxs-lookup"><span data-stu-id="95a46-144">The UI application should always re-read and display all options after making a change in case the change caused a cascade effect.</span></span> <span data-ttu-id="95a46-145">Eine Anwendung sollte darauf vorbereitet sein, die fehlgeschlagene Frame Initialisierung für Codecs zu behandeln, die nur minimale Fehlerberichterstattung über ihren Eigenschaften Behälter bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="95a46-145">An application should be prepared to handle failed frame initialization for codecs that only provide minimal error reporting through their property bag.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="95a46-146">Codierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="95a46-146">Encoder Options</span></span>

<span data-ttu-id="95a46-147">Eine Anwendung kann die folgenden Codierungsoptionen erwarten.</span><span class="sxs-lookup"><span data-stu-id="95a46-147">An application can expect to encounter the following set of encoder options.</span></span> <span data-ttu-id="95a46-148">Die Codierungsoptionen spiegeln die Funktionen eines Encoders und des zugrunde liegenden Container Formats wider und sind daher von Natur aus nicht wirklich Codec-agnostisch.</span><span class="sxs-lookup"><span data-stu-id="95a46-148">Encoder options reflect the capabilities of an encoder and the underlying container format, and therefore are by their nature not really codec-agnostic.</span></span> <span data-ttu-id="95a46-149">Wenn möglich, sollten neue Optionen normalisiert werden, damit Sie auf neue Codecs angewendet werden können, die sich ergeben.</span><span class="sxs-lookup"><span data-stu-id="95a46-149">When possible, new options should be normalized so they can be applied to new codecs that emerge.</span></span>



| <span data-ttu-id="95a46-150">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="95a46-150">Property Name</span></span>      | <span data-ttu-id="95a46-151">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="95a46-151">VARTYPE</span></span>  | <span data-ttu-id="95a46-152">Wert</span><span class="sxs-lookup"><span data-stu-id="95a46-152">Value</span></span>                                                                     | <span data-ttu-id="95a46-153">Anwendbare Codecs</span><span class="sxs-lookup"><span data-stu-id="95a46-153">Applicable Codecs</span></span> |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="95a46-154">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="95a46-154">ImageQuality</span></span>       | <span data-ttu-id="95a46-155">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="95a46-155">VT\_R4</span></span>   | <span data-ttu-id="95a46-156">0-1.0</span><span class="sxs-lookup"><span data-stu-id="95a46-156">0-1.0</span></span>                                                                     | <span data-ttu-id="95a46-157">JPEG, HDPhoto</span><span class="sxs-lookup"><span data-stu-id="95a46-157">JPEG, HDPhoto</span></span>     |
| <span data-ttu-id="95a46-158">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="95a46-158">CompressionQuality</span></span> | <span data-ttu-id="95a46-159">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="95a46-159">VT\_R4</span></span>   | <span data-ttu-id="95a46-160">0-1.0</span><span class="sxs-lookup"><span data-stu-id="95a46-160">0-1.0</span></span>                                                                     | <span data-ttu-id="95a46-161">TIFF</span><span class="sxs-lookup"><span data-stu-id="95a46-161">TIFF</span></span>              |
| <span data-ttu-id="95a46-162">Lossless</span><span class="sxs-lookup"><span data-stu-id="95a46-162">Lossless</span></span>           | <span data-ttu-id="95a46-163">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="95a46-163">VT\_BOOL</span></span> | <span data-ttu-id="95a46-164">**true**, **false**</span><span class="sxs-lookup"><span data-stu-id="95a46-164">**TRUE**, **FALSE**</span></span>                                                       | <span data-ttu-id="95a46-165">HDPhoto</span><span class="sxs-lookup"><span data-stu-id="95a46-165">HDPhoto</span></span>           |
| <span data-ttu-id="95a46-166">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="95a46-166">BitmapTransform</span></span>    | <span data-ttu-id="95a46-167">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="95a46-167">VT\_UI1</span></span>  | [<span data-ttu-id="95a46-168">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="95a46-168">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="95a46-169">JPEG</span><span class="sxs-lookup"><span data-stu-id="95a46-169">JPEG</span></span>              |



 

<span data-ttu-id="95a46-170">Imagequalty von 0,0 bedeutet, dass die niedrigste mögliche Treue Gabe und 1,0 die höchste Genauigkeit bedeuten. Dies kann je nach Codec auch Verluste bedeuten.</span><span class="sxs-lookup"><span data-stu-id="95a46-170">ImageQualty of 0.0 means the lowest possible fidelity rendition and 1.0 means the highest fidelity, which may also imply lossless depending on the codec.</span></span>

<span data-ttu-id="95a46-171">CompressionQuality von 0,0 bedeutet das am wenigsten effiziente Komprimierungs Schema, das in der Regel eine schnelle Codierung, aber eine größere Ausgabe ergibt.</span><span class="sxs-lookup"><span data-stu-id="95a46-171">CompressionQuality of 0.0 means the least efficient compression scheme available, typically resulting in a fast encode but larger output.</span></span> <span data-ttu-id="95a46-172">Der Wert 1,0 ist das effizienteste verfügbare Schema, das in der Regel mehr Zeit in Anspruch nimmt, um eine geringere Ausgabe zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="95a46-172">A value of 1.0 means the most efficient scheme available, typically taking more time to encode but producing smaller output.</span></span> <span data-ttu-id="95a46-173">Abhängig von den Funktionen des Codecs kann dieser Bereich einem diskreten Satz verfügbarer Komprimierungs Methoden zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="95a46-173">Depending on the capabilities of the codec, this range may be mapped onto a discrete set of available compression methods.</span></span>

<span data-ttu-id="95a46-174">Verlust lose bedeutet, dass der Codec das Image als verlustfreie Methode ohne Bild Datenverlust codiert.</span><span class="sxs-lookup"><span data-stu-id="95a46-174">Lossless means that the codec encodes the image as lossless with no image data loss.</span></span> <span data-ttu-id="95a46-175">Wenn Lossless aktiviert ist, wird ImageQuality ignoriert.</span><span class="sxs-lookup"><span data-stu-id="95a46-175">If Lossless is enabled, ImageQuality is ignored.</span></span>

<span data-ttu-id="95a46-176">Zusätzlich zu den oben genannten generischen Codierungsoptionen unterstützen mit WIC bereitgestellte Codecs die folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="95a46-176">In addition to the above generic encoder options, codecs supplied with WIC support the following options.</span></span> <span data-ttu-id="95a46-177">Wenn ein Codec eine Option unterstützen muss, die mit der Verwendung in den angegebenen Codecs konsistent ist, wird es empfohlen, dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="95a46-177">If a codec has a need to support an option that is consistent with the usage in these supplied codecs, it is encouraged to do so.</span></span>



| <span data-ttu-id="95a46-178">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="95a46-178">Property Name</span></span>           | <span data-ttu-id="95a46-179">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="95a46-179">VARTYPE</span></span>           | <span data-ttu-id="95a46-180">Wert</span><span class="sxs-lookup"><span data-stu-id="95a46-180">Value</span></span>                                                                             | <span data-ttu-id="95a46-181">Anwendbare Codecs</span><span class="sxs-lookup"><span data-stu-id="95a46-181">Applicable Codecs</span></span> |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="95a46-182">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="95a46-182">InterlaceOption</span></span>         | <span data-ttu-id="95a46-183">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="95a46-183">VT\_BOOL</span></span>          | <span data-ttu-id="95a46-184">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="95a46-184">On/Off</span></span>                                                                            | <span data-ttu-id="95a46-185">PNG</span><span class="sxs-lookup"><span data-stu-id="95a46-185">PNG</span></span>               |
| <span data-ttu-id="95a46-186">FilterOption</span><span class="sxs-lookup"><span data-stu-id="95a46-186">FilterOption</span></span>            | <span data-ttu-id="95a46-187">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="95a46-187">VT\_UI1</span></span>           | [<span data-ttu-id="95a46-188">**Wicpngfilteroption**</span><span class="sxs-lookup"><span data-stu-id="95a46-188">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | <span data-ttu-id="95a46-189">PNG</span><span class="sxs-lookup"><span data-stu-id="95a46-189">PNG</span></span>               |
| <span data-ttu-id="95a46-190">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="95a46-190">TiffCompressionMethod</span></span>   | <span data-ttu-id="95a46-191">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="95a46-191">VT\_UI1</span></span>           | [<span data-ttu-id="95a46-192">**Wictiffcompressionoption**</span><span class="sxs-lookup"><span data-stu-id="95a46-192">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | <span data-ttu-id="95a46-193">TIFF</span><span class="sxs-lookup"><span data-stu-id="95a46-193">TIFF</span></span>              |
| <span data-ttu-id="95a46-194">Luminance</span><span class="sxs-lookup"><span data-stu-id="95a46-194">Luminance</span></span>               | <span data-ttu-id="95a46-195">VT \_ UI4/VT- \_ Array</span><span class="sxs-lookup"><span data-stu-id="95a46-195">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="95a46-196">64 Einträge (DCT)</span><span class="sxs-lookup"><span data-stu-id="95a46-196">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="95a46-197">JPEG</span><span class="sxs-lookup"><span data-stu-id="95a46-197">JPEG</span></span>              |
| <span data-ttu-id="95a46-198">Chrominance</span><span class="sxs-lookup"><span data-stu-id="95a46-198">Chrominance</span></span>             | <span data-ttu-id="95a46-199">VT \_ UI4/VT- \_ Array</span><span class="sxs-lookup"><span data-stu-id="95a46-199">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="95a46-200">64 Einträge (DCT)</span><span class="sxs-lookup"><span data-stu-id="95a46-200">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="95a46-201">JPEG</span><span class="sxs-lookup"><span data-stu-id="95a46-201">JPEG</span></span>              |
| <span data-ttu-id="95a46-202">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="95a46-202">JpegYCrCbSubsampling</span></span>    | <span data-ttu-id="95a46-203">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="95a46-203">VT\_UI1</span></span>           | [<span data-ttu-id="95a46-204">**Wicjppfgycrcbsubsamplingoption**</span><span class="sxs-lookup"><span data-stu-id="95a46-204">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | <span data-ttu-id="95a46-205">JPEG</span><span class="sxs-lookup"><span data-stu-id="95a46-205">JPEG</span></span>              |
| <span data-ttu-id="95a46-206">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="95a46-206">SuppressApp0</span></span>            | <span data-ttu-id="95a46-207">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="95a46-207">VT\_BOOL</span></span>          |                                                                                   | <span data-ttu-id="95a46-208">JPEG</span><span class="sxs-lookup"><span data-stu-id="95a46-208">JPEG</span></span>              |
| <span data-ttu-id="95a46-209">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="95a46-209">EnableV5Header32bppBGRA</span></span> | <span data-ttu-id="95a46-210">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="95a46-210">VT\_BOOL</span></span>          | <span data-ttu-id="95a46-211">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="95a46-211">On/Off</span></span>                                                                            | <span data-ttu-id="95a46-212">BMP</span><span class="sxs-lookup"><span data-stu-id="95a46-212">BMP</span></span>               |



 

<span data-ttu-id="95a46-213">Verwenden Sie **VT \_ empty** , um anzugeben, dass nicht als Standard **\* \* festgelegt** ist.</span><span class="sxs-lookup"><span data-stu-id="95a46-213">Use **VT\_EMPTY** to indicate **\*not set\*** as the default.</span></span> <span data-ttu-id="95a46-214">Wenn zusätzliche Eigenschaften festgelegt, aber nicht unterstützt werden, sollte der Encoder diese ignorieren. Dadurch können Anwendungen weniger Logik codieren, wenn Sie eine Funktion benötigen, die möglicherweise vorhanden ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="95a46-214">If additional properties are set but not supported, the encoder should ignore them; this allows applications to code less logic if they want a capability that may or may not be present.</span></span>

## <a name="encoder-options-examples"></a><span data-ttu-id="95a46-215">Beispiele für Codierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="95a46-215">Encoder Options Examples</span></span>

<span data-ttu-id="95a46-216">Im obigen [Beispiel](#tiff-encoding-example) für die TIFF-Codierung wird eine bestimmte Encoder-Option festgelegt.</span><span class="sxs-lookup"><span data-stu-id="95a46-216">In the [TIFF Encoding Example](#tiff-encoding-example) above, a specific encoder option is set.</span></span> <span data-ttu-id="95a46-217">Der *pstrinname* -Member der PROPBAG2-Struktur wird auf den entsprechenden Eigenschaftsnamen festgelegt, und der Variant-Wert wird auf den entsprechenden VarType und den gewünschten Wert festgelegt – in diesem Fall ein Member der [**wictiffcompressionoption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="95a46-217">The *pstrName* member of the PROPBAG2 structure is set to the appropriate property name, and the VARIANT is set to the corresponding VARTYPE and the desired value—in this case, a member of the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) enumeration.</span></span>


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



<span data-ttu-id="95a46-218">Um die standardmäßigen Codierungsoptionen zu verwenden, initialisieren Sie einfach den BitmapFrame mit dem Eigenschaften Behälter, der beim Erstellen des Frames zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="95a46-218">To use the default encoder options, simply initialize the bitmap frame with the property bag returned when the frame was created.</span></span>


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



<span data-ttu-id="95a46-219">Es ist auch möglich, den Eigenschaften Behälter zu entfernen, wenn keine Codierungsoptionen berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="95a46-219">It is also possible to eliminate the property bag when no encoder options are being considered.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="95a46-220">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95a46-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="95a46-221">**Licher**</span><span class="sxs-lookup"><span data-stu-id="95a46-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="95a46-222">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="95a46-222">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="95a46-223">Decodierung: Übersicht</span><span class="sxs-lookup"><span data-stu-id="95a46-223">Decoding Overview</span></span>](-wic-creating-decoder.md)
</dt> <dt>

<span data-ttu-id="95a46-224">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="95a46-224">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="95a46-225">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="95a46-225">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
