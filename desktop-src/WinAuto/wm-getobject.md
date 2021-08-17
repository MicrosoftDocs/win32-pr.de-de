---
title: WM_GETOBJECT (Winuser.h)
description: Wird sowohl von Microsoft Active Accessibility als auch von Microsoft Benutzeroberflächenautomatisierung, um Informationen zu einem barrierefreien Objekt zu erhalten, das in einer Serveranwendung enthalten ist.
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- WM_GETOBJECT-Nachricht Windows Barrierefreiheit
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
ms.openlocfilehash: 2767a689b87c2e293cb481647c61a29ad40167992e637802d1c0be63d18fc74e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744736"
---
# <a name="wm_getobject-message"></a>WM \_ GETOBJECT-Nachricht

Wird sowohl von Microsoft Active Accessibility als auch von Microsoft Benutzeroberflächenautomatisierung, um Informationen zu einem barrierefreien Objekt zu erhalten, das in einer Serveranwendung enthalten ist.

Anwendungen senden diese Nachricht nie direkt. Microsoft Active Accessibility sendet diese Nachricht als Reaktion auf Aufrufe von [**AccessibleObjectFromPoint,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)oder [**AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) Serveranwendungen verarbeiten diese Meldung jedoch. Benutzeroberflächenautomatisierung sendet diese Nachricht als Reaktion auf Aufrufe von [**IUIAutomation::ElementFromHandle,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle) [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)und [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)und bei der Behandlung von Ereignissen, für die ein Client registriert wurde.


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* 
</dt> <dd>

Stellt zusätzliche Informationen zur Meldung zur Verfügung und wird nur vom System verwendet. Server übergeben *dwFlags* beim Behandeln der Nachricht als *wParam-Parameter* im Aufruf von [**LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)

</dd> <dt>

*dwObjId* 
</dt> <dd>

Objektbezeichner. Dieser Wert ist eine der [Objektbezeichnerkonst](object-identifiers.md) constants oder ein benutzerdefinierter Objektbezeichner. Eine Serveranwendung muss diesen Wert überprüfen, um den Typ der angeforderten Informationen zu identifizieren. Bevor dieser Wert mit den OBJID-Werten verglichen wird, muss er vom Server in DWORD umgeformt werden. Andernfalls kann die Signierungserweiterung von \_ *lParam* bei 64-Bit-Windows den Vergleich beeinträchtigen. 

-   Wenn *dwObjId* einer der OBJID-Werte ist, z. B. \_ [**OBJID \_ CLIENT,**](object-identifiers.md)ist die Anforderung für ein Microsoft Active Accessibility-Objekt, das [**IAccessible implementiert.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
-   Wenn *dwObjId* gleich **UiaRootObjectId ist,** ist die Anforderung für einen Benutzeroberflächenautomatisierung. Wenn der Server einen Benutzeroberflächenautomatisierung, sollte er mithilfe der [**UiaReturnRawElementProvider-Funktion einen Anbieter**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) zurückgeben.
-   Wenn *dwObjId* [**OBJID \_ NATIVEOM ist,**](object-identifiers.md)ist die Anforderung für das zugrunde liegende Objektmodell des Steuerelements. Wenn das Steuerelement diese Anforderung unterstützt, sollte es eine entsprechende COM-Schnittstelle zurückgeben, indem die [**LresultFromObject-Funktion aufgerufen**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) wird.
-   Wenn *dwObjId* [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md)ist, ist die Anforderung, dass sich das Steuerelement als standardes Windows-Steuerelement oder als allgemeines Steuerelement identifiziert, das von der allgemeinen Steuerelementbibliothek (Common Control Library, ComCtrl.dll) implementiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn das Fenster oder Steuerelement nicht auf diese Nachricht reagieren muss, sollte es die Nachricht an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben. Andernfalls sollte das Fenster oder Steuerelement einen Wert zurückgeben, der der von *dwObjId* angegebenen Anforderung entspricht:

-   Wenn das Fenster oder Steuerelement Benutzeroberflächenautomatisierung implementiert, sollte das Fenster oder Steuerelement den Wert zurückgeben, der durch einen Aufruf der [**UiaReturnRawElementProvider-Funktion erhalten**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) wurde.
-   Wenn *dwObjId* [**OBJID \_ NATIVEOM**](object-identifiers.md) ist und das Fenster ein natives Objektmodell verfügbar macht, sollten die Fenster den Wert zurückgeben, der durch einen Aufruf der [**LresultFromObject-Funktion erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) wurde.
-   Wenn *dwObjId* [**OBJID \_ CLIENT**](object-identifiers.md) ist und das Fenster [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementiert, sollte das Fenster den Wert zurückgeben, der durch einen Aufruf der [**LresultFromObject-Funktion erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) wurde.

## <a name="remarks"></a>Hinweise

Wenn ein Client [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) oder eine der anderen **AccessibleObjectFrom**_X-Funktionen_ aufruft, die eine Schnittstelle zu einem Objekt abrufen, sendet Microsoft Active Accessibility die **WM \_ GETOBJECT-Nachricht** an die entsprechende Fensterprozedur in der entsprechenden Serveranwendung. Bei der **Verarbeitung von WM \_ GETOBJECT** rufen Serveranwendungen [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) auf und verwenden den Rückgabewert dieser Funktion als Rückgabewert für die Nachricht. Microsoft Active Accessibility führt in Verbindung mit der COM-Bibliothek das entsprechende Marshalling aus und übergibt den Schnittstellenzeiger vom Server zurück an den Client.

Server reagieren nicht auf **WM \_ GETOBJECT,** bevor das Objekt vollständig initialisiert wird oder nachdem es geschlossen wird. Wenn eine Anwendung ein neues Fenster erstellt, sendet das System [**EVENT \_ OBJECT \_ CREATE,**](event-constants.md) um Clients zu benachrichtigen, bevor die [WM \_ CREATE-Nachricht](../winmsg/wm-create.md) an die Fensterprozedur der Anwendung gesendet wird. Da viele Anwendungen WM CREATE verwenden, um ihren Initialisierungsprozess zu starten, antworten Server erst dann auf die \_ **WM \_ GETOBJECT-Nachricht,** wenn die Verarbeitung der **WM \_ CREATE-Nachricht abgeschlossen** ist.

Ein Server verwendet **WM \_ GETOBJECT,** um die folgenden Aufgaben auszuführen:

-   [Erstellen neuer barrierefreier Objekte](create-new-accessible-objects.md)
-   [Wiederverwenden vorhandener Zeiger auf Objekte](reuse-existing-pointers-to-objects.md)
-   [Erstellen neuer Schnittstellen für dasselbe Objekt](create-new-interfaces-to-the-same-object.md)

Für Clients bedeutet dies, dass sie abhängig von der Aktion des Servers möglicherweise unterschiedliche Schnittstellenzeker für dasselbe Benutzeroberflächenelement erhalten. Um zu bestimmen, ob zwei Schnittstellenzeker auf dasselbe Benutzeroberflächenelement zeigen, vergleichen Clients [**die IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des Objekts. Das Vergleichen von Zeigern funktioniert nicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Verteilbare Komponente<br/>          | Active Accessibility 1.3 RDK unter Windows NT 4.0 mit SP6 und höher und Windows 95<br/>              |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Behandeln von WM \_ GETOBJECT](how-to-handle-wm-getobject.md)
</dt> <dt>

[Funktionsweise von WM \_ GETOBJECT](how-wm-getobject-works.md)
</dt> <dt>

[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

