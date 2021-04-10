---
title: WM_GETOBJECT Meldung (Winuser. h)
description: Wird von Microsoft Active Accessibility und Microsoft UI Automation gesendet, um Informationen über ein Barrierefreies Objekt zu erhalten, das in einer Serveranwendung enthalten ist.
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- Windows-Barrierefreiheit für WM_GETOBJECT Meldung
topic_type:
- apiref
api_name:
- WM_GETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcac5c7f6dd8203c32b9f6f3c4eb59144cc3f8ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106466"
---
# <a name="wm_getobject-message"></a><span data-ttu-id="124b3-104">WM- \_ GetObject-Nachricht</span><span class="sxs-lookup"><span data-stu-id="124b3-104">WM\_GETOBJECT message</span></span>

<span data-ttu-id="124b3-105">Wird von Microsoft Active Accessibility und Microsoft UI Automation gesendet, um Informationen über ein Barrierefreies Objekt zu erhalten, das in einer Serveranwendung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="124b3-105">Sent by both Microsoft Active Accessibility and Microsoft UI Automation to obtain information about an accessible object contained in a server application.</span></span>

<span data-ttu-id="124b3-106">Anwendungen senden diese Nachricht niemals direkt.</span><span class="sxs-lookup"><span data-stu-id="124b3-106">Applications never send this message directly.</span></span> <span data-ttu-id="124b3-107">Microsoft Active Accessibility sendet diese Nachricht als Antwort auf Aufrufe von [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)oder [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="124b3-107">Microsoft Active Accessibility sends this message in response to calls to [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span> <span data-ttu-id="124b3-108">Diese Nachricht wird jedoch von Server Anwendungen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="124b3-108">However, server applications handle this message.</span></span> <span data-ttu-id="124b3-109">Die Benutzeroberflächenautomatisierung sendet diese Nachricht als Antwort auf Aufrufe von [**iuiautomation:: elementfromhandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**elementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)und [**getfocucements**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)sowie bei der Behandlung von Ereignissen, die von einem Client registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="124b3-109">UI Automation sends this message in response to calls to [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which a client has registered.</span></span>


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a><span data-ttu-id="124b3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="124b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="124b3-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="124b3-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="124b3-112">Stellt zusätzliche Informationen über die Meldung bereit und wird nur vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="124b3-112">Provides additional information about the message and is used only by the system.</span></span> <span data-ttu-id="124b3-113">Server übergeben *dwFlags* als *wParam* -Parameter beim Aufrufen von [**lresultfrowbject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) bei der Verarbeitung der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="124b3-113">Servers pass *dwFlags* as the *wParam* parameter in the call to [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) when handling the message.</span></span>

</dd> <dt>

<span data-ttu-id="124b3-114">*dwobjid*</span><span class="sxs-lookup"><span data-stu-id="124b3-114">*dwObjId*</span></span> 
</dt> <dd>

<span data-ttu-id="124b3-115">Objekt Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="124b3-115">Object identifier.</span></span> <span data-ttu-id="124b3-116">Dieser Wert ist eine der [objektbezeichnerkonstanten](object-identifiers.md) oder ein benutzerdefinierter Objekt Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="124b3-116">This value is one of the [object identifier](object-identifiers.md) constants or a custom object identifier.</span></span> <span data-ttu-id="124b3-117">Eine Serveranwendung muss diesen Wert überprüfen, um den Typ der angeforderten Informationen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="124b3-117">A server application must check this value to identify the type of information being requested.</span></span> <span data-ttu-id="124b3-118">Bevor Sie diesen Wert mit den objID \_ -Werten vergleichen, muss der Server ihn in **DWORD** umwandeln. andernfalls kann die Signierungs Erweiterung des *LPARAM* -Element mit dem Vergleich in 64-Bit-Fenstern beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="124b3-118">Before comparing this value against the OBJID\_ values, the server must cast it to **DWORD**; otherwise, on 64-bit Windows, the sign extension of the *lParam* can interfere with the comparison.</span></span>

-   <span data-ttu-id="124b3-119">Wenn *dwobjid* einer der ObjID- \_ Werte ist, z. b. [**objID- \_ Client**](object-identifiers.md), ist die Anforderung für ein Microsoft Active Accessibility Objekt, das [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementiert.</span><span class="sxs-lookup"><span data-stu-id="124b3-119">If *dwObjId* is one of the OBJID\_ values such as [**OBJID\_CLIENT**](object-identifiers.md), the request is for a Microsoft Active Accessibility object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>
-   <span data-ttu-id="124b3-120">Wenn *dwobjid* gleich **uiarootobjectid** ist, ist die Anforderung ein Benutzeroberflächenautomatisierungs-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="124b3-120">If *dwObjId* is equal to **UiaRootObjectId**, the request is for a UI Automation provider.</span></span> <span data-ttu-id="124b3-121">Wenn der Server die Benutzeroberflächen Automatisierung implementiert, sollte er mithilfe der [**uiareturnrawelementprovider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) -Funktion einen Anbieter zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="124b3-121">If the server is implementing UI Automation, it should return a provider using the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="124b3-122">Wenn *dwobjid* " [**objID \_ nativeom**](object-identifiers.md)" ist, ist die Anforderung für das zugrunde liegende Objektmodell des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="124b3-122">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md), the request is for the control's underlying object model.</span></span> <span data-ttu-id="124b3-123">Wenn das Steuerelement diese Anforderung unterstützt, sollte es eine entsprechende COM-Schnittstelle zurückgeben, indem Sie die [**lresultfrobobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="124b3-123">If the control supports this request, it should return an appropriate COM interface by calling the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="124b3-124">Wenn *dwobjid* " [**objID \_ queryclassnameidx**](object-identifiers.md)" ist, ist die Anforderung, dass sich das Steuerelement selbst als standardmäßiges Windows-Steuerelement oder ein gängiges Steuerelement identifiziert, das von der allgemeinen Steuerelement Bibliothek (ComCtrl.dll) implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="124b3-124">If *dwObjId* is [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md), the request is for the control to identify itself as a standard Windows control or a common control implemented by the common control library (ComCtrl.dll).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="124b3-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="124b3-125">Return value</span></span>

<span data-ttu-id="124b3-126">Wenn das Fenster oder das Steuerelement nicht auf diese Meldung reagieren muss, sollte die Nachricht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben werden. Andernfalls sollte das Fenster oder Steuerelement einen Wert zurückgeben, der der von *dwobjid* angegebenen Anforderung entspricht:</span><span class="sxs-lookup"><span data-stu-id="124b3-126">If the window or control does not need to respond to this message, it should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function; otherwise, the window or control should return a value that corresponds to the request specified by *dwObjId*:</span></span>

-   <span data-ttu-id="124b3-127">Wenn das Fenster oder das Steuerelement die Benutzeroberflächen Automatisierung implementiert, sollte das Fenster oder Steuerelement den Wert zurückgeben, der durch einen Aufrufder [**uiareturnrawelementprovider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) -Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="124b3-127">If the window or control implements UI Automation, the window or control should return the value obtained by a call to the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="124b3-128">Wenn *dwobjid* auf [**objID \_ nativeom**](object-identifiers.md) festgelegt ist und das Fenster ein System eigenes Objektmodell verfügbar macht, sollte das Fenster den Wert zurückgeben, der durch einen Aufrufe der [**lresultfrofubject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) -Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="124b3-128">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md) and the window exposes a native Object Model, the windows should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="124b3-129">Wenn *dwobjid* ein [**objID- \_ Client**](object-identifiers.md) ist und das Fenster [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementiert, sollte das Fenster den Wert zurückgeben, der durch einen Aufruf der [**lresultfrofubject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) -Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="124b3-129">If *dwObjId* is [**OBJID\_CLIENT**](object-identifiers.md) and the window implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), the window should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="124b3-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="124b3-130">Remarks</span></span>

<span data-ttu-id="124b3-131">Wenn ein Client [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) oder eine der anderen **accessibleobjectfrom**_X_ -Funktionen aufruft, die eine Schnittstelle zu einem Objekt abrufen, sendet Microsoft Active Accessibility die **WM- \_ GetObject** -Nachricht an die entsprechende Fenster Prozedur innerhalb der entsprechenden Serveranwendung.</span><span class="sxs-lookup"><span data-stu-id="124b3-131">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other **AccessibleObjectFrom**_X_ functions that retrieve an interface to an object, Microsoft Active Accessibility sends the **WM\_GETOBJECT** message to the appropriate window procedure within the appropriate server application.</span></span> <span data-ttu-id="124b3-132">Beim Verarbeiten von **WM \_ GetObject** wird von Server Anwendungen [**lresultfrobugbject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) aufgerufen und der Rückgabewert dieser Funktion als Rückgabewert für die Nachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="124b3-132">While processing **WM\_GETOBJECT**, server applications call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) and use the return value of this function as the return value for the message.</span></span> <span data-ttu-id="124b3-133">Microsoft Active Accessibility führt in Verbindung mit der com-Bibliothek das entsprechende Marshalling durch und übergibt den Schnittstellen Zeiger vom Server an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="124b3-133">Microsoft Active Accessibility, in conjunction with the COM library, performs the appropriate marshaling and passes the interface pointer from the server back to the client.</span></span>

<span data-ttu-id="124b3-134">Server Antworten nicht auf das **WM- \_ GetObject** -Objekt, bevor das Objekt vollständig initialisiert wurde, oder nachdem es begonnen hat, zu schließen.</span><span class="sxs-lookup"><span data-stu-id="124b3-134">Servers do not respond to **WM\_GETOBJECT** before the object is fully initialized or after it begins to close down.</span></span> <span data-ttu-id="124b3-135">Wenn eine Anwendung ein neues Fenster erstellt, sendet das System das [**Ereignis \_ Objekt \_ Create**](event-constants.md) zum Benachrichtigen von Clients, bevor es die [WM \_ Create](../winmsg/wm-create.md) -Meldung an die Fenster Prozedur der Anwendung sendet.</span><span class="sxs-lookup"><span data-stu-id="124b3-135">When an application creates a new window, the system sends [**EVENT\_OBJECT\_CREATE**](event-constants.md) to notify clients before it sends the [WM\_CREATE](../winmsg/wm-create.md) message to the application's window procedure.</span></span> <span data-ttu-id="124b3-136">Da viele Anwendungen WM Create verwenden, \_ um den Initialisierungs Prozess zu starten, reagieren Server erst dann auf die **WM- \_ GetObject** -Nachricht, wenn die Verarbeitung der **WM \_ Create** -Nachricht abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="124b3-136">Because many applications use WM\_CREATE to start their initialization process, servers do not respond to the **WM\_GETOBJECT** message until finished processing the **WM\_CREATE** message.</span></span>

<span data-ttu-id="124b3-137">Ein Server verwendet **WM \_ GetObject** , um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="124b3-137">A server uses **WM\_GETOBJECT** to perform the following tasks:</span></span>

-   [<span data-ttu-id="124b3-138">Neue barrierefreie Objekte erstellen</span><span class="sxs-lookup"><span data-stu-id="124b3-138">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="124b3-139">Wieder verwenden vorhandener Zeiger auf Objekte</span><span class="sxs-lookup"><span data-stu-id="124b3-139">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="124b3-140">Erstellen neuer Schnittstellen für dasselbe Objekt</span><span class="sxs-lookup"><span data-stu-id="124b3-140">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

<span data-ttu-id="124b3-141">Für Clients bedeutet dies, dass Sie abhängig von der Aktion des Servers möglicherweise unterschiedliche Schnittstellen Zeiger für dasselbe Benutzeroberflächen Element erhalten.</span><span class="sxs-lookup"><span data-stu-id="124b3-141">For clients, this means that they might receive distinct interface pointers for the same user interface element, depending on the server's action.</span></span> <span data-ttu-id="124b3-142">Um zu ermitteln, ob zwei Schnittstellen Zeiger auf dasselbe Benutzeroberflächen Element zeigen, vergleichen Clients die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften des Objekts.</span><span class="sxs-lookup"><span data-stu-id="124b3-142">To determine if two interface pointers point to the same user interface element, clients compare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties of the object.</span></span> <span data-ttu-id="124b3-143">Das Vergleichen von Zeigern funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="124b3-143">Comparing pointers does not work.</span></span>

## <a name="requirements"></a><span data-ttu-id="124b3-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="124b3-144">Requirements</span></span>



| <span data-ttu-id="124b3-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="124b3-145">Requirement</span></span> | <span data-ttu-id="124b3-146">Wert</span><span class="sxs-lookup"><span data-stu-id="124b3-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="124b3-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="124b3-147">Minimum supported client</span></span><br/> | <span data-ttu-id="124b3-148">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="124b3-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="124b3-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="124b3-149">Minimum supported server</span></span><br/> | <span data-ttu-id="124b3-150">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="124b3-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="124b3-151">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="124b3-151">Redistributable</span></span><br/>          | <span data-ttu-id="124b3-152">Active Accessibility 1,3 RDK unter Windows NT 4,0 mit SP6 und höher und Windows 95</span><span class="sxs-lookup"><span data-stu-id="124b3-152">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>              |
| <span data-ttu-id="124b3-153">Header</span><span class="sxs-lookup"><span data-stu-id="124b3-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="124b3-154"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="124b3-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="124b3-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="124b3-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="124b3-156">Behandeln von WM- \_ GetObject</span><span class="sxs-lookup"><span data-stu-id="124b3-156">How to Handle WM\_GETOBJECT</span></span>](how-to-handle-wm-getobject.md)
</dt> <dt>

[<span data-ttu-id="124b3-157">Funktionsweise von WM- \_ GetObject</span><span class="sxs-lookup"><span data-stu-id="124b3-157">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
</dt> <dt>

[<span data-ttu-id="124b3-158">**Lresultfromobject.**</span><span class="sxs-lookup"><span data-stu-id="124b3-158">**LresultFromObject**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

