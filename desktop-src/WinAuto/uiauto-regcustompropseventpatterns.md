---
title: Registrieren von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelement Mustern
description: Bevor eine benutzerdefinierte Eigenschaft, ein Ereignis oder ein Steuerelement Muster verwendet werden kann, müssen sowohl der Anbieter als auch der Client die Eigenschaft, das Ereignis oder das Steuerelement Muster zur Laufzeit registrieren.
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- Benutzeroberflächen Automatisierung, benutzerdefinierte Eigenschaften
- UI-Automatisierung, Übersicht über Ereignisse
- UI-Automatisierung, Übersicht über Steuerelement Muster
- Benutzeroberflächen Automatisierung, registrieren benutzerdefinierter Eigenschaften
- Benutzeroberflächen Automatisierung, Registrieren von Ereignissen
- Benutzeroberflächen Automatisierung, Registrieren von Steuerelement Mustern
- benutzerdefinierte Eigenschaften, registrieren
- Ereignisse, registrieren
- Steuerelement Muster, registrieren
- registrieren, benutzerdefinierte Eigenschaften
- registrieren, Ereignisse
- registrieren, Steuerelement Muster
- Steuerelement Muster, Benutzer definiert
- Steuerelement Muster, Implementieren von benutzerdefinierten
- Implementieren von benutzerdefinierten Steuerelement Mustern
- benutzerdefinierte Steuerelement Muster
- Client-Wrapper
- Muster Handler
- Implementieren von Muster Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b157e8f08a2c0be74af6b9f53d3578d1e4d03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039430"
---
# <a name="register-custom-properties-events-and-control-patterns"></a>Registrieren von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelement Mustern

