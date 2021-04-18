---
title: UDM_GETPOS Meldung (kommstrg. h)
description: Ruft die aktuelle Position eines auf-ab-Steuer Elements mit 16-Bit-Genauigkeit ab.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- Windows-Steuerelemente für UDM_GETPOS Meldung
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e78ad19289d85b93ebcb39a244a896ddb4f33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339127"
---
# <a name="udm_getpos-message"></a><span data-ttu-id="6b438-104">UDM- \_ GetPos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="6b438-104">UDM\_GETPOS message</span></span>

<span data-ttu-id="6b438-105">Ruft die aktuelle Position eines auf-ab-Steuer Elements mit 16-Bit-Genauigkeit ab.</span><span class="sxs-lookup"><span data-stu-id="6b438-105">Retrieves the current position of an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b438-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b438-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b438-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b438-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6b438-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6b438-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6b438-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b438-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6b438-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6b438-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b438-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b438-111">Return value</span></span>

<span data-ttu-id="6b438-112">Bei erfolgreicher Ausführung wird das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) auf 0 (null) festgelegt, und das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) wird auf die aktuelle Position des Steuer Elements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b438-112">If successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is set to zero and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is set to the control's current position.</span></span> <span data-ttu-id="6b438-113">Wenn ein Fehler auftritt, wird das **HIWORD** auf einen Wert ungleich 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b438-113">If an error occurs, the **HIWORD** is set to a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b438-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b438-114">Remarks</span></span>

<span data-ttu-id="6b438-115">Bei der Verarbeitung dieser Nachricht aktualisiert das auf-ab-Steuerelement die aktuelle Position basierend auf der Beschriftung des Buddy-Fensters.</span><span class="sxs-lookup"><span data-stu-id="6b438-115">When processing this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="6b438-116">Das auf-ab-Steuerelement gibt einen Fehler zurück, wenn kein Buddy-Fenster vorhanden ist oder wenn die Beschriftung einen ungültigen Wert oder einen Wert außerhalb des gültigen Bereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="6b438-116">The up-down control returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span> <span data-ttu-id="6b438-117">Außerdem wird ein Fehlerflag im HIWORD der Rückgabe festgelegt, wenn das Steuerelement ohne den [**UDS- \_ setbuddyint**](up-down-control-styles.md) -Stil erstellt wird, obwohl es einen gültigen Positionswert im LoWord der Rückgabe zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6b438-117">Also, an error flag is set in the HIWORD of the return if the control is created without the [**UDS\_SETBUDDYINT**](up-down-control-styles.md) style, even though it returns a valid position value in the LOWORD of the return.</span></span>

<span data-ttu-id="6b438-118">Wenn 32-Bit-Werte für ein auf-ab-Steuerelement mit [**UDM- \_ SETRANGE32**](udm-setrange32.md)aktiviert wurden, gibt diese Meldung nur die unteren 16 Bits der Position zurück.</span><span class="sxs-lookup"><span data-stu-id="6b438-118">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), this message returns only the lower 16 bits of the position.</span></span> <span data-ttu-id="6b438-119">Um die vollständige 32-Bit-Position abzurufen, verwenden Sie [**UDM \_ GETPOS32**](udm-getpos32.md).</span><span class="sxs-lookup"><span data-stu-id="6b438-119">To retrieve the full 32-bit position, use [**UDM\_GETPOS32**](udm-getpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b438-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b438-120">Requirements</span></span>



| <span data-ttu-id="6b438-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b438-121">Requirement</span></span> | <span data-ttu-id="6b438-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6b438-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b438-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b438-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6b438-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b438-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b438-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b438-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6b438-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b438-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b438-127">Header</span><span class="sxs-lookup"><span data-stu-id="6b438-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b438-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b438-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b438-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b438-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="6b438-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="6b438-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6b438-131">**UDM- \_ GetRange**</span><span class="sxs-lookup"><span data-stu-id="6b438-131">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="6b438-132">**UDM \_ GETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="6b438-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)
</dt> <dt>

[<span data-ttu-id="6b438-133">**UDM- \_ SetPos**</span><span class="sxs-lookup"><span data-stu-id="6b438-133">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="6b438-134">**UDM \_ SETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="6b438-134">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)
</dt> </dl>

 

