---
title: LVM_GETITEMRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck für den gesamten oder einen Teil eines Elements in der aktuellen Ansicht ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItemRect-Makros senden.
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- Windows-Steuerelemente für LVM_GETITEMRECT Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0915c9afc16f13ac8f36a639524fb5af6e8082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040890"
---
# <a name="lvm_getitemrect-message"></a><span data-ttu-id="53028-105">LVM- \_ GetItemRect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="53028-105">LVM\_GETITEMRECT message</span></span>

<span data-ttu-id="53028-106">Ruft das umgebende Rechteck für den gesamten oder einen Teil eines Elements in der aktuellen Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="53028-106">Retrieves the bounding rectangle for all or part of an item in the current view.</span></span> <span data-ttu-id="53028-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="53028-107">You can send this message explicitly or by using the [**ListView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="53028-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="53028-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53028-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53028-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53028-110">Der Index des Listen Ansichts Elements.</span><span class="sxs-lookup"><span data-stu-id="53028-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="53028-111">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="53028-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53028-112">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das umschließende Rechteck empfängt.</span><span class="sxs-lookup"><span data-stu-id="53028-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="53028-113">Wenn die Nachricht gesendet wird, wird der **linke** Member dieser Struktur verwendet, um den Teil des Listen Ansichts Elements anzugeben, aus dem das umgebende Rechteck abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="53028-113">When the message is sent, the **left** member of this structure is used to specify the portion of the list-view item from which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="53028-114">Für sie muss einer der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="53028-114">It must be set to one of the following values:</span></span>



| <span data-ttu-id="53028-115">Wert</span><span class="sxs-lookup"><span data-stu-id="53028-115">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="53028-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="53028-116">Meaning</span></span>                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="53028-117"><dt>**lvir- \_ Begrenzungen**</dt></span><span class="sxs-lookup"><span data-stu-id="53028-117"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl>                   | <span data-ttu-id="53028-118">Gibt das umgebende Rechteck des gesamten Elements zurück, einschließlich des Symbols und der Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="53028-118">Returns the bounding rectangle of the entire item, including the icon and label.</span></span><br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="53028-119"><dt>**lvir- \_ Symbol**</dt></span><span class="sxs-lookup"><span data-stu-id="53028-119"><dt>**LVIR\_ICON**</dt></span></span> </dl>                         | <span data-ttu-id="53028-120">Gibt das umgebende Rechteck des Symbols oder des kleinen Symbols zurück.</span><span class="sxs-lookup"><span data-stu-id="53028-120">Returns the bounding rectangle of the icon or small icon.</span></span><br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="53028-121"><dt>**lvir- \_ Bezeichnung**</dt></span><span class="sxs-lookup"><span data-stu-id="53028-121"><dt>**LVIR\_LABEL**</dt></span></span> </dl>                      | <span data-ttu-id="53028-122">Gibt das umgebende Rechteck des Element Texts zurück.</span><span class="sxs-lookup"><span data-stu-id="53028-122">Returns the bounding rectangle of the item text.</span></span><br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <span data-ttu-id="53028-123"><dt>**lvir- \_ selectbounds**</dt></span><span class="sxs-lookup"><span data-stu-id="53028-123"><dt>**LVIR\_SELECTBOUNDS**</dt></span></span> </dl> | <span data-ttu-id="53028-124">Gibt die Gesamtmenge des lvir \_ -Symbols und der lvir- \_ Beschriftungs Rechtecke zurück, schließt jedoch Spalten in der Berichtsansicht aus.</span><span class="sxs-lookup"><span data-stu-id="53028-124">Returns the union of the LVIR\_ICON and LVIR\_LABEL rectangles, but excludes columns in report view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53028-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53028-125">Return value</span></span>

<span data-ttu-id="53028-126">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="53028-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="53028-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53028-127">Requirements</span></span>



| <span data-ttu-id="53028-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53028-128">Requirement</span></span> | <span data-ttu-id="53028-129">Wert</span><span class="sxs-lookup"><span data-stu-id="53028-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53028-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53028-130">Minimum supported client</span></span><br/> | <span data-ttu-id="53028-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53028-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53028-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53028-132">Minimum supported server</span></span><br/> | <span data-ttu-id="53028-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53028-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53028-134">Header</span><span class="sxs-lookup"><span data-stu-id="53028-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="53028-135"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="53028-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

