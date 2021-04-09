---
title: Gegenseitige Authentifizierung in RPC-Anwendungen
description: RPC-Dienste können Dienst Verbindungspunkte verwenden, um sich selbst zu veröffentlichen, oder Sie können die RpcNs-APIs (RPC Name Service) verwenden.
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- Gegenseitige Authentifizierung in RPC-Anwendungen AD
- Active Directory, Verwendung von gegenseitiger Authentifizierung, RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a8591056293c916205b5b600c1b1a061d169f0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858137"
---
# <a name="mutual-authentication-in-rpc-applications"></a>Gegenseitige Authentifizierung in RPC-Anwendungen

RPC-Dienste können Dienst Verbindungspunkte verwenden, um sich selbst zu veröffentlichen, oder Sie können die RpcNs-APIs (RPC Name Service) verwenden. In diesem Thema wird erläutert, wie die gegenseitige Authentifizierung mit einem RPC-Dienst durchgeführt wird, der sich mit den RpcNs-APIs (RPC Name Service) selbst veröffentlicht

**So registrieren Sie einen SPN im Verzeichnis**

1.  Aufrufen der [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) -Funktion zum Verfassen eines Dienst Prinzipal namens (SPN) für den Dienst.
2.  Wenden Sie die [**dswrite-accountspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) -Funktion an, um den SPN für das Dienst Konto oder das Computer Konto zu registrieren, in dessen Kontext der Dienst ausgeführt wird.

**So registrieren Sie einen Dienst beim RPC-Naming Service**

1.  Vergewissern Sie sich, dass die entsprechenden SPNs für das Konto, unter dem der Dienst ausgeführt wird, registriert sind. Weitere Informationen finden Sie unter [Anmelde Konto-Wartungs Tasks](logon-account-maintenance-tasks.md).
2.  Wenden Sie die [**rpcserverregisterauthinfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) -Funktion an, um den Dienst-SPN beim RPC-Authentifizierungsdienst zu registrieren, und geben Sie **RPC \_ C \_ authn \_ GSS \_ aushandeln** als Authentifizierungsdienst an, der verwendet werden soll.

Weitere Informationen zum Ausführen der gegenseitigen Authentifizierung in einem RPC-Dienst finden Sie unter [Schreiben eines authentifizierten SSPI-Servers](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).

**So authentifizieren Sie den Dienst vom Client**

1.  Extrahieren Sie den Hostnamen aus der RPC-Bindung.
2.  Erstellen Sie den SPN für den Dienst, indem Sie die [**dsmakespn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) -Funktion mit der Dienstklasse, dem DNS-Hostnamen und dem Dienstnamen aufrufen. Dies ist der Distinguished Name des Verbindungs Punkts im Fall von RpcNs.

    Weitere Informationen zum Erstellen eines SPN für einen RpcNs-Dienst finden Sie unter Verfassen von Dienst Prinzipal Namen ( [SPN) für einen RpcNs-Dienst](composing-spns-for-an-rpcns-service.md).

3.  Richten Sie eine [**RPC \_ - \_ sicherheitsqos**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) -Struktur ein, um die gegenseitige Authentifizierung anzufordern.
4.  Aufrufen der Funktion [**rpcbindingsetauthinfoex**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) zum Festlegen der Authentifizierungsdaten für die RPC-Bindung. Der Client muss mindestens die **\_ \_ \_ \_ Pkt- \_ Integrität der RPC-C-authn-Ebene** anfordern, um sicherzustellen, dass die Kommunikation nicht manipuliert wurde. Um die Sicherheit zu erhöhen, muss der Client den **RPC- \_ C- \_ authn- \_ Level \_ Pkt \_ Privacy** angeben, um die Verschlüsselung anzufordern.
5.  Führen Sie den RPC-Aufruf aus.

Weitere Informationen zum Ausführen der gegenseitigen Authentifizierung bei einem RPC-Client finden Sie unter [Schreiben eines authentifizierten SSPI-Clients](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).

**So authentifizieren Sie den Client über den Dienst**

1.  Zum Überprüfen der vom Client angegebenen Authentifizierungs Parameter wird die [**rpcbindinginqauthclient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) -Funktion aufgerufen. Wenn der Client die gewünschte Authentifizierungs Stufe nicht angefordert hat, lehnen Sie den-Befehl ab. Beachten Sie, dass ein RPC-Dienst bei jedem Aufruf die Authentifizierungs Ebene, den Authentifizierungsdienst und die Client Identität überprüfen muss, um sicherzustellen, dass der Client ordnungsgemäß authentifiziert wurde.
2.  Zum Annehmen der Identität des Clients wird die [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) -Funktion aufgerufen.
3.  Führt den angeforderten Vorgang aus.
4.  Aufrufen der [**rpkrevertteself**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) -Funktion, um zum Dienst Sicherheitskontext zurückzukehren.

Weitere Informationen zum Identitätswechsel des RPC-Clients finden Sie unter [Client](/windows/desktop/Rpc/client-impersonation)Identitätswechsel.

Weitere Informationen finden Sie unter

-   [Veröffentlichen mit dem RPC-Namensdienst (RPC Name Service, RpcNs)](publishing-with-the-rpc-name-service-rpcns.md)
-   [Grundlagen zu RPC](/windows/desktop/Rpc/rpc-security-essentials)

 

 