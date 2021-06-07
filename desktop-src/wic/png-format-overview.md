---
description: Dieses Thema enthält Informationen zum nativen PNG-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Übersicht über das PNG-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb00b7530a22fcdbcce112053431ace5e553383
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444441"
---
# <a name="png-format-overview"></a><span data-ttu-id="e0c97-103">Übersicht über das PNG-Format</span><span class="sxs-lookup"><span data-stu-id="e0c97-103">PNG Format Overview</span></span>

<span data-ttu-id="e0c97-104">Dieses Thema enthält Informationen zum nativen PNG-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e0c97-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="e0c97-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="e0c97-105">Codec Identity</span></span>

<span data-ttu-id="e0c97-106">Die folgende Tabelle enthält Informationen zur Codecidentifikation.</span><span class="sxs-lookup"><span data-stu-id="e0c97-106">The following table provides codec identification information.</span></span>



|     <span data-ttu-id="e0c97-107">Komponente</span><span class="sxs-lookup"><span data-stu-id="e0c97-107">Component</span></span>          | <span data-ttu-id="e0c97-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0c97-108">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="e0c97-109">Formale Namen</span><span class="sxs-lookup"><span data-stu-id="e0c97-109">Formal Name(s)</span></span>         | <span data-ttu-id="e0c97-110">PNG (Portable Network Graphics)</span><span class="sxs-lookup"><span data-stu-id="e0c97-110">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="e0c97-111">Dateinamenerweiterungen</span><span class="sxs-lookup"><span data-stu-id="e0c97-111">File Name Extension(s)</span></span> | <span data-ttu-id="e0c97-112">png</span><span class="sxs-lookup"><span data-stu-id="e0c97-112">png</span></span>                             |
| <span data-ttu-id="e0c97-113">MIME-Typ (MIME type)</span><span class="sxs-lookup"><span data-stu-id="e0c97-113">MIME type</span></span>              | <span data-ttu-id="e0c97-114">image/png</span><span class="sxs-lookup"><span data-stu-id="e0c97-114">image/png</span></span>                       |
| <span data-ttu-id="e0c97-115">Spezifikationsunterstützung</span><span class="sxs-lookup"><span data-stu-id="e0c97-115">Specification Support</span></span>  | <span data-ttu-id="e0c97-116">PNG-Spezifikation 1.2</span><span class="sxs-lookup"><span data-stu-id="e0c97-116">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="e0c97-117">In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen PNG-Codeckomponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0c97-117">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="e0c97-118">Komponente</span><span class="sxs-lookup"><span data-stu-id="e0c97-118">Component</span></span>        | <span data-ttu-id="e0c97-119">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="e0c97-119">Friendly Name</span></span>            | <span data-ttu-id="e0c97-120">GUID</span><span class="sxs-lookup"><span data-stu-id="e0c97-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="e0c97-121">Containerformat</span><span class="sxs-lookup"><span data-stu-id="e0c97-121">Container Format</span></span> | <span data-ttu-id="e0c97-122">GUID \_ ContainerFormatPng</span><span class="sxs-lookup"><span data-stu-id="e0c97-122">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="e0c97-123">1b7cfaf4-713f-473c-mussd6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="e0c97-123">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="e0c97-124">Decoder</span><span class="sxs-lookup"><span data-stu-id="e0c97-124">Decoder</span></span>          | <span data-ttu-id="e0c97-125">CLSID \_ WICPngDecoder</span><span class="sxs-lookup"><span data-stu-id="e0c97-125">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="e0c97-126">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="e0c97-126">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="e0c97-127">Encoder</span><span class="sxs-lookup"><span data-stu-id="e0c97-127">Encoder</span></span>          | <span data-ttu-id="e0c97-128">CLSID \_ WICPngEncoder</span><span class="sxs-lookup"><span data-stu-id="e0c97-128">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="e0c97-129">27949969-876a-41d7-9447568f6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="e0c97-129">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="e0c97-130">Windows 8 und höher</span><span class="sxs-lookup"><span data-stu-id="e0c97-130">Windows 8 and later</span></span>

<span data-ttu-id="e0c97-131">Ab Windows 8 WIC wird ein zusätzlicher PNG-Decoder bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e0c97-131">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="e0c97-132">Codierung</span><span class="sxs-lookup"><span data-stu-id="e0c97-132">Encoding</span></span>

