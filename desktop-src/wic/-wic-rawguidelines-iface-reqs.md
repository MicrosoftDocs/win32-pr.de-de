---
description: Schnittstellen Methoden Anforderungen
ms.assetid: 8c2afeb3-3e0b-4f8a-a2f4-df7c9ce4b098
title: Schnittstellen Methoden Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9cabe02900fa789773f4104cf282ab326bd4930
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362851"
---
# <a name="interface-method-requirements"></a><span data-ttu-id="ec189-103">Schnittstellen Methoden Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec189-103">Interface Method Requirements</span></span>

<span data-ttu-id="ec189-104">Nicht jede Methode für jede Schnittstelle muss über eine Implementierung verfügen.</span><span class="sxs-lookup"><span data-stu-id="ec189-104">Not every method on every interface must have an implementation.</span></span> <span data-ttu-id="ec189-105">Einige Codecs verfügen z. b. über globale Metadaten, Miniaturansichten oder Farb Kontexte, während andere Codecs diese nur pro Frame bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ec189-105">For example, some codecs have global metadata, thumbnails, or color contexts, whereas other codecs provide these only on a per-frame basis.</span></span> <span data-ttu-id="ec189-106">Wenn Codec-Autoren diese nur pro Frame bereitstellen, müssen Sie nur die [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) -oder ColorContext-Methode implementieren oder die [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) -Methode oder die [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) -Methode für [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) und [**iwicbitmapframecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) anstelle von [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) und [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)implementieren.</span><span class="sxs-lookup"><span data-stu-id="ec189-106">If codec authors provide these only on a per-frame basis, they need only implement the [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) or ColorContexts, or implement the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) or [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) rather than on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span> <span data-ttu-id="ec189-107">Ebenso verwenden einige Codecs keine indizierten Formate und sind daher nicht zum Implementieren der [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) -und [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) -Methoden erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec189-107">Likewise, some codecs do not use indexed formats and so are not required to implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) and [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) methods.</span></span> <span data-ttu-id="ec189-108">Diese Methoden sind daher optional und bleiben dem Ermessen des Codec-Erstellers überlassen.</span><span class="sxs-lookup"><span data-stu-id="ec189-108">These methods are therefore optional and are left to the discretion of the codec creator.</span></span> <span data-ttu-id="ec189-109">Die meisten anderen Methoden sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec189-109">Most other methods are required.</span></span>

<span data-ttu-id="ec189-110">Für Windows 7 sind [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) / [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) und [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) erforderlich. Sie müssen entweder auf den Klassen auf Klassenebene oder auf Frame-Ebene implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ec189-110">For Windows 7 [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)/[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) and [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) are required and must be implemented on either the contain-level classes or on the frame-level classes.</span></span> <span data-ttu-id="ec189-111">Wenn Ihr Bild Dateiformat keine Vorschau oder Miniaturansichten an einem dieser Orte unterstützt, sollten Sie das Bild Dateiformat überarbeiten, um eine solche Unterstützung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ec189-111">If your image file format doesn't support previews or thumbnails in either of these locations, then you should revise your image file format to provide such support.</span></span>

<span data-ttu-id="ec189-112">Wenn eine Methode nicht implementiert wird, ist es wichtig, einen entsprechenden Fehler zurückzugeben, damit der Aufrufer feststellen kann, dass die angeforderte Funktion nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ec189-112">When a method is not implemented, it is important to return an appropriate error so the caller can determine that the requested feature is not supported.</span></span> <span data-ttu-id="ec189-113">Wenn z. b. Codec-Autoren keine Miniaturansichten auf Container Ebene unterstützen, sollten Sie [wincodec \_ Err \_ codecnothumbnail](-wic-codec-error-codes.md) zurückgeben, wenn eine Anwendung [**getminiatur**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md)aufruft. Wenn Sie über keine Palette verfügen, sollten Sie [wincodec \_ Err \_ palettenicht verfügbar](-wic-codec-error-codes.md)zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ec189-113">For example, if codec authors do not support container-level thumbnails, they should return [WINCODEC\_ERR\_CODECNOTHUMBNAIL](-wic-codec-error-codes.md) when an application calls [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md), and if they don't have a palette, they should return [WINCODEC\_ERR\_PALETTEUNAVAILABLE](-wic-codec-error-codes.md).</span></span> <span data-ttu-id="ec189-114">Wenn kein geeigneter [wincodec- \_ Err](-wic-codec-error-codes.md) -Code vorhanden ist, sollte der Codec E \_ notimpl für nicht implementierte Methoden zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ec189-114">If no suitable [WINCODEC\_ERR](-wic-codec-error-codes.md) code exists, then the codec should return E\_NOTIMPL for unimplemented methods.</span></span>

