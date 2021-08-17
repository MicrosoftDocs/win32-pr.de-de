---
description: Asynchrones Aufrufen von Dienstmethoden
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Asynchrones Aufrufen von Dienstmethoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3288f739b92de78ed25193756791d422fb1a87cf304e97f4aee904a85ed784b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697237"
---
# <a name="invoking-service-methods-asynchronously"></a>Asynchrones Aufrufen von Dienstmethoden

Die WpdServiceApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung die Dienstmethoden asynchron aufrufen kann. In diesem Beispiel werden die folgenden Schnittstellen verwendet.



| Schnittstelle    | Beschreibung          |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | Wird zum Abrufen der **IPortableDeviceServiceMethods-Schnittstelle** zum Aufrufen von Methoden für einen bestimmten Dienst verwendet.                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | Wird zum Aufrufen einer Dienstmethode verwendet.                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                                  | Wird verwendet, um die ausgehenden Methodenparameter und die Ergebnisse der eingehenden Methode zu enthalten. Dies kann **NULL sein,** wenn die Methode keine Parameter erfordert oder Ergebnisse zurückgibt. |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | Wird von der Anwendung implementiert, um die Methodenergebnisse zu empfangen, wenn eine Methode abgeschlossen wurde.                                                                               |



 

Wenn der Benutzer die Option "10" in der Befehlszeile auswählt, ruft die Anwendung die **InvokeMethodsAsync-Methode** auf, die sich im Modul ServiceMethods.cpp befindet. Beachten Sie, dass die Beispielanwendung vor dem Aufrufen der Methoden einen Contacts-Dienst auf einem verbundenen Gerät öffnet.

Dienstmethoden kapseln Funktionen, die von jedem Dienst definiert und implementiert werden. Sie sind für jeden Diensttyp eindeutig und werden durch eine GUID dargestellt. Der Contacts-Dienst definiert beispielsweise eine **BeginSync-Methode,** die Anwendungen aufrufen, um das Gerät für die Synchronisierung von Contact-Objekten vorzubereiten, und eine **EndSync-Methode,** um das Gerät zu benachrichtigen, dass die Synchronisierung abgeschlossen wurde. Anwendungen führen eine portable Gerätedienstmethode aus, indem [**sie IPortableDeviceServiceMethods::Invoke aufrufen.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke)

Dienstmethoden sollten nicht mit WPD-Befehlen verwechselt werden. WPD-Befehle sind Teil der standardmäßigen WPD Device Driver Interface (DDI) und stellen den Mechanismus für die Kommunikation zwischen einer WPD-Anwendung und dem Treiber dar. Befehle sind vordefiniert, nach Kategorien (z. B. **WPD \_ CATEGORY \_ COMMON)** unterteilt und werden durch eine **PROPERTYKEY-Struktur** dargestellt. Eine Anwendung sendet Befehle an den Gerätetreiber, indem [**sie IPortableDeviceService::SendCommand aufruft.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) Weitere Informationen finden Sie im Thema Befehle.

Die **InvokeMethodsAsync-Methode** ruft [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) auf, um eine [**IPortableDeviceServiceMethods-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) abzurufen. Über diese Schnittstelle wird die **InvokeMethodAsync-Hilfsfunktion** zweimal aufgerufen. einmal für die **BeginSync-Methode** und einmal für die **EndSync-Methode.** In diesem Beispiel wartet **InvokeMethodAsync** unbegrenzt darauf, dass ein globales Ereignis signalisiert wird, wenn [**IPortableDeviceServiceMethodCallback::OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) aufgerufen wird.

Im folgenden Code wird die **InvokeMethodsAsync-Methode** verwendet.


```C++
// Invoke methods on the Contacts Service asynchornously.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethodsAsync(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke the BeginSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_BeginSync);

        // This method does not take any parameters, so we pass in NULL
        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_BeginSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_EndSync);

        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_EndSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
    }
}
```



Die **InvokeMethodAsync-Hilfsfunktion** führt für jede aufgerufene Methode Folgendes aus:

-   Erstellt ein globales Ereignishand handle, das überwacht wird, um den Methodenabschluss zu bestimmen.
-   Erstellt ein **CMethodCallback-Objekt,** das als Argument für [**IPortableDeviceServiceMethods:InvokeAsync bereitgestellt wird.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync)
-   Ruft die **IPortableDeviceServiceMethods::InvokeAsync-Methode** auf, um die gegebene Methode auf aufruft.
-   Überwacht das globale Ereignishand handle auf Abschluss.
-   Führt eine Bereinigung durch.

Die **CMethodCallback-Klasse** veranschaulicht, wie eine Anwendung [**IPortableDeviceServiceMethodCallback implementieren kann.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback) Die Implementierung von **OnComplete** in dieser Klasse signalisiert ein Ereignis, um die Anwendung zu benachrichtigen, dass die Dienstmethode abgeschlossen wurde. Zusätzlich zur **OnComplete-Methode** implementiert diese Klasse **AddRef,** **QueryInterface** und **Release,** die verwendet werden, um die Verweisanzahl des Objekts und die schnittstellen, die es implementiert, zu verwalten.


```C++
class CMethodCallback : public IPortableDeviceServiceMethodCallback
{
public:
   CMethodCallback () : m_cRef(1)
   {
   }

   ~CMethodCallback ()
   {
   }

public:
    // IPortableDeviceServiceMethodCallback::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE OnComplete(
        HRESULT                 hrStatus,
        IPortableDeviceValues*  /*pResults*/) // We are ignoring results as our methods will not return any results
    {
        printf("** Method completed, status HRESULT = 0x%lx **\n", hrStatus);

        if (g_hMethodCompleteEvent != NULL)
        {
            SetEvent(g_hMethodCompleteEvent);
        }          
        return S_OK;
    }

    // IUnknown::AddRef
    virtual ULONG STDMETHODCALLTYPE AddRef(void)
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    // IUnknown::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceServiceMethodCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            *ppvObj = NULL;
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    // IUnknown::Release
    virtual ULONG STDMETHODCALLTYPE Release(void)
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

private:
    DWORD   m_cRef;
};
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
