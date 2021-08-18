---
title: Schreiben eines authentifizierten SSPI-Clients
description: Schreiben eines authentifizierten SSPI-Clients und Remoteprozeduraufrufs (RPC).
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- Remoteprozeduraufruf RPC , Tasks, Schreiben eines authentifizierten SSPI-Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445d5340b03f07805a9e2ab89deb8c915a76160db67b504259ae8de0bbabee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010358"
---
# <a name="writing-an-authenticated-sspi-client"></a>Schreiben eines authentifizierten SSPI-Clients

Alle RPC-Client-/Serversitzungen erfordern eine Bindung zwischen dem Client und dem Server. Um Client-/Serveranwendungen Sicherheit hinzuzufügen, müssen die Programme eine authentifizierte Bindung verwenden. In diesem Abschnitt wird der Prozess zum Erstellen einer authentifizierten Bindung zwischen dem Client und dem Server beschrieben.

-   [Erstellen clientseitiger Bindungshandles](#creating-client-side-binding-handles)
-   [Bereitstellen von Clientanmeldeinformationen für den Server](#providing-client-credentials-to-the-server)

Weitere Informationen finden Sie unter Verfahren, die [mit den meisten Sicherheitspaketen und Protokollen](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) im Platform Software Development Kit (SDK) verwendet werden.

## <a name="creating-client-side-binding-handles"></a>Erstellen clientseitiger Bindungshandles

Um eine authentifizierte Sitzung mit einem Serverprogramm zu erstellen, müssen Clientanwendungen Authentifizierungsinformationen mit ihrem Bindungshandle bereitstellen. Clients rufen die [**RpcBindingSetAuthInfo-**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) oder [**RpcBindingSetAuthInfo-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) auf, um ein authentifiziertes Bindungshandle einzurichten. Diese beiden Funktionen sind nahezu identisch. Der einzige Unterschied besteht darin, dass der Client die Dienstqualität mit der **RpcBindingSetAuthInfoEx-Funktion** angeben kann.

Das folgende Codefragment zeigt, wie ein Aufruf von [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) aussehen kann.


```C++
// This code fragment assumes that rpcBinding is a valid binding 
// handle between the client and the server. It also assumes that
// pAuthCredentials is a valid pointer to a data structure which
// contains the user's authentication credentials.

dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

//...

rpcStatus = RpcBindingSetAuthInfo(
    rpcBinding,                       // Valid binding handle
    pszSpn,                           // Principal name 
    RPC_C_AUTHN_LEVEL_PKT_INTEGRITY,  // Authentication level
    RPC_C_AUTHN_GSS_NEGOTIATE,        // Use Negotiate SSP
    NULL,                             // Authentication credentials <entity type="ndash"/> use current thread credentials
    RPC_C_AUTHZ_NAME);                // Authorization service
```



Nachdem der Client die [**Funktionen RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) oder [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) erfolgreich aufgerufen hat, authentifiziert die RPC-Laufzeitbibliothek automatisch alle RPC-Aufrufe für die Bindung. Die Vom Client ausgewählte Sicherheitsstufe und Authentifizierungsebene gilt nur für dieses Bindungshandle. Kontexthandles, die vom Bindungshandle abgeleitet werden, verwenden die gleichen Sicherheitsinformationen, aber nachfolgende Änderungen am Bindungshandle werden nicht in den Kontexthandles widergespiegelt. Weitere Informationen finden Sie unter [Kontexthandles.](context-handles.md)

Die Authentifizierungsebene bleibt wirksam, bis der Client eine andere Ebene ausschließt oder bis der Prozess beendet wird. Für die meisten Anwendungen ist keine Änderung der Sicherheitsstufe erforderlich. Der Client kann ein beliebiges Bindungshandle abfragen, um seine Autorisierungsinformationen abzurufen, indem [**rpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) aufgerufen und das Bindungshandle übergeben wird.

## <a name="providing-client-credentials-to-the-server"></a>Bereitstellen von Clientanmeldeinformationen für den Server

Server verwenden die Bindungsinformationen des Clients, um die Sicherheit zu erzwingen. Clients übergeben immer ein Bindungshandle als ersten Parameter eines Remoteprozeduraufrufs. Server können das Handle jedoch nur verwenden, wenn es als erster Parameter für Remoteprozeduren entweder in der IDL-Datei oder in der Anwendungskonfigurationsdatei (Application Configuration File, ACF) des Servers deklariert ist. Sie können das Bindungshandle in der IDL-Datei auflisten. Dadurch werden jedoch alle Clients gezwungen, das Bindungshandle zu deklarieren und zu bearbeiten, anstatt die automatische oder implizite Bindung zu verwenden. Weitere Informationen finden Sie unter [Die IDL- und ACF-Dateien.](the-idl-and-acf-files.md)

Eine weitere Methode besteht darin, die Bindungshandles aus der IDL-Datei zu lassen und das **explizite \_ Handleattribut** in den ACF des Servers zu platzieren. Auf diese Weise kann der Client den Bindungstyp verwenden, der für die Anwendung am besten geeignet ist, während der Server das Bindungshandle so verwendet, als ob es explizit deklariert worden wäre.

Das Extrahieren der Clientanmeldeinformationen aus dem Bindungshandle erfolgt wie folgt:

-   RPC-Clients rufen [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) auf und fügen ihre Authentifizierungsinformationen als Teil der Bindungsinformationen ein, die an den Server übergeben werden.
-   In der Regel ruft der Server [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) auf, um sich so zu verhalten, als wäre es der Client. Wenn das Bindungshandle nicht authentifiziert ist, schlägt der Aufruf mit RPC \_ S NO CONTEXT AVAILABLE \_ \_ \_ fehl. Um den Benutzernamen des Clients abzurufen, rufen Sie [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) auf, während Sie die Identität annehmen, oder rufen Sie auf Windows XP oder neueren Versionen von Windows [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) auf, um den Autorisierungskontext abzurufen, und rufen Sie dann den Namen mithilfe von Authz-Funktionen ab.
-   Der Server ruft normalerweise [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) auf, um Objekte mit ACLs zu erstellen. Nachdem dies erfolgt ist, werden spätere Sicherheitsüberprüfungen automatisch durchgeführt.

 

 