---
description: Das WMI-Repository enthält vorinstallierte Leistungsklassen für alle Leistungs Bibliotheksobjekte.
ms.assetid: 2158385f-d0dc-4102-84db-ce02d2b0ee53
ms.tgt_platform: multiple
title: Zugreifen auf vorinstallierte WMI-Leistungsklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265f9b4008913a463545ed03cd6f1025b58ef5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347623"
---
# <a name="accessing-wmi-preinstalled-performance-classes"></a>Zugreifen auf vorinstallierte WMI-Leistungsklassen

Das WMI-Repository enthält vorinstallierte Leistungsklassen für alle Leistungs Bibliotheksobjekte. Beispielsweise stellen Instanzen der RAW-Daten Leistungsklasse [**Win32 \_ perfrawdata \_ perfproc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) Prozesse dar. Dieses Leistungs Objekt ist im System Monitor als Prozess Objekt sichtbar.

Die **pagefehlerspersec** -Eigenschaft des [**Win32 \_ perfrawdata \_ perfproc- \_ Prozesses**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) stellt den Leistungs Leistungs Monitor "Seiten Fehler pro Sekunde" für den Prozess dar. Die [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Klassen enthalten die berechneten Datenwerte, die im System Monitor (Perfmon.exe) angezeigt werden. Der Wert der **pagefehlerspersec** -Eigenschaft des [**Win32 \_ perfformatteddata \_ perfproc- \_ Prozesses**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) entspricht dem, wenn er im System Monitor angezeigt wird.

Verwenden Sie entweder die [com-API für WMI](com-api-for-wmi.md) oder die [Skript-API für WMI](scripting-api-for-wmi.md) , um über die [Leistungs Leistungsdaten Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)auf Leistungsdaten zuzugreifen. In beiden Fällen ist [*ein*](gloss-r.md) Aktualisierungs Objekt zum Abrufen der einzelnen Daten Stichproben erforderlich. Weitere Informationen und Skriptcode Beispiele für die Verwendung von aktualisierungsproblegern und den Zugriff auf Leistungsklassen finden Sie unter [WMI-Tasks: Leistungsüberwachung](wmi-tasks--performance-monitoring.md). Weitere Informationen finden Sie unter [zugreifen auf Leistungsdaten im Skript](accessing-performance-data-in-script.md).

## <a name="accessing-performance-data-from-c"></a>Zugreifen auf Leistungsdaten von C++

Im folgenden C++-Codebeispiel wird der Leistungsindikatorenanbieter verwendet, um auf vordefinierte hochleistungsklassen zuzugreifen. Er erstellt ein Aktualisierungs Objekt und fügt dem Aktualisierungs Programm ein Objekt hinzu. Das-Objekt ist eine [**Win32 \_ perfrawdata \_ perfproc- \_ Prozess**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) Instanz, die die Leistung eines bestimmten Prozesses überwacht. Der Code liest nur eine Counter-Eigenschaft im Process-Objekt, der **virtualbytes** -Eigenschaft. Der Code erfordert, dass die folgenden Verweise und **\# include** -Anweisungen ordnungsgemäß kompiliert werden.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Im folgenden Verfahren wird gezeigt, wie Sie in C++ auf Daten von einem Hochleistungs Anbieter zugreifen können.

**So greifen Sie auf Daten eines Hochleistungs Anbieters in C++ zu**

1.  Stellen Sie eine Verbindung mit dem WMI-Namespace her, und legen Sie die WMI-Sicherheit mithilfe eines Aufrufes von [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) und [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)fest.

    Dieser Schritt ist ein Standard Schritt zum Erstellen einer beliebigen WMI-Client Anwendung. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung mithilfe von C++](creating-a-wmi-application-using-c-.md).

2.  Erstellen Sie ein Aktualisierungs Objekt, indem Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit CLSID \_ wbemaktualisierungs Programm verwenden. Fordern Sie mithilfe der [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode eine [**iwbemconfigurerefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) -Schnittstelle an. Fordern Sie mithilfe der **QueryInterface** -Methode eine [**iwbemaktualisierungs**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) -Schnittstelle an.

    Die [**iwbemfreshsher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) -Schnittstelle ist die Hauptschnittstelle für das [**WMI-**](swbemrefreshableitem-refresher.md) Aktualisierungs Objekt.

    Im folgenden C++-Codebeispiel wird gezeigt, wie [**iwbemconfigurerefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)abgerufen wird.

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

    

3.  Fügen Sie dem Aktualisierungs Programm ein Objekt hinzu, indem Sie die [**iwbemconfigurerefresher:: addobjectbypath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) -Methode aufrufen.

    Wenn Sie dem Aktualisierungs Programm ein Objekt hinzufügen, aktualisiert WMI das Objekt, wenn Sie die [**iwbemrefresh Sher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) -Methode aufruft. Das Objekt, das Sie hinzufügen, bestimmt den Anbieter in seinen Klassen Qualifizierern.

    Im folgenden C++-Codebeispiel wird gezeigt, wie [**addobjectbypath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath)aufgerufen wird.

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

    

4.  Um einen schnelleren Zugriff auf das Objekt einzurichten, stellen Sie über [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf der [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Schnittstelle eine Verbindung mit der [**iwbewbjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) -Schnittstelle her.

    Im folgenden C++-Codebeispiel wird gezeigt, wie ein Zeiger auf das-Objekt mithilfe von [**iwbemubjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) anstelle von [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)abgerufen wird.

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    Die [**iwbemubjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) -Schnittstelle steigert die Leistung, da Sie Handles für bestimmte Leistungstest Eigenschaften abrufen können. Außerdem müssen Sie das Objekt im Code Sperren und entsperren. dabei handelt es sich um einen Vorgang, den [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) für jeden Eigenschaften Zugriff ausführt.

5.  Rufen Sie die Handles der zu überprüfenden Eigenschaften mithilfe von Aufrufen der [**iwbewbjectaccess:: getpropertyhandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) -Methode ab.

    Eigenschaften Handles sind für alle Instanzen einer Klasse identisch. Dies bedeutet, dass Sie das Eigenschaften Handle verwenden, das Sie von einer bestimmten Instanz für alle Instanzen einer bestimmten Klasse abrufen. Sie können auch ein Handle von einem Klassenobjekt abrufen, um Eigenschaftswerte aus einem Instanzobjekt abzurufen.

    Im folgenden C++-Codebeispiel wird gezeigt, wie ein Eigenschaften Handle abgerufen wird.

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

    

6.  Erstellen Sie eine Programmier Schleife, die die folgenden Aktionen ausführt:

    -   Aktualisieren Sie das Objekt mit einem [**callbemrefresh Sher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) -Befehl, indem Sie den Zeiger verwenden, der im vorherigen Aufrufen von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)erstellt wurde.

        In diesem-Befehl aktualisiert das WMI-Aktualisierungs Programm das-Client Objekt mithilfe von Daten, die der Anbieter bereitstellt.

    -   Führen Sie für das Objekt gegebenenfalls eine beliebige Aktion aus, z. b. das Abrufen eines Eigenschafts namens, eines Datentyps oder eines Werts.

        Sie können über das zuvor erhaltene Eigenschaften Handle auf die-Eigenschaft zugreifen. Aufgrund des [**Aktualisierungs**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) Aufrufes aktualisiert WMI die-Eigenschaft jedes Mal durch die-Schleife.

Im folgenden Beispiel wird gezeigt, wie die Hochleistungs-API von WMI verwendet wird.


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

[Leistungs Leistungsdaten-Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[WMI-Tasks: Leistungsüberwachung](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
