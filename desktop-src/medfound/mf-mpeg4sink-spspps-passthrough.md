---
description: Gibt an, ob die MPEG-4-Datei Senke Sequence Parameter Set (SPS) und Picture Parameter Set (PPS) nalus filtert.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: MF_MPEG4SINK_SPSPPS_PASSTHROUGH-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754273"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a><span data-ttu-id="9d9be-103">MF \_ MPEG4SINK \_ spspps- \_ Passthrough-Attribut</span><span class="sxs-lookup"><span data-stu-id="9d9be-103">MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute</span></span>

<span data-ttu-id="9d9be-104">Gibt an, ob die [**MPEG-4-Datei Senke**](mpeg-4-file-sink.md) Sequence Parameter Set (SPS) und Picture Parameter Set (PPS) nalus filtert.</span><span class="sxs-lookup"><span data-stu-id="9d9be-104">Specifies whether the [**MPEG-4 File Sink**](mpeg-4-file-sink.md) filters out sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

## <a name="data-type"></a><span data-ttu-id="9d9be-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9d9be-105">Data type</span></span>

<span data-ttu-id="9d9be-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d9be-106">**BOOL** stored as **UINT32**</span></span>

## <a name="applies-to"></a><span data-ttu-id="9d9be-107">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="9d9be-107">Applies to</span></span>

[<span data-ttu-id="9d9be-108">**Imfmediasink**</span><span class="sxs-lookup"><span data-stu-id="9d9be-108">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a><span data-ttu-id="9d9be-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d9be-109">Remarks</span></span>

<span data-ttu-id="9d9be-110">Die [**MPEG-4-Datei Senke**](mpeg-4-file-sink.md) schreibt die SPS-und PPS-Parameter in das Feld für die Beispiel Beschreibung der MP4-Datei.</span><span class="sxs-lookup"><span data-stu-id="9d9be-110">The [**MPEG-4 File Sink**](mpeg-4-file-sink.md) writes the SPS and PPS parameters into the sample description box of the MP4 file.</span></span> <span data-ttu-id="9d9be-111">Standardmäßig werden SPS und PPS nalus aus dem Videostream herausgefiltert.</span><span class="sxs-lookup"><span data-stu-id="9d9be-111">By default, it filters out the SPS and PPS NALUs from the video stream.</span></span> <span data-ttu-id="9d9be-112">Um dieses Verhalten zu überschreiben, legen \_ Sie das Attribut "MF MPEG4SINK \_ spspps \_ Passthrough" auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="9d9be-112">To override this behavior, set the MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d9be-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d9be-113">Requirements</span></span>



| <span data-ttu-id="9d9be-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d9be-114">Requirement</span></span> | <span data-ttu-id="9d9be-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9d9be-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9d9be-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d9be-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9d9be-117">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9d9be-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="9d9be-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d9be-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9d9be-119">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9d9be-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="9d9be-120">Header</span><span class="sxs-lookup"><span data-stu-id="9d9be-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d9be-121"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d9be-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d9be-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d9be-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d9be-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9d9be-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




