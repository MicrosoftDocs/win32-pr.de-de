---
description: Senkenwriter-Attribute
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Senkenwriter-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130469"
---
# <a name="sink-writer-attributes"></a><span data-ttu-id="c6280-103">Senkenwriter-Attribute</span><span class="sxs-lookup"><span data-stu-id="c6280-103">Sink Writer Attributes</span></span>

<span data-ttu-id="c6280-104">Die folgenden Attribute können verwendet werden, um den senkenwriter zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="c6280-104">The following attributes can be used to initialize the sink writer.</span></span>



| <span data-ttu-id="c6280-105">Attribut</span><span class="sxs-lookup"><span data-stu-id="c6280-105">Attribute</span></span>                                                                                  | <span data-ttu-id="c6280-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6280-106">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6280-107">MF mit \_ niedriger \_ Latenz</span><span class="sxs-lookup"><span data-stu-id="c6280-107">MF\_LOW\_LATENCY</span></span>](mf-low-latency.md)                                                     | <span data-ttu-id="c6280-108">Ermöglicht die Verarbeitung mit niedriger Latenz.</span><span class="sxs-lookup"><span data-stu-id="c6280-108">Enables low-latency processing.</span></span>                                                                                                                                                                                                    |
| [<span data-ttu-id="c6280-109">MF- \_ Lese Schreibvorgänge \_ Deaktivieren \_</span><span class="sxs-lookup"><span data-stu-id="c6280-109">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)                  | <span data-ttu-id="c6280-110">Aktiviert oder deaktiviert Formatkonvertierungen durch den senkenwriter.</span><span class="sxs-lookup"><span data-stu-id="c6280-110">Enables or disables format conversions by the sink writer.</span></span>                                                                                                                                                                         |
| [<span data-ttu-id="c6280-111">MF- \_ Lese schreiben \_ Aktivieren von \_ Hardware \_ Transformationen</span><span class="sxs-lookup"><span data-stu-id="c6280-111">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS</span></span>](mf-readwrite-enable-hardware-transforms.md) | <span data-ttu-id="c6280-112">Ermöglicht es dem senkenwriter, hardwarebasierte Media Foundation Transformationen (MFTs) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6280-112">Enables the sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>                                                                                                                                                  |
| [<span data-ttu-id="c6280-113">asynchroner Rückruf für den MF- \_ Senke \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c6280-113">MF\_SINK\_WRITER\_ASYNC\_CALLBACK</span></span>](mf-sink-writer-async-callback.md)                     | <span data-ttu-id="c6280-114">Enthält einen Zeiger auf die Rückruf Schnittstelle der Anwendung für den Senke-Writer.</span><span class="sxs-lookup"><span data-stu-id="c6280-114">Contains a pointer to the application's callback interface for the sink writer.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="c6280-115">MF- \_ Sink- \_ Writer Deaktivieren der \_ \_ Drosselung</span><span class="sxs-lookup"><span data-stu-id="c6280-115">MF\_SINK\_WRITER\_DISABLE\_THROTTLING</span></span>](mf-sink-writer-disable-throttling.md)             | <span data-ttu-id="c6280-116">Gibt an, ob der senderwriter die Rate eingehender Daten einschränkt.</span><span class="sxs-lookup"><span data-stu-id="c6280-116">Specifies whether the sink writer limits the rate of incoming data.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="c6280-117">MF- \_ transcode- \_ ContainerType</span><span class="sxs-lookup"><span data-stu-id="c6280-117">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                             | <span data-ttu-id="c6280-118">Gibt den Containertyp der Ausgabedatei an.</span><span class="sxs-lookup"><span data-stu-id="c6280-118">Specifies the container type of the output file.</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="c6280-119">MFT \_ fieldofuse \_ Unlock- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="c6280-119">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)                  | <span data-ttu-id="c6280-120">Enthält einen [**imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Zeiger, der verwendet wird, um ein MFT mit Einschränkungen für das Feld zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="c6280-120">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which is used to unlock an MFT with field-of-use restrictions.</span></span> <span data-ttu-id="c6280-121">Weitere Informationen finden Sie unter [Einschränkungen](field-of-use-restrictions.md)für das Feld "Verwendung".</span><span class="sxs-lookup"><span data-stu-id="c6280-121">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> |
| [<span data-ttu-id="c6280-122">MF \_ Sink \_ Writer \_ D3D \_ Manager</span><span class="sxs-lookup"><span data-stu-id="c6280-122">MF\_SINK\_WRITER\_D3D\_MANAGER</span></span>](mf-sink-writer-d3d-manager.md)                           | <span data-ttu-id="c6280-123">Verwenden Sie dieses Attribut, um ein Direct3D-Gerät für alle Video Encoder oder Medien senken bereitzustellen, die vom senkenwriter geladen werden.</span><span class="sxs-lookup"><span data-stu-id="c6280-123">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the sink writer.</span></span>                                                                                                                   |



 

<span data-ttu-id="c6280-124">Verwenden Sie diese Attribute mit den folgenden Methoden und Funktionen:</span><span class="sxs-lookup"><span data-stu-id="c6280-124">Use these attributes with the following methods and functions:</span></span>

-   [<span data-ttu-id="c6280-125">**Imfreadschreiteclassfactory:: kreateinstancefromuject**</span><span class="sxs-lookup"><span data-stu-id="c6280-125">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [<span data-ttu-id="c6280-126">**Imfreadschreiteclassfactory:: forateinstancefromurl**</span><span class="sxs-lookup"><span data-stu-id="c6280-126">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [<span data-ttu-id="c6280-127">**Mfkreatesinkschreiterfrommediasink**</span><span class="sxs-lookup"><span data-stu-id="c6280-127">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="c6280-128">**MF | atesinkschreiterfromurl**</span><span class="sxs-lookup"><span data-stu-id="c6280-128">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="c6280-129">Um eines dieser Attribute zu verwenden, rufen Sie zuerst [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen neuen Attribut Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6280-129">To use any of these attributes, first call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span> <span data-ttu-id="c6280-130">Verwenden Sie dann die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle, um die gewünschten Attribute im Attribut Speicher festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c6280-130">Then use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface to set the desired attributes on the attribute store.</span></span> <span data-ttu-id="c6280-131">Übergeben Sie den **imfattributes** -Zeiger an den *pattributes* -Parameter einer der zuvor aufgeführten Methoden oder Funktionen.</span><span class="sxs-lookup"><span data-stu-id="c6280-131">Pass the **IMFAttributes** pointer to the *pAttributes* parameter of any of the methods or functions listed previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6280-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6280-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6280-133">**Imbersink Writer**</span><span class="sxs-lookup"><span data-stu-id="c6280-133">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="c6280-134">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c6280-134">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



