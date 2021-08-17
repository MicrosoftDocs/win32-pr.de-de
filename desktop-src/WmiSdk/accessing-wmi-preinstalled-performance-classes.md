---
description: Das WMI-Repository enthält vorinstallierte Leistungsklassen für alle Leistungsbibliotheksobjekte.
ms.assetid: 2158385f-d0dc-4102-84db-ce02d2b0ee53
ms.tgt_platform: multiple
title: Zugreifen auf vorinstallierte WMI-Leistungsklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656c3434d2f20bd73ae9ff5273f7e67439fc6caa01ac9ee5bf0283850e64b34a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131893"
---
# <a name="accessing-wmi-preinstalled-performance-classes"></a>Zugreifen auf vorinstallierte WMI-Leistungsklassen

Das WMI-Repository enthält vorinstallierte Leistungsklassen für alle Leistungsbibliotheksobjekte. Beispielsweise stellen Instanzen der Rohdaten-Leistungsklasse [**Win32 \_ PerfRawData \_ PerfProc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) Prozesse dar. Dieses Leistungsobjekt wird im Systemmonitor als Prozessobjekt angezeigt.

Die **PageFaultsPerSec-Eigenschaft** des [**Win32 \_ PerfRawData \_ PerfProc-Prozesses \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) stellt den Leistungsindikator Seitenfehler pro Sekunde für den Prozess dar. Die [**Win32 \_ PerfFormattedData-Klassen**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) enthalten die berechneten Datenwerte, die im Systemmonitor (Perfmon.exe) angezeigt werden. Der Wert der **PageFaultsPerSec-Eigenschaft** von [**Win32 \_ PerfFormattedData \_ PerfProc \_ Process entspricht**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) dem Wert, der im Systemmonitor angezeigt wird.

Verwenden Sie entweder die [COM-API für WMI](com-api-for-wmi.md) oder die [Skript-API für WMI,](scripting-api-for-wmi.md) um über die [Leistungsindikatorklassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)auf Leistungsdaten zuzugreifen. In beiden Fällen ist ein [*Aktualisierungsobjekt*](gloss-r.md) erforderlich, um jedes Datenbeispiel abzurufen. Weitere Informationen und Skriptcodebeispiele für die Verwendung von Aktualisierungen und den Zugriff auf Leistungsklassen finden Sie unter [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md). Weitere Informationen finden Sie unter [Zugreifen auf Leistungsdaten in Skript](accessing-performance-data-in-script.md).

## <a name="accessing-performance-data-from-c"></a>Zugreifen auf Leistungsdaten aus C++

Im folgenden C++-Codebeispiel wird der Leistungsindikatoranbieter verwendet, um auf vordefinierte Hochleistungsklassen zuzugreifen. Es erstellt ein Aktualisierungsobjekt und fügt der Aktualisierung ein -Objekt hinzu. Das -Objekt ist eine [**Win32 \_ PerfRawData \_ PerfProc-Prozessinstanz, \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) die die Leistung eines bestimmten Prozesses überwacht. Der Code liest nur eine Indikatoreigenschaft im Prozessobjekt, die **VirtualBytes-Eigenschaft.** Der Code erfordert die folgenden Verweise und **\# include-Anweisungen,** um ordnungsgemäß zu kompilieren.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Das folgende Verfahren veranschaulicht den Zugriff auf Daten von einem Hochleistungsanbieter in C++.

**So greifen Sie von einem Hochleistungsanbieter in C++ auf Daten zu**

1.  Stellen Sie eine Verbindung mit dem WMI-Namespace her, und legen Sie die WMI-Sicherheit fest, indem [**Sie IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) und [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)aufrufen.

    Dieser Schritt ist ein Standardschritt zum Erstellen einer beliebigen WMI-Clientanwendung. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung mit C++](creating-a-wmi-application-using-c-.md).

