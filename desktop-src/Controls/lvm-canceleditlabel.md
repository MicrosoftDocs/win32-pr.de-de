---
title: LVM_CANCELEDITLABEL Meldung (kommstrg. h)
description: Bricht einen Element Text Bearbeitungsvorgang ab.
ms.assetid: 73e9c922-3223-4c49-a33c-df7c09443ccc
keywords:
- Windows-Steuerelemente für LVM_CANCELEDITLABEL Meldung
topic_type:
- apiref
api_name:
- LVM_CANCELEDITLABEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfed26fb3c38d91f7a5b07683079d29ecd4597d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102907"
---
# <a name="lvm_canceleditlabel-message"></a><span data-ttu-id="76f8d-104">LVM \_ canceleditlabel-Nachricht</span><span class="sxs-lookup"><span data-stu-id="76f8d-104">LVM\_CANCELEDITLABEL message</span></span>

<span data-ttu-id="76f8d-105">Bricht einen Element Text Bearbeitungsvorgang ab.</span><span class="sxs-lookup"><span data-stu-id="76f8d-105">Cancels an item text editing operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="76f8d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76f8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76f8d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76f8d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="76f8d-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="76f8d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="76f8d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76f8d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="76f8d-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="76f8d-110">Must be zero.</span></span></dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76f8d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76f8d-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="76f8d-112">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="76f8d-112">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="76f8d-113">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="76f8d-113">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="76f8d-114">Diese Meldung bewirkt, dass eine [LVN \_ endlabeledit](lvn-endlabeledit.md) -Benachrichtigung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="76f8d-114">This message causes a an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification to be sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="76f8d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76f8d-115">Requirements</span></span>



| <span data-ttu-id="76f8d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76f8d-116">Requirement</span></span> | <span data-ttu-id="76f8d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="76f8d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76f8d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76f8d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="76f8d-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76f8d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76f8d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76f8d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="76f8d-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76f8d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76f8d-122">Header</span><span class="sxs-lookup"><span data-stu-id="76f8d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="76f8d-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="76f8d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





