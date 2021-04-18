---
description: Bei der WMI-Hochleistungs-API handelt es sich um eine Reihe von Schnittstellen, die Daten aus Leistungs Leistungsdaten Klassen abrufen.
ms.assetid: ee0a2ead-f53a-4651-a287-04a62eba3f84
ms.tgt_platform: multiple
title: Zugreifen auf Leistungsdaten in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b076e1ab15b934f347ee491711d7d3d1b8fbbe0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352780"
---
# <a name="accessing-performance-data-in-c"></a>Zugreifen auf Leistungsdaten in C++

Bei der WMI-Hochleistungs-API handelt es sich um eine Reihe von Schnittstellen, die Daten aus [Leistungs Leistungsdaten Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)abrufen. Diese Schnittstellen erfordern die Verwendung [*eines Aktualisierungs Objekts,*](gloss-r.md) um die Samplingrate zu erhöhen. Weitere Informationen zur Verwendung des Aktualisierungs Objekts bei der Skripterstellung finden Sie unter [zugreifen auf Leistungsdaten in Skripts](accessing-performance-data-in-script.md) und [WMI-Tasks: Leistungsüberwachung](wmi-tasks--performance-monitoring.md).

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Aktualisieren von Leistungsdaten](#refreshing-performance-data)
-   [Hinzufügen von Enumeratoren zum WMI-Aktualisierungs Programm](#adding-enumerators-to-the-wmi-refresher)
-   [Beispiel](#example)
-   [Zugehörige Themen](#related-topics)

## <a name="refreshing-performance-data"></a>Aktualisieren von Leistungsdaten

Ein Aktualisierungs Objekt erhöht die Datenanbieter-und Client Leistung, indem Daten abgerufen werden, ohne dass Prozess Grenzen überschritten werden. Wenn sich sowohl der Client als auch der Server auf demselben Computer befinden, lädt ein Aktualisierungs Programm den Hochleistungs Anbieter Prozess seitig in den Client und kopiert Daten direkt von Anbieter Objekten in Client Objekte. Wenn sich der Client und der Server auf unterschiedlichen Computern befinden, steigert das Aktualisierungs Programm die Leistung, indem Objekte auf dem Remote Computer zwischengespeichert werden und minimale Datasets an den Client übertragen werden.

Ein Aktualisierungs Programm ist ebenfalls:

-   Verbindet einen Client automatisch erneut mit einem WMI-Remote Dienst, wenn ein Netzwerkfehler auftritt oder der Remote Computer neu gestartet wird.

    Standardmäßig versucht ein Aktualisierungs Programm, eine Verbindung zwischen der Anwendung und dem relevanten Hochleistungs Anbieter herzustellen, wenn eine Remote Verbindung zwischen den beiden Computern fehlschlägt. Um die erneute Verbindung zu verhindern, übergeben Sie im [**Aktualisierungs**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) Methoden aufrufsbefehl das **WBEM- \_ Flag \_ aktualisieren \_ No \_ Auto \_ Reconnect** . Skript Clients müssen die Eigenschaft " [**Swap. autoreconnetct**](swbemrefresher-autoreconnect.md) " auf " **false**" festlegen.

-   Lädt mehrere-Objekte und Enumeratoren, die von demselben oder unterschiedlichen Anbietern bereitgestellt werden.

    Ermöglicht es Ihnen, mehrere Objekte, Enumeratoren oder beides einem Aktualisierungs Programm hinzuzufügen.

-   Listet-Objekte auf.

    Wie bei anderen Anbietern kann ein Hochleistungs Anbieter Objekte aufzählen.

Nachdem Sie den Hochleistungs Client geschrieben haben, möchten Sie möglicherweise die Reaktionszeit verbessern. Da die [**iwbefibjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) -Schnittstelle für die Geschwindigkeit optimiert ist, ist die Schnittstelle nicht intrinsisch Thread sicher. Daher können Sie während eines Aktualisierungs Vorgangs nicht auf das aktualisierbare Objekt oder die Aufzählung zugreifen. Verwenden Sie zum Schutz von Objekten während der **iwbemubjectaccess** -Methodenaufrufe die Methoden [**iwbemubjectaccess:: Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) und [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) . Synchronisieren Sie Ihre Threads, um die Leistung zu verbessern, sodass Sie keine einzelnen Threads Sperren müssen. Das Reduzieren von Threads und das Synchronisieren von Gruppen von Objekten für Aktualisierungs Vorgänge bietet die beste Gesamtleistung.

## <a name="adding-enumerators-to-the-wmi-refresher"></a>Hinzufügen von Enumeratoren zum WMI-Aktualisierungs Programm

Die Anzahl der Instanzen und Daten in jeder Instanz werden aktualisiert, indem dem Aktualisierungs Programm ein Enumerator hinzugefügt wird, sodass jeder [**callbemrefresh Sher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) -Befehl eine komplette Enumeration ergibt.

Im folgenden C++-Codebeispiel werden die folgenden Verweise und \# include-Anweisungen für die ordnungsgemäße Kompilierung benötigt.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Im folgenden Verfahren wird gezeigt, wie ein Enumerator zu einem Aktualisierungs Programm hinzugefügt wird.

**So fügen Sie einem Aktualisierungs Programm einen Enumerator hinzu**

1.  Rufen Sie die [**iwbemconfigurerefresher:: AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) -Methode auf, indem Sie den Pfad zum aktualisierbaren Objekt und die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle verwenden.

    Das Aktualisierungs Programm gibt einen Zeiger auf eine [**iwbemhiperfenum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) -Schnittstelle zurück. Sie können die **iwbemhiperferum** -Schnittstelle verwenden, um auf die Objekte in der-Enumeration zuzugreifen.

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

    

2.  Erstellen Sie eine-Schleife, die die folgenden Aktionen ausführt:

    -   Aktualisiert das-Objekt mithilfe eines Aufrufes von [**iwbemrefresh Sher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).
    -   Stellt ein Array von [**iwbearbjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) -Schnittstellen Zeigern für die [**iwbemhiperferum:: GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) -Methode bereit.
    -   Greift auf die Eigenschaften des Enumerators zu, indem die [**iwbemubjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) -Methoden verwendet werden, die an [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects)übermittelt werden.

        Ein Eigenschaften Handle kann an jede [**iwbemubjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) -Instanz übermittelt werden, um den aktualisierten Wert abzurufen. Der Client muss [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufrufen, um die von [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects)zurückgegebenen **iwbemubjectaccess** -Zeiger freizugeben.

## <a name="example"></a>Beispiel

Im folgenden C++-Codebeispiel wird eine Hochleistungs Klasse aufgelistet, bei der der Client ein Eigenschaften Handle aus dem ersten-Objekt abruft und das Handle für den Rest des Aktualisierungs Vorgangs erneut verwendet. Jeder Aufrufe der [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) -Methode aktualisiert die Anzahl von Instanzen und die Instanzdaten.


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

[Leistungs Leistungsdaten-Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Zugreifen auf Leistungsdaten im Skript](accessing-performance-data-in-script.md)
</dt> <dt>

[Aktualisieren von WMI-Daten in Skripts](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[WMI-Tasks: Leistungsüberwachung](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> <dt>

[Eigenschafts Qualifizierer für formatierte Leistungs Objektklassen](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[WMI-Leistungsdaten Typen](wmi-performance-counter-types.md)
</dt> <dt>

[**Wmiadap.exe**](wmiadap.md)
</dt> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
