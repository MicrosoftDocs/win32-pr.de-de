---
description: Der erste Schritt beim Herstellen einer Verbindung mit WMI ist das Einrichten der com-Aufrufe an CoInitializeEx und CoInitializeSecurity.
ms.assetid: c9291aa7-702c-4752-8bd0-97d7a6e6dd54
ms.tgt_platform: multiple
title: Initialisieren von com für eine WMI-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6c2e590ddb64914f5aab723a56dee2385a49bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960797"
---
# <a name="initializing-com-for-a-wmi-application"></a>Initialisieren von com für eine WMI-Anwendung

Der erste Schritt beim Herstellen einer Verbindung mit WMI ist das Einrichten der com-Aufrufe an [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

Die Codebeispiele in diesem Thema erfordern die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Im folgenden Verfahren wird beschrieben, wie com aus einer Client Anwendung initialisiert wird.

**So initialisieren Sie com über eine Client Anwendung**

1.  Initialisieren Sie com mit einem Aufrufen von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Der Aufruf von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) ist ein Standardverfahren zum Einrichten einer COM-Schnittstelle. Daher ist es für WMI nicht erforderlich, dass Sie beim Aufrufen von **CoInitializeEx** weitere Prozeduren beachten. Weitere Informationen finden Sie unter [com](../com/component-object-model--com--portal.md).

    Im folgenden Codebeispiel wird beschrieben, wie [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)aufgerufen wird.

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  Legen Sie die allgemeinen com-Sicherheitsstufen mit einem aufrufswert für die [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) -Schnittstelle fest.

    [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ist eine Standardfunktion, die beim Einrichten einer COM-Schnittstelle für einen Prozess aufgerufen werden muss. **CoInitializeSecurity** wird aufgerufen, wenn Sie die Standard Sicherheitseinstellungen für die Authentifizierung, den Identitätswechsel oder den Authentifizierungsdienst für einen gesamten Prozess festlegen möchten. Weitere Informationen finden Sie unter [Festlegen der Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md). Wenn Sie die Sicherheit für einen bestimmten Proxy festlegen oder ändern möchten, müssen Sie [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)aufrufen. Verwenden Sie **CoSetProxyBlanket** , wenn Sie com-Sicherheit festlegen oder ändern müssen, wenn Sie in einem anderen Prozess ausgeführt werden, in dem Sie die Standard Sicherheitseinstellungen für die Authentifizierung, den Identitätswechsel oder den Authentifizierungsdienst nicht steuern können. Weitere Informationen finden Sie unter [Festlegen der Sicherheitsstufen für eine WMI-Verbindung](setting-the-security-levels-on-a-wmi-connection.md) und [Festlegen der Sicherheit für IWbemServices und andere](setting-the-security-on-iwbemservices-and-other-proxies.md)Proxys.

    WMI weist mehrere Sicherheitsprobleme auf, die Sie beim Programmieren einer WMI-Client Anwendung beachten sollten. Weitere Informationen finden Sie unter [Festlegen der Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md).

    Im folgenden Codebeispiel wird beschrieben, wie [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufgerufen wird, um die com-Sicherheit für den Prozess festzulegen.

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

    

Nachdem Sie com initialisiert haben, besteht der nächste Schritt im Erstellen einer Verbindung mit einem WMI-Namespace. Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace](creating-a-connection-to-a-wmi-namespace.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer WMI-Anwendung mithilfe von C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
