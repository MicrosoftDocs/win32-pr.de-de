---
description: Gibt an, ob der Aufrufer die für die Ausgabe verwendeten Texturen zuweist.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: MF_XVP_CALLER_ALLOCATES_OUTPUT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527395"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a><span data-ttu-id="464b8-103">MF \_ xvp \_ Caller \_ weist das \_ Ausgabe Attribut zu</span><span class="sxs-lookup"><span data-stu-id="464b8-103">MF\_XVP\_CALLER\_ALLOCATES\_OUTPUT attribute</span></span>

<span data-ttu-id="464b8-104">Gibt an, ob der Aufrufer die für die Ausgabe verwendeten Texturen zuweist.</span><span class="sxs-lookup"><span data-stu-id="464b8-104">Specifies whether that the caller will allocate the textures used for output.</span></span>

## <a name="data-type"></a><span data-ttu-id="464b8-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="464b8-105">Data type</span></span>

<span data-ttu-id="464b8-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="464b8-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="464b8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="464b8-107">Remarks</span></span>

<span data-ttu-id="464b8-108">Wenn dieses Attribut den Wert **true** hat, erwartet der Videoprozessor, dass Ausgabe Texturen vom Aufrufer zugeordnet werden, auch wenn er im DXVA-Modus (DirectX Video Acceleration) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="464b8-108">If this attribute is **TRUE**, the video processor expect output textures to be allocated by the caller, even when operating in DirectX Video Acceleration (DXVA) mode.</span></span> <span data-ttu-id="464b8-109">Wenn dieses Attribut den Wert **false** hat, weist der Videoprozessor die Ausgabe Texturen beim Betrieb im DXVA-Modus zu und schlägt fehl, wenn vom Aufrufer bereitgestellte Ausgabe Texturen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="464b8-109">If this attribute is **FALSE**, the video processor will allocate the output textures when operating in DXVA mode, and will fail if caller provided output textures are provided.</span></span>

<span data-ttu-id="464b8-110">So legen Sie dieses Attribut fest:</span><span class="sxs-lookup"><span data-stu-id="464b8-110">To set this attribute:</span></span>

1.  <span data-ttu-id="464b8-111">Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Videoprozessor.</span><span class="sxs-lookup"><span data-stu-id="464b8-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="464b8-112">Rückrufe [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="464b8-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="464b8-113">Legen Sie das-Attribut vor Beginn des Streamings fest.</span><span class="sxs-lookup"><span data-stu-id="464b8-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="464b8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="464b8-114">Requirements</span></span>



| <span data-ttu-id="464b8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="464b8-115">Requirement</span></span> | <span data-ttu-id="464b8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="464b8-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="464b8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="464b8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="464b8-118">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="464b8-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="464b8-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="464b8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="464b8-120">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="464b8-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="464b8-121">Header</span><span class="sxs-lookup"><span data-stu-id="464b8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="464b8-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="464b8-122"><dt>Mfidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="464b8-123">IDL</span><span class="sxs-lookup"><span data-stu-id="464b8-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="464b8-124"><dt>MFI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="464b8-124"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="464b8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="464b8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="464b8-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="464b8-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




