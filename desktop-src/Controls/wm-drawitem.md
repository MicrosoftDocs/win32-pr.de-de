---
title: WM_DRAWITEM Meldung (Winuser. h)
description: Wird an das übergeordnete Fenster einer vom Besitzer gezeichneten Schaltfläche, einem Kombinations Feld, einem Listenfeld oder einem Menü gesendet, wenn sich ein visueller Aspekt der Schaltfläche, des Kombinations Felds, des Listen Felds oder des Menüs geändert hat.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- Windows-Steuerelemente für WM_DRAWITEM Meldung
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bd6465a560a0590ed9f5b483afae4c0d72d637
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741361"
---
# <a name="wm_drawitem-message"></a><span data-ttu-id="d60af-104">WM- \_ DrawItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d60af-104">WM\_DRAWITEM message</span></span>

<span data-ttu-id="d60af-105">Wird an das übergeordnete Fenster einer vom Besitzer gezeichneten Schaltfläche, einem Kombinations Feld, einem Listenfeld oder einem Menü gesendet, wenn sich ein visueller Aspekt der Schaltfläche, des Kombinations Felds, des Listen Felds oder des Menüs geändert hat.</span><span class="sxs-lookup"><span data-stu-id="d60af-105">Sent to the parent window of an owner-drawn button, combo box, list box, or menu when a visual aspect of the button, combo box, list box, or menu has changed.</span></span>

<span data-ttu-id="d60af-106">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d60af-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d60af-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d60af-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d60af-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d60af-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d60af-109">Gibt den Bezeichner des Steuer Elements an, das die **WM- \_ DrawItem** -Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="d60af-109">Specifies the identifier of the control that sent the **WM\_DRAWITEM** message.</span></span> <span data-ttu-id="d60af-110">Wenn die Nachricht von einem Menü gesendet wurde, ist dieser Parameter gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d60af-110">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="d60af-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d60af-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d60af-112">Ein Zeiger auf eine [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur, die Informationen über das zu zeichende Element und den Typ der erforderlichen Zeichnung enthält.</span><span class="sxs-lookup"><span data-stu-id="d60af-112">Pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d60af-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d60af-113">Return value</span></span>

<span data-ttu-id="d60af-114">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d60af-114">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d60af-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d60af-115">Remarks</span></span>

<span data-ttu-id="d60af-116">Standardmäßig zeichnet die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion das Fokus Rechteck für ein vom Besitzer gezeichnetes Listenfeld Element.</span><span class="sxs-lookup"><span data-stu-id="d60af-116">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the focus rectangle for an owner-drawn list box item.</span></span>

<span data-ttu-id="d60af-117">Der *itemaction* -Member der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur gibt den Zeichnungs Vorgang an, den eine Anwendung ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="d60af-117">The *itemAction* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="d60af-118">Vor der Rückgabe aus der Verarbeitung dieser Nachricht muss eine Anwendung sicherstellen, dass der vom *hdc* -Member der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur identifizierte Gerätekontext den Standardstatus aufweist.</span><span class="sxs-lookup"><span data-stu-id="d60af-118">Before returning from processing this message, an application should ensure that the device context identified by the *hDC* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="d60af-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d60af-119">Requirements</span></span>



| <span data-ttu-id="d60af-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d60af-120">Requirement</span></span> | <span data-ttu-id="d60af-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d60af-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d60af-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d60af-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d60af-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d60af-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d60af-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d60af-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d60af-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d60af-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d60af-126">Header</span><span class="sxs-lookup"><span data-stu-id="d60af-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d60af-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d60af-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d60af-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d60af-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="d60af-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d60af-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d60af-130">**DRAWITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="d60af-130">**DRAWITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

<span data-ttu-id="d60af-131">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="d60af-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d60af-132">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="d60af-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

