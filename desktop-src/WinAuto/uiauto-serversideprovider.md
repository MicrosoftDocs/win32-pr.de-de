---
title: Implementieren eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters
description: In diesem Thema wird beschrieben, wie ein serverseitiger Microsoft UI Automation-Anbieter für ein benutzerdefiniertes Steuerelement implementiert wird, das in C++ geschrieben ist
ms.assetid: c3a919b2-8b8c-4dde-ad71-587f3845a9f5
keywords:
- Benutzeroberflächen Automatisierung, serverseitige Anbieter Implementierung
- UI-Automatisierung, Anbieter Implementierung
- Benutzeroberflächen Automatisierung, implementieren serverseitiger Anbieter
- Benutzeroberflächen Automatisierung, Implementieren von Anbietern
- Serverseitige Anbieter, implementieren
- Serverseitige Anbieter, Schnittstellen
- Serverseitige Anbieter, Eigenschaftswerte
- Serverseitige Anbieter, Ereignisse
- Serverseitige Anbieter, Zuweisen eines neuen übergeordneten Elements
- Ereignisse, serverseitige Anbieter
- Schnittstellen, serverseitige Anbieter
- Anbieter, implementieren
- Implementieren serverseitiger Anbieter
- Implementieren von Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7fafbb9d03a25eb2e4713330c0622c25d17f9ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339290"
---
# <a name="implement-a-server-side-ui-automation-provider"></a>Implementieren eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters

In diesem Thema wird beschrieben, wie ein serverseitiger Microsoft UI Automation-Anbieter für ein benutzerdefiniertes Steuerelement implementiert wird, das in C++ geschrieben ist Sie enthält die folgenden Abschnitte:

