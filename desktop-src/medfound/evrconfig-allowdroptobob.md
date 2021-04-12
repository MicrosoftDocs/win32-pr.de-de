---
description: Ermöglicht dem erweiterten Videorenderer (EVR), die Leistung mithilfe von Bob Deinterlacing zu verbessern.
ms.assetid: e145e862-b987-4962-a94b-f8370bbcd5ac
title: EVRConfig_AllowDropToBob-Attribut (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3940edd0945999f7300060d963806e3572a5d0fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393266"
---
# <a name="evrconfig_allowdroptobob-attribute"></a><span data-ttu-id="8da1b-103">Evrconfig \_ allowdroptybob-Attribut</span><span class="sxs-lookup"><span data-stu-id="8da1b-103">EVRConfig\_AllowDropToBob attribute</span></span>

<span data-ttu-id="8da1b-104">Ermöglicht dem erweiterten Videorenderer (EVR), die Leistung mithilfe von Bob Deinterlacing zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="8da1b-104">Allows the Enhanced Video Renderer (EVR) to improve performance by using bob deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="8da1b-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8da1b-105">Data type</span></span>

<span data-ttu-id="8da1b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8da1b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="8da1b-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="8da1b-107">Get/set</span></span>

<span data-ttu-id="8da1b-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="8da1b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="8da1b-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="8da1b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="8da1b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8da1b-110">Remarks</span></span>

<span data-ttu-id="8da1b-111">Dieses Attribut kann für die evrmedia-Senke festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8da1b-111">This attribute can be set on the EVRmedia sink.</span></span> <span data-ttu-id="8da1b-112">Um das Attribut festzulegen, wird **QueryInterface** zum Abfragen der EVR-Medien Senke für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8da1b-112">To set the attribute, **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="8da1b-113">Das Festlegen dieses Attributs hat dieselbe Auswirkung wie das Festlegen des " **MF videomixprefs \_ allowdroptybob** "-Flags für den EVR.</span><span class="sxs-lookup"><span data-stu-id="8da1b-113">Setting this attribute has the same effect as setting the **MFVideoMixPrefs\_AllowDropToBob** flag on the EVR.</span></span> <span data-ttu-id="8da1b-114">Eine Beschreibung dieses Flags finden Sie unter [**MF videomixprefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) .</span><span class="sxs-lookup"><span data-stu-id="8da1b-114">See [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) for a description of this flag.</span></span>

<span data-ttu-id="8da1b-115">Die GUID-Konstante für dieses Attribut wird aus "straumiids. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="8da1b-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8da1b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8da1b-116">Requirements</span></span>



| <span data-ttu-id="8da1b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8da1b-117">Requirement</span></span> | <span data-ttu-id="8da1b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8da1b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8da1b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8da1b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8da1b-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8da1b-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8da1b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8da1b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8da1b-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8da1b-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8da1b-123">Header</span><span class="sxs-lookup"><span data-stu-id="8da1b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8da1b-124"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="8da1b-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8da1b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8da1b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da1b-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="8da1b-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8da1b-127">EVR-Attribute</span><span class="sxs-lookup"><span data-stu-id="8da1b-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="8da1b-128">Video Qualitäts Verwaltung</span><span class="sxs-lookup"><span data-stu-id="8da1b-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




