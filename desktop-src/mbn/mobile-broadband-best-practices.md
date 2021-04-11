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
# <a name="mobile-broadband-api-best-practices"></a><span data-ttu-id="63dc3-103">Bewährte Methoden für die mobile Breitband-API</span><span class="sxs-lookup"><span data-stu-id="63dc3-103">Mobile Broadband API Best Practices</span></span>

<span data-ttu-id="63dc3-104">Beim Arbeiten mit der mobilen Breitband-API sollten die folgenden bewährten Methoden verwendet werden, um die bestmögliche Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="63dc3-104">When working with the Mobile Broadband API the following set of best practices should be used in order to achieve the best possible performance.</span></span>

## <a name="do-not-cache-functional-objects"></a><span data-ttu-id="63dc3-105">Funktionale Objekte nicht zwischenspeichern</span><span class="sxs-lookup"><span data-stu-id="63dc3-105">Do Not Cache Functional Objects</span></span>

<span data-ttu-id="63dc3-106">Funktionale Objekte, wie z. [**b. imbninterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) und andere, werden von Manager-Objekten wie [**imbninterfacemanager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager)abgerufen, wobei die Enumerationsmethode für das entsprechende Manager-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63dc3-106">Functional objects, such as [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) and others, are obtained from manager objects, like [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), using the enumeration method on the corresponding manager object.</span></span> <span data-ttu-id="63dc3-107">Zwischenspeichern Sie diese funktionalen Objekte nicht, da zwischengespeicherte funktionale Objekte veraltete Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="63dc3-107">Do not cache these functional objects, since cached functional objects contain stale data.</span></span> <span data-ttu-id="63dc3-108">Bei synchronen Vorgängen, die für diese funktionalen Objekte ausgeführt werden, werden dieselben Daten zurückgegeben, bis die funktionalen Objekte erneut abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="63dc3-108">The synchronous operations performed on these functional objects will return the same data until the functional objects are obtained again.</span></span>

<span data-ttu-id="63dc3-109">Zwischenspeichern Sie stattdessen die Manager-Objekte, und rufen Sie die funktionalen Objekte aus dem Manager-Objekt mithilfe der Enumerationsmethode für das entsprechende Manager-Objekt ab, um die neuesten Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="63dc3-109">Instead, cache the manager objects and obtain the functional objects from manager object using the enumeration method on the corresponding manager object again to get the latest data.</span></span>

<span data-ttu-id="63dc3-110">Das folgende Codebeispiel veranschaulicht die richtige Methode zum Zwischenspeichern von Manager-Objekten.</span><span class="sxs-lookup"><span data-stu-id="63dc3-110">The following code example demonstrates the proper way to cache manager objects.</span></span>


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



## <a name="handle-all-notifications"></a><span data-ttu-id="63dc3-111">Alle Benachrichtigungen behandeln</span><span class="sxs-lookup"><span data-stu-id="63dc3-111">Handle All Notifications</span></span>

<span data-ttu-id="63dc3-112">Befolgen und behandeln Sie alle Benachrichtigungen, auch wenn Sie nicht von Ihrer Anwendung ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="63dc3-112">Follow and handle all notifications, even if they are not triggered by your application.</span></span> <span data-ttu-id="63dc3-113">Dies ist erforderlich, um die Benutzeroberfläche mit dem tatsächlichen Status des Geräts synchron zu halten.</span><span class="sxs-lookup"><span data-stu-id="63dc3-113">This is required to keep the UI in sync with the actual state of the device.</span></span>

<span data-ttu-id="63dc3-114">Auf einem Computer können mehrere Verbindungs-Manager ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="63dc3-114">There can be more than one connection manager running on a computer.</span></span> <span data-ttu-id="63dc3-115">Die von Windows 7 bereitgestellte Benutzeroberfläche für die native Anzeige verfügbarer Netzwerkschnittstellen ist ein Verbindungs-Manager.</span><span class="sxs-lookup"><span data-stu-id="63dc3-115">The native View Available Network Interface UI provided by Windows 7 is a connection manager.</span></span> <span data-ttu-id="63dc3-116">Alle anderen Verbindungs-Manager müssen auf alle Benachrichtigungen reagieren, damit Sie in der systemeigenen Windows-Benutzeroberfläche synchron bleiben.</span><span class="sxs-lookup"><span data-stu-id="63dc3-116">Any other connection managers need to respond to all notifications to remain in sync the Windows native UI.</span></span> <span data-ttu-id="63dc3-117">Ein Benutzer kann einen Vorgang für einen der Verbindungs-Manager ausführen, was zu einer Zustandsänderung des mobilen Breitband Geräts führen kann.</span><span class="sxs-lookup"><span data-stu-id="63dc3-117">A user may opt to perform some operation on one of the connection managers which may result in a state change of the Mobile Broadband device.</span></span> <span data-ttu-id="63dc3-118">Andere Verbindungs-Manager müssen jedoch aktualisiert werden, um den geänderten Zustand des Geräts korrekt anzugeben.</span><span class="sxs-lookup"><span data-stu-id="63dc3-118">However, other connection managers need to remain updated in order to properly indicate the modified state of the device.</span></span>

