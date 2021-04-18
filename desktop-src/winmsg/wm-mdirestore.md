---
description: Eine Anwendung sendet die WM- \_ mdirestore-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster von maximierter oder minimierter Größe wiederherzustellen.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: WM_MDIRESTORE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354464"
---
# <a name="wm_mdirestore-message"></a><span data-ttu-id="879c8-103">WM- \_ mumgeleitet-Speicher Nachricht</span><span class="sxs-lookup"><span data-stu-id="879c8-103">WM\_MDIRESTORE message</span></span>

<span data-ttu-id="879c8-104">Eine Anwendung sendet die **WM- \_ mdirestore** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster von maximierter oder minimierter Größe wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="879c8-104">An application sends the **WM\_MDIRESTORE** message to a multiple-document interface (MDI) client window to restore an MDI child window from maximized or minimized size.</span></span>


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a><span data-ttu-id="879c8-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="879c8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="879c8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="879c8-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="879c8-107">Ein Handle für das untergeordnete MDI-Fenster, das wieder hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="879c8-107">A handle to the MDI child window to be restored.</span></span>

</dd> <dt>

<span data-ttu-id="879c8-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="879c8-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="879c8-109">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="879c8-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="879c8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="879c8-110">Return value</span></span>

<span data-ttu-id="879c8-111">Typ: **null**</span><span class="sxs-lookup"><span data-stu-id="879c8-111">Type: **zero**</span></span>

<span data-ttu-id="879c8-112">Der Rückgabewert ist immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="879c8-112">The return value is always zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="879c8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="879c8-113">Requirements</span></span>



| <span data-ttu-id="879c8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="879c8-114">Requirement</span></span> | <span data-ttu-id="879c8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="879c8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="879c8-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="879c8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="879c8-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="879c8-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="879c8-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="879c8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="879c8-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="879c8-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="879c8-120">Header</span><span class="sxs-lookup"><span data-stu-id="879c8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="879c8-121"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="879c8-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="879c8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="879c8-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="879c8-123">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="879c8-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="879c8-124">**WM- \_ mdimaximierung**</span><span class="sxs-lookup"><span data-stu-id="879c8-124">**WM\_MDIMAXIMIZE**</span></span>](wm-mdimaximize.md)
</dt> <dt>

<span data-ttu-id="879c8-125">**Licher**</span><span class="sxs-lookup"><span data-stu-id="879c8-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="879c8-126">Mehrere Dokument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="879c8-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




