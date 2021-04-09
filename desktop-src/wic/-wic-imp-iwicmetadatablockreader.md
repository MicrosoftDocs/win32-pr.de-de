---
description: Implementieren von IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Implementieren von IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bfe53e87dae52d004fa90d1104fb60f252085d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865548"
---
# <a name="implementing-iwicmetadatablockreader"></a><span data-ttu-id="9502e-103">Implementieren von IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="9502e-103">Implementing IWICMetadataBlockReader</span></span>

## <a name="iwicmetadatablockreader"></a><span data-ttu-id="9502e-104">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="9502e-104">IWICMetadataBlockReader</span></span>

<span data-ttu-id="9502e-105">Häufig sind mehrere Metadatenblöcke innerhalb eines Bilds vorhanden, von denen jedes verschiedene Informationstypen in unterschiedlichen Formaten verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="9502e-105">Multiple blocks of metadata often exist within an image, each exposing different types of information in different formats.</span></span> <span data-ttu-id="9502e-106">Im WIC-Modell (Windows Imaging Component, Windows Imaging Component) handelt es sich bei metadatenhandlern um unterschiedliche Komponenten, die wie Decoders zur Laufzeit erkennbar sind.</span><span class="sxs-lookup"><span data-stu-id="9502e-106">In the Windows Imaging Component (WIC) model, metadata handlers are distinct components that, like decoders, are discoverable at run time.</span></span> <span data-ttu-id="9502e-107">Jedes Metadatenformat verfügt über einen separaten Handler, und jeder dieser Metadatenhandler kann mit jedem Bildformat verwendet werden, das das von ihm verwendete Metadatenformat unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9502e-107">Each metadata format has a separate handler, and each of these metadata handlers can be used with any image format that supports the metadata format it handles.</span></span> <span data-ttu-id="9502e-108">Wenn Ihr Bildformat also EXIF, XMP, IPTC oder ein anderes Format unterstützt, können Sie die standardmäßigen Metadatenhandler für diese Formate nutzen, die mit WIC ausgeliefert werden, und Sie müssen keine eigenen schreiben.</span><span class="sxs-lookup"><span data-stu-id="9502e-108">Therefore, if your image format supports EXIF, XMP, IPTC, or another format, you can take advantage of the standard metadata handlers for these formats that ship with WIC, and you do not need to write your own.</span></span> <span data-ttu-id="9502e-109">Wenn Sie ein neues Metadatenformat erstellen, müssen Sie selbstverständlich einen Metadatenhandler dafür schreiben, der zur Laufzeit so erkannt und aufgerufen wird, wie es bei den standardmäßigen der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="9502e-109">Of course, if you create a new metadata format, you must write a metadata handler for it, which will be discovered and invoked at run time just as the standard ones are.</span></span>

> [!Note]  
> <span data-ttu-id="9502e-110">Wenn Ihr Bildformat auf einem Tagged Image File Format (TIFF) oder JPEG-Container basiert, müssen Sie keine Metadatenhandler schreiben (es sei denn, Sie entwickeln ein neues oder proprietäres Metadatenformat).</span><span class="sxs-lookup"><span data-stu-id="9502e-110">If your image format is based on a Tagged Image File Format (TIFF) or JPEG container, you won’t need to write any metadata handlers (unless you develop a new or proprietary metadata format).</span></span> <span data-ttu-id="9502e-111">In TIFF-und JPEG-Containern befinden sich Metadatenblöcke innerhalb von ifds, und jeder Container hat eine andere IFD-Struktur.</span><span class="sxs-lookup"><span data-stu-id="9502e-111">In TIFF and JPEG containers, blocks of metadata are located within IFDs, and each container has a different IFD structure.</span></span> <span data-ttu-id="9502e-112">WIC stellt IFD-Handler für beide Containerformate bereit, die in der IFD-Struktur navigieren und an die standardmetadatenhandler delegiert werden, um auf die darin enthaltenen Metadaten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="9502e-112">WIC provides IFD handlers for both of these container formats that navigate the IFD structure and delegate to the standard metadata handlers to access the metadata within them.</span></span> <span data-ttu-id="9502e-113">Wenn Ihr Bildformat also auf einem dieser Container basiert, können Sie die WIC-IFD-Handler automatisch nutzen.</span><span class="sxs-lookup"><span data-stu-id="9502e-113">So, if your image format is based on either of these containers, you can automatically take advantage of the WIC IFD handlers.</span></span> <span data-ttu-id="9502e-114">Wenn Sie jedoch über ein proprietäres Containerformat verfügen, das über eine eigene, eindeutige Metadatenstruktur der obersten Ebene verfügt, müssen Sie einen Handler schreiben, der in der Struktur der obersten Ebene navigieren und an die entsprechenden Metadaten-Handler delegieren kann, genau wie bei den IFD-Handlern.)</span><span class="sxs-lookup"><span data-stu-id="9502e-114">However, if you have a proprietary container format that has its own unique top-level metadata structure, you must write a handler that can navigate that top-level structure and delegate to the appropriate metadata handlers, just like the IFD handlers do.)</span></span>

 

