---
title: Implementieren eines Server-Side Benutzeroberflächenautomatisierung Anbieters
description: In diesem Thema wird beschrieben, wie Sie einen serverseitigen Microsoft Benutzeroberflächenautomatisierung-Anbieter für ein benutzerdefiniertes Steuerelement implementieren, das in C++ geschrieben ist.
ms.assetid: c3a919b2-8b8c-4dde-ad71-587f3845a9f5
keywords:
- Benutzeroberflächenautomatisierung,serverseitige Anbieterimplementierung
- Benutzeroberflächenautomatisierung,Anbieterimplementierung
- Benutzeroberflächenautomatisierung,implementierende serverseitige Anbieter
- Benutzeroberflächenautomatisierung,implementierende Anbieter
- serverseitige Anbieter, implementieren
- serverseitige Anbieter,Schnittstellen
- serverseitige Anbieter, Eigenschaftswerte
- serverseitige Anbieter,Ereignisse
- Serverseitige Anbieter, Zuweisen eines neuen übergeordneten Elements
- Ereignisse,serverseitige Anbieter
- Schnittstellen,serverseitige Anbieter
- providers,implementing
- Implementieren serverseitiger Anbieter
- Implementieren von Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 583b9a5f91bb8be53a3e8b0e356ce558978b8ea28d5b726b56f52420cd7bff37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413440"
---
# <a name="implement-a-server-side-ui-automation-provider"></a>Implementieren eines Server-Side Benutzeroberflächenautomatisierung Anbieters

In diesem Thema wird beschrieben, wie Sie einen serverseitigen Microsoft Benutzeroberflächenautomatisierung-Anbieter für ein benutzerdefiniertes Steuerelement implementieren, das in C++ geschrieben ist. Sie enthält die folgenden Abschnitte:

