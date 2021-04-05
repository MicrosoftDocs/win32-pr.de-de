---
description: Dieses Thema enthält Informationen über den systemeigenen BMP-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Übersicht zum BMP-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3492189f80b43915bab94a7ea8359f2e5950f7c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756912"
---
# <a name="bmp-format-overview"></a><span data-ttu-id="9d327-103">Übersicht zum BMP-Format</span><span class="sxs-lookup"><span data-stu-id="9d327-103">BMP Format Overview</span></span>

<span data-ttu-id="9d327-104">Dieses Thema enthält Informationen über den systemeigenen BMP-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9d327-104">This topic provides information about the native BMP codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="9d327-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="9d327-105">Codec Identity</span></span>

<span data-ttu-id="9d327-106">In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9d327-106">The following table provides codec identification information.</span></span>



|                        |                       |
|------------------------|-----------------------|
| <span data-ttu-id="9d327-107">Formaler Name (n)</span><span class="sxs-lookup"><span data-stu-id="9d327-107">Formal Name(s)</span></span>         | <span data-ttu-id="9d327-108">Windows-Bitmap-Format</span><span class="sxs-lookup"><span data-stu-id="9d327-108">Windows Bitmap Format</span></span> |
| <span data-ttu-id="9d327-109">Dateinamenerweiterung (en)</span><span class="sxs-lookup"><span data-stu-id="9d327-109">File Name Extension(s)</span></span> | <span data-ttu-id="9d327-110">BMP, DIB</span><span class="sxs-lookup"><span data-stu-id="9d327-110">bmp, dib</span></span>              |
| <span data-ttu-id="9d327-111">MIME-Typ (MIME type)</span><span class="sxs-lookup"><span data-stu-id="9d327-111">MIME type</span></span>              | <span data-ttu-id="9d327-112">image/bmp</span><span class="sxs-lookup"><span data-stu-id="9d327-112">image/bmp</span></span>             |
| <span data-ttu-id="9d327-113">Spezifikations Unterstützung</span><span class="sxs-lookup"><span data-stu-id="9d327-113">Specification Support</span></span>  | <span data-ttu-id="9d327-114">BMP-Spezifikation V5</span><span class="sxs-lookup"><span data-stu-id="9d327-114">BMP Specification v5</span></span>  |



 

<span data-ttu-id="9d327-115">In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen BMP-Codec-Komponenten identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9d327-115">The following table lists the GUIDs used to identify the native BMP codec components.</span></span>



| <span data-ttu-id="9d327-116">Komponente</span><span class="sxs-lookup"><span data-stu-id="9d327-116">Component</span></span>        | <span data-ttu-id="9d327-117">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="9d327-117">Friendly Name</span></span>            | <span data-ttu-id="9d327-118">GUID</span><span class="sxs-lookup"><span data-stu-id="9d327-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="9d327-119">Container Format</span><span class="sxs-lookup"><span data-stu-id="9d327-119">Container Format</span></span> | <span data-ttu-id="9d327-120">GUID \_ containerformatbmp</span><span class="sxs-lookup"><span data-stu-id="9d327-120">GUID\_ContainerFormatBmp</span></span> | <span data-ttu-id="9d327-121">0af1d87e-Fcfe-4188-bdeba7906471cbe3</span><span class="sxs-lookup"><span data-stu-id="9d327-121">0af1d87e-fcfe-4188-bdeba7906471cbe3</span></span> |
| <span data-ttu-id="9d327-122">Decoder</span><span class="sxs-lookup"><span data-stu-id="9d327-122">Decoder</span></span>          | <span data-ttu-id="9d327-123">CLSID \_ wicbmpdecoder</span><span class="sxs-lookup"><span data-stu-id="9d327-123">CLSID\_WICBmpDecoder</span></span>     | <span data-ttu-id="9d327-124">6b462062-7cbf-400D-9F db813dd10f 2778</span><span class="sxs-lookup"><span data-stu-id="9d327-124">6b462062-7cbf-400d-9fdb813dd10f2778</span></span> |
| <span data-ttu-id="9d327-125">Encoder</span><span class="sxs-lookup"><span data-stu-id="9d327-125">Encoder</span></span>          | <span data-ttu-id="9d327-126">CLSID \_ wicbmpencoder</span><span class="sxs-lookup"><span data-stu-id="9d327-126">CLSID\_WICBmpEncoder</span></span>     | <span data-ttu-id="9d327-127">69be8bb4-d66d-47c8-865aed1589433782</span><span class="sxs-lookup"><span data-stu-id="9d327-127">69be8bb4-d66d-47c8-865aed1589433782</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="9d327-128">Codierung</span><span class="sxs-lookup"><span data-stu-id="9d327-128">Encoding</span></span>

<span data-ttu-id="9d327-129">Die WIC-Codierungs-API ist als Codec-unabhängig konzipiert und ist daher im Wesentlichen identisch mit der Bildcodierung für WIC-fähige Codecs.</span><span class="sxs-lookup"><span data-stu-id="9d327-129">The WIC encoding API are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="9d327-130">Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="9d327-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="9d327-131">Codierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="9d327-131">Encoder Options</span></span>

