---
description: Stellt Informationen zum nativen DDS-Codec bereit, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Übersicht über das DDS-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f860a5759218575acb53be5f2142e71aa34e9554
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444951"
---
# <a name="dds-format-overview"></a><span data-ttu-id="a30fa-103">Übersicht über das DDS-Format</span><span class="sxs-lookup"><span data-stu-id="a30fa-103">DDS Format Overview</span></span>

<span data-ttu-id="a30fa-104">Dieses Thema enthält Informationen zum nativen DDS-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a30fa-104">This topic provides information about the native DDS codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="a30fa-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="a30fa-105">Codec Identity</span></span>

<span data-ttu-id="a30fa-106">Die folgende Tabelle enthält Informationen zur Codecidentifikation.</span><span class="sxs-lookup"><span data-stu-id="a30fa-106">The following table provides codec identification information.</span></span>



| <span data-ttu-id="a30fa-107">Komponente</span><span class="sxs-lookup"><span data-stu-id="a30fa-107">Component</span></span>              | <span data-ttu-id="a30fa-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a30fa-108">Description</span></span>        |
|------------------------|--------------------|
| <span data-ttu-id="a30fa-109">Formale Namen</span><span class="sxs-lookup"><span data-stu-id="a30fa-109">Formal Name(s)</span></span>         | <span data-ttu-id="a30fa-110">DirectDraw Surface</span><span class="sxs-lookup"><span data-stu-id="a30fa-110">DirectDraw Surface</span></span> |
| <span data-ttu-id="a30fa-111">Dateinamenerweiterungen</span><span class="sxs-lookup"><span data-stu-id="a30fa-111">File Name Extension(s)</span></span> | <span data-ttu-id="a30fa-112">Dds</span><span class="sxs-lookup"><span data-stu-id="a30fa-112">dds</span></span>                |
| <span data-ttu-id="a30fa-113">MIME-Typ (MIME type)</span><span class="sxs-lookup"><span data-stu-id="a30fa-113">MIME type</span></span>              | <span data-ttu-id="a30fa-114">image/vnd-ms.dds</span><span class="sxs-lookup"><span data-stu-id="a30fa-114">image/vnd-ms.dds</span></span>   |



 

<span data-ttu-id="a30fa-115">In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen DDS-Codeckomponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a30fa-115">The following table lists the GUIDs used to identify the native DDS codec components.</span></span>



| <span data-ttu-id="a30fa-116">Komponente</span><span class="sxs-lookup"><span data-stu-id="a30fa-116">Component</span></span>        | <span data-ttu-id="a30fa-117">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="a30fa-117">Friendly Name</span></span>            | <span data-ttu-id="a30fa-118">GUID</span><span class="sxs-lookup"><span data-stu-id="a30fa-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="a30fa-119">Containerformat</span><span class="sxs-lookup"><span data-stu-id="a30fa-119">Container Format</span></span> | <span data-ttu-id="a30fa-120">GUID \_ ContainerFormatDds</span><span class="sxs-lookup"><span data-stu-id="a30fa-120">GUID\_ContainerFormatDds</span></span> | <span data-ttu-id="a30fa-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span><span class="sxs-lookup"><span data-stu-id="a30fa-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span></span> |
| <span data-ttu-id="a30fa-122">Decoder</span><span class="sxs-lookup"><span data-stu-id="a30fa-122">Decoder</span></span>          | <span data-ttu-id="a30fa-123">CLSID \_ WICDdsDecoder</span><span class="sxs-lookup"><span data-stu-id="a30fa-123">CLSID\_WICDdsDecoder</span></span>     | <span data-ttu-id="a30fa-124">9053699f-a341-429d-9e90ee437cf80c73</span><span class="sxs-lookup"><span data-stu-id="a30fa-124">9053699f-a341-429d-9e90ee437cf80c73</span></span> |
| <span data-ttu-id="a30fa-125">Encoder</span><span class="sxs-lookup"><span data-stu-id="a30fa-125">Encoder</span></span>          | <span data-ttu-id="a30fa-126">CLSID \_ WICDdsEncoder</span><span class="sxs-lookup"><span data-stu-id="a30fa-126">CLSID\_WICDdsEncoder</span></span>     | <span data-ttu-id="a30fa-127">a61dde94-66ce-4ac1-881b71680588895e</span><span class="sxs-lookup"><span data-stu-id="a30fa-127">a61dde94-66ce-4ac1-881b71680588895e</span></span> |



 