Bevor eine benutzerdefinierte Eigenschaft, ein Ereignis oder ein Steuerelement Muster verwendet werden kann, müssen sowohl der Anbieter als auch der Client die Eigenschaft, das Ereignis oder das Steuerelement Muster zur Laufzeit registrieren. Die Registrierung wird global innerhalb eines Anwendungsprozesses wirksam und bleibt wirksam, bis der Prozess beendet oder das letzte Microsoft UI Automation-Element Objekt ([**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) oder [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) innerhalb des Prozesses freigegeben wird.

Die Registrierung umfasst die Übergabe einer GUID an die Benutzeroberflächen Automatisierung sowie ausführliche Informationen über die benutzerdefinierte Eigenschaft, das Ereignis oder das Steuerelement Muster. Der Versuch, dieselbe GUID ein zweites Mal mit denselben Informationen zu registrieren, ist erfolgreich, aber der Versuch, dieselbe GUID ein zweites Mal zu registrieren, aber mit unterschiedlichen Informationen (z. b. eine benutzerdefinierte Eigenschaft eines anderen Typs) schlägt fehl. Wenn die benutzerdefinierte Spezifikation in Zukunft akzeptiert und in den Benutzeroberflächenautomatisierungs-Kern integriert wird, werden die benutzerdefinierten Registrierungsinformationen von der Benutzeroberflächen Automatisierung überprüft und der bereits registrierte Code anstelle der "offiziellen" Frameworkimplementierung verwendet, wodurch Anwendungs Kompatibilitätsprobleme minimiert werden. Eigenschaften, Ereignisse oder Steuerelement Muster, die bereits registriert sind, können nicht entfernt werden.

Dieses Thema enthält folgende Abschnitte:

-   [Registrieren von benutzerdefinierten Eigenschaften und Ereignissen](#registering-custom-properties-and-events)
-   [Implementieren von benutzerdefinierten Steuerelement Mustern](#implementing-custom-control-patterns)
    -   [Der Client-Wrapper und der Muster Handler](#the-client-wrapper-and-the-pattern-handler)
    -   [Implementieren des Client Wrappers](#implementing-the-client-wrapper)
    -   [Implementieren des Muster Handlers](#implementing-the-pattern-handler)
    -   [Registrieren eines benutzerdefinierten Steuerelement Musters](#registering-a-custom-control-pattern)
    -   [Beispiel Implementierung eines benutzerdefinierten Steuerelement Musters](#example-implementation-of-a-custom-control-pattern)
-   [Zugehörige Themen](#related-topics)

## <a name="registering-custom-properties-and-events"></a>Registrieren von benutzerdefinierten Eigenschaften und Ereignissen

Wenn Sie eine benutzerdefinierte Eigenschaft oder ein Ereignis registrieren, können der Anbieter und der Client eine ID für die Eigenschaft oder das Ereignis abrufen, die dann an verschiedene API-Methoden weitergegeben werden kann, die IDs als Parameter annehmen.

So registrieren Sie eine Eigenschaft oder ein Ereignis:

1.  Definieren Sie eine GUID für die benutzerdefinierte Eigenschaft oder das Ereignis.
2.  Füllen Sie eine [**uiautomationpropertyinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) -oder [**uiautomationeventinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) -Struktur mit Informationen über die Eigenschaft oder das Ereignis aus, einschließlich der GUID und einer nicht lokalisierbaren Zeichenfolge, die den Namen der benutzerdefinierten Eigenschaft oder des Ereignisses enthält. Benutzerdefinierte Eigenschaften erfordern außerdem, dass der Datentyp der Eigenschaft angegeben wird, z. b. ob die Eigenschaft eine ganze Zahl oder eine Zeichenfolge enthält. Der Datentyp muss einer der folgenden Typen sein, die durch die [**uiautomationtype**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) -Enumeration angegeben werden. Für benutzerdefinierte Eigenschaften werden keine anderen Datentypen unterstützt.
    -   **Uiautomationtype \_ bool**
    -   **Uiautomationtype \_ Double**
    -   **Uiautomationtype- \_ Element**
    -   **Uiautomationtype \_ int**
    -   **Uiautomationtype- \_ Punkt**
    -   **Uiautomationtype- \_ Zeichenfolge**
3.  Verwenden Sie die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion, um eine Instanz des [**cuiautomationregistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) -Objekts zu erstellen und einen Zeiger auf die [**iuiautomationregistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) -Schnittstelle des Objekts abzurufen.
4.  Aufrufen der [**iuiautomationregistrar:: registerproperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) -Methode oder der [**registerevent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) -Methode und übergeben der Adresse der [**uiautomationpropertyinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) -Struktur oder der [**uiautomationeventinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) -Struktur.

Die [**iuiautomationregistrar:: registerproperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) -Methode oder die [**registerevent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) -Methode gibt eine eigen schafts-ID oder Ereignis-ID zurück, die von einer Anwendung an eine beliebige Benutzeroberflächenautomatisierungs-Methode übergeben werden kann. Beispielsweise können Sie eine registrierte eigen schafts-ID an die [**iuiautomationelement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) -Methode oder an die [**iuiautomation:: deatepropertycondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) -Methode übergeben.

Im folgenden Beispiel wird veranschaulicht, wie eine benutzerdefinierte Eigenschaft registriert wird.


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



Die von den Methoden [**iuiautomationregistrar:: registerproperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) und [**registerevent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) abgerufenen Eigenschaften-und Ereignis Bezeichner sind nur im Kontext der Anwendung gültig, von der Sie abgerufen werden, und nur für die Dauer der Anwendungs Lebensdauer. Die Registrierungsmethoden können andere ganzzahlige Werte für dieselbe GUID zurückgeben, wenn Sie über verschiedene Lauf Zeit Instanzen derselben Anwendung aufgerufen werden.

Es gibt keine Methode, die die Registrierung einer benutzerdefinierten Eigenschaft oder eines Ereignisses abhebt. Stattdessen wird die Registrierung implizit aufgehoben, wenn das letzte Benutzeroberflächenautomatisierungs-Objekt freigegeben wird.

> [!IMPORTANT]
> Wenn es sich bei dem Code um einen MSAA-Client (Microsoft Active Accessibility) handelt, müssen Sie die [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) -Funktion aufzurufen, wenn Sie den Wert einer benutzerdefinierten Eigenschaft ändern.

 

## <a name="implementing-custom-control-patterns"></a>Implementieren von benutzerdefinierten Steuerelement Mustern

Ein benutzerdefiniertes Steuerelement Muster ist nicht in der Benutzeroberflächenautomatisierungs-API enthalten, wird jedoch von einem Drittanbieter zur Laufzeit bereitgestellt. Entwickler von Client-und Anbieter Anwendungen müssen zusammenarbeiten, um ein benutzerdefiniertes Steuerelement Muster zu definieren, einschließlich der Methoden, Eigenschaften und Ereignisse, die vom Steuerelement Muster unterstützt werden. Nachdem Sie das-Steuerelement Muster definiert haben, müssen sowohl der Client als auch der Anbieter unterstützende Component Object Model (com)-Objekte zusammen mit Code implementieren, um das Steuerelement Muster zur Laufzeit zu registrieren. Ein benutzerdefiniertes Steuerelement Muster erfordert die Implementierung von zwei COM-Objekten: einen Client-Wrapper und einen Muster Handler.

> [!Note]  
> In den Beispielen in den folgenden Themen wird veranschaulicht, wie Sie ein benutzerdefiniertes Steuerelement Muster implementieren, das die Funktionalität des vorhandenen [value](uiauto-implementingvalue.md) -Steuerelement Musters dupliziert. Diese Beispiele sind nur für Lehrzwecke vorgesehen. Ein tatsächliches benutzerdefiniertes Steuerelement Muster sollte Funktionen bereitstellen, die nicht über die standardmäßigen Benutzeroberflächenautomatisierungs-Steuerelement Muster

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a>Der Client-Wrapper und der Muster Handler

Der Client Wrapper implementiert die API, die vom Client verwendet wird, um Eigenschaften abzurufen und Methoden aufzurufen, die durch das benutzerdefinierte Steuerelement Muster verfügbar gemacht werden. Die API wird als COM-Schnittstelle implementiert, die alle Eigenschafts Anforderungen und Methodenaufrufe an den Benutzeroberflächenautomatisierungs-Kern übergibt, der dann die Anforderungen und Aufrufe an den Anbieter marshallst.

Der Code, der ein benutzerdefiniertes Steuerelement Muster registriert, muss eine Klassenfactory bereitstellen, mit der die Benutzeroberflächen Automatisierung Instanzen des Client Wrapper Objekts erstellen kann. Wenn ein benutzerdefiniertes Steuerelement Muster erfolgreich registriert wird, gibt die Benutzeroberflächen Automatisierung einen [**iuiautomationpatterninstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) -Schnittstellen Zeiger zurück, der vom Client verwendet wird, um Eigenschaften Anforderungen und Methodenaufrufe an den Benutzeroberflächenautomatisierungs-Kern weiterzuleiten.

Auf der Anbieterseite nimmt der Benutzeroberflächenautomatisierungs-Kern die Eigenschaften Anforderungen und Methodenaufrufe vom Client an und übergibt sie an das musterhandlerobjekt. Der Muster Handler ruft dann die entsprechenden Methoden auf der Anbieter Schnittstelle für das benutzerdefinierte Steuerelement Muster auf.

Der Code, der ein benutzerdefiniertes Steuerelement Muster registriert, erstellt das musterhandlerobjekt und stellt beim Registrieren des Steuerelement Musters eine Benutzeroberflächen Automatisierung mit einem Zeiger auf die [**iuiautomationpatternhandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) -Schnittstelle des Objekts bereit.

Das folgende Diagramm zeigt, wie ein Client Eigenschafts Anforderungs-oder-Methodenaufrufe vom Client-Wrapper über die Benutzeroberflächenautomatisierungs-Kernkomponenten an den Muster Handler und dann an die Anbieter Schnittstelle fließt.

![Diagramm, das den Flow vom Client-Wrapper zum Muster Handler und-Anbieter anzeigt](images/custompatternsupport.jpg)

Die Objekte, die die Client Wrapper-und musterhandlerschnittstellen implementieren, müssen freigegeben sein. Außerdem muss der Benutzeroberflächenautomatisierungs-Kern in der Lage sein, die Objekte direkt ohne zwischenmarshallingcode aufzurufen.

### <a name="implementing-the-client-wrapper&quot;></a>Implementieren des Client Wrappers

Der Client Wrapper ist ein Objekt, das eine ixxxpattern-Schnittstelle verfügbar macht, mit der der Client Eigenschaften anfordert und Methoden aufruft, die vom benutzerdefinierten Steuerelement Muster unterstützt werden. Die Schnittstelle besteht aus einem Paar von &quot;Getter&quot;-Methoden für jede unterstützte Eigenschaft (&quot;get \_ currentxxx&quot; und &quot;get \_ cachedxxx Method") und einer "Caller"-Methode für jede unterstützte Methode. Wenn das Objekt instanziiert wird, empfängt der Objektkonstruktor einen Zeiger auf die [**iuiautomationpatterninstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) -Schnittstelle, die vom Benutzeroberflächenautomatisierungs-Kern implementiert wird. Die Methoden der ixxxpattern-Schnittstelle verwenden die [**iuiautomationpatterninstance:: GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) -Methode und die [**CALLMETHOD-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) , um Eigenschafts Anforderungen und Methodenaufrufe an den Benutzeroberflächenautomatisierungs-Kern weiterzuleiten.

Im folgenden Beispiel wird gezeigt, wie ein Client Wrapper Objekt für ein einfaches benutzerdefiniertes Steuerelement Muster implementiert wird, das eine einzelne Eigenschaft unterstützt. Ein komplexeres Beispiel finden Sie unter [Beispiel Implementierung eines benutzerdefinierten Steuerelement Musters](#example-implementation-of-a-custom-control-pattern).


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a>Implementieren des Muster Handlers

Der Muster Handler ist ein Objekt, das die [**iuiautomationpatternhandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) -Schnittstelle implementiert. Diese Schnittstelle verfügt über zwei Methoden: [**iuiautomationpatternhandler:: kreateclientwrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) und [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch). Die Methode " **kreateclientwrapper** " wird vom Benutzeroberflächenautomatisierungs-Kern aufgerufen und empfängt einen Zeiger auf die [**iuiautomationpatterninstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) -Schnittstelle. " **Anateclientwrapper** " antwortet, indem das Client Wrapper Objekt instanziiert und der **iuiautomationpatterninstance** -Schnittstellen Zeiger an den clientwrapper-Konstruktor übergeben wird.

Die [**dispatchmethode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) wird vom Benutzeroberflächenautomatisierungs-Kern verwendet, um Eigenschafts Anforderungen und Methodenaufrufe an die Anbieter Schnittstelle für das benutzerdefinierte Steuerelement Muster zu übergeben. Parameter enthalten einen Zeiger auf die Anbieter Schnittstelle, den NULL basierten Index des aufzurufenden Eigenschaften Getters oder der aufzurufenden Methode und ein Array von [**uiautomationparameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) -Strukturen, die die Parameter enthalten, die an den Anbieter übergeben werden. Der Muster Handler antwortet, indem er den Index-Parameter prüft, um zu bestimmen, welche Anbieter Methode aufgerufen werden soll. Anschließend ruft er die Anbieter Schnittstelle auf und übergibt die in den **uiautomationparameter** -Strukturen enthaltenen Parameter.

Das musterhandlerobjekt wird durch denselben Code instanziiert, der das benutzerdefinierte Steuerelement Muster registriert, bevor das Steuerelement Muster registriert wird. Der Code muss den [**iuiautomationpatternhandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) -Schnittstellen Zeiger des musterhandlerobjekts zum Zeitpunkt der Registrierung an den Benutzeroberflächenautomatisierungs-Kern übergeben.

Im folgenden Beispiel wird gezeigt, wie ein musterhandlerobjekt für ein einfaches benutzerdefiniertes Steuerelement Muster implementiert wird, das eine einzelne Eigenschaft unterstützt. Ein komplexeres Beispiel finden Sie unter [Beispiel Implementierung eines benutzerdefinierten Steuerelement Musters](#example-implementation-of-a-custom-control-pattern).


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a>Registrieren eines benutzerdefinierten Steuerelement Musters

Bevor Sie verwendet werden kann, muss ein benutzerdefiniertes Steuerelement Muster sowohl vom Anbieter als auch vom Client registriert werden. Die Registrierung stellt dem Benutzeroberflächenautomatisierungs-Kern ausführliche Informationen über das-Steuerelement Muster bereit und stellt dem Anbieter oder Client die Steuerelement Muster-ID und IDs für die Eigenschaften und Ereignisse bereit, die vom-Steuerelement Muster unterstützt werden. Auf der Anbieterseite muss das benutzerdefinierte Steuerelement Muster registriert werden, bevor das zugeordnete Steuerelement die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht oder zur gleichen Zeit behandelt.

Wenn Sie ein benutzerdefiniertes Steuerelement Muster registrieren, liefert der Anbieter oder Client die folgenden Informationen:

-   Der GUID des benutzerdefinierten Steuerelement Musters.
-   Eine nicht lokalisierbare Zeichenfolge, die den Namen des benutzerdefinierten Steuerelement Musters enthält.
-   Der GUID der Anbieter Schnittstelle, die das benutzerdefinierte Steuerelement Muster unterstützt.
-   Der GUID der Client Schnittstelle, die das benutzerdefinierte Steuerelement Muster unterstützt.
-   Ein Array von [**uiautomationpropertyinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) -Strukturen, die die Eigenschaften beschreiben, die vom benutzerdefinierten Steuerelement Muster unterstützt werden. Für jede Eigenschaft müssen die GUID, der Eigenschaftsname und der Datentyp angegeben werden.
-   Ein Array von [**uiautomationmethodinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) -Strukturen, die die Methoden beschreiben, die vom benutzerdefinierten Steuerelement Muster unterstützt werden. Für jede Methode enthält die-Struktur die folgenden Informationen: den Methodennamen, eine Anzahl von Parametern, eine Liste von Parameter Datentypen und eine Liste der Parameternamen.
-   Ein Array von [**uiautomationeventinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) -Strukturen, die die Ereignisse beschreiben, die vom benutzerdefinierten Steuerelement Muster ausgelöst werden. Für jedes Ereignis müssen die GUID und der Ereignis Name angegeben werden.
-   Die Adresse der [**iuiautomationpatternhandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) -Schnittstelle des musterhandlerobjekts, das das benutzerdefinierte Steuerelement Muster für Clients verfügbar macht.

Um das benutzerdefinierte Steuerelement Muster zu registrieren, muss der Anbieter oder Client Code die folgenden Schritte ausführen:

1.  Füllen Sie eine [**uiautomationpatterninfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) -Struktur mit den vorangehenden Informationen aus.
2.  Verwenden Sie die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion, um eine Instanz des [**cuiautomationregistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) -Objekts zu erstellen und einen Zeiger auf die [**iuiautomationregistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) -Schnittstelle des Objekts abzurufen.
3.  Aufrufen der [**iuiautomationregistrar:: registerpattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) -Methode, wobei die Adresse der [**uiautomationpatterninfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) -Struktur übergeben wird.

Die [**registerpattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) -Methode gibt eine Steuerelement Muster-ID zusammen mit einer Liste von Eigenschaften-IDs und Ereignis-IDs zurück. Eine Anwendung kann diese IDs an jede Benutzeroberflächen-Automatisierungs Methode übergeben, die einen solchen Bezeichner als Parameter annimmt. Beispielsweise können Sie eine registrierte Muster-ID an die [**iuiautomationelement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) -Methode übergeben, um einen Zeiger auf die Anbieter Schnittstelle für das Steuerelement Muster abzurufen.

Es gibt keine Methode, die die Registrierung eines benutzerdefinierten Steuerelement Musters abhebt. Stattdessen wird die Registrierung implizit aufgehoben, wenn das letzte Benutzeroberflächenautomatisierungs-Objekt freigegeben wird.

Ein Beispiel, das zeigt, wie ein benutzerdefiniertes Steuerelement Muster registriert wird, finden Sie im folgenden Abschnitt.

### <a name="example-implementation-of-a-custom-control-pattern"></a>Beispiel Implementierung eines benutzerdefinierten Steuerelement Musters

Dieser Abschnitt enthält Beispielcode, der veranschaulicht, wie die clientwrapper-und musterhandlerobjekte für ein benutzerdefiniertes Steuerelement Muster implementiert werden. Im Beispiel wird ein benutzerdefiniertes Steuerelement Muster implementiert, das auf dem [value](uiauto-implementingvalue.md) -Steuerelement Muster basiert.


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Entwerfen von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelement Mustern](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 