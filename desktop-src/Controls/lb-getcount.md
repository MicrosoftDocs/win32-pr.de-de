---
title: LB_GETCOUNT Meldung (Winuser. h)
description: Ruft die Anzahl der Elemente in einem Listenfeld ab.
ms.assetid: 1fbe44fc-8b9d-4bfa-a8bb-06817eecf064
keywords:
- Windows-Steuerelemente für LB_GETCOUNT Meldung
topic_type:
- apiref
api_name:
- LB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddedbd7b9165e00e722edbadbb8806a68417551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478963"
---
# <a name="lb_getcount-message"></a><span data-ttu-id="74e73-104">LB- \_ GetCount-Nachricht</span><span class="sxs-lookup"><span data-stu-id="74e73-104">LB\_GETCOUNT message</span></span>

<span data-ttu-id="74e73-105">Ruft die Anzahl der Elemente in einem Listenfeld ab.</span><span class="sxs-lookup"><span data-stu-id="74e73-105">Gets the number of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="74e73-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="74e73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74e73-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74e73-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74e73-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="74e73-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="74e73-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74e73-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74e73-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="74e73-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74e73-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74e73-111">Return value</span></span>

<span data-ttu-id="74e73-112">Der Rückgabewert ist die Anzahl der Elemente im Listenfeld oder lb Err, \_ Wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="74e73-112">The return value is the number of items in the list box, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="74e73-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74e73-113">Remarks</span></span>

<span data-ttu-id="74e73-114">Die zurückgegebene Anzahl ist ein Wert größer als der Indexwert des letzten Elements (der Index ist NULL basiert).</span><span class="sxs-lookup"><span data-stu-id="74e73-114">The returned count is one greater than the index value of the last item (the index is zero-based).</span></span>

## <a name="requirements"></a><span data-ttu-id="74e73-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74e73-115">Requirements</span></span>



| <span data-ttu-id="74e73-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74e73-116">Requirement</span></span> | <span data-ttu-id="74e73-117">Wert</span><span class="sxs-lookup"><span data-stu-id="74e73-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74e73-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74e73-118">Minimum supported client</span></span><br/> | <span data-ttu-id="74e73-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74e73-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="74e73-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74e73-120">Minimum supported server</span></span><br/> | <span data-ttu-id="74e73-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74e73-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="74e73-122">Header</span><span class="sxs-lookup"><span data-stu-id="74e73-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="74e73-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="74e73-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74e73-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74e73-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74e73-125">**LB- \_ SetCount**</span><span class="sxs-lookup"><span data-stu-id="74e73-125">**LB\_SETCOUNT**</span></span>](lb-setcount.md)
</dt> </dl>

 

 





