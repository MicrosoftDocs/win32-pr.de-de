---
description: Dieses Thema enthält Informationen über den nativen DNG-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Übersicht über das DNG-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f766356f7c13d7b2bb25adab5411ae55c2735f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345818"
---
# <a name="dng-format-overview"></a><span data-ttu-id="595bf-103">Übersicht über das DNG-Format</span><span class="sxs-lookup"><span data-stu-id="595bf-103">DNG Format Overview</span></span>

<span data-ttu-id="595bf-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="595bf-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="595bf-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="595bf-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="595bf-106">Dieses Thema enthält Informationen über den nativen DNG-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="595bf-106">This topic provides information about the native DNG codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="595bf-107">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="595bf-107">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="595bf-108">Decodierung</span><span class="sxs-lookup"><span data-stu-id="595bf-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="595bf-109">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="595bf-109">Codec Identity</span></span>

<span data-ttu-id="595bf-110">In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="595bf-110">The following table provides codec identification information.</span></span>



|                        |                                                      |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="595bf-111">Formaler Name (n)</span><span class="sxs-lookup"><span data-stu-id="595bf-111">Formal Name(s)</span></span>         | <span data-ttu-id="595bf-112">Digitale negative Zahl (DNG)</span><span class="sxs-lookup"><span data-stu-id="595bf-112">Digital Negative (DNG)</span></span>                               |
| <span data-ttu-id="595bf-113">Dateinamenerweiterung (en)</span><span class="sxs-lookup"><span data-stu-id="595bf-113">File Name Extension(s)</span></span> | <span data-ttu-id="595bf-114">.dng</span><span class="sxs-lookup"><span data-stu-id="595bf-114">.dng</span></span>                                                 |
| <span data-ttu-id="595bf-115">MIME-Typ (en)</span><span class="sxs-lookup"><span data-stu-id="595bf-115">MIME type(s)</span></span>           | <span data-ttu-id="595bf-116">Bild/DNG</span><span class="sxs-lookup"><span data-stu-id="595bf-116">image/DNG</span></span>                                            |
| <span data-ttu-id="595bf-117">Spezifikations Unterstützung</span><span class="sxs-lookup"><span data-stu-id="595bf-117">Specification Support</span></span>  | <span data-ttu-id="595bf-118">Digital Negative (DNG)-Spezifikations Version 1.4.0.0</span><span class="sxs-lookup"><span data-stu-id="595bf-118">Digital Negative (DNG) Specification Version 1.4.0.0</span></span> |



 

<span data-ttu-id="595bf-119">In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen DNG-Codec-Komponenten identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="595bf-119">The following table lists the GUIDs used to identify the native DNG codec components.</span></span>



| <span data-ttu-id="595bf-120">Komponente</span><span class="sxs-lookup"><span data-stu-id="595bf-120">Component</span></span>        | <span data-ttu-id="595bf-121">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="595bf-121">Friendly Name</span></span>             | <span data-ttu-id="595bf-122">GUID</span><span class="sxs-lookup"><span data-stu-id="595bf-122">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="595bf-123">Container Format</span><span class="sxs-lookup"><span data-stu-id="595bf-123">Container Format</span></span> | <span data-ttu-id="595bf-124">GUID \_ containerformatadng</span><span class="sxs-lookup"><span data-stu-id="595bf-124">GUID\_ContainerFormatAdng</span></span> | <span data-ttu-id="595bf-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span><span class="sxs-lookup"><span data-stu-id="595bf-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span></span> |
| <span data-ttu-id="595bf-126">Decoder</span><span class="sxs-lookup"><span data-stu-id="595bf-126">Decoder</span></span>          | <span data-ttu-id="595bf-127">CLSID- \_ wicadngdecoder</span><span class="sxs-lookup"><span data-stu-id="595bf-127">CLSID\_WICAdngDecoder</span></span>     | <span data-ttu-id="595bf-128">981d9411-909e-42a7-8f5da747ff052edb</span><span class="sxs-lookup"><span data-stu-id="595bf-128">981d9411-909e-42a7-8f5da747ff052edb</span></span> |



 

## <a name="decoding"></a><span data-ttu-id="595bf-129">Decodierung</span><span class="sxs-lookup"><span data-stu-id="595bf-129">Decoding</span></span>

<span data-ttu-id="595bf-130">Die WIC-Decodierung-API ist als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="595bf-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="595bf-131">Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="595bf-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="595bf-132">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="595bf-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="595bf-133">Der Decoder unterstützt das Decodieren von Rohdaten Sensordaten nicht und unterstützt nur Dateien mit einer nicht unformatierten Bilddarstellung, die in eine IFD mit einem newsubfiletype gleich 1 eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="595bf-133">The decoder does not support decoding raw sensor data and only supports files with a non-raw image representation embedded in an IFD with NewSubFileType equal to 1.</span></span>

 

 



