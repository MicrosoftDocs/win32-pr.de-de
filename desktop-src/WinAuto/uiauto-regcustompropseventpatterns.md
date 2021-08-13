---
title: Registrieren von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelementmustern
description: Bevor eine benutzerdefinierte Eigenschaft, ein Ereignis oder ein Steuerelementmuster verwendet werden kann, müssen sowohl der Anbieter als auch der Client die Eigenschaft, das Ereignis oder das Steuerelementmuster zur Laufzeit registrieren.
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- Benutzeroberflächenautomatisierung, benutzerdefinierte Eigenschaften
- übersicht über Benutzeroberflächenautomatisierung,Ereignisse
- Übersicht über Benutzeroberflächenautomatisierung,Steuerelementmuster
- Benutzeroberflächenautomatisierung,Registrieren benutzerdefinierter Eigenschaften
- Benutzeroberflächenautomatisierung,Registrieren von Ereignissen
- Benutzeroberflächenautomatisierung,Registrieren von Steuerelementmustern
- Benutzerdefinierte Eigenschaften,Registrieren
- Ereignisse,Registrieren
- Steuerelementmuster,Registrieren
- Registrieren, benutzerdefinierte Eigenschaften
- registering,events
- Registrieren, Steuern von Mustern
- Steuerelementmuster, benutzerdefiniert
- Steuerelementmuster,Implementieren von benutzerdefinierten
- Implementieren von benutzerdefinierten Steuerelementmustern
- Benutzerdefinierte Steuerelementmuster
- Clientwrapper
- Musterhandler
- Implementieren von Musterhandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7205d088f76f235b3078d5a053202f3d39b609389ef6adbc5dbdbca18d9b652b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564055"
---
# <a name="register-custom-properties-events-and-control-patterns"></a>Registrieren von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelementmustern

Bevor eine benutzerdefinierte Eigenschaft, ein Ereignis oder ein Steuerelementmuster verwendet werden kann, müssen sowohl der Anbieter als auch der Client die Eigenschaft, das Ereignis oder das Steuerelementmuster zur Laufzeit registrieren. Die Registrierung ist global innerhalb eines Anwendungsprozesses wirksam und bleibt wirksam, bis der Prozess geschlossen oder das letzte Microsoft Benutzeroberflächenautomatisierung-Elementobjekt ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) oder [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) innerhalb des Prozesses freigegeben wird.

Die Neugistation umfasst die Übergabe einer GUID an Benutzeroberflächenautomatisierung sowie ausführliche Informationen über die benutzerdefinierte Eigenschaft, das Ereignis oder das Steuerelementmuster. Der Versuch, die gleiche GUID ein zweites Mal mit denselben Informationen zu registrieren, ist erfolgreich, aber der Versuch, die gleiche GUID ein zweites Mal zu registrieren, aber mit anderen Informationen (z. B. einer benutzerdefinierten Eigenschaft eines anderen Typs), schlägt fehl. Wenn die benutzerdefinierte Spezifikation akzeptiert und in den Benutzeroberflächenautomatisierung Core integriert wird, werden Benutzeroberflächenautomatisierung in Zukunft die benutzerdefinierten Registrierungsinformationen überprüfen und den bereits registrierten Code anstelle der "offiziellen" Frameworkimplementierung verwenden, wodurch Anwendungskompatibilitätsprobleme minimiert werden. Eigenschaften, Ereignisse oder Steuerelementmuster, die bereits registriert sind, können nicht entfernt werden.

Dieses Thema enthält folgende Abschnitte:

