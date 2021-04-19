---
description: Dieses Thema enthält Informationen über den nativen ICO-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Übersicht über ICO-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d370497e9231d6deb8d1793a26a53565b5cd99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360814"
---
# <a name="ico-format-overview"></a><span data-ttu-id="8ddb2-103">Übersicht über ICO-Format</span><span class="sxs-lookup"><span data-stu-id="8ddb2-103">ICO Format Overview</span></span>

<span data-ttu-id="8ddb2-104">Dieses Thema enthält Informationen über den nativen ICO-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8ddb2-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="8ddb2-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="8ddb2-105">Codec Identity</span></span>

<span data-ttu-id="8ddb2-106">In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8ddb2-106">The following table provides codec identification information.</span></span>



|                        |                   |
|------------------------|-------------------|
| <span data-ttu-id="8ddb2-107">Formaler Name (n)</span><span class="sxs-lookup"><span data-stu-id="8ddb2-107">Formal Name(s)</span></span>         | <span data-ttu-id="8ddb2-108">Symbol Format (ICO)</span><span class="sxs-lookup"><span data-stu-id="8ddb2-108">Icon Format (ICO)</span></span> |
| <span data-ttu-id="8ddb2-109">Dateinamenerweiterung (en)</span><span class="sxs-lookup"><span data-stu-id="8ddb2-109">File Name Extension(s)</span></span> | <span data-ttu-id="8ddb2-110">ICO</span><span class="sxs-lookup"><span data-stu-id="8ddb2-110">ico</span></span>               |
| <span data-ttu-id="8ddb2-111">MIME-Typ (MIME type)</span><span class="sxs-lookup"><span data-stu-id="8ddb2-111">MIME type</span></span>              | <span data-ttu-id="8ddb2-112">Image/ICO</span><span class="sxs-lookup"><span data-stu-id="8ddb2-112">image/ico</span></span>         |
| <span data-ttu-id="8ddb2-113">Spezifikations Unterstützung</span><span class="sxs-lookup"><span data-stu-id="8ddb2-113">Specification Support</span></span>  |                   |



 

<span data-ttu-id="8ddb2-114">In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen ICO-Codec-Komponenten identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="8ddb2-114">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="8ddb2-115">Komponente</span><span class="sxs-lookup"><span data-stu-id="8ddb2-115">Component</span></span>        | <span data-ttu-id="8ddb2-116">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="8ddb2-116">Friendly Name</span></span>            | <span data-ttu-id="8ddb2-117">GUID</span><span class="sxs-lookup"><span data-stu-id="8ddb2-117">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="8ddb2-118">Container Format</span><span class="sxs-lookup"><span data-stu-id="8ddb2-118">Container Format</span></span> | <span data-ttu-id="8ddb2-119">GUID \_ containerformatico</span><span class="sxs-lookup"><span data-stu-id="8ddb2-119">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="8ddb2-120">a3a860c4-338f-4c17-919afba4b5628f</span><span class="sxs-lookup"><span data-stu-id="8ddb2-120">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="8ddb2-121">Decoder</span><span class="sxs-lookup"><span data-stu-id="8ddb2-121">Decoder</span></span>          | <span data-ttu-id="8ddb2-122">CLSID- \_ wicikodecoder</span><span class="sxs-lookup"><span data-stu-id="8ddb2-122">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="8ddb2-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="8ddb2-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="8ddb2-124">Encoder</span><span class="sxs-lookup"><span data-stu-id="8ddb2-124">Encoder</span></span>          | <span data-ttu-id="8ddb2-125">NICHT VERFÜGBAR</span><span class="sxs-lookup"><span data-stu-id="8ddb2-125">NOT AVAILABLE</span></span>            | <span data-ttu-id="8ddb2-126">NICHT VERFÜGBAR</span><span class="sxs-lookup"><span data-stu-id="8ddb2-126">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="8ddb2-127">Codierung</span><span class="sxs-lookup"><span data-stu-id="8ddb2-127">Encoding</span></span>

<span data-ttu-id="8ddb2-128">WIC stellt keinen systemeigenen ICO-Image Encoder bereit.</span><span class="sxs-lookup"><span data-stu-id="8ddb2-128">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="8ddb2-129">Decodierung</span><span class="sxs-lookup"><span data-stu-id="8ddb2-129">Decoding</span></span>

<span data-ttu-id="8ddb2-130">Die WIC-Decodierung-API ist als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="8ddb2-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="8ddb2-131">Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="8ddb2-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="8ddb2-132">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="8ddb2-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



