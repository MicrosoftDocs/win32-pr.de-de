---
description: Implementieren von IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implementieren von IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b31bca377828606fe1beb68d6f1d95d290e01407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042331"
---
# <a name="implementing-iwicbitmapdecoder"></a><span data-ttu-id="c5db3-103">Implementieren von IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="c5db3-103">Implementing IWICBitmapDecoder</span></span>

## <a name="iwicbitmapdecoder"></a><span data-ttu-id="c5db3-104">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="c5db3-104">IWICBitmapDecoder</span></span>

<span data-ttu-id="c5db3-105">Wenn eine Anwendung einen Decoder anfordert, wird die [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Schnittstelle als erster Punkt der Interaktion mit dem Codec behandelt.</span><span class="sxs-lookup"><span data-stu-id="c5db3-105">When an application requests a decoder, the first point of interaction with the codec is through the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface.</span></span> <span data-ttu-id="c5db3-106">Dabei handelt es sich um die Schnittstelle auf Container Ebene, die Zugriff auf die Eigenschaften der obersten Ebene des Containers und, am wichtigsten, die darin enthaltenen Frames bietet.</span><span class="sxs-lookup"><span data-stu-id="c5db3-106">This is the container-level interface that provides access to the top-level properties of the container and, most importantly, the frames it contains.</span></span> <span data-ttu-id="c5db3-107">Dies ist die primäre Schnittstelle in Ihrer Decoder-Klasse auf Container-Ebene.</span><span class="sxs-lookup"><span data-stu-id="c5db3-107">This is the primary interface on your container-level decoder class.</span></span>

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

<span data-ttu-id="c5db3-108">Einige Bildformate verfügen über globale Miniaturansichten, Farb Kontexte oder Metadaten, während viele Bildformate diese nur pro Frame bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c5db3-108">Some image formats have global thumbnails, color contexts, or metadata, while many image formats provide these only on a per-frame basis.</span></span> <span data-ttu-id="c5db3-109">Die Methoden für den Zugriff auf diese Elemente sind für [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)optional, jedoch für [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c5db3-109">The methods for accessing these items are optional on [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), but are required on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span> <span data-ttu-id="c5db3-110">Ebenso verwenden einige Codecs keine indizierten Pixel Formate und müssen daher nicht die [CopyPalette](-wic-imp-iwicbitmapframedecode.md) -Methoden für beide Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="c5db3-110">Likewise, some codecs do not use indexed pixel formats and so do not need to implement the [CopyPalette](-wic-imp-iwicbitmapframedecode.md) methods on either interface.</span></span> <span data-ttu-id="c5db3-111">Weitere Informationen zu den optionalen **IWICBitmapDecoder** -Methoden finden Sie unter [Implementieren von IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), wo Sie am häufigsten implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="c5db3-111">For more information on the optional **IWICBitmapDecoder** methods, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), where they are most commonly implemented.</span></span>

### <a name="querycapability"></a><span data-ttu-id="c5db3-112">QueryCapability</span><span class="sxs-lookup"><span data-stu-id="c5db3-112">QueryCapability</span></span>

<span data-ttu-id="c5db3-113">[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) ist die Methode, die für die Codec-Vermittlung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5db3-113">[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is the method used for codec arbitration.</span></span> <span data-ttu-id="c5db3-114">(Informationen finden Sie unter Ermittlung [und Schiedsgerichtsbarkeit](-wic-howwicworks.md) im Thema [wie die Windows Imaging-Komponente funktioniert](-wic-howwicworks.md) .)</span><span class="sxs-lookup"><span data-stu-id="c5db3-114">(See [Discovery and Arbitration](-wic-howwicworks.md) in the [How The Windows Imaging Component Works](-wic-howwicworks.md) topic).</span></span> <span data-ttu-id="c5db3-115">Wenn zwei Codecs das gleiche Bildformat decodieren können, oder wenn ein Muster Konflikt auftritt, bei dem zwei Codecs dasselbe identifizierende Muster verwenden, können Sie mit dieser Methode den Codec auswählen, mit dem ein bestimmtes Bild am besten verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c5db3-115">If two codecs are capable of decoding the same image format, or if a pattern collision occurs in which two codecs use the same identifying pattern, this method allows you to select the codec that can best handle any specific image.</span></span>

