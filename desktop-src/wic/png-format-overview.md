---
description: Dieses Thema enthält Informationen über den systemeigenen PNG-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Übersicht über PNG-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118d6af831c8fb6f8cacc8407e90f610c0fc426d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360747"
---
# <a name="png-format-overview"></a><span data-ttu-id="c8da6-103">Übersicht über PNG-Format</span><span class="sxs-lookup"><span data-stu-id="c8da6-103">PNG Format Overview</span></span>

<span data-ttu-id="c8da6-104">Dieses Thema enthält Informationen über den systemeigenen PNG-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c8da6-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="c8da6-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="c8da6-105">Codec Identity</span></span>

<span data-ttu-id="c8da6-106">In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c8da6-106">The following table provides codec identification information.</span></span>



|                        |                                 |
|------------------------|---------------------------------|
| <span data-ttu-id="c8da6-107">Formaler Name (n)</span><span class="sxs-lookup"><span data-stu-id="c8da6-107">Formal Name(s)</span></span>         | <span data-ttu-id="c8da6-108">PNG (Portable Network Graphics)</span><span class="sxs-lookup"><span data-stu-id="c8da6-108">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="c8da6-109">Dateinamenerweiterung (en)</span><span class="sxs-lookup"><span data-stu-id="c8da6-109">File Name Extension(s)</span></span> | <span data-ttu-id="c8da6-110">png</span><span class="sxs-lookup"><span data-stu-id="c8da6-110">png</span></span>                             |
| <span data-ttu-id="c8da6-111">MIME-Typ (MIME type)</span><span class="sxs-lookup"><span data-stu-id="c8da6-111">MIME type</span></span>              | <span data-ttu-id="c8da6-112">image/png</span><span class="sxs-lookup"><span data-stu-id="c8da6-112">image/png</span></span>                       |
| <span data-ttu-id="c8da6-113">Spezifikations Unterstützung</span><span class="sxs-lookup"><span data-stu-id="c8da6-113">Specification Support</span></span>  | <span data-ttu-id="c8da6-114">PNG-Spezifikation 1,2</span><span class="sxs-lookup"><span data-stu-id="c8da6-114">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="c8da6-115">In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen PNG-Codec-Komponenten identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c8da6-115">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="c8da6-116">Komponente</span><span class="sxs-lookup"><span data-stu-id="c8da6-116">Component</span></span>        | <span data-ttu-id="c8da6-117">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="c8da6-117">Friendly Name</span></span>            | <span data-ttu-id="c8da6-118">GUID</span><span class="sxs-lookup"><span data-stu-id="c8da6-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="c8da6-119">Container Format</span><span class="sxs-lookup"><span data-stu-id="c8da6-119">Container Format</span></span> | <span data-ttu-id="c8da6-120">GUID \_ containerformatpng</span><span class="sxs-lookup"><span data-stu-id="c8da6-120">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="c8da6-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="c8da6-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="c8da6-122">Decoder</span><span class="sxs-lookup"><span data-stu-id="c8da6-122">Decoder</span></span>          | <span data-ttu-id="c8da6-123">CLSID- \_ wicpngdecoder</span><span class="sxs-lookup"><span data-stu-id="c8da6-123">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="c8da6-124">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="c8da6-124">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="c8da6-125">Encoder</span><span class="sxs-lookup"><span data-stu-id="c8da6-125">Encoder</span></span>          | <span data-ttu-id="c8da6-126">CLSID \_ wicpngencoder</span><span class="sxs-lookup"><span data-stu-id="c8da6-126">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="c8da6-127">27949969-876a-41d7-9447568f & 6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="c8da6-127">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="c8da6-128">Windows 8 und höher</span><span class="sxs-lookup"><span data-stu-id="c8da6-128">Windows 8 and later</span></span>

<span data-ttu-id="c8da6-129">Ab Windows 8 bietet WIC einen zusätzlichen PNG-Decoder.</span><span class="sxs-lookup"><span data-stu-id="c8da6-129">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="c8da6-130">Codierung</span><span class="sxs-lookup"><span data-stu-id="c8da6-130">Encoding</span></span>

<span data-ttu-id="c8da6-131">Die WIC-Codierungs-API ist als Codec-unabhängig konzipiert, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="c8da6-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="c8da6-132">Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="c8da6-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="c8da6-133">Codierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="c8da6-133">Encoder Options</span></span>

