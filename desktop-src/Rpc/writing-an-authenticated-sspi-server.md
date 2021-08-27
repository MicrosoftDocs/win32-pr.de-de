---
title: Schreiben eines authentifizierten SSPI-Servers
description: Bevor die authentifizierte Kommunikation zwischen client- und serverseitigen Programmen erfolgen kann, muss der Server seine Authentifizierungsinformationen registrieren.
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- Remoteprozeduraufruf RPC , Tasks, Schreiben eines authentifizierten SSPI-Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462f153905d6b654a0533c7bd05bff0e9627869d6910fb1fea05fe9340b788a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010348"
---
# <a name="writing-an-authenticated-sspi-server"></a>Schreiben eines authentifizierten SSPI-Servers

Bevor die authentifizierte Kommunikation zwischen client- und serverseitigen Programmen erfolgen kann, muss der Server seine Authentifizierungsinformationen registrieren. Insbesondere muss der Server seinen Prinzipalnamen registrieren und den verwendeten Authentifizierungsdienst angeben. Weitere Informationen zu Prinzipalnamen finden Sie unter [Prinzipalnamen.](principal-names.md) Weitere Informationen zu Authentifizierungsdiensten finden Sie unter [Authentifizierungsdienste.](authentication-services.md)

Um seine Authentifizierungsinformationen zu registrieren, rufen Server die [**RpcServerRegisterAuthInfo-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) auf. Übergeben Sie einen Zeiger auf den Prinzipalnamen als Wert des ersten Parameters. Legen Sie den zweiten Parameter auf eine Konstante fest, die den von der Anwendung verwendeten Authentifizierungsdienst angibt. Eine Beschreibung der Authentifizierungsdienste finden Sie unter [Authentication-Service-Konstanten.](authentication-service-constants.md)

Der Server kann auch die Adresse einer Schlüsselerwerbsfunktion als Wert des dritten Parameters übergeben. Weitere Informationen finden Sie [unter Key Acquisition Functions](key-acquisition-functions.md). Um die Standardfunktion für den Schlüsselerwerb für den ausgewählten Authentifizierungsdienst zu verwenden, legen Sie den dritten Parameter auf **NULL** fest. Der letzte Parameter der [**RpcServerRegisterAuthInfo-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) sind Zeigerdaten, die an die Schlüsselerfassungsfunktion übergeben werden sollen, wenn Sie eine Schlüsselerfassungsfunktion bereitstellen. Ein Aufruf von **RpcServerRegisterAuthInfo** wird im folgenden Codefragment angezeigt.


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



Darüber hinaus kann der Server die RPC-Laufzeitbibliothek mit einer Autorisierungsfunktion bereitstellen. Um eine Autorisierungsfunktion festzulegen, rufen Sie die [**RpcMgmtSetAuthorizationFn-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) auf.

Der Serverteil einer verteilten Anwendung kann die Funktion [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) oder [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) aufrufen, um ein Bindungshandle nach Authentifizierungsinformationen abzufragen.

Wenn sich Ihr Server bei einem Sicherheitssupportanbieter registriert, werden Clientaufrufe mit ungültigen Anmeldeinformationen nicht gesendet. Aufrufe ohne Anmeldeinformationen werden jedoch gesendet. Es gibt drei Möglichkeiten, dies zu verhindern:

-   Registrieren Sie die Schnittstelle mit [**rpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)mit einer Sicherheitsrückruffunktion. Dadurch lehnt die RPC-Laufzeitbibliothek nicht authentifizierte Aufrufe dieser Schnittstelle automatisch ab. Das Registrieren einer Rückruffunktion ist mit anderen Methoden zum Überprüfen von Zugriffsanmeldeinformationen kompatibel. Die Rückruffunktion kann die Funktionen [**RpcImpersonateClient,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)oder [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) oder andere aufrufen. Diese Funktionen können jedoch nicht die argumente verwenden, die an die Funktion übergeben werden, da sie an diesem Punkt nicht unmarsmarkiert sind.

> [!IMPORTANT]
> Das Registrieren der Schnittstelle mit [**rpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) bei einer Sicherheitsrückruffunktion ist die am häufigsten empfohlene Methode zum Überprüfen von Clientanmeldeinformationen.

 

-   Rufen Sie [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) auf, um die Sicherheitsstufe zu bestimmen, die der Client verwendet. Ihr Stub kann dann einen Fehler zurückgeben, wenn der Client nicht authentifiziert ist.

 

 