<span data-ttu-id="c5db3-116">Wenn Sie diese Methode aufrufen, übergibt die Windows Imaging Component (WIC) den eigentlichen Stream, der das Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="c5db3-116">When invoking this method, Windows Imaging Component (WIC) passes you the actual stream containing the image.</span></span> <span data-ttu-id="c5db3-117">Sie müssen überprüfen, ob Sie jeden Frame innerhalb des Bilds decodieren und die Metadatenblöcke durchlaufen können, um genau zu deklarieren, welche Funktionen dieser Decoder in Bezug auf den an ihn übergebenen spezifischen Dateistream hat.</span><span class="sxs-lookup"><span data-stu-id="c5db3-117">You must verify whether you can decode each frame within the image and enumerate through the metadata blocks, to accurately declare what capabilities this decoder has with respect to the specific file stream passed to it.</span></span> <span data-ttu-id="c5db3-118">Dies ist für alle Decoder wichtig, jedoch besonders wichtig für Bildformate, die auf Tagged Image File Format (TIFF)-Containern basieren.</span><span class="sxs-lookup"><span data-stu-id="c5db3-118">This is important for all decoders, but particularly important for image formats based on Tagged Image File Format (TIFF) containers.</span></span> <span data-ttu-id="c5db3-119">Der Ermittlungs Vorgang funktioniert, indem den Decodern in der Registrierung zugeordneten Mustern Muster in der eigentlichen Bilddatei zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c5db3-119">The discovery process works by matching patterns associated with decoders in the registry to patterns in the actual image file.</span></span> <span data-ttu-id="c5db3-120">Wenn Sie Ihr identifizierendes Muster in der Registrierung deklarieren, gewährleisten Sie, dass Ihr Decoder immer für Bilder in Ihrem Bildformat erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="c5db3-120">Declaring your identifying pattern in the registry guarantees that your decoder will always be detected for images in your image format.</span></span> <span data-ttu-id="c5db3-121">Der Decoder kann jedoch weiterhin für Bilder in anderen Formaten erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="c5db3-121">However, your decoder could still be detected for images in other formats.</span></span> <span data-ttu-id="c5db3-122">Beispielsweise enthalten alle TIFF-Container das TIFF-Muster, bei dem es sich um ein gültiges Identifikationsmuster für das TIFF-Bildformat handelt.</span><span class="sxs-lookup"><span data-stu-id="c5db3-122">For example, all TIFF containers include the TIFF pattern, which is a valid identifying pattern for the TIFF image format.</span></span> <span data-ttu-id="c5db3-123">Dies bedeutet, dass bei der Ermittlung mindestens zwei identifizierende Muster in Bilddateien für ein beliebiges Bildformat gefunden werden, das auf einem Container im TIFF-Format basiert.</span><span class="sxs-lookup"><span data-stu-id="c5db3-123">This means that, during discovery, at least two identifying patterns will be found in image files for any image format that’s based on a TIFF-style container.</span></span> <span data-ttu-id="c5db3-124">Eine ist das TIFF-Muster, und die andere ist das tatsächliche Bildformat Muster.</span><span class="sxs-lookup"><span data-stu-id="c5db3-124">One will be the TIFF pattern and the other will be the actual image format pattern.</span></span> <span data-ttu-id="c5db3-125">Obwohl es weniger wahrscheinlich ist, gibt es auch Muster Konflikte zwischen anderen nicht verknüpften Bildformaten.</span><span class="sxs-lookup"><span data-stu-id="c5db3-125">While less likely, there could be pattern collisions between other unrelated image formats as well.</span></span> <span data-ttu-id="c5db3-126">Aus diesem Grund ist die Ermittlung und die Schiedsgerichtsbarkeit ein zweistufiger Prozess.</span><span class="sxs-lookup"><span data-stu-id="c5db3-126">This is why discovery and arbitration is a two-stage process.</span></span> <span data-ttu-id="c5db3-127">Überprüfen Sie immer, ob der an [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) übergebenen Bildstream tatsächlich eine gültige Instanz Ihres eigenen Bildformats ist.</span><span class="sxs-lookup"><span data-stu-id="c5db3-127">Always verify that the image stream passed to [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is actually a valid instance of your own image format.</span></span> <span data-ttu-id="c5db3-128">Wenn Ihr Codec ein Bildformat decodiert, für das Sie die Spezifikation nicht besitzen, sollte Ihre **QueryCapability** -Implementierung außerdem prüfen, ob eine Funktion vorhanden ist, die möglicherweise in der Bildformat Spezifikation gültig ist, die Ihr Codec nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c5db3-128">Also, if your codec decodes an image format for which you don’t own the specification, your **QueryCapability** implementation should check for the presence of any feature that may be valid under the image format specification that your codec doesn’t implement.</span></span> <span data-ttu-id="c5db3-129">Dadurch wird sichergestellt, dass Benutzer keine unnötigen Decodierungs Fehler haben oder unerwartete Ergebnisse mit Ihrem Codec erhalten.</span><span class="sxs-lookup"><span data-stu-id="c5db3-129">This will ensure that users do not experience unnecessary decoding failures or get unexpected results with your codec.</span></span>

