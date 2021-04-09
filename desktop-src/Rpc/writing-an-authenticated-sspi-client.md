---
title: Schreiben eines authentifizierten SSPI-Clients
description: Schreiben eines authentifizierten SSPI-Clients und eines Remote Prozedur Aufrufs (RPC).
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Schreiben eines authentifizierten SSPI-Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8476772a2ed652f6646b078c2876234cbcc0d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102027"
---
# <a name="writing-an-authenticated-sspi-client"></a>Schreiben eines authentifizierten SSPI-Clients

Alle RPC-Client-/Serversitzungen erfordern eine Bindung zwischen dem Client und dem Server. Zum Hinzufügen von Sicherheit zu Client-/Server-Anwendungen müssen die Programme eine authentifizierte Bindung verwenden. In diesem Abschnitt wird beschrieben, wie Sie eine authentifizierte Bindung zwischen Client und Server erstellen.

-   [Erstellen von Client seitigen Bindungs Handles](#creating-client-side-binding-handles)
-   [Bereitstellen von Client Anmelde Informationen für den Server](#providing-client-credentials-to-the-server)

Weitere Informationen finden Sie unter [Prozeduren, die mit den meisten Sicherheitspaketen und Protokollen](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) im Platform Software Development Kit (SDK) verwendet werden.

## <a name="creating-client-side-binding-handles"></a>Erstellen von Client seitigen Bindungs Handles

Zum Erstellen einer authentifizierten Sitzung mit einem Serverprogramm müssen Client Anwendungen Authentifizierungsinformationen mit Ihrem Bindungs handle bereitstellen. Zum Einrichten eines authentifizierten Bindungs Handles rufen Clients die [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) -oder [**rpcbindingsetauthinfoex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) -Funktion auf. Diese beiden Funktionen sind nahezu identisch. Der einzige Unterschied besteht darin, dass der Client die Quality of Service mit der **rpcbindingsetauthinfoex** -Funktion angeben kann.

Das folgende Code Fragment zeigt, wie ein Aufrufen von [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) aussehen könnte.


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



Nachdem der Client die Funktionen [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) oder [**rpcbindingsetauthinfoex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) erfolgreich aufgerufen hat, authentifiziert die RPC-Lauf Zeit Bibliothek automatisch alle RPC-Aufrufe für die Bindung. Die Sicherheitsstufe und die Authentifizierung, die vom Client ausgewählt werden, gelten nur für diesen Bindungs handle. Vom Bindungs handle abgeleitete Kontext Handles verwenden die gleichen Sicherheitsinformationen. nachfolgende Änderungen am Bindungs handle werden jedoch nicht in den Kontext Handles widergespiegelt. Weitere Informationen finden Sie unter [Kontext Handles](context-handles.md).

Die Authentifizierungs Ebene bleibt wirksam, bis der Client eine andere Ebene auswählt, oder bis der Prozess beendet wird. Die meisten Anwendungen erfordern keine Änderung der Sicherheitsstufe. Der Client kann ein beliebiges Bindungs handle Abfragen, um seine Autorisierungs Informationen abzurufen, indem er [**rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) aufruft und ihm das Bindungs handle übergibt.

## <a name="providing-client-credentials-to-the-server"></a>Bereitstellen von Client Anmelde Informationen für den Server

Server verwenden die Bindungs Informationen des Clients, um die Sicherheit zu erzwingen. Clients übergeben immer ein Bindungs Handle als ersten Parameter eines Remote Prozedur Aufrufes. Allerdings können Server das Handle nicht verwenden, es sei denn, Sie ist als erster Parameter für Remote Prozeduren in der IDL-Datei oder in der Anwendungs Konfigurationsdatei (ACF) des Servers deklariert. Sie können das Bindungs Handle in der IDL-Datei auflisten, Dies zwingt jedoch alle Clients, das Bindungs Handle zu deklarieren und zu bearbeiten, anstatt eine automatische oder implizite Bindung zu verwenden. Weitere Informationen finden Sie in [den IDL-und ACF-Dateien](the-idl-and-acf-files.md).

Eine andere Methode besteht darin, die Bindungs Handles aus der IDL-Datei zu lassen und das **explizite \_ handle** -Attribut in der ACF des Servers zu platzieren. Auf diese Weise kann der Client den Bindungstyp verwenden, der am besten für die Anwendung geeignet ist, während der Server das Bindungs Handle verwendet, als ob er explizit deklariert wurde.

Der Prozess zum Extrahieren der Client Anmelde Informationen aus dem Bindungs handle erfolgt wie folgt:

-   RPC-Clients wenden [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) an und schließen Ihre Authentifizierungsinformationen als Teil der an den Server über gebenden Bindungs Informationen ein.
-   Normalerweise ruft der Server [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) auf, damit er sich so verhält, als wäre er der Client. Wenn das Bindungs Handle nicht authentifiziert ist, schlägt der Aufruf fehl, \_ und \_ es ist kein \_ Kontext \_ verfügbar. Um den Benutzernamen des Clients abzurufen, rufen Sie beim Identitätswechsel [**rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) auf, oder rufen Sie unter Windows XP oder neueren Windows-Versionen [**rpcgetauthorizationcontextforclient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) auf, um den Autorisierungs Kontext abzurufen, und verwenden Sie dann Authz-Funktionen, um den Namen abzurufen.
-   Der Server ruft normalerweise " [**kreateprivateobjectsecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) " auf, um Objekte mit ACLs zu erstellen. Anschließend werden spätere Sicherheitsüberprüfungen automatisch durchgeführt.

 

 