-   [Registrieren von benutzerdefinierten Eigenschaften und Ereignissen](#registering-custom-properties-and-events)
-   [Implementieren von benutzerdefinierten Steuerelementmustern](#implementing-custom-control-patterns)
    -   [Der Clientwrapper und der Musterhandler](#the-client-wrapper-and-the-pattern-handler)
    -   [Implementieren des Clientwrappers](#implementing-the-client-wrapper)
    -   [Implementieren des Musterhandlers](#implementing-the-pattern-handler)
    -   [Registrieren eines benutzerdefinierten Steuerelementmusters](#registering-a-custom-control-pattern)
    -   [Beispielimplementierungen eines benutzerdefinierten Steuerelementmusters](#example-implementation-of-a-custom-control-pattern)
-   [Zugehörige Themen](#related-topics)

## <a name="registering-custom-properties-and-events"></a>Registrieren von benutzerdefinierten Eigenschaften und Ereignissen

Durch das Registrieren einer benutzerdefinierten Eigenschaft oder eines benutzerdefinierten Ereignisses können Anbieter und Client eine ID für die Eigenschaft oder das Ereignis abrufen, die dann an verschiedene API-Methoden übergeben werden kann, die IDs als Parameter verwenden.

So registrieren Sie eine Eigenschaft oder ein Ereignis:

1.  Definieren Sie eine GUID für die benutzerdefinierte Eigenschaft oder das ereignis.
2.  Füllen Sie eine [**UIAutomationPropertyInfo-**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) oder [**UIAutomationEventInfo-Struktur**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) mit Informationen über die Eigenschaft oder das Ereignis aus, einschließlich der GUID und einer nichtlokalisierbaren Zeichenfolge, die den Namen der benutzerdefinierten Eigenschaft oder des ereignisses enthält. Benutzerdefinierte Eigenschaften erfordern auch, dass der Datentyp der Eigenschaft angegeben wird, z. B. ob die Eigenschaft eine ganze Zahl oder eine Zeichenfolge enthält. Der Datentyp muss einer der folgenden Typen sein, der von der [**UIAutomationType-Enumeration**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) angegeben wird. Für benutzerdefinierte Eigenschaften werden keine anderen Datentypen unterstützt.
    -   **UIAutomationType \_ Bool**
    -   **UIAutomationType \_ Double**
    -   **\_UIAutomationType-Element**
    -   **UIAutomationType \_ Int**
    -   **\_UIAutomationType-Punkt**
    -   **\_UIAutomationType-Zeichenfolge**
3.  Verwenden Sie die [**CoCreateInstance-Funktion,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) um eine Instanz des [**CUIAutomationRegistrar-Objekts**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) zu erstellen und einen Zeiger auf die [**IUIAutomationRegistrar-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) des Objekts abzurufen.
4.  Rufen Sie die [**IUIAutomationRegistrar::RegisterProperty-**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) oder [**RegisterEvent-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) auf, und übergeben Sie die Adresse der [**UIAutomationPropertyInfo-Struktur**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) oder der [**UIAutomationEventInfo-Struktur.**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo)

Die [**IUIAutomationRegistrar::RegisterProperty-**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) oder [**RegisterEvent-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) gibt eine Eigenschaften-ID oder Ereignis-ID zurück, die eine Anwendung an jede Benutzeroberflächenautomatisierung Methode übergeben kann, die einen solchen Bezeichner als Parameter annimmt. Beispielsweise können Sie eine registrierte Eigenschaften-ID an die [**IUIAutomationElement::GetCurrentPropertyValue-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) oder an die [**IUIAutomation::CreatePropertyCondition-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) übergeben.

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



Die Eigenschaften- und Ereignisbezeichner, die von den Methoden [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) und [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) abgerufen werden, sind nur im Kontext der Anwendung gültig, die sie abruft, und nur für die Dauer der Lebensdauer der Anwendung. Die Registrierungsmethoden können verschiedene ganzzahlige Werte für dieselbe GUID zurückgeben, wenn sie über verschiedene Laufzeitinstanzen derselben Anwendung aufgerufen wird.

Es gibt keine Methode, die die Registrierung einer benutzerdefinierten Eigenschaft oder eines benutzerdefinierten Ereignisses auflädt. Stattdessen wird die Registrierung implizit aufgehoben, wenn das letzte Benutzeroberflächenautomatisierung-Objekt freigegeben wird.

> [!IMPORTANT]
> Wenn ihr Code ein MSAA-Client (Microsoft Active Accessibility) ist, müssen Sie die [**NotifyWinEvent-Funktion**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) aufrufen, wenn Sie den Wert einer benutzerdefinierten Eigenschaft ändern.

 

## <a name="implementing-custom-control-patterns"></a>Implementieren von benutzerdefinierten Steuerelementmustern

Ein benutzerdefiniertes Steuerelementmuster ist nicht in der Benutzeroberflächenautomatisierung-API enthalten, wird jedoch von einem Drittanbieter zur Laufzeit bereitgestellt. Entwickler von Client- und Anbieteranwendungen müssen zusammenarbeiten, um ein benutzerdefiniertes Steuerelementmuster zu definieren, einschließlich der Methoden, Eigenschaften und Ereignisse, die das Steuerelementmuster unterstützt. Nach dem Definieren des Steuerelementmusters müssen sowohl der Client als auch der Anbieter unterstützende Component Object Model -Objekte (COM) zusammen mit Code implementieren, um das Steuerelementmuster zur Laufzeit zu registrieren. Ein benutzerdefiniertes Steuerelementmuster erfordert die Implementierung von zwei COM-Objekten: einem Clientwrapper und einem Musterhandler.

> [!Note]  
> Die Beispiele in den folgenden Themen veranschaulichen, wie sie ein benutzerdefiniertes Steuerelementmuster implementieren, das die Funktionalität des vorhandenen [Value-Steuerelementmusters](uiauto-implementingvalue.md) dupliziert. Diese Beispiele dienen nur zu Anweisungszwecken. Ein tatsächliches benutzerdefiniertes Steuerelementmuster sollte Funktionen bereitstellen, die im Standard-Benutzeroberflächenautomatisierung Steuerelementmustern nicht verfügbar sind.

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a>Der Clientwrapper und der Musterhandler

Der Clientwrapper implementiert die API, die vom Client verwendet wird, um Eigenschaften abzurufen und Methoden aufzurufen, die vom benutzerdefinierten Steuerelementmuster verfügbar gemacht werden. Die API wird als COM-Schnittstelle implementiert, die alle Eigenschaftsanforderungen und Methodenaufrufe an den Benutzeroberflächenautomatisierung Core übergibt, der dann die Anforderungen und Aufrufe an den Anbieter marshallt.

Der Code, der ein benutzerdefiniertes Steuerelementmuster registriert, muss eine Klassenfactory bereitstellen, die Benutzeroberflächenautomatisierung verwenden können, um Instanzen des Clientwrapperobjekts zu erstellen. Wenn ein benutzerdefiniertes Steuerelementmuster erfolgreich registriert wurde, gibt Benutzeroberflächenautomatisierung einen [**IUIAutomationPatternInstance-Schnittstellenzeiger**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) zurück, der vom Client verwendet wird, um Eigenschaftsanforderungen und Methodenaufrufe an den Benutzeroberflächenautomatisierung Core weiterzuleiten.

Auf Anbieterseite übernimmt der Benutzeroberflächenautomatisierung Core die Eigenschaftsanforderungen und Methodenaufrufe vom Client und übergibt sie an das Musterhandlerobjekt. Der Musterhandler ruft dann die entsprechenden Methoden für die Anbieterschnittstelle für das benutzerdefinierte Steuerelementmuster auf.

Der Code, der ein benutzerdefiniertes Steuerelementmuster registriert, erstellt das Musterhandlerobjekt und stellt beim Registrieren des Steuerelementmusters Benutzeroberflächenautomatisierung mit einem Zeiger auf die [**IUIAutomationPatternHandler-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) des Objekts bereit.

Das folgende Diagramm zeigt, wie eine Clienteigenschaftsanforderung oder ein Methodenaufruf vom Clientwrapper über die Benutzeroberflächenautomatisierung Kernkomponenten zum Musterhandler und dann zur Anbieterschnittstelle fließt.

![Diagramm, das den Fluss vom Clientwrapper zum Musterhandler und Anbieter zeigt](images/custompatternsupport.jpg)

Die Objekte, die die Clientwrapper- und Musterhandlerschnittstellen implementieren, müssen free-threaded sein. Außerdem muss der Benutzeroberflächenautomatisierung Core in der Lage sein, die Objekte direkt ohne zwischengeschalteten Marshallingcode aufzurufen.

### <a name="implementing-the-client-wrapper"></a>Implementieren des Clientwrappers

Der Clientwrapper ist ein Objekt, das eine IXxxPattern-Schnittstelle verfügbar macht, die der Client verwendet, um Eigenschaften anzufordern und Methoden aufzurufen, die vom benutzerdefinierten Steuerelementmuster unterstützt werden. Die Schnittstelle besteht aus einem Paar von Gettermethoden für jede unterstützte Eigenschaft (get \_ CurrentXxx und get \_ CachedXxx-Methode) und einer "Aufrufer"-Methode für jede unterstützte Methode. Wenn das Objekt instanziiert wird, empfängt der Objektkonstruktor einen Zeiger auf die [**IUIAutomationPatternInstance-Schnittstelle,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) die vom Benutzeroberflächenautomatisierung Core implementiert wird. Die Methoden der IXxxPattern-Schnittstelle verwenden die Methoden [**IUIAutomationPatternInstance::GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) und [**CallMethod,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) um Eigenschaftsanforderungen und Methodenaufrufe an den Benutzeroberflächenautomatisierung Core weiterzuleiten.

Das folgende Beispiel zeigt, wie ein Clientwrapperobjekt für ein einfaches benutzerdefiniertes Steuerelementmuster implementiert wird, das eine einzelne Eigenschaft unterstützt. Ein komplexeres Beispiel finden Sie unter [Beispielimplementierungen eines benutzerdefinierten Steuerelementmusters.](#example-implementation-of-a-custom-control-pattern)


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



### <a name="implementing-the-pattern-handler"></a>Implementieren des Musterhandlers

Der Musterhandler ist ein Objekt, das die [**IUIAutomationPatternHandler-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) implementiert. Diese Schnittstelle verfügt über zwei Methoden: [**IUIAutomationPatternHandler::CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) und [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch). Die **CreateClientWrapper-Methode** wird vom Benutzeroberflächenautomatisierung Core aufgerufen und empfängt einen Zeiger auf die [**IUIAutomationPatternInstance-Schnittstelle.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) **CreateClientWrapper** antwortet, indem das Clientwrapperobjekt instanziiert und der **IUIAutomationPatternInstance-Schnittstellenzeiger** an den Clientwrapperkonstruktor übergeben wird.

Die [**Dispatch-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) wird vom Benutzeroberflächenautomatisierung Core verwendet, um Eigenschaftsanforderungen und Methodenaufrufe an die Anbieterschnittstelle für das benutzerdefinierte Steuerelementmuster zu übergeben. Parameter umfassen einen Zeiger auf die Anbieterschnittstelle, den nullbasierten Index des aufgerufenen Eigenschaften-Getters oder der aufgerufenen Methode und ein Array von [**UIAutomationParameter-Strukturen,**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) die die Parameter enthalten, die an den Anbieter übergeben werden sollen. Der Musterhandler antwortet, indem er den Indexparameter überprüft, um zu bestimmen, welche Anbietermethode aufgerufen werden soll, und ruft dann diese Anbieterschnittstelle auf, wobei die in den **UIAutomationParameter-Strukturen** enthaltenen Parameter übergeben werden.

Das Musterhandlerobjekt wird durch den gleichen Code instanziiert, der das benutzerdefinierte Steuerelementmuster registriert, bevor das Steuerelementmuster registriert wird. Der Code muss den [**IUIAutomationPatternHandler-Schnittstellenzeiger**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) des Musterhandlerobjekts zur Registrierungszeit an den Benutzeroberflächenautomatisierung Core übergeben.

Das folgende Beispiel zeigt, wie ein Musterhandlerobjekt für ein einfaches benutzerdefiniertes Steuerelementmuster implementiert wird, das eine einzelne Eigenschaft unterstützt. Ein komplexeres Beispiel finden Sie unter [Beispielimplementierungen eines benutzerdefinierten Steuerelementmusters.](#example-implementation-of-a-custom-control-pattern)


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



### <a name="registering-a-custom-control-pattern"></a>Registrieren eines benutzerdefinierten Steuerelementmusters

Bevor es verwendet werden kann, muss ein benutzerdefiniertes Steuerelementmuster sowohl vom Anbieter als auch vom Client registriert werden. Die Registrierung stellt den Benutzeroberflächenautomatisierung Core mit detaillierten Informationen zum Steuerelementmuster bereit und stellt dem Anbieter oder Client die Steuerelementmuster-ID sowie IDs für die Eigenschaften und Ereignisse bereit, die vom Steuerelementmuster unterstützt werden. Auf Anbieterseite muss das benutzerdefinierte Steuerelementmuster registriert werden, bevor das zugeordnete Steuerelement die [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) verarbeitet oder gleichzeitig.

Beim Registrieren eines benutzerdefinierten Steuerelementmusters stellt der Anbieter oder Client die folgenden Informationen bereit:

-   Die GUID des benutzerdefinierten Steuerelementmusters.
-   Eine nicht zuordnungsfähige Zeichenfolge, die den Namen des benutzerdefinierten Steuerelementmusters enthält.
-   Die GUID der Anbieterschnittstelle, die das benutzerdefinierte Steuerelementmuster unterstützt.
-   Die GUID der Clientschnittstelle, die das benutzerdefinierte Steuerelementmuster unterstützt.
-   Ein Array von [**UIAutomationPropertyInfo-Strukturen,**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) die die vom benutzerdefinierten Steuerelementmuster unterstützten Eigenschaften beschreiben. Für jede Eigenschaft müssen die GUID, der Eigenschaftenname und der Datentyp angegeben werden.
-   Ein Array von [**UIAutomationMethodInfo-Strukturen,**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) die die vom benutzerdefinierten Steuerelementmuster unterstützten Methoden beschreiben. Für jede Methode enthält die -Struktur die folgenden Informationen: den Methodennamen, die Anzahl der Parameter, eine Liste der Parameterdatentypen und eine Liste der Parameternamen.
-   Ein Array von [**UIAutomationEventInfo-Strukturen,**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) die die vom benutzerdefinierten Steuerelementmuster ausgelösten Ereignisse beschreiben. Für jedes Ereignis müssen die GUID und der Ereignisname angegeben werden.
-   Die Adresse der [**IUIAutomationPatternHandler-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) des Musterhandlerobjekts, das clients das benutzerdefinierte Steuerelementmuster zur Verfügung stellt.

Um das benutzerdefinierte Steuerelementmuster zu registrieren, muss der Anbieter- oder Clientcode die folgenden Schritte ausführen:

1.  Füllen Sie eine [**UIAutomationPatternInfo-Struktur**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) mit den vorherigen Informationen aus.
2.  Verwenden Sie die [**CoCreateInstance-Funktion,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) um eine Instanz des [**CUIAutomationRegistrar-Objekts**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) zu erstellen und einen Zeiger auf die [**IUIAutomationRegistrar-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) des Objekts abzurufen.
3.  Rufen Sie die [**IUIAutomationRegistrar::RegisterPattern-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) auf, und übergeben Sie dabei die Adresse der [**UIAutomationPatternInfo-Struktur.**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo)

Die [**RegisterPattern-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) gibt eine Steuerelementmuster-ID zusammen mit einer Liste von Eigenschaften-IDs und Ereignis-IDs zurück. Eine Anwendung kann diese IDs an jede Benutzeroberflächenautomatisierung Methode übergeben, die einen solchen Bezeichner als Parameter annimmt. Beispielsweise können Sie eine registrierte Muster-ID an die [**IUIAutomationElement::GetCurrentPattern-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) übergeben, um einen Zeiger auf die Anbieterschnittstelle für das Steuerelementmuster abzurufen.

Es gibt keine Methode, die die Registrierung eines benutzerdefinierten Steuerelementmusters auflädt. Stattdessen wird die Registrierung implizit aufgehoben, wenn das letzte Benutzeroberflächenautomatisierung-Objekt freigegeben wird.

Ein Beispiel, das zeigt, wie Sie ein benutzerdefiniertes Steuerelementmuster registrieren, finden Sie im folgenden Abschnitt.

### <a name="example-implementation-of-a-custom-control-pattern"></a>Beispielimplementierungen eines benutzerdefinierten Steuerelementmusters

Dieser Abschnitt enthält Beispielcode, der veranschaulicht, wie der Clientwrapper und Musterhandlerobjekte für ein benutzerdefiniertes Steuerelementmuster implementiert werden. Im Beispiel wird ein benutzerdefiniertes Steuerelementmuster implementiert, das auf dem [Wert-Steuerelementmuster](uiauto-implementingvalue.md) basiert.


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

**Konzeptionellen**
</dt> <dt>

[Entwerfen von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelementmustern](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 