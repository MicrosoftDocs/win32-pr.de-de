---
description: Enthält Informationen über den systemeigenen DDS-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Übersicht über das DDS-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c45222a66d5a250caaf46db465d2359e09b3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348648"
---
# <a name="dds-format-overview"></a><span data-ttu-id="96da7-103">Übersicht über das DDS-Format</span><span class="sxs-lookup"><span data-stu-id="96da7-103">DDS Format Overview</span></span>

<span data-ttu-id="96da7-104">Dieses Thema enthält Informationen über den systemeigenen DDS-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="96da7-104">This topic provides information about the native DDS codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="96da7-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="96da7-105">Codec Identity</span></span>

<span data-ttu-id="96da7-106">In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="96da7-106">The following table provides codec identification information.</span></span>



|                        |                    |
|------------------------|--------------------|
| <span data-ttu-id="96da7-107">Formaler Name (n)</span><span class="sxs-lookup"><span data-stu-id="96da7-107">Formal Name(s)</span></span>         | <span data-ttu-id="96da7-108">DirectDraw-Oberfläche</span><span class="sxs-lookup"><span data-stu-id="96da7-108">DirectDraw Surface</span></span> |
| <span data-ttu-id="96da7-109">Dateinamenerweiterung (en)</span><span class="sxs-lookup"><span data-stu-id="96da7-109">File Name Extension(s)</span></span> | <span data-ttu-id="96da7-110">DDS</span><span class="sxs-lookup"><span data-stu-id="96da7-110">dds</span></span>                |
| <span data-ttu-id="96da7-111">MIME-Typ (MIME type)</span><span class="sxs-lookup"><span data-stu-id="96da7-111">MIME type</span></span>              | <span data-ttu-id="96da7-112">Image/vnd-ms. DDS</span><span class="sxs-lookup"><span data-stu-id="96da7-112">image/vnd-ms.dds</span></span>   |



 

<span data-ttu-id="96da7-113">In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen DDS-Codec-Komponenten identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="96da7-113">The following table lists the GUIDs used to identify the native DDS codec components.</span></span>



| <span data-ttu-id="96da7-114">Komponente</span><span class="sxs-lookup"><span data-stu-id="96da7-114">Component</span></span>        | <span data-ttu-id="96da7-115">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="96da7-115">Friendly Name</span></span>            | <span data-ttu-id="96da7-116">GUID</span><span class="sxs-lookup"><span data-stu-id="96da7-116">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="96da7-117">Container Format</span><span class="sxs-lookup"><span data-stu-id="96da7-117">Container Format</span></span> | <span data-ttu-id="96da7-118">GUID \_ containerformatdds</span><span class="sxs-lookup"><span data-stu-id="96da7-118">GUID\_ContainerFormatDds</span></span> | <span data-ttu-id="96da7-119">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span><span class="sxs-lookup"><span data-stu-id="96da7-119">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span></span> |
| <span data-ttu-id="96da7-120">Decoder</span><span class="sxs-lookup"><span data-stu-id="96da7-120">Decoder</span></span>          | <span data-ttu-id="96da7-121">CLSID \_ wicddsdecoder</span><span class="sxs-lookup"><span data-stu-id="96da7-121">CLSID\_WICDdsDecoder</span></span>     | <span data-ttu-id="96da7-122">9053699f-A341-429d-9e90ee437cf80c73</span><span class="sxs-lookup"><span data-stu-id="96da7-122">9053699f-a341-429d-9e90ee437cf80c73</span></span> |
| <span data-ttu-id="96da7-123">Encoder</span><span class="sxs-lookup"><span data-stu-id="96da7-123">Encoder</span></span>          | <span data-ttu-id="96da7-124">CLSID \_ wicddsencoder</span><span class="sxs-lookup"><span data-stu-id="96da7-124">CLSID\_WICDdsEncoder</span></span>     | <span data-ttu-id="96da7-125">a61dde94-66ce-4ac1-881b71680588895e</span><span class="sxs-lookup"><span data-stu-id="96da7-125">a61dde94-66ce-4ac1-881b71680588895e</span></span> |



 

