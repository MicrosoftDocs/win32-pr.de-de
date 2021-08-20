---
description: Bei der Arbeit mit der Mobilen Breitband-API sollten die folgenden bewährten Methoden verwendet werden, um die bestmögliche Leistung zu erzielen.
ms.assetid: 523e3ea4-1d4e-45d1-bc24-93aa2fb14390
title: Bewährte Methoden für die mobile Breitband-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3a6c1e236a61dd2a5321be2edb7a68156f904605bd8a1da5fc169ea8b70e464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881654"
---
# <a name="mobile-broadband-api-best-practices"></a>Bewährte Methoden für die mobile Breitband-API

Bei der Arbeit mit der Mobilen Breitband-API sollten die folgenden bewährten Methoden verwendet werden, um die bestmögliche Leistung zu erzielen.

## <a name="do-not-cache-functional-objects"></a>Funktionale Objekte nicht zwischenspeichern

Funktionale Objekte, z. B. [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) und andere, werden von Managerobjekten wie [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager)mithilfe der Enumerationsmethode für das entsprechende Managerobjekt abgerufen. Diese funktionalen Objekte dürfen nicht zwischengespeichert werden, da zwischengespeicherte funktionale Objekte veraltete Daten enthalten. Die synchronen Vorgänge, die für diese funktionalen Objekte ausgeführt werden, geben die gleichen Daten zurück, bis die funktionalen Objekte erneut abgerufen werden.

Cachen Sie stattdessen die Manager-Objekte zwischen, und rufen Sie die funktionalen Objekte aus dem Manager-Objekt ab, indem Sie die Enumerationsmethode für das entsprechende Managerobjekt erneut verwenden, um die neuesten Daten abzurufen.

Im folgenden Codebeispiel wird die richtige Methode zum Zwischenspeichern von Managerobjekten veranschaulicht.


```C++
#include <atlbase.h>
#include "mbnapi.h"
#include <tchar.h>

int main()
{
    HRESULT hr = E_FAIL;
    int returnVal = 0;

    do
    {
        hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);    
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;

        //Do the below once(cache the manager objects)
        hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        SAFEARRAY *psa = NULL;

        //Do the below each time(do not cache functional objects)
        hr = g_InterfaceMgr->GetInterfaces(&psa);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        LONG lLower;
        LONG lUpper;

        hr = SafeArrayGetLBound(psa, 1, &lLower);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        hr = SafeArrayGetUBound(psa, 1, &lUpper);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterface>  pInf = NULL;
        MBN_READY_STATE readyState;

        for (LONG l = lLower; l <= lUpper; l++)
        {
            hr = SafeArrayGetElement(psa, &l, (void*)(&pInf));
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            hr = pInf->GetReadyState(&readyState);
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            _tprintf(_T("Ready State = %d"), readyState); 
        }

        if (FAILED(hr))
        {
            break;
        }
    } while (FALSE);


    CoUninitialize();
    return returnVal;
}
```



## <a name="handle-all-notifications"></a>Behandeln aller Benachrichtigungen

Befolgen Und verarbeiten Sie alle Benachrichtigungen, auch wenn sie nicht von Ihrer Anwendung ausgelöst werden. Dies ist erforderlich, um die Benutzeroberfläche mit dem tatsächlichen Zustand des Geräts synchron zu halten.

Auf einem Computer können mehrere Verbindungs-Manager ausgeführt werden. Die von Windows 7 bereitgestellte benutzeroberfläche für die native Ansicht verfügbarer Netzwerkschnittstellen ist ein Verbindungs-Manager. Alle anderen Verbindungs-Manager müssen auf alle Benachrichtigungen reagieren, um die Synchronisierung der Windows nativen Benutzeroberfläche zu erhalten. Ein Benutzer kann einige Vorgänge für einen verbindungs-Manager ausführen, was zu einer Zustandsänderung des mobilen Breitbandgeräts führen kann. Andere Verbindungs-Manager müssen jedoch aktualisiert bleiben, um den geänderten Zustand des Geräts ordnungsgemäß anzugeben.

