---
title: WM_EXITMENULOOP Meldung (Winuser. h)
description: Benachrichtigt die Hauptfenster Prozedur einer Anwendung, dass eine modale Menü Schleife beendet wurde.
ms.assetid: b2a9d537-af7c-4c8a-932a-95e45eb8deb5
keywords:
- WM_EXITMENULOOP von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_EXITMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8440e1a255968eb3e1607b5d54375900f7b5de16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741705"
---
# <a name="wm_exitmenuloop-message"></a><span data-ttu-id="278f3-104">WM \_ exitmenuloop-Meldung</span><span class="sxs-lookup"><span data-stu-id="278f3-104">WM\_EXITMENULOOP message</span></span>

<span data-ttu-id="278f3-105">Benachrichtigt die Hauptfenster Prozedur einer Anwendung, dass eine modale Menü Schleife beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="278f3-105">Notifies an application's main window procedure that a menu modal loop has been exited.</span></span>


```C++
#define WM_EXITMENULOOP                 0x0212
```



## <a name="parameters"></a><span data-ttu-id="278f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="278f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="278f3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="278f3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="278f3-108">Gibt an, ob das Menü ein Kontextmenü ist.</span><span class="sxs-lookup"><span data-stu-id="278f3-108">Specifies whether the menu is a shortcut menu.</span></span> <span data-ttu-id="278f3-109">Dieser Parameter hat den Wert **true** , wenn es sich um ein Kontextmenü handelt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="278f3-109">This parameter has a value of **TRUE** if it is a shortcut menu, **FALSE** if it is not.</span></span>

</dd> <dt>

<span data-ttu-id="278f3-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="278f3-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="278f3-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="278f3-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="278f3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="278f3-112">Return value</span></span>

<span data-ttu-id="278f3-113">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="278f3-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="278f3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="278f3-114">Remarks</span></span>

<span data-ttu-id="278f3-115">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="278f3-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="278f3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="278f3-116">Requirements</span></span>



| <span data-ttu-id="278f3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="278f3-117">Requirement</span></span> | <span data-ttu-id="278f3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="278f3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="278f3-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="278f3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="278f3-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="278f3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="278f3-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="278f3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="278f3-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="278f3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="278f3-123">Header</span><span class="sxs-lookup"><span data-stu-id="278f3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="278f3-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="278f3-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="278f3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="278f3-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="278f3-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="278f3-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="278f3-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="278f3-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="278f3-128">**WM- \_ entermenuloop**</span><span class="sxs-lookup"><span data-stu-id="278f3-128">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
</dt> <dt>

<span data-ttu-id="278f3-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="278f3-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="278f3-130">Menüs</span><span class="sxs-lookup"><span data-stu-id="278f3-130">Menus</span></span>](menus.md)
</dt> </dl>

 