2.  Erstellen Sie ein Aktualisierungsobjekt mithilfe von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit CLSID \_ WbemRefresher. Fordern Sie über die [**QueryInterface-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) eine [**IWbemConfigureRefresher-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) an. Fordern Sie eine [**IWbemRefresher-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) über die **QueryInterface-Methode** an.

    Die [**IWbemRefresher-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) ist die Hauptschnittstelle für das [**WMI-Aktualisierungsobjekt.**](swbemrefreshableitem-refresher.md)

    Das folgende C++-Codebeispiel zeigt, wie [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)abgerufen wird.

    ```C++
    IWbemRefresher* pRefresher = NULL;

    HRESULT hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher,
        (void**) &pRefresher);

    IWbemConfigureRefresher* pConfig = NULL;

    pRefresher->QueryInterface( 
        IID_IWbemConfigureRefresher,
        (void**) &pConfig
      );
    ```

    

3.  Fügen Sie der Aktualisierung über einen Aufruf der [**IWbemConfigureRefresher::AddObjectByPath-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) ein Objekt hinzu.

    Wenn Sie der Aktualisierung ein Objekt hinzufügen, aktualisiert WMI das Objekt immer dann, wenn Sie die [**IWbemRefresher::Refresh-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) aufrufen. Das objekt, das Sie hinzufügen, bestimmt den Anbieter in seinen Klassenqualifizierern.

    Das folgende C++-Codebeispiel zeigt, wie [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath)aufgerufen wird.

    ```C++
    IWbemClassObject* pObj = NULL;
    IWbemServices* pNameSpace = NULL;

    // Add the instance to be refreshed.
    hr = pConfig->AddObjectByPath(
         pNameSpace,
         L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
         0L,
         NULL,
         &pObj,
         NULL
    );
    if (FAILED(hr))
    {
       cout << "Could not add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }
    ```

    

4.  Stellen Sie über [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) in der [**IWbemClassObject-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) eine Verbindung mit der [**IWbemObjectAccess-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) her, um einen schnelleren Zugriff auf das Objekt einzurichten.

    Das folgende C++-Codebeispiel zeigt, wie ein Zeiger auf das -Objekt mithilfe von [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) anstelle von [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)abgerufen wird.

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    Die [**IWbemObjectAccess-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) erhöht die Leistung, da Sie Handles für bestimmte Indikatoreigenschaften abrufen können, und sie erfordert, dass Sie das Objekt in Ihrem Code sperren und entsperren. Dies ist ein Vorgang, den [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) für jeden Eigenschaftenzugriff ausführt.

5.  Rufen Sie die Zu überprüfenden Handles der Eigenschaften ab, indem Sie Aufrufe der [**IWbemObjectAccess::GetPropertyHandle-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) verwenden.

    Eigenschaftshandles sind für alle Instanzen einer Klasse identisch. Dies bedeutet, dass sie das Eigenschaftenhandle verwenden, das Sie von einer bestimmten Instanz für alle Instanzen einer bestimmten Klasse abrufen. Sie können auch ein Handle aus einem Klassenobjekt abrufen, um Eigenschaftswerte aus einem Instanzobjekt abzurufen.

    Das folgende C++-Codebeispiel zeigt, wie ein Eigenschaftenhandle abgerufen wird.

    ```C++
        // Get a property handle for the VirtualBytes property
        long lVirtualBytesHandle = 0;
        DWORD dwVirtualBytes = 0;
        CIMTYPE variant;

        hr = pAcc->GetPropertyHandle(L"VirtualBytes",
             &variant,
             &lVirtualBytesHandle 
        );
        if (FAILED(hr))
        {
           cout << "Could not get property handle. Error code: 0x"
                << hex << hr << endl;
           return hr;
        }
    ```

    

