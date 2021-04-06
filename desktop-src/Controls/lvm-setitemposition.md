---
title: LVM_SETITEMPOSITION Meldung (kommstrg. h)
description: Verschiebt ein Element an eine angegebene Position in einem Listenansicht-Steuerelement (muss sich in der Symbol Ansicht oder in der kleinen Symbol Ansicht befinden). Sie können diese Nachricht explizit oder mithilfe des ListView-Makros "-Tabelle" senden \_ .
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- Windows-Steuerelemente für LVM_SETITEMPOSITION Meldung
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858941"
---
# <a name="lvm_setitemposition-message"></a><span data-ttu-id="904ef-105">LVM- \_ Nachricht "abtitemposition"</span><span class="sxs-lookup"><span data-stu-id="904ef-105">LVM\_SETITEMPOSITION message</span></span>

<span data-ttu-id="904ef-106">Verschiebt ein Element an eine angegebene Position in einem Listenansicht-Steuerelement (muss sich in der Symbol Ansicht oder in der kleinen Symbol Ansicht befinden).</span><span class="sxs-lookup"><span data-stu-id="904ef-106">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="904ef-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) -Makros "-Tabelle" senden.</span><span class="sxs-lookup"><span data-stu-id="904ef-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="904ef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="904ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="904ef-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="904ef-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="904ef-110">Der Index des Listen Ansichts Elements.</span><span class="sxs-lookup"><span data-stu-id="904ef-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="904ef-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="904ef-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="904ef-112">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die neue x-Position der oberen linken Ecke des Elements in Ansichts Koordinaten an.</span><span class="sxs-lookup"><span data-stu-id="904ef-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new x-position of the item's upper-left corner, in view coordinates.</span></span> <span data-ttu-id="904ef-113">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die neue y-Position der oberen linken Ecke des Elements in Ansichts Koordinaten an.</span><span class="sxs-lookup"><span data-stu-id="904ef-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new y-position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="904ef-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="904ef-114">Return value</span></span>

<span data-ttu-id="904ef-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="904ef-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="904ef-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="904ef-116">Remarks</span></span>

<span data-ttu-id="904ef-117">Wenn das Listenansicht-Steuerelement den [**LVS \_ AutoArrange**](list-view-window-styles.md) -Stil aufweist, werden die Elemente im Listenansicht-Steuerelement nach dem Festlegen der Position des Elements angeordnet.</span><span class="sxs-lookup"><span data-stu-id="904ef-117">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, the items in the list-view control are arranged after the position of the item is set.</span></span>

<span data-ttu-id="904ef-118">Unter Windows Vista führt das Senden dieser Nachricht an ein Listenansicht-Steuerelement mit dem [**LVS \_ AutoArrange**](list-view-window-styles.md) -Stil nichts aus, und der Rückgabewert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="904ef-118">On Windows Vista, sending this message to a list-view control with the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style does nothing, and the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="904ef-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="904ef-119">Requirements</span></span>



| <span data-ttu-id="904ef-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="904ef-120">Requirement</span></span> | <span data-ttu-id="904ef-121">Wert</span><span class="sxs-lookup"><span data-stu-id="904ef-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="904ef-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="904ef-122">Minimum supported client</span></span><br/> | <span data-ttu-id="904ef-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="904ef-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="904ef-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="904ef-124">Minimum supported server</span></span><br/> | <span data-ttu-id="904ef-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="904ef-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="904ef-126">Header</span><span class="sxs-lookup"><span data-stu-id="904ef-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="904ef-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="904ef-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