<span data-ttu-id="c8da6-134">WIC-fähige Codecs unterscheiden sich auf der Codierungs Options Ebene.</span><span class="sxs-lookup"><span data-stu-id="c8da6-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="c8da6-135">Codierungsoptionen entsprechen den Funktionen eines Bild Encoders, und jeder Native Codec unterstützt eine Reihe dieser Codierungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="c8da6-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="c8da6-136">Codierungsoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (aber nicht unbedingt unterstützt werden), oder für Codec-spezifische Optionen, die vom Abbild Format</span><span class="sxs-lookup"><span data-stu-id="c8da6-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="c8da6-137">Zum Verwalten dieser Codierungsoptionen während des Codierungs Prozesses verwendet WIC die [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c8da6-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="c8da6-138">Weitere Informationen zur Verwendung der **IPropertyBag2** -Schnittstelle für WIC-Codierung finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="c8da6-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="c8da6-139">Der PNG-Codec verwendet grundlegende WIC-Encoder-Optionen.</span><span class="sxs-lookup"><span data-stu-id="c8da6-139">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="c8da6-140">In der folgenden Tabelle werden die vom systemeigenen PNG-Codec unterstützten WIC-Encoder-Optionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c8da6-140">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="c8da6-141">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="c8da6-141">Property Name</span></span>   | <span data-ttu-id="c8da6-142">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c8da6-142">VARTYPE</span></span>  | <span data-ttu-id="c8da6-143">Wertbereich</span><span class="sxs-lookup"><span data-stu-id="c8da6-143">Value Range</span></span>                                                 | <span data-ttu-id="c8da6-144">Standardwert</span><span class="sxs-lookup"><span data-stu-id="c8da6-144">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c8da6-145">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="c8da6-145">InterlaceOption</span></span> | <span data-ttu-id="c8da6-146">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="c8da6-146">VT\_BOOL</span></span> | <span data-ttu-id="c8da6-147">**True** / **False**</span><span class="sxs-lookup"><span data-stu-id="c8da6-147">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="c8da6-148">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="c8da6-148">**FALSE**</span></span>                                                        |
| <span data-ttu-id="c8da6-149">FilterOption</span><span class="sxs-lookup"><span data-stu-id="c8da6-149">FilterOption</span></span>    | <span data-ttu-id="c8da6-150">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="c8da6-150">VT\_UI1</span></span>  | [<span data-ttu-id="c8da6-151">**Wicpngfilteroption**</span><span class="sxs-lookup"><span data-stu-id="c8da6-151">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="c8da6-152">**Wicpngfilterunspezifiziert**</span><span class="sxs-lookup"><span data-stu-id="c8da6-152">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="c8da6-153">Wenn eine Encoder-Option in der [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Optionsliste vorhanden ist, die der Codec nicht unterstützt, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c8da6-153">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="c8da6-154">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="c8da6-154">InterlaceOption</span></span>

<span data-ttu-id="c8da6-155">Gibt an, ob die Bilddaten als Zeilen Sprung codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c8da6-155">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="c8da6-156">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="c8da6-156">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="c8da6-157">FilterOption</span><span class="sxs-lookup"><span data-stu-id="c8da6-157">FilterOption</span></span>

<span data-ttu-id="c8da6-158">Gibt die für die Bildkomprimierung zu verwendende Filteroption an.</span><span class="sxs-lookup"><span data-stu-id="c8da6-158">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="c8da6-159">Der Standardwert ist " [**wicpngfilterunspezifiziert**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)".</span><span class="sxs-lookup"><span data-stu-id="c8da6-159">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="c8da6-160">Decodierung</span><span class="sxs-lookup"><span data-stu-id="c8da6-160">Decoding</span></span>

<span data-ttu-id="c8da6-161">Die WIC-Decodierung-API ist als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="c8da6-161">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="c8da6-162">Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="c8da6-162">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="c8da6-163">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="c8da6-163">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="c8da6-164">Der Native PNG-Codec unterstützt auch [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) bei der Frame-Decodierung und fügt Erweiterte Optionen für das Decodieren eines bildstreams hinzu.</span><span class="sxs-lookup"><span data-stu-id="c8da6-164">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="c8da6-165">Weitere Informationen zu diesen erweiterten Optionen finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="c8da6-165">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
