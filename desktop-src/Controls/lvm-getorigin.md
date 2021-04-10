---
title: LVM_GETORIGIN Meldung (kommstrg. h)
description: Ruft den aktuellen Ansichts Ursprung für ein Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getorigin-Makros senden.
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- Windows-Steuerelemente für LVM_GETORIGIN Meldung
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af42f3d616aa609d6b9e41d3991adb9d68eb24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105495"
---
# <a name="lvm_getorigin-message"></a><span data-ttu-id="563c4-105">LVM \_ getorigin-Nachricht</span><span class="sxs-lookup"><span data-stu-id="563c4-105">LVM\_GETORIGIN message</span></span>

<span data-ttu-id="563c4-106">Ruft den aktuellen Ansichts Ursprung für ein Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="563c4-106">Retrieves the current view origin for a list-view control.</span></span> <span data-ttu-id="563c4-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getorigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="563c4-107">You can send this message explicitly or by using the [**ListView\_GetOrigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="563c4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="563c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="563c4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="563c4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="563c4-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="563c4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="563c4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="563c4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="563c4-112">Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die den Ansichts Ursprung empfängt.</span><span class="sxs-lookup"><span data-stu-id="563c4-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the view origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="563c4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="563c4-113">Return value</span></span>

<span data-ttu-id="563c4-114">Gibt **true** zurück, wenn erfolgreich, oder **false** , wenn die aktuelle Ansicht eine Listen-oder Berichtsansicht ist.</span><span class="sxs-lookup"><span data-stu-id="563c4-114">Returns **TRUE** if successful, or **FALSE** if the current view is list or report view.</span></span>

## <a name="requirements"></a><span data-ttu-id="563c4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="563c4-115">Requirements</span></span>



| <span data-ttu-id="563c4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="563c4-116">Requirement</span></span> | <span data-ttu-id="563c4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="563c4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="563c4-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="563c4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="563c4-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="563c4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="563c4-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="563c4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="563c4-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="563c4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="563c4-122">Header</span><span class="sxs-lookup"><span data-stu-id="563c4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="563c4-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="563c4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

