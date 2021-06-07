---
description: Dieses Thema enthält Informationen zum nativen GIF-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Übersicht über das GIF-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf7e9924c921b7944de114f5fe667cb2aa33cae
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444451"
---
# <a name="gif-format-overview"></a><span data-ttu-id="a2fc0-103">Übersicht über das GIF-Format</span><span class="sxs-lookup"><span data-stu-id="a2fc0-103">GIF Format Overview</span></span>

<span data-ttu-id="a2fc0-104">Dieses Thema enthält Informationen zum nativen GIF-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a2fc0-104">This topic provides information about the native GIF codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="a2fc0-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="a2fc0-105">Codec Identity</span></span>

<span data-ttu-id="a2fc0-106">Die folgende Tabelle enthält Informationen zur Codecidentifikation.</span><span class="sxs-lookup"><span data-stu-id="a2fc0-106">The following table provides codec identification information.</span></span>



|  <span data-ttu-id="a2fc0-107">Komponente</span><span class="sxs-lookup"><span data-stu-id="a2fc0-107">Component</span></span>             | <span data-ttu-id="a2fc0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2fc0-108">Description</span></span>                           |
|------------------------|---------------------------------------|
| <span data-ttu-id="a2fc0-109">Formale Namen</span><span class="sxs-lookup"><span data-stu-id="a2fc0-109">Formal Name(s)</span></span>         | <span data-ttu-id="a2fc0-110">Graphics Interchange Format 89a (GIF)</span><span class="sxs-lookup"><span data-stu-id="a2fc0-110">Graphics Interchange Format 89a (GIF)</span></span> |
| <span data-ttu-id="a2fc0-111">Dateinamenerweiterungen</span><span class="sxs-lookup"><span data-stu-id="a2fc0-111">File Name Extension(s)</span></span> | <span data-ttu-id="a2fc0-112">GIF</span><span class="sxs-lookup"><span data-stu-id="a2fc0-112">gif</span></span>                                   |
| <span data-ttu-id="a2fc0-113">MIME-Typ (MIME type)</span><span class="sxs-lookup"><span data-stu-id="a2fc0-113">MIME type</span></span>              | <span data-ttu-id="a2fc0-114">image/gif</span><span class="sxs-lookup"><span data-stu-id="a2fc0-114">image/gif</span></span>                             |
| <span data-ttu-id="a2fc0-115">Spezifikationsunterstützung</span><span class="sxs-lookup"><span data-stu-id="a2fc0-115">Specification Support</span></span>  | <span data-ttu-id="a2fc0-116">GIF-Spezifikation 89a/89m</span><span class="sxs-lookup"><span data-stu-id="a2fc0-116">GIF Specification 89a/89m</span></span>             |



 

<span data-ttu-id="a2fc0-117">In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen GIF-Codeckomponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2fc0-117">The following table lists the GUIDs used to identify the native GIF codec components.</span></span>



| <span data-ttu-id="a2fc0-118">Komponente</span><span class="sxs-lookup"><span data-stu-id="a2fc0-118">Component</span></span>        | <span data-ttu-id="a2fc0-119">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="a2fc0-119">Friendly Name</span></span>            | <span data-ttu-id="a2fc0-120">GUID</span><span class="sxs-lookup"><span data-stu-id="a2fc0-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="a2fc0-121">Containerformat</span><span class="sxs-lookup"><span data-stu-id="a2fc0-121">Container Format</span></span> | <span data-ttu-id="a2fc0-122">GUID \_ ContainerFormatGif</span><span class="sxs-lookup"><span data-stu-id="a2fc0-122">GUID\_ContainerFormatGif</span></span> | <span data-ttu-id="a2fc0-123">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span><span class="sxs-lookup"><span data-stu-id="a2fc0-123">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span></span> |
| <span data-ttu-id="a2fc0-124">Decoder</span><span class="sxs-lookup"><span data-stu-id="a2fc0-124">Decoder</span></span>          | <span data-ttu-id="a2fc0-125">CLSID \_ WICGifDecoder</span><span class="sxs-lookup"><span data-stu-id="a2fc0-125">CLSID\_WICGifDecoder</span></span>     | <span data-ttu-id="a2fc0-126">381dda3c-9ce9-4834-a23e1f98f8fc52be</span><span class="sxs-lookup"><span data-stu-id="a2fc0-126">381dda3c-9ce9-4834-a23e1f98f8fc52be</span></span> |
| <span data-ttu-id="a2fc0-127">Encoder</span><span class="sxs-lookup"><span data-stu-id="a2fc0-127">Encoder</span></span>          | <span data-ttu-id="a2fc0-128">CLSID \_ WICGifEncoder</span><span class="sxs-lookup"><span data-stu-id="a2fc0-128">CLSID\_WICGifEncoder</span></span>     | <span data-ttu-id="a2fc0-129">114f5598-0b22-40a0-86a1c83ea495adbd</span><span class="sxs-lookup"><span data-stu-id="a2fc0-129">114f5598-0b22-40a0-86a1c83ea495adbd</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="a2fc0-130">Codierung</span><span class="sxs-lookup"><span data-stu-id="a2fc0-130">Encoding</span></span>

<span data-ttu-id="a2fc0-131">Die WIC-Codierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="a2fc0-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="a2fc0-132">Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="a2fc0-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="a2fc0-133">Encoderoptionen</span><span class="sxs-lookup"><span data-stu-id="a2fc0-133">Encoder Options</span></span>

<span data-ttu-id="a2fc0-134">WIC-fähige Codecs unterscheiden sich auf Codierungsoptionenebene.</span><span class="sxs-lookup"><span data-stu-id="a2fc0-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="a2fc0-135">Encoderoptionen spiegeln die Funktionen eines Bildencoders wider, und jeder native Codec unterstützt eine Reihe dieser Encoderoptionen.</span><span class="sxs-lookup"><span data-stu-id="a2fc0-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="a2fc0-136">Encoderoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (obwohl sie nicht unbedingt unterstützt werden) oder codecspezifische Optionen, die vom Bildformatcodec entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="a2fc0-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="a2fc0-137">Um diese Codierungsoptionen während des Codierungsprozesses zu verwalten, verwendet WIC die [**IPropertyBag2-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a2fc0-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="a2fc0-138">Weitere Informationen zur Verwendung der **IPropertyBag2-Schnittstelle** für die WIC-Codierung finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="a2fc0-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="a2fc0-139">Der GIF-Encoder unterstützt keine grundlegenden WIC-Optionen und stellt keine benutzerdefinierten Encoderoptionen bereit.</span><span class="sxs-lookup"><span data-stu-id="a2fc0-139">The GIF encoder does not support any basic WIC options and does not provide custom encoder options.</span></span> <span data-ttu-id="a2fc0-140">Wenn eine Encoderoption in der [**IPropertyBag2-Optionsliste**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) enthalten ist, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a2fc0-140">If an encoder option is in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list, it is ignored.</span></span>

## <a name="decoding"></a><span data-ttu-id="a2fc0-141">Decodierung</span><span class="sxs-lookup"><span data-stu-id="a2fc0-141">Decoding</span></span>

<span data-ttu-id="a2fc0-142">Die WIC-Decodierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="a2fc0-142">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="a2fc0-143">Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="a2fc0-143">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="a2fc0-144">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="a2fc0-144">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
