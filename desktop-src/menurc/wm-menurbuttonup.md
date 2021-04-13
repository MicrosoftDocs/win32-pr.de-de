---
title: WM_MENURBUTTONUP Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer die Rechte Maustaste loslässt, während sich der Cursor auf einem Menü Element befindet.
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- WM_MENURBUTTONUP von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341348"
---
# <a name="wm_menurbuttonup-message"></a><span data-ttu-id="8b402-104">WM- \_ menurbuttonup-Meldung</span><span class="sxs-lookup"><span data-stu-id="8b402-104">WM\_MENURBUTTONUP message</span></span>

<span data-ttu-id="8b402-105">Wird gesendet, wenn der Benutzer die Rechte Maustaste loslässt, während sich der Cursor auf einem Menü Element befindet.</span><span class="sxs-lookup"><span data-stu-id="8b402-105">Sent when the user releases the right mouse button while the cursor is on a menu item.</span></span>


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a><span data-ttu-id="8b402-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b402-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b402-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b402-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b402-108">Der null basierte Index des Menü Elements, auf dem die Rechte Maustaste losgelassen wurde.</span><span class="sxs-lookup"><span data-stu-id="8b402-108">The zero-based index of the menu item on which the right mouse button was released.</span></span>

</dd> <dt>

<span data-ttu-id="8b402-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b402-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b402-110">Ein Handle für das Menü, das das Element enthält.</span><span class="sxs-lookup"><span data-stu-id="8b402-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b402-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b402-111">Remarks</span></span>

<span data-ttu-id="8b402-112">Mit der " **WM \_ menurbuttonup** "-Meldung können Anwendungen ein Kontext abhängiger Menü bereitstellen, das auch als Kontextmenü für das Menü Element bezeichnet wird, das in dieser Meldung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b402-112">The **WM\_MENURBUTTONUP** message allows applications to provide a context-sensitive menu also known as a shortcut menu for the menu item specified in this message.</span></span> <span data-ttu-id="8b402-113">Wenn Sie ein Kontextmenü für ein Menü Element anzeigen möchten, können Sie die [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) -Funktion mit **TPM \_ recurse** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8b402-113">To display a context-sensitive menu for a menu item, call the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function with **TPM\_RECURSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b402-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b402-114">Requirements</span></span>



| <span data-ttu-id="8b402-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b402-115">Requirement</span></span> | <span data-ttu-id="8b402-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8b402-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b402-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b402-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8b402-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b402-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8b402-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b402-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8b402-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b402-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8b402-121">Header</span><span class="sxs-lookup"><span data-stu-id="8b402-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b402-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="8b402-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b402-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b402-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b402-124">Übersicht über Menüs</span><span class="sxs-lookup"><span data-stu-id="8b402-124">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





