---
title: UDM_GETPOS32 Meldung (kommstrg. h)
description: Gibt die 32-Bit-Position eines auf-ab-Steuer Elements zurück.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- Windows-Steuerelemente für UDM_GETPOS32 Meldung
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f316b6833c67cd01d4e01910399a8730691f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475726"
---
# <a name="udm_getpos32-message"></a><span data-ttu-id="d6640-104">UDM \_ GETPOS32 Meldung</span><span class="sxs-lookup"><span data-stu-id="d6640-104">UDM\_GETPOS32 message</span></span>

<span data-ttu-id="d6640-105">Gibt die 32-Bit-Position eines auf-ab-Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="d6640-105">Returns the 32-bit position of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d6640-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6640-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6640-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6640-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6640-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d6640-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d6640-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6640-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6640-110">Zeiger auf einen **booleschen** Wert, der auf 0 (null) festgelegt wird, wenn der Wert erfolgreich abgerufen wird, oder ungleich NULL, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="d6640-110">Pointer to a **BOOL** value that is set to zero if the value is successfully retrieved or nonzero if an error occurs.</span></span> <span data-ttu-id="d6640-111">Wenn dieser Parameter auf **null** festgelegt ist, werden keine Fehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="d6640-111">If this parameter is set to **NULL**, errors are not reported.</span></span>

<span data-ttu-id="d6640-112">Wenn **UDM \_ GETPOS32** in einer prozessübergreifenden Situation verwendet wird, muss dieser Parameter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="d6640-112">If **UDM\_GETPOS32** is used in a cross-process situation, this parameter must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6640-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6640-113">Return value</span></span>

<span data-ttu-id="d6640-114">Gibt die Position eines auf-ab-Steuer Elements mit 32-Bit-Genauigkeit zurück.</span><span class="sxs-lookup"><span data-stu-id="d6640-114">Returns the position of an up-down control with 32-bit precision.</span></span> <span data-ttu-id="d6640-115">Anwendungen müssen den *LPARAM* -Wert überprüfen, um zu bestimmen, ob der Rückgabewert gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d6640-115">Applications must check the *lParam* value to determine whether the return value is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6640-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6640-116">Remarks</span></span>

<span data-ttu-id="d6640-117">Wenn diese Nachricht verarbeitet wird, aktualisiert das auf-ab-Steuerelement die aktuelle Position basierend auf der Beschriftung des Buddy-Fensters.</span><span class="sxs-lookup"><span data-stu-id="d6640-117">When it processes this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="d6640-118">Es wird ein Fehler zurückgegeben, wenn kein Buddy-Fenster vorhanden ist oder wenn die Beschriftung einen ungültigen Wert oder außerhalb des gültigen Bereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="d6640-118">It returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6640-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6640-119">Requirements</span></span>



| <span data-ttu-id="d6640-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6640-120">Requirement</span></span> | <span data-ttu-id="d6640-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d6640-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6640-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6640-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d6640-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6640-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d6640-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6640-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d6640-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6640-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d6640-126">Header</span><span class="sxs-lookup"><span data-stu-id="d6640-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6640-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6640-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6640-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6640-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6640-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d6640-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d6640-130">**UDM- \_ GetPos**</span><span class="sxs-lookup"><span data-stu-id="d6640-130">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="d6640-131">**UDM- \_ SetPos**</span><span class="sxs-lookup"><span data-stu-id="d6640-131">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="d6640-132">**UDM \_ SETPOS32**</span><span class="sxs-lookup"><span data-stu-id="d6640-132">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)
</dt> </dl>

 

 