<span data-ttu-id="63dc3-119">Wenn Sie z. b. eine Verbindung mithilfe eines der Verbindungs-Manager herstellen, wird der Status des Geräts von "verfügbar" in "verbunden" geändert.</span><span class="sxs-lookup"><span data-stu-id="63dc3-119">For example, performing a connect using one of the connection managers will change the state of the device from available to connected.</span></span> <span data-ttu-id="63dc3-120">Diese Änderung sollte für die Verbindungs-Manager sichtbar sein, die diese Aktion nicht initiiert haben.</span><span class="sxs-lookup"><span data-stu-id="63dc3-120">This change should be visible to the connection managers that didn’t initiate this action.</span></span> <span data-ttu-id="63dc3-121">Alle Verbindungs-Manager, die über eine Benutzeroberfläche verfügen, die den Verbindungsstatus des Geräts angibt, müssen die Verbindungs Zustands Benachrichtigungen überwachen und verarbeiten, um die Benutzeroberfläche ordnungsgemäß aktualisieren zu können.</span><span class="sxs-lookup"><span data-stu-id="63dc3-121">All connection managers that have UI that indicates the connection state of the device, need to listen to and handle the connection state notifications in order to properly update their user interface.</span></span>

## <a name="sending-and-receiving-bytes"></a><span data-ttu-id="63dc3-122">Senden und empfangen von Bytes</span><span class="sxs-lookup"><span data-stu-id="63dc3-122">Sending And Receiving Bytes</span></span>

<span data-ttu-id="63dc3-123">Verwenden Sie die IP-Hilfsfunktionen [getlfentry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) und [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) , um Bytes zu senden und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="63dc3-123">Use the IP Helper functions [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) and [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) to send and receive bytes.</span></span>

## <a name="using-the-pin-unblock-api"></a><span data-ttu-id="63dc3-124">Verwenden der PIN Unblock-API</span><span class="sxs-lookup"><span data-stu-id="63dc3-124">Using The Pin Unblock API</span></span>

<span data-ttu-id="63dc3-125">Eine aufrufende Client Anwendung muss erhöht werden, damit [**imbnpin:: Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock)erfolgreich aufgerufen werden konnte.</span><span class="sxs-lookup"><span data-stu-id="63dc3-125">A calling client application must be elevated in order to successfully to invoke [**IMbnPin::Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock).</span></span> <span data-ttu-id="63dc3-126">Diese Methode ist der einzige Teil der mobilen Breitband-API, für die Administrator-oder NCO-Berechtigungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="63dc3-126">This method is the only portion of the Mobile Broadband API that requires administrator or NCO privileges.</span></span> <span data-ttu-id="63dc3-127">Weitere Informationen finden Sie [in der Beschreibung der Gruppe "Netzwerkkonfigurations-Operatoren]( https://support.microsoft.com/kb/297938/en-us) ".</span><span class="sxs-lookup"><span data-stu-id="63dc3-127">See [A Description of the Network Configuration Operators Group]( https://support.microsoft.com/kb/297938/en-us) for more information.</span></span>

## <a name="working-with-safearrays"></a><span data-ttu-id="63dc3-128">Arbeiten mit SAFEARRAYs</span><span class="sxs-lookup"><span data-stu-id="63dc3-128">Working With SafeArrays</span></span>

-   <span data-ttu-id="63dc3-129">Verwenden Sie ZeroMemory (), bevor Sie auf Elemente in einem SafeArray zugreifen.</span><span class="sxs-lookup"><span data-stu-id="63dc3-129">Use ZeroMemory() before accessing any elements in a SafeArray.</span></span>

-   <span data-ttu-id="63dc3-130">Überprüfen Sie die Indizes eines SAFEARRAY nicht.</span><span class="sxs-lookup"><span data-stu-id="63dc3-130">Don’t check on the indexes of a SafeArray.</span></span> <span data-ttu-id="63dc3-131">Sie können negativ sein.</span><span class="sxs-lookup"><span data-stu-id="63dc3-131">They may be negative.</span></span>

<span data-ttu-id="63dc3-132">Im folgenden Codebeispiel wird gezeigt, wie ein SAFEARRAY ordnungsgemäß behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="63dc3-132">The following code example shows how to properly handle a SafeArray.</span></span>


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



 

 
