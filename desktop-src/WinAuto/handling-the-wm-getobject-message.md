---
title: Behandeln der WM_GETOBJECT Nachricht
description: Sowohl Microsoft Active Accessibility als auch Microsoft Benutzeroberflächenautomatisierung WM GETOBJECT-Nachricht an einen Server oder eine Anbieteranwendung senden, um Informationen zu einem barrierefreien Objekt abzurufen, das vom Server oder \_ Anbieter unterstützt wird.
ms.assetid: 4b8e551f-aba7-4a89-8874-ba690175f525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732ebd21cc6d198040e5502554ce2a8cf1abb718c055bc9af9f88e0c5d123b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994190"
---
# <a name="handling-the-wm_getobject-message"></a>Behandeln der WM \_ GETOBJECT-Nachricht

Sowohl Microsoft Active Accessibility als auch Microsoft Benutzeroberflächenautomatisierung [**die \_ WM GETOBJECT-Nachricht**](wm-getobject.md) an einen Server oder eine Anbieteranwendung senden, um Informationen zu einem barrierefreien Objekt abzurufen, das vom Server oder Anbieter unterstützt wird. Clients senden **WM \_ GETOBJECT nie** direkt. Stattdessen sendet Microsoft Active Accessibility Nachricht, wenn ein Client die [**Funktionen AccessibleObjectFromPoint,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)und [**AccessibleObjectFromWindow aufruft.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) Benutzeroberflächenautomatisierung sendet **WM \_ GETOBJECT,** wenn ein Client [**IUIAutomation::ElementFromHandle,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle) [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)und [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)aufruft, und wenn Ereignisse behandelt werden, für die der Client registriert wurde.

Microsoft Active Accessibility oder Benutzeroberflächenautomatisierung gibt den Typ des Objekts an, für das Informationen  benötigt werden, indem ein Als Objektbezeichner bezeichneter Wert mit der [**WM \_ GETOBJECT-Nachricht übergeben**](wm-getobject.md) wird. Wenn die Nachricht empfangen wird, überprüft der Server oder Anbieter den Objektbezeichner, um zu bestimmen, wie auf die Nachricht reagiert werden soll. Die Antwort hängt davon ab, ob die empfangende Anwendung Microsoft Active Accessibility (server), Benutzeroberflächenautomatisierung (anbieter) oder keines von beiden für das angegebene Objekt implementiert.

-   Wenn die empfangende Anwendung ein Microsoft Active Accessibility-Server ist und die [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) den Objektbezeichner [**OBJID \_ CLIENT**](object-identifiers.md)enthält, sollte der Server den Wert zurückgeben, der durch Übergeben der [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des Objekts an die [**LresultFromObject-Funktion**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) ermittelt wurde.
-   Wenn die empfangende Anwendung einUI-Automatisierungsanbieter und der Objektbezeichner **UiaRootObjectId** ist, sollte der Anbieter die [**IRawElementProviderSimple-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) des Objekts zurückgeben. Der Anbieter ruft die Schnittstelle ab, indem er die [**UiaReturnRawElementProvider-Funktion**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) aufruft.
-   Wenn die empfangende Anwendung weder Microsoft Active Accessibility noch Benutzeroberflächenautomatisierung implementiert, sollte sie die [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben. Durch Übergeben der Nachricht kann das Barrierefreiheitsframework ermitteln, ob ein Proxy für das angegebene Objekt verfügbar ist.
-   Wenn der Objektbezeichner weder [**OBJID \_ CLIENT**](object-identifiers.md) noch UiaRootObjectId ist, sollte die empfangende Anwendung die [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben. Durch Übergeben der Nachricht kann das Barrierefreiheitsframework die Standardanbieter für Standardmäßige Benutzeroberflächenelemente verwenden.

Microsoft Active Accessibility und Benutzeroberflächenautomatisierung können benutzerdefinierte Objektbezeichner in einer [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) übergeben, um anwendungsdefinierte Werte oder Objekte von einem Server oder Anbieter abzurufen. Der [**OBJEKTbezeichner \_ OBJID NATIVEOM**](object-identifiers.md) oder [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) kann zum Abrufen einer nativen Objektmodellschnittstelle oder zum Anfordern eines bestimmten Proxyobjekts verwendet werden, das von Oleacc.dll.

Durch die Behandlung der [**Objektbezeichner OBJID \_ CLIENT**](object-identifiers.md) und **UiaRootObjectId** kann eine Microsoft Active Accessibility-Serverimplementierung zusammen mit einer implementierung des Benutzeroberflächenautomatisierung vorhanden sein. Da die Windows Standardsteuerelemente und allgemeinen Steuerelemente, die von der allgemeinen Steuerelementbibliothek (ComCtl32.dll) implementiert werden, weder Microsoft Active Accessibility noch Benutzeroberflächenautomatisierung implementieren, verarbeiten diese Steuerelemente in der Regel nicht die [**WM \_ GETOBJECT-Nachricht.**](wm-getobject.md) Stattdessen überprüft Microsoft Active Accessibility oder Benutzeroberflächenautomatisierungs-Framework, ob ein Proxyobjekt für ein bestimmtes Benutzeroberflächenelement verfügbar ist. Andernfalls wird das Standardproxyobjekt für das Hostfensterobjekt angegeben.

 

 