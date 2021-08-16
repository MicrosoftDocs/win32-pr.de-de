---
title: Informationen zur gegenseitigen Authentifizierung mit Kerberos
description: Bei der gegenseitigen Authentifizierung müssen der Client und der Dienst ihre jeweiligen Identitäten untereinander überprüfen, bevor Sie Anwendungsfunktionen ausführen.
ms.assetid: 5ce923d6-bede-4acb-b297-e93f2f506ea9
ms.tgt_platform: multiple
keywords:
- Informationen zur gegenseitigen Authentifizierung mit Kerberos AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b020b2d808cee96319cf411b4199bb4ff78f357cfdf8379f01c7d07bc1c5c1c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841010"
---
# <a name="about-mutual-authentication-using-kerberos"></a>Informationen zur gegenseitigen Authentifizierung mit Kerberos

Bei der gegenseitigen Authentifizierung müssen der Client und der Dienst ihre jeweiligen Identitäten untereinander überprüfen, bevor Sie Anwendungsfunktionen ausführen. Keine der Parteien kann Vorgänge mit der anderen ausführen, bis die Identität überprüft wurde. Das heißt, der Dienst muss in der Lage sein, den Client zu überprüfen, ohne den Client abfragen zu müssen, und der Client muss in der Lage sein, den Dienst zu überprüfen, ohne den Dienst abfragen zu müssen.

Der Wert eines Diensts, der einen Client authentifizieren kann, ist bekannt. Beispielsweise wird von einem Dateidienst die Identität eines Clients angenommen, um zu bestimmen, auf welche Dateien der Client zugreifen kann.

Der Wert eines Clients, der einen Dienst authentifizieren kann, ist weniger verständlich. Durch die Authentifizierung eines Diensts kann der Client den Vom Dienst empfangenen Daten vertrauen und beim Senden vertraulicher Daten an den Dienst sicher sein. Die Fähigkeit eines Clients, einen Dienst zu authentifizieren, ist besonders wichtig in Client-/Dienstanwendungen, die die Delegierung des Sicherheitskontexts des Clients unterstützen. Das heißt, der Client autorisiert den Dienst, als dessen Delegat beim Zugriff auf zusätzliche Dienste oder Netzwerkressourcen zu fungieren.

Ein Dienst authentifiziert einen Client wie folgt: Der Client richtet einen lokalen Sicherheitskontext ein, indem er entweder in einem zuvor eingerichteten Kontext ausgeführt wird, z. B. in der Sitzung eines angemeldeten Benutzers, oder indem er dem zugrunde liegenden Sicherheitsanbieter explizit Anmeldeinformationen präsentiert. Der Dienst kann keine Verbindungen von einem nicht authentifizierten Client akzeptieren.

Der Kerberos-Mechanismus, mit dem ein Client einen Dienst authentifiziert, funktioniert wie folgt: Wenn ein Dienst installiert wird, registriert ein Dienstinstallationsprogramm, das mit Administratorrechten ausgeführt wird, einen oder mehrere eindeutige SPNs für jede Dienstinstanz. Die Namen werden im Active Directory-Domäne Controller (DC) des Benutzer- oder Computerkontoobjekts registriert, das von der Dienstinstanz für die Anmeldung verwendet wird. Wenn ein Client eine Verbindung mit einem Dienst an fordert, erstellt er einen SPN für eine Dienstinstanz unter Verwendung bekannter Daten oder daten, die vom Benutzer bereitgestellt werden. Der Client verwendet dann das SSPI-Aushandlungspaket, um den SPN dem Schlüsselverteilungscenter (KDC) für das Clientdomänenkonto zu präsentieren. Das KDC durchsucht die Gesamtstruktur nach einem Benutzer- oder Computerkonto, für das der SPN registriert ist. Wenn der SPN für mehrere Konten registriert ist, schlägt die Authentifizierung fehl. Andernfalls verschlüsselt das KDC eine Nachricht mit dem Kennwort des Kontos, für das der SPN registriert wurde. Das KDC übergibt diese verschlüsselte Nachricht an den Client, der sie wiederum an die Dienstinstanz übergibt. Der Dienst verwendet das SSPI-Aushandlungspaket, um die Nachricht zu entschlüsseln, die an den Client und an das KDC des Clients zurückübergibt. Das KDC authentifiziert den Dienst, wenn die entschlüsselte Nachricht der ursprünglichen Nachricht entspricht.

-   Weitere Informationen zum Komponieren und Registrieren von SPNs finden Sie unter . [Dienstprinzipalnamen](service-principal-names.md)
-   Weitere Informationen und ein Codebeispiel, in dem ein SPN für einen Windows Sockets-Dienst erstellt wird, der sich selbst mit einem Dienstverbindungspunkt veröffentlicht, finden Sie unter Erstellen der SPNs für einen Dienst mit einem [SCP.](composing-the-spns-for-a-service-with-an-scp.md)
-   Weitere Informationen und ein Codebeispiel, aus dem ein SPN für einen RPC-Dienst erstellt wird, finden Sie unter Erstellen von [SPNs für einen RpcNs-Dienst.](composing-spns-for-an-rpcns-service.md)

 

 