## <a name="pixel-format-support"></a><span data-ttu-id="96da7-126">Unterstützung für Pixel Formate</span><span class="sxs-lookup"><span data-stu-id="96da7-126">Pixel Format Support</span></span>

<span data-ttu-id="96da7-127">Beachten Sie, dass das DDS-Format einen beliebigen gültigen [**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Wert unterstützt.</span><span class="sxs-lookup"><span data-stu-id="96da7-127">Note that the DDS format supports any valid [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value.</span></span> <span data-ttu-id="96da7-128">Der WIC-DDS-Codec unterstützt jedoch nur das Decodieren und Codieren von Dateien, die die folgenden Formate enthalten:</span><span class="sxs-lookup"><span data-stu-id="96da7-128">However, the WIC DDS codec only supports decoding and encoding files containing the following formats:</span></span>

-   <span data-ttu-id="96da7-129">DXGI- \_ Format \_ BC1 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="96da7-129">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="96da7-130">DXGI- \_ Format \_ BC2 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="96da7-130">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="96da7-131">DXGI- \_ Format \_ BC3 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="96da7-131">DXGI\_FORMAT\_BC3\_UNORM</span></span>

## <a name="encoding"></a><span data-ttu-id="96da7-132">Codierung</span><span class="sxs-lookup"><span data-stu-id="96da7-132">Encoding</span></span>

<span data-ttu-id="96da7-133">Die WIC-Codierungs-APIs sind als Codec-unabhängig konzipiert, daher ist die Bildcodierung für WIC-fähige Codecs im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="96da7-133">The WIC encoding APIs are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="96da7-134">Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="96da7-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="96da7-135">Das DDS-Dateiformat weist besondere Anforderungen auf, die aus der Unterstützung von Konzepten wie Mipmaps und Textur Arrays entstehen.</span><span class="sxs-lookup"><span data-stu-id="96da7-135">The DDS file format has unique requirements that arise from its support for concepts such as mipmaps and texture arrays.</span></span> <span data-ttu-id="96da7-136">Um die Kontrolle über die DDS-Bildcodierung vollständig zu steuern, sollten Sie die [**iwicddsencoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) -Schnittstelle verwenden, um DDS-spezifische Codierungs Parameter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="96da7-136">To fully exercise control over DDS image encoding, you should use the [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) interface to set DDS-specific encoding parameters.</span></span>

## <a name="decoding"></a><span data-ttu-id="96da7-137">Decodierung</span><span class="sxs-lookup"><span data-stu-id="96da7-137">Decoding</span></span>

<span data-ttu-id="96da7-138">Die WIC-Decodierung-APIs sind als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="96da7-138">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="96da7-139">Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="96da7-139">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="96da7-140">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="96da7-140">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="block-compressed-data-access"></a><span data-ttu-id="96da7-141">Komprimierten Datenzugriff blockieren</span><span class="sxs-lookup"><span data-stu-id="96da7-141">Block compressed data access</span></span>

<span data-ttu-id="96da7-142">Zusätzlich zur Unterstützung der standardmäßigen WIC-Codec-Schnittstellen ermöglicht der DDS-Decoder den direkten Zugriff auf die systemeigenen Block komprimierten Daten mithilfe der DDS-spezifischen Schnittstellen [**iwicddsdecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) und [**iwicddsframedecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span><span class="sxs-lookup"><span data-stu-id="96da7-142">In addition to supporting the standard WIC codec interfaces, the DDS decoder provides direct access to the native block compressed data using the DDS-specific interfaces, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) and [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span></span> <span data-ttu-id="96da7-143">Um diese Schnittstellen zu verwenden, wird QueryInterface von [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) bzw. [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="96da7-143">To use these interfaces, call QueryInterface off of [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectively.</span></span>

 

 