<span data-ttu-id="9d327-132">WIC-fähige Codecs unterscheiden sich auf der Codierungs Options Ebene.</span><span class="sxs-lookup"><span data-stu-id="9d327-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="9d327-133">Codierungsoptionen entsprechen den Funktionen eines Bild Encoders, und jeder Native Codec unterstützt eine Reihe dieser Codierungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="9d327-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="9d327-134">Codierungsoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (aber nicht unbedingt unterstützt werden), oder für Codec-spezifische Optionen, die vom Abbild Format</span><span class="sxs-lookup"><span data-stu-id="9d327-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="9d327-135">Zum Verwalten dieser Codierungsoptionen während des Codierungs Prozesses verwendet WIC die [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9d327-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="9d327-136">Weitere Informationen zur Verwendung der **IPropertyBag2** -Schnittstelle für die WIC-Codierung finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="9d327-136">For more information about using the **IPropertyBag2** interface for WIC encoding see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="9d327-137">In der folgenden Tabelle sind die vom systemeigenen BMP-Codec unterstützten WIC-Encoder-Optionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d327-137">The following table lists the WIC encoder options supported by the native BMP codec.</span></span>



| <span data-ttu-id="9d327-138">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="9d327-138">Property Name</span></span>               | <span data-ttu-id="9d327-139">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9d327-139">VARTYPE</span></span>      | <span data-ttu-id="9d327-140">Wertbereich</span><span class="sxs-lookup"><span data-stu-id="9d327-140">Value Range</span></span>                      | <span data-ttu-id="9d327-141">Standardwert</span><span class="sxs-lookup"><span data-stu-id="9d327-141">Default Value</span></span>      |
|-----------------------------|--------------|----------------------------------|--------------------|
| <span data-ttu-id="9d327-142">**EnableV5Header32bppBGRA**</span><span class="sxs-lookup"><span data-stu-id="9d327-142">**EnableV5Header32bppBGRA**</span></span> | <span data-ttu-id="9d327-143">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="9d327-143">**VT\_BOOL**</span></span> | <span data-ttu-id="9d327-144">**Variant \_ true/Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="9d327-144">**VARIANT\_TRUE/VARIANT\_FALSE**</span></span> | <span data-ttu-id="9d327-145">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="9d327-145">**VARIANT\_FALSE**</span></span> |



 

### <a name="enablev5header32bppbgra"></a><span data-ttu-id="9d327-146">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="9d327-146">EnableV5Header32bppBGRA</span></span>

<span data-ttu-id="9d327-147">Gibt an, ob das Codieren von Daten im GUID- \_ WICPixelFormat32bppBGRA Pixel Format zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="9d327-147">Specifies whether to allow encoding data in the GUID\_WICPixelFormat32bppBGRA pixel format.</span></span> <span data-ttu-id="9d327-148">Wenn diese Option auf **Variant \_ true** festgelegt ist, wird die BMP mit einem BITMAPV5HEADER-Header geschrieben.</span><span class="sxs-lookup"><span data-stu-id="9d327-148">If this option is set to **VARIANT\_TRUE**, the BMP will be written out with a BITMAPV5HEADER header.</span></span>

<span data-ttu-id="9d327-149">Der Standardwert ist **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="9d327-149">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="9d327-150">Wenn eine Encoder-Option in der IPropertyBag2-Optionsliste vorhanden ist, die der Codec nicht unterstützt, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9d327-150">If an encoder option is present in the IPropertyBag2 option list that the codec does not support, it is ignored.</span></span>

<span data-ttu-id="9d327-151">Hinweis bei Windows-BMP-Dateien mit 16-Bit-und 32-Bit-Dateien ignoriert der BMP-Codec alle Alphakanäle, da viele Legacy Bilddateien ungültige Daten in diesem zusätzlichen Kanal enthalten.</span><span class="sxs-lookup"><span data-stu-id="9d327-151">Note for 16-bit and 32-bit Windows BMP files, the BMP codec ignores any alpha channel, as many legacy image files contain invalid data in this extra channel.</span></span> <span data-ttu-id="9d327-152">Ab Windows 8 werden 32-Bit-Windows-BMP-Dateien, die mithilfe von **BITMAPV5HEADER** mit gültigem Alphakanal Inhalt geschrieben wurden, als WICPixelFormat32bppBGRA gelesen.</span><span class="sxs-lookup"><span data-stu-id="9d327-152">Starting with Windows 8, 32-bit Windows BMP files written using the **BITMAPV5HEADER** with valid alpha channel content are read as WICPixelFormat32bppBGRA</span></span>

## <a name="decoding"></a><span data-ttu-id="9d327-153">Decodierung</span><span class="sxs-lookup"><span data-stu-id="9d327-153">Decoding</span></span>

<span data-ttu-id="9d327-154">Die WIC-Decodierung-API ist als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="9d327-154">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="9d327-155">Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="9d327-155">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="9d327-156">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="9d327-156">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
