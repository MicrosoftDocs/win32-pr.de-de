---
description: Konfigurieren von Codec-MFTs
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: Konfigurieren von Codec-MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0065f05d10eae367b13ef6f7caf3fe2ab322163a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484099"
---
# <a name="configuring-codec-mfts"></a><span data-ttu-id="fa859-103">Konfigurieren von Codec-MFTs</span><span class="sxs-lookup"><span data-stu-id="fa859-103">Configuring Codec MFTs</span></span>

<span data-ttu-id="fa859-104">In diesem Thema wird der Prozess der Konfiguration der Codec-MFTs beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fa859-104">This topic describes the process of configuring the codec MFTs.</span></span> <span data-ttu-id="fa859-105">Jeder Codec verfügt über bestimmte Prozeduren, aber die gemeinsamen Informationen werden hier beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fa859-105">Each codec has specific procedures, but the information common to all is described here.</span></span>

## <a name="configuring-mft-inputs-and-outputs"></a><span data-ttu-id="fa859-106">Konfigurieren von MFT-Eingaben und-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa859-106">Configuring MFT Inputs and Outputs</span></span>

<span data-ttu-id="fa859-107">Jede MFT unterstützt bestimmte Eingabe-und Ausgabetypen.</span><span class="sxs-lookup"><span data-stu-id="fa859-107">Every MFT supports specific input and output types.</span></span> <span data-ttu-id="fa859-108">Sie können unterstützte Eingabetypen abrufen, indem Sie " [**imftransform:: getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)" wiederholt aufrufen und dabei den Typindex bei jedem Aufruf inkrementieren.</span><span class="sxs-lookup"><span data-stu-id="fa859-108">You can retrieve supported input types by repeatedly calling [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), incrementing the type index with each call.</span></span> <span data-ttu-id="fa859-109">Wenn Sie einen geeigneten Typ finden, legen Sie den Eingabetyp durch Aufrufen von [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)fest.</span><span class="sxs-lookup"><span data-stu-id="fa859-109">When you find an appropriate type, set the input type by calling [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span> <span data-ttu-id="fa859-110">Anschließend können Sie den Vorgang für den Ausgabetyp mit den Aufrufen [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) und [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)wiederholen.</span><span class="sxs-lookup"><span data-stu-id="fa859-110">You can then repeat the process for the output type using the calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) and [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="fa859-111">Sie müssen die verfügbaren Ausgabetypen erst Abfragen oder festlegen, nachdem Sie den Eingabetyp festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="fa859-111">You must query or set the available output types only after setting the input type.</span></span>

## <a name="configuring-the-codec-mfts-for-encoding"></a><span data-ttu-id="fa859-112">Konfigurieren der Codec-MFTs für die Codierung</span><span class="sxs-lookup"><span data-stu-id="fa859-112">Configuring the Codec MFTs for Encoding</span></span>

<span data-ttu-id="fa859-113">Alle Windows Media Audio-und Video Codecs unterstützen eine Vielzahl von Codierungs Features.</span><span class="sxs-lookup"><span data-stu-id="fa859-113">All of the Windows Media Audio and Video codecs support a variety of encoding features.</span></span> <span data-ttu-id="fa859-114">Diese Features werden in der Regel durch Festlegen der Eigenschaften für die MFT mithilfe der Methoden der **IPropertyStore** -Schnittstelle konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="fa859-114">These features are generally configured by setting properties on the MFT by using the methods of the **IPropertyStore** interface.</span></span> <span data-ttu-id="fa859-115">Einige Eigenschaften werden mithilfe spezieller Codec-Schnittstellen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="fa859-115">Some properties are configured using specialized codec interfaces.</span></span> <span data-ttu-id="fa859-116">Diese Schnittstellen werden für jeden Codec im Abschnitt [Codec-Objekte](codecobjects.md)aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fa859-116">These interfaces are listed for each codec in the section [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="fa859-117">Die allgemeine Reihenfolge der Vorgänge zum Konfigurieren einer Codierungs-MFT lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fa859-117">The general order of operations for configuring an encoding MFT is as follows:</span></span>

1.  <span data-ttu-id="fa859-118">Konfigurieren Sie die Codec-Features wie gewünscht mithilfe der Methoden von **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="fa859-118">Configure codec features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="fa859-119">Verwenden Sie die Codec-MFT-Schnittstellen, um zusätzliche Features zu konfigurieren, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fa859-119">Use the codec MFT interfaces to configure additional features, if needed.</span></span>
3.  <span data-ttu-id="fa859-120">Konfigurieren Sie die Eingabe-und Ausgabetypen.</span><span class="sxs-lookup"><span data-stu-id="fa859-120">Configure the input and output types.</span></span> <span data-ttu-id="fa859-121">Die Reihenfolge, in der die Typen konfiguriert werden sollten, variiert für einzelne Codecs.</span><span class="sxs-lookup"><span data-stu-id="fa859-121">The order in which the types should be configured varies for individual codecs.</span></span> <span data-ttu-id="fa859-122">Weitere Informationen finden Sie unter [Arbeiten mit Audiodaten](workingwithaudio.md) und [Arbeiten mit Videos](workingwithvideo.md).</span><span class="sxs-lookup"><span data-stu-id="fa859-122">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

## <a name="configuring-the-codec-mfts-for-decoding"></a><span data-ttu-id="fa859-123">Konfigurieren der Codec-MFTs für das Decodieren</span><span class="sxs-lookup"><span data-stu-id="fa859-123">Configuring the Codec MFTs for Decoding</span></span>

<span data-ttu-id="fa859-124">Decodierung ist einfacher als die Codierung, da weniger Decoder-Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="fa859-124">Decoding is simpler than encoding, as fewer decoder features are supported.</span></span>

<span data-ttu-id="fa859-125">Die allgemeine Reihenfolge der Vorgänge zum Konfigurieren einer MFT-Decodierung lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fa859-125">The general order of operations for configuring a decoding MFT is as follows:</span></span>

1.  <span data-ttu-id="fa859-126">Konfigurieren Sie die decoderfeatures wie gewünscht mithilfe der Methoden von **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="fa859-126">Configure decoder features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="fa859-127">Legen Sie den Eingabetyp auf den für die encoderausgabe verwendeten Typ fest.</span><span class="sxs-lookup"><span data-stu-id="fa859-127">Set the input type to the type used for the encoder output.</span></span>
3.  <span data-ttu-id="fa859-128">Konfigurieren Sie den Ausgabetyp.</span><span class="sxs-lookup"><span data-stu-id="fa859-128">Configure the output type.</span></span> <span data-ttu-id="fa859-129">Die unterstützten Ausgabetypen unterscheiden sich für unterschiedliche Eingaben.</span><span class="sxs-lookup"><span data-stu-id="fa859-129">The supported output types are different for different inputs.</span></span>

> [!Note]  
> <span data-ttu-id="fa859-130">Es ist wichtig, den gleichen Medientyp für die decodereingabe zu verwenden, die für die encoderausgabe verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fa859-130">It is important to use the same media type for the decoder input as was used for the encoder output.</span></span> <span data-ttu-id="fa859-131">Dies liegt daran, dass die Windows Media Audio-und Video Codecs Medienformate mit zusätzlichen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="fa859-131">This is because the Windows Media Audio and Video codecs use media formats with extra data.</span></span> <span data-ttu-id="fa859-132">Ohne die erweiterten Formatierungsdaten können Sie den komprimierten Inhalt nicht decodieren.</span><span class="sxs-lookup"><span data-stu-id="fa859-132">Without the extended format data, you cannot decode the compressed content.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fa859-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fa859-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa859-134">Arbeiten mit Codec-MFTs</span><span class="sxs-lookup"><span data-stu-id="fa859-134">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



