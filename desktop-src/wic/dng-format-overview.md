---
description: Dieses Thema enthält Informationen zum nativen DNG-Codec, der über Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Übersicht über das DNG-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815d6a24bb8e57e6c64b90f9e9068765838e148
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444931"
---
# <a name="dng-format-overview"></a><span data-ttu-id="0cd32-103">Übersicht über das DNG-Format</span><span class="sxs-lookup"><span data-stu-id="0cd32-103">DNG Format Overview</span></span>

<span data-ttu-id="0cd32-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="0cd32-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0cd32-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="0cd32-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0cd32-106">Dieses Thema enthält Informationen zum nativen DNG-Codec, der über Windows-Bilderstellungskomponente (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0cd32-106">This topic provides information about the native DNG codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="0cd32-107">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="0cd32-107">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="0cd32-108">Decodierung</span><span class="sxs-lookup"><span data-stu-id="0cd32-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="0cd32-109">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="0cd32-109">Codec Identity</span></span>

<span data-ttu-id="0cd32-110">Die folgende Tabelle enthält Informationen zur Codecidentifikation.</span><span class="sxs-lookup"><span data-stu-id="0cd32-110">The following table provides codec identification information.</span></span>



|     <span data-ttu-id="0cd32-111">Komponente</span><span class="sxs-lookup"><span data-stu-id="0cd32-111">Component</span></span>          |  <span data-ttu-id="0cd32-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0cd32-112">Description</span></span>                                         |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0cd32-113">Formale Namen</span><span class="sxs-lookup"><span data-stu-id="0cd32-113">Formal Name(s)</span></span>         | <span data-ttu-id="0cd32-114">Digital Negative (DNG)</span><span class="sxs-lookup"><span data-stu-id="0cd32-114">Digital Negative (DNG)</span></span>                               |
| <span data-ttu-id="0cd32-115">Dateinamenerweiterungen</span><span class="sxs-lookup"><span data-stu-id="0cd32-115">File Name Extension(s)</span></span> | <span data-ttu-id="0cd32-116">.dng</span><span class="sxs-lookup"><span data-stu-id="0cd32-116">.dng</span></span>                                                 |
| <span data-ttu-id="0cd32-117">MIME-Typen</span><span class="sxs-lookup"><span data-stu-id="0cd32-117">MIME type(s)</span></span>           | <span data-ttu-id="0cd32-118">image/DNG</span><span class="sxs-lookup"><span data-stu-id="0cd32-118">image/DNG</span></span>                                            |
| <span data-ttu-id="0cd32-119">Spezifikationsunterstützung</span><span class="sxs-lookup"><span data-stu-id="0cd32-119">Specification Support</span></span>  | <span data-ttu-id="0cd32-120">Digital Negative (DNG) Specification Version 1.4.0.0</span><span class="sxs-lookup"><span data-stu-id="0cd32-120">Digital Negative (DNG) Specification Version 1.4.0.0</span></span> |



 

<span data-ttu-id="0cd32-121">In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen DNG-Codeckomponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0cd32-121">The following table lists the GUIDs used to identify the native DNG codec components.</span></span>



| <span data-ttu-id="0cd32-122">Komponente</span><span class="sxs-lookup"><span data-stu-id="0cd32-122">Component</span></span>        | <span data-ttu-id="0cd32-123">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="0cd32-123">Friendly Name</span></span>             | <span data-ttu-id="0cd32-124">GUID</span><span class="sxs-lookup"><span data-stu-id="0cd32-124">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="0cd32-125">Containerformat</span><span class="sxs-lookup"><span data-stu-id="0cd32-125">Container Format</span></span> | <span data-ttu-id="0cd32-126">GUID \_ ContainerFormatAdng</span><span class="sxs-lookup"><span data-stu-id="0cd32-126">GUID\_ContainerFormatAdng</span></span> | <span data-ttu-id="0cd32-127">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span><span class="sxs-lookup"><span data-stu-id="0cd32-127">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span></span> |
| <span data-ttu-id="0cd32-128">Decoder</span><span class="sxs-lookup"><span data-stu-id="0cd32-128">Decoder</span></span>          | <span data-ttu-id="0cd32-129">CLSID \_ WICAdngDecoder</span><span class="sxs-lookup"><span data-stu-id="0cd32-129">CLSID\_WICAdngDecoder</span></span>     | <span data-ttu-id="0cd32-130">981d9411-909e-42a7-8f5da747ff052edb</span><span class="sxs-lookup"><span data-stu-id="0cd32-130">981d9411-909e-42a7-8f5da747ff052edb</span></span> |



 

## <a name="decoding"></a><span data-ttu-id="0cd32-131">Decodierung</span><span class="sxs-lookup"><span data-stu-id="0cd32-131">Decoding</span></span>

<span data-ttu-id="0cd32-132">Die WIC-Decodierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="0cd32-132">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="0cd32-133">Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="0cd32-133">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="0cd32-134">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="0cd32-134">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="0cd32-135">Der Decoder unterstützt keine Decodierung von Sensorrohdaten und nur Dateien mit einer nicht rohen Bilddarstellung, die in eine IFD mit NewSubFileType gleich 1 eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="0cd32-135">The decoder does not support decoding raw sensor data and only supports files with a non-raw image representation embedded in an IFD with NewSubFileType equal to 1.</span></span>

 

 