<span data-ttu-id="e0c97-133">Die WIC-Codierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="e0c97-133">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="e0c97-134">Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="e0c97-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="e0c97-135">Encoderoptionen</span><span class="sxs-lookup"><span data-stu-id="e0c97-135">Encoder Options</span></span>

<span data-ttu-id="e0c97-136">WIC-fähige Codecs unterscheiden sich auf Codierungsoptionenebene.</span><span class="sxs-lookup"><span data-stu-id="e0c97-136">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="e0c97-137">Encoderoptionen spiegeln die Funktionen eines Bildencoders wider, und jeder native Codec unterstützt eine Reihe dieser Encoderoptionen.</span><span class="sxs-lookup"><span data-stu-id="e0c97-137">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="e0c97-138">Encoderoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes (jedoch nicht unbedingt unterstützt) oder codecspezifische Optionen verfügbar sind, die vom Bildformatcodec entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="e0c97-138">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="e0c97-139">Um diese Codierungsoptionen während des Codierungsprozesses zu verwalten, verwendet WIC die [**IPropertyBag2-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e0c97-139">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="e0c97-140">Weitere Informationen zur Verwendung der **IPropertyBag2-Schnittstelle** für die WIC-Codierung finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="e0c97-140">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="e0c97-141">Der PNG-Codec verwendet grundlegende WIC-Encoderoptionen.</span><span class="sxs-lookup"><span data-stu-id="e0c97-141">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="e0c97-142">In der folgenden Tabelle sind die WIC-Encoderoptionen aufgeführt, die vom nativen PNG-Codec unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e0c97-142">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="e0c97-143">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="e0c97-143">Property Name</span></span>   | <span data-ttu-id="e0c97-144">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e0c97-144">VARTYPE</span></span>  | <span data-ttu-id="e0c97-145">Wertbereich</span><span class="sxs-lookup"><span data-stu-id="e0c97-145">Value Range</span></span>                                                 | <span data-ttu-id="e0c97-146">Standardwert</span><span class="sxs-lookup"><span data-stu-id="e0c97-146">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e0c97-147">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="e0c97-147">InterlaceOption</span></span> | <span data-ttu-id="e0c97-148">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="e0c97-148">VT\_BOOL</span></span> | <span data-ttu-id="e0c97-149">**TRUE** / **FALSE**</span><span class="sxs-lookup"><span data-stu-id="e0c97-149">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="e0c97-150">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="e0c97-150">**FALSE**</span></span>                                                        |
| <span data-ttu-id="e0c97-151">FilterOption</span><span class="sxs-lookup"><span data-stu-id="e0c97-151">FilterOption</span></span>    | <span data-ttu-id="e0c97-152">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="e0c97-152">VT\_UI1</span></span>  | [<span data-ttu-id="e0c97-153">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="e0c97-153">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="e0c97-154">**WICPngFilterUnspecified**</span><span class="sxs-lookup"><span data-stu-id="e0c97-154">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="e0c97-155">Wenn eine Encoderoption in der [**IPropertyBag2-Optionsliste**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) vorhanden ist, die der Codec nicht unterstützt, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e0c97-155">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="e0c97-156">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="e0c97-156">InterlaceOption</span></span>

<span data-ttu-id="e0c97-157">Gibt an, ob die Bilddaten als Interlacing codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e0c97-157">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="e0c97-158">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e0c97-158">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="e0c97-159">FilterOption</span><span class="sxs-lookup"><span data-stu-id="e0c97-159">FilterOption</span></span>

<span data-ttu-id="e0c97-160">Gibt die Filteroption an, die für die Bildkomprimierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0c97-160">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="e0c97-161">Der Standardwert ist [**WICPngFilterUnspecified.**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)</span><span class="sxs-lookup"><span data-stu-id="e0c97-161">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="e0c97-162">Decodierung</span><span class="sxs-lookup"><span data-stu-id="e0c97-162">Decoding</span></span>

<span data-ttu-id="e0c97-163">Die WIC-Decodierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="e0c97-163">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="e0c97-164">Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="e0c97-164">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="e0c97-165">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="e0c97-165">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="e0c97-166">Der native PNG-Codec unterstützt auch [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) bei der Framedecodierung und fügt erweiterte Optionen zum Decodieren eines Bilddatenstroms hinzu.</span><span class="sxs-lookup"><span data-stu-id="e0c97-166">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="e0c97-167">Weitere Informationen zu diesen erweiterten Optionen finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="e0c97-167">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
