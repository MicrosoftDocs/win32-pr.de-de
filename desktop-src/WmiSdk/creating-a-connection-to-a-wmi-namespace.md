---
description: Nachdem Sie die Standardaufrufe für COM festgelegt haben, müssen Sie über einen Aufruf der IWbemLocator::ConnectServer-Methode eine Verbindung mit WMI herstellen.
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: Erstellen einer Verbindung mit einem WMI-Namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2587024d7f581cd28a8fdaf339db9567b17c509599c01aca0599b701186fb786
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412140"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a>Erstellen einer Verbindung mit einem WMI-Namespace

Nachdem Sie die Standardaufrufe für COM festgelegt haben, müssen Sie über einen Aufruf der [**IWbemLocator::ConnectServer-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) eine Verbindung mit WMI herstellen. Die **ConnectServer-Methode** gibt einen Proxy einer [**IWbemServices-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) zurück. Über **IWbemServices können** Sie auf die verschiedenen Funktionen von WMI zugreifen.

Die Codebeispiele in diesem Thema erfordern die folgenden Verweise und \# Include-Anweisungen, um ordnungsgemäß zu kompilieren.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Im folgenden Verfahren wird beschrieben, wie Eine Verbindung mit einem WMI-Namespace erstellt wird.

**So erstellen Sie eine Verbindung mit einem WMI-Namespace**

-   Initialisieren [**Sie die IWbemLocator-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) über einen Aufruf von [**CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)

    WMI erfordert keine zusätzlichen Prozeduren beim Aufrufen von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in [**IWbemLocator.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)

    Im folgenden Codebeispiel wird beschrieben, wie [**IWbemLocator initialisiert wird.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)

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

    

    -   Verbinden über einen Aufruf der [**IWbemLocator::ConnectServer-Methode an WMI.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)

        Die [**ConnectServer-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) gibt einen Proxy an eine [**IWbemServices-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) zurück, die für den Zugriff auf den lokalen oder Remote-WMI-Namespace verwendet, der im Aufruf von **ConnectServer angegeben ist.**

        Im folgenden Codebeispiel wird das Aufrufen von [**ConnectServer beschrieben.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)

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

        

Nachdem Sie einen Zeiger auf den [**IWbemServices-Proxy**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) erhalten haben, müssen Sie die Sicherheit für den Proxy für den Zugriff auf WMI festlegen. Weitere Informationen finden Sie unter [Festlegen der Sicherheitsebenen für eine WMI-Verbindung.](setting-the-security-levels-on-a-wmi-connection.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer WMI-Anwendung mit C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[IPv6- und IPv4-Unterstützung in WMI](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
