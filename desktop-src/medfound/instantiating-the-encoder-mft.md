---
description: Instanziieren eines MFT-Encoders
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: Instanziieren eines MFT-Encoders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5344c19a3a00c659efbbfd88d42176b876528380
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217032"
---
# <a name="instantiating-an-encoder-mft"></a><span data-ttu-id="2f873-103">Instanziieren eines MFT-Encoders</span><span class="sxs-lookup"><span data-stu-id="2f873-103">Instantiating an Encoder MFT</span></span>

<span data-ttu-id="2f873-104">In Microsoft Media Foundation werden Encoder als [Media Foundation Transformationen](media-foundation-transforms.md) (MFTs) implementiert.</span><span class="sxs-lookup"><span data-stu-id="2f873-104">In Microsoft Media Foundation, encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs).</span></span> <span data-ttu-id="2f873-105">Bevor Sie einen Encoder erstellen, müssen Sie zuerst den Encoder ermitteln, der für Ihre Anforderungen am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="2f873-105">Before creating an encoder, you must first find the encoder that is most suited to your needs.</span></span>

-   <span data-ttu-id="2f873-106">Windows Media-Audiocodecs</span><span class="sxs-lookup"><span data-stu-id="2f873-106">Windows Media audio codecs</span></span>

    <span data-ttu-id="2f873-107">Kategorie: **\_ \_ \_ Audioencoder der MFT-Kategorie**</span><span class="sxs-lookup"><span data-stu-id="2f873-107">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="2f873-108">Haupttyp: MF MediaType \_ -Audiodatei</span><span class="sxs-lookup"><span data-stu-id="2f873-108">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="2f873-109">SubType: MF Audioformat \_ WMAudioV9, MF Audioformat \_ WMAudioV8, MF Audioformat \_ wmaudio \_ Lossless, MF Audioformat \_ wmaspdif</span><span class="sxs-lookup"><span data-stu-id="2f873-109">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="2f873-110">Windows Media-Video Codecs</span><span class="sxs-lookup"><span data-stu-id="2f873-110">Windows Media video codecs</span></span>

    <span data-ttu-id="2f873-111">Kategorie: **\_ \_ Video \_ Encoder der MFT-Kategorie**</span><span class="sxs-lookup"><span data-stu-id="2f873-111">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="2f873-112">Haupttyp: MF MediaType- \_ Video</span><span class="sxs-lookup"><span data-stu-id="2f873-112">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="2f873-113">Untertyp: MF-Format \_ WVC1, MF-Format \_ WMV3, MF-Format \_ WMV2, MF-Format \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="2f873-113">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="2f873-114">Media Foundation bietet verschiedene Funktionen, die von der Anwendung aufgerufen werden können, um die verschiedenen Encoder aufzulisten, die im System verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2f873-114">Media Foundation provides several functions that your application can call to enumerate the various encoders available in your system.</span></span> <span data-ttu-id="2f873-115">Encoder werden als COM-Objekte registriert, und der Registrierungs Eintrag folgt dem Standardformat für com-Klassenfactorys.</span><span class="sxs-lookup"><span data-stu-id="2f873-115">Encoders are registered as COM objects and the registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="2f873-116">Die Registrierung verwaltet die CLSIDs für die Encoder, die nach dem Medienformat (Audiodatei oder Video) kategorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="2f873-116">The registry maintains the CLSIDs for the encoders, which are categorized by the media format (audio or video).</span></span> <span data-ttu-id="2f873-117">Die Klassen Bezeichner der Windows Media Encoder werden als Konstanten in der Header Datei "wmcodecdsp. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="2f873-117">The class identifiers of the Windows Media encoders are defined as constants in the wmcodecdsp.h header file.</span></span> <span data-ttu-id="2f873-118">In Media Foundation können die Encoder durch Aufrufe von [**mftregisterlocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) oder [**mftregisterlocalbyclsid**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) registriert werden, indem der catertyp, die unterstützten Eingabetypen und die unterstützten Ausgabetypen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2f873-118">In Media Foundation, the encoders can be registered through calls to [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) by specifying the catergory, the supported input types, and the supported output types.</span></span> <span data-ttu-id="2f873-119">Bei erfolgreicher Registrierung durch diese Funktionen werden die MFTs von den Media Foundation Enumerationsfunktionen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="2f873-119">Upon successful registration through these functions, the MFTs are considered by the Media Foundation enumeration functions.</span></span>

<span data-ttu-id="2f873-120">Zum Erstellen einer Instanz eines MFT-Encoders hat eine Anwendung die folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="2f873-120">For creating an instance of an encoder MFT, an application has the following choices.</span></span>

-   <span data-ttu-id="2f873-121">Erstellen Sie den Encoder-MFT direkt, und erhalten Sie einen Zeiger auf die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2f873-121">Create the encoder MFT directly and receive a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="2f873-122">Weitere Informationen finden Sie unter [Erstellen eines Encoders mithilfe von cokreateinstance](using-an-encoder-s-imftransform--interface.md).</span><span class="sxs-lookup"><span data-stu-id="2f873-122">For more information, see [Creating an Encoder by Using CoCreateInstance](using-an-encoder-s-imftransform--interface.md).</span></span>
-   <span data-ttu-id="2f873-123">Erstellen Sie eine Instanz des Aktivierungs Objekts für den Encoder-MFT, und erhalten Sie einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2f873-123">Create an instance of the activation object for the encoder MFT and receive a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="2f873-124">Weitere Informationen finden Sie unter [Verwenden der Aktivierungs Objekte eines Encoders](using-an-encoder-s-activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2f873-124">For more information, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="2f873-125">Wenn Ihre Anwendung in der [Pipeline Schicht-ASF-Komponenten](pipeline-layer-asf-components.md) verwendet, um eine Datei in das ASF-Format zu codieren, müssen Sie den Encoder-MFT als Transformations Knoten in die Pipeline einfügen.</span><span class="sxs-lookup"><span data-stu-id="2f873-125">If your application is using [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) to encode a file to ASF format, you must insert the encoder MFT into the pipeline as a transform node.</span></span> <span data-ttu-id="2f873-126">Wenn Sie den Transformations Knoten in der Codierungs Topologie erstellen, können Sie entweder den Objekttyp als Zeiger auf die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle oder das [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Objekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="2f873-126">While creating the transform node in the encoding topology, you can either set the object type as a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface or the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object.</span></span> <span data-ttu-id="2f873-127">Media Foundation stellt Aktivierungs Objekte für Windows Media Encoder bereit, sodass Sie bequem als Transformations Knoten in der Codierungs Topologie festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="2f873-127">Media Foundation provides activation objects for Windows Media encoders so that they can be conveniently set as the transform node in the encoding topology.</span></span> <span data-ttu-id="2f873-128">Wenn die Topologie aufgelöst wird, verwendet die Medien Sitzung das Aktivierungs Objekt, um eine Instanz des MFT-Encoders zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2f873-128">When the topology is resolved, the Media Session uses the activation object to create an instance of the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f873-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2f873-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f873-130">Windows Media Encoder</span><span class="sxs-lookup"><span data-stu-id="2f873-130">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