## <a name="pixel-format-support"></a><span data-ttu-id="a30fa-128">Pixelformatunterstützung</span><span class="sxs-lookup"><span data-stu-id="a30fa-128">Pixel Format Support</span></span>

<span data-ttu-id="a30fa-129">Beachten Sie, dass das DDS-Format jeden gültigen [**DXGI \_ FORMAT-Wert**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a30fa-129">Note that the DDS format supports any valid [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value.</span></span> <span data-ttu-id="a30fa-130">Der WIC-DDS-Codec unterstützt jedoch nur das Decodieren und Codieren von Dateien mit den folgenden Formaten:</span><span class="sxs-lookup"><span data-stu-id="a30fa-130">However, the WIC DDS codec only supports decoding and encoding files containing the following formats:</span></span>

-   <span data-ttu-id="a30fa-131">\_DXGI-FORMAT \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="a30fa-131">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="a30fa-132">DXGI \_ FORMAT \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="a30fa-132">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="a30fa-133">\_DXGI-FORMAT \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="a30fa-133">DXGI\_FORMAT\_BC3\_UNORM</span></span>

## <a name="encoding"></a><span data-ttu-id="a30fa-134">Codierung</span><span class="sxs-lookup"><span data-stu-id="a30fa-134">Encoding</span></span>

<span data-ttu-id="a30fa-135">Die WIC-Codierungs-APIs sind codecunabhängig. Daher ist die Bildcodierung für WIC-fähige Codecs im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="a30fa-135">The WIC encoding APIs are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="a30fa-136">Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="a30fa-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="a30fa-137">Das DDS-Dateiformat weist besondere Anforderungen auf, die sich aus der Unterstützung von Konzepten wie Mipmaps und Texturarrays ergeben.</span><span class="sxs-lookup"><span data-stu-id="a30fa-137">The DDS file format has unique requirements that arise from its support for concepts such as mipmaps and texture arrays.</span></span> <span data-ttu-id="a30fa-138">Um die Kontrolle über die DDS-Bildcodierung vollständig zu steuern, sollten Sie die [**IWICDdsEncoder-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) verwenden, um DDS-spezifische Codierungsparameter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a30fa-138">To fully exercise control over DDS image encoding, you should use the [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) interface to set DDS-specific encoding parameters.</span></span>

## <a name="decoding"></a><span data-ttu-id="a30fa-139">Decodierung</span><span class="sxs-lookup"><span data-stu-id="a30fa-139">Decoding</span></span>

<span data-ttu-id="a30fa-140">Die WIC-Decodierungs-APIs sind so konzipiert, dass sie codecunabhängig sind, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="a30fa-140">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="a30fa-141">Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="a30fa-141">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="a30fa-142">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="a30fa-142">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="block-compressed-data-access"></a><span data-ttu-id="a30fa-143">Blockieren des Zugriffs auf komprimierte Daten</span><span class="sxs-lookup"><span data-stu-id="a30fa-143">Block compressed data access</span></span>

<span data-ttu-id="a30fa-144">Zusätzlich zur Unterstützung der standardmäßigen WIC-Codecschnittstellen ermöglicht der DDS-Decoder mithilfe der DDS-spezifischen Schnittstellen [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) und [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode)direkten Zugriff auf die nativen komprimierten Blockdaten.</span><span class="sxs-lookup"><span data-stu-id="a30fa-144">In addition to supporting the standard WIC codec interfaces, the DDS decoder provides direct access to the native block compressed data using the DDS-specific interfaces, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) and [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span></span> <span data-ttu-id="a30fa-145">Um diese Schnittstellen zu verwenden, rufen Sie QueryInterface von [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) bzw. [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)auf.</span><span class="sxs-lookup"><span data-stu-id="a30fa-145">To use these interfaces, call QueryInterface off of [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectively.</span></span>

 

 
