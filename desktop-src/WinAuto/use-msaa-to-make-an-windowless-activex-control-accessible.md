---
title: Verwenden von MSAA, um den Zugriff auf ein fensterloses ActiveX zu ermöglichen
description: Beschreibt die Verwendung des Microsoft Active Accessibility \ 32; API, um sicherzustellen, dass Ihr fensterloses Microsoft ActiveX-Steuerelement für HILFSTECHNOLOGIE-Clientanwendungen (AT) zugänglich ist.
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- ActiveX Steuerelement, Barrierefreiheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bac5c4d2a27e5f069f2242999438eebe85e2ea7df1a6bc94890aec142db246c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098110"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a>Verwenden von MSAA, um den Zugriff auf ein fensterloses ActiveX zu ermöglichen

Beschreibt die Verwendung der Microsoft Active Accessibility-API, um sicherzustellen, dass ihr fensterloses Microsoft ActiveX-Steuerelement für HILFSTECHNOLOGIE-Clientanwendungen (AT) zugänglich ist.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [ActiveX-Steuerelemente](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Microsoft Win32- und Component Object Model-Programmierung (COM)
-   Fensterlose ActiveX Steuerelemente
-   Microsoft Active Accessibility Server

## <a name="instructions"></a>Anweisungen

### <a name="step-1-implement-the-iaccessible-interface"></a>Schritt 1: Implementieren sie die IAccessible-Schnittstelle.

Um das fensterlose ActiveX-Steuerelement zugänglich zu machen, müssen Sie die Microsoft Active Accessibility [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) wie bei einem fensterbasierten Steuerelement implementieren, außer wie in den folgenden Schritten beschrieben. Weitere Informationen zum Implementieren von **IAccessible finden** Sie im [Entwicklerhandbuch für Active Accessibility Server.](developer-s-guide-for-active-accessibility-servers.md)

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Schritt 2: Implementieren sie die IServiceProvider-Schnittstelle.

Wenn ein Client Barrierefreiheitsinformationen zu Ihrem fensterlosen Steuerelement anfragt, ruft der Container die [**IServiceProvider::QueryService-Methode**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) Ihres Steuerelements auf, um den [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) abzurufen.

Dieses Beispiel zeigt, wie die [**QueryService-Methode implementiert**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) wird.


```C++
STDMETHODIMP CMyAccessibleMSAAControl::QueryService(REFGUID guidService, 
        REFIID riid, void **ppvObject)
{      
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL;  

    if (guidService == __uuidof(IAccessible))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a>Schritt 3: Delegieren Sie IAccessible::get accParent-Methodenaufrufe an die \_ IAccessibleWindowlessSite::GetParentAccessible-Methode der Steuerungswebsite.

Wenn ein Client das übergeordnete Objekt Ihres fensterlosen Steuerelements an fordert, ruft der Container die [**IAccessible::get \_ accParent-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) Ihres Steuerelements auf. Ihre **get \_ accParent-Implementierung** sollte an die [**IAccessibleWindowlessSite::GetParentAccessible-Methode**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) des Containers delegieren.

Dieses Beispiel zeigt, wie die [**get \_ accParent-Methode implementiert**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) wird.


```C++
HRESULT CMyAccessibleMSAAControl::get_accParent(IDispatch **ppdispParent)  
{  
    if (ppdispParent == NULL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_FALSE;  
    *ppdispParent = NULL;  

    IAccessibleWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        IAccessible *pParentAcc = NULL;
        if (SUCCEEDED(pWindowlessSite->GetParentAccessible(&pParentAcc)))
        {
            hr = pParentAcc->QueryInterface(IID_PPV_ARGS(ppdispParent));  
        }
    }  

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a>Schritt 4: Beziehen Sie einen Bereich von Objekt-IDs, die den Ereignisquellen in Ihrem fensterlosen Steuerelement zugewiesen werden.

Wie fensterbasierte Steuerelemente ruft ein fensterloses ActiveX die [**NotifyWinEvent-Funktion**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) auf, um Clients über wichtige Ereignisse zu benachrichtigen. Die Funktionsparameter enthalten die Objekt-ID des Elements, das das Ereignis auswertet. Ihr fensterloses Steuerelement muss Objekt-IDs mithilfe eines Werts aus einem Bereich zuweisen, der durch Aufrufen der [**IAccessibleWindowlessSite::AcquireObjectIdRange-Methode**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) der Steuerelementwebsite erworben wurde.

In diesem Beispiel wird gezeigt, wie sie einen Bereich von Objekt-ID-Werten aus dem Steuerelementcontainer erhalten.


```C++
IAccessibleWindowlessSite *pWindowlessSite = NULL;

if (SUCCEEDED(m_pClientSite->QueryInterface(
        IID_PPV_ARGS(&pWindowlessSite))))  
{  
    if (FAILED(pWindowlessSite->AcquireObjectIdRange(100, this, 
            &m_idObjectBase)))  
    {  
        m_idObjectBase = -1;  
    } 
}

SafeRelease(&pWindowlessSite);
```



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a>Schritt 5: Implementieren sie die IAccessibleHandler-Schnittstelle.

Wenn ein fensterloses Steuerelement die [**NotifyWinEvent-Funktion**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) aufruft, gibt das Steuerelement die Objekt-ID des Benutzeroberflächenelements an, das das Ereignis ausgibt, und gibt den Steuerelementcontainer als Fenster an, das im Namen des Steuerelements auf [**WM \_ GETOBJECT-Nachrichten**](wm-getobject.md) reagiert.

Wenn eine Clientanwendung auf das Ereignis reagiert, empfängt der Steuerelementcontainer eine [**WM \_ GETOBJECT-Nachricht,**](wm-getobject.md) die die Objekt-ID des Benutzeroberflächenelements enthält, das das Ereignis ausgelöst hat. Der Steuerelementcontainer reagiert, indem er nach dem fensterlosen Steuerelement sucht, das die Objekt-ID "besitzt" und dann die [**IAccessibleHandler::AccessibleObjectFromID-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) dieses Steuerelements aufruft. Die **AccessibleObjectFromID-Methode** gibt den [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für das Benutzeroberflächenelement zurück, und der Steuerelementcontainer gibt den Zeiger an die Clientanwendung weiter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden Benutzeroberflächenautomatisierung, um den Zugriff auf ein fensterloses ActiveX-Steuerelement zu ermöglichen](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[Fensterloses ActiveX Barrierefreiheit](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 