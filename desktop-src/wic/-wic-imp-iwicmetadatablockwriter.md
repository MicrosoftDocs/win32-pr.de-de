---
description: Implementieren von IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implementieren von IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530269"
---
# <a name="implementing-iwicmetadatablockwriter"></a><span data-ttu-id="c0af8-103">Implementieren von IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="c0af8-103">Implementing IWICMetadataBlockWriter</span></span>

## <a name="iwicmetadatablockwriter"></a><span data-ttu-id="c0af8-104">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="c0af8-104">IWICMetadataBlockWriter</span></span>

-   [<span data-ttu-id="c0af8-105">InitializeFromBlockReader</span><span class="sxs-lookup"><span data-stu-id="c0af8-105">InitializeFromBlockReader</span></span>](#initializefromblockreader)
-   [<span data-ttu-id="c0af8-106">"Getschreiterbyindex"</span><span class="sxs-lookup"><span data-stu-id="c0af8-106">GetWriterByIndex</span></span>](#getwriterbyindex)
-   [<span data-ttu-id="c0af8-107">AddWriter</span><span class="sxs-lookup"><span data-stu-id="c0af8-107">AddWriter</span></span>](#addwriter)
-   [<span data-ttu-id="c0af8-108">Setschreiterbyindex</span><span class="sxs-lookup"><span data-stu-id="c0af8-108">SetWriterByIndex</span></span>](#setwriterbyindex)
-   [<span data-ttu-id="c0af8-109">Removeschreiterbyindex</span><span class="sxs-lookup"><span data-stu-id="c0af8-109">RemoveWriterByIndex</span></span>](#removewriterbyindex)

<span data-ttu-id="c0af8-110">Die Codierungs Klasse auf Frame-Ebene implementiert diese Schnittstelle, um alle Metadatenblöcke verfügbar zu machen und den entsprechenden metadatenwriter für jeden Block anzufordern.</span><span class="sxs-lookup"><span data-stu-id="c0af8-110">The frame-level encoding class implements this interface to expose all the metadata blocks and request the appropriate metadata writer for each block.</span></span> <span data-ttu-id="c0af8-111">Wenn Ihr Bildformat globale Metadaten außerhalb eines einzelnen Frames unterstützt, sollten Sie diese Schnittstelle auch in der Encoder-Klasse auf Container-Ebene implementieren.</span><span class="sxs-lookup"><span data-stu-id="c0af8-111">If your image format supports global metadata, outside of any individual frame, you should also implement this interface on the container-level encoder class.</span></span> <span data-ttu-id="c0af8-112">Eine ausführlichere Erläuterung von metadatenhandlern finden Sie im Abschnitt [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) im Abschnitt über die Implementierung eines WIC-Enabled Decoders.</span><span class="sxs-lookup"><span data-stu-id="c0af8-112">For a more detailed discussion of metadata handlers, refer to the section on the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the section on Implementing a WIC-Enabled Decoder.</span></span>

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a><span data-ttu-id="c0af8-113">InitializeFromBlockReader</span><span class="sxs-lookup"><span data-stu-id="c0af8-113">InitializeFromBlockReader</span></span>

<span data-ttu-id="c0af8-114">[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) verwendet ein [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) , um den blockwriter zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="c0af8-114">[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) uses an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) to initialize the block writer.</span></span> <span data-ttu-id="c0af8-115">Sie können den **IWICMetadataBlockReader** aus dem Decoder, der das Bild decodiert hat, erhalten.</span><span class="sxs-lookup"><span data-stu-id="c0af8-115">You can get the **IWICMetadataBlockReader** from the decoder that decoded the image.</span></span>


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



<span data-ttu-id="c0af8-116">Da die Initialisierung des [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) mit einem [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) einen metadatenwriter für jeden metadatenreader instanziiert, der vom **IWICMetadataBlockReader** -Objekt verfügbar gemacht wird, muss die Anwendung einen Writer nicht explizit für jeden Metadatenblock anfordern.</span><span class="sxs-lookup"><span data-stu-id="c0af8-116">Because initializing the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) with an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) instantiates a metadata writer for each metadata reader exposed by the **IWICMetadataBlockReader** object, the application doesn’t have to explicitly request a writer for each block of metadata.</span></span>

### <a name="getwriterbyindex"></a><span data-ttu-id="c0af8-117">"Getschreiterbyindex"</span><span class="sxs-lookup"><span data-stu-id="c0af8-117">GetWriterByIndex</span></span>

<span data-ttu-id="c0af8-118">[**Getschreiterbyindex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) gibt das [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) -Objekt für den ten-Metadatenblock zurück, wobei n der Wert ist, der im *nIndex* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c0af8-118">[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) returns the [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) object for the nth metadata block, where n is the value passed in the *nIndex* parameter.</span></span> <span data-ttu-id="c0af8-119">Wenn kein metadatenwriter registriert ist, der den Typ der Metadaten im ten-Block verarbeiten kann, gibt die komponentenfactory den unbekannten Metadatenhandler zurück, der den Metadatenblock als Binary Large Object (BLOB) behandelt.</span><span class="sxs-lookup"><span data-stu-id="c0af8-119">If there is no metadata writer registered that can handle the type of metadata in the nth block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB).</span></span> <span data-ttu-id="c0af8-120">Sie wird als Bitstream serialisiert, ohne zu versuchen, Sie zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="c0af8-120">It will serialize it out as a bit stream without attempting to parse it.</span></span>

### <a name="addwriter"></a><span data-ttu-id="c0af8-121">AddWriter</span><span class="sxs-lookup"><span data-stu-id="c0af8-121">AddWriter</span></span>

<span data-ttu-id="c0af8-122">[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) ermöglicht einem Aufrufer, einen neuen metadatenwriter hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c0af8-122">[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) allows a caller to add a new metadata writer.</span></span> <span data-ttu-id="c0af8-123">Dies ist erforderlich, wenn eine Anwendung Metadaten eines anderen Formats als einen der vorhandenen Metadatenblöcke hinzufügen möchte.</span><span class="sxs-lookup"><span data-stu-id="c0af8-123">This is required if an application wants to add metadata of a different format than any of the existing metadata blocks.</span></span> <span data-ttu-id="c0af8-124">Beispielsweise kann eine Anwendung einige XMP-Metadaten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c0af8-124">For example, an application may want to add some XMP metadata.</span></span> <span data-ttu-id="c0af8-125">Wenn kein vorhandener XMP-Metadatenblock vorhanden ist, muss die Anwendung einen XMP-metadatenwriter instanziieren und die **AddWriter** -Methode verwenden, um Sie in die Auflistung von metadatenwritern einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="c0af8-125">If there is no existing XMP metadata block, the application must instantiate an XMP metadata writer and use the **AddWriter** method to include it in the collection of metadata writers.</span></span>

### <a name="setwriterbyindex"></a><span data-ttu-id="c0af8-126">Setschreiterbyindex</span><span class="sxs-lookup"><span data-stu-id="c0af8-126">SetWriterByIndex</span></span>

<span data-ttu-id="c0af8-127">[**Setschreiterbyindex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) wird verwendet, um einen metadatenwriter an einem bestimmten Index in der Auflistung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c0af8-127">[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) is used to add a metadata writer at a specific index in the collection.</span></span> <span data-ttu-id="c0af8-128">Wenn ein metadatenwriter derzeit an diesem Index vorhanden ist, sollte der neue einen metadatenwriter ersetzen.</span><span class="sxs-lookup"><span data-stu-id="c0af8-128">If a metadata writer is currently exists at that index, the new one should replace it.</span></span>

### <a name="removewriterbyindex"></a><span data-ttu-id="c0af8-129">Removeschreiterbyindex</span><span class="sxs-lookup"><span data-stu-id="c0af8-129">RemoveWriterByIndex</span></span>

<span data-ttu-id="c0af8-130">[**Removeschreiterbyindex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) wird verwendet, um einen metadatenwriter aus der Auflistung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c0af8-130">[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) is used to remove a metadata writer from the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0af8-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c0af8-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c0af8-132">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c0af8-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c0af8-133">Implementieren von iwicbitmapframecocode</span><span class="sxs-lookup"><span data-stu-id="c0af8-133">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="c0af8-134">Codec-Installation und-Registrierung</span><span class="sxs-lookup"><span data-stu-id="c0af8-134">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="c0af8-135">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="c0af8-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="c0af8-136">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="c0af8-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



