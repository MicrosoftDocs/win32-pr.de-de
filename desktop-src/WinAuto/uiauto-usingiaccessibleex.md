---
title: Hinzufügen von Funktionen für die Benutzeroberflächen Automatisierung zu Active Accessibility Servern
description: Steuerelemente, die nicht über einen Microsoft-Benutzeroberflächenautomatisierungs-Anbieter verfügen, aber IAccessible implementieren, können problemlos aktualisiert werden, um einige Funktionen zur Automatisierung der Benutzeroberfläche bereitzustellen
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- Benutzeroberflächen Automatisierung, Active Accessibility Server
- Benutzeroberflächen Automatisierung, Microsoft Active Accessibility-Server
- Benutzeroberflächen Automatisierung, IAccessible
- UI-Automatisierung, iaccessibleex
- Benutzeroberflächen Automatisierung, verfügbar machen von iaccessibleex
- Benutzeroberflächen Automatisierung, Implementieren von iaccessibleex
- IAccessible
- IAccessibleEx
- Microsoft Active Accessibility
- Active Accessibility
- verfügbar machen von iaccessibleex
- Implementieren von iaccessibleex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45311deb8d3ec20fb8102285cddea1339373f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948797"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a>Hinzufügen von Funktionen für die Benutzeroberflächen Automatisierung zu Active Accessibility Servern