<span data-ttu-id="9502e-115">Die gleiche Art und Weise, wie WIC eine Abstraktions Ebene für Anwendungen bereitstellt, die Ihnen das Arbeiten mit allen Bildformaten auf die gleiche Weise durch einen konsistenten Satz von Schnittstellen ermöglicht, stellt WIC eine Abstraktions Ebene für Codec-Autoren in Bezug auf Metadatenformate bereit.</span><span class="sxs-lookup"><span data-stu-id="9502e-115">The same way WIC provides a layer of abstraction for applications that allows them to work with all image formats in the same way through a consistent set of interfaces, WIC provides a layer of abstraction for codec authors with regard to metadata formats.</span></span> <span data-ttu-id="9502e-116">Wie bereits erwähnt, müssen Codec-Autoren in der Regel nicht direkt mit den verschiedenen Metadatenformaten arbeiten, die möglicherweise in einem Bild vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9502e-116">As noted previously, codec authors generally do not need to work directly with the various metadata formats that may be present in an image.</span></span> <span data-ttu-id="9502e-117">Jeder Codec-Autor ist jedoch dafür zuständig, die Metadatenblöcke aufzuzählen, damit ein geeigneter Metadatenhandler für jeden Block ermittelt und instanziiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9502e-117">However, every codec author is responsible for providing a way to enumerate the blocks of metadata so an appropriate metadata handler can be discovered and instantiated for each block.</span></span>

<span data-ttu-id="9502e-118">Sie müssen diese Schnittstelle für die Decodierung der Frame-Ebene implementieren.</span><span class="sxs-lookup"><span data-stu-id="9502e-118">You must implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="9502e-119">Sie müssen Sie möglicherweise auch in Ihrer Decoder-Klasse auf Container-Ebene implementieren, wenn Ihr Bildformat globale Metadaten außerhalb einzelner Bild Rahmen verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="9502e-119">You may also need to implement it on your container-level decoder class if your image format exposes global metadata outside of any individual image frames.</span></span>

``` syntax
interface IWICMetadataBlockReader : IUnknown
{
   // All methods required
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetCount ( UINT *pcCount );
   HRESULT GetEnumerator ( IEnumUnknown **ppIEnumMetadata );
   HRESULT GetReaderByIndex ( UINT nIndex, IWICMetadataReader **ppIMetadataReader );
}
```

