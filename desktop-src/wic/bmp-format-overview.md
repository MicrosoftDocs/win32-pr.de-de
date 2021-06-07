---
description: Dieses Thema enthält Informationen zum nativen BMP-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Übersicht über das BMP-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975f27af5b731ed1f62f3571109553848705239
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444961"
---
# <a name="bmp-format-overview"></a><span data-ttu-id="dcb44-103">Übersicht über das BMP-Format</span><span class="sxs-lookup"><span data-stu-id="dcb44-103">BMP Format Overview</span></span>

<span data-ttu-id="dcb44-104">Dieses Thema enthält Informationen zum nativen BMP-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="dcb44-104">This topic provides information about the native BMP codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="dcb44-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="dcb44-105">Codec Identity</span></span>

<span data-ttu-id="dcb44-106">Die folgende Tabelle enthält Informationen zur Codecidentifikation.</span><span class="sxs-lookup"><span data-stu-id="dcb44-106">The following table provides codec identification information.</span></span>



| <span data-ttu-id="dcb44-107">Komponente</span><span class="sxs-lookup"><span data-stu-id="dcb44-107">Component</span></span>              | <span data-ttu-id="dcb44-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcb44-108">Description</span></span>           |
|------------------------|-----------------------|
| <span data-ttu-id="dcb44-109">Formale Namen</span><span class="sxs-lookup"><span data-stu-id="dcb44-109">Formal Name(s)</span></span>         | <span data-ttu-id="dcb44-110">Windows Bitmap-Format</span><span class="sxs-lookup"><span data-stu-id="dcb44-110">Windows Bitmap Format</span></span> |
| <span data-ttu-id="dcb44-111">Dateinamenerweiterungen</span><span class="sxs-lookup"><span data-stu-id="dcb44-111">File Name Extension(s)</span></span> | <span data-ttu-id="dcb44-112">bmp, dib</span><span class="sxs-lookup"><span data-stu-id="dcb44-112">bmp, dib</span></span>              |
| <span data-ttu-id="dcb44-113">MIME-Typ (MIME type)</span><span class="sxs-lookup"><span data-stu-id="dcb44-113">MIME type</span></span>              | <span data-ttu-id="dcb44-114">image/bmp</span><span class="sxs-lookup"><span data-stu-id="dcb44-114">image/bmp</span></span>             |
| <span data-ttu-id="dcb44-115">Spezifikationsunterstützung</span><span class="sxs-lookup"><span data-stu-id="dcb44-115">Specification Support</span></span>  | <span data-ttu-id="dcb44-116">BMP-Spezifikation v5</span><span class="sxs-lookup"><span data-stu-id="dcb44-116">BMP Specification v5</span></span>  |



 

<span data-ttu-id="dcb44-117">In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen BMP-Codeckomponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dcb44-117">The following table lists the GUIDs used to identify the native BMP codec components.</span></span>



| <span data-ttu-id="dcb44-118">Komponente</span><span class="sxs-lookup"><span data-stu-id="dcb44-118">Component</span></span>        | <span data-ttu-id="dcb44-119">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="dcb44-119">Friendly Name</span></span>            | <span data-ttu-id="dcb44-120">GUID</span><span class="sxs-lookup"><span data-stu-id="dcb44-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="dcb44-121">Containerformat</span><span class="sxs-lookup"><span data-stu-id="dcb44-121">Container Format</span></span> | <span data-ttu-id="dcb44-122">GUID \_ ContainerFormatBmp</span><span class="sxs-lookup"><span data-stu-id="dcb44-122">GUID\_ContainerFormatBmp</span></span> | <span data-ttu-id="dcb44-123">0af1d87e-fcfe-4188-bdeba7906471cbe3</span><span class="sxs-lookup"><span data-stu-id="dcb44-123">0af1d87e-fcfe-4188-bdeba7906471cbe3</span></span> |
| <span data-ttu-id="dcb44-124">Decoder</span><span class="sxs-lookup"><span data-stu-id="dcb44-124">Decoder</span></span>          | <span data-ttu-id="dcb44-125">CLSID \_ WICBmpDecoder</span><span class="sxs-lookup"><span data-stu-id="dcb44-125">CLSID\_WICBmpDecoder</span></span>     | <span data-ttu-id="dcb44-126">6b462062-7cbf-400d-9fdb813dd10f2778</span><span class="sxs-lookup"><span data-stu-id="dcb44-126">6b462062-7cbf-400d-9fdb813dd10f2778</span></span> |
| <span data-ttu-id="dcb44-127">Encoder</span><span class="sxs-lookup"><span data-stu-id="dcb44-127">Encoder</span></span>          | <span data-ttu-id="dcb44-128">CLSID \_ WICBmpEncoder</span><span class="sxs-lookup"><span data-stu-id="dcb44-128">CLSID\_WICBmpEncoder</span></span>     | <span data-ttu-id="dcb44-129">69be8bb4-d66d-47c8-865aed1589433782</span><span class="sxs-lookup"><span data-stu-id="dcb44-129">69be8bb4-d66d-47c8-865aed1589433782</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="dcb44-130">Codierung</span><span class="sxs-lookup"><span data-stu-id="dcb44-130">Encoding</span></span>

