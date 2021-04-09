---
description: Dieses Attribut gibt zusätzlichen Schutz an, der von einer Video-Output Trust Authority (OTA) geboten wird, wenn ein Connector keinen Ausgabe Schutz bietet.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: MFPROTECTION_CONSTRICTVIDEO_NOOPM-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617bd629852a3aa03708d12dca7736b4f773094b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959241"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a><span data-ttu-id="01c06-103">Noopm-Attribut für MF Protection- \_ \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="01c06-103">MFPROTECTION\_CONSTRICTVIDEO\_NOOPM attribute</span></span>

<span data-ttu-id="01c06-104">Dieses Attribut gibt zusätzlichen Schutz an, der von einer Video-Output Trust Authority (OTA) geboten wird, wenn ein Connector keinen Ausgabe Schutz bietet.</span><span class="sxs-lookup"><span data-stu-id="01c06-104">This attribute specifies additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="01c06-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="01c06-105">Data type</span></span>

<span data-ttu-id="01c06-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="01c06-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="01c06-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01c06-107">Remarks</span></span>

<span data-ttu-id="01c06-108">Dies ist ein zusätzlicher Schutz, der von einer Video-Output Trust Authority (OTA) geboten wird, wenn ein Connector keinen Ausgabe Schutz bietet (siehe [**IMF outputtrustauthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)).</span><span class="sxs-lookup"><span data-stu-id="01c06-108">This is an additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection (see [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)).</span></span> <span data-ttu-id="01c06-109">In diesem Fall bietet das OTA ggf. diesen Schutz, dessen Auswirkung mit dem Schutz durch den Schutz durch den [mfprotection-Schutz \_ überein](mfprotection-constrictvideo.md) stimmt.</span><span class="sxs-lookup"><span data-stu-id="01c06-109">In this case the OTA may offer this protection whose effect is the same as the [MFPROTECTION\_CONSTRICTVIDEO](mfprotection-constrictvideo.md) protection.</span></span> <span data-ttu-id="01c06-110">Dies wird definiert, um Verwechslungen mit vorherigen Aufrufen von [**imfoutputpolicy:: generaterequiredschemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) -Interaktionen zu vermeiden, bei denen das vorhanden sein von "mfprotection" \_ für den Connector "Windows-Manager" verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="01c06-110">This is defined to avoid confusion with previous calls to [**IMFOutputPolicy::GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) interactions where the presence of MFPROTECTION\_CONSTRICTVIDEO protection was used to help identify the desktop window manager pseudo-connector.</span></span>

## <a name="requirements"></a><span data-ttu-id="01c06-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01c06-111">Requirements</span></span>



| <span data-ttu-id="01c06-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01c06-112">Requirement</span></span> | <span data-ttu-id="01c06-113">Wert</span><span class="sxs-lookup"><span data-stu-id="01c06-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01c06-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01c06-114">Minimum supported client</span></span><br/> | <span data-ttu-id="01c06-115">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="01c06-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="01c06-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01c06-116">Minimum supported server</span></span><br/> | <span data-ttu-id="01c06-117">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01c06-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="01c06-118">Header</span><span class="sxs-lookup"><span data-stu-id="01c06-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="01c06-119"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="01c06-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01c06-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01c06-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c06-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="01c06-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




