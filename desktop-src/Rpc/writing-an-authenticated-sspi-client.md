---
title: Schreiben eines authentifizierten SSPI-Clients
description: Schreiben eines authentifizierten SSPI-Clients und eines Remoteprozeduraufrufs (RPC).
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- REMOTE PROCEDURE Call RPC , Tasks, Schreiben eines authentifizierten SSPI-Clients
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

Alle RPC-Client-/Serversitzungen erfordern eine Bindung zwischen dem Client und dem Server. Um Client-/Serveranwendungen Sicherheit zu gewährleisten, müssen die Programme eine authentifizierte Bindung verwenden. In diesem Abschnitt wird der Prozess zum Erstellen einer authentifizierten Bindung zwischen dem Client und dem Server beschrieben.

-   [Erstellen clientseitiger Bindungshandles](#creating-client-side-binding-handles)
-   [Bereitstellen von Clientanmeldeinformationen für den Server](#providing-client-credentials-to-the-server)

Weitere Informationen finden Sie unter [Verfahren, die mit den meisten Sicherheitspaketen und](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) Protokollen im Platform Software Development Kit (SDK) verwendet werden.

## <a name="creating-client-side-binding-handles"></a>Erstellen clientseitiger Bindungshandles

Um eine authentifizierte Sitzung mit einem Serverprogramm zu erstellen, müssen Clientanwendungen Authentifizierungsinformationen mit ihrem Bindungshand handle bereitstellen. Zum Einrichten eines authentifizierten Bindungshandpunkts rufen Clients die [**RpcBindingSetAuthInfo-**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) oder [**RpcBindingSetAuthInfoEx-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) auf. Diese beiden Funktionen sind nahezu identisch. Der einzige Unterschied besteht in der Angabe der Dienstqualität durch den Client mit der **RpcBindingSetAuthInfoEx-Funktion.**

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



Nachdem der Client die [**RpcBindingSetAuthInfo-**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) oder [**RpcBindingSetAuthInfoEx-Funktionen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) erfolgreich aufruft, authentifiziert die RPC-Laufzeitbibliothek automatisch alle RPC-Aufrufe für die Bindung. Die Sicherheits- und Authentifizierungsebene, die der Client auswählt, gilt nur für dieses Bindungshand handle. Vom Bindungshandles abgeleitete Kontexthandles verwenden dieselben Sicherheitsinformationen, nachfolgende Änderungen am Bindungshandles werden jedoch nicht in den Kontexthandles widergespiegelt. Weitere Informationen finden Sie unter [Kontexthandles.](context-handles.md)

Die Authentifizierungsebene bleibt wirksam, bis der Client eine andere Ebene auswählt oder bis der Prozess beendet wird. Die meisten Anwendungen erfordern keine Änderung der Sicherheitsstufe. Der Client kann ein beliebiges Bindungshand handle abfragen, um seine Autorisierungsinformationen zu erhalten, indem er [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) aufruft und ihm das Bindungshand handle über gibt.

## <a name="providing-client-credentials-to-the-server"></a>Bereitstellen von Clientanmeldeinformationen für den Server

Server verwenden die Bindungsinformationen des Clients, um die Sicherheit zu erzwingen. Clients übergeben immer ein Bindungshand handle als ersten Parameter eines Remoteprozeduraufrufs. Server können das Handle jedoch nur verwenden, wenn es als erster Parameter für Remoteverfahren in der IDL-Datei oder in der Anwendungskonfigurationsdatei (Application Configuration File, ACF) des Servers deklariert ist. Sie können das Bindungshandl in der IDL-Datei auflisten. Dies zwingt jedoch alle Clients, das Bindungshandl zu deklarieren und zu bearbeiten, anstatt die automatische oder implizite Bindung zu verwenden. Weitere Informationen finden Sie unter [Die IDL- und ACF-Dateien](the-idl-and-acf-files.md).

Eine andere Methode besteht im Verlassen der Bindungshandles **\_** aus der IDL-Datei und dem Platzieren des expliziten Handleattributs im ACF des Servers. Auf diese Weise kann der Client den Bindungstyp verwenden, der am besten für die Anwendung geeignet ist, während der Server das Bindungshand handle so verwendet, als wäre es explizit deklariert.

Das Extrahieren der Clientanmeldeinformationen aus dem Bindungshand handle erfolgt wie folgt:

-   RPC-Clients rufen [**RpcBindingSetAuthInfo auf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) und schließen ihre Authentifizierungsinformationen als Teil der Bindungsinformationen ein, die an den Server übergeben werden.
-   In der Regel ruft der Server [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) auf, um sich so zu verhalten, als wäre er der Client. Wenn das Bindungshandling nicht authentifiziert ist, schlägt der Aufruf mit RPC \_ S NO CONTEXT AVAILABLE \_ \_ \_ fehl. Rufen Sie zum Abrufen des Benutzernamens des Clients [**rpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) während des Identitätswechsels auf, oder rufen Sie unter Windows XP oder höher von Windows [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) auf, um den Autorisierungskontext abzurufen, und rufen Sie dann den Namen mithilfe von Funktionen vonAuthhz ab.
-   Der Server wird normalerweise [**CreatePrivateObjectSecurity aufrufen,**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) um Objekte mit ACLs zu erstellen. Nachdem dies erreicht wurde, werden spätere Sicherheitsüberprüfungen automatisch durchgeführt.

 

 