---
description: Gibt an, ob der topologielader den Transcode-Video Prozessor (xvp) aktiviert. für Konvertierungen, Aktivieren der Hardware beschleunigten Farbkonvertierung.
title: MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK-Attribut (mspdl. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: e36841db57e8343248ef5e369915d4bc357815bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350629"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a><span data-ttu-id="b0bf3-104">MF- \_ Topologie \_ \_ xvp \_ für \_ Wiedergabe Attribut aktivieren</span><span class="sxs-lookup"><span data-stu-id="b0bf3-104">MF\_TOPOLOGY\_ENABLE\_XVP\_FOR\_PLAYBACK attribute</span></span>

<span data-ttu-id="b0bf3-105">Gibt an, ob der topologielader den Transcode-Video Prozessor (xvp) aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b0bf3-105">Specifies whether the topology loader enables the Transcode Video Processor (XVP).</span></span> <span data-ttu-id="b0bf3-106">für Konvertierungen, Aktivieren der Hardware beschleunigten Farbkonvertierung.</span><span class="sxs-lookup"><span data-stu-id="b0bf3-106">for conversions, enabling hardware accelerated color conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="b0bf3-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b0bf3-107">Data type</span></span>

<span data-ttu-id="b0bf3-108">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0bf3-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b0bf3-109">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="b0bf3-109">Get/set</span></span>

<span data-ttu-id="b0bf3-110">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b0bf3-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b0bf3-111">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b0bf3-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b0bf3-112">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="b0bf3-112">Applies to</span></span>

[<span data-ttu-id="b0bf3-113">**Imftopology**</span><span class="sxs-lookup"><span data-stu-id="b0bf3-113">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="b0bf3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0bf3-114">Remarks</span></span>

<span data-ttu-id="b0bf3-115">Wenn dieses Attribut festgelegt ist, ruft das topologielader ggf. bei Bedarf während der nicht-transcode-topologieauflösung einen Pull in den Videoprozessor ab.</span><span class="sxs-lookup"><span data-stu-id="b0bf3-115">If this attribute is set, the topology loader will pull in the video processor, if necessary, during non-transcode topology resolution.</span></span> <span data-ttu-id="b0bf3-116">Wenn Sie die Topologie zum Erstellen einer eigenen [imftopologie](/windows/win32/api/mfidl/nn-mfidl-imftopology) verwenden, weist das Attribut das Lade Modul an, anstelle des Legacy Farb Konverters xvp für Konvertierungen zu verwenden, sodass die hardwarebeschleunigte Farbkonvertierung aktiviert werden kann. der Legacy Farb Konverter ist nur Software.</span><span class="sxs-lookup"><span data-stu-id="b0bf3-116">When you are using the topology to build your own [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) this attribute tells the loader to use XVP for conversions instead of the legacy color converter, thus enabling hardware accelerated color conversion; the legacy color converter is software-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0bf3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0bf3-117">Requirements</span></span>



| <span data-ttu-id="b0bf3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0bf3-118">Requirement</span></span> | <span data-ttu-id="b0bf3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b0bf3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0bf3-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0bf3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b0bf3-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0bf3-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b0bf3-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0bf3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b0bf3-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0bf3-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b0bf3-124">Header</span><span class="sxs-lookup"><span data-stu-id="b0bf3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0bf3-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0bf3-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0bf3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0bf3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0bf3-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b0bf3-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b0bf3-128">Direct3D Device Manager</span><span class="sxs-lookup"><span data-stu-id="b0bf3-128">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="b0bf3-129">Topologieattribute</span><span class="sxs-lookup"><span data-stu-id="b0bf3-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




