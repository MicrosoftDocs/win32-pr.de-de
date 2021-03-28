---
description: Wird an eine DLL-Prozedur der Datei-Manager-Erweiterung gesendet, wenn der Benutzer F1 in einem Menü oder Symbolleisten-Befehls Element drückt. Die Erweiterung sollte WinHelp aufrufen, wobei der hWnd-Parameter der Funktion auf den Wert des HWND-Parameters der Erweiterung festgelegt ist.
title: FMEVENT_HELPMENUITEM Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: c20b5828a6e2362b9b9c13fc9b2986b0ea7b5fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977089"
---
# <a name="fmevent_helpmenuitem-message"></a><span data-ttu-id="1f258-104">Meldung zu "f mevent \_ helpmenuitem"</span><span class="sxs-lookup"><span data-stu-id="1f258-104">FMEVENT\_HELPMENUITEM message</span></span>

<span data-ttu-id="1f258-105">Wird an eine DLL-Prozedur der Datei-Manager-Erweiterung gesendet, wenn der Benutzer F1 in einem Menü oder Symbolleisten-Befehls Element drückt.</span><span class="sxs-lookup"><span data-stu-id="1f258-105">Sent to a File Manager extension DLL procedure when the user presses F1 on a menu or toolbar command item.</span></span> <span data-ttu-id="1f258-106">Die Erweiterung sollte [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)aufrufen, wobei der *HWND* -Parameter der Funktion auf den Wert des *HWND* -Parameters der Erweiterung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1f258-106">The extension should call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), with that function's *hwnd* parameter set to the value of the extension's *hwnd* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f258-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f258-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f258-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f258-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1f258-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1f258-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1f258-110">*uitem*</span><span class="sxs-lookup"><span data-stu-id="1f258-110">*uItem*</span></span> 
</dt> <dd>

<span data-ttu-id="1f258-111">Ein-Wert, der das Menü oder das Symbolleisten-Befehls Element identifiziert, für das die Hilfe gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="1f258-111">A value that identifies the menu or toolbar command item for which Help is desired.</span></span> <span data-ttu-id="1f258-112">Die Erweiterungs Prozedur verwendet diesen Wert, um zu bestimmen, wie [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)am besten aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1f258-112">The extension procedure uses this value to determine how best to call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f258-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f258-113">Return value</span></span>

<span data-ttu-id="1f258-114">Eine Erweiterungs-DLL-Prozedur sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="1f258-114">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f258-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1f258-115">Requirements</span></span>



| <span data-ttu-id="1f258-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f258-116">Requirement</span></span> | <span data-ttu-id="1f258-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1f258-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1f258-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f258-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1f258-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f258-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1f258-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f258-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1f258-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f258-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1f258-122">Header</span><span class="sxs-lookup"><span data-stu-id="1f258-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f258-123"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f258-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f258-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1f258-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f258-125">**"F"**</span><span class="sxs-lookup"><span data-stu-id="1f258-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="1f258-126">**-HelpString für "f" \_**</span><span class="sxs-lookup"><span data-stu-id="1f258-126">**FMEVENT\_HELPSTRING**</span></span>](fmevent-helpstring.md)
</dt> </dl>

 

 




