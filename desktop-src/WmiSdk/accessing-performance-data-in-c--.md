---
description: Die WMI-Api für hohe Leistung ist eine Reihe von Schnittstellen, die Daten aus Leistungsindikatorklassen abrufen.
ms.assetid: ee0a2ead-f53a-4651-a287-04a62eba3f84
ms.tgt_platform: multiple
title: Zugreifen auf Leistungsdaten in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e566fb5803e598e42fac06d8f04fe3e71935008668e397a47d0226a96560eec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820327"
---
# <a name="accessing-performance-data-in-c"></a>Zugreifen auf Leistungsdaten in C++

Die WMI-Api für hohe Leistung ist eine Reihe von Schnittstellen, die Daten aus [Leistungsindikatorklassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)abrufen. Diese Schnittstellen erfordern [](gloss-r.md) die Verwendung eines Aktualisierungsobjekts, um die Samplingrate zu erhöhen. Weitere Informationen zur Verwendung des Aktualisierungsobjekts bei der Skripterstellung finden Sie unter [Zugreifen auf Leistungsdaten in Skript-](accessing-performance-data-in-script.md) und [WMI-Aufgaben: Leistungsüberwachung.](wmi-tasks--performance-monitoring.md)

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [Aktualisieren von Leistungsdaten](#refreshing-performance-data)
-   [Hinzufügen von Enumeratoren zur WMI-Aktualisierung](#adding-enumerators-to-the-wmi-refresher)
-   [Beispiel](#example)
-   [Zugehörige Themen](#related-topics)

## <a name="refreshing-performance-data"></a>Aktualisieren von Leistungsdaten

Ein Aktualisierungsobjekt erhöht die Datenanbieter- und Clientleistung, indem Daten abgerufen werden, ohne Prozessgrenzen zu überschreiten. Wenn sich sowohl der Client als auch der Server auf demselben Computer befinden, lädt eine Aktualisierung den prozessübergreifenden Hochleistungsanbieter auf den Client und kopiert Daten direkt aus Anbieterobjekten in Clientobjekte. Wenn sich der Client und der Server auf verschiedenen Computern befinden, erhöht die Aktualisierung die Leistung, indem Objekte auf dem Remotecomputer zwischengespeichert und minimale Datensätze an den Client übertragen werden.

Eine Aktualisierungs-Aktualisierer-Aktualisiererin:

-   Verbindet einen Client automatisch erneut mit einem WMI-Remotedienst, wenn ein Netzwerkfehler auftritt oder der Remotecomputer neu gestartet wird.

    Standardmäßig versucht eine Aktualisierung, ihre Anwendung erneut mit dem relevanten Hochleistungsanbieter zu verbinden, wenn eine Remoteverbindung zwischen den beiden Computern fehlschlägt. Um eine erneute Verbindung zu verhindern, übergeben Sie das **Flag WBEM \_ FLAG REFRESH NO AUTO \_ \_ \_ \_ RECONNECT** im [**Refresh-Methodenaufruf.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) Skriptclients müssen die [**SWbemRefresher.AutoReconnect-Eigenschaft**](swbemrefresher-autoreconnect.md) auf **FALSE** festlegen.

-   Lädt mehrere Objekte und Enumeratoren, die von denselben oder verschiedenen Anbietern bereitgestellt werden.

    Ermöglicht es Ihnen, einer Aktualisierung mehrere Objekte, Enumeratoren oder beides hinzuzufügen.

-   Listet Objekte auf.

    Wie andere Anbieter kann ein Hochleistungsanbieter Objekte aufzählen.

Nachdem Sie das Schreiben Ihres Hochleistungsclients abgeschlossen haben, können Sie die Antwortzeit verbessern. Da die [**IWbemObjectAccess-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) für geschwindigkeitsoptimiert ist, ist die Schnittstelle nicht systemintern threadsicher. Greifen Sie daher während eines Aktualisierungsvorgangs nicht auf das aktualisierbare Objekt oder die aktualisierbare Enumeration zu. Um Objekte während **IWbemObjectAccess-Methodenaufrufen** threadübergreifend zu schützen, verwenden Sie die [**Methoden IWbemObjectAccess::Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) und [**Unlock.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) Synchronisieren Sie Ihre Threads, um die Leistung zu verbessern, sodass Sie keine einzelnen Threads sperren müssen. Das Reduzieren von Threads und Synchronisieren von Objektgruppen für Aktualisierungsvorgänge bietet die beste Gesamtleistung.

## <a name="adding-enumerators-to-the-wmi-refresher"></a>Hinzufügen von Enumeratoren zur WMI-Aktualisierung

Sowohl die Anzahl der Instanzen als auch die Daten in jeder Instanz werden aktualisiert, indem der Aktualisierung ein Enumerator hinzugefügt wird, sodass jeder Aufruf von [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) zu einer vollständigen Enumeration führt.

Das folgende C++-Codebeispiel erfordert die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Im folgenden Verfahren wird gezeigt, wie Sie einer Aktualisierung einen Enumerator hinzufügen.

**So fügen Sie einer Aktualisierung einen Enumerator hinzu**

1.  Rufen Sie die [**IWbemConfigureRefresher::AddEnum-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) mithilfe des Pfads zum aktualisierbaren Objekt und der [**IWbemServices-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) auf.

    Die Aktualisierung gibt einen Zeiger auf eine [**IWbemHiPerfEnum-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) zurück. Sie können die **IWbemHiPerfEnum-Schnittstelle** verwenden, um auf die Objekte in der Enumeration zuzugreifen.

    ```C++
    IWbemHiPerfEnum* pEnum = NULL;
    long lID;
    IWbemConfigureRefresher* pConfig;
    IWbemServices* pNameSpace;

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL,
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;
    ```

    

2.  Erstellen Sie eine Schleife, die die folgenden Aktionen ausführt:

    -   Aktualisiert das -Objekt mithilfe eines Aufrufs von [**IWbemRefresher::Refresh.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)
    -   Stellt ein Array von [**IWbemObjectAccess-Schnittstellenzeigern**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) auf die [**IWbemHiPerfEnum::GetObjects-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) bereit.
    -   Greift mithilfe der [**IWbemObjectAccess-Methoden,**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) die an [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects)übergeben werden, auf die Eigenschaften des Enumerators zu.

        Ein Eigenschaftenhandle kann an jede [**IWbemObjectAccess-Instanz**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) übergeben werden, um den aktualisierten Wert abzurufen. Der Client muss [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufrufen, um die von [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects)zurückgegebenen **IWbemObjectAccess-Zeiger** freizugeben.

## <a name="example"></a>Beispiel

Im folgenden C++-Codebeispiel wird eine Hochleistungsklasse aufgeführt, bei der der Client ein Eigenschaftenhandle aus dem ersten Objekt abruft und das Handle für den Rest des Aktualisierungsvorgangs wiederverwendet. Jeder Aufruf der [**Refresh-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) aktualisiert die Anzahl der Instanzen und die Instanzdaten.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int __cdecl wmain(int argc, wchar_t* argv[])
{
    // To add error checking,
    // check returned HRESULT below where collected.
    HRESULT                 hr = S_OK;
    IWbemRefresher          *pRefresher = NULL;
    IWbemConfigureRefresher *pConfig = NULL;
    IWbemHiPerfEnum         *pEnum = NULL;
    IWbemServices           *pNameSpace = NULL;
    IWbemLocator            *pWbemLocator = NULL;
    IWbemObjectAccess       **apEnumAccess = NULL;
    BSTR                    bstrNameSpace = NULL;
    long                    lID = 0;
    long                    lVirtualBytesHandle = 0;
    long                    lIDProcessHandle = 0;
    DWORD                   dwVirtualBytes = 0;
    DWORD                   dwProcessId = 0;
    DWORD                   dwNumObjects = 0;
    DWORD                   dwNumReturned = 0;
    DWORD                   dwIDProcess = 0;
    DWORD                   i=0;
    int                     x=0;

    if (FAILED (hr = CoInitializeEx(NULL,COINIT_MULTITHREADED)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_NONE,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, EOAC_NONE, 0)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemLocator, 
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemLocator,
        (void**) &pWbemLocator)))
    {
        goto CLEANUP;
    }

    // Connect to the desired namespace.
    bstrNameSpace = SysAllocString(L"\\\\.\\root\\cimv2");
    if (NULL == bstrNameSpace)
    {
        hr = E_OUTOFMEMORY;
        goto CLEANUP;
    }
    if (FAILED (hr = pWbemLocator->ConnectServer(
        bstrNameSpace,
        NULL, // User name
        NULL, // Password
        NULL, // Locale
        0L,   // Security flags
        NULL, // Authority
        NULL, // Wbem context
        &pNameSpace)))
    {
        goto CLEANUP;
    }
    pWbemLocator->Release();
    pWbemLocator=NULL;
    SysFreeString(bstrNameSpace);
    bstrNameSpace = NULL;

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher, 
        (void**) &pRefresher)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = pRefresher->QueryInterface(
        IID_IWbemConfigureRefresher,
        (void **)&pConfig)))
    {
        goto CLEANUP;
    }

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL, 
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;

    // Get a property handle for the VirtualBytes property.

    // Refresh the object ten times and retrieve the value.
    for(x = 0; x < 10; x++)
    {
        dwNumReturned = 0;
        dwIDProcess = 0;
        dwNumObjects = 0;

        if (FAILED (hr =pRefresher->Refresh(0L)))
        {
            goto CLEANUP;
        }

        hr = pEnum->GetObjects(0L, 
            dwNumObjects, 
            apEnumAccess, 
            &dwNumReturned);
        // If the buffer was not big enough,
        // allocate a bigger buffer and retry.
        if (hr == WBEM_E_BUFFER_TOO_SMALL 
            && dwNumReturned > dwNumObjects)
        {
            apEnumAccess = new IWbemObjectAccess*[dwNumReturned];
            if (NULL == apEnumAccess)
            {
                hr = E_OUTOFMEMORY;
                goto CLEANUP;
            }
            SecureZeroMemory(apEnumAccess,
                dwNumReturned*sizeof(IWbemObjectAccess*));
            dwNumObjects = dwNumReturned;

            if (FAILED (hr = pEnum->GetObjects(0L, 
                dwNumObjects, 
                apEnumAccess, 
                &dwNumReturned)))
            {
                goto CLEANUP;
            }
        }
        else
        {
            if (hr == WBEM_S_NO_ERROR)
            {
                hr = WBEM_E_NOT_FOUND;
                goto CLEANUP;
            }
        }

        // First time through, get the handles.
        if (0 == x)
        {
            CIMTYPE VirtualBytesType;
            CIMTYPE ProcessHandleType;
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"VirtualBytes",
                &VirtualBytesType,
                &lVirtualBytesHandle)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"IDProcess",
                &ProcessHandleType,
                &lIDProcessHandle)))
            {
                goto CLEANUP;
            }
        }
           
        for (i = 0; i < dwNumReturned; i++)
        {
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lVirtualBytesHandle,
                &dwVirtualBytes)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lIDProcessHandle,
                &dwIDProcess)))
            {
                goto CLEANUP;
            }

            wprintf(L"Process ID %lu is using %lu bytes\n",
                dwIDProcess, dwVirtualBytes);

            // Done with the object
            apEnumAccess[i]->Release();
            apEnumAccess[i] = NULL;
        }

        if (NULL != apEnumAccess)
        {
            delete [] apEnumAccess;
            apEnumAccess = NULL;
        }

       // Sleep for a second.
       Sleep(1000);
    }
    // exit loop here
    CLEANUP:

    if (NULL != bstrNameSpace)
    {
        SysFreeString(bstrNameSpace);
    }

    if (NULL != apEnumAccess)
    {
        for (i = 0; i < dwNumReturned; i++)
        {
            if (apEnumAccess[i] != NULL)
            {
                apEnumAccess[i]->Release();
                apEnumAccess[i] = NULL;
            }
        }
        delete [] apEnumAccess;
    }
    if (NULL != pWbemLocator)
    {
        pWbemLocator->Release();
    }
    if (NULL != pNameSpace)
    {
        pNameSpace->Release();
    }
    if (NULL != pEnum)
    {
        pEnum->Release();
    }
    if (NULL != pConfig)
    {
        pConfig->Release();
    }
    if (NULL != pRefresher)
    {
        pRefresher->Release();
    }

    CoUninitialize();

    if (FAILED (hr))
    {
        wprintf (L"Error status=%08x\n",hr);
    }

    return 1;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Leistungsindikatorklassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Zugreifen auf Leistungsdaten in Skripts](accessing-performance-data-in-script.md)
</dt> <dt>

[Aktualisieren von WMI-Daten in Skripts](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[WMI-Aufgaben: Leistungsüberwachung](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> <dt>

[Eigenschaftsqualifizierer für formatierte Leistungsindikatorklassen](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[WMI-Leistungsindikatortypen](wmi-performance-counter-types.md)
</dt> <dt>

[**Wmiadap.exe**](wmiadap.md)
</dt> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
