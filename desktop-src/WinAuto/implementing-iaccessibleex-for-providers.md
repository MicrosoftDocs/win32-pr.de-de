---
title: Implementieren von iaccessibleex für Anbieter
description: In diesem Abschnitt wird erläutert, wie Sie Microsoft Benutzeroberflächenautomatisierungs-Anbieter Funktionen zu einem Microsoft Active Accessibility Server hinzufügen, indem Sie die iaccessibleex-Schnittstelle
ms.assetid: c03dc552-7919-4a35-8ff2-4cdd822bc0b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9460ccbd243aef390b7ade0deb41626173c927a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338668"
---
# <a name="implementing-iaccessibleex-for-providers"></a>Implementieren von iaccessibleex für Anbieter

In diesem Abschnitt wird erläutert, wie Sie Microsoft Benutzeroberflächenautomatisierungs-Anbieter Funktionen zu einem Microsoft Active Accessibility Server hinzufügen, indem Sie die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle

Berücksichtigen Sie vor der Implementierung von [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)die folgenden Anforderungen:

-   Die grundlegende Microsoft Active Accessibility barrierefreie Objekthierarchie muss bereinigt werden. [**Iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) kann Probleme mit vorhandenen zugänglichen Objekt Hierarchien nicht beheben. Alle Probleme mit der Objektmodell Struktur müssen in der Microsoft Active Accessibility-Implementierung korrigiert werden, bevor **iaccessibleex** implementiert wird.
-   Die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierung muss sowohl der Microsoft Active Accessibility Spezifikation als auch der Benutzeroberflächenautomatisierungs-Spezifikation entsprechen. Tools sind verfügbar, um die Konformität unter beiden Spezifikationen zu überprüfen. Weitere Informationen finden Sie unter Test [Tools](testing-tools.md) und [UI Automation Verify (UIA Verify) Test Automation Framework](https://www.codeplex.com/UIAutomationVerify/).

Die Implementierung von [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) erfordert die folgenden Hauptschritte:

-   Implementieren Sie **IServiceProvider** für das barrierefreie Objekt, sodass die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle für dieses oder ein separates Objekt gefunden werden kann.
-   Implementieren Sie [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) für das barrierefreie Objekt.
-   Erstellen Sie barrierefreie Objekte für alle untergeordneten Elemente von Microsoft Active Accessibility, die in Microsoft Active Accessibility durch die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle für das übergeordnete Objekt (z. b. Listenelemente) repräsentiert werden. Implementieren Sie [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) für diese Objekte.
-   Implementieren Sie [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) für alle zugänglichen Objekte.
-   Implementieren Sie die entsprechenden Steuerelement Muster-Schnittstellen für die barrierefreien Objekte.

### <a name="implementing-the-iserviceprovider-interface"></a>Implementieren der IServiceProvider-Schnittstelle

Da sich die Implementierung von [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) für ein Steuerelement in einem separaten Objekt befinden kann, können Client Anwendungen nicht auf [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) zurückgreifen, um diese Schnittstelle zu erhalten. Stattdessen wird von Clients erwartet, dass **IServiceProvider:: QueryService** aufgerufen wird. In der folgenden Beispiel Implementierung dieser Methode wird davon ausgegangen, dass **iaccessibleex** nicht in einem separaten Objekt implementiert ist. Daher ruft die Methode einfach über **QueryInterface** auf.


```C++
           
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (ppvObject == NULL)
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
        return E_NOINTERFACE;
    }
};      
```



### <a name="implementing-the-iaccessibleex-interface"></a>Implementieren der iaccessibleex-Schnittstelle

In Microsoft Active Accessibility wird ein UI-Element immer durch eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle und eine untergeordnete ID identifiziert. Eine einzelne Instanz von **IAccessible** kann mehrere Benutzeroberflächen Elemente darstellen.

Da jede [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Instanz nur ein einzelnes UI-Element darstellt, muss jedes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -und untergeordnete ID-Paar einer einzelnen **iaccessibleex** -Instanz zugeordnet werden. **Iaccessibleex** enthält zwei Methoden, um diese Zuordnung zu behandeln:

-   [**Getobjectforchild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)– Ruft die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle für das angegebene untergeordnete Element ab. Diese Methode gibt **null** zurück, wenn die **iaccessibleex** -Implementierung die angegebene untergeordnete ID nicht erkennt, keine **iaccessibleex** für das angegebene untergeordnete Element aufweist oder ein untergeordnetes Element darstellt.
-   [**Getiaccessiblepair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)– Ruft die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle und die untergeordnete ID für das [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Element ab. Bei **IAccessible** -Implementierungen, die keine untergeordnete ID verwenden, ruft diese Methode das entsprechende Objekt mit **IAccessible** und childID \_ selbst ab.

Das folgende Beispiel zeigt die Implementierung der Methoden [**getobjectforchild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) und [**getiaccessiblepair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) für ein Element in einer benutzerdefinierten Listenansicht. Die-Methoden ermöglichen der Benutzeroberflächen Automatisierung, das [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -paar und das untergeordnete ID-Paar einer entsprechenden [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Instanz zuzuordnen.


```C++
           
HRESULT CListboxAccessibleObject::GetObjectForChild(
    long idChild, IAccessibleEx **ppRetVal)
{ 
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;
    HRESULT hr = ValidateChildId(vChild);
    if (FAILED(hr))
    {
        return E_INVALIDARG;
    }
    // List item accessible objects are stored as an array of
    // pointers; for the purpose of this example it is assumed that 
    // the list contents will not change. Accessible objects are
    // created only when needed.
    if (itemProviders[idChild - 1] == NULL)
    {
        // Create an object that supports UI Automation and
        // IAccessibleEx for the item.
        itemProviders[idChild - 1] = 
          new CListItemAccessibleObject(idChild, 
          g_pListboxControl);
        if (itemProviders[idChild - 1] == NULL)
        {
            return E_OUTOFMEMORY;
        }
    }
    IAccessibleEx* pAccEx = static_cast<IAccessibleEx*>
      (itemProviders[idChild - 1]);
    if (pAccEx != NULL)
    {
      pAccEx->AddRef();
    }
    *ppRetVal = pAccEx;
    return S_OK; 
}

HRESULT CListItemAccessibleObject::GetIAccessiblePair(
    IAccessible **ppAcc, long *pidChild)
{ 
    if (ppAcc == NULL || pidChild == NULL)
    {
        return E_INVALIDARG;   
    }

                CListboxAccessibleObject* pParent = 
        m_control->GetAccessibleObject();

    HRESULT hr = pParent->QueryInterface( 
        __uuidof(IAccessible), (void**)ppAcc);
    if (FAILED(hr))
    {
        *pidChild = 0;
        return E_NOINTERFACE;
    }
    *pidChild = m_childID; 
    return S_OK; 
}
}
```



Wenn eine barrierefreie Objekt Implementierung keine untergeordnete ID verwendet, können die Methoden dennoch implementiert werden, wie im folgenden Code Ausschnitt gezeigt.


```C++
           

    // This sample implements IAccessibleEx on the same object; it could use a tear-off
    // or inner object instead.
    class MyAccessibleImpl: public IAccessible,
                        public IAccessibleEx,
                        public IRawElementProviderSimple
    {
    public:
    ...
   HRESULT STDMETHODCALLTYPE GetObjectForChild( long idChild, IAccessibleEx **ppRetVal )
    {
        // This implementation does not support child IDs.
        *ppRetVal = NULL;
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE GetIAccessiblePair( IAccessible ** ppAcc, long * pidChild )
    {
        // This implementation assumes that IAccessibleEx is implemented on same object as
        // IAccessible.
        *ppAcc = static_cast<IAccessible *>(this);
        (*ppAcc)->AddRef();
        *pidChild = CHILDID_SELF;
        return S_OK;
    }
```



### <a name="implement-the-irawelementprovidersimple-interface"></a>Implementieren der IRawElementProviderSimple-Schnittstelle

Server verwenden " [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) ", um Informationen über Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Muster verfügbar zu machen **IRawElementProviderSimple** umfasst die folgenden Methoden:

-   [**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)– diese Methode wird verwendet, um Steuerelement Muster-Schnittstellen verfügbar zu machen. Es gibt ein Objekt zurück, das das angegebene Steuerelement Muster unterstützt, oder **null** , wenn das Steuerelement Muster nicht unterstützt wird.
-   [**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue)– diese Methode wird verwendet, um Eigenschaftswerte für die Benutzeroberflächen Automatisierung verfügbar zu machen.
-   " [**Hustrawelementprovider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)" – Diese Methode wird nicht mit [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierungen verwendet.
-   [**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions)– diese Methode wird nicht mit [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierungen verwendet.

Ein [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Server macht Steuerelement Muster durch Implementieren von [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)verfügbar. Diese Methode nimmt einen ganzzahligen Parameter an, der das-Steuerelement Muster angibt. Der Server gibt **null** zurück, wenn das Muster nicht unterstützt wird. Wenn die Steuerelement Muster Schnittstelle unterstützt wird, geben Server einen [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Wert zurück, und der Client ruft dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um das entsprechende Steuerelement Muster zu erhalten.

Ein [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Server kann Benutzeroberflächenautomatisierungs-Eigenschaften (z. b. LabeledBy und isrequirements dforform) unterstützen, indem er [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) implementiert und eine ganzzahlige PropertyId bereitstellt, die die Eigenschaft als Parameter identifiziert. Dieses Verfahren gilt nur für Benutzeroberflächenautomatisierungs-Eigenschaften, die nicht in einer Steuerelement Muster-Schnittstelle enthalten sind. Eigenschaften, die einer Steuerelement Muster Schnittstelle zugeordnet sind, werden über die Steuerelement Muster-Schnittstellen Methode verfügbar gemacht. Beispielsweise würde die issgewählt-Eigenschaft des [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Musters mit [**ISelectionItemProvider:: get \_ issgewählt**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)verfügbar gemacht werden.

 

 