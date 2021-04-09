---
title: NM_LDOWN (Symbolleisten-) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die linke Maustaste gedrückt wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: f5b356fb-265b-4eb0-a5a3-2a22d688f847
keywords:
- NM_LDOWN (Symbolleiste) Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60f1f05d85aa8885acf31a36098056d68612ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858641"
---
# <a name="nm_ldown-toolbar-notification-code"></a><span data-ttu-id="b7607-105">NM- \_ ldown-Benachrichtigungs Code (Symbolleiste)</span><span class="sxs-lookup"><span data-stu-id="b7607-105">NM\_LDOWN (toolbar) notification code</span></span>

<span data-ttu-id="b7607-106">Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die linke Maustaste gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="b7607-106">Notifies a toolbar's parent window that the left mouse button has been pressed.</span></span> <span data-ttu-id="b7607-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="b7607-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_LDOWN

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b7607-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7607-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7607-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7607-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7607-110">Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="b7607-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="b7607-111">Wenn auf ein Symbolleisten Element auf die Maus geklickt wurde, enthält das Element **dwitemspec** den Element Bezeichner, und der **dwitemdata** -Member enthält die Elementdaten.</span><span class="sxs-lookup"><span data-stu-id="b7607-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="b7607-112">Wenn die Maus auf ein Trennzeichen oder Leerraum auf der Symbolleiste geklickt wurde, enthält das Element **dwitemspec** -1.</span><span class="sxs-lookup"><span data-stu-id="b7607-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7607-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7607-113">Return value</span></span>

<span data-ttu-id="b7607-114">Gibt **false** zurück, damit das Symbolleisten-Steuerelement die Standard Verarbeitung des Ereignisses ausführen kann, oder **true** , um zu verhindern, dass das Steuerelement das Ereignis verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b7607-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7607-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7607-115">Remarks</span></span>

<span data-ttu-id="b7607-116">Diese Benachrichtigung wird gesendet, nachdem der Benachrichtigungs Code für die [TBN- \_ Dropdown](tbn-dropdown.md) Liste gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b7607-116">This notification is sent after the [TBN\_DROPDOWN](tbn-dropdown.md) notification code has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7607-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7607-117">Requirements</span></span>



| <span data-ttu-id="b7607-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7607-118">Requirement</span></span> | <span data-ttu-id="b7607-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b7607-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7607-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7607-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b7607-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7607-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7607-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7607-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b7607-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7607-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7607-124">Header</span><span class="sxs-lookup"><span data-stu-id="b7607-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7607-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7607-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