-   [<span data-ttu-id="9502e-120">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="9502e-120">GetContainerFormat</span></span>](#getcontainerformat)
-   [<span data-ttu-id="9502e-121">GetCount</span><span class="sxs-lookup"><span data-stu-id="9502e-121">GetCount</span></span>](#getcount)
-   [<span data-ttu-id="9502e-122">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="9502e-122">GetEnumerator</span></span>](#getenumerator)
-   [<span data-ttu-id="9502e-123">GetReaderByIndex</span><span class="sxs-lookup"><span data-stu-id="9502e-123">GetReaderByIndex</span></span>](#getreaderbyindex)

### <a name="getcontainerformat"></a><span data-ttu-id="9502e-124">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="9502e-124">GetContainerFormat</span></span>

<span data-ttu-id="9502e-125">[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) ist identisch mit der Methode [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) bei der [Implementierung von IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).</span><span class="sxs-lookup"><span data-stu-id="9502e-125">[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) is the same as the [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) method on [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).</span></span>

### <a name="getcount"></a><span data-ttu-id="9502e-126">GetCount</span><span class="sxs-lookup"><span data-stu-id="9502e-126">GetCount</span></span>

<span data-ttu-id="9502e-127">" [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) " gibt die Anzahl der Metadatenblöcke auf oberster Ebene zurück, die dem Frame zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9502e-127">[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) returns the number of top-level metadata blocks associated with the frame.</span></span>

### <a name="getenumerator"></a><span data-ttu-id="9502e-128">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="9502e-128">GetEnumerator</span></span>

<span data-ttu-id="9502e-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) gibt einen Enumerator zurück, der vom Aufrufer verwendet werden kann, um die Metadatenblöcke im Frame aufzulisten und ihre Metadaten zu lesen.</span><span class="sxs-lookup"><span data-stu-id="9502e-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) returns an enumerator that the caller can use to enumerate over the metadata blocks in the frame and read their metadata.</span></span> <span data-ttu-id="9502e-130">Zum Implementieren dieser Methode müssen Sie einen metadatenreader für jeden Metadatenblock erstellen und ein Enumerationsobjekt implementieren, das die Auflistung der metadatenleser auflistet.</span><span class="sxs-lookup"><span data-stu-id="9502e-130">To implement this method, you need to create a metadata reader for each block of metadata, and implement an enumeration object that enumerates over the collection of metadata readers.</span></span> <span data-ttu-id="9502e-131">Das Enumerationsobjekt muss [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) implementieren, damit Sie es in IEnumUnknown umwandeln können, wenn Sie es im Parameter *ppIEnumMetadata* zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9502e-131">The enumeration object must implement [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) so you can cast it to IEnumUnknown when you return it in the *ppIEnumMetadata* parameter.</span></span>

<span data-ttu-id="9502e-132">Beim Implementieren des enumerationsobjektobjekts können Sie alle metadatenleser erstellen, wenn Sie das [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) -Objekt erstmalig erstellen, oder wenn Sie das Enumerationsobjekt erstmalig erstellen, oder Sie können es verzögert innerhalb der Implementierung der [IEnumUnknown:: Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) -Methode erstellen.</span><span class="sxs-lookup"><span data-stu-id="9502e-132">When implementing the enumeration object, you can create all the metadata readers when you first create the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object or when you first create the enumeration object, or you can create them lazily inside the implementation of the [IEnumUnknown::Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) method.</span></span> <span data-ttu-id="9502e-133">In vielen Fällen ist es effizienter, Sie verzögert zu erstellen, aber im folgenden Beispiel werden alle Block Leser im Konstruktor erstellt, um Speicherplatz zu sparen.</span><span class="sxs-lookup"><span data-stu-id="9502e-133">In many cases, it’s more efficient to create them lazily but, in the following example, the block readers are all created in the constructor to save space.</span></span>


```C++
public class MetadataReaderEnumerator : public IEnumUnknown
{
   UINT m_current;
   UINT m_blockCount;
   IWICMetadataReader** m_ppMetadataReader;
   IStream* m_pStream;

   MetadataReaderEnumerator() 
   {
       // Set m_blockCount to the number of metadata blocks in the frame. 
      ...
      m_ppMetadataReader = IWICMetadataReader*[m_blockCount];
       m_current = 0;

      for (UINT x=0; x < m_blockCount; x++) 
      {
         // Find the position in the file where the xth
         // block of metadata lives and seek m_piStream 
         // to that position.
         ...

         m_pComponentFactory->CreateMetadataReaderFromContainer(
            GUID_ContainerFormatTiff,
                        NULL,
                        WICPersistOptions.WICPersistOptionsDefault | 
            WICMetadataCreationOptions.WICMetadataCreationDefault, 
                        m_pStream, &m_ppMetadataReader[x]);
        }
    }

    // Implementation of IEnumUnknown and IUnknown interfaces
    ...
}
```



<span data-ttu-id="9502e-134">Um die metadatenleser zu erstellen, verwenden Sie die [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9502e-134">To create the metadata readers, you use the [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) method.</span></span> <span data-ttu-id="9502e-135">Wenn Sie diese Methode aufrufen, übergeben Sie die GUID des Container Formats im *guidContainerFormat* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="9502e-135">When invoking this method, you pass in the GUID of the container format in the *guidContainerFormat* parameter.</span></span> <span data-ttu-id="9502e-136">Wenn Sie den Anbieter für einen metadatenleser bevorzugen, können Sie die GUID Ihres bevorzugten Anbieters im *pguidVendor* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="9502e-136">If you have a preference of vendor for a metadata reader, you can pass the GUID of your preferred vendor in the *pGuidVendor* parameter.</span></span> <span data-ttu-id="9502e-137">Wenn Ihr Unternehmen beispielsweise Metadatenhandler schreibt und Sie Ihre eigenen, falls vorhanden, verwenden möchten, können Sie die GUID des Anbieters übergeben.</span><span class="sxs-lookup"><span data-stu-id="9502e-137">For example, if your company writes metadata handlers, and you want to use your own if present, you can pass in your vendor GUID.</span></span> <span data-ttu-id="9502e-138">In den meisten Fällen würden Sie einfach **null** übergeben und es dem System ermöglichen, den passenden metadatenreader auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="9502e-138">In most cases, you would just pass **NULL**, and let the system select the appropriate metadata reader.</span></span> <span data-ttu-id="9502e-139">Wenn Sie einen bestimmten Anbieter anfordern und der Anbieter einen metadatenleser auf dem Computer installiert hat, gibt WIC den Leser dieses Anbieters zurück.</span><span class="sxs-lookup"><span data-stu-id="9502e-139">If you do request a specific vendor, and that vendor does have a metadata reader installed on the computer, WIC will return that vendor’s reader.</span></span> <span data-ttu-id="9502e-140">Wenn der angeforderte Anbieter jedoch keinen metadatenleser auf dem Computer installiert hat und ein entsprechender metadatenleser verfügbar ist, wird dieser Reader zurückgegeben, auch wenn er nicht vom bevorzugten Anbieter ist.</span><span class="sxs-lookup"><span data-stu-id="9502e-140">However, if the requested vendor does not have a metadata reader installed on the computer, and if there is an appropriate metadata reader available, that reader will be returned even though it is not from the preferred vendor.</span></span> <span data-ttu-id="9502e-141">Wenn auf dem Computer kein metadatenleser für den Typ der Metadaten im-Block vorhanden ist, gibt die komponentenfactory den unbekannten Metadatenhandler zurück, der den Metadatenblock als Binary Large Object (BLOB) behandelt und den Metadatenblock aus der Datei deserialisiert, ohne dass versucht wird, ihn zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="9502e-141">If there is no metadata reader on the computer for the type of metadata in the block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB), and will deserialize the block of metadata from the file without any attempt at parsing it.</span></span>

<span data-ttu-id="9502e-142">Führen Sie für den *dwOptions* -Parameter eine OR-Operation zwischen den entsprechenden [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) -Vorgängen mit der entsprechenden [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)aus.</span><span class="sxs-lookup"><span data-stu-id="9502e-142">For the *dwOptions* parameter, perform an OR operation between the appropriate [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) with the appropriate [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions).</span></span> <span data-ttu-id="9502e-143">Die **WICPersistOptions** beschreiben, wie Ihr Container angelegt wird. Der Standardwert ist Little--in.</span><span class="sxs-lookup"><span data-stu-id="9502e-143">The **WICPersistOptions** describe how your container is laid out. Little-endian is the default.</span></span>

``` syntax
enum WICPersistOptions
{   
   WICPersistOptionDefault,
   WICPersistOptionLittleEndian,
   WICPersistOptionBigEndian,
   WICPersistOptionStrictFormat,
   WICPersistOptionNoCacheStream,
   WICPersistOptionPreferUTF8
};
```

<span data-ttu-id="9502e-144">[**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) geben Sie an, ob Sie den UnknownMetadataHandler zurückerhalten möchten, wenn auf dem Computer kein metadatenleser gefunden wird, der das Metadatenformat eines bestimmten Blocks lesen kann.</span><span class="sxs-lookup"><span data-stu-id="9502e-144">The [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) specify whether you want to get back the UnknownMetadataHandler if no metadata reader is found on the machine that can read the metadata format of a particular block.</span></span> <span data-ttu-id="9502e-145">**WICMetadataCreationAllowUnknown** ist die Standardeinstellung, und Sie sollten immer die Erstellung des UnknownMetadtataHandler zulassen.</span><span class="sxs-lookup"><span data-stu-id="9502e-145">**WICMetadataCreationAllowUnknown** is the default, and you should always allow creation of the UnknownMetadtataHandler.</span></span> <span data-ttu-id="9502e-146">Der UnknownMetadataHandler behandelt nicht erkannte Metadaten als BLOB.</span><span class="sxs-lookup"><span data-stu-id="9502e-146">The UnknownMetadataHandler treats unrecognized metadata as a BLOB.</span></span> <span data-ttu-id="9502e-147">Sie kann Sie nicht analysieren, sondern schreibt Sie als BLOB in den Stream und speichert sie intakt, wenn Sie während der Codierung in den Stream zurückgeschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="9502e-147">It cannot parse it, but it writes it out into the stream as a BLOB, and persists it intact when it’s written back to the stream during encoding.</span></span> <span data-ttu-id="9502e-148">Dadurch ist es sicher, Metadatenhandler für proprietäre Metadaten oder Metadatenformate zu erstellen, die nicht mit dem System ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="9502e-148">This makes it safe to create metadata handlers for proprietary metadata or metadata formats that don’t ship with the system.</span></span> <span data-ttu-id="9502e-149">Da Metadaten intakt bleiben, sind die Metadaten weiterhin vorhanden und können gelesen werden, auch wenn kein Handler auf dem Computer vorhanden ist, der Sie erkennt, wenn ein entsprechender Metadatenhandler später installiert wird.</span><span class="sxs-lookup"><span data-stu-id="9502e-149">Because metadata is preserved intact, even if no handler is present on the computer that recognizes it, when an appropriate metadata handler is later installed, the metadata will still be there and can be read.</span></span> <span data-ttu-id="9502e-150">Wenn Sie die Erstellung des UnknownMetadataHandler nicht zulassen, besteht die Alternative darin, nicht erkannte Metadaten zu verwerfen oder zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="9502e-150">If you don’t allow creation of the UnknownMetadataHandler, the alternative is discarding or overwriting unrecognized metadata.</span></span> <span data-ttu-id="9502e-151">Dies ist eine Form von Datenverlusten.</span><span class="sxs-lookup"><span data-stu-id="9502e-151">This is a form of data loss.</span></span>

> [!Note]  
> <span data-ttu-id="9502e-152">Wenn Sie einen eigenen Metadatenhandler für proprietäre Metadaten schreiben, sollten Sie keine Verweise auf etwas außerhalb des Metadatenblocks selbst einschließen.</span><span class="sxs-lookup"><span data-stu-id="9502e-152">If you write your own metadata handler for proprietary metadata, you should never include references to anything outside the metadata block itself.</span></span> <span data-ttu-id="9502e-153">Obwohl UnknownMetadataHandler die Metadaten intakt behält, werden die Metadaten beim Bearbeiten von Dateien verschoben, und alle Verweise auf Elemente außerhalb des eigenen Blocks sind in diesem Fall nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="9502e-153">Even though the UnknownMetadataHandler preserves metadata intact, metadata does get moved when files are edited, and any references to anything outside its own block will no longer be valid when this happens.</span></span>

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

<span data-ttu-id="9502e-154">Der *pIStream* -Parameter ist der tatsächliche Datenstrom, den Sie decodieren.</span><span class="sxs-lookup"><span data-stu-id="9502e-154">The *pIStream* parameter is the actual stream that you are decoding.</span></span> <span data-ttu-id="9502e-155">Bevor Sie den Stream übergeben, sollten Sie am Anfang des Metadatenblocks suchen, für den Sie einen Reader anfordern.</span><span class="sxs-lookup"><span data-stu-id="9502e-155">Before passing in the stream, you should seek to the beginning of the metadata block for which you’re requesting a reader.</span></span> <span data-ttu-id="9502e-156">Der entsprechende metadatenleser für den Metadatenblock an der aktuellen Position im [IStream](/windows/desktop/api/objidl/nn-objidl-istream) wird im *ppiReader* -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9502e-156">The appropriate metadata reader for the metadata block at the current position in the [IStream](/windows/desktop/api/objidl/nn-objidl-istream) will be returned in the *ppiReader* parameter.</span></span>

### <a name="getreaderbyindex"></a><span data-ttu-id="9502e-157">GetReaderByIndex</span><span class="sxs-lookup"><span data-stu-id="9502e-157">GetReaderByIndex</span></span>

<span data-ttu-id="9502e-158">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) gibt den metadatenreader am angeforderten Index in der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="9502e-158">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) returns the metadata reader at the requested index in the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9502e-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9502e-159">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9502e-160">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="9502e-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9502e-161">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="9502e-161">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="9502e-162">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9502e-162">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9502e-163">Implementieren von IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="9502e-163">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="9502e-164">Implementieren von IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="9502e-164">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="9502e-165">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="9502e-165">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="9502e-166">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="9502e-166">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
