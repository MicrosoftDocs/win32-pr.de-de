---
description: Wird an das oberste betroffene Fenster gesendet, nachdem die Eingabe Sprache einer Anwendung geändert wurde. Legen Sie alle anwendungsspezifischen Einstellungen fest, und übergeben Sie die Nachricht an die defwindowproc-Funktion, die die Nachricht an alle untergeordneten Fenster der ersten Ebene übergibt.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: WM_INPUTLANGCHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128961"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="ff261-104">WM- \_ inputlangchange-Meldung</span><span class="sxs-lookup"><span data-stu-id="ff261-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="ff261-105">Wird an das oberste betroffene Fenster gesendet, nachdem die Eingabe Sprache einer Anwendung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ff261-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="ff261-106">Legen Sie alle anwendungsspezifischen Einstellungen fest, und übergeben Sie die Nachricht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion, die die Nachricht an alle untergeordneten Fenster der ersten Ebene übergibt.</span><span class="sxs-lookup"><span data-stu-id="ff261-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="ff261-107">Diese untergeordneten Fenster können die Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben, damit Sie die Nachricht an ihre untergeordneten Fenster weiterleiten kann usw.</span><span class="sxs-lookup"><span data-stu-id="ff261-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="ff261-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ff261-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a><span data-ttu-id="ff261-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff261-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff261-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff261-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff261-111">Der Zeichensatz des neuen Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="ff261-111">The character set of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="ff261-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff261-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff261-113">Der Eingabe Gebiets Schema Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="ff261-113">The input locale identifier.</span></span> <span data-ttu-id="ff261-114">Weitere Informationen finden Sie unter [Sprachen, Gebiets Schemas und Tastatur Layouts](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="ff261-114">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff261-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff261-115">Return value</span></span>

<span data-ttu-id="ff261-116">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="ff261-116">Type: **LRESULT**</span></span>

<span data-ttu-id="ff261-117">Eine Anwendung sollte bei der Verarbeitung dieser Nachricht einen Wert ungleich 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ff261-117">An application should return nonzero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff261-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff261-118">Requirements</span></span>



| <span data-ttu-id="ff261-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff261-119">Requirement</span></span> | <span data-ttu-id="ff261-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ff261-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff261-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff261-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ff261-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff261-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ff261-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff261-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ff261-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff261-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ff261-125">Header</span><span class="sxs-lookup"><span data-stu-id="ff261-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff261-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="ff261-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff261-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff261-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff261-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ff261-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ff261-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="ff261-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="ff261-130">**WM \_ inputlangchangerequest**</span><span class="sxs-lookup"><span data-stu-id="ff261-130">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)
</dt> <dt>

<span data-ttu-id="ff261-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ff261-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff261-132">Windows</span><span class="sxs-lookup"><span data-stu-id="ff261-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
