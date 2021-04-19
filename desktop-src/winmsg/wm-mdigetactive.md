---
description: Eine Anwendung sendet die WM- \_ mdigetactive-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um das Handle für das aktive untergeordnete MDI-Fenster abzurufen.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: WM_MDIGETACTIVE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373167"
---
# <a name="wm_mdigetactive-message"></a><span data-ttu-id="f73f9-103">WM- \_ mdigetactive-Meldung</span><span class="sxs-lookup"><span data-stu-id="f73f9-103">WM\_MDIGETACTIVE message</span></span>

<span data-ttu-id="f73f9-104">Eine Anwendung sendet die **WM- \_ mdigetactive** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um das Handle für das aktive untergeordnete MDI-Fenster abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f73f9-104">An application sends the **WM\_MDIGETACTIVE** message to a multiple-document interface (MDI) client window to retrieve the handle to the active MDI child window.</span></span>


```C++
#define WM_MDIGETACTIVE                  0x0229
```



## <a name="parameters"></a><span data-ttu-id="f73f9-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f73f9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f73f9-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f73f9-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f73f9-107">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f73f9-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f73f9-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f73f9-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f73f9-109">Der maximierte Zustand.</span><span class="sxs-lookup"><span data-stu-id="f73f9-109">The maximized state.</span></span> <span data-ttu-id="f73f9-110">Wenn dieser Parameter nicht **null** ist, handelt es sich um einen Zeiger auf einen Wert, der den maximierten Zustand des untergeordneten MDI-Fensters angibt.</span><span class="sxs-lookup"><span data-stu-id="f73f9-110">If this parameter is not **NULL**, it is a pointer to a value that indicates the maximized state of the MDI child window.</span></span> <span data-ttu-id="f73f9-111">Wenn der Wert **true** ist, wird das Fenster maximiert. der Wert **false** gibt an, dass dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="f73f9-111">If the value is **TRUE**, the window is maximized; a value of **FALSE** indicates that it is not.</span></span> <span data-ttu-id="f73f9-112">Wenn dieser Parameter **null** ist, wird der-Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f73f9-112">If this parameter is **NULL**, the parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f73f9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f73f9-113">Return value</span></span>

<span data-ttu-id="f73f9-114">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="f73f9-114">Type: **HWND**</span></span>

<span data-ttu-id="f73f9-115">Der Rückgabewert ist das Handle des aktiven untergeordneten MDI-Fensters.</span><span class="sxs-lookup"><span data-stu-id="f73f9-115">The return value is the handle to the active MDI child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="f73f9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f73f9-116">Requirements</span></span>



| <span data-ttu-id="f73f9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f73f9-117">Requirement</span></span> | <span data-ttu-id="f73f9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f73f9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f73f9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f73f9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f73f9-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f73f9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f73f9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f73f9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f73f9-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f73f9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f73f9-123">Header</span><span class="sxs-lookup"><span data-stu-id="f73f9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f73f9-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f73f9-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f73f9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f73f9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f73f9-126">Übersicht über mehrere Dokument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f73f9-126">Multiple Document Interface Overview</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