<span data-ttu-id="c5db3-130">Bevor Sie einen Vorgang für das Bild ausführen, müssen Sie die aktuelle Position des Streams speichern, damit Sie Sie an ihrer ursprünglichen Position wiederherstellen können, bevor Sie von der-Methode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c5db3-130">Before performing any operation on the image, you must save the current position of the stream, so you can restore it to its original position before returning from the method.</span></span> <span data-ttu-id="c5db3-131">Die [**wicbitmapdecoderfunktionen**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) -Enumeration, die die Funktionen angibt, wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="c5db3-131">The [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) enumeration that specifies the capabilities is defined as follows:</span></span>

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

<span data-ttu-id="c5db3-132">Sie sollten **WICBitmapDecoderCapabilitySameEncoder** nur deklarieren, wenn der Encoder der Codierer ist, der das Image codiert hat.</span><span class="sxs-lookup"><span data-stu-id="c5db3-132">You should declare **WICBitmapDecoderCapabilitySameEncoder** only if your encoder was the one that encoded the image.</span></span> <span data-ttu-id="c5db3-133">Wenn Sie überprüft haben, ob Sie die einzelnen Frames im Container decodieren können, deklarieren Sie entweder **WICBitmapDecoderCapabilityCanDecodeSomeImages** , wenn Sie einige, aber nicht alle Frames decodieren können, **WICBitmapDecoderCapabilityCanDecodeAllImages** , wenn Sie alle Frames decodieren können, oder keines von beiden.</span><span class="sxs-lookup"><span data-stu-id="c5db3-133">After verifying whether you can decode each frame in the container, declare either **WICBitmapDecoderCapabilityCanDecodeSomeImages** if you can decode some but not all of the frames, **WICBitmapDecoderCapabilityCanDecodeAllImages** if you can decode all of the frames, or neither if you cannot decode any of them.</span></span> <span data-ttu-id="c5db3-134">(Diese zwei auffügeenden schließen sich gegenseitig aus. Wenn Sie **WICBitmapDecoderCapabilityCanDecodeAllImages** zurückgeben, wird **WICBitmapDecoderCapabilityCanDecodeSomeImages** ignoriert.) Deklarieren Sie **WICBitmapDecoderCapabilityCanEnumerateMetadata** , nachdem Sie sich vergewissert haben, dass Sie die Metadatenblöcke im Bild Container durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="c5db3-134">(These two enums are mutually exclusive; if you return **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** will be ignored.) Declare **WICBitmapDecoderCapabilityCanEnumerateMetadata** after verifying that you can enumerate through the metadata blocks in the image container.</span></span> <span data-ttu-id="c5db3-135">Sie müssen nicht in jedem Frame eine Miniaturansicht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c5db3-135">You don’t have to check for a thumbnail in every frame.</span></span> <span data-ttu-id="c5db3-136">Wenn eine globale Miniaturansicht vorliegt und Sie Sie decodieren können, können Sie **wicbitmapdecodercapabilitycandecodeminiatur** deklarieren.</span><span class="sxs-lookup"><span data-stu-id="c5db3-136">If there is a global thumbnail and you can decode it, you can declare **WICBitmapDecoderCapabilityCanDecodeThumbnail**.</span></span> <span data-ttu-id="c5db3-137">Wenn keine globale Miniaturansicht vorhanden ist, versuchen Sie, die Miniaturansicht für Frame 0 zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="c5db3-137">If there is no global thumbnail, then attempt to decode the thumbnail for Frame 0.</span></span> <span data-ttu-id="c5db3-138">Wenn keine Miniaturansicht an einem dieser Orte vorhanden ist, deklarieren Sie diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="c5db3-138">If there is no thumbnail in either of these places, do not declare this capability.</span></span>

<span data-ttu-id="c5db3-139">Nachdem Sie die Funktionen des Decoders in Bezug auf den an diese Methode übergebenen Bildstream festgelegt haben, führen Sie eine OR-Operation mit den [**wicbitmapdecoderfunktionen**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) aus, die Sie überprüft haben, die dieser Decoder für dieses Bild ausführen kann, und geben das Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="c5db3-139">After determining the capabilities of the decoder with respect to the image stream passed to this method, perform an OR operation with the [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) you have verified that this decoder can perform on this image, and return the result.</span></span> <span data-ttu-id="c5db3-140">Denken Sie daran, den Datenstrom vor der Rückgabe an seine ursprüngliche Position wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="c5db3-140">Remember to restore the stream to its original position before returning.</span></span>

