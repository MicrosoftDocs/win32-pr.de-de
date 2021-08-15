---
title: Gegenseitige Authentifizierung mithilfe von Kerberos
description: Die gegenseitige Authentifizierung ist ein Sicherheitsfeature, bei dem ein Clientprozess seine Identität gegenüber einem Dienst nachweisen muss und der Dienst seine Identität gegenüber dem Client nachweisen muss, bevor Anwendungsdatenverkehr über die Client-/Dienstverbindung übertragen wird.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, Verwenden, gegenseitige Authentifizierung
- Active Directory, Using, Sicherheit, gegenseitige Authentifizierung
- Sicherheits-AD
- Sicherheits-AD, gegenseitige Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e22a9f83712b15f22f9d9b05aee4219f3cbc892d88d0b44ba2d63fb9bbe2b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185950"
---
# <a name="mutual-authentication-using-kerberos"></a>Gegenseitige Authentifizierung mithilfe von Kerberos

Die gegenseitige Authentifizierung ist ein Sicherheitsfeature, bei dem ein Clientprozess seine Identität gegenüber einem Dienst nachweisen muss und der Dienst seine Identität gegenüber dem Client nachweisen muss, bevor Anwendungsdatenverkehr über die Client-/Dienstverbindung übertragen wird.

Active Directory Domain Services und Windows unterstützung für Dienstprinzipalnamen (Service Principal Names, SPN), die eine wichtige Komponente im Kerberos-Mechanismus sind, mit dem ein Client einen Dienst authentifiziert. Ein SPN ist ein eindeutiger Name, der eine Instanz eines Diensts identifiziert und dem Anmeldekonto zugeordnet ist, unter dem die Dienstinstanz ausgeführt wird. Die Komponenten eines SPN sind so, dass ein Client einen SPN für einen Dienst ohne das Dienstanmeldungskonto erstellen kann. Dadurch kann der Client den Dienst zur Authentifizierung seines Kontos anfordern, obwohl der Client nicht über den Kontonamen verfügt.

Dieser Abschnitt enthält eine Übersicht über Folgendes:

-   Gegenseitige Authentifizierung mit Kerberos.
-   Verfassen eines eindeutigen SPN.
-   Wie ein Dienstinstallationsprogramm SPNs für das Kontoobjekt registriert, das einer Dienstinstanz zugeordnet ist.
-   Wie eine Clientanwendung das Dienstverbindungspunktobjekt (Service Connection Point, SCP) einer Dienstinstanz in Active Directory Domain Services verwendet, um Daten abzurufen, aus denen ein SPN für den Dienst erstellt werden soll.
-   Wie eine Clientanwendung einen Dienst-SPN in Verbindung mit der Security Support Provider Interface (SSPI) verwendet, um den Dienst zu authentifizieren.
-   Ein Codebeispiel für eine Windows Sockets-Client-/Dienstanwendung, die einen SCP und SSPI verwendet, um gegenseitige Authentifizierung durchzuführen.
-   Ein Codebeispiel für einen RPC-Client/-Dienst, der die gegenseitige Authentifizierung mithilfe des RPC-Namensdiensts und der RPC-Authentifizierung ausführt.
-   Wie ein Windows Sockets Registration and Resolution (RnR)-Dienst SPNs verwendet, um gegenseitige Authentifizierung durchzuführen.

In diesem Abschnitt wird die Verwendung Active Directory-Domäne Service für die gegenseitige Authentifizierung erläutert, insbesondere der Zweck von Dienstverbindungspunkten und Dienstprinzipalnamen bei der gegenseitigen Authentifizierung. Es ist keine vollständige Erörterung der Verwendung von SSPI für die gegenseitige Authentifizierung oder der Authentifizierungs- und Sicherheitsunterstützung, die für RPC- und Windows Sockets-Anwendungen verfügbar ist.

Weitere Informationen finden Sie unter

-   [Veröffentlichen mit Dienstverbindungspunkten](publishing-with-service-connection-points.md)
-   [SSPI](/windows/desktop/SecAuthN/sspi)
-   [Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [RPC](/windows/desktop/Rpc/rpc-start-page)

 

 