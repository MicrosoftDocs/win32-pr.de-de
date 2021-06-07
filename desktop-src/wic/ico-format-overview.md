---
description: Dieses Thema enthält Informationen zum nativen ICO-Codec, der über Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Übersicht über das ICO-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329a53a3b5d386c5e5386141162c608dc9db1ec0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444470"
---
# <a name="ico-format-overview"></a><span data-ttu-id="8aacb-103">Übersicht über das ICO-Format</span><span class="sxs-lookup"><span data-stu-id="8aacb-103">ICO Format Overview</span></span>

<span data-ttu-id="8aacb-104">Dieses Thema enthält Informationen zum nativen ICO-Codec, der über Windows-Bilderstellungskomponente (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8aacb-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="8aacb-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="8aacb-105">Codec Identity</span></span>

<span data-ttu-id="8aacb-106">Die folgende Tabelle enthält Informationen zur Codecidentifikation.</span><span class="sxs-lookup"><span data-stu-id="8aacb-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="8aacb-107">Komponente</span><span class="sxs-lookup"><span data-stu-id="8aacb-107">Component</span></span>            | <span data-ttu-id="8aacb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8aacb-108">Description</span></span>       |
|------------------------|-------------------|
| <span data-ttu-id="8aacb-109">Formale Namen</span><span class="sxs-lookup"><span data-stu-id="8aacb-109">Formal Name(s)</span></span>         | <span data-ttu-id="8aacb-110">Symbolformat (ICO)</span><span class="sxs-lookup"><span data-stu-id="8aacb-110">Icon Format (ICO)</span></span> |
| <span data-ttu-id="8aacb-111">Dateinamenerweiterungen</span><span class="sxs-lookup"><span data-stu-id="8aacb-111">File Name Extension(s)</span></span> | <span data-ttu-id="8aacb-112">Ico</span><span class="sxs-lookup"><span data-stu-id="8aacb-112">ico</span></span>               |
| <span data-ttu-id="8aacb-113">MIME-Typ (MIME type)</span><span class="sxs-lookup"><span data-stu-id="8aacb-113">MIME type</span></span>              | <span data-ttu-id="8aacb-114">image/ico</span><span class="sxs-lookup"><span data-stu-id="8aacb-114">image/ico</span></span>         |
| <span data-ttu-id="8aacb-115">Spezifikationsunterstützung</span><span class="sxs-lookup"><span data-stu-id="8aacb-115">Specification Support</span></span>  |                   |



 

<span data-ttu-id="8aacb-116">In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen ICO-Codeckomponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8aacb-116">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="8aacb-117">Komponente</span><span class="sxs-lookup"><span data-stu-id="8aacb-117">Component</span></span>        | <span data-ttu-id="8aacb-118">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="8aacb-118">Friendly Name</span></span>            | <span data-ttu-id="8aacb-119">GUID</span><span class="sxs-lookup"><span data-stu-id="8aacb-119">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="8aacb-120">Containerformat</span><span class="sxs-lookup"><span data-stu-id="8aacb-120">Container Format</span></span> | <span data-ttu-id="8aacb-121">GUID \_ ContainerFormatIco</span><span class="sxs-lookup"><span data-stu-id="8aacb-121">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="8aacb-122">a3a860c4-338f-4c17-919afba4b5628f21</span><span class="sxs-lookup"><span data-stu-id="8aacb-122">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="8aacb-123">Decoder</span><span class="sxs-lookup"><span data-stu-id="8aacb-123">Decoder</span></span>          | <span data-ttu-id="8aacb-124">CLSID \_ WICIcoDecoder</span><span class="sxs-lookup"><span data-stu-id="8aacb-124">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="8aacb-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="8aacb-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="8aacb-126">Encoder</span><span class="sxs-lookup"><span data-stu-id="8aacb-126">Encoder</span></span>          | <span data-ttu-id="8aacb-127">NICHT VERFÜGBAR</span><span class="sxs-lookup"><span data-stu-id="8aacb-127">NOT AVAILABLE</span></span>            | <span data-ttu-id="8aacb-128">NICHT VERFÜGBAR</span><span class="sxs-lookup"><span data-stu-id="8aacb-128">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="8aacb-129">Codierung</span><span class="sxs-lookup"><span data-stu-id="8aacb-129">Encoding</span></span>

<span data-ttu-id="8aacb-130">WIC stellt keinen nativen ICO-Imageencoder bereit.</span><span class="sxs-lookup"><span data-stu-id="8aacb-130">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="8aacb-131">Decodierung</span><span class="sxs-lookup"><span data-stu-id="8aacb-131">Decoding</span></span>

<span data-ttu-id="8aacb-132">Die WIC-Decodierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="8aacb-132">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="8aacb-133">Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="8aacb-133">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="8aacb-134">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="8aacb-134">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



