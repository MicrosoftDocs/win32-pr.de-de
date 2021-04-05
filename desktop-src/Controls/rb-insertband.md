---
title: RB_INSERTBAND Meldung (kommstrg. h)
description: Fügt ein neues Band in ein Grund leisten-Steuerelement ein.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- Windows-Steuerelemente für RB_INSERTBAND Meldung
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39b45eb662fb4c2058b87837352339c84762188
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859336"
---
# <a name="rb_insertband-message"></a><span data-ttu-id="5abb3-104">RB \_ InsertBand-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5abb3-104">RB\_INSERTBAND message</span></span>

<span data-ttu-id="5abb3-105">Fügt ein neues Band in ein Grund leisten-Steuerelement ein.</span><span class="sxs-lookup"><span data-stu-id="5abb3-105">Inserts a new band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5abb3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5abb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5abb3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5abb3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5abb3-108">Der null basierte Index der Position, an der das Band eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="5abb3-108">Zero-based index of the location where the band will be inserted.</span></span> <span data-ttu-id="5abb3-109">Wenn Sie diesen Parameter auf "-1" festlegen, fügt das Steuerelement das neue Band am letzten Speicherort hinzu.</span><span class="sxs-lookup"><span data-stu-id="5abb3-109">If you set this parameter to -1, the control will add the new band at the last location.</span></span>

</dd> <dt>

<span data-ttu-id="5abb3-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5abb3-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5abb3-111">Ein Zeiger auf eine [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur, die das einzufügende Band definiert.</span><span class="sxs-lookup"><span data-stu-id="5abb3-111">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be inserted.</span></span> <span data-ttu-id="5abb3-112">Sie müssen den **CBSIZE** -Member dieser Struktur auf **sizeof**(REBARBANDINFO) festlegen, bevor Sie diese Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="5abb3-112">You must set the **cbSize** member of this structure to **sizeof**(REBARBANDINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5abb3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5abb3-113">Return value</span></span>

<span data-ttu-id="5abb3-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="5abb3-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5abb3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5abb3-115">Requirements</span></span>



| <span data-ttu-id="5abb3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5abb3-116">Requirement</span></span> | <span data-ttu-id="5abb3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5abb3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5abb3-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5abb3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5abb3-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5abb3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5abb3-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5abb3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5abb3-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5abb3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5abb3-122">Header</span><span class="sxs-lookup"><span data-stu-id="5abb3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5abb3-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5abb3-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5abb3-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="5abb3-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5abb3-125">**RB \_ Insertbandw** (Unicode) und **RB \_ insertbanda** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5abb3-125">**RB\_INSERTBANDW** (Unicode) and **RB\_INSERTBANDA** (ANSI)</span></span><br/>               |



 

 