6.  Erstellen Sie eine Programmierschleife, die die folgenden Aktionen ausführt:

    -   Aktualisieren Sie das -Objekt mit einem Aufruf von [**IWbemRefresher::Refresh,**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) indem Sie den Zeiger verwenden, der im vorherigen Aufruf von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)erstellt wurde.

        In diesem Aufruf aktualisiert die WMI-Aktualisierung das Clientobjekt mithilfe der vom Anbieter bereitgestellten Daten.

    -   Führen Sie nach Bedarf eine beliebige Aktion für das Objekt aus, z. B. das Abrufen eines Eigenschaftsnamens, Datentyps oder Werts.

        Sie können über das zuvor abgerufene Eigenschaftenhandle auf die Eigenschaft zugreifen. Aufgrund des [**Refresh-Aufrufs**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) aktualisiert WMI die -Eigenschaft jedes Mal durch die -Schleife.

Im folgenden C++-Beispiel wird die Verwendung der WMI-Api für hohe Leistung veranschaulicht.


```C++
// Get the local locator object
IWbemServices* pNameSpace = NULL;
IWbemLocator* pWbemLocator = NULL;
CIMTYPE variant;
VARIANT VT;

CoCreateInstance( CLSID_WbemLocator, NULL,
    CLSCTX_INPROC_SERVER, IID_IWbemLocator, (void**) &pWbemLocator
);

// Connect to the desired namespace
BSTR bstrNameSpace = SysAllocString( L"\\\\.\\root\\cimv2" );

HRESULT hr = WBEM_S_NO_ERROR;

hr = pWbemLocator->ConnectServer(
     bstrNameSpace,      // Namespace name
     NULL,               // User name
     NULL,               // Password
     NULL,               // Locale
     0L,                 // Security flags
     NULL,               // Authority
     NULL,               // Wbem context
     &pNameSpace         // Namespace
);

if ( SUCCEEDED( hr ) )
{
    // Set namespace security.
    IUnknown* pUnk = NULL;
    pNameSpace->QueryInterface( IID_IUnknown, (void**) &pUnk );

    hr = CoSetProxyBlanket(
         pNameSpace, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }

    hr = CoSetProxyBlanket(pUnk, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pUnk->Release();
       return hr;
    }

    // Clean up the IUnknown.
    pUnk->Release();

    IWbemRefresher* pRefresher = NULL;
    IWbemConfigureRefresher* pConfig = NULL;

    // Create a WMI Refresher and get a pointer to the
    // IWbemConfigureRefresher interface.
    CoCreateInstance(CLSID_WbemRefresher, 
                     NULL,
                     CLSCTX_INPROC_SERVER, 
                     IID_IWbemRefresher, 
                     (void**) &pRefresher 
    );
    
    pRefresher->QueryInterface(IID_IWbemConfigureRefresher,
                               (void**) &pConfig );

    IWbemClassObject* pObj = NULL;

    // Add the instance to be refreshed.
    pConfig->AddObjectByPath(
       pNameSpace,
       L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
       0L,
       NULL,
       &pObj,
       NULL 
    );
    if (FAILED(hr))
    {
       cout << "Cannot add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       
       return hr;
    }

    // For quick property retrieval, use IWbemObjectAccess.
    IWbemObjectAccess* pAcc = NULL;
    pObj->QueryInterface(IID_IWbemObjectAccess, 
                         (void**) &pAcc );

    // This is not required.
    pObj->Release();

    // Get a property handle for the VirtualBytes property.
    long lVirtualBytesHandle = 0;
    DWORD dwVirtualBytes = 0;

    pAcc->GetPropertyHandle(L"VirtualBytes", 
                            &variant, 
                            &lVirtualBytesHandle );

    // Refresh the object ten times and retrieve the value.
    for( int x = 0; x < 10; x++ )
    {
        pRefresher->Refresh( 0L );
        pAcc->ReadDWORD( lVirtualBytesHandle, &dwVirtualBytes );
        printf( "Process is using %lu bytes\n", dwVirtualBytes );
        // Sleep for a second.
        Sleep( 1000 );
    }
    // Clean up all the objects.
    pAcc->Release();
    // Done with these too.
    pConfig->Release();
    pRefresher->Release();
    pNameSpace->Release();
}
SysFreeString( bstrNameSpace );
pWbemLocator->Release();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Leistungsindikatorklassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[WMI-Aufgaben: Leistungsüberwachung](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