<span data-ttu-id="dcb44-131">Die WIC-Codierungs-API ist so konzipiert, dass sie codecunabhängig ist. Daher ist die Bildcodierung für WIC-fähige Codecs im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="dcb44-131">The WIC encoding API are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="dcb44-132">Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="dcb44-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="dcb44-133">Encoderoptionen</span><span class="sxs-lookup"><span data-stu-id="dcb44-133">Encoder Options</span></span>

<span data-ttu-id="dcb44-134">WIC-fähige Codecs unterscheiden sich auf Codierungsoptionenebene.</span><span class="sxs-lookup"><span data-stu-id="dcb44-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="dcb44-135">Encoderoptionen spiegeln die Funktionen eines Bildencoders wider, und jeder native Codec unterstützt eine Reihe dieser Encoderoptionen.</span><span class="sxs-lookup"><span data-stu-id="dcb44-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="dcb44-136">Encoderoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes (jedoch nicht unbedingt unterstützt) oder codecspezifische Optionen verfügbar sind, die vom Bildformatcodec entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="dcb44-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="dcb44-137">Um diese Codierungsoptionen während des Codierungsprozesses zu verwalten, verwendet WIC die [**IPropertyBag2-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dcb44-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="dcb44-138">Weitere Informationen zur Verwendung der **IPropertyBag2-Schnittstelle** für die WIC-Codierung finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="dcb44-138">For more information about using the **IPropertyBag2** interface for WIC encoding see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="dcb44-139">In der folgenden Tabelle sind die WIC-Encoderoptionen aufgeführt, die vom nativen BMP-Codec unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="dcb44-139">The following table lists the WIC encoder options supported by the native BMP codec.</span></span>



| <span data-ttu-id="dcb44-140">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="dcb44-140">Property Name</span></span>               | <span data-ttu-id="dcb44-141">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="dcb44-141">VARTYPE</span></span>      | <span data-ttu-id="dcb44-142">Wertbereich</span><span class="sxs-lookup"><span data-stu-id="dcb44-142">Value Range</span></span>                      | <span data-ttu-id="dcb44-143">Standardwert</span><span class="sxs-lookup"><span data-stu-id="dcb44-143">Default Value</span></span>      |
|-----------------------------|--------------|----------------------------------|--------------------|
| <span data-ttu-id="dcb44-144">**EnableV5Header32bppBGRA**</span><span class="sxs-lookup"><span data-stu-id="dcb44-144">**EnableV5Header32bppBGRA**</span></span> | <span data-ttu-id="dcb44-145">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="dcb44-145">**VT\_BOOL**</span></span> | <span data-ttu-id="dcb44-146">**VARIANT \_ TRUE/VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="dcb44-146">**VARIANT\_TRUE/VARIANT\_FALSE**</span></span> | <span data-ttu-id="dcb44-147">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="dcb44-147">**VARIANT\_FALSE**</span></span> |



 

### <a name="enablev5header32bppbgra"></a><span data-ttu-id="dcb44-148">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="dcb44-148">EnableV5Header32bppBGRA</span></span>

<span data-ttu-id="dcb44-149">Gibt an, ob Codierungsdaten im \_ GUID-Format WICPixelFormat32bppBGRA-Pixel zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="dcb44-149">Specifies whether to allow encoding data in the GUID\_WICPixelFormat32bppBGRA pixel format.</span></span> <span data-ttu-id="dcb44-150">Wenn diese Option auf **VARIANT \_ TRUE** festgelegt ist, wird der BMP mit einem BITMAPV5HEADER-Header geschrieben.</span><span class="sxs-lookup"><span data-stu-id="dcb44-150">If this option is set to **VARIANT\_TRUE**, the BMP will be written out with a BITMAPV5HEADER header.</span></span>

<span data-ttu-id="dcb44-151">Der Standardwert ist **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="dcb44-151">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="dcb44-152">Wenn eine Encoderoption in der IPropertyBag2-Optionsliste vorhanden ist, die der Codec nicht unterstützt, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="dcb44-152">If an encoder option is present in the IPropertyBag2 option list that the codec does not support, it is ignored.</span></span>

<span data-ttu-id="dcb44-153">Beachten Sie, dass der BMP-Codec bei 16-Bit- und 32-Bit-Windows-BMP-Dateien alle Alphakanäle ignoriert, da viele Legacyimagedateien ungültige Daten in diesem zusätzlichen Kanal enthalten.</span><span class="sxs-lookup"><span data-stu-id="dcb44-153">Note for 16-bit and 32-bit Windows BMP files, the BMP codec ignores any alpha channel, as many legacy image files contain invalid data in this extra channel.</span></span> <span data-ttu-id="dcb44-154">Ab Windows 8 werden 32-Bit-Windows-BMP-Dateien, die mit **BITMAPV5HEADER** mit gültigem Alphakanalinhalt geschrieben wurden, als WICPixelFormat32bppBGRA gelesen.</span><span class="sxs-lookup"><span data-stu-id="dcb44-154">Starting with Windows 8, 32-bit Windows BMP files written using the **BITMAPV5HEADER** with valid alpha channel content are read as WICPixelFormat32bppBGRA</span></span>

## <a name="decoding"></a><span data-ttu-id="dcb44-155">Decodierung</span><span class="sxs-lookup"><span data-stu-id="dcb44-155">Decoding</span></span>

<span data-ttu-id="dcb44-156">Die WIC-Decodierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="dcb44-156">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="dcb44-157">Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="dcb44-157">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="dcb44-158">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="dcb44-158">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
