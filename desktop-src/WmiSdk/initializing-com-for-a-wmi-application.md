---
description: Der erste Schritt beim Herstellen einer Verbindung mit WMI ist das Einrichten der COM-Aufrufe von CoInitializeEx und CoInitializeSecurity.
ms.assetid: c9291aa7-702c-4752-8bd0-97d7a6e6dd54
ms.tgt_platform: multiple
title: Initialisieren von COM für eine WMI-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723188602e440cd3ba49d78d8efb3c28ddae30f35dd0d4361a4fdb5ced026ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318574"
---
# <a name="initializing-com-for-a-wmi-application"></a>Initialisieren von COM für eine WMI-Anwendung

Der erste Schritt beim Herstellen einer Verbindung mit WMI ist das Einrichten der COM-Aufrufe von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

Die Codebeispiele in diesem Thema erfordern die folgenden Verweise und \# Include-Anweisungen, um ordnungsgemäß zu kompilieren.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Im folgenden Verfahren wird beschrieben, wie COM aus einer Clientanwendung initialisiert wird.

**So initialisieren Sie COM aus einer Clientanwendung**

1.  Initialisieren Sie COM mit einem Aufruf von [**CoInitializeEx.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)

    Das [**Aufrufen von CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) ist eine Standardprozedur zum Einrichten einer COM-Schnittstelle. Daher ist es für WMI nicht erforderlich, zusätzliche Prozeduren beim Aufrufen von **CoInitializeEx zu beachten.** Weitere Informationen finden Sie unter [COM](../com/component-object-model--com--portal.md).

    Im folgenden Codebeispiel wird beschrieben, wie [**CoInitializeEx aufruft.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  Legen Sie die allgemeinen COM-Sicherheitsebenen mit einem Aufruf der [**CoInitializeSecurity-Schnittstelle**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) fest.

    [**CoInitializeSecurity ist**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) eine Standardfunktion, die Sie beim Einrichten einer COM-Schnittstelle für einen Prozess aufrufen müssen. Rufen **Sie CoInitializeSecurity auf,** wenn Sie die Standardsicherheitseinstellungen für die Authentifizierung, den Identitätswechsel oder den Authentifizierungsdienst für einen gesamten Prozess festlegen möchten. Weitere Informationen finden Sie unter [Setting Client Application Process Security](setting-client-application-process-security.md). Wenn Sie die Sicherheit für einen bestimmten Proxy festlegen oder ändern möchten, müssen Sie [**CoSetProxyBlanket aufrufen.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) Verwenden **Sie CoSetProxyBlanket** immer dann, wenn Sie die COM-Sicherheit festlegen oder ändern müssen, wenn sie in einem anderen Prozess ausgeführt wird, bei dem Sie die Standardsicherheitseinstellungen für Authentifizierung, Identitätswechsel oder Authentifizierungsdienst nicht steuern können. Weitere Informationen finden Sie unter Festlegen der Sicherheitsebenen für [eine WMI-Verbindung](setting-the-security-levels-on-a-wmi-connection.md) und [Festlegen der Sicherheit für IWbemServices und andere Proxys.](setting-the-security-on-iwbemservices-and-other-proxies.md)

    WMI hat mehrere Sicherheitsprobleme, die Sie beim Programmieren einer WMI-Clientanwendung beachten sollten. Weitere Informationen finden Sie unter [Setting Client Application Process Security](setting-client-application-process-security.md).

    Im folgenden Codebeispiel wird beschrieben, wie [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) zum Festlegen der COM-Sicherheit für den Prozess aufruft.

    ```C++
    hr =  CoInitializeSecurity(
        NULL,                        // Security descriptor    
        -1,                          // COM negotiates authentication service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication level for proxies
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation level for proxies
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities of the client or server
        NULL);                       // Reserved

    if (FAILED(hr))
    {
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       CoUninitialize();
       return hr;                  // Program has failed.
    }
    ```

    

Nachdem Sie COM initialisiert haben, besteht der nächste Schritt im Erstellen einer Verbindung mit einem WMI-Namespace. Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace.](creating-a-connection-to-a-wmi-namespace.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer WMI-Anwendung mit C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
