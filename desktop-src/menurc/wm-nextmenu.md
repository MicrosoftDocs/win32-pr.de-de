---
title: WM_NEXTMENU Meldung (Winuser. h)
description: Wird an eine Anwendung gesendet, wenn mit der nach-rechts-oder der nach-links-Taste zwischen der Menüleiste und dem Systemmenü gewechselt wird.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecb8efe8c80a3355a30ab0abf28019f87b33963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957218"
---
# <a name="wm_nextmenu-message"></a><span data-ttu-id="2bb63-104">WM- \_ nextmenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="2bb63-104">WM\_NEXTMENU message</span></span>

<span data-ttu-id="2bb63-105">Wird an eine Anwendung gesendet, wenn mit der nach-rechts-oder der nach-links-Taste zwischen der Menüleiste und dem Systemmenü gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="2bb63-105">Sent to an application when the right or left arrow key is used to switch between the menu bar and the system menu.</span></span>


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a><span data-ttu-id="2bb63-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bb63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bb63-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2bb63-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2bb63-108">Der Code für den virtuellen Schlüssel des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="2bb63-108">The virtual-key code of the key.</span></span> <span data-ttu-id="2bb63-109">Siehe [**virtuelle Schlüssel Codes**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="2bb63-109">See [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="2bb63-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2bb63-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2bb63-111">Ein Zeiger auf eine [**mdinextmenu**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) -Struktur, die Informationen über das zu aktivierende Menü enthält.</span><span class="sxs-lookup"><span data-stu-id="2bb63-111">A pointer to a [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) structure that contains information about the menu to be activated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bb63-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2bb63-112">Remarks</span></span>

<span data-ttu-id="2bb63-113">Wenn Sie auf diese Meldung reagieren, kann die Anwendung das Menü angeben, zu dem im **hmenunext** -Member von [**mdinextmenu**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) gewechselt werden soll, und das Fenster, um die Menü Benachrichtigungs Meldungen im **hwndnext** -Member der **mdinextmenu** -Struktur zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="2bb63-113">In responding to this message, the application can specify the menu to switch to in the **hmenuNext** member of [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) and the window to receive the menu notification messages in the **hwndNext** member of the **MDINEXTMENU** structure.</span></span> <span data-ttu-id="2bb63-114">Beide Elemente müssen festgelegt werden, damit die Änderungen wirksam werden (Sie sind anfänglich **null**).</span><span class="sxs-lookup"><span data-stu-id="2bb63-114">You must set both members for the changes to take effect (they are initially **NULL**).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bb63-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bb63-115">Requirements</span></span>



| <span data-ttu-id="2bb63-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bb63-116">Requirement</span></span> | <span data-ttu-id="2bb63-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb63-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bb63-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2bb63-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2bb63-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bb63-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2bb63-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2bb63-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2bb63-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bb63-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2bb63-122">Header</span><span class="sxs-lookup"><span data-stu-id="2bb63-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bb63-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="2bb63-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bb63-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2bb63-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="2bb63-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="2bb63-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2bb63-126">**Mdinextmenu**</span><span class="sxs-lookup"><span data-stu-id="2bb63-126">**MDINEXTMENU**</span></span>](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

<span data-ttu-id="2bb63-127">**Licher**</span><span class="sxs-lookup"><span data-stu-id="2bb63-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2bb63-128">Menüs</span><span class="sxs-lookup"><span data-stu-id="2bb63-128">Menus</span></span>](menus.md)
</dt> </dl>

 

