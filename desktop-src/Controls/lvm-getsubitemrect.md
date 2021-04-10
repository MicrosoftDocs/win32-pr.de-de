---
title: LVM_GETSUBITEMRECT Meldung (kommstrg. h)
description: Ruft Informationen über das umgebende Rechteck für ein Unterelement in einem Listenansicht-Steuerelement ab.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- Windows-Steuerelemente für LVM_GETSUBITEMRECT Meldung
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105489"
---
# <a name="lvm_getsubitemrect-message"></a><span data-ttu-id="84632-104">LVM \_ getsubitemrect-Meldung</span><span class="sxs-lookup"><span data-stu-id="84632-104">LVM\_GETSUBITEMRECT message</span></span>

<span data-ttu-id="84632-105">Ruft Informationen über das umgebende Rechteck für ein Unterelement in einem Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="84632-105">Retrieves information about the bounding rectangle for a subitem in a list-view control.</span></span> <span data-ttu-id="84632-106">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getsubitemrect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) -Makros (empfohlen) senden.</span><span class="sxs-lookup"><span data-stu-id="84632-106">You can send this message explicitly or by using the [**ListView\_GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) macro (recommended).</span></span> <span data-ttu-id="84632-107">Diese Nachricht soll nur mit Listenansicht-Steuerelementen verwendet werden, die den [**LVS- \_ Berichts**](list-view-window-styles.md) Stil verwenden.</span><span class="sxs-lookup"><span data-stu-id="84632-107">This message is intended to be used only with list-view controls that use the [**LVS\_REPORT**](list-view-window-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="84632-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="84632-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84632-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84632-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84632-110">Der Index des übergeordneten Elements des unter Elements.</span><span class="sxs-lookup"><span data-stu-id="84632-110">Index of the subitem's parent item.</span></span>

</dd> <dt>

<span data-ttu-id="84632-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84632-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84632-112">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Informationen zu umschließenden Rechtecks des unter Elements empfängt.</span><span class="sxs-lookup"><span data-stu-id="84632-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the subitem bounding rectangle information.</span></span> <span data-ttu-id="84632-113">Seine Member müssen gemäß den folgenden Element-/Wert-Beziehungen initialisiert werden:</span><span class="sxs-lookup"><span data-stu-id="84632-113">Its members must be initialized according to the following member/value relationships:</span></span>



| <span data-ttu-id="84632-114">Wert</span><span class="sxs-lookup"><span data-stu-id="84632-114">Value</span></span>                                                                                                                             | <span data-ttu-id="84632-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="84632-115">Meaning</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="84632-116"><dt>**top**</dt></span><span class="sxs-lookup"><span data-stu-id="84632-116"><dt>**top**</dt></span></span> </dl>    | <span data-ttu-id="84632-117">Der einbasierte Index des unter Elements.</span><span class="sxs-lookup"><span data-stu-id="84632-117">The one-based index of the subitem.</span></span><br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="84632-118"><dt>**linken**</dt></span><span class="sxs-lookup"><span data-stu-id="84632-118"><dt>**left**</dt></span></span> </dl> | <span data-ttu-id="84632-119">Flagwert (siehe Hinweise).</span><span class="sxs-lookup"><span data-stu-id="84632-119">Flag value (see remarks).</span></span> <span data-ttu-id="84632-120">Gibt den Teil des Listen Ansichts unter Elements an, für das das umgebende Rechteck abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="84632-120">Indicates the portion of the list-view subitem for which to retrieve the bounding rectangle.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84632-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84632-121">Return value</span></span>

<span data-ttu-id="84632-122">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="84632-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="84632-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84632-123">Remarks</span></span>

<span data-ttu-id="84632-124">Im folgenden finden Sie die Flagwerte, die festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="84632-124">Following are the flag values that may be set.</span></span>



| <span data-ttu-id="84632-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84632-125">Requirement</span></span> | <span data-ttu-id="84632-126">Wert</span><span class="sxs-lookup"><span data-stu-id="84632-126">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84632-127">**Flagwert**</span><span class="sxs-lookup"><span data-stu-id="84632-127">**Flag Value**</span></span> | <span data-ttu-id="84632-128">**Bedeutung**</span><span class="sxs-lookup"><span data-stu-id="84632-128">**Meaning**</span></span>                                                                                                         |
| <span data-ttu-id="84632-129">lvir- \_ Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="84632-129">LVIR\_BOUNDS</span></span>   | <span data-ttu-id="84632-130">Gibt das umgebende Rechteck des gesamten Elements zurück, einschließlich des Symbols und der Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="84632-130">Returns the bounding rectangle of the entire item, including the icon and label.</span></span>                                    |
| <span data-ttu-id="84632-131">lvir- \_ Symbol</span><span class="sxs-lookup"><span data-stu-id="84632-131">LVIR\_ICON</span></span>     | <span data-ttu-id="84632-132">Gibt das umgebende Rechteck des Symbols oder des kleinen Symbols zurück.</span><span class="sxs-lookup"><span data-stu-id="84632-132">Returns the bounding rectangle of the icon or small icon.</span></span>                                                           |
| <span data-ttu-id="84632-133">lvir- \_ Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="84632-133">LVIR\_LABEL</span></span>    | <span data-ttu-id="84632-134">Gibt das umgebende Rechteck des gesamten Elements zurück, einschließlich des Symbols und der Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="84632-134">Returns the bounding rectangle of the entire item, including the icon and label.</span></span> <span data-ttu-id="84632-135">Dies ist mit lvir- \_ Begrenzungen identisch.</span><span class="sxs-lookup"><span data-stu-id="84632-135">This is identical to LVIR\_BOUNDS.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="84632-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84632-136">Requirements</span></span>



| <span data-ttu-id="84632-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84632-137">Requirement</span></span> | <span data-ttu-id="84632-138">Wert</span><span class="sxs-lookup"><span data-stu-id="84632-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84632-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84632-139">Minimum supported client</span></span><br/> | <span data-ttu-id="84632-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84632-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84632-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84632-141">Minimum supported server</span></span><br/> | <span data-ttu-id="84632-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84632-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84632-143">Header</span><span class="sxs-lookup"><span data-stu-id="84632-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="84632-144"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="84632-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

