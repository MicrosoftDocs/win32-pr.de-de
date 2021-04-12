---
description: Dieses Thema enthält Informationen über den nativen GIF-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Übersicht über GIF-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f592b50300edf79c71ff4050a2c0d5aeba8b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216964"
---
# <a name="gif-format-overview"></a><span data-ttu-id="7c4ce-103">Übersicht über GIF-Format</span><span class="sxs-lookup"><span data-stu-id="7c4ce-103">GIF Format Overview</span></span>

<span data-ttu-id="7c4ce-104">Dieses Thema enthält Informationen über den nativen GIF-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7c4ce-104">This topic provides information about the native GIF codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="7c4ce-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="7c4ce-105">Codec Identity</span></span>

<span data-ttu-id="7c4ce-106">In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7c4ce-106">The following table provides codec identification information.</span></span>



|                        |                                       |
|------------------------|---------------------------------------|
| <span data-ttu-id="7c4ce-107">Formaler Name (n)</span><span class="sxs-lookup"><span data-stu-id="7c4ce-107">Formal Name(s)</span></span>         | <span data-ttu-id="7c4ce-108">Graphics Interchange Format 89A (GIF)</span><span class="sxs-lookup"><span data-stu-id="7c4ce-108">Graphics Interchange Format 89a (GIF)</span></span> |
| <span data-ttu-id="7c4ce-109">Dateinamenerweiterung (en)</span><span class="sxs-lookup"><span data-stu-id="7c4ce-109">File Name Extension(s)</span></span> | <span data-ttu-id="7c4ce-110">GIF</span><span class="sxs-lookup"><span data-stu-id="7c4ce-110">gif</span></span>                                   |
| <span data-ttu-id="7c4ce-111">MIME-Typ (MIME type)</span><span class="sxs-lookup"><span data-stu-id="7c4ce-111">MIME type</span></span>              | <span data-ttu-id="7c4ce-112">image/gif</span><span class="sxs-lookup"><span data-stu-id="7c4ce-112">image/gif</span></span>                             |
| <span data-ttu-id="7c4ce-113">Spezifikations Unterstützung</span><span class="sxs-lookup"><span data-stu-id="7c4ce-113">Specification Support</span></span>  | <span data-ttu-id="7c4ce-114">GIF-Spezifikation 89A/89m</span><span class="sxs-lookup"><span data-stu-id="7c4ce-114">GIF Specification 89a/89m</span></span>             |



 

<span data-ttu-id="7c4ce-115">In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen GIF-Codec-Komponenten identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="7c4ce-115">The following table lists the GUIDs used to identify the native GIF codec components.</span></span>



| <span data-ttu-id="7c4ce-116">Komponente</span><span class="sxs-lookup"><span data-stu-id="7c4ce-116">Component</span></span>        | <span data-ttu-id="7c4ce-117">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="7c4ce-117">Friendly Name</span></span>            | <span data-ttu-id="7c4ce-118">GUID</span><span class="sxs-lookup"><span data-stu-id="7c4ce-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="7c4ce-119">Container Format</span><span class="sxs-lookup"><span data-stu-id="7c4ce-119">Container Format</span></span> | <span data-ttu-id="7c4ce-120">GUID \_ containerformatgif</span><span class="sxs-lookup"><span data-stu-id="7c4ce-120">GUID\_ContainerFormatGif</span></span> | <span data-ttu-id="7c4ce-121">1F 8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span><span class="sxs-lookup"><span data-stu-id="7c4ce-121">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span></span> |
| <span data-ttu-id="7c4ce-122">Decoder</span><span class="sxs-lookup"><span data-stu-id="7c4ce-122">Decoder</span></span>          | <span data-ttu-id="7c4ce-123">CLSID- \_ wicgifdecoder</span><span class="sxs-lookup"><span data-stu-id="7c4ce-123">CLSID\_WICGifDecoder</span></span>     | <span data-ttu-id="7c4ce-124">381dda3c-9ce9-4834-a23e1f98f8fc52be</span><span class="sxs-lookup"><span data-stu-id="7c4ce-124">381dda3c-9ce9-4834-a23e1f98f8fc52be</span></span> |
| <span data-ttu-id="7c4ce-125">Encoder</span><span class="sxs-lookup"><span data-stu-id="7c4ce-125">Encoder</span></span>          | <span data-ttu-id="7c4ce-126">CLSID \_ wicgifencoder</span><span class="sxs-lookup"><span data-stu-id="7c4ce-126">CLSID\_WICGifEncoder</span></span>     | <span data-ttu-id="7c4ce-127">114 f 5598-0b22-40A0-86a1c83ea495adbd</span><span class="sxs-lookup"><span data-stu-id="7c4ce-127">114f5598-0b22-40a0-86a1c83ea495adbd</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="7c4ce-128">Codierung</span><span class="sxs-lookup"><span data-stu-id="7c4ce-128">Encoding</span></span>

<span data-ttu-id="7c4ce-129">Die WIC-Codierungs-API ist als Codec-unabhängig konzipiert, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="7c4ce-129">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="7c4ce-130">Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="7c4ce-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="7c4ce-131">Codierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="7c4ce-131">Encoder Options</span></span>

<span data-ttu-id="7c4ce-132">WIC-fähige Codecs unterscheiden sich auf der Codierungs Options Ebene.</span><span class="sxs-lookup"><span data-stu-id="7c4ce-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="7c4ce-133">Codierungsoptionen entsprechen den Funktionen eines Bild Encoders, und jeder Native Codec unterstützt eine Reihe dieser Codierungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="7c4ce-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="7c4ce-134">Codierungsoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (aber nicht unbedingt unterstützt werden), oder für Codec-spezifische Optionen, die vom Abbild Format</span><span class="sxs-lookup"><span data-stu-id="7c4ce-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="7c4ce-135">Zum Verwalten dieser Codierungsoptionen während des Codierungs Prozesses verwendet WIC die [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7c4ce-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="7c4ce-136">Weitere Informationen zur Verwendung der **IPropertyBag2** -Schnittstelle für WIC-Codierung finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="7c4ce-136">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="7c4ce-137">Der GIF-Encoder unterstützt keine grundlegenden WIC-Optionen und bietet keine benutzerdefinierten Codierungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="7c4ce-137">The GIF encoder does not support any basic WIC options and does not provide custom encoder options.</span></span> <span data-ttu-id="7c4ce-138">Wenn eine Encoder-Option in der [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Optionsliste enthalten ist, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7c4ce-138">If an encoder option is in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list, it is ignored.</span></span>

## <a name="decoding"></a><span data-ttu-id="7c4ce-139">Decodierung</span><span class="sxs-lookup"><span data-stu-id="7c4ce-139">Decoding</span></span>

<span data-ttu-id="7c4ce-140">Die WIC-Decodierung-API ist als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="7c4ce-140">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="7c4ce-141">Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="7c4ce-141">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="7c4ce-142">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="7c4ce-142">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
