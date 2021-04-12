---
description: Asynchrones Aufrufen von Dienst Methoden
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Asynchrones Aufrufen von Dienst Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d312cc76cf8cb737136629c1e2c8135d1b7bd1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216956"
---
# <a name="invoking-service-methods-asynchronously"></a>Asynchrones Aufrufen von Dienst Methoden

Die Anwendung wpdserviceapisample enthält Code, der veranschaulicht, wie eine Anwendung die Dienst Methoden asynchron aufrufen kann. In diesem Beispiel werden die folgenden Schnittstellen verwendet.



|                                                                                         |                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstelle                                                                               | BESCHREIBUNG                                                                                                                                                             |
| [**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | Wird zum Abrufen der **iportabledeviceservicemethods** -Schnittstelle verwendet, um Methoden für einen bestimmten Dienst aufzurufen.                                                                  |
| [**Iportabledeviceservicemethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | Wird verwendet, um eine Dienst Methode aufzurufen.                                                                                                                                        |
| [**Iportablede vicevalues**](iportabledevicevalues.md)                                  | Wird verwendet, um die Parameter für die ausgehende Methode und die Ergebnisse der eingehenden Methode aufzunehmen. Dieser Wert kann **null** sein, wenn die Methode keine Parameter erfordert oder keine Ergebnisse zurückgibt. |
| [**Iportablede viceservicemethodcallback**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | Wird von der Anwendung implementiert, um die Methoden Ergebnisse zu empfangen, wenn eine Methode abgeschlossen wurde.                                                                               |



 

Wenn der Benutzer die Option "10" in der Befehlszeile auswählt, ruft die Anwendung die **invokemethodsasync** -Methode auf, die im Modul "servicemethods. cpp" zu finden ist. Beachten Sie, dass die Beispielanwendung vor dem Aufrufen der Methoden einen Contacts-Dienst auf einem verbundenen Gerät öffnet.

Dienst Methoden Kapseln Funktionen, die von den einzelnen Diensten definiert und implementiert werden. Sie sind für jeden Diensttyp eindeutig und werden durch eine GUID dargestellt. Der Kontakt Dienst definiert z. b. eine **BeginSync** -Methode, die Anwendungen aufrufen, um das Gerät für die Synchronisierung von Kontakt Objekten vorzubereiten, und eine **EndSync** -Methode, um das Gerät zu benachrichtigen, dass die Synchronisierung abgeschlossen ist. Anwendungen führen eine Dienst Methode für tragbare Geräte durch Aufrufen von [**iportabledeviceservicemethods::**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke)Call aus.

Dienst Methoden sollten nicht mit WPD-Befehlen verwechselt werden. WPD-Befehle sind Teil der standardmäßigen WPD-Gerätetreiber Schnittstelle (DDI) und stellen den Mechanismus für die Kommunikation zwischen einer WPD-Anwendung und dem Treiber dar. Befehle sind vordefiniert, nach Kategorien gruppiert (z. b. **WPD- \_ Kategorie \_ Common**) und werden durch eine **PropertyKey** -Struktur dargestellt. Eine Anwendung sendet durch Aufrufen von [**iportabledeviceservice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)Befehle an den Gerätetreiber. Weitere Informationen finden Sie im Thema "Befehle".

Die **invokemethodsasync** -Methode ruft [**iportabledeviceservice:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) auf, um eine [**iportabledeviceservicemethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) -Schnittstelle abzurufen. Mithilfe dieser Schnittstelle ruft Sie die **invokemethodasync** -Hilfsfunktion zweimal auf. einmal für die **BeginSync** -Methode und einmal für die **EndSync** -Methode. In diesem Beispiel wartet **invokemethodasync** unbegrenzt darauf, dass ein globales Ereignis signalisiert wird, wenn [**iportablede viceservicemethodcallback:: OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) aufgerufen wird.

Im folgenden Code wird die **invokemethodsasync** -Methode verwendet.


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



Die Hilfsfunktion **invokemethodasync** führt für jede aufgerufenen Methode Folgendes aus:

-   Erstellt einen globalen Ereignis handle, den es überwacht, um den Abschluss der Methode zu bestimmen.
-   Erstellt ein **cmethodcallback** -Objekt, das als Argument für [**iportabledeviceservicemethods: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync)bereitgestellt wird.
-   Ruft die **iportabledeviceservicemethods:: InvokeAsync** -Methode auf, um die angegebene Methode aufzurufen.
-   Überwacht den globalen Ereignis Handle auf den Abschluss.
-   Führt eine Bereinigung durch.

Die **cmethodcallback** -Klasse veranschaulicht, wie eine Anwendung [**iportabledeviceservicemethodcallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)implementieren kann. Die Implementierung von **OnComplete** in dieser Klasse signalisiert einem Ereignis, dass die Anwendung benachrichtigt wird, dass die Dienst Methode abgeschlossen wurde. Zusätzlich zur **OnComplete** -Methode implementiert diese Klasse " **adressf**", " **QueryInterface**" und " **Release**", die zum Verwalten des Verweis Zählers des Objekts und der von ihm implementierten Schnittstellen verwendet werden.


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

[**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**Iportablede viceservicemethodcallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[**Iportabledeviceservicemethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[Wpdservicesapisample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
