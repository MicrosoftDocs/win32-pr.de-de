---
description: Deaktiviert die Frameraten Konvertierung in der MFT des Video Prozessors.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: MF_XVP_DISABLE_FRC-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1922705514c51308138f9f301a3681e598ca6278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959142"
---
# <a name="mf_xvp_disable_frc-attribute"></a><span data-ttu-id="e67fd-103">MF \_ xvp \_ - \_ Attribut "FRC deaktivieren"</span><span class="sxs-lookup"><span data-stu-id="e67fd-103">MF\_XVP\_DISABLE\_FRC attribute</span></span>

<span data-ttu-id="e67fd-104">Deaktiviert die Frameraten Konvertierung in der [**MFT des Video Prozessors**](video-processor-mft.md).</span><span class="sxs-lookup"><span data-stu-id="e67fd-104">Disables frame-rate conversion in the [**Video Processor MFT**](video-processor-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="e67fd-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e67fd-105">Data type</span></span>

<span data-ttu-id="e67fd-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e67fd-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e67fd-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e67fd-107">Remarks</span></span>

<span data-ttu-id="e67fd-108">Wenn dieses Attribut **true** ist, führt der Videoprozessor keine Frameraten Konvertierung durch.</span><span class="sxs-lookup"><span data-stu-id="e67fd-108">If this attribute is **TRUE**, the video processor will not perform frame-rate conversion.</span></span> <span data-ttu-id="e67fd-109">Standardmäßig konvertiert der Videoprozessor die Framerate entsprechend dem Ausgabe Medientyp.</span><span class="sxs-lookup"><span data-stu-id="e67fd-109">By default, the video processor will convert the frame rate to match the output media type.</span></span>

<span data-ttu-id="e67fd-110">So legen Sie dieses Attribut fest:</span><span class="sxs-lookup"><span data-stu-id="e67fd-110">To set this attribute:</span></span>

1.  <span data-ttu-id="e67fd-111">Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Videoprozessor.</span><span class="sxs-lookup"><span data-stu-id="e67fd-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="e67fd-112">Rückrufe [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e67fd-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="e67fd-113">Legen Sie das-Attribut vor Beginn des Streamings fest.</span><span class="sxs-lookup"><span data-stu-id="e67fd-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="e67fd-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e67fd-114">Requirements</span></span>



| <span data-ttu-id="e67fd-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e67fd-115">Requirement</span></span> | <span data-ttu-id="e67fd-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e67fd-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e67fd-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e67fd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e67fd-118">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e67fd-118">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e67fd-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e67fd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e67fd-120">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e67fd-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e67fd-121">Header</span><span class="sxs-lookup"><span data-stu-id="e67fd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e67fd-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e67fd-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e67fd-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e67fd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e67fd-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e67fd-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




