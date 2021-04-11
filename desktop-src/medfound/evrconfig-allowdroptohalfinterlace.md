---
description: Ermöglicht dem erweiterten Videorenderer (EVR), die Leistung zu verbessern, indem das zweite Feld jedes Zeilen Sprung Rahmens übersprungen wird.
ms.assetid: de7efc6a-19ae-4f3a-8675-38fda3c979e2
title: EVRConfig_AllowDropToHalfInterlace-Attribut (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9989fe833ea763166ba870c331add5c18bcb45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214310"
---
# <a name="evrconfig_allowdroptohalfinterlace-attribute"></a><span data-ttu-id="5f36f-103">Evrconfig \_ allowdroptyfinterlace-Attribut</span><span class="sxs-lookup"><span data-stu-id="5f36f-103">EVRConfig\_AllowDropToHalfInterlace attribute</span></span>

<span data-ttu-id="5f36f-104">Ermöglicht dem erweiterten Videorenderer (EVR), die Leistung zu verbessern, indem das zweite Feld jedes Zeilen Sprung Rahmens übersprungen wird.</span><span class="sxs-lookup"><span data-stu-id="5f36f-104">Allows the Enhanced Video Renderer (EVR) to improve performance by skipping the second field of every interlaced frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="5f36f-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5f36f-105">Data type</span></span>

<span data-ttu-id="5f36f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5f36f-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="5f36f-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="5f36f-107">Get/set</span></span>

<span data-ttu-id="5f36f-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5f36f-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5f36f-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="5f36f-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="5f36f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f36f-110">Remarks</span></span>

<span data-ttu-id="5f36f-111">Dieses Attribut kann in der EVR-Medien Senke festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5f36f-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="5f36f-112">Zum Festlegen des-Attributs verwenden Sie **QueryInterface** , um die EVR-Medien Senke für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle abzufragen.</span><span class="sxs-lookup"><span data-stu-id="5f36f-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="5f36f-113">Das Festlegen dieses Attributs hat dieselbe Auswirkung wie das Festlegen des " **MF videomixprefs \_ allowdroponhalfinterlace** "-Flags für den EVR.</span><span class="sxs-lookup"><span data-stu-id="5f36f-113">Setting this attribute has the same effect as setting the **MFVideoMixPrefs\_AllowDropToHalfInterlace** flag on the EVR.</span></span> <span data-ttu-id="5f36f-114">Eine Beschreibung dieses Flags finden Sie unter [**MF videomixprefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) .</span><span class="sxs-lookup"><span data-stu-id="5f36f-114">See [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) for a description of this flag.</span></span>

<span data-ttu-id="5f36f-115">Die GUID-Konstante für dieses Attribut wird aus "straumiids. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="5f36f-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f36f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f36f-116">Requirements</span></span>



| <span data-ttu-id="5f36f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f36f-117">Requirement</span></span> | <span data-ttu-id="5f36f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5f36f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5f36f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f36f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f36f-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f36f-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5f36f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f36f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f36f-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f36f-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5f36f-123">Header</span><span class="sxs-lookup"><span data-stu-id="5f36f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f36f-124"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f36f-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f36f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f36f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f36f-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="5f36f-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5f36f-127">EVR-Attribute</span><span class="sxs-lookup"><span data-stu-id="5f36f-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="5f36f-128">Video Qualitäts Verwaltung</span><span class="sxs-lookup"><span data-stu-id="5f36f-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




