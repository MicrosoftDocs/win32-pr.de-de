---
title: LVM_HASGROUP Meldung (kommstrg. h)
description: Bestimmt, ob das Listenansicht-Steuerelement über eine angegebene Gruppe verfügt.
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- Windows-Steuerelemente für LVM_HASGROUP Meldung
topic_type:
- apiref
api_name:
- LVM_HASGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb05fed8466188aa0025d2128ce64ad7f1512c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478501"
---
# <a name="lvm_hasgroup-message"></a><span data-ttu-id="c0fd6-104">LVM- \_ hasgroup-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c0fd6-104">LVM\_HASGROUP message</span></span>

<span data-ttu-id="c0fd6-105">Bestimmt, ob das Listenansicht-Steuerelement über eine angegebene Gruppe verfügt.</span><span class="sxs-lookup"><span data-stu-id="c0fd6-105">Determines whether the list-view control has a specified group.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0fd6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0fd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0fd6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0fd6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c0fd6-108">Die ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="c0fd6-108">ID of the group.</span></span></dd> <dt>

<span data-ttu-id="c0fd6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0fd6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c0fd6-110">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c0fd6-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0fd6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0fd6-111">Return value</span></span>

<span data-ttu-id="c0fd6-112">Gibt **true** zurück, wenn das Listenansicht-Steuerelement über die angegebene Gruppe verfügt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="c0fd6-112">Returns **TRUE** if the list-view control has the specified group, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0fd6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0fd6-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c0fd6-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="c0fd6-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c0fd6-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c0fd6-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0fd6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0fd6-116">Requirements</span></span>



| <span data-ttu-id="c0fd6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0fd6-117">Requirement</span></span> | <span data-ttu-id="c0fd6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c0fd6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0fd6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0fd6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0fd6-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0fd6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0fd6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0fd6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0fd6-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0fd6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0fd6-123">Header</span><span class="sxs-lookup"><span data-stu-id="c0fd6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0fd6-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0fd6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





