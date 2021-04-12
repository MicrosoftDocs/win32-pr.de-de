---
description: Implementieren von IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Implementieren von IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0809e1e56fe3c05c8803bb70106c4a24a466eafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347188"
---
# <a name="implementing-iwicbitmapsourcetransform"></a><span data-ttu-id="9ea74-103">Implementieren von IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="9ea74-103">Implementing IWICBitmapSourceTransform</span></span>

## <a name="iwicbitmapsourcetransform"></a><span data-ttu-id="9ea74-104">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="9ea74-104">IWICBitmapSourceTransform</span></span>

<span data-ttu-id="9ea74-105">Obwohl es optional ist, wird dringend empfohlen, dass jeder Decoder diese Schnittstelle in der Decodierung der Frame-Ebene implementiert, da er wichtige Leistungsvorteile bieten kann.</span><span class="sxs-lookup"><span data-stu-id="9ea74-105">Though optional, we highly recommend that every decoder implement this interface on your frame-level decoding class, because it can provide major performance benefits.</span></span> <span data-ttu-id="9ea74-106">Wenn eine Anwendung einen bestimmten Bereich von Interesse, Größe, Ausrichtung oder Pixel Format anfordert, anstatt nur das gesamte Bild bei vollständiger Auflösung zu decodieren und dann die angeforderten Transformationen anzuwenden, ruft Windows Imaging Component (WIC) [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für diese Schnittstelle für das [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="9ea74-106">When an application requests a specific region of interest, size, orientation, or pixel format, instead of just decoding the whole image at full resolution and then applying the requested transforms, Windows Imaging Component (WIC) calls [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for this interface on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span> <span data-ttu-id="9ea74-107">Wenn der Frame-Decoder dies unterstützt, ruft WIC die entsprechenden Methoden oder Methoden auf, um zu bestimmen, ob der Frame-Decoder die angeforderte Transformation durchführen kann, oder um die nächstgelegene Größe oder das Pixel Format festzulegen, die der Decoder für die angeforderte</span><span class="sxs-lookup"><span data-stu-id="9ea74-107">If the frame decoder supports it, WIC calls the appropriate method or methods to determine whether the frame decoder can perform the requested transform or determine the closest size or pixel format the decoder can provide to the one requested.</span></span> <span data-ttu-id="9ea74-108">Wenn der Decoder die angeforderte Transformation oder Transformationen ausführen kann, ruft WIC [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) mit den entsprechenden Parametern auf.</span><span class="sxs-lookup"><span data-stu-id="9ea74-108">If the decoder can perform the requested transform or transforms, WIC invokes [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the appropriate parameters.</span></span> <span data-ttu-id="9ea74-109">Wenn der Decoder einige, jedoch nicht alle angeforderten Transformationen ausführen kann, WIC fordert den Decoder dazu auf, diese auszuführen, und verwendet die WIC Transform-Objekte ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)und [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)), um die verbleibenden Transformationen auszuführen, die vom Frame Decoder beim Ergebnis des **copypixel** -Aufrufes nicht ausgeführt werden konnten.</span><span class="sxs-lookup"><span data-stu-id="9ea74-109">If the decoder can perform some, but not all of the requested transforms, WIC asks the decoder to perform those that it can, and uses the WIC transform objects ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) to perform the remaining transforms that could not be performed by the frame decoder on the result of the **CopyPixels** call.</span></span> <span data-ttu-id="9ea74-110">Wenn der Decoder [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)nicht unterstützt, muss WIC die Transform-Objekte verwenden, um alle Transformationen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9ea74-110">If the decoder doesn’t support [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), then WIC must use the transform objects to perform all of the transforms.</span></span> <span data-ttu-id="9ea74-111">Es ist in der Regel viel effizienter, wenn der Decoder während des Decodierungs Prozesses Transformationen ausführt, als das gesamte Bild zu decodieren und dann die Transformationen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9ea74-111">It’s usually much more efficient for the decoder to perform transforms during the decoding process than it is to decode the entire image and then perform the transforms.</span></span> <span data-ttu-id="9ea74-112">Dies gilt insbesondere für Vorgänge wie die Skalierung auf eine wesentlich geringere Größe oder Pixel Formatkonvertierungen.</span><span class="sxs-lookup"><span data-stu-id="9ea74-112">This is especially true for operations such as scaling to a much smaller size or pixel format conversions.</span></span>


```C++
interface IWICBitmapSourceTransform : IUnknown
{
   // Required methods
   HRESULT DoesSupportTransform ( WICTransformOptions dstTransform,
              BOOL *pfIsSupported);
   HRESULT CopyPixels ( WICRect *prcSrc, 
      UINT uiWidth, 
      UINT uiHeight,
      WICPixelFormatGUID * pguidDstFormat,
      WICBitmapTransformOptions dstTransform, 
      UINT nStride, 
      UINT cbBufferSize, 
      BYTE *pbBuffer );

   // Optional methods
   HRESULT GetClosestSize ( UINT *puiWidth,
              UINT *puiHeight);
   HRESULT GetClosestPixelFormat ( WICPixelFormatGUID *pguidDstFormat);
}
```



-   [<span data-ttu-id="9ea74-113">DoesSupportTransform</span><span class="sxs-lookup"><span data-stu-id="9ea74-113">DoesSupportTransform</span></span>](#doessupporttransform)
-   [<span data-ttu-id="9ea74-114">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="9ea74-114">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="9ea74-115">GetClosestSize</span><span class="sxs-lookup"><span data-stu-id="9ea74-115">GetClosestSize</span></span>](#getclosestsize)
-   [<span data-ttu-id="9ea74-116">GetClosestPixelFormat</span><span class="sxs-lookup"><span data-stu-id="9ea74-116">GetClosestPixelFormat</span></span>](#getclosestpixelformat)

### <a name="doessupporttransform"></a><span data-ttu-id="9ea74-117">DoesSupportTransform</span><span class="sxs-lookup"><span data-stu-id="9ea74-117">DoesSupportTransform</span></span>

<span data-ttu-id="9ea74-118">[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) fragt, ob der Decoder den angeforderten Rotations-oder flippingvorgang unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ea74-118">[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) asks whether the decoder supports the requested rotation or flipping operation.</span></span> <span data-ttu-id="9ea74-119">Die folgenden [**WICBitmapTransformOptions-Optionen**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) sind möglich:</span><span class="sxs-lookup"><span data-stu-id="9ea74-119">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) that may be requested are:</span></span>


```C++
enum WICBitmapTransformOptions
{   
   WICBitmapTransformRotate0,
   WICBitmapTransformRotate90,
   WICBitmapTransformRotate180,
   WICBitmapTransformRotate270,
   WICBitmapTransformFlipHorizontal,
   WICBitmapTransformFlipVertical
}
```



### <a name="copypixels"></a><span data-ttu-id="9ea74-120">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="9ea74-120">CopyPixels</span></span>

<span data-ttu-id="9ea74-121">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) führt die eigentliche Dekodierung der Bildbits aus, z. b. die [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) -Methode in der [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Schnittstelle, aber die [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) -Methode für [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) ist viel leistungsfähiger und kann die Bildverarbeitungsleistung erheblich verbessern.</span><span class="sxs-lookup"><span data-stu-id="9ea74-121">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) performs the actual work of decoding the image bits, such as the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, but the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method on [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) is much more powerful, and can improve image processing performance significantly.</span></span>

<span data-ttu-id="9ea74-122">Wenn mehrere Transformations Vorgänge angefordert werden, hängt das Ergebnis von der Reihenfolge ab, in der die Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9ea74-122">When multiple transform operations are requested, the result is dependent on the order in which the operations are performed.</span></span> <span data-ttu-id="9ea74-123">Um die Vorhersagbarkeit und Konsistenz zwischen Codecs sicherzustellen, ist es wichtig, dass alle Codecs diese Vorgänge in derselben Reihenfolge ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ea74-123">To ensure predictability and consistency across codecs, it’s important that all codecs perform these operations in the same order.</span></span> <span data-ttu-id="9ea74-124">Dies ist die kanonische Reihenfolge zum Durchführen dieser Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="9ea74-124">This is the canonical order for performing these operations.</span></span>

1.  <span data-ttu-id="9ea74-125">Skalieren</span><span class="sxs-lookup"><span data-stu-id="9ea74-125">Scale</span></span>
2.  <span data-ttu-id="9ea74-126">Crop</span><span class="sxs-lookup"><span data-stu-id="9ea74-126">Crop</span></span>
3.  <span data-ttu-id="9ea74-127">Rotate</span><span class="sxs-lookup"><span data-stu-id="9ea74-127">Rotate</span></span>

<span data-ttu-id="9ea74-128">Die Konvertierung von Pixel Formaten kann jederzeit ausgeführt werden, da Sie keine Auswirkungen auf die anderen Transformationen hat.</span><span class="sxs-lookup"><span data-stu-id="9ea74-128">Pixel format conversion can be performed at any time, because it has no effect on the other transforms.</span></span>

<span data-ttu-id="9ea74-129">Der erste Parameter, *prcSrc*, wird verwendet, um den Bereich anzugeben, der für das Abschneiden des Bilds von Interesse ist.</span><span class="sxs-lookup"><span data-stu-id="9ea74-129">The first parameter, *prcSrc*, is used to specify the region of interest for clipping the image.</span></span> <span data-ttu-id="9ea74-130">Da die Skalierung durchgeführt wird, bevor das Abbild nach der Konvention abgeschnitten wird, muss der relevante Bereich nach dem Skalieren des Bilds festgelegt werden, wenn das Bild skaliert und abgeschnitten werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ea74-130">Because scaling is performed before clipping by convention, if the image is to be scaled as well as clipped, the region of interest should be determined after the image has been scaled.</span></span>

<span data-ttu-id="9ea74-131">Der zweite und dritte Parameter geben die Größe an, in der das Bild skaliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ea74-131">The second and third parameters indicate the size to which to scale the image.</span></span>

<span data-ttu-id="9ea74-132">Der *pguidDstFormat* -Parameter gibt das angeforderte Pixel Format für das decodierte Bild an.</span><span class="sxs-lookup"><span data-stu-id="9ea74-132">The *pguidDstFormat* parameter indicates the requested pixel format for the decoded image.</span></span> <span data-ttu-id="9ea74-133">Da WIC bereits [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)aufgerufen hat, sollte dies ein Pixel Format sein, das der Decoder angibt, dass es unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ea74-133">Because WIC has already called [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), this should be a pixel format that the decoder has indicated that it supports.</span></span>

<span data-ttu-id="9ea74-134">Der *dsttransform* -Parameter gibt den angeforderten Drehwinkel an und gibt an, ob das Bild vertikal, horizontal oder beides gekippt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ea74-134">The *dstTransform* parameter indicates the requested rotation angle, and whether to flip the image vertically, horizontally, or both.</span></span> <span data-ttu-id="9ea74-135">Da WIC bereits " [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)" aufgerufen hat, sollte die angeforderte Transformation eine solche Transformation sein, die der Decoder bereits angibt, dass Sie unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ea74-135">Again, because WIC will have already called [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), the requested transform should be one that the decoder has already indicated that it supports.</span></span> <span data-ttu-id="9ea74-136">Beachten Sie, dass die Rotation immer nach dem Skalieren und Abschneiden erfolgen sollte.</span><span class="sxs-lookup"><span data-stu-id="9ea74-136">Remember that rotation should always be performed after scaling and clipping.</span></span>

### <a name="getclosestsize"></a><span data-ttu-id="9ea74-137">GetClosestSize</span><span class="sxs-lookup"><span data-stu-id="9ea74-137">GetClosestSize</span></span>

<span data-ttu-id="9ea74-138">[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) übernimmt zwei in/out-Parameter.</span><span class="sxs-lookup"><span data-stu-id="9ea74-138">[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) takes two in/out parameters.</span></span> <span data-ttu-id="9ea74-139">Der Aufrufer verwendet die Parameter " *puiWidth* " und " *puiHeight* ", um die Größe anzugeben, mit der der Aufrufer das Bild als decodiert eingibt.</span><span class="sxs-lookup"><span data-stu-id="9ea74-139">The caller uses the *puiWidth* and *puiHeight* parameters to specify the size at which that the caller prefers the image to be decoded.</span></span> <span data-ttu-id="9ea74-140">Ein Decoder kann jedoch ein Bild nur in eine Größe decodieren, die ein Vielfaches seiner DCT-Größe ist, und unterschiedliche Bildformate können unterschiedliche DCT-Größen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9ea74-140">However, a decoder can decode an image only to a size that’s a multiple of its DCT size, and different image formats can have different DCT sizes.</span></span> <span data-ttu-id="9ea74-141">Der Decoder sollte auf der Grundlage seiner eigenen DCT-Größe ermitteln, dem am nächsten liegenden Wert der angeforderten Größe und dem Wert für " *puiWidth* " und " *puiHeight* " bei der Rückgabe.</span><span class="sxs-lookup"><span data-stu-id="9ea74-141">The decoder should determine, based on its own DCT size, the closest it can come to the requested size, and set the *puiWidth* and *puiHeight* to those dimensions on return.</span></span> <span data-ttu-id="9ea74-142">Wenn eine größere Größe angefordert wird, der Codec jedoch keine upskalierung unterstützt, sollte das Original zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9ea74-142">If a larger size is requested, but the codec doesn’t support upscaling, the original should be returned.</span></span>

### <a name="getclosestpixelformat"></a><span data-ttu-id="9ea74-143">GetClosestPixelFormat</span><span class="sxs-lookup"><span data-stu-id="9ea74-143">GetClosestPixelFormat</span></span>

<span data-ttu-id="9ea74-144">[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) wird verwendet, um das nächste Pixel Format für das angeforderte Pixel Format festzulegen, das der Decoder ohne Datenverlust bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="9ea74-144">[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) is used to determine the closest pixel format to the requested pixel format that the decoder can provide without loss of data.</span></span> <span data-ttu-id="9ea74-145">Es ist immer empfehlenswert, in ein breiteres Pixel Format zu konvertieren, als es sich um einen engeren handelt, auch wenn die Größe des Bilds vergrößert wird, da es bei Bedarf immer wieder in ein restriktiveres Format konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ea74-145">It’s always preferable to convert to a wider pixel format than a narrower one, even though it will increase the size of the image, because it can always be reconverted to a more restrictive format if necessary.</span></span> <span data-ttu-id="9ea74-146">Nachdem die Daten verloren gegangen sind, können Sie jedoch nicht wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9ea74-146">However, after the data is lost, it can’t be recovered.</span></span>

## <a name="continued-reading"></a><span data-ttu-id="9ea74-147">Fortgesetztes lesen</span><span class="sxs-lookup"><span data-stu-id="9ea74-147">Continued Reading</span></span>

<span data-ttu-id="9ea74-148">Weitere Informationen zum Erstellen eines WIC-fähigen Codecs finden Sie unter Implementieren von [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).</span><span class="sxs-lookup"><span data-stu-id="9ea74-148">To learn more about how to create a WIC-enabled codec, see [Implementing IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ea74-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ea74-149">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9ea74-150">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="9ea74-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9ea74-151">**IWICBitmapSourceTransform**</span><span class="sxs-lookup"><span data-stu-id="9ea74-151">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[<span data-ttu-id="9ea74-152">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="9ea74-152">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="9ea74-153">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9ea74-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9ea74-154">Implementieren von IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="9ea74-154">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="9ea74-155">Implementieren von IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="9ea74-155">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="9ea74-156">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="9ea74-156">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="9ea74-157">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="9ea74-157">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
