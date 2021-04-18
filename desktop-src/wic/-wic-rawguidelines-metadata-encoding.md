---
description: Codierung
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Codierung (Windows Imaging-Komponente)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6d15b983b7455d0fe0c406cbad64dbbb77588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350800"
---
# <a name="encoding-windows-imaging-component"></a><span data-ttu-id="fec7d-103">Codierung (Windows Imaging-Komponente)</span><span class="sxs-lookup"><span data-stu-id="fec7d-103">Encoding (Windows Imaging Component)</span></span>

<span data-ttu-id="fec7d-104">Der codierautor muss folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="fec7d-104">The encoder author must do the following:</span></span>

-   <span data-ttu-id="fec7d-105">Implementieren Sie die [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) -Schnittstelle und die [**iwicbitmapframekocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fec7d-105">Implement [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) interfaces.</span></span>
-   <span data-ttu-id="fec7d-106">Implementieren Sie [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) auf dem Frame Encoder.</span><span class="sxs-lookup"><span data-stu-id="fec7d-106">Implement [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on the frame encoder.</span></span> <span data-ttu-id="fec7d-107">Wenn der Codec Metadaten auf Container Ebene unterstützt, muss diese Schnittstelle sowohl für den Encoder auf Container Ebene als auch für den Frame Encoder implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="fec7d-107">If the codec supports container-level metadata, this interface must be implemented on the container-level encoder as well as on the frame encoder.</span></span>
-   <span data-ttu-id="fec7d-108">Wenn das Containerformat implizit irgendwelche obligatorischen Metadatenblöcke enthält, instanziieren Sie einen metadatenwriter für jeden dieser Blöcke.</span><span class="sxs-lookup"><span data-stu-id="fec7d-108">If the container format implicitly contains any mandatory metadata blocks, instantiate a metadata writer for each such block.</span></span> <span data-ttu-id="fec7d-109">Beispielsweise erfordert das TIFF-Format für jeden Frame ein Schnittstellen Gerät (IFD), sodass der IFD-Writer immer verfügbar gemacht werden muss.</span><span class="sxs-lookup"><span data-stu-id="fec7d-109">For example, the TIFF format requires an interface device (IFD) for each frame, so the IFD writer must always be exposed.</span></span>
-   <span data-ttu-id="fec7d-110">Implementieren Sie Unterstützung für die Verwaltung der Auflistung von metadatenwritern.</span><span class="sxs-lookup"><span data-stu-id="fec7d-110">Implement support for managing the collection of metadata writers.</span></span> <span data-ttu-id="fec7d-111">Der blockwriter verwaltet alle Bestell Anforderungen oder Container Beschränkungen für die Arten von metadatenblöcken, die codiert werden können.</span><span class="sxs-lookup"><span data-stu-id="fec7d-111">The block writer manages any order requirements or container restrictions on the kinds of metadata blocks that can be encoded.</span></span> <span data-ttu-id="fec7d-112">Der blockwriter muss überprüfen, ob alle neuen metadatenwriter innerhalb des Container Formats eingebettet werden können.</span><span class="sxs-lookup"><span data-stu-id="fec7d-112">The block writer must verify that any new metadata writers can be embedded within the container format.</span></span>
-   <span data-ttu-id="fec7d-113">Beim Codieren des bildstreams wird [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) aufgerufen, um den Inhalt jedes metadatenwriters in den Stream zu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="fec7d-113">When encoding the image stream, call [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) to serialize each metadata writer’s content into the stream.</span></span> <span data-ttu-id="fec7d-114">Wenn der Metadatenblock "Critical"-Metadaten enthält, muss der Encoder die kritischen Metadatenelemente festlegen, bevor er den metadatenwriter anfordert, Inhalte zu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="fec7d-114">If the metadata block contains "critical" metadata the encoder must set the critical metadata items before asking the metadata writer to serialize content.</span></span>
-   <span data-ttu-id="fec7d-115">Suchen Sie nach unbekannten metadatenhandlern, um sicherzustellen, dass redundante Metadatenblöcke nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="fec7d-115">Check for any unknown metadata handlers to ensure that redundant metadata blocks are not present.</span></span> <span data-ttu-id="fec7d-116">Dies ist wichtig, da bei der Beibehaltung von Metadaten in einem decodieren oder Codieren von Szenarien unbekannte Blöcke möglicherweise ein Duplikat erforderlicher Metadatenblöcke sind.</span><span class="sxs-lookup"><span data-stu-id="fec7d-116">This is important because, while preserving metadata in a decode or encode scenario, unknown blocks might be a duplicate of mandatory metadata blocks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fec7d-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fec7d-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fec7d-118">**Licher**</span><span class="sxs-lookup"><span data-stu-id="fec7d-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fec7d-119">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="fec7d-119">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="fec7d-120">WIC-Richtlinien für Kamera Rohbild Formate</span><span class="sxs-lookup"><span data-stu-id="fec7d-120">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="fec7d-121">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="fec7d-121">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



