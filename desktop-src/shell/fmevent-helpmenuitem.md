---
description: Wird an eine DLL-Prozedur der Datei-Manager-Erweiterung gesendet, wenn der Benutzer F1 in einem Menü- oder Symbolleistenbefehlselement drückt. Die Erweiterung sollte WinHelp aufrufen, bei dem der hwnd-Parameter dieser Funktion auf den Wert des hwnd-Parameters der Erweiterung festgelegt ist.
title: FMEVENT_HELPMENUITEM (Wfext.h)
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
ms.openlocfilehash: 46cb246e91f9901204432527ba36fd8ac72beba4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842311"
---
# <a name="fmevent_helpmenuitem-message"></a><span data-ttu-id="6ce99-104">FMEVENT \_ HELPMENUITEM-Meldung</span><span class="sxs-lookup"><span data-stu-id="6ce99-104">FMEVENT\_HELPMENUITEM message</span></span>

<span data-ttu-id="6ce99-105">Wird an eine DLL-Prozedur der Datei-Manager-Erweiterung gesendet, wenn der Benutzer F1 in einem Menü- oder Symbolleistenbefehlselement drückt.</span><span class="sxs-lookup"><span data-stu-id="6ce99-105">Sent to a File Manager extension DLL procedure when the user presses F1 on a menu or toolbar command item.</span></span> <span data-ttu-id="6ce99-106">Die Erweiterung sollte [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)aufrufen, bei dem der *hwnd-Parameter* dieser Funktion auf den Wert des *hwnd-Parameters der Erweiterung festgelegt* ist.</span><span class="sxs-lookup"><span data-stu-id="6ce99-106">The extension should call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), with that function's *hwnd* parameter set to the value of the extension's *hwnd* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ce99-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ce99-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ce99-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ce99-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6ce99-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6ce99-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6ce99-110">*uItem*</span><span class="sxs-lookup"><span data-stu-id="6ce99-110">*uItem*</span></span> 
</dt> <dd>

<span data-ttu-id="6ce99-111">Ein -Wert, der das Menü- oder Symbolleistenbefehlselement identifiziert, für das Hilfe gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="6ce99-111">A value that identifies the menu or toolbar command item for which Help is desired.</span></span> <span data-ttu-id="6ce99-112">Die Erweiterungsprozedur verwendet diesen Wert, um zu bestimmen, wie WinHelp am besten [**aufruft.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)</span><span class="sxs-lookup"><span data-stu-id="6ce99-112">The extension procedure uses this value to determine how best to call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ce99-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ce99-113">Return value</span></span>

<span data-ttu-id="6ce99-114">Eine DLL-Erweiterungsprozedur sollte 0 (null) zurückgeben, wenn diese Meldung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="6ce99-114">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ce99-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ce99-115">Requirements</span></span>



| <span data-ttu-id="6ce99-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ce99-116">Requirement</span></span> | <span data-ttu-id="6ce99-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6ce99-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ce99-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ce99-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6ce99-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ce99-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6ce99-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ce99-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6ce99-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ce99-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6ce99-122">Header</span><span class="sxs-lookup"><span data-stu-id="6ce99-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ce99-123"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="6ce99-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ce99-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ce99-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ce99-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="6ce99-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="6ce99-126">**FMEVENT \_ HELPSTRING**</span><span class="sxs-lookup"><span data-stu-id="6ce99-126">**FMEVENT\_HELPSTRING**</span></span>](fmevent-helpstring.md)
</dt> </dl>

 

 




