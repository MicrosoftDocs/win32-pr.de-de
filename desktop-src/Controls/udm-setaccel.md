---
title: UDM_SETACCEL Meldung (kommstrg. h)
description: Legt die Beschleunigung für ein auf-ab-Steuerelement fest.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- Windows-Steuerelemente für UDM_SETACCEL Meldung
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43ed290ce1668ffcaa9fb086a99ad52e5129ad6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041005"
---
# <a name="udm_setaccel-message"></a><span data-ttu-id="6c5b1-104">UDM- \_ SetAccel-Meldung</span><span class="sxs-lookup"><span data-stu-id="6c5b1-104">UDM\_SETACCEL message</span></span>

<span data-ttu-id="6c5b1-105">Legt die Beschleunigung für ein auf-ab-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="6c5b1-105">Sets the acceleration for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c5b1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c5b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c5b1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c5b1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c5b1-108">Anzahl der von *aaccels* angegebenen [**udaccel**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="6c5b1-108">Number of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures specified by *aAccels*.</span></span>

</dd> <dt>

<span data-ttu-id="6c5b1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c5b1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c5b1-110">Zeiger auf ein Array von [**udaccel**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) -Strukturen, die Beschleunigungs Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6c5b1-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that contain acceleration information.</span></span> <span data-ttu-id="6c5b1-111">Elemente müssen in aufsteigender Reihenfolge basierend auf dem **nsec** -Member sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c5b1-111">Elements should be sorted in ascending order based on the **nSec** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c5b1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c5b1-112">Return value</span></span>

<span data-ttu-id="6c5b1-113">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="6c5b1-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c5b1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c5b1-114">Requirements</span></span>



| <span data-ttu-id="6c5b1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c5b1-115">Requirement</span></span> | <span data-ttu-id="6c5b1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6c5b1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5b1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c5b1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6c5b1-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c5b1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c5b1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c5b1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6c5b1-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c5b1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c5b1-121">Header</span><span class="sxs-lookup"><span data-stu-id="6c5b1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c5b1-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c5b1-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c5b1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c5b1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c5b1-124">**UDM \_ GetAccel**</span><span class="sxs-lookup"><span data-stu-id="6c5b1-124">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)
</dt> </dl>

 

 





