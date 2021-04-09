---
title: Informationen zur gegenseitigen Authentifizierung mithilfe von Kerberos
description: Bei gegenseitiger Authentifizierung müssen der Client und der Dienst vor dem Ausführen von Anwendungsfunktionen ihre jeweiligen Identitäten vor dem Ausführen von Anwendungsfunktionen überprüfen.
ms.assetid: 5ce923d6-bede-4acb-b297-e93f2f506ea9
ms.tgt_platform: multiple
keywords:
- Informationen zur gegenseitigen Authentifizierung mithilfe von Kerberos AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9685dad0bd20f233b8dcb0ecf12af338f318646f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036267"
---
# <a name="about-mutual-authentication-using-kerberos"></a>Informationen zur gegenseitigen Authentifizierung mithilfe von Kerberos

Bei gegenseitiger Authentifizierung müssen der Client und der Dienst vor dem Ausführen von Anwendungsfunktionen ihre jeweiligen Identitäten vor dem Ausführen von Anwendungsfunktionen überprüfen. Keine der Parteien kann Vorgänge mit dem anderen ausführen, bis die Identität überprüft wurde. Das heißt, der Dienst muss in der Lage sein, den Client zu überprüfen, ohne den Client abzufragen, und der Client muss in der Lage sein, den Dienst zu überprüfen, ohne den Dienst abzufragen.

Der Wert eines Dienstanbieter, der einen Client authentifizieren kann, ist bekannt. Ein Datei Dienst nimmt z. b. die Identität eines Clients an, um zu bestimmen, auf welche Dateien der Client zugreifen kann.

Der Wert eines Clients, der einen Dienst authentifizieren kann, ist weniger verständlich. Durch die Authentifizierung eines Dienstanbieter kann der Client die Daten, die er vom Dienst erhält, als vertrauenswürdig einstufen und beim Senden von sensiblen Daten an den Dienst sicher sein. Die Fähigkeit eines Clients, einen Dienst zu authentifizieren, ist besonders bei Client-/Dienstanwendungen wichtig, die die Delegierung des Sicherheits Kontexts des Clients unterstützen. Das heißt, dass der Client den Dienst autorisiert, als Delegat für den Zugriff auf zusätzliche Dienste oder Netzwerkressourcen zu fungieren.

Ein-Dienst authentifiziert einen Client wie folgt: der Client richtet einen lokalen Sicherheitskontext ein, indem er entweder in einem zuvor eingerichteten Kontext ausgeführt wird, z. b. in der Sitzung eines angemeldeten Benutzers oder durch explizites Bereitstellen von Anmelde Informationen für den zugrunde liegenden Sicherheitsanbieter. Der Dienst kann keine Verbindungen von einem nicht authentifizierten Client annehmen.

Der Kerberos-Mechanismus, mit dem ein Client einen Dienst authentifiziert, funktioniert wie folgt: Wenn ein Dienst installiert wird, registriert ein Dienst Installationsprogramm, das mit Administratorrechten ausgeführt wird, einen oder mehrere eindeutige SPNs für jede Dienst Instanz. Die Namen werden im Active Directory-Domäne Controller (DC) für das Benutzer-oder Computer Konto Objekt registriert, das von der Dienst Instanz für die Anmeldung verwendet wird. Wenn ein Client eine Verbindung mit einem Dienst anfordert, wird ein SPN für eine Dienst Instanz mit bekannten Daten oder Daten verwendet, die vom Benutzer bereitgestellt werden. Der Client verwendet dann das SSPI-Aushandlungs Paket, um den SPN für das Client Domänen Konto dem Schlüsselverteilungscenter (KDC) darzustellen. Der KDC sucht in der Gesamtstruktur nach einem Benutzer-oder Computer Konto, für das der SPN registriert ist. Wenn der SPN für mehr als ein Konto registriert ist, schlägt die Authentifizierung fehl. Andernfalls verschlüsselt der KDC eine Nachricht mit dem Kennwort des Kontos, für das der SPN registriert wurde. Die KDC übergibt diese verschlüsselte Nachricht an den Client, der Sie wiederum an die Dienst Instanz übergibt. Der Dienst verwendet das SSPI-Aushandlungs Paket zum Entschlüsseln der Nachricht, die an den Client zurückgeleitet wird, und auf den KDC des Clients. Das KDC authentifiziert den Dienst, wenn die entschlüsselte Nachricht mit der ursprünglichen Nachricht übereinstimmt.

-   Weitere Informationen zum Erstellen und Registrieren von SPNs finden Sie unter. [Dienst Prinzipal Namen](service-principal-names.md)
-   Weitere Informationen und ein Codebeispiel, das einen SPN für einen Windows Sockets-Dienst verfasst, der sich selbst mit einem Dienst Verbindungspunkt veröffentlicht, finden Sie unter Erstellen [der SPNs für einen Dienst mit einem SCP](composing-the-spns-for-a-service-with-an-scp.md).
-   Weitere Informationen und ein Codebeispiel, das einen SPN für einen RPC-Dienst verfasst, finden Sie unter Verfassen von Dienst Prinzipal Namen ( [SPN) für einen RpcNs-Dienst](composing-spns-for-an-rpcns-service.md).

 

 




