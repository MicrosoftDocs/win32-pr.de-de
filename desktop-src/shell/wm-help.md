---
description: Gibt an, dass der Benutzer die F1-Taste gedrückt hat.
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: WM_HELP Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd1b042a2e57fb64eb3aa81f38cec336e33efab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979464"
---
# <a name="wm_help-message"></a><span data-ttu-id="8811a-103">WM- \_ Hilfe Meldung</span><span class="sxs-lookup"><span data-stu-id="8811a-103">WM\_HELP message</span></span>

<span data-ttu-id="8811a-104">Gibt an, dass der Benutzer die F1-Taste gedrückt hat.</span><span class="sxs-lookup"><span data-stu-id="8811a-104">Indicates that the user pressed the F1 key.</span></span> <span data-ttu-id="8811a-105">Wenn ein Menü aktiv ist, wenn F1 gedrückt wird, wird die **WM- \_ Hilfe** an das Fenster gesendet, das dem Menü zugeordnet ist. andernfalls wird die **WM- \_ Hilfe** an das Fenster mit dem Tastaturfokus gesendet.</span><span class="sxs-lookup"><span data-stu-id="8811a-105">If a menu is active when F1 is pressed, **WM\_HELP** is sent to the window associated with the menu; otherwise, **WM\_HELP** is sent to the window that has the keyboard focus.</span></span> <span data-ttu-id="8811a-106">Wenn kein Fenster den Tastaturfokus besitzt, wird die **WM- \_ Hilfe** an das derzeit aktive Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="8811a-106">If no window has the keyboard focus, **WM\_HELP** is sent to the currently active window.</span></span>

## <a name="parameters"></a><span data-ttu-id="8811a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8811a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8811a-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8811a-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8811a-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8811a-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8811a-110">*lphi*</span><span class="sxs-lookup"><span data-stu-id="8811a-110">*lphi*</span></span> 
</dt> <dd>

<span data-ttu-id="8811a-111">Die Adresse einer [**helpinfo**](/windows/win32/api/winuser/ns-winuser-helpinfo) -Struktur, die Informationen über das Menü Element, das Steuerelement, das Dialogfeld oder das Fenster enthält, für das die Hilfe angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="8811a-111">The address of a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains information about the menu item, control, dialog box, or window for which Help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8811a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8811a-112">Return value</span></span>

<span data-ttu-id="8811a-113">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="8811a-113">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8811a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8811a-114">Remarks</span></span>

<span data-ttu-id="8811a-115">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt die **WM- \_ Hilfe** an das übergeordnete Fenster eines untergeordneten Fensters oder an den Besitzer eines Fensters der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="8811a-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes **WM\_HELP** to the parent window of a child window or to the owner of a top-level window.</span></span>

## <a name="requirements"></a><span data-ttu-id="8811a-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8811a-116">Requirements</span></span>



| <span data-ttu-id="8811a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8811a-117">Requirement</span></span> | <span data-ttu-id="8811a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8811a-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8811a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8811a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8811a-120">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8811a-120">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8811a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8811a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8811a-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8811a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8811a-123">Header</span><span class="sxs-lookup"><span data-stu-id="8811a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8811a-124"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="8811a-124"><dt>Winuser.h</dt></span></span> </dl> |



 

 
