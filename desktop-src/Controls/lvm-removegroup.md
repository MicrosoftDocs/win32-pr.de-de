---
title: LVM_REMOVEGROUP Meldung (kommstrg. h)
description: Entfernt eine Gruppe aus einem Listenansicht-Steuerelement.
ms.assetid: c6f4f54c-4cf8-47d0-8e96-fa8a1df0501b
keywords:
- Windows-Steuerelemente für LVM_REMOVEGROUP Meldung
topic_type:
- apiref
api_name:
- LVM_REMOVEGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa631593e791f90c76a9f74aa1d967d9678540f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956721"
---
# <a name="lvm_removegroup-message"></a><span data-ttu-id="ead49-104">LVM- \_ removegroup-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ead49-104">LVM\_REMOVEGROUP message</span></span>

<span data-ttu-id="ead49-105">Entfernt eine Gruppe aus einem Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ead49-105">Removes a group from a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ead49-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ead49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ead49-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ead49-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ead49-108">ID, die die Gruppe angibt, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ead49-108">ID that specifies the group to remove.</span></span></dd> <dt>

<span data-ttu-id="ead49-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ead49-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ead49-110">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="ead49-110">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ead49-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ead49-111">Return value</span></span>

<span data-ttu-id="ead49-112">Gibt den Index der Gruppe zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="ead49-112">Returns the index of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ead49-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ead49-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ead49-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="ead49-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ead49-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ead49-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ead49-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ead49-116">Requirements</span></span>



| <span data-ttu-id="ead49-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ead49-117">Requirement</span></span> | <span data-ttu-id="ead49-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ead49-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ead49-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ead49-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ead49-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ead49-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ead49-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ead49-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ead49-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ead49-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ead49-123">Header</span><span class="sxs-lookup"><span data-stu-id="ead49-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ead49-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ead49-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