Wenn Sie beispielsweise eine Verbindung mit einem der Verbindungs-Manager herstellen, ändert sich der Zustand des Geräts von verfügbar in verbunden. Diese Änderung sollte für die Verbindungs-Manager sichtbar sein, die diese Aktion nicht initiiert haben. Alle Verbindungs-Manager, die über eine Benutzeroberfläche verfügen, die den Verbindungsstatus des Geräts angibt, müssen die Benachrichtigungen zum Verbindungszustand abhören und verarbeiten, um ihre Benutzeroberfläche ordnungsgemäß zu aktualisieren.

## <a name="sending-and-receiving-bytes"></a>Senden und Empfangen von Bytes

Verwenden Sie die IP-Hilfsfunktionen [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) und [GetlfEntry2,](/windows/win32/api/netioapi/nf-netioapi-getifentry2) um Bytes zu senden und zu empfangen.

## <a name="using-the-pin-unblock-api"></a>Verwenden der API zum Anheften der Blockierung

Eine aufrufende Clientanwendung muss erhöht werden, damit [**IMbnPin::Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock)erfolgreich aufgerufen werden kann. Diese Methode ist der einzige Teil der mobilen Breitband-API, der Administrator- oder NCO-Berechtigungen erfordert. Weitere Informationen finden Sie unter [Eine Beschreibung der Gruppe "Netzwerkkonfigurationsoperatoren".]( https://support.microsoft.com/kb/297938/en-us)

## <a name="working-with-safearrays"></a>Arbeiten mit SafeArrays

-   Verwenden Sie ZeroMemory(), bevor Sie auf Elemente in einem SafeArray zugreifen.

-   Überprüfen Sie nicht die Indizes eines SafeArray. Sie können negativ sein.

Das folgende Codebeispiel zeigt, wie ein SafeArray ordnungsgemäß behandelt wird.


```C++
#include <atlbase.h>
#include "mbnapi.h"

void CreateVisibleProviderList(LPCWSTR interfaceID)
{
    CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;
    SAFEARRAY *visibleProviders = NULL;
    long visibleLower = 0;
    long visibleUpper = 0;
    MBN_PROVIDER *pProvider = NULL;
    CComPtr<IMbnInterface> pInterface = NULL;

    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
    
    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = g_InterfaceMgr->GetInterface(interfaceID, & pInterface);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    ULONG age;

    hr = pInterface->GetVisibleProviders(&age, &visibleProviders);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetLBound(visibleProviders, 1, &visibleLower);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetUBound(visibleProviders, 1, &visibleUpper);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    //don't check on the indexes of safearray to be positive
    if (visibleLower > visibleUpper) 
    {
        // There are no visible providers in this case.
        hr = HRESULT_FROM_WIN32(ERROR_NOT_FOUND);
        goto ERROR_0;
    }

    DWORD size = (visibleUpper - visibleLower + 1) * sizeof(BOOL);
    DBG_UNREFERENCED_LOCAL_VARIABLE(size); 
    
    pProvider = (MBN_PROVIDER *)CoTaskMemAlloc(sizeof(MBN_PROVIDER));
    if (!pProvider) 
    {
        hr = E_OUTOFMEMORY;
        goto ERROR_0;
    }

    for (LONG vIndex = visibleLower; vIndex <= visibleUpper; vIndex++) 
    {
        //use zeromemory before accessing any elements in a safearray
        ZeroMemory(pProvider, sizeof(MBN_PROVIDER));
        hr = SafeArrayGetElement(visibleProviders, &vIndex, (void *)pProvider);
        if (FAILED(hr)) 
        {
            continue;
        }
    }

ERROR_0:
    if (visibleProviders) 
    {
        SafeArrayDestroy(visibleProviders);
        visibleProviders = NULL;
    }

    CoUninitialize();
}
```



 

 
