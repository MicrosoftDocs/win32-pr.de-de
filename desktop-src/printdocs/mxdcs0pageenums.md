---
description: Die Enumeration "mxdc \_ S0 \_ Page \_ Enums" wird verwendet, um Typen von Ressourcen anzugeben, die Seiten in XPS-Dokumenten zugeordnet werden können und die von Microsoft XPS Document Converter (mxdc) an Ihre Ausgabe verarbeitet bzw. nicht verarbeitet werden können.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: MXDC_S0_PAGE_ENUMS-Enumeration (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1b4331210027f7fc23f36fb6b9d13a2c232ccbf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864959"
---
# <a name="mxdc_s0_page_enums-enumeration"></a><span data-ttu-id="7826e-103">Mxdc \_ S0 \_ - \_ Enumeration für Seiten Enumeration</span><span class="sxs-lookup"><span data-stu-id="7826e-103">MXDC\_S0\_PAGE\_ENUMS enumeration</span></span>

<span data-ttu-id="7826e-104">Die Enumeration " **mxdc \_ S0 \_ Page \_ Enums** " wird verwendet, um Typen von Ressourcen anzugeben, die Seiten in XPS-Dokumenten zugeordnet werden können und die von Microsoft XPS Document Converter (mxdc) an Ihre Ausgabe verarbeitet bzw. nicht verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="7826e-104">The **MXDC\_S0\_PAGE\_ENUMS** enumeration is used to specify types of resources that can be associated with pages in XPS documents and that can be processed, or passed unprocessed, by Microsoft XPS Document Converter (MXDC) to its output.</span></span>

## <a name="syntax"></a><span data-ttu-id="7826e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7826e-105">Syntax</span></span>


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a><span data-ttu-id="7826e-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="7826e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7826e-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**mxdc- \_ Ressource \_ ttf**</span><span class="sxs-lookup"><span data-stu-id="7826e-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC\_RESOURCE\_TTF**</span></span>
</dt> <dd>

<span data-ttu-id="7826e-108">TrueType-oder OpenType-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="7826e-108">TrueType or OpenType font.</span></span>

</dd> <dt>

<span data-ttu-id="7826e-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**mxdc- \_ Ressource \_ JPEG**</span><span class="sxs-lookup"><span data-stu-id="7826e-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC\_RESOURCE\_JPEG**</span></span>
</dt> <dd>

<span data-ttu-id="7826e-110">JPEG-Bild</span><span class="sxs-lookup"><span data-stu-id="7826e-110">JPEG image</span></span>

</dd> <dt>

<span data-ttu-id="7826e-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**mxdc- \_ Ressource \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="7826e-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC\_RESOURCE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="7826e-112">PNG-Bild</span><span class="sxs-lookup"><span data-stu-id="7826e-112">PNG image.</span></span>

</dd> <dt>

<span data-ttu-id="7826e-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**mxdc- \_ Ressource \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="7826e-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC\_RESOURCE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="7826e-114">TIFF-Bild</span><span class="sxs-lookup"><span data-stu-id="7826e-114">TIFF image.</span></span>

</dd> <dt>

<span data-ttu-id="7826e-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**mxdc- \_ Ressource ( \_ WDP)**</span><span class="sxs-lookup"><span data-stu-id="7826e-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC\_RESOURCE\_WDP**</span></span>
</dt> <dd>

<span data-ttu-id="7826e-116">Bild für Windows Media-Foto.</span><span class="sxs-lookup"><span data-stu-id="7826e-116">Windows Media Photo image.</span></span>

</dd> <dt>

<span data-ttu-id="7826e-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**mxdc- \_ Ressourcen \_ Wörterbuch**</span><span class="sxs-lookup"><span data-stu-id="7826e-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**MXDC\_RESOURCE\_DICTIONARY**</span></span>
</dt> <dd>

<span data-ttu-id="7826e-118">Das Remote Ressourcen Wörterbuch, das an die nicht verarbeitete Ausgabe von mxdc weitergeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7826e-118">Remote resource dictionary that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="7826e-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**mxdc- \_ Ressourcen- \_ ICC- \_ Profil**</span><span class="sxs-lookup"><span data-stu-id="7826e-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**MXDC\_RESOURCE\_ICC\_PROFILE**</span></span>
</dt> <dd>

<span data-ttu-id="7826e-120">Das ICC-Profil, das an die nicht verarbeitete Ausgabe von mxdc übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7826e-120">ICC profile that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="7826e-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**mxdc- \_ Ressource \_ JPEG- \_ Miniaturansicht**</span><span class="sxs-lookup"><span data-stu-id="7826e-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**MXDC\_RESOURCE\_JPEG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="7826e-122">JPEG-Miniaturansicht, die an die nicht verarbeitete Ausgabe von mxdc übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7826e-122">JPEG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="7826e-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**mxdc- \_ Ressource \_ PNG- \_ Miniaturansicht**</span><span class="sxs-lookup"><span data-stu-id="7826e-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**MXDC\_RESOURCE\_PNG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="7826e-124">PNG-Miniaturansicht, die an die nicht verarbeitete Ausgabe von mxdc übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7826e-124">PNG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="7826e-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**mxdc- \_ Ressource \_ Max**</span><span class="sxs-lookup"><span data-stu-id="7826e-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC\_RESOURCE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="7826e-126">Die maximale Ressourcen Anzahl für die Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="7826e-126">The maximum resource count for validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7826e-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7826e-127">Remarks</span></span>

<span data-ttu-id="7826e-128">Diese Enumeration wird hauptsächlich als **dwresourcetype** -Member der [**mxdc \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="7826e-128">This enumeration is primarily used as the **dwResourceType** member of the [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="7826e-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7826e-129">Requirements</span></span>



| <span data-ttu-id="7826e-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7826e-130">Requirement</span></span> | <span data-ttu-id="7826e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="7826e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7826e-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7826e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7826e-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7826e-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7826e-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7826e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7826e-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7826e-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7826e-136">Header</span><span class="sxs-lookup"><span data-stu-id="7826e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7826e-137"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7826e-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




