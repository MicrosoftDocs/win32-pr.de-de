---
title: Schreiben eines authentifizierten SSPI-Servers
description: Vor der Authentifizierung zwischen den Client-und Serverprogrammen muss der Server seine Authentifizierungsinformationen registrieren.
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Schreiben eines authentifizierten SSPI-Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b1cb06cfc626bc8130f3c4b0cee0a7b6d7893e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036913"
---
# <a name="writing-an-authenticated-sspi-server"></a>Schreiben eines authentifizierten SSPI-Servers

Vor der Authentifizierung zwischen den Client-und Serverprogrammen muss der Server seine Authentifizierungsinformationen registrieren. Insbesondere muss der Server seinen Prinzipal Namen registrieren und den Authentifizierungsdienst angeben, den er verwendet. Weitere Informationen zu Prinzipal Namen finden Sie unter [Prinzipal Namen](principal-names.md). Weitere Informationen zu Authentifizierungsdiensten finden Sie unter [Authentifizierungsdienste](authentication-services.md).

Zum Registrieren der Authentifizierungsinformationen wird von den Servern die [**rpcserverregisterauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) -Funktion aufgerufen. Übergeben Sie einen Zeiger auf den Prinzipal Namen als Wert des ersten Parameters. Legen Sie den zweiten Parameter auf eine Konstante fest, die den Authentifizierungsdienst angibt, der von der Anwendung verwendet wird. Eine Beschreibung der Authentifizierungsdienste finden Sie unter [Authentication-Service-Konstanten](authentication-service-constants.md).

Der Server übergibt möglicherweise auch die Adresse einer Schlüssel Erwerbs Funktion als Wert des dritten Parameters. Siehe [Schlüsselerwerbs Funktionen](key-acquisition-functions.md). Legen Sie den dritten Parameter auf **null** fest, um die standardmäßige Schlüssel Erwerbs Funktion für den ausgewählten Authentifizierungsdienst zu verwenden. Der letzte Parameter für die [**rpcserverregisterauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) -Funktion ist ein Zeiger Daten, der an die Schlüssel Erwerbs Funktion übergeben werden soll, wenn Sie eine Schlüssel Erwerbs Funktion bereitstellen. Ein Aufrufen von **rpcserverregisterauthinfo** ist im folgenden Code Fragment dargestellt.


```C++
dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

rpcStatus = RpcServerRegisterAuthInfo (
    psz,                                   // Server principal name
    RPC_C_AUTHN_GSS_NEGOTIATE,             // Authentication service
    NULL,                                  // Use default key function
    NULL);                                 // No arg for key function
```



Außerdem kann der Server die RPC-Lauf Zeit Bibliothek mit einer Autorisierungs Funktion bereitstellen. Um eine Autorisierungs Funktion festzulegen, nennen Sie die [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) -Funktion.

Der Serverteil einer verteilten Anwendung kann die Funktion [**rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) oder [**rpcbindinginqauthclientex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) zum Abfragen eines Bindungs Handles für Authentifizierungsinformationen aufruft.

Wenn Ihr Server bei einem Security Support Provider registriert wird, werden keine Client Aufrufe mit ungültigen Anmelde Informationen gesendet. Allerdings werden Aufrufe ohne Anmelde Informationen gesendet. Es gibt drei Möglichkeiten, dies zu verhindern:

-   Registrieren Sie die Schnittstelle mithilfe von [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), mit einer Sicherheits Rückruffunktion. Dies bewirkt, dass die RPC-Lauf Zeit Bibliothek nicht authentifizierte Aufrufe an diese Schnittstelle automatisch ablehnt. Das Registrieren einer Rückruffunktion ist mit anderen Methoden zum Überprüfen von Zugriffs Anmelde Informationen kompatibel. die Rückruffunktion kann selbst die Funktionen [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**rpcgetauthorizationcontextforclient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)oder [**rpcbindinginqauthclientex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) aufrufen. Diese Funktionen können jedoch nicht die Argumente verwenden, die an die Funktion übermittelt werden, da Sie an diesem Punkt nicht gemarshallt werden.

> [!IMPORTANT]
> Das Registrieren der-Schnittstelle mithilfe von [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) mit einer Sicherheits Rückruffunktion ist die am häufigsten empfohlene Methode zum Überprüfen von Client Anmelde Informationen.

 

-   Wenden Sie [**rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) an, um die Sicherheitsstufe zu ermitteln, die vom Client verwendet wird. Der Stub kann dann einen Fehler zurückgeben, wenn der Client nicht authentifiziert ist.

 

 