<span data-ttu-id="ec189-115">In den folgenden Tabellen sind die erforderlichen und optionalen Methoden für jede WIC-Schnittstelle (Windows Imaging Component) aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ec189-115">The following tables list the required and optional methods for each Windows Imaging Component (WIC) interfaces.</span></span>

[<span data-ttu-id="ec189-116">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="ec189-116">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)



<span data-ttu-id="ec189-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ec189-117">Required</span></span>

[<span data-ttu-id="ec189-118">**QueryCapability**</span><span class="sxs-lookup"><span data-stu-id="ec189-118">**QueryCapability**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability)

[<span data-ttu-id="ec189-119">**Initialisieren**</span><span class="sxs-lookup"><span data-stu-id="ec189-119">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize)

[<span data-ttu-id="ec189-120">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="ec189-120">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)

[<span data-ttu-id="ec189-121">**GetDecoderInfo**</span><span class="sxs-lookup"><span data-stu-id="ec189-121">**GetDecoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)

[<span data-ttu-id="ec189-122">**GetFrameCount**</span><span class="sxs-lookup"><span data-stu-id="ec189-122">**GetFrameCount**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

[<span data-ttu-id="ec189-123">**GetFrame**</span><span class="sxs-lookup"><span data-stu-id="ec189-123">**GetFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)

<span data-ttu-id="ec189-124">Optional</span><span class="sxs-lookup"><span data-stu-id="ec189-124">Optional</span></span>

<span data-ttu-id="ec189-125">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹</span><span class="sxs-lookup"><span data-stu-id="ec189-125">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹</span></span>

<span data-ttu-id="ec189-126">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="ec189-126">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span></span>

[<span data-ttu-id="ec189-127">**Getcolorkontexte**</span><span class="sxs-lookup"><span data-stu-id="ec189-127">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

[<span data-ttu-id="ec189-128">**GetMetadataQueryReader**</span><span class="sxs-lookup"><span data-stu-id="ec189-128">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)

[<span data-ttu-id="ec189-129">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="ec189-129">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="ec189-130">¹ erforderlich, wenn das Image Dateiformat Vorschauen auf Container Ebene unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec189-130">¹Required if your image file format supports container-level previews.</span></span> <span data-ttu-id="ec189-131">Wenn dies nicht der Fall ist, wird dringend empfohlen, das Bild Dateiformat zu überarbeiten, um dies zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ec189-131">If this is not the case you are strongly encouraged to revise your image file format to support this.</span></span> <span data-ttu-id="ec189-132">Wenn Sie hier implementiert sind, ist für die Codieren-Klasse auf Container Ebene eine entsprechende [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec189-132">If implemented here, then a corresponding [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) is required on the container-level encode class.</span></span>

<span data-ttu-id="ec189-133">² ist entweder hier oder auf der decodierklasse auf Frame-Ebene erforderlich, abhängig davon, wo das Bild Dateiformat Miniaturansichten speichert.</span><span class="sxs-lookup"><span data-stu-id="ec189-133">²Required either here, or on the frame-level decode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="ec189-134">Wenn Sie hier implementiert sind, ist für die codierklasse auf Container Ebene eine entsprechende [**setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) -Klasse erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec189-134">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) is required on the container-level encode class.</span></span>

[<span data-ttu-id="ec189-135">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="ec189-135">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)



<span data-ttu-id="ec189-136">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ec189-136">Required</span></span>

[<span data-ttu-id="ec189-137">**Getcolorkontexte**</span><span class="sxs-lookup"><span data-stu-id="ec189-137">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

[<span data-ttu-id="ec189-138">**GetMetadataQueryReader**</span><span class="sxs-lookup"><span data-stu-id="ec189-138">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

[<span data-ttu-id="ec189-139">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="ec189-139">**GetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

[<span data-ttu-id="ec189-140">**GetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="ec189-140">**GetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

[<span data-ttu-id="ec189-141">**GetResolution**</span><span class="sxs-lookup"><span data-stu-id="ec189-141">**GetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)

[<span data-ttu-id="ec189-142">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="ec189-142">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

<span data-ttu-id="ec189-143">Optional</span><span class="sxs-lookup"><span data-stu-id="ec189-143">Optional</span></span>

<span data-ttu-id="ec189-144">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span><span class="sxs-lookup"><span data-stu-id="ec189-144">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span></span>

[<span data-ttu-id="ec189-145">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="ec189-145">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="ec189-146">¹ erforderlich entweder hier oder in der Decodierungs Klasse auf Container Ebene, je nachdem, wo Sie das Bild Dateiformat für Miniaturansichten speichert.</span><span class="sxs-lookup"><span data-stu-id="ec189-146">¹Required either here, or on the container-level decode class, depending on where you image file format stores thumbnails.</span></span> <span data-ttu-id="ec189-147">Wenn Sie hier implementiert sind, ist für die Encoder-Klasse auf Frame-Ebene eine entsprechende [**setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) -Klasse erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec189-147">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is required on the frame-level encoder class.</span></span>

[<span data-ttu-id="ec189-148">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="ec189-148">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="ec189-149">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ec189-149">Required</span></span>

[<span data-ttu-id="ec189-150">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="ec189-150">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)

[<span data-ttu-id="ec189-151">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="ec189-151">**GetCount**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)

[<span data-ttu-id="ec189-152">**GetReaderByIndex**</span><span class="sxs-lookup"><span data-stu-id="ec189-152">**GetReaderByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

[<span data-ttu-id="ec189-153">**GetEnumerator**</span><span class="sxs-lookup"><span data-stu-id="ec189-153">**GetEnumerator**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator)



 

[<span data-ttu-id="ec189-154">**IWICBitmapSourceTransform**</span><span class="sxs-lookup"><span data-stu-id="ec189-154">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)



<span data-ttu-id="ec189-155">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ec189-155">Required</span></span>

[<span data-ttu-id="ec189-156">**DoesSupportTransform**</span><span class="sxs-lookup"><span data-stu-id="ec189-156">**DoesSupportTransform**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)

[<span data-ttu-id="ec189-157">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="ec189-157">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)

<span data-ttu-id="ec189-158">Optional</span><span class="sxs-lookup"><span data-stu-id="ec189-158">Optional</span></span>

[<span data-ttu-id="ec189-159">**GetClosestSize**</span><span class="sxs-lookup"><span data-stu-id="ec189-159">**GetClosestSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)

[<span data-ttu-id="ec189-160">**GetClosestPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="ec189-160">**GetClosestPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)



 

[<span data-ttu-id="ec189-161">**IWICDevelopRaw**</span><span class="sxs-lookup"><span data-stu-id="ec189-161">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)

<span data-ttu-id="ec189-162">Weitere Informationen finden Sie [unter Unterstützung für IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md)weiter unten in diesem Dokument.</span><span class="sxs-lookup"><span data-stu-id="ec189-162">See [Support for IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md), later in this document.</span></span>

[<span data-ttu-id="ec189-163">**Iwicbitmapcoder**</span><span class="sxs-lookup"><span data-stu-id="ec189-163">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)



<span data-ttu-id="ec189-164">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ec189-164">Required</span></span>

[<span data-ttu-id="ec189-165">**Initialisieren**</span><span class="sxs-lookup"><span data-stu-id="ec189-165">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="ec189-166">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="ec189-166">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)

[<span data-ttu-id="ec189-167">**GetEncoderInfo**</span><span class="sxs-lookup"><span data-stu-id="ec189-167">**GetEncoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

[<span data-ttu-id="ec189-168">**"Kreatenewframe"**</span><span class="sxs-lookup"><span data-stu-id="ec189-168">**CreateNewFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)

[<span data-ttu-id="ec189-169">**Einzusetzen**</span><span class="sxs-lookup"><span data-stu-id="ec189-169">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="ec189-170">Optional</span><span class="sxs-lookup"><span data-stu-id="ec189-170">Optional</span></span>

<span data-ttu-id="ec189-171">[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹</span><span class="sxs-lookup"><span data-stu-id="ec189-171">[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹</span></span>

<span data-ttu-id="ec189-172">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="ec189-172">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span></span>

[<span data-ttu-id="ec189-173">**Setcolorkontexte**</span><span class="sxs-lookup"><span data-stu-id="ec189-173">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setcolorcontexts)

[<span data-ttu-id="ec189-174">**GetMetadataQueryWriter**</span><span class="sxs-lookup"><span data-stu-id="ec189-174">**GetMetadataQueryWriter**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

[<span data-ttu-id="ec189-175">**SetPalette**</span><span class="sxs-lookup"><span data-stu-id="ec189-175">**SetPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)



 

<span data-ttu-id="ec189-176">¹ erforderlich, wenn das Bild Dateiformat Vorschauen auf Frame-Ebene unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec189-176">¹Required if your image file format supports frame-level previews.</span></span>

<span data-ttu-id="ec189-177">² ist entweder hier oder auf der codieren-Klasse auf Frame-Ebene erforderlich, abhängig davon, wo Ihr Bild Dateiformat Miniaturansichten speichert.</span><span class="sxs-lookup"><span data-stu-id="ec189-177">²Required either here, or on the frame-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="ec189-178">Wenn Sie hier implementiert sind, ist für die decodierklasse auf Container Ebene eine entsprechende [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) -Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec189-178">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) is required on the container-level decode class.</span></span>

[<span data-ttu-id="ec189-179">**IWICBitmapFrameEncode**</span><span class="sxs-lookup"><span data-stu-id="ec189-179">**IWICBitmapFrameEncode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)



<span data-ttu-id="ec189-180">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ec189-180">Required</span></span>

[<span data-ttu-id="ec189-181">**Initialisieren**</span><span class="sxs-lookup"><span data-stu-id="ec189-181">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="ec189-182">**Setcolorkontexte**</span><span class="sxs-lookup"><span data-stu-id="ec189-182">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="ec189-183">**Setcolorkontexte**</span><span class="sxs-lookup"><span data-stu-id="ec189-183">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="ec189-184">**SetSize**</span><span class="sxs-lookup"><span data-stu-id="ec189-184">**SetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)

[<span data-ttu-id="ec189-185">**SetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="ec189-185">**SetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat)

[<span data-ttu-id="ec189-186">**Projekt Mappe**</span><span class="sxs-lookup"><span data-stu-id="ec189-186">**SetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

[<span data-ttu-id="ec189-187">**"WritePixels"**</span><span class="sxs-lookup"><span data-stu-id="ec189-187">**WritePixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)

[<span data-ttu-id="ec189-188">**Schreibgeschützte Datenquelle**</span><span class="sxs-lookup"><span data-stu-id="ec189-188">**WriteSource**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)

[<span data-ttu-id="ec189-189">**Einzusetzen**</span><span class="sxs-lookup"><span data-stu-id="ec189-189">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="ec189-190">Optional</span><span class="sxs-lookup"><span data-stu-id="ec189-190">Optional</span></span>

<span data-ttu-id="ec189-191">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹</span><span class="sxs-lookup"><span data-stu-id="ec189-191">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹</span></span>

[<span data-ttu-id="ec189-192">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="ec189-192">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)



 

<span data-ttu-id="ec189-193">¹ erforderlich entweder hier oder auf der Codierungs Klasse auf Container Ebene, abhängig davon, wo das Bild Dateiformat Miniaturansichten speichert.</span><span class="sxs-lookup"><span data-stu-id="ec189-193">¹Required either here, or on the container-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="ec189-194">Wenn Sie hier implementiert sind, ist für die decodierklasse auf Frame-Ebene eine zugehörige [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) -Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec189-194">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) is required on the frame-level decode class.</span></span>

[<span data-ttu-id="ec189-195">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="ec189-195">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="ec189-196">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ec189-196">Required</span></span>

[<span data-ttu-id="ec189-197">**InitializeFromBlockReader**</span><span class="sxs-lookup"><span data-stu-id="ec189-197">**InitializeFromBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader)

[<span data-ttu-id="ec189-198">**AddWriter**</span><span class="sxs-lookup"><span data-stu-id="ec189-198">**AddWriter**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter)

[<span data-ttu-id="ec189-199">**"Getschreiterbyindex"**</span><span class="sxs-lookup"><span data-stu-id="ec189-199">**GetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex)

[<span data-ttu-id="ec189-200">**Setschreiterbyindex**</span><span class="sxs-lookup"><span data-stu-id="ec189-200">**SetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex)

[<span data-ttu-id="ec189-201">**Removeschreiterbyindex**</span><span class="sxs-lookup"><span data-stu-id="ec189-201">**RemoveWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex)



 

## <a name="related-topics"></a><span data-ttu-id="ec189-202">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec189-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ec189-203">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ec189-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ec189-204">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="ec189-204">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="ec189-205">WIC-Richtlinien für Kamera Rohbild Formate</span><span class="sxs-lookup"><span data-stu-id="ec189-205">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="ec189-206">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="ec189-206">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
