---
description: 'Weitere Informationen finden Sie unter: Implementieren eines WIC-Enabled Decoders'
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implementieren eines WIC-Enabled Decoders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866763"
---
# <a name="implementing-a-wic-enabled-decoder"></a><span data-ttu-id="fa9de-103">Implementieren eines WIC-Enabled Decoders</span><span class="sxs-lookup"><span data-stu-id="fa9de-103">Implementing a WIC-Enabled Decoder</span></span>


<span data-ttu-id="fa9de-104">Zum Implementieren eines WIC-Decoders (Windows Imaging Component) müssen zwei Klassen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fa9de-104">Implementing a Windows Imaging Component (WIC) decoder requires writing two classes.</span></span> <span data-ttu-id="fa9de-105">Die Schnittstellen für diese Klassen entsprechen direkt den Decoder-Zuständigkeiten, die im Abschnitt [decodieren](-wic-howwicworks.md) der [Funktionsweise der Windows-Abbild](-wic-howwicworks.md)Erstellungs Komponente beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fa9de-105">The interfaces on these classes correspond directly to the decoder responsibilities outlined in the [Decoding](-wic-howwicworks.md) section of [How The Windows Imaging Component Works](-wic-howwicworks.md).</span></span>

<span data-ttu-id="fa9de-106">Eine der-Klassen stellt Dienste auf Container Ebene bereit und implementiert die [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fa9de-106">One of the classes provides container-level services and implements the [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) interface.</span></span> <span data-ttu-id="fa9de-107">Wenn Ihr Bildformat Metadaten auf Container Ebene unterstützt, müssen Sie auch die [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) -Schnittstelle für diese Klasse implementieren.</span><span class="sxs-lookup"><span data-stu-id="fa9de-107">If your image format supports container-level metadata, you must also implement the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface on this class.</span></span> <span data-ttu-id="fa9de-108">Es wird empfohlen, dass Sie die [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) -Schnittstelle sowohl für den Decoder als auch für den Encoder unterstützen, um eine bessere Benutzeroberfläche zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fa9de-108">It is recommended that you support the [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) interface on both the decoder and encoder to support a better user experience.</span></span>

<span data-ttu-id="fa9de-109">Die andere Klasse, die Sie implementieren, stellt Dienste auf Frame-Ebene bereit und führt die eigentliche Decodierung der Bildbits für jeden Frame im Container aus.</span><span class="sxs-lookup"><span data-stu-id="fa9de-109">The other class you will implement provides frame-level services and does the actual decoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="fa9de-110">Diese Klasse implementiert die [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) -Schnittstelle und die [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fa9de-110">This class implements the [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) interface and the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface.</span></span> <span data-ttu-id="fa9de-111">Wenn Sie einen Decoder für ein Rohdaten Format schreiben, implementieren Sie auch die [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) -Schnittstelle für diese Klasse.</span><span class="sxs-lookup"><span data-stu-id="fa9de-111">If you are writing a decoder for a raw format, you also implement the [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) interface on this class.</span></span> <span data-ttu-id="fa9de-112">Zusätzlich zu den erforderlichen Schnittstellen wird dringend empfohlen, dass Sie die [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) -Schnittstelle für diese Klasse implementieren, um die bestmögliche Leistung für Ihr Bildformat zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="fa9de-112">In addition to the required interfaces, it is highly recommended that you implement the [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) interface on this class to enable the best possible performance for your image format.</span></span>

<span data-ttu-id="fa9de-113">Eines der-Objekte, die von WIC bereitgestellt werden, ist die [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="fa9de-113">One of the objects provided by WIC is the [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span> <span data-ttu-id="fa9de-114">Häufig verwenden Sie die [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) -Schnittstelle für dieses Objekt, um verschiedene Komponenten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa9de-114">You frequently use the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) interface on this object to create various components.</span></span> <span data-ttu-id="fa9de-115">Da Sie häufig verwendet wird, sollten Sie einen Verweis darauf als Element Eigenschaft in den Decoder-und Encoder-Klassen speichern.</span><span class="sxs-lookup"><span data-stu-id="fa9de-115">Because it is used frequently, you should keep a reference to it as a member property on both your decoder and encoder classes.</span></span>


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a><span data-ttu-id="fa9de-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fa9de-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fa9de-117">**Licher**</span><span class="sxs-lookup"><span data-stu-id="fa9de-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fa9de-118">Funktionsweise der Windows-Abbild Erstellungs Komponente</span><span class="sxs-lookup"><span data-stu-id="fa9de-118">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

[<span data-ttu-id="fa9de-119">Decoder-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="fa9de-119">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="fa9de-120">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="fa9de-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="fa9de-121">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="fa9de-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="fa9de-122">Übersicht über WIC-Metadaten</span><span class="sxs-lookup"><span data-stu-id="fa9de-122">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="fa9de-123">Übersicht über die Codierung</span><span class="sxs-lookup"><span data-stu-id="fa9de-123">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> </dl>

 

 



