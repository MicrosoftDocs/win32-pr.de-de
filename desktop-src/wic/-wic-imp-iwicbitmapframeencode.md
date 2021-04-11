---
description: Implementieren von iwicbitmapframecocode
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: Implementieren von iwicbitmapframecocode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217384"
---
# <a name="implementing-iwicbitmapframeencode"></a><span data-ttu-id="68efe-103">Implementieren von iwicbitmapframecocode</span><span class="sxs-lookup"><span data-stu-id="68efe-103">Implementing IWICBitmapFrameEncode</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="68efe-104">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="68efe-104">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="68efe-105">[**Iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) ist das Gegenstück zur [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="68efe-105">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the encoder’s counterpart to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span> <span data-ttu-id="68efe-106">Sie können diese Schnittstelle in der Codierungs Klasse auf Frame-Ebene implementieren, bei der es sich um die Klasse handelt, die die tatsächliche Codierung der Bildbits für jeden Frame durchführt.</span><span class="sxs-lookup"><span data-stu-id="68efe-106">You can implement this interface on your frame-level encoding class, which is the class that does the actual encoding of the image bits for each frame.</span></span>


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [<span data-ttu-id="68efe-107">Initialisieren</span><span class="sxs-lookup"><span data-stu-id="68efe-107">Initialize</span></span>](#initialize)
-   [<span data-ttu-id="68efe-108">SetSize und SetResolution</span><span class="sxs-lookup"><span data-stu-id="68efe-108">SetSize and SetResolution</span></span>](#setsize-and-setresolution)
-   [<span data-ttu-id="68efe-109">SetPixelFormat</span><span class="sxs-lookup"><span data-stu-id="68efe-109">SetPixelFormat</span></span>](#setpixelformat)
-   [<span data-ttu-id="68efe-110">Setcolorkontexte</span><span class="sxs-lookup"><span data-stu-id="68efe-110">SetColorContexts</span></span>](#setcolorcontexts)
-   [<span data-ttu-id="68efe-111">GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="68efe-111">GetMetadataQueryWriter</span></span>](#getmetadataquerywriter)
-   [<span data-ttu-id="68efe-112">Setminiatur</span><span class="sxs-lookup"><span data-stu-id="68efe-112">SetThumbnail</span></span>](#setthumbnail)
-   [<span data-ttu-id="68efe-113">"WritePixels"</span><span class="sxs-lookup"><span data-stu-id="68efe-113">WritePixels</span></span>](#writepixels)
-   [<span data-ttu-id="68efe-114">Schreibgeschützte Datenquelle</span><span class="sxs-lookup"><span data-stu-id="68efe-114">WriteSource</span></span>](#writesource)
-   [<span data-ttu-id="68efe-115">Commit</span><span class="sxs-lookup"><span data-stu-id="68efe-115">Commit</span></span>](#commit)
-   [<span data-ttu-id="68efe-116">SetPalette</span><span class="sxs-lookup"><span data-stu-id="68efe-116">SetPalette</span></span>](#setpalette)

### <a name="initialize"></a><span data-ttu-id="68efe-117">Initialisieren</span><span class="sxs-lookup"><span data-stu-id="68efe-117">Initialize</span></span>

<span data-ttu-id="68efe-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) ist die erste Methode, die für ein [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Objekt aufgerufen wird, nachdem es instanziiert wurde.</span><span class="sxs-lookup"><span data-stu-id="68efe-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) is the first method invoked on an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object after it has been instantiated.</span></span> <span data-ttu-id="68efe-119">Diese Methode verfügt über einen Parameter, der möglicherweise auf **null** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="68efe-119">This method has one parameter, which may be set to **NULL**.</span></span> <span data-ttu-id="68efe-120">Dieser Parameter stellt die Codierungsoptionen dar und ist dieselbe [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Instanz, die Sie in der Methode " [**kreatenewframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) " für den Decoder auf Container-Ebene erstellt und an den Aufrufer im pIEncoderOptions-Parameter dieser Methode zurückgegeben haben.</span><span class="sxs-lookup"><span data-stu-id="68efe-120">This parameter represents the encoder options, and is the same [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) instance that you created in the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method on the container-level decoder, and passed back to the caller in the pIEncoderOptions parameter of that method.</span></span> <span data-ttu-id="68efe-121">Zu diesem Zeitpunkt haben Sie die IPropertyBag2-Struktur mit Eigenschaften aufgefüllt, die die Codierungsoptionen darstellen, die von Ihrem Encoder auf Frame-Ebene unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="68efe-121">At that time, you populated the IPropertyBag2 struct with properties that represent the encoding options supported by your frame-level encoder.</span></span> <span data-ttu-id="68efe-122">Der Aufrufer hat nun Werte für diese Eigenschaften bereitgestellt, um bestimmte Codierungs Optionsparameter anzugeben, und übergibt das gleiche Objekt an Sie zurück, um das **IWICBitmapFrameEncode** -Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="68efe-122">The caller has now provided values for those properties to indicate certain encoding option parameters, and is passing the same object back to you to initialize the **IWICBitmapFrameEncode** object.</span></span> <span data-ttu-id="68efe-123">Beim Codieren der Bildbits sollten Sie die angegebenen Optionen anwenden.</span><span class="sxs-lookup"><span data-stu-id="68efe-123">You should apply the specified options when encoding the image bits.</span></span>

### <a name="setsize-and-setresolution"></a><span data-ttu-id="68efe-124">SetSize und SetResolution</span><span class="sxs-lookup"><span data-stu-id="68efe-124">SetSize and SetResolution</span></span>

<span data-ttu-id="68efe-125">[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) und [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) sind selbsterklärend.</span><span class="sxs-lookup"><span data-stu-id="68efe-125">[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) and [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) are self-explanatory.</span></span> <span data-ttu-id="68efe-126">Der Aufrufer verwendet diese Methoden, um die Größe und Auflösung für das codierte Bild anzugeben.</span><span class="sxs-lookup"><span data-stu-id="68efe-126">The caller uses these methods to specify the size and resolution for the encoded image.</span></span>

### <a name="setpixelformat"></a><span data-ttu-id="68efe-127">SetPixelFormat</span><span class="sxs-lookup"><span data-stu-id="68efe-127">SetPixelFormat</span></span>

<span data-ttu-id="68efe-128">[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) wird verwendet, um ein Pixel Format anzufordern, in dem das Bild codiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="68efe-128">[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) is used to request a pixel format in which to encode the image.</span></span> <span data-ttu-id="68efe-129">Wenn das angeforderte Pixel Format nicht unterstützt wird, sollten Sie die GUID des nächstgelegenen Pixel Formats zurückgeben, das in *pPixelFormat* unterstützt wird. Hierbei handelt es sich um einen in/out-Parameter.</span><span class="sxs-lookup"><span data-stu-id="68efe-129">If the requested pixel format is not supported, you should return the GUID of the closest pixel format that is supported in *pPixelFormat*, which is an in/out parameter.</span></span>

### <a name="setcolorcontexts"></a><span data-ttu-id="68efe-130">Setcolorkontexte</span><span class="sxs-lookup"><span data-stu-id="68efe-130">SetColorContexts</span></span>

<span data-ttu-id="68efe-131">[**Setcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) dient zum Angeben eines oder mehrerer gültiger Farb Kontexte (auch als Farbprofile bezeichnet) für dieses Bild.</span><span class="sxs-lookup"><span data-stu-id="68efe-131">[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) is used to specify one or more valid color contexts (also known as color profiles) for this image.</span></span> <span data-ttu-id="68efe-132">Es ist wichtig, die Farb Kontexte anzugeben, sodass eine Anwendung, die das Image zu einem späteren Zeitpunkt decodiert, vom Quell Farbprofil in das Ziel Profil des Geräts konvertiert werden kann, das zum Anzeigen oder Drucken des Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="68efe-132">It’s important to specify the color contexts, so an application that decodes the image at a later time can convert from the source color profile to the destination profile of the device being used to display or print the image.</span></span> <span data-ttu-id="68efe-133">Ohne ein Farbprofil ist es nicht möglich, konsistente Farben auf verschiedenen Geräten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="68efe-133">Without a color profile, it is not possible to get consistent colors across different devices.</span></span> <span data-ttu-id="68efe-134">Dies kann für Endbenutzer frustrierend sein, wenn Ihre Fotos auf verschiedenen Monitoren anders aussehen, und Sie können die Druckvorgänge nicht so erhalten, wie Sie auf dem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="68efe-134">This can be frustrating for end users when their photos look different on different monitors, and they can’t get the prints to match what they see on screen.</span></span>

### <a name="getmetadataquerywriter"></a><span data-ttu-id="68efe-135">GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="68efe-135">GetMetadataQueryWriter</span></span>

<span data-ttu-id="68efe-136">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) gibt eine [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) zurück, die eine Anwendung verwenden kann, um bestimmte Metadateneigenschaften in einem Metadatenblock im Bild Rahmen einzufügen oder zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="68efe-136">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) returns an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) that an application can use to insert or edit specific metadata properties in a metadata block on the image frame.</span></span>

<span data-ttu-id="68efe-137">Sie können eine [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) aus [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) auf verschiedene Weise instanziieren.</span><span class="sxs-lookup"><span data-stu-id="68efe-137">You can instantiate an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) from the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) in several ways.</span></span> <span data-ttu-id="68efe-138">Sie können Sie entweder von Ihrer [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)aus erstellen, und zwar auf dieselbe Weise wie [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) von einem [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in der [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) -Methode der [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Schnittstelle aus erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="68efe-138">You can either create it from your [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), the same way [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) was created from an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span>


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



<span data-ttu-id="68efe-139">Sie können Sie auch aus einem vorhandenen [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)erstellen, z. b. mit dem, der mit der vorherigen Methode abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="68efe-139">You can also create it from an existing [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), such as the one obtained using the previous method.</span></span>


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



<span data-ttu-id="68efe-140">Mit dem *pguidVendor* -Parameter können Sie einen bestimmten Anbieter angeben, den der Abfrage Schreiber beim Instanziieren eines metadatenwriters verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="68efe-140">The *pguidVendor* parameter allows you to specify a particular vendor for the query writer to use when instantiating a metadata writer.</span></span> <span data-ttu-id="68efe-141">Wenn Sie z. b. eigene metadatenwriter bereitstellen, möchten Sie möglicherweise Ihre eigene GUID für den Anbieter angeben.</span><span class="sxs-lookup"><span data-stu-id="68efe-141">For example, if you provide your own metadata writers, you may want to specify your own vendor GUID.</span></span> <span data-ttu-id="68efe-142">Sie können **null** an diesen Parameter übergeben, wenn Sie nicht über eine bevorzugte Einstellung verfügen.</span><span class="sxs-lookup"><span data-stu-id="68efe-142">You can pass **NULL** to this parameter if you don’t have a preference.</span></span>

### <a name="setthumbnail"></a><span data-ttu-id="68efe-143">Setminiatur</span><span class="sxs-lookup"><span data-stu-id="68efe-143">SetThumbnail</span></span>

<span data-ttu-id="68efe-144">[**Setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) wird verwendet, um eine Miniaturansicht bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="68efe-144">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is used to provide a thumbnail.</span></span> <span data-ttu-id="68efe-145">Alle Bilder sollten eine Miniaturansicht entweder global, in jedem Frame oder beides bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="68efe-145">All images should provide a thumbnail either globally, on each frame, or both.</span></span> <span data-ttu-id="68efe-146">Die Methoden **getminiatur** und **setminiatur** sind auf Container Ebene optional, aber wenn ein Codec wincodec \_ Err \_ codecnominiatur aus der [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) -Methode zurückgibt, ruft die Windows Imaging Component (WIC) die [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) -Methode für Frame 0 auf.</span><span class="sxs-lookup"><span data-stu-id="68efe-146">The **GetThumbnail** and **SetThumbnail** methods are optional at the container-level but, if a codec returns WINCODEC\_ERR\_CODECNOTHUMBNAIL from the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method, Windows Imaging Component (WIC) will invoke the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method for Frame 0.</span></span> <span data-ttu-id="68efe-147">Wenn an keinem Ort eine Miniaturansicht gefunden wird, muss WIC das vollständige Image decodieren und es auf die Miniatur Ansichts Größe skalieren, was bei größeren Images zu einer hohen Leistungs Einbuße kommen könnte.</span><span class="sxs-lookup"><span data-stu-id="68efe-147">If no thumbnail is found in either place, WIC must decode the full image and scale it to thumbnail size, which could incur a large performance penalty for larger images.</span></span>

<span data-ttu-id="68efe-148">Die Miniaturansicht sollte eine Größe und Auflösung aufweisen, die Sie schnell decodieren und anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="68efe-148">The thumbnail should be of a size and resolution that makes it quick to decode and display.</span></span> <span data-ttu-id="68efe-149">Aus diesem Grund sind Miniaturansichten am häufigsten JPEG-Bilder.</span><span class="sxs-lookup"><span data-stu-id="68efe-149">For this reason, thumbnails are most commonly JPEG images.</span></span> <span data-ttu-id="68efe-150">Beachten Sie Folgendes: Wenn Sie JPEG für Ihre Miniaturansichten verwenden, müssen Sie keinen JPEG-Encoder schreiben, um Sie zu codieren, oder einen JPEG-Decoder zum Decodieren.</span><span class="sxs-lookup"><span data-stu-id="68efe-150">Note that, if you use JPEG for your thumbnails, you don’t have to write a JPEG encoder to encode them, or a JPEG decoder to decode them.</span></span> <span data-ttu-id="68efe-151">Sie sollten immer an den JPEG-CODEC delegieren, der in der WIC-Plattform zum Codieren und Decodieren von Miniaturansichten enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="68efe-151">You should always delegate to the JPEG codec that ships with the WIC platform for encoding and decoding thumbnails.</span></span>

### <a name="writepixels"></a><span data-ttu-id="68efe-152">"WritePixels"</span><span class="sxs-lookup"><span data-stu-id="68efe-152">WritePixels</span></span>

<span data-ttu-id="68efe-153">" [**Write Pixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) " ist die Methode, mit der Scan Zeilen aus einer Bitmap im Arbeitsspeicher für die Codierung übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="68efe-153">[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) is the method used to pass in scan lines from a bitmap in memory for encoding.</span></span> <span data-ttu-id="68efe-154">Die-Methode wird wiederholt aufgerufen, bis alle Überprüfungs Zeilen übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="68efe-154">The method will be called repeatedly until all of the scan lines have been passed in.</span></span> <span data-ttu-id="68efe-155">Der *LineCount* -Parameter gibt an, wie viele Scan Zeilen in diesem-Befehl geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="68efe-155">The *lineCount* parameter indicates how many scan lines are to be written in this call.</span></span> <span data-ttu-id="68efe-156">Der *cbStride* -Parameter gibt die Anzahl der Bytes pro Scan Zeile an.</span><span class="sxs-lookup"><span data-stu-id="68efe-156">The *cbStride* parameter indicates the number of bytes per scan line.</span></span> <span data-ttu-id="68efe-157">*cbBufferSize* gibt die Größe des Puffers an, der im pbPixels-Parameter übergeben wird, der die eigentlichen zu codierenden Bildbits enthält.</span><span class="sxs-lookup"><span data-stu-id="68efe-157">*cbBufferSize* indicates the size of the buffer passed in the pbPixels parameter, which contains the actual image bits to be encoded.</span></span> <span data-ttu-id="68efe-158">Wenn die kombinierte Höhe der Scan Zeilen von kumulativen Aufrufen größer als die in der [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) -Methode angegebene Höhe ist, wird wincodec \_ Err \_ toomanyscanlines zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68efe-158">If the combined height of the scan lines from cumulative calls is greater than the height specified in [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="68efe-159">Wenn [**wicbitmapcodercacheoption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) den Wert **wicbitmapcodercacheinmemory** hat, sollten die Scan Zeilen im Arbeitsspeicher zwischengespeichert werden, bis alle Überprüfungs Zeilen übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="68efe-159">When the [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) is **WICBitmapEncoderCacheInMemory**, the scan lines should be cached in memory until all scan lines have been passed in.</span></span> <span data-ttu-id="68efe-160">Wenn die Encoder-Cache-Option **wicbitmapcodercachetempfile** ist, sollten die Überprüfungs Zeilen in einer temporären Datei zwischengespeichert werden, die beim Initialisieren des Objekts erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="68efe-160">If the encoder cache option is **WICBitmapEncoderCacheTempFile**, the scan lines should be cached in a temporary file, created when initializing the object.</span></span> <span data-ttu-id="68efe-161">In jedem dieser Fälle sollte das Bild erst codiert werden, wenn der Aufrufer den [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit)aufruft.</span><span class="sxs-lookup"><span data-stu-id="68efe-161">In either of these cases, the image should not be encoded until the caller calls [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).</span></span> <span data-ttu-id="68efe-162">Wenn die Cache Option **wicbitmapcodernocache** ist, sollte der Encoder die Überprüfungs Zeilen nach Möglichkeit codieren, sobald Sie empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="68efe-162">In the case where the cache option is **WICBitmapEncoderNoCache**, the encoder should encode the scan lines as they’re received, if possible.</span></span> <span data-ttu-id="68efe-163">(In manchen Formaten ist dies nicht möglich, und die Scan Zeilen müssen zwischengespeichert werden, bis Commit aufgerufen wird.)</span><span class="sxs-lookup"><span data-stu-id="68efe-163">(In some formats, this is not possible, and the scan lines must be cached until Commit is called.)</span></span>

<span data-ttu-id="68efe-164">Die meisten Rohdaten CODECs implementieren keine [**Beschreib tepixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), da Sie das Ändern der Bildbits in der Rohdatendatei nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="68efe-164">Most raw codecs will not implement [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), because they don’t support altering the image bits in the raw file.</span></span> <span data-ttu-id="68efe-165">Unformatierte Codecs sollten jedoch immer noch " **Write Pixels**" implementieren, denn wenn Metadaten hinzugefügt werden, kann die Größe der Datei erhöht werden, sodass die Datei auf dem Datenträger neu geschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="68efe-165">Raw codecs should still implement **WritePixels**, however, because when metadata is added, it may increase the size of the file, requiring the file to be rewritten on the disk.</span></span> <span data-ttu-id="68efe-166">In diesem Fall müssen die vorhandenen Bildbits kopiert werden können. Dies ist die Methode der Methode " **Write** ".</span><span class="sxs-lookup"><span data-stu-id="68efe-166">In that case, it’s necessary to be able to copy the existing image bits, which is what the **WritePixels** method does.</span></span>

### <a name="writesource"></a><span data-ttu-id="68efe-167">Schreibgeschützte Datenquelle</span><span class="sxs-lookup"><span data-stu-id="68efe-167">WriteSource</span></span>

<span data-ttu-id="68efe-168">" [**Write-ource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) " wird verwendet, um ein [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Objekt zu codieren.</span><span class="sxs-lookup"><span data-stu-id="68efe-168">[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) is used to encode an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span> <span data-ttu-id="68efe-169">Der erste Parameter ist ein Zeiger auf ein **IWICBitmapSource** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="68efe-169">The first parameter is a pointer to an **IWICBitmapSource** object.</span></span> <span data-ttu-id="68efe-170">Der zweite Parameter ist ein WICRect, das den zu codierenden Bereich angibt.</span><span class="sxs-lookup"><span data-stu-id="68efe-170">The second parameter is a WICRect that specifies the region of interest to encode.</span></span> <span data-ttu-id="68efe-171">Diese Methode kann mehrmals nacheinander aufgerufen werden, solange die Breite jedes Rechtecks dieselbe Breite des zu codierenden endgültigen Bilds hat.</span><span class="sxs-lookup"><span data-stu-id="68efe-171">This method may be called multiple times in succession, as long as the width of each rectangle is the same width of the final image to be encoded.</span></span> <span data-ttu-id="68efe-172">Wenn die Breite des Rechtecks, das in den PRC-Parameter übergeben wird, von der in der SetSize-Methode angegebenen Breite abweicht, wird wincodec \_ Err \_ sourcerectdoesnotmatchdimensions zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68efe-172">If the width of the rectangle passed in the prc parameter is different than the width specified in the SetSize method, return WINCODEC\_ERR\_SOURCERECTDOESNOTMATCHDIMENSIONS.</span></span> <span data-ttu-id="68efe-173">Wenn die kombinierte Höhe der Scan Zeilen von kumulativen Aufrufen größer als die in der SetSize-Methode angegebene Höhe ist, wird wincodec \_ Err \_ toomanyscanlines zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68efe-173">If the combined height of the scan lines from cumulative calls is greater than the height specified in SetSize method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="68efe-174">Die Cache Optionen funktionieren mit dieser Methode genauso wie mit der zuvor beschriebenen Methode " [**Write Pixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) ".</span><span class="sxs-lookup"><span data-stu-id="68efe-174">The cache options work the same way with this method as with the [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) method described previously.</span></span>

### <a name="commit"></a><span data-ttu-id="68efe-175">Commit</span><span class="sxs-lookup"><span data-stu-id="68efe-175">Commit</span></span>

<span data-ttu-id="68efe-176">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) ist die Methode, die die codierten Bildbits in den Dateistream serialisiert und alle metadatenwriter für den Frame durchläuft, der Sie anfordert, ihre Metadaten in den Stream zu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="68efe-176">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) is the method that serializes the encoded image bits to the file stream, and iterates through all the metadata writers for the frame requesting them to serialize their metadata to the stream.</span></span> <span data-ttu-id="68efe-177">Wenn die Encoder-Cache-Option "wicbitmapcodercacheinmemory" oder "wicbitmapcodercachetempfile" ist, ist diese Methode auch für das Codieren des Bilds zuständig. wenn die Cache Option "wicbitmapcodercachetempfile" ist, sollte die **Commit** -Methode auch die temporäre Datei löschen, die zum</span><span class="sxs-lookup"><span data-stu-id="68efe-177">In the case where the encoder cache option is WICBitmapEncoderCacheInMemory or WICBitmapEncoderCacheTempFile, this method is also responsible for encoding the image, and when the cache option is WICBitmapEncoderCacheTempFile, the **Commit** method should also delete the temporary file used to cache the image data before encoding.</span></span>

<span data-ttu-id="68efe-178">Diese Methode wird immer aufgerufen, nachdem alle Scan Zeilen oder Rechtecke, die das Bild bilden, mithilfe der [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) -oder der [**Write-ource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) -Methode übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="68efe-178">This method is always invoked after all the scan lines or rectangles that make up the image have been passed in using either the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) or [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) method.</span></span> <span data-ttu-id="68efe-179">Die Größe des abschließenden Rechtecks, das durch die akkumulierten Aufrufe von "Write-Pixels" oder "Write-ource" besteht, muss dieselbe Größe aufweisen wie in der SetSize-Methode.</span><span class="sxs-lookup"><span data-stu-id="68efe-179">The size of the final rectangle that is composed through the accumulated calls to WritePixels or WriteSource must be the same size as was specified in the SetSize method.</span></span> <span data-ttu-id="68efe-180">Wenn die Größe nicht der erwarteten Größe entspricht, sollte diese Methode wincodecerror \_ unexpectedsize zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="68efe-180">If the size does not match the expected size, this method should return WINCODECERROR\_UNEXPECTEDSIZE.</span></span>

<span data-ttu-id="68efe-181">Um die metadatenwriter zu durchlaufen und jeden metadatenwriter anzuweisen, seine Metadaten zu serialisieren, rufen Sie den Stream auf, rufen Sie GetWriterByIndex auf, um die Writer für jeden Block zu durchlaufen, und rufen Sie IWICPersistStream. Save für jeden metadatenwriter auf.</span><span class="sxs-lookup"><span data-stu-id="68efe-181">To iterate through the metadata writers and tell each metadata writer to serialize its metadata go the stream, invoke GetWriterByIndex to iterate through the writers for each block, and invoke IWICPersistStream.Save on each metadata writer.</span></span>


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a><span data-ttu-id="68efe-182">SetPalette</span><span class="sxs-lookup"><span data-stu-id="68efe-182">SetPalette</span></span>

<span data-ttu-id="68efe-183">Nur Codecs mit indizierten Formaten müssen die [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) -Methode implementieren.</span><span class="sxs-lookup"><span data-stu-id="68efe-183">Only codecs that have indexed formats need to implement the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) method.</span></span> <span data-ttu-id="68efe-184">Wenn ein Bild ein indiziertes Format verwendet, verwenden Sie diese Methode, um die Palette der Farben anzugeben, die im Bild verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68efe-184">If an image uses an indexed format, use this method to specify the palette of colors used in the image.</span></span> <span data-ttu-id="68efe-185">Wenn Ihr CODEC kein indiziertes Format hat, geben Sie wincodec \_ Err \_ palettenicht aus dieser Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="68efe-185">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE from this method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68efe-186">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="68efe-186">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="68efe-187">**Licher**</span><span class="sxs-lookup"><span data-stu-id="68efe-187">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="68efe-188">Implementieren von IWICBitmapCodecProgressNotification (Encoder)</span><span class="sxs-lookup"><span data-stu-id="68efe-188">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[<span data-ttu-id="68efe-189">Implementieren von IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="68efe-189">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="68efe-190">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="68efe-190">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="68efe-191">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="68efe-191">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
