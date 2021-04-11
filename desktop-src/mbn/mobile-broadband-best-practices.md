---
description: Beim Arbeiten mit der mobilen Breitband-API sollten die folgenden bewährten Methoden verwendet werden, um die bestmögliche Leistung zu erzielen.
ms.assetid: 523e3ea4-1d4e-45d1-bc24-93aa2fb14390
title: Bewährte Methoden für die mobile Breitband-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399c2ebc40a357eac9686bc3c2c9f471e3b853f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214701"
---
# <a name="mobile-broadband-api-best-practices"></a>Bewährte Methoden für die mobile Breitband-API

Beim Arbeiten mit der mobilen Breitband-API sollten die folgenden bewährten Methoden verwendet werden, um die bestmögliche Leistung zu erzielen.

## <a name="do-not-cache-functional-objects"></a>Funktionale Objekte nicht zwischenspeichern

Funktionale Objekte, wie z. [**b. imbninterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) und andere, werden von Manager-Objekten wie [**imbninterfacemanager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager)abgerufen, wobei die Enumerationsmethode für das entsprechende Manager-Objekt verwendet wird. Zwischenspeichern Sie diese funktionalen Objekte nicht, da zwischengespeicherte funktionale Objekte veraltete Daten enthalten. Bei synchronen Vorgängen, die für diese funktionalen Objekte ausgeführt werden, werden dieselben Daten zurückgegeben, bis die funktionalen Objekte erneut abgerufen werden.

Zwischenspeichern Sie stattdessen die Manager-Objekte, und rufen Sie die funktionalen Objekte aus dem Manager-Objekt mithilfe der Enumerationsmethode für das entsprechende Manager-Objekt ab, um die neuesten Daten abzurufen.

Das folgende Codebeispiel veranschaulicht die richtige Methode zum Zwischenspeichern von Manager-Objekten.


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



## <a name="handle-all-notifications"></a>Alle Benachrichtigungen behandeln

Befolgen und behandeln Sie alle Benachrichtigungen, auch wenn Sie nicht von Ihrer Anwendung ausgelöst werden. Dies ist erforderlich, um die Benutzeroberfläche mit dem tatsächlichen Status des Geräts synchron zu halten.

Auf einem Computer können mehrere Verbindungs-Manager ausgeführt werden. Die von Windows 7 bereitgestellte Benutzeroberfläche für die native Anzeige verfügbarer Netzwerkschnittstellen ist ein Verbindungs-Manager. Alle anderen Verbindungs-Manager müssen auf alle Benachrichtigungen reagieren, damit Sie in der systemeigenen Windows-Benutzeroberfläche synchron bleiben. Ein Benutzer kann einen Vorgang für einen der Verbindungs-Manager ausführen, was zu einer Zustandsänderung des mobilen Breitband Geräts führen kann. Andere Verbindungs-Manager müssen jedoch aktualisiert werden, um den geänderten Zustand des Geräts korrekt anzugeben.

Wenn Sie z. b. eine Verbindung mithilfe eines der Verbindungs-Manager herstellen, wird der Status des Geräts von "verfügbar" in "verbunden" geändert. Diese Änderung sollte für die Verbindungs-Manager sichtbar sein, die diese Aktion nicht initiiert haben. Alle Verbindungs-Manager, die über eine Benutzeroberfläche verfügen, die den Verbindungsstatus des Geräts angibt, müssen die Verbindungs Zustands Benachrichtigungen überwachen und verarbeiten, um die Benutzeroberfläche ordnungsgemäß aktualisieren zu können.

## <a name="sending-and-receiving-bytes"></a>Senden und empfangen von Bytes

Verwenden Sie die IP-Hilfsfunktionen [getlfentry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) und [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) , um Bytes zu senden und zu empfangen.

## <a name="using-the-pin-unblock-api"></a>Verwenden der PIN Unblock-API

Eine aufrufende Client Anwendung muss erhöht werden, damit [**imbnpin:: Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock)erfolgreich aufgerufen werden konnte. Diese Methode ist der einzige Teil der mobilen Breitband-API, für die Administrator-oder NCO-Berechtigungen erforderlich sind. Weitere Informationen finden Sie [in der Beschreibung der Gruppe "Netzwerkkonfigurations-Operatoren]( https://support.microsoft.com/kb/297938/en-us) ".

## <a name="working-with-safearrays"></a>Arbeiten mit SAFEARRAYs

-   Verwenden Sie ZeroMemory (), bevor Sie auf Elemente in einem SafeArray zugreifen.

-   Überprüfen Sie die Indizes eines SAFEARRAY nicht. Sie können negativ sein.

Im folgenden Codebeispiel wird gezeigt, wie ein SAFEARRAY ordnungsgemäß behandelt wird.


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



 

 