Steuerelemente, die nicht über einen Microsoft-Benutzeroberflächenautomatisierungs-Anbieter verfügen, aber [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementieren, können problemlos aktualisiert werden, um einige Funktionen zur [**Automatisierung der Benutzeroberfläche bereit**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) zustellen Diese Schnittstelle ermöglicht es dem Steuerelement, Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Muster verfügbar zu machen, ohne dass eine vollständige Implementierung von Schnittstellen für Benutzeroberflächenautomatisierungs-Anbieter wie [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) Zum Implementieren von **iaccessibleex** muss die grundlegende Microsoft Active Accessibility-Objekthierarchie keine Fehler oder Inkonsistenzen enthalten (z. b. ein untergeordnetes Objekt, dessen übergeordnetes Objekt Sie nicht als untergeordnetes Element aufführt) und kein Konflikt mit Benutzeroberflächenautomatisierungs-Spezifikationen Wenn die Microsoft Active Accessibility-Objekthierarchie diese Anforderungen erfüllt, ist Sie ein guter Kandidat für das Hinzufügen von Funktionen mithilfe von **iaccessibleex**. Andernfalls müssen Sie die Benutzeroberflächen Automatisierung allein oder zusammen mit der Microsoft Active Accessibility-Implementierung implementieren.

Nehmen Sie den Fall eines benutzerdefinierten Steuer Elements, das über einen Bereichs Wert verfügt. Der Microsoft Active Accessibility Server für das Steuerelement definiert seine Rolle und kann seinen aktuellen Wert zurückgeben. es fehlen jedoch die Möglichkeit, den minimalen und maximalen Wert des Steuer Elements zurückzugeben, da diese Eigenschaften nicht in Microsoft Active Accessibility definiert sind. Ein Benutzeroberflächenautomatisierungs-Client kann die Rolle, den aktuellen Wert und andere Eigenschaften von Microsoft Active Accessibility abrufen, da der Benutzeroberflächenautomatisierungs-Kern diese über [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)abrufen kann. Ohne Zugriff auf eine [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) -Schnittstelle für das Objekt kann die Benutzeroberflächen Automatisierung jedoch auch nicht die maximalen und minimalen Werte abrufen.

Der Steuerelement Entwickler könnte einen kompletten Benutzeroberflächenautomatisierungs-Anbieter für das Steuerelement bereitstellen. Dies würde jedoch bedeuten, dass ein Großteil der vorhandenen Funktionen der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung duplizieren würde, z. b. Navigation und allgemeine Eigenschaften. Stattdessen kann sich der Entwickler weiterhin auf **IAccessible** verlassen, um diese Funktionalität bereitzustellen, und gleichzeitig Unterstützung für Steuerelement spezifische Eigenschaften durch [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)hinzufügen.

Zum Aktualisieren des benutzerdefinierten Steuer Elements sind die folgenden Hauptschritte erforderlich:

-   Implementieren Sie [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) für das barrierefreie Objekt, sodass die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle für dieses oder ein separates Objekt gefunden werden kann.
-   Implementieren Sie [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) für das barrierefreie Objekt.
-   Erstellen Sie unterschiedliche barrierefreie Objekte für alle untergeordneten Elemente von Microsoft Active Accessibility, die in Microsoft Active Accessibility möglicherweise durch die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle für das übergeordnete Objekt (z. b. Listenelemente) repräsentiert wurden. Implementieren Sie [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) für diese Objekte.
-   Implementieren Sie [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) für alle zugänglichen Objekte.
-   Implementieren Sie die entsprechenden Steuerelement Muster-Schnittstellen für die barrierefreien Objekte.

Dieses Thema enthält folgende Abschnitte:

-   [Verfügbar machen von iaccessibleex](#exposing-iaccessibleex)
-   [Implementieren von iaccessibleex](#implementing-iaccessibleex)
-   [Zugehörige Themen](#related-topics)

## <a name="exposing-iaccessibleex"></a>Verfügbar machen von iaccessibleex

Da sich die Implementierung von [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) für ein Steuerelement in einem separaten Objekt befinden kann, können Client Anwendungen nicht auf [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) zurückgreifen, um diese Schnittstelle zu erhalten. Stattdessen wird von Clients erwartet, dass [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85))aufgerufen wird. In der folgenden Beispiel Implementierung dieser Methode wird davon ausgegangen, dass **iaccessibleex** nicht in einem separaten Objekt implementiert ist. Daher ruft die Methode einfach über **QueryInterface** auf.


```C++
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (!ppvObject)
    {
        return E_INVALIDARG;
    }
    *ppvObject = NULL;
    if (guidService == __uuidof(IAccessibleEx))
    {
        return QueryInterface(riid, ppvObject);
    }
    else 
    {
        return E_INVALIDARG;
    }
};
```



## <a name="implementing-iaccessibleex"></a>Implementieren von iaccessibleex

Die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Methode, die von Interesse ist, ist [**getobjectforchild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild). Diese Methode ermöglicht es dem Microsoft Active Accessibility-Server, ein Barrierefreies Objekt (eines, das mindestens **iaccessibleex** verfügbar macht) für ein untergeordnetes Element zu erstellen. In Microsoft Active Accessibility werden untergeordnete Elemente in der Regel nicht als barrierefreie Objekte, sondern als untergeordnete Elemente eines barrierefreien Objekts dargestellt. Da die Benutzeroberflächen Automatisierung jedoch erfordert, dass jedes Element durch ein separates Barrierefreies Objekt dargestellt wird, muss **getobjectforchild** bei Bedarf ein separates Objekt für jedes untergeordnete Objekt erstellen.

Die folgende Beispiel Implementierung gibt ein Barrierefreies Objekt für ein Element in einer benutzerdefinierten Listenansicht zurück.


```C++
HRESULT CListboxAccessibleObject::GetObjectForChild(long idChild, IAccessibleEx **pRetVal)
{ 
    *pRetVal = NULL;
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;

    // ValidateChildId is an application-defined function that checks whether
    // the child ID is valid. This is similar to code that validates the varChild
    // parameter in IAccessible methods.
    //
    // Additionally, if this idChild corresponds to a child that has its own
    // IAccessible, we should also return E_INVALIDARG here. (The caller
    // should instead be using the IAccessibleEx from that child's own
    // IAccessible in that case.)
    if (idChild == CHILDID_SELF || FAILED(ValidateChildId(vChild)))
    {
        return E_INVALIDARG;
    }

    // Return a suitable provider for this specific child.
    // This implementation returns a new instance each time; an implementation
    // can cache these if desired.

    // _pListboxControl is a member variable pointer to the owning control.
    IAccessibleEx* pAccEx  = new CListItemAccessibleObject(idChild, _pListboxControl);
    if (pAccEx == NULL)
    {
        return E_OUTOFMEMORY;
    }
    *pRetVal = pAccEx;
    return S_OK; 
}
```



Eine vollständige Beispiel Implementierung finden [Sie unter Erstellen von benutzerdefinierten Steuerelementen, Teil 5: Verwenden von iaccessibleex zum Hinzufügen von Benutzeroberflächenautomatisierungs-Unterstützung zu einem benutzerdefinierten Steuer](/previous-versions/msdn10/cc307850(v=msdn.10)) Element auf MSDN

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-providerportal.md)
</dt> </dl>

 

 