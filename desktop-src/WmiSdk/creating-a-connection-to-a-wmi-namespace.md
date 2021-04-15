---
description: 'Nachdem Sie die Standard Aufrufe von com festgelegt haben, müssen Sie mithilfe eines Aufrufs der IWbemLocator:: ConnectServer-Methode eine Verbindung mit WMI herstellen.'
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: Erstellen einer Verbindung mit einem WMI-Namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce0e1caeef15709742704570c008012feeaf8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485742"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a>Erstellen einer Verbindung mit einem WMI-Namespace

Nachdem Sie die Standard Aufrufe von com festgelegt haben, müssen Sie mithilfe eines Aufrufs der [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) -Methode eine Verbindung mit WMI herstellen. Die **ConnectServer** -Methode gibt einen Proxy einer [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle zurück. Mithilfe von **IWbemServices** können Sie auf die verschiedenen Funktionen von WMI zugreifen.

Die Codebeispiele in diesem Thema erfordern die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Im folgenden Verfahren wird beschrieben, wie eine Verbindung mit einem WMI-Namespace erstellt wird.

**So erstellen Sie eine Verbindung mit einem WMI-Namespace**

-   Initialisieren Sie die [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) -Schnittstelle durch einen Aufrufen von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Für WMI ist es nicht erforderlich, dass Sie beim Aufrufen von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) für [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)zusätzliche Prozeduren ausführen.

    Im folgenden Codebeispiel wird die Initialisierung von [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)beschrieben.

    ```C++
        IWbemLocator *pLoc = 0;
        HRESULT hr;

        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
            CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
     
        if (FAILED(hr))
        {
            cout << "Failed to create IWbemLocator object. Err code = 0x"
                 << hex << hr << endl;
            CoUninitialize();
            return hr;     // Program has failed.
        }
    ```

    

    -   Stellen Sie eine Verbindung mit WMI her, indem Sie die Methode [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) abrufen.

        Die [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) -Methode gibt einen Proxy an eine [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle zurück, die verwendet, um auf den lokalen WMI-Namespace zuzugreifen, der in dem Aufrufen von **ConnectServer** angegeben ist.

        Im folgenden Codebeispiel wird das Abrufen von [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)beschrieben.

        ```C++
        IWbemServices *pSvc = 0;

            // Connect to the root\default namespace with the current user.
            hr = pLoc->ConnectServer(
                    BSTR(L"ROOT\\DEFAULT"),  //namespace
                    NULL,       // User name 
                    NULL,       // User password
                    0,         // Locale 
                    NULL,     // Security flags
                    0,         // Authority 
                    0,        // Context object 
                    &pSvc);   // IWbemServices proxy


            if (FAILED(hr))
            {
                cout << "Could not connect. Error code = 0x" 
                     << hex << hr << endl;
                pLoc->Release();
                CoUninitialize();
                return hr;      // Program has failed.
            }

            cout << "Connected to WMI" << endl;
        ```

        

Nachdem Sie einen Zeiger auf den [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Proxy erhalten haben, müssen Sie die Sicherheit des Proxys für den Zugriff auf WMI festlegen. Weitere Informationen finden Sie unter [Festlegen der Sicherheitsstufen für eine WMI-Verbindung](setting-the-security-levels-on-a-wmi-connection.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer WMI-Anwendung mithilfe von C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[IPv6-und IPv4-Unterstützung in WMI](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
