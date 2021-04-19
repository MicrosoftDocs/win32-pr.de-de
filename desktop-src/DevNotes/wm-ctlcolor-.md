---
description: Die "WM \_ CtlColor"-Meldung wird in 16-Bit-Versionen von Windows verwendet, um das Farbschema von Listenfeldern, die Listenfelder von Kombinations Feldern, Meldungs Feldern, Schaltflächen Steuerelementen, Bearbeitungs Steuerelemente, statische Steuerelemente und Dialogfelder zu ändern. Hinweis Informationen zu dieser Nachricht und 32-Bit-Versionen von Windows finden Sie unter "Hinweise".
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: WM_CTLCOLOR Meldung (WINDOWSX. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8166979c17b7d2eef50af062e5df13712e9d32ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370131"
---
# <a name="wm_ctlcolor-message"></a><span data-ttu-id="d875c-103">WM- \_ CtlColor-Meldung</span><span class="sxs-lookup"><span data-stu-id="d875c-103">WM\_CTLCOLOR message</span></span>

<span data-ttu-id="d875c-104">Die " **WM \_ CtlColor** "-Meldung wird in 16-Bit-Versionen von Windows verwendet, um das Farbschema von Listenfeldern, die Listenfelder von Kombinations Feldern, Meldungs Feldern, Schaltflächen Steuerelementen, Bearbeitungs Steuerelemente, statische Steuerelemente und Dialogfelder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d875c-104">The **WM\_CTLCOLOR** message is used in 16-bit versions of Windows to change the color scheme of list boxes, the list boxes of combo boxes, message boxes, button controls, edit controls, static controls, and dialog boxes.</span></span>

> [!Note]  
> <span data-ttu-id="d875c-105">Informationen im Zusammenhang mit dieser Nachricht und 32-Bit-Versionen von Windows finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="d875c-105">For information related to this message and 32-bit versions of Windows, see Remarks.</span></span>

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a><span data-ttu-id="d875c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d875c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d875c-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d875c-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d875c-108">Ein Handle für das Zielfenster.</span><span class="sxs-lookup"><span data-stu-id="d875c-108">A handle to destination window.</span></span>

</dd> <dt>

<span data-ttu-id="d875c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d875c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d875c-110">Ein Handle für einen Anzeige Kontext (DC).</span><span class="sxs-lookup"><span data-stu-id="d875c-110">A handle to a display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="d875c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d875c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d875c-112">Ein Handle für ein untergeordnetes Fenster (-Steuerelement).</span><span class="sxs-lookup"><span data-stu-id="d875c-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d875c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d875c-113">Return value</span></span>

<span data-ttu-id="d875c-114">Wenn eine Anwendung diese Nachricht verarbeitet, wird ein Handle für einen Pinsel zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d875c-114">If an application processes this message, it returns a handle to a brush.</span></span> <span data-ttu-id="d875c-115">Das System verwendet den Pinsel, um den Hintergrund des Steuer Elements zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d875c-115">The system uses the brush to paint the background of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="d875c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d875c-116">Remarks</span></span>

<span data-ttu-id="d875c-117">Die **WM \_ CtlColor** -Meldung von 16-Bit-Fenstern wurde durch spezifischere Benachrichtigungen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d875c-117">The **WM\_CTLCOLOR** message from 16-bit Windows has been replaced by more specific notifications.</span></span> <span data-ttu-id="d875c-118">Diese Ersetzungen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d875c-118">These replacements include the following:</span></span>

-   [<span data-ttu-id="d875c-119">**WM \_ ctlcolorbtn**</span><span class="sxs-lookup"><span data-stu-id="d875c-119">**WM\_CTLCOLORBTN**</span></span>](../controls/wm-ctlcolorbtn.md)
-   [<span data-ttu-id="d875c-120">**WM \_ ctlcoloredit**</span><span class="sxs-lookup"><span data-stu-id="d875c-120">**WM\_CTLCOLOREDIT**</span></span>](../controls/wm-ctlcoloredit.md)
-   [<span data-ttu-id="d875c-121">**WM \_ ctlcolordlg**</span><span class="sxs-lookup"><span data-stu-id="d875c-121">**WM\_CTLCOLORDLG**</span></span>](../dlgbox/wm-ctlcolordlg.md)
-   [<span data-ttu-id="d875c-122">**WM \_ ctlcolorlistbox**</span><span class="sxs-lookup"><span data-stu-id="d875c-122">**WM\_CTLCOLORLISTBOX**</span></span>](../controls/wm-ctlcolorlistbox.md)
-   [<span data-ttu-id="d875c-123">**WM \_ ctlcolorscrollbar**</span><span class="sxs-lookup"><span data-stu-id="d875c-123">**WM\_CTLCOLORSCROLLBAR**</span></span>](../controls/wm-ctlcolorscrollbar.md)
-   [<span data-ttu-id="d875c-124">**WM \_ ctlcolorstatic**</span><span class="sxs-lookup"><span data-stu-id="d875c-124">**WM\_CTLCOLORSTATIC**</span></span>](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a><span data-ttu-id="d875c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d875c-125">Requirements</span></span>



| <span data-ttu-id="d875c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d875c-126">Requirement</span></span> | <span data-ttu-id="d875c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d875c-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d875c-128">Header</span><span class="sxs-lookup"><span data-stu-id="d875c-128">Header</span></span><br/> | <dl> <span data-ttu-id="d875c-129"><dt>WINDOWSX. h</dt></span><span class="sxs-lookup"><span data-stu-id="d875c-129"><dt>WindowsX.h</dt></span></span> </dl> |



 

 
