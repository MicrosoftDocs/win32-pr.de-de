---
title: Verwenden von MSAA zum Zugreifen auf ein fensterloses ActiveX-Steuerelement
description: Beschreibt die Verwendung des Microsoft Active Accessibility \ 32; API, um sicherzustellen, dass das fensterlose Microsoft-ActiveX-Steuerelement für Hilfstechnologien (at)-Client Anwendungen zugänglich ist.
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- ActiveX-Steuerelement, Barrierefreiheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a76aa72fadef502a6a4319284ab34fdd5214d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337243"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a>Verwenden von MSAA zum Zugreifen auf ein fensterloses ActiveX-Steuerelement

Beschreibt, wie die Microsoft Active Accessibility-API verwendet wird, um sicherzustellen, dass das fensterlose Microsoft-ActiveX-Steuerelement für Hilfstechnologien (at)-Client Anwendungen zugänglich ist.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [ActiveX-Steuerelemente](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmierung von Microsoft Win32 und Component Object Model (com)
-   Fensterlose ActiveX-Steuerelemente
-   Microsoft Active Accessibility-Server

## <a name="instructions"></a>Anweisungen

### <a name="step-1-implement-the-iaccessible-interface"></a>Schritt 1: Implementieren Sie die IAccessible-Schnittstelle.

Um das fensterlose ActiveX-Steuerelement zugänglich zu machen, müssen Sie die Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle implementieren, genauso wie für ein Fenster basiertes Steuerelement, es sei denn, dies wird in den folgenden Schritten beschrieben. Weitere Informationen zum Implementieren von **IAccessible** finden Sie [im Entwicklerhandbuch für Active Accessibility-Server](developer-s-guide-for-active-accessibility-servers.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Schritt 2: Implementieren Sie die IServiceProvider-Schnittstelle.

Wenn ein Client Barrierefreiheits Informationen über das fensterlose Steuerelement anfordert, ruft der Container die [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) -Methode Ihres Steuer Elements auf, um den [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger abzurufen.

Dieses Beispiel zeigt, wie die [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) -Methode implementiert wird.


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



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a>Schritt 3: Delegieren von IAccessible:: get \_ accParent-Methoden aufrufen an die iaccessiblewindowlesssite:: getsamentaccessible-Methode der Steuerelement Website.

Wenn ein Client das übergeordnete Objekt des fensterlosen Steuer Elements anfordert, ruft der Container die [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) -Methode Ihres Steuer Elements auf. Die **get \_ accParent** -Implementierung sollte an die [**iaccessiblewindowlesssite:: getparameentaccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) -Methode des Containers delegieren.

In diesem Beispiel wird gezeigt, wie die [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) -Methode implementiert wird.


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



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a>Schritt 4: beschaffen eines Bereichs von Objekt-IDs, die den Ereignis Quellen in Ihrem fensterlosen Steuerelement zugewiesen werden sollen.

Wie fensterbasierte Steuerelemente Ruft ein fensterloses ActiveX-Steuerelement die [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) -Funktion auf, um Clients über wichtige Ereignisse zu benachrichtigen. Die Funktionsparameter enthalten die Objekt-ID des Elements, das das Ereignis aufhebt. Das fensterlose Steuerelement muss Objekt-IDs mithilfe eines Werts aus einem Bereich zuweisen, der durch Aufrufen der [**iaccessiblewindowlesssite:: acquireobjectidrange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) -Methode der Steuerelement Website abgerufen wird.

Dieses Beispiel zeigt, wie Sie einen Bereich von Objekt-ID-Werten aus dem Steuerelement Container abrufen.


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



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a>Schritt 5: Implementieren Sie die IAccessibleHandler-Schnittstelle.

Wenn ein fensterloses Steuerelement die [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) -Funktion aufruft, gibt das Steuerelement die Objekt-ID des Benutzeroberflächen Elements an, das das Ereignis aufhebt, und gibt den Steuerelement Container als das Fenster an, das auf die [**WM- \_ GetObject**](wm-getobject.md) -Nachrichten im Namen des Steuer Elements antwortet.

Wenn eine Client Anwendung auf das-Ereignis reagiert, empfängt der Steuerelement Container eine [**WM \_ GetObject**](wm-getobject.md) -Nachricht, die die Objekt-ID des UI-Elements enthält, das das Ereignis ausgelöst hat. Der Steuerelement Container antwortet, indem er das fensterlose Steuerelement sucht, das die Objekt-ID besitzt, und dann die [**iaccessibleobjectfromid**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) -Methode dieses Steuer Elements aufruft. Die **AccessibleObjectFromID** -Methode gibt den [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger für das UI-Element zurück, und der Steuerelement Container leitet den Zeiger an die Client Anwendung weiter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Benutzeroberflächen Automatisierung, um ein fensterloses ActiveX-Steuerelement zugänglich zu machen](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[Barrierefreiheit für das fensterlose ActiveX-Steuerelement](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 