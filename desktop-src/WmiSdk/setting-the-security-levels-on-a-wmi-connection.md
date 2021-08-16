---
description: Nachdem Sie einen Zeiger auf einen IWbemServices-Proxy abgerufen haben, müssen Sie die Sicherheit auf dem Proxy für den Zugriff auf WMI über den Proxy festlegen.
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: Festlegen der Sicherheitsebenen für eine WMI-Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c2c4a492d4b40410b42fd9a94f22d346617a84d3baaa0679db325452a69c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315324"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a>Festlegen der Sicherheitsebenen für eine WMI-Verbindung

Nachdem Sie einen Zeiger auf einen [**IWbemServices-Proxy**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) abgerufen haben, müssen Sie die Sicherheit auf dem Proxy für den Zugriff auf WMI über den Proxy festlegen. Sie müssen die Sicherheit festlegen, da der **IWbemServices-Proxy** Zugriff auf ein Out-of-Process-Objekt gewährt. Im Allgemeinen lässt die COM-Sicherheit nicht zu, dass ein Prozess auf einen anderen Prozess zutritt, wenn Sie nicht die richtigen Sicherheitseigenschaften festlegen. Weitere Informationen finden Sie unter Setting the Security on IWbemServices and Other Proxys (Festlegen der Sicherheit für [IWbemServices und andere Proxys).](setting-the-security-on-iwbemservices-and-other-proxies.md) Verbindungen mit verschiedenen Betriebssystemen erfordern unterschiedliche Authentifizierungs- und Identitätswechselebenen. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)

Die Codebeispiele in diesem Thema erfordern die folgenden Verweise und \# Include-Anweisungen, um ordnungsgemäß zu kompilieren.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Im folgenden Verfahren wird beschrieben, wie die Sicherheitsebenen für eine WMI-Verbindung festgelegt werden.

**So legen Sie die Sicherheitsebenen für eine WMI-Verbindung fest**

-   Legen Sie die Sicherheitsebenen für den [**IWbemServices-Proxy**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) mit einem Aufruf von [**CoSetProxyBlanket fest.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)

    Im folgenden Codebeispiel wird eine gängige Methode zum Aufrufen von [**CoSetProxyBlanket beschrieben.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)

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

    

Nachdem Sie die Sicherheitsebenen für Ihren [**IWbemServices-Zeiger**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) festgelegt haben, können Sie auf die verschiedenen Funktionen von WMI zugreifen. Nachdem Sie die Verwendung von WMI abgeschlossen haben, müssen Sie Die Anwendung herunterfahren. Weitere Informationen finden Sie unter [Bereinigen und Herunterfahren einer WMI-Anwendung.](cleaning-up-and-shutting-down-a-wmi-application.md)

 

 
