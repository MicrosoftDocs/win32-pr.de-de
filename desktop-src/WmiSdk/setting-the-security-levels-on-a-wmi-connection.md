---
description: Nachdem Sie einen Zeiger auf einen IWbemServices-Proxy abgerufen haben, müssen Sie die Sicherheit des Proxys für den Zugriff auf WMI über den Proxy festlegen.
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: Festlegen der Sicherheitsstufen für eine WMI-Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc58b4bbbe1a01d927d8f5977c21003cdae2e315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350933"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a>Festlegen der Sicherheitsstufen für eine WMI-Verbindung

Nachdem Sie einen Zeiger auf einen [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Proxy abgerufen haben, müssen Sie die Sicherheit des Proxys für den Zugriff auf WMI über den Proxy festlegen. Sie müssen die Sicherheit festlegen, da der **IWbemServices** -Proxy Zugriff auf ein Out-of-Process-Objekt gewährt. Im Allgemeinen lässt die com-Sicherheit nicht zu, dass ein Prozess auf einen anderen Prozess zugreift, wenn Sie die richtigen Sicherheitseigenschaften nicht festlegen. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für IWbemServices und andere](setting-the-security-on-iwbemservices-and-other-proxies.md)Proxys. Verbindungen mit unterschiedlichen Betriebssystemen erfordern unterschiedliche Authentifizierungs Stufen und Identitätswechsel. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).

Die Codebeispiele in diesem Thema erfordern die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Im folgenden Verfahren wird beschrieben, wie die Sicherheitsstufen für eine WMI-Verbindung festgelegt werden.

**So legen Sie die Sicherheitsstufen für eine WMI-Verbindung fest**

-   Legen Sie die Sicherheitsstufen des [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Proxys mit einem Aufrufen von [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)fest.

    Im folgenden Codebeispiel wird eine gängige Methode zum Aufrufen von [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)beschrieben.

    ```C++
        HRESULT hres;
        IWbemServices *pSvc = 0;
        IWbemLocator *pLoc = 0;

        // Set the proxy so that impersonation of the client occurs.
        hres = CoSetProxyBlanket(pSvc,
           RPC_C_AUTHN_WINNT,
           RPC_C_AUTHZ_NONE,
           NULL,
           RPC_C_AUTHN_LEVEL_CALL,
           RPC_C_IMP_LEVEL_IMPERSONATE,
           NULL,
           EOAC_NONE
        );

        if (FAILED(hres))
        {
            cout << "Could not set proxy blanket. Error code = 0x" 
                 << hex << hres << endl;
           pSvc->Release();
          pLoc->Release();     
            CoUninitialize();
            return hres;      // Program has failed.
        }
    ```

    

Nachdem Sie die Sicherheitsstufen für Ihren [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Zeiger festgelegt haben, können Sie auf die verschiedenen Funktionen von WMI zugreifen. Nachdem Sie die Verwendung von WMI abgeschlossen haben, müssen Sie die Anwendung Herunterfahren. Weitere Informationen finden Sie unter [Bereinigen und Herunterfahren einer WMI-Anwendung](cleaning-up-and-shutting-down-a-wmi-application.md).

 

 
