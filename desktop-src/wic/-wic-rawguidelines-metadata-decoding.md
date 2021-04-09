---
description: Decodierung
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Decodierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6700865d55ba7349447f5e41285d60446f0e4630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867319"
---
# <a name="decoding"></a><span data-ttu-id="321da-103">Decodierung</span><span class="sxs-lookup"><span data-stu-id="321da-103">Decoding</span></span>

<span data-ttu-id="321da-104">Um Metadaten ordnungsgemäß zu unterstützen, müssen Decoder-Autoren folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="321da-104">To properly support metadata, decoder authors must do the following:</span></span>

-   <span data-ttu-id="321da-105">Implementieren Sie die [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -und [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="321da-105">Implement [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interfaces.</span></span>
-   <span data-ttu-id="321da-106">Implementieren Sie [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) auf dem Frame-Decoder.</span><span class="sxs-lookup"><span data-stu-id="321da-106">Implement [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on the frame decoder.</span></span> <span data-ttu-id="321da-107">Wenn der Codec Metadaten auf Container Ebene unterstützt, muss diese Schnittstelle sowohl für den Decoder auf Container Ebene als auch für den Frame Decoder implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="321da-107">If the codec supports container-level metadata, this interface must be implemented on the container-level decoder as well as on the frame decoder.</span></span>
-   <span data-ttu-id="321da-108">Beim Decodieren des bildstreams muss [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) aufgerufen werden, um einen metadatenreader für jeden Metadatenblock zu instanziieren.</span><span class="sxs-lookup"><span data-stu-id="321da-108">While decoding the image stream, call [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) to instantiate a metadata reader for each metadata block.</span></span> <span data-ttu-id="321da-109">(Alle neuen metadatenleser, die der Codec implementiert, müssen bei WIC registriert werden.)</span><span class="sxs-lookup"><span data-stu-id="321da-109">(Any new metadata readers that the codec implements must be registered with WIC.)</span></span>

    <span data-ttu-id="321da-110">Der Decoder sollte keine eigenen metadatenleser erstellen, sondern stattdessen WIC verwenden, um Sie basierend auf den metadatenblöcken im Datenstrom zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="321da-110">The decoder should not create metadata readers on its own, but rather use WIC to create them based on the metadata blocks in the stream.</span></span> <span data-ttu-id="321da-111">Der Decoder muss dies für alle gefundenen Blöcke ausführen, auch wenn Sie dem docoder nicht nativ bekannt sind, da zukünftige metadatenleser möglicherweise auf dem System installiert sind, die verstehen, wie diese Metadatenblöcke behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="321da-111">The decoder must do this on all blocks that it finds, even if they are not natively known to the docoder, because future metadata readers might be installed on the system that do understand how to handle these metadata blocks.</span></span>

-   <span data-ttu-id="321da-112">Wenn kein Metadatenhandler für einen-Block vorhanden ist, instanziieren Sie den unbekannten metadatenreader, indem Sie die Optionen für die Metadatenerstellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="321da-112">If there is no metadata handler for a block, instantiate the unknown metadata reader by using the metadata creation options.</span></span>
-   <span data-ttu-id="321da-113">Machen Sie die Auflistung von metadatenlesern über die [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="321da-113">Expose the collection of metadata readers through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="321da-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="321da-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="321da-115">**Licher**</span><span class="sxs-lookup"><span data-stu-id="321da-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="321da-116">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="321da-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="321da-117">WIC-Richtlinien für Kamera Rohbild Formate</span><span class="sxs-lookup"><span data-stu-id="321da-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="321da-118">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="321da-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