-   [Anbieterschnittstellen](#provider-interfaces)
-   [Erforderliche Funktionalität für Benutzeroberflächenautomatisierungs-Anbieter](#required-functionality-for-ui-automation-providers)
-   [Eigenschaftswerte](#property-values)
-   [Ereignisse von Anbietern](#events-from-providers)
-   [Anbieter Navigation](#provider-navigation)
-   [Zuweisen eines neuen übergeordneten Elements](#assigning-a-new-parent)
-   [Neupositionierung des Anbieters](#provider-repositioning)
-   [Trennen der Verbindung von Anbietern](#disconnecting-providers)
-   [Zugehörige Themen](#related-topics)

Codebeispiele, die zeigen, wie serverseitige Anbieter implementiert werden, finden Sie unter Gewusst [-wie-Themen für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-howto-topics-for-uiautomation-providers.md).

## <a name="provider-interfaces"></a>Anbieterschnittstellen

Die folgenden Component Object Model (com)-Schnittstellen stellen Funktionalität für benutzerdefinierte Steuerelemente bereit. Zum Bereitstellen grundlegender Funktionen muss jeder Benutzeroberflächenautomatisierungs-Anbieter mindestens die [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle implementieren. Die-Schnittstellen " [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) " und " [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) " sind optional, sollten jedoch für Elemente in einem komplexen Steuerelement implementiert werden, um zusätzliche Funktionen bereitzustellen.



| Schnittstelle                                                                         | BESCHREIBUNG                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)             | Stellt grundlegende Funktionen für ein in einem Fenster gehostetes Steuerelement bereit, einschließlich der Unterstützung für Steuerelement Muster und Eigenschaften.                                                         |
| [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)         | Fügt Funktionen für ein Element in einem komplexen Steuerelement hinzu, einschließlich Navigation im Fragment, Festlegen des Fokus und Zurückgeben des umgebenden Rechtecks des Elements.             |
| [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) | Fügt Funktionen für das Stammelement in einem komplexen Steuerelement hinzu, einschließlich Suchen eines untergeordneten Elements an angegebenen Koordinaten und Festlegen des Fokuszustands für das gesamte Steuerelement. |



 

> [!Note]  
> In der Benutzeroberflächenautomatisierungs-API für verwalteten Code bilden diese Schnittstellen eine Vererbungs Hierarchie. Dies ist in C++ nicht der Fall, in dem die Schnittstellen vollständig voneinander getrennt sind.

 

Die folgenden Schnittstellen bieten zusätzliche Funktionen, aber die Implementierung ist optional.



| Schnittstelle                                                                         | BESCHREIBUNG                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Irawelementprovideradvil-Ereignisse**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | Ermöglicht dem Anbieter, Anforderungen für Ereignisse zu verfolgen.                                      |
| [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) | Ermöglicht das Neupositionieren von Fenster basierten Elementen in der Benutzeroberflächenautomatisierungs-Struktur eines Fragments. |



 

## <a name="required-functionality-for-ui-automation-providers"></a>Erforderliche Funktionalität für Benutzeroberflächenautomatisierungs-Anbieter

Um mit der Benutzeroberflächen Automatisierung zu kommunizieren, muss das Steuerelement die Hauptbereiche der Funktionalität implementieren, die in der folgenden Tabelle beschrieben werden.



| Funktionalität                                              | Implementierung                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Machen Sie den Anbieter für die Benutzeroberflächen Automatisierung verfügbar.                      | Geben Sie als Antwort auf eine an das Steuerelement Fenster gesendete [**WM- \_ GetObject**](wm-getobject.md) -Nachricht das Objekt zurück, das [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)implementiert. Für Fragmente muss dies der Anbieter für den Fragmentstamm sein.                                           |
| Geben Sie Eigenschaftswerte an.                                   | Implementieren Sie [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) , um Werte bereitzustellen oder zu überschreiben.                                                                                                                                                             |
| Ermöglicht es dem Client, mit dem Steuerelement zu interagieren.            | Implementieren Sie Schnittstellen, die jedes geeignete Steuerelement Muster unterstützen, z. b. [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider). Geben Sie diese Steuerelement Muster Anbieter in der Implementierung von [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)zurück. |
| Ereignisse aufwecken.                                              | [**Uiaraiseautomationevent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent), Methoden von [**iproxyproviderwineventsink**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iproxyproviderwineventsink).                                                                                                                                                |
| Aktivieren der Navigation und Fokussierung in einem Fragment              | Implementieren Sie [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) für jedes Element innerhalb des Fragments. Nicht erforderlich für Elemente, die nicht Teil eines Fragments sind.                                                                                                                         |
| Ermöglicht das Fokussieren und suchen untergeordneter Elemente in einem Fragment. | Implementieren Sie [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot). Nicht erforderlich für Elemente, die keine Fragmentstämme sind.                                                                                                                                                          |



 

## <a name="property-values"></a>Eigenschaftswerte

Benutzeroberflächenautomatisierungs-Anbieter für benutzerdefinierte Steuerelemente müssen bestimmte Eigenschaften unterstützen, die von der Benutzeroberflächen Automatisierung und Client Anwendungen verwendet werden können. Für Elemente, die in Windows gehostet werden, kann die Benutzeroberflächen Automatisierung einige Eigenschaften vom Standardfenster Anbieter abrufen, muss jedoch andere vom benutzerdefinierten Anbieter erhalten.

In der Regel müssen Anbieter für fensterbasierte Steuerelemente die folgenden Eigenschaften nicht bereitstellen, die durch **PropertyId** identifiziert werden:

-   [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)
-   [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)
-   [**UIA \_ processidpropertyid**](uiauto-automation-element-propids.md)
-   [**UIA \_ classnamepropertyid**](uiauto-automation-element-propids.md)
-   [**UIA \_ haskeyboardfocuspropertyid**](uiauto-automation-element-propids.md)
-   [**UIA \_ isenabledpropertyid**](uiauto-automation-element-propids.md)
-   [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)
-   [**UIA \_ ispasswordpropertyid**](uiauto-automation-element-propids.md)
-   [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)
-   [**UIA \_ runtimeidpropertyid**](uiauto-automation-element-propids.md)

Die runtimeId-Eigenschaft eines in einem Fenster gehosteten einfachen Elements oder fragmentstamms wird aus dem Fenster abgerufen. Fragmentelemente unterhalb des Stamms (z. b. Listenelemente in einem Listenfeld) müssen jedoch eigene Bezeichner bereitstellen. Weitere Informationen finden Sie unter [**IRawElementProviderFragment:: GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid).

Die iskeyboardfocverwendbare-Eigenschaft sollte für Anbieter zurückgegeben werden, die in einem Windows Forms Steuerelement gehostet werden. In diesem Fall ist der Standardfensteranbieter möglicherweise nicht in der Lage, den richtigen Wert abzurufen.

Die Name-Eigenschaft wird in der Regel vom Host Anbieter bereitgestellt.

## <a name="events-from-providers"></a>Ereignisse von Anbietern

Benutzeroberflächenautomatisierungs-Anbieter sollten Ereignisse ausgeben, um Client Anwendungen über Änderungen im Status der Benutzeroberfläche zu benachrichtigen. Die folgenden Funktionen werden verwendet, um Ereignisse zu erhöhen.



| Funktion                                                                                   | BESCHREIBUNG                                                                                                              |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**Uiaraiserautomationevent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)                  | Löst verschiedene Ereignisse aus, einschließlich Ereignissen, die von Steuerelementmustern ausgelöst werden.                                                   |
| [**Uiaraiminautomationpropertychangede Vent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent) | Löst ein Ereignis aus, wenn eine Benutzeroberflächenautomatisierungs-Eigenschaft geändert wurde.                                                               |
| [**Uiaraiminstructurechangede Vent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)      | Löst ein Ereignis aus, wenn sich die Struktur der Benutzeroberflächenautomatisierungs-Struktur geändert hat, z. b. durch Entfernen oder Hinzufügen eines Elements. |



 

Der Zweck eines Ereignisses besteht darin, den Client über etwas zu benachrichtigen, das in der Benutzeroberfläche stattfindet. Anbieter sollten ein Ereignis auslösen, unabhängig davon, ob die Änderung durch Benutzereingaben oder durch eine Client Anwendung mithilfe der Benutzeroberflächen Automatisierung ausgelöst wurde. Beispielsweise sollte das von [**UIA identifizierte Ereignis \_ \_ invokedeventid**](uiauto-event-ids.md) immer dann ausgelöst werden, wenn das-Steuerelement aufgerufen wird. Dies geschieht entweder über eine direkte Benutzereingabe oder durch die Client Anwendung, die [**iuiautomationinvokepattern::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke)Call aufruft.

Zum Optimieren der Leistung kann ein Anbieter Ereignisse selektiv auslösen oder keine Ereignisse auslösen, wenn für deren Empfang keine Clientanwendung registriert ist. Die folgenden API-Elemente werden zur Optimierung verwendet.



| API-Element                                                                       | BESCHREIBUNG                                                                                                                                                       |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Uiaclientsarelistening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)           | Diese Funktion bezieht sich darauf, ob Client Anwendungen Benutzeroberflächenautomatisierungs-Ereignisse abonniert haben.                                                                 |
| [**Irawelementprovideradvil-Ereignisse**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | Wenn Sie diese Schnittstelle in einem Fragmentstamm implementieren, kann der Anbieter darüber informiert werden, wenn die Registrierung von Ereignis Handlern für Ereignisse auf dem Fragment durch Clients registriert wird. |



 

> [!Note]  
> Ähnlich wie bei der Implementierung der Verweis Zählung bei der com-Programmierung ist es für Benutzeroberflächenautomatisierungs-Anbieter wichtig, die Methoden [**irawelementprovideradviseevents:: adviseeventadded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) und [**adviseeventremoved**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventremoved) wie die [**IUnknown:: adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) -und [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) -Methoden der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle zu behandeln. Solange **adviseeventadded** mehrmals als **adviseeventremoved** für ein bestimmtes Ereignis oder eine bestimmte Eigenschaft bezeichnet wurde, sollte der Anbieter weiterhin entsprechende Ereignisse aufrufen, da einige Clients weiterhin lauschen. Sie können auch Benutzeroberflächenautomatisierungs-Anbieter verwenden, um zu bestimmen, ob mindestens ein Client abhört und, wenn [**dies der Fall**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening) ist, alle entsprechenden Ereignisse auslöst.

 

## <a name="provider-navigation"></a>Anbieter Navigation

Anbieter für einfache Steuerelemente, wie z. b. eine benutzerdefinierte Schaltfläche, die in einem-Fenster gehostet wird, müssen die Navigation in der Benutzeroberflächenautomatisierungs-Struktur Die Navigation zum und vom Element wird vom Standardanbieter für das Host Fenster behandelt, das in der Implementierung von [**IRawElementProviderSimple:: HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)angegeben wird. Wenn Sie jedoch einen Anbieter für ein komplexes benutzerdefiniertes Steuerelement implementieren, müssen Sie die Navigation zwischen dem Stammknoten des Fragments und seinen Nachfolgern sowie zwischen nebengeordneten Knoten unterstützen.

> [!Note]  
> Elemente eines anderen Fragments als der Stamm müssen von [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider) **null** zurückgeben, da Sie nicht direkt in einem Fenster gehostet werden und kein Standardanbieter die Navigation zu und von Ihnen unterstützen kann.

 

Die Struktur des Fragments wird durch ihre Implementierung von [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)bestimmt. Diese Methode gibt für jedes Fragment und jede mögliche Richtung das Anbieterobjekt für das in dieser Richtung liegende Element zurück. Wenn kein Element in dieser Richtung vorhanden ist, gibt die Methode **null** zurück.

Der Fragmentstamm unterstützt nur die Navigation zu untergeordneten Elementen. Ein Listenfeld gibt z. b. das erste Element in der Liste zurück, wenn die Richtung " **navigatedirection \_ FirstChild**" ist, und gibt das letzte Element zurück, wenn die Richtung " **navigatedirection \_ LastChild**" lautet. Der Fragmentstamm unterstützt keine Navigation zu einem übergeordneten Element oder zu gleich geordneten Elementen. Dies wird vom Host Fenster Anbieter behandelt.

Die Nicht-Stammelemente eines Fragments müssen die Navigation zum übergeordneten Element sowie zu allen vorhandenen nebengeordneten und untergeordneten Elementen unterstützen.

## <a name="assigning-a-new-parent"></a>Zuweisen eines neuen übergeordneten Elements

Popup Fenster sind tatsächlich Fenster der obersten Ebene und werden in der Benutzeroberflächenautomatisierungs-Struktur standardmäßig als untergeordnete Elemente des Desktops angezeigt. Eigentlich sind Popupfenster in vielen Fällen jedoch untergeordnete Elemente anderer Steuerelemente. Beispielsweise ist die Dropdownliste eines Kombinationsfelds logischerweise ein untergeordnetes Element des Kombinationsfelds. Dementsprechend ist ein Menüpopupfenster logischerweise ein untergeordnetes Element des Menüs. Die Benutzeroberflächen Automatisierung bietet Unterstützung für das Zuweisen eines neuen übergeordneten Elements zu einem Popup Fenster, sodass es als untergeordnetes Element des zugeordneten Steuer Elements angezeigt wird.

So weisen Sie einem Popup Fenster ein neues übergeordnetes Element zu:

1.  Erstellen Sie einen Anbieter für das Popupfenster. Hierfür muss die Klasse des Popup Fensters im Voraus bekannt sein.
2.  Implementieren Sie alle Eigenschaften und Steuerelement Muster wie üblich für dieses Popup, als wäre es ein eigenes Steuerelement.
3.  Implementieren Sie die Eigenschaft " [**IRawElementProviderSimple:: Host Provider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider) ", sodass Sie den Wert zurückgibt, der von " [**uiahostproviderfromhwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)" abgerufen wurde, wobei der Parameter das Fenster Handle des Popup Fensters ist.
4.  Implementieren Sie [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) für das Popup Fenster und das übergeordnete Element, sodass die Navigation vom logischen übergeordneten Element zu den logischen untergeordneten Elementen und zwischen gleich geordneten untergeordneten Elementen ordnungsgemäß verarbeitet wird.

Wenn die Benutzeroberflächen Automatisierung das Popup Fenster findet, erkennt Sie, dass die Navigation standardmäßig überschrieben wird, und überspringt das Popup Fenster, wenn es als untergeordnetes Element des Desktops auftritt. Stattdessen ist der Knoten nur über das Fragment erreichbar.

Das Zuweisen eines neuen übergeordneten Elements eignet sich nicht für Fälle, in denen ein Steuerelement ein Fenster einer beliebigen Klasse hosten kann. Beispielsweise kann ein Grund leisten-Steuerelement beliebige Fenstertypen in seinen Bändern hosten. Um diese Fälle zu behandeln, unterstützt die Benutzeroberflächen Automatisierung eine alternative Form der Fenster Verlagerung, wie im nächsten Abschnitt beschrieben.

## <a name="provider-repositioning"></a>Neupositionierung des Anbieters

Benutzeroberflächenautomatisierungs-Fragmente enthalten möglicherweise zwei oder mehr Elemente, die jeweils in einem Fenster enthalten sind. Da jedes Fenster über einen eigenen Standardanbieter verfügt, der das Fenster als untergeordnetes Element eines enthaltenden Fensters ansieht, werden in der Benutzeroberflächenautomatisierungs-Struktur standardmäßig die Fenster im Fragment als untergeordnete Elemente des übergeordneten Fensters angezeigt. In den meisten Fällen ist dies wünschenswert, aber manchmal kann es zu Verwirrung führen, da es nicht der logischen Struktur der Benutzeroberfläche entspricht.

Ein gutes Beispiel hierfür ist ein Grundleistensteuerelement. Ein Grund leisten-Steuerelement enthält Bänder, von denen jedes wiederum ein Fenster basiertes Steuerelement enthalten kann, z. b. eine Symbolleiste, ein Eingabefeld oder ein Kombinations Feld. Der Standardfenster Anbieter für das Fenster "Info Leiste" sieht die Band Steuerungs Fenster als untergeordnete Elemente, und der Grund leisten Anbieter sieht die Bänder als untergeordnete Elemente. Da der Fenster Anbieter und der Grund leisten Anbieter zusammenarbeiten und ihre untergeordneten Elemente kombinieren, werden sowohl die Bänder als auch die Fenster basierten Steuerelemente als untergeordnete Elemente des Grund leisten-Steuer Elements angezeigt. Logisch, jedoch sollten nur die Bänder als untergeordnete Elemente des Grund leisten-Steuer Elements angezeigt werden, und jeder Band Anbieter sollte mit dem Standardfenster Anbieter für das enthaltene Steuerelement gekoppelt werden.

Um dies zu erreichen, macht der Fragment-Stamm Anbieter für das Grund leisten-Steuerelement einen Satz untergeordneter Elemente verfügbar, die die Bänder darstellen. Jedes Band verfügt über einen einzelnen Anbieter, der Eigenschaften und Steuerelement Muster verfügbar machen kann. In der Implementierung von [**IRawElementProviderSimple:: HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)gibt der Band Anbieter den Standardfenster Anbieter für das Steuerelement Fenster zurück, das er durch Aufrufen von " [**uiahostproviderfromhwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)" erhält und dabei den Fenster Handle (**HWND**) des Steuer Elements übergibt. Schließlich implementiert der fragmentstammpbieter für die Grund Leiste die [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) -Schnittstelle, und bei der Implementierung von [**IRawElementProviderHwndOverride:: GetOverrideProviderForHwnd**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderhwndoverride-getoverrideproviderforhwnd)wird der entsprechende Band Anbieter für das Steuerelement zurückgegeben, das im angegebenen Fenster enthalten ist.

## <a name="disconnecting-providers"></a>Trennen der Verbindung von Anbietern

Anwendungen erstellen in der Regel Steuerelemente, wenn Sie benötigt werden, und zerstören Sie anschließend. Nachdem ein Steuerelement zerstört wurde, sollten die dem Steuerelement zugeordneten Benutzeroberflächenautomatisierungs-Anbieter Ressourcen durch Aufrufen von [**uiadisconnectprovider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider)freigegeben werden.

Ebenso sollte eine Anwendung die [**uiadisconnectallproviders**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders) -Funktion verwenden, um alle Benutzeroberflächenautomatisierungs-Ressourcen freizugeben, die von allen Anbietern der Anwendung aufbewahrt werden, bevor Sie heruntergefahren werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-providerportal.md)
</dt> </dl>

 

 