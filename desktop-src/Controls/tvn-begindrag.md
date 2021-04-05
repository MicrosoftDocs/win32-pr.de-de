---
title: TVN_BEGINDRAG Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass ein Drag & Drop-Vorgang mit der linken Maustaste initiiert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- Windows-Steuerelemente für TVN_BEGINDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f47f55a5e2eae552f64234a8e43ef0961f38c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858935"
---
# <a name="tvn_begindrag-notification-code"></a><span data-ttu-id="db3c0-105">TVN \_ BeginDrag-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="db3c0-105">TVN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="db3c0-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass ein Drag & Drop-Vorgang mit der linken Maustaste initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="db3c0-106">Notifies a tree-view control's parent window that a drag-and-drop operation involving the left mouse button is being initiated.</span></span> <span data-ttu-id="db3c0-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="db3c0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="db3c0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="db3c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db3c0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db3c0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db3c0-110">Zeiger auf eine [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="db3c0-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="db3c0-111">Der **itemnew** -Member ist eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die gültige Informationen über das Element enthält, das in den **Hitem**-, **State**-und **LPARAM** -Membern gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="db3c0-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being dragged in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="db3c0-112">Der **ptdrag** -Member gibt die aktuellen Bildschirm Koordinaten der Maus an.</span><span class="sxs-lookup"><span data-stu-id="db3c0-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db3c0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db3c0-113">Return value</span></span>

<span data-ttu-id="db3c0-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="db3c0-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="db3c0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db3c0-115">Remarks</span></span>

<span data-ttu-id="db3c0-116">Ein Strukturansicht-Steuerelement, das über den " [**TVs \_ disabledragdrop**](tree-view-control-window-styles.md) "-Stil verfügt, sendet diesen Benachrichtigungs Code nicht.</span><span class="sxs-lookup"><span data-stu-id="db3c0-116">A tree-view control that has the [**TVS\_DISABLEDRAGDROP**](tree-view-control-window-styles.md) style does not send this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="db3c0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db3c0-117">Requirements</span></span>



| <span data-ttu-id="db3c0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db3c0-118">Requirement</span></span> | <span data-ttu-id="db3c0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="db3c0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db3c0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db3c0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="db3c0-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db3c0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db3c0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db3c0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="db3c0-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db3c0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db3c0-124">Header</span><span class="sxs-lookup"><span data-stu-id="db3c0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="db3c0-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="db3c0-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="db3c0-126">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="db3c0-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="db3c0-127">**TVN \_ Begindragw** (Unicode) und **TVN \_ begindraga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="db3c0-127">**TVN\_BEGINDRAGW** (Unicode) and **TVN\_BEGINDRAGA** (ANSI)</span></span><br/>               |



 

 





