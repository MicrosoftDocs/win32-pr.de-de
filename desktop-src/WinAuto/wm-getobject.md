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
# <a name="wm_getobject-message"></a>WM- \_ GetObject-Nachricht

Wird von Microsoft Active Accessibility und Microsoft UI Automation gesendet, um Informationen über ein Barrierefreies Objekt zu erhalten, das in einer Serveranwendung enthalten ist.

Anwendungen senden diese Nachricht niemals direkt. Microsoft Active Accessibility sendet diese Nachricht als Antwort auf Aufrufe von [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)oder [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow). Diese Nachricht wird jedoch von Server Anwendungen verarbeitet. Die Benutzeroberflächenautomatisierung sendet diese Nachricht als Antwort auf Aufrufe von [**iuiautomation:: elementfromhandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**elementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)und [**getfocucements**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)sowie bei der Behandlung von Ereignissen, die von einem Client registriert wurden.


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* 
</dt> <dd>

Stellt zusätzliche Informationen über die Meldung bereit und wird nur vom System verwendet. Server übergeben *dwFlags* als *wParam* -Parameter beim Aufrufen von [**lresultfrowbject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) bei der Verarbeitung der Nachricht.

</dd> <dt>

*dwobjid* 
</dt> <dd>

Objekt Bezeichner. Dieser Wert ist eine der [objektbezeichnerkonstanten](object-identifiers.md) oder ein benutzerdefinierter Objekt Bezeichner. Eine Serveranwendung muss diesen Wert überprüfen, um den Typ der angeforderten Informationen zu ermitteln. Bevor Sie diesen Wert mit den objID \_ -Werten vergleichen, muss der Server ihn in **DWORD** umwandeln. andernfalls kann die Signierungs Erweiterung des *LPARAM* -Element mit dem Vergleich in 64-Bit-Fenstern beeinträchtigt werden.

-   Wenn *dwobjid* einer der ObjID- \_ Werte ist, z. b. [**objID- \_ Client**](object-identifiers.md), ist die Anforderung für ein Microsoft Active Accessibility Objekt, das [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementiert.
-   Wenn *dwobjid* gleich **uiarootobjectid** ist, ist die Anforderung ein Benutzeroberflächenautomatisierungs-Anbieter. Wenn der Server die Benutzeroberflächen Automatisierung implementiert, sollte er mithilfe der [**uiareturnrawelementprovider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) -Funktion einen Anbieter zurückgeben.
-   Wenn *dwobjid* " [**objID \_ nativeom**](object-identifiers.md)" ist, ist die Anforderung für das zugrunde liegende Objektmodell des Steuer Elements. Wenn das Steuerelement diese Anforderung unterstützt, sollte es eine entsprechende COM-Schnittstelle zurückgeben, indem Sie die [**lresultfrobobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) -Funktion aufrufen.
-   Wenn *dwobjid* " [**objID \_ queryclassnameidx**](object-identifiers.md)" ist, ist die Anforderung, dass sich das Steuerelement selbst als standardmäßiges Windows-Steuerelement oder ein gängiges Steuerelement identifiziert, das von der allgemeinen Steuerelement Bibliothek (ComCtrl.dll) implementiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn das Fenster oder das Steuerelement nicht auf diese Meldung reagieren muss, sollte die Nachricht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben werden. Andernfalls sollte das Fenster oder Steuerelement einen Wert zurückgeben, der der von *dwobjid* angegebenen Anforderung entspricht:

-   Wenn das Fenster oder das Steuerelement die Benutzeroberflächen Automatisierung implementiert, sollte das Fenster oder Steuerelement den Wert zurückgeben, der durch einen Aufrufder [**uiareturnrawelementprovider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) -Funktion abgerufen wird.
-   Wenn *dwobjid* auf [**objID \_ nativeom**](object-identifiers.md) festgelegt ist und das Fenster ein System eigenes Objektmodell verfügbar macht, sollte das Fenster den Wert zurückgeben, der durch einen Aufrufe der [**lresultfrofubject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) -Funktion abgerufen wird.
-   Wenn *dwobjid* ein [**objID- \_ Client**](object-identifiers.md) ist und das Fenster [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementiert, sollte das Fenster den Wert zurückgeben, der durch einen Aufruf der [**lresultfrofubject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) -Funktion abgerufen wird.

## <a name="remarks"></a>Bemerkungen

Wenn ein Client [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) oder eine der anderen **accessibleobjectfrom**_X_ -Funktionen aufruft, die eine Schnittstelle zu einem Objekt abrufen, sendet Microsoft Active Accessibility die **WM- \_ GetObject** -Nachricht an die entsprechende Fenster Prozedur innerhalb der entsprechenden Serveranwendung. Beim Verarbeiten von **WM \_ GetObject** wird von Server Anwendungen [**lresultfrobugbject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) aufgerufen und der Rückgabewert dieser Funktion als Rückgabewert für die Nachricht verwendet. Microsoft Active Accessibility führt in Verbindung mit der com-Bibliothek das entsprechende Marshalling durch und übergibt den Schnittstellen Zeiger vom Server an den Client zurück.

Server Antworten nicht auf das **WM- \_ GetObject** -Objekt, bevor das Objekt vollständig initialisiert wurde, oder nachdem es begonnen hat, zu schließen. Wenn eine Anwendung ein neues Fenster erstellt, sendet das System das [**Ereignis \_ Objekt \_ Create**](event-constants.md) zum Benachrichtigen von Clients, bevor es die [WM \_ Create](../winmsg/wm-create.md) -Meldung an die Fenster Prozedur der Anwendung sendet. Da viele Anwendungen WM Create verwenden, \_ um den Initialisierungs Prozess zu starten, reagieren Server erst dann auf die **WM- \_ GetObject** -Nachricht, wenn die Verarbeitung der **WM \_ Create** -Nachricht abgeschlossen ist.

Ein Server verwendet **WM \_ GetObject** , um die folgenden Aufgaben auszuführen:

-   [Neue barrierefreie Objekte erstellen](create-new-accessible-objects.md)
-   [Wieder verwenden vorhandener Zeiger auf Objekte](reuse-existing-pointers-to-objects.md)
-   [Erstellen neuer Schnittstellen für dasselbe Objekt](create-new-interfaces-to-the-same-object.md)

Für Clients bedeutet dies, dass Sie abhängig von der Aktion des Servers möglicherweise unterschiedliche Schnittstellen Zeiger für dasselbe Benutzeroberflächen Element erhalten. Um zu ermitteln, ob zwei Schnittstellen Zeiger auf dasselbe Benutzeroberflächen Element zeigen, vergleichen Clients die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften des Objekts. Das Vergleichen von Zeigern funktioniert nicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Verteilbare Komponente<br/>          | Active Accessibility 1,3 RDK unter Windows NT 4,0 mit SP6 und höher und Windows 95<br/>              |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Behandeln von WM- \_ GetObject](how-to-handle-wm-getobject.md)
</dt> <dt>

[Funktionsweise von WM- \_ GetObject](how-wm-getobject-works.md)
</dt> <dt>

[**Lresultfromobject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