-   [Anbieterschnittstellen](#provider-interfaces)
-   [Erforderliche Funktionalität für Benutzeroberflächenautomatisierung Anbieter](#required-functionality-for-ui-automation-providers)
-   [Eigenschaftswerte](#property-values)
-   [Ereignisse von Anbietern](#events-from-providers)
-   [Anbieternavigation](#provider-navigation)
-   [Zuweisen eines neuen übergeordneten Elements](#assigning-a-new-parent)
-   [Neupositionierung des Anbieters](#provider-repositioning)
-   [Trennen von Anbietern](#disconnecting-providers)
-   [Zugehörige Themen](#related-topics)

Codebeispiele, die zeigen, wie serverseitige Anbieter implementiert werden, finden Sie unter [How-To Topics for Benutzeroberflächenautomatisierung Providers](uiauto-howto-topics-for-uiautomation-providers.md).

## <a name="provider-interfaces"></a>Anbieterschnittstellen

Die folgenden Component Object Model (COM) stellen Funktionen für benutzerdefinierte Steuerelemente bereit. Um grundlegende Funktionen bereitstellen zu können, muss Benutzeroberflächenautomatisierung Anbieter mindestens die [**IRawElementProviderSimple-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) implementieren. Die [**Schnittstellen IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) und [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) sind optional, sollten jedoch für Elemente in einem komplexen Steuerelement implementiert werden, um zusätzliche Funktionen zu bieten.



| Schnittstelle                                                                         | Beschreibung                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Irawelementprovidersimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)             | Stellt grundlegende Funktionen für ein steuerelement zur Verfügung, das in einem Fenster gehostet wird, einschließlich Unterstützung für Steuerelementmuster und -eigenschaften.                                                         |
| [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)         | Fügt Funktionen für ein Element in einem komplexen Steuerelement hinzu, einschließlich navigieren im Fragment, Festlegen des Fokus und Zurückgeben des umgebundenen Rechtecks des Elements.             |
| [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) | Fügt Funktionen für das Stammelement in einem komplexen Steuerelement hinzu, einschließlich Suchen eines untergeordneten Elements an angegebenen Koordinaten und Festlegen des Fokuszustands für das gesamte Steuerelement. |



 

> [!Note]  
> In der Benutzeroberflächenautomatisierung-API für verwalteten Code bilden diese Schnittstellen eine Vererbungshierarchie. Dies ist in C++ nicht der Fall, wenn die Schnittstellen vollständig getrennt sind.

 

Die folgenden Schnittstellen bieten zusätzliche Funktionalität, die Implementierung ist jedoch optional.



| Schnittstelle                                                                         | Beschreibung                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | Ermöglicht dem Anbieter, Anforderungen für Ereignisse zu verfolgen.                                      |
| [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) | Ermöglicht die Neupositionierung fensterbasierter Elemente in der Benutzeroberflächenautomatisierung struktur eines Fragments. |



 

## <a name="required-functionality-for-ui-automation-providers"></a>Erforderliche Funktionalität für Benutzeroberflächenautomatisierung Anbieter

Um mit Benutzeroberflächenautomatisierung kommunizieren zu können, muss Ihr Steuerelement die in der folgenden Tabelle beschriebenen Hauptfunktionen implementieren.



| Funktionalität                                              | Implementierung                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Machen Sie den Anbieter für Benutzeroberflächenautomatisierung.                      | Geben Sie als Reaktion auf eine [**WM \_ GETOBJECT-Nachricht,**](wm-getobject.md) die an das Steuerungsfenster gesendet wird, das Objekt zurück, das [**IRawElementProviderSimple implementiert.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) Für Fragmente muss dies der Anbieter für den Fragmentstamm sein.                                           |
| Geben Sie Eigenschaftswerte an.                                   | Implementieren [**Sie IRawElementProviderSimple::GetPropertyValue zum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) Bereitstellen oder Überschreiben von Werten.                                                                                                                                                             |
| Ermöglichen Sie es dem Client, mit dem Steuerelement zu interagieren.            | Implementieren Sie Schnittstellen, die jedes geeignete Steuerelementmuster unterstützen, z. B. [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider). Geben Sie diese Steuerelementmusteranbieter in Ihrer Implementierung von [**IRawElementProviderSimple::GetPatternProvider zurück.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) |
| Ereignisse werden aus dem Ereignis 2016-                                              | [**UiaRautomationAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent), Methoden von [**IProxyProviderWinEventSink**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iproxyproviderwineventsink).                                                                                                                                                |
| Aktivieren Sie das Navigieren und Konzentrieren in einem Fragment.              | Implementieren [**Sie IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) für jedes Element innerhalb des Fragments. Nicht erforderlich für Elemente, die nicht Teil eines Fragments sind.                                                                                                                         |
| Aktivieren Sie das Konzentrieren und Suchen untergeordneter Elemente in einem Fragment. | Implementieren [**Sie IRawElementProviderFragmentRoot.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) Nicht erforderlich für Elemente, die keine Fragmentswurzeln sind.                                                                                                                                                          |



 

## <a name="property-values"></a>Eigenschaftswerte

Benutzeroberflächenautomatisierung-Anbieter für benutzerdefinierte Steuerelemente müssen bestimmte Eigenschaften unterstützen, die von Benutzeroberflächenautomatisierung clientanwendungen verwendet werden können. Für Elemente, die in Fenstern gehostet werden, Benutzeroberflächenautomatisierung einige Eigenschaften vom Standardfensteranbieter abrufen, andere müssen jedoch vom benutzerdefinierten Anbieter abgerufen werden.

In der Regel müssen Anbieter für fensterbasierte Steuerelemente nicht die folgenden Eigenschaften bereitstellen, die durch **PROPERTYID identifiziert werden:**

-   [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ProcessIdPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ClassNamePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ HasKeyboardFocusPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsEnabledPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ RuntimeIdPropertyId**](uiauto-automation-element-propids.md)

Die RuntimeId-Eigenschaft eines einfachen Elements oder Fragmentstamms, der in einem Fenster gehostet wird, wird aus dem Fenster ermittelt. Fragmentelemente unterhalb des Stamms, z. B. Listenelemente in einem Listenfeld, müssen jedoch eigene Bezeichner bereitstellen. Weitere Informationen finden Sie unter [**IRawElementProviderFragment::GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid).

Die IsKeyboardFocusable-Eigenschaft sollte für Anbieter zurückgegeben werden, die in einem Windows Forms-Steuerelement gehostet werden. In diesem Fall ist der Standardfensteranbieter möglicherweise nicht in der Lage, den richtigen Wert abzurufen.

Die Name-Eigenschaft wird in der Regel vom Hostanbieter bereitgestellt.

## <a name="events-from-providers"></a>Ereignisse von Anbietern

Benutzeroberflächenautomatisierung-Anbieter sollten Ereignisse zur Benachrichtigung von Clientanwendungen über Änderungen im Zustand der Benutzeroberfläche erstellen. Die folgenden Funktionen werden zum Ausführen von Ereignissen verwendet.



| Funktion                                                                                   | Beschreibung                                                                                                              |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**UiaRautomationAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)                  | Löst verschiedene Ereignisse aus, einschließlich Ereignissen, die von Steuerelementmustern ausgelöst werden.                                                   |
| [**UiaRautomationPropertyChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent) | Löst ein -Ereignis aus, wenn Benutzeroberflächenautomatisierung geändert wurde.                                                               |
| [**UiaRiererStructureChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)      | Löst ein -Ereignis aus, wenn die Struktur der Benutzeroberflächenautomatisierung geändert wurde, z. B. durch Entfernen oder Hinzufügen eines Elements. |



 

Der Zweck eines Ereignisses besteht in der Benachrichtigung des Clients über etwas, das auf der Benutzeroberfläche stattfindet. Anbieter sollten ein Ereignis auslösen, unabhängig davon, ob die Änderung durch Benutzereingaben oder durch eine Clientanwendung ausgelöst wurde, die Benutzeroberflächenautomatisierung. Beispielsweise sollte das durch [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md) identifizierte Ereignis immer dann ausgelöst werden, wenn das Steuerelement aufgerufen wird, entweder über eine direkte Benutzereingabe oder durch die Clientanwendung, die [**IUIAutomationInvokePattern::Invoke aufruft.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke)

Zum Optimieren der Leistung kann ein Anbieter Ereignisse selektiv auslösen oder keine Ereignisse auslösen, wenn für deren Empfang keine Clientanwendung registriert ist. Die folgenden API-Elemente werden zur Optimierung verwendet.



| API-Element                                                                       | Beschreibung                                                                                                                                                       |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)           | Diese Funktion ermittelt, ob Clientanwendungen Benutzeroberflächenautomatisierung abonniert haben.                                                                 |
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | Durch die Implementierung dieser Schnittstelle auf einem Fragmentstamm kann der Anbieter darauf hingewiesen werden, wenn Clients Ereignishandler für Ereignisse im Fragment registrieren und deren Registrierung aufheben. |



 

> [!Note]  
> Ähnlich wie beim Implementieren der Verweiszählung in der COM-Programmierung ist es wichtig, dass Benutzeroberflächenautomatisierung-Anbieter die [**Methoden IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) und [**AdviseEventRemoved**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventremoved) wie die [**Methoden IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) und [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) der [**IUnknown-Schnittstelle**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) behandeln. Solange **AdviseEventAdded** für ein bestimmtes Ereignis oder eine bestimmte Eigenschaft mehrmals aufgerufen wurde als **AdviseEventRemoved,** sollte der Anbieter weiterhin entsprechende Ereignisse ausgelöst, da einige Clients noch lauschen. Alternativ können Benutzeroberflächenautomatisierung die [**UiaClientsAreListening-Funktion**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening) verwenden, um zu bestimmen, ob mindestens ein Client lauselt, und in diesem Fall alle entsprechenden Ereignisse ausgibt.

 

## <a name="provider-navigation"></a>Anbieternavigation

Anbieter für einfache Steuerelemente, z. B. eine benutzerdefinierte Schaltfläche, die in einem Fenster gehostet wird, müssen die Navigation in der Benutzeroberflächenautomatisierung unterstützen. Die Navigation zum und vom -Element wird vom Standardanbieter für das Hostfenster verarbeitet, der in der Implementierung von [**IRawElementProviderSimple::HostRawElementProvider angegeben ist.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider) Wenn Sie jedoch einen Anbieter für ein komplexes benutzerdefiniertes Steuerelement implementieren, müssen Sie die Navigation zwischen dem Stammknoten des Fragments und seinen Nachfolgern sowie zwischen nebengeordneten Knoten unterstützen.

> [!Note]  
> Elemente eines anderen Fragments als dem Stamm müssen **NULL** von [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)zurückgeben, da sie nicht direkt in einem Fenster gehostet werden und kein Standardanbieter die Navigation zu und von ihnen unterstützen kann.

 

Die Struktur des Fragments wird durch Ihre Implementierung von [**IRawElementProviderFragment::Navigate bestimmt.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) Diese Methode gibt für jedes Fragment und jede mögliche Richtung das Anbieterobjekt für das in dieser Richtung liegende Element zurück. Wenn kein Element in dieser Richtung vorkommt, gibt die Methode **NULL zurück.**

Der Fragmentstamm unterstützt nur die Navigation zu untergeordneten Elementen. Beispielsweise gibt ein Listenfeld das erste Element in der Liste zurück, wenn die Richtung **NavigateDirection \_ FirstChild** ist, und gibt das letzte Element zurück, wenn die Richtung **NavigateDirection \_ LastChild ist.** Der Fragmentstamm unterstützt keine Navigation zu einem übergeordneten Element oder zu gleichgeordneten Elemente. dies wird vom Hostfensteranbieter verarbeitet.

Die Nicht-Stammelemente eines Fragments müssen die Navigation zum übergeordneten Element sowie zu allen vorhandenen nebengeordneten und untergeordneten Elementen unterstützen.

## <a name="assigning-a-new-parent"></a>Zuweisen eines neuen übergeordneten Elements

Popupfenster sind eigentlich Fenster der obersten Ebene und werden standardmäßig in der Benutzeroberflächenautomatisierung als children des Desktops angezeigt. Eigentlich sind Popupfenster in vielen Fällen jedoch untergeordnete Elemente anderer Steuerelemente. Beispielsweise ist die Dropdownliste eines Kombinationsfelds logischerweise ein untergeordnetes Element des Kombinationsfelds. Dementsprechend ist ein Menüpopupfenster logischerweise ein untergeordnetes Element des Menüs. Benutzeroberflächenautomatisierung bietet Unterstützung für das Zuweisen eines neuen übergeordneten Elements zu einem Popupfenster, sodass es dem zugeordneten -Steuerelement als untergeordnetes Element erscheint.

So weisen Sie einem Popupfenster ein neues übergeordnetes Element zu:

1.  Erstellen Sie einen Anbieter für das Popupfenster. Dies erfordert, dass die Klasse des Popupfensters im Voraus bekannt ist.
2.  Implementieren Sie alle Eigenschaften und Steuerelementmuster wie gewohnt für dieses Popupfenster, als wäre es ein Steuerelement.
3.  Implementieren Sie die [**IRawElementProviderSimple::HostRawElementProvider-Eigenschaft,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider) sodass sie den wert zurückgibt, der von [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)erhalten wurde, wobei der Parameter das Fensterhand handle des Popupfensters ist.
4.  Implementieren [**Sie IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) für das Popupfenster und das übergeordnete Fenster, sodass die Navigation vom logischen übergeordneten Element zu den logischen untergeordneten Und zwischen gleichgeordneten übergeordneten Elemente ordnungsgemäß verarbeitet wird.

Wenn Benutzeroberflächenautomatisierung auf das Popupfenster trifft, erkennt es, dass die Navigation vom Standard überschrieben wird, und überspringt das Popupfenster, wenn es als untergeordnetes Fenster des Desktops erkannt wird. Stattdessen ist der Knoten nur über das Fragment erreichbar.

Das Zuweisen eines neuen übergeordneten Elements eignet sich nicht für Fälle, in denen ein Steuerelement ein Fenster einer beliebigen Klasse hosten kann. Beispielsweise kann ein Rebar-Steuerelement jede Art von Fenster in seinen Bänder hosten. Um diese Fälle zu behandeln, Benutzeroberflächenautomatisierung eine alternative Form der Fensterverlagerung unterstützt, wie im nächsten Abschnitt beschrieben.

## <a name="provider-repositioning"></a>Neupositionierung des Anbieters

Benutzeroberflächenautomatisierung Fragmente können zwei oder mehr Elemente enthalten, die jeweils in einem Fenster enthalten sind. Da jedes Fenster über einen eigenen Standardanbieter verfügt, der das Fenster als untergeordnetes Element eines enthaltenden Fensters betrachtet, zeigt die Benutzeroberflächenautomatisierung-Struktur die Fenster im Fragment standardmäßig als untergeordnete Fenster des übergeordneten Fensters an. In den meisten Fällen ist dies wünschenswert, kann aber manchmal zu Verwirrung führen, da es nicht mit der logischen Struktur der Benutzeroberfläche übereinstimmen kann.

Ein gutes Beispiel hierfür ist ein Grundleistensteuerelement. Ein Rebar-Steuerelement enthält Bänder, von denen jedes wiederum ein fensterbasiertes Steuerelement enthalten kann, z. B. eine Symbolleiste, ein Bearbeitungsfeld oder ein Kombinationsfeld. Der Standardfensteranbieter für das Leistenfenster sieht die Fenster des Bandsteuersteuerfensters als children, und der Rebar-Anbieter sieht die Bänder als children. Da der Fensteranbieter und der Rebar-Anbieter zusammen arbeiten und ihre kindergruppenbasierten Steuerelemente kombinieren, werden sowohl die Bänder als auch die fensterbasierten Steuerelemente als children des Steuerelements für die Leiste angezeigt. Logischerweise sollten jedoch nur die Bänder als children des Rebar-Steuerelements angezeigt werden, und jeder Bandanbieter sollte mit dem Standardfensteranbieter für das enthaltene Steuerelement gekoppelt werden.

Um dies zu erreichen, macht der Fragmentstammanbieter für das Rebar-Steuerelement eine Gruppe von unteren Bänder verfügbar, die die Bänder darstellen. Jedes Band verfügt über einen einzelnen Anbieter, der Eigenschaften und Steuerelementmuster verfügbar machen kann. In seiner Implementierung von [**IRawElementProviderSimple::HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)gibt der Bandanbieter den Standardfensteranbieter für das Steuerelementfenster zurück, den er durch Aufrufen von [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)erhält, und übergibt das Fensterhand handle (**HWND**) des Steuerelements. Schließlich implementiert der Fragmentstammanbieter für die Leiste die [**IRawElementProviderHwndOverride-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) und gibt in seiner Implementierung von [**IRawElementProviderHwndOverride::GetOverrideProviderForHwnd**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderhwndoverride-getoverrideproviderforhwnd)den entsprechenden Bandanbieter für das im angegebenen Fenster enthaltene Steuerelement zurück.

## <a name="disconnecting-providers"></a>Trennen von Anbietern

Anwendungen erstellen in der Regel Steuerelemente, wenn sie benötigt werden, und zerstören sie anschließend. Nach dem Zerstören eines Steuerelements sollten die Benutzeroberflächenautomatisierung, die dem Steuerelement zugeordnet sind, durch Aufrufen von [**UiaDisconnectProvider freigegeben werden.**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider)

Auf ähnliche Weise sollte eine Anwendung die [**UiaDisconnectAllProviders-Funktion**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders) verwenden, um alle Benutzeroberflächenautomatisierung-Ressourcen frei zu geben, die von allen Anbietern in der Anwendung vor dem Herunterfahren gehalten werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzeroberflächenautomatisierung-Anbieterprogrammiererhandbuch](uiauto-providerportal.md)
</dt> </dl>

 

 