### <a name="initialize"></a><span data-ttu-id="c5db3-141">Initialisieren</span><span class="sxs-lookup"><span data-stu-id="c5db3-141">Initialize</span></span>

<span data-ttu-id="c5db3-142">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) wird von einer Anwendung aufgerufen, nachdem ein Decoder zum Decodieren eines bestimmten Bilds ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="c5db3-142">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) is invoked by an application after a decoder has been selected to decode a specific image.</span></span> <span data-ttu-id="c5db3-143">Der Bildstream wird an den Decoder übergeben, und ein Aufrufer kann optional die [**wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) -Cache Option für den Umgang mit den Metadaten in der Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="c5db3-143">The image stream is passed to the decoder, and a caller may optionally specify the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) cache option for dealing with the metadata in the file.</span></span>

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

<span data-ttu-id="c5db3-144">Einige Anwendungen verwenden Metadaten mehr als andere.</span><span class="sxs-lookup"><span data-stu-id="c5db3-144">Some applications use metadata more than others.</span></span> <span data-ttu-id="c5db3-145">Die meisten Anwendungen müssen nicht auf alle Metadaten in einer Bilddatei zugreifen, und es werden bestimmte Metadaten angefordert, wenn Sie benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="c5db3-145">Most applications don’t need to access all the metadata in an image file, and will request specific metadata as they need it.</span></span> <span data-ttu-id="c5db3-146">Andere Anwendungen würden stattdessen alle Metadaten vorab zwischenspeichern, um den Datei Datenstrom zu öffnen und die Datenträger-e/a jedes Mal auszuführen, wenn Sie auf Metadaten zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="c5db3-146">Other applications would rather cache all the metadata up front than keep the file stream open and perform disk I/O every time they need to access metadata.</span></span> <span data-ttu-id="c5db3-147">Wenn der Aufrufer keine Metadatencache-Option angibt, sollte das Standardverhalten beim Zwischenspeichern bei Bedarf Zwischenspeichern erfolgen.</span><span class="sxs-lookup"><span data-stu-id="c5db3-147">If the caller doesn’t specify a metadata cache option, the default caching behavior should be cache on demand.</span></span> <span data-ttu-id="c5db3-148">Dies bedeutet, dass keine Metadaten in den Arbeitsspeicher geladen werden sollen, bis die Anwendung eine bestimmte Anforderung für diese Metadaten sendet.</span><span class="sxs-lookup"><span data-stu-id="c5db3-148">This means no metadata should be loaded into memory until the application makes a specific request for that metadata.</span></span> <span data-ttu-id="c5db3-149">Wenn die Anwendung **WICDecodeMetadataCacheOnLoad** angibt, sollten die Metadaten sofort in den Speicher geladen und zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c5db3-149">If the application specifies **WICDecodeMetadataCacheOnLoad**, the metadata should be loaded in memory immediately and cached.</span></span> <span data-ttu-id="c5db3-150">Wenn Metadaten beim Laden zwischengespeichert werden, kann der Datei Datenstrom freigegeben werden, nachdem die Metadaten zwischengespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="c5db3-150">When metadata is cached on load, the file stream may be released after the metadata has been cached.</span></span>

### <a name="getcontainerformat"></a><span data-ttu-id="c5db3-151">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="c5db3-151">GetContainerFormat</span></span>

