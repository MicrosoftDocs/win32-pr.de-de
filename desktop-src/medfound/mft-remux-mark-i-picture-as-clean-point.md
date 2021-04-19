---
description: Gibt an, ob die e. 264-Video-REMUX-MFT I-Bilder als Clean Point markieren soll, um eine bessere Suchfunktion zu erzielen. Dadurch haben Sie die Möglichkeit, für Suchvorgänge in nicht konformen abschließenden MP4-Dateien Beschädigungen zu beschädigen.
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c9fe8398507f6d7af5d0e4bf45a36a4454f220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360183"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a><span data-ttu-id="cd483-104">MFT \_ REMUX \_ Mark \_ I \_ Bild \_ als \_ Clean \_ Point-Attribut</span><span class="sxs-lookup"><span data-stu-id="cd483-104">MFT\_REMUX\_MARK\_I\_PICTURE\_AS\_CLEAN\_POINT attribute</span></span>

<span data-ttu-id="cd483-105">Gibt an, ob die e. 264-Video-REMUX-MFT I-Bilder als Clean Point markieren soll, um eine bessere Suchfunktion zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="cd483-105">Specifies whether the H.264 video remux MFT should mark I pictures as clean point for better seek-ability.</span></span> <span data-ttu-id="cd483-106">Dadurch haben Sie die Möglichkeit, für Suchvorgänge in nicht konformen abschließenden MP4-Dateien Beschädigungen zu beschädigen.</span><span class="sxs-lookup"><span data-stu-id="cd483-106">This has the potential for corruptions on seeks in non-conforming final MP4 files.</span></span>

## <a name="data-type"></a><span data-ttu-id="cd483-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cd483-107">Data type</span></span>

<span data-ttu-id="cd483-108">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd483-108">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cd483-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd483-109">Remarks</span></span>

<span data-ttu-id="cd483-110">Das saubere Punkt Bild sollte per Definition komprimierte IDR-Bilder sein.</span><span class="sxs-lookup"><span data-stu-id="cd483-110">Clean point picture should be compressed IDR pictures by definition.</span></span>

<span data-ttu-id="cd483-111">Dies wird nicht empfohlen, um MP4-Dateien aufzuzeichnen oder erneut zu verarbeiten, es sei denn, eine solche Übung besteht darin, einige zwischen Pseudo-MP4-Dateien für die Videobearbeitung zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="cd483-111">This is not recommended for recording or remuxing MP4 files, unless such an exercise is to produce some intermediate pseudo MP4 files for video editing.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd483-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd483-112">Requirements</span></span>



| <span data-ttu-id="cd483-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd483-113">Requirement</span></span> | <span data-ttu-id="cd483-114">Wert</span><span class="sxs-lookup"><span data-stu-id="cd483-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd483-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd483-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cd483-116">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="cd483-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="cd483-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd483-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cd483-118">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="cd483-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="cd483-119">Header</span><span class="sxs-lookup"><span data-stu-id="cd483-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd483-120"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cd483-120"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd483-121">IDL</span><span class="sxs-lookup"><span data-stu-id="cd483-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cd483-122"><dt>"MF Transform. idl"</dt></span><span class="sxs-lookup"><span data-stu-id="cd483-122"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd483-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd483-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd483-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="cd483-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




