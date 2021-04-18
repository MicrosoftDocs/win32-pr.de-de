---
title: DM_GETDEFID Meldung (Winuser. h)
description: Ruft den Bezeichner des Standard Steuer Elements für die pushschaltfläche für ein Dialogfeld ab.
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- Dialog Felder DM_GETDEFID Meldung
topic_type:
- apiref
api_name:
- DM_GETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fdcdfc2cd278ab452d48ecb1c254bdb00ffbb7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518881"
---
# <a name="dm_getdefid-message"></a><span data-ttu-id="4c297-104">DM \_ getdefid-Meldung</span><span class="sxs-lookup"><span data-stu-id="4c297-104">DM\_GETDEFID message</span></span>

<span data-ttu-id="4c297-105">Ruft den Bezeichner des Standard Steuer Elements für die pushschaltfläche für ein Dialogfeld ab.</span><span class="sxs-lookup"><span data-stu-id="4c297-105">Retrieves the identifier of the default push button control for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
```



## <a name="parameters"></a><span data-ttu-id="4c297-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c297-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c297-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c297-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c297-108">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4c297-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4c297-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c297-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c297-110">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4c297-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c297-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c297-111">Return value</span></span>

<span data-ttu-id="4c297-112">Wenn eine Standard-Push-Schaltfläche vorhanden ist, enthält das hochwertige Wort des Rückgabewerts den Wert **DC \_ hasdefid** , und das nieder wertige Wort enthält den Steuerelement Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="4c297-112">If a default push button exists, the high-order word of the return value contains the value **DC\_HASDEFID** and the low-order word contains the control identifier.</span></span> <span data-ttu-id="4c297-113">Andernfalls ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4c297-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c297-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c297-114">Remarks</span></span>

<span data-ttu-id="4c297-115">Die Funktion [**defdlgproc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) verarbeitet diese Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4c297-115">The [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c297-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c297-116">Requirements</span></span>



| <span data-ttu-id="4c297-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c297-117">Requirement</span></span> | <span data-ttu-id="4c297-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4c297-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c297-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c297-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4c297-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c297-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4c297-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c297-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4c297-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c297-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4c297-123">Header</span><span class="sxs-lookup"><span data-stu-id="4c297-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c297-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="4c297-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c297-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c297-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="4c297-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="4c297-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4c297-127">**Defdlgproc**</span><span class="sxs-lookup"><span data-stu-id="4c297-127">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="4c297-128">**DM \_ -setdefid**</span><span class="sxs-lookup"><span data-stu-id="4c297-128">**DM\_SETDEFID**</span></span>](dm-setdefid.md)
</dt> <dt>

<span data-ttu-id="4c297-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="4c297-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4c297-130">Dialog Felder</span><span class="sxs-lookup"><span data-stu-id="4c297-130">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

 