<span data-ttu-id="c5db3-152">Zum Implementieren von [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)geben Sie einfach die GUID des Bildformats des Bilds zurück, für das der Decoder instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="c5db3-152">To implement [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), just return the GUID of the image format of the image for which the decoder is instantiated.</span></span> <span data-ttu-id="c5db3-153">Diese Methode ist auch auf [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) und [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)implementiert.</span><span class="sxs-lookup"><span data-stu-id="c5db3-153">This method is also implemented on [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span>

### <a name="getdecoderinfo"></a><span data-ttu-id="c5db3-154">GetDecoderInfo</span><span class="sxs-lookup"><span data-stu-id="c5db3-154">GetDecoderInfo</span></span>

<span data-ttu-id="c5db3-155">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) gibt ein [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c5db3-155">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) returns an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) object.</span></span> <span data-ttu-id="c5db3-156">Um das **IWICBitmapDecoderInfo** -Objekt zu erhalten, übergeben Sie einfach die GUID Ihres Decoders an die Methode " [**fiatecomponentinfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) " in [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), und fordern Sie dann die **IWICBitmapDecoderInfo** -Schnittstelle an, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c5db3-156">To get the **IWICBitmapDecoderInfo** object, just pass the GUID of your decoder to the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method on [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), and then request the **IWICBitmapDecoderInfo** interface on it, as shown in the following example.</span></span>


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a><span data-ttu-id="c5db3-157">GetFrameCount</span><span class="sxs-lookup"><span data-stu-id="c5db3-157">GetFrameCount</span></span>

<span data-ttu-id="c5db3-158">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) gibt nur die Anzahl der Frames im Container zurück.</span><span class="sxs-lookup"><span data-stu-id="c5db3-158">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) just returns the number of frames in the container.</span></span> <span data-ttu-id="c5db3-159">Einige Containerformate unterstützen mehrere Frames, und andere unterstützen nur einen Frame pro Container.</span><span class="sxs-lookup"><span data-stu-id="c5db3-159">Some container formats support multiple frames, and others support only one frame per container.</span></span>

### <a name="getframe"></a><span data-ttu-id="c5db3-160">GetFrame</span><span class="sxs-lookup"><span data-stu-id="c5db3-160">GetFrame</span></span>

<span data-ttu-id="c5db3-161">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) ist eine wichtige Methode für die [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Schnittstelle, da der Frame die eigentlichen Bildbits enthält und das von dieser Methode zurückgegebene Frame-Decoderobjekt das Objekt ist, das die tatsächliche Decodierung des angeforderten Bilds durchführt.</span><span class="sxs-lookup"><span data-stu-id="c5db3-161">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) is an important method on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface because the frame contains the actual image bits, and the frame decoder object returned from this method is the object that does the actual decoding of the requested image.</span></span> <span data-ttu-id="c5db3-162">Dies ist das andere Objekt, das beim Schreiben eines Decoders implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c5db3-162">That is the other object you need to implement when writing a decoder.</span></span> <span data-ttu-id="c5db3-163">Weitere Informationen zu Frame-Decodern finden Sie unter [Implementieren von IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).</span><span class="sxs-lookup"><span data-stu-id="c5db3-163">For more information on frame decoders, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).</span></span>

### <a name="getpreview"></a><span data-ttu-id="c5db3-164">GetPreview</span><span class="sxs-lookup"><span data-stu-id="c5db3-164">GetPreview</span></span>

<span data-ttu-id="c5db3-165">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) gibt eine Vorschau des Images zurück.</span><span class="sxs-lookup"><span data-stu-id="c5db3-165">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) returns a preview of the image.</span></span> <span data-ttu-id="c5db3-166">Eine ausführliche Erläuterung zu Vorschauen finden Sie unter [Implementieren der iwicbitmapcoder](-wic-imp-iwicbitmapencoder.md) -Methode auf der Schnittstelle [Implementieren der iwicbitmakcoder](-wic-imp-iwicbitmapencoder.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c5db3-166">For a detailed discussion of previews, see the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) method on the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) interface.</span></span>

<span data-ttu-id="c5db3-167">Wenn Ihr Bildformat eine eingebettete JPEG-Vorschau enthält, wird dringend empfohlen, anstatt einen JPEG-Decoder zum Decodieren zu schreiben, delegieren Sie an den JPEG-Decoder, der mit der WIC-Plattform ausgeliefert wird, um Vorschauen und Miniaturansichten zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="c5db3-167">If your image format contains an embedded JPEG preview, it is strongly recommend that, instead of writing a JPEG decoder to decode it, you delegate to the JPEG decoder that ships with the WIC platform for decoding previews and thumbnails.</span></span> <span data-ttu-id="c5db3-168">Suchen Sie zu diesem Zweck den Anfang der Daten des Vorschau Bilds im Stream, und rufen Sie die Methode " [**foratedecoderfromstream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) " für [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)auf.</span><span class="sxs-lookup"><span data-stu-id="c5db3-168">To do this, seek to the beginning of the preview image data in the stream and invoke the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method on the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a><span data-ttu-id="c5db3-169">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5db3-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c5db3-170">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="c5db3-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c5db3-171">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="c5db3-171">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="c5db3-172">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="c5db3-172">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="c5db3-173">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c5db3-173">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c5db3-174">Decoder-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c5db3-174">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="c5db3-175">Implementieren von IWICBitmapCodecProgressNotification (Decoder)</span><span class="sxs-lookup"><span data-stu-id="c5db3-175">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="c5db3-176">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="c5db3-176">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="c5db3-177">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="c5db3-177">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



