---
title: Gegenseitige Authentifizierung in RPC-Anwendungen
description: RPC-Dienste können Dienstverbindungspunkte verwenden, um sich selbst zu veröffentlichen, oder sie können die RPC-Namensdienst-APIs (RpcNs) verwenden.
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- Gegenseitige Authentifizierung in RPC-Anwendungen AD
- Active Directory, Using, Gegenseitige Authentifizierung, RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c7d5ea3632d08671861b72267419efd54c1a6a89770fbde72543596b29fa8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186055"
---
# <a name="mutual-authentication-in-rpc-applications"></a>Gegenseitige Authentifizierung in RPC-Anwendungen

RPC-Dienste können Dienstverbindungspunkte verwenden, um sich selbst zu veröffentlichen, oder sie können die RPC-Namensdienst-APIs (RpcNs) verwenden. In diesem Thema wird erläutert, wie die gegenseitige Authentifizierung mit einem RPC-Dienst durchgeführt wird, der sich selbst mithilfe der RPC-Namensdienst-APIs (RpcNs) veröffentlicht.

**So registrieren Sie einen SPN im Verzeichnis**

1.  Rufen Sie die [**DsGetSpn-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) auf, um einen Dienstprinzipalnamen (SPN) für den Dienst zu erstellen.
2.  Rufen Sie die [**DsWriteAccountSpn-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) auf, um den SPN für das Dienstkonto oder Computerkonto zu registrieren, in dessen Kontext der Dienst ausgeführt wird.

**So registrieren Sie einen Dienst beim RPC-Benennungsdienst**

1.  Überprüfen Sie, ob die entsprechenden SPNs für das Konto registriert sind, unter dem der Dienst ausgeführt wird. Weitere Informationen finden Sie unter [Wartungstasks für Anmeldekonten.](logon-account-maintenance-tasks.md)
2.  Rufen Sie die [**RpcServerRegisterAuthInfo-Funktion**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) auf, um den Dienst-SPN beim RPC-Authentifizierungsdienst zu registrieren, und geben Sie **RPC C \_ \_ AUTHN \_ GSS \_ NEGOTIATE** als zu verwendenden Authentifizierungsdienst an.

Weitere Informationen zum Ausführen der gegenseitigen Authentifizierung in einem RPC-Dienst finden Sie unter [Schreiben eines authentifizierten SSPI-Servers.](/windows/desktop/Rpc/writing-an-authenticated-sspi-server)

**So authentifizieren Sie den Dienst über den Client**

1.  Extrahieren Sie den Hostnamen aus der RPC-Bindung.
2.  Erstellen Sie den SPN für den Dienst, indem Sie die [**DsMakeSpn-Funktion**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) mit der Dienstklasse, dem DNS-Hostnamen und dem Dienstnamen aufrufen. , der im Fall von RpcNs der Distinguished Name des Verbindungspunkts ist.

    Weitere Informationen zum Verfassen eines SPN für einen RpcNs-Dienst finden Sie unter [Verfassen von SPNs für einen RpcNs-Dienst.](composing-spns-for-an-rpcns-service.md)

3.  Richten Sie eine [**RPC \_ SECURITY \_ QOS-Struktur**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) ein, um gegenseitige Authentifizierung anzufordern.
4.  Rufen Sie die [**RpcBindingSetAuthInfoEx-Funktion**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) auf, um die Authentifizierungsdaten für die RPC-Bindung festzulegen. Der Client muss mindestens **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY** anfordern, um sicherzustellen, dass die Kommunikation nicht manipuliert wurde. Zur Erhöhung der Sicherheit sollte der Client **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** angeben, um die Verschlüsselung anzufordern.
5.  Führen Sie den RPC-Aufruf aus.

Weitere Informationen zum Ausführen der gegenseitigen Authentifizierung in einem RPC-Client finden Sie unter [Schreiben eines authentifizierten SSPI-Clients.](/windows/desktop/Rpc/writing-an-authenticated-sspi-client)

**So authentifizieren Sie den Client über den Dienst**

1.  Rufen Sie die [**RpcBindingInqAuthClient-Funktion**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) auf, um die vom Client angegebenen Authentifizierungsparameter zu überprüfen. Wenn der Client nicht die gewünschte Authentifizierungsebene angefordert hat, weisen Sie den Aufruf zurück. Beachten Sie, dass ein RPC-Dienst bei jedem Aufruf die Authentifizierungsebene, den Authentifizierungsdienst und die Clientidentität überprüfen muss, um sicherzustellen, dass der Client ordnungsgemäß authentifiziert wurde.
2.  Rufen Sie die [**RpcImpersonateClient-Funktion**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) auf, um die Identität des Clients zu annehmen.
3.  Führen Sie den angeforderten Vorgang aus.
4.  Rufen Sie die [**RpcRevertToSelf-Funktion**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) auf, um zum Dienstsicherheitskontext zurückzukehren.

Weitere Informationen zum RPC-Clientidentitätswechsel finden Sie unter [Clientidentitätswechsel.](/windows/desktop/Rpc/client-impersonation)

Weitere Informationen finden Sie unter

-   [Veröffentlichen mit dem RPC-Namensdienst (RPCNs)](publishing-with-the-rpc-name-service-rpcns.md)
-   [RPC Security Essentials](/windows/desktop/Rpc/rpc-security-essentials)

 

 