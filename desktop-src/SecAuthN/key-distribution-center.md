---
description: Die Schlüsselverteilungscenter (KDC) wird als Domänendienst implementiert. Sie verwendet Active Directory als Kontodatenbank und den globalen Katalog für die Weiterleitung von Empfehlungen an KDCs in anderen Domänen.
ms.assetid: f2a7c87c-9be7-4fd8-8ecd-4edf1f2336ef
title: Schlüsselverteilungscenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eef410ccb9289d30507708dc35000e1c15d5d4c9998b28b33a2e51d1a15b1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013340"
---
# <a name="key-distribution-center"></a>Schlüsselverteilungscenter

Die Schlüsselverteilungscenter (KDC) wird als Domänendienst implementiert. Sie verwendet Active Directory als Kontodatenbank und den globalen Katalog für die Weiterleitung von Empfehlungen an KDCs in anderen Domänen.

Wie bei anderen Implementierungen des [*Kerberos-Protokolls*](../secgloss/k-gly.md)ist das KDC ein einzelner Prozess, der zwei Dienste bereitstellt:

-   Authentifizierungsdienst (AS)

    Dieser Dienst stellt Ticketgewährungstickets (Ticket Granting Tickets, TGTs) für die Verbindung mit dem Ticketerteilungsdienst in seiner eigenen Domäne oder in einer beliebigen vertrauenswürdigen Domäne aus. Bevor ein Client ein Ticket für einen anderen Computer anfordern kann, muss er ein TGT vom Authentifizierungsdienst in der Kontodomäne des Clients anfordern. Der Authentifizierungsdienst gibt ein TGT für den Ticketgewährungsdienst in der Domäne des Zielcomputers zurück. Das TGT kann wiederverwendet werden, bis es abläuft. Der erste Zugriff auf den Ticketgewährungsdienst einer Domäne erfordert jedoch immer eine Fahrt zum Authentifizierungsdienst in der Kontodomäne des Clients.

-   Ticket-Granting Service (TGS)

    Dieser Dienst stellt Tickets für die Verbindung mit Computern in seiner eigenen Domäne aus. Wenn Clients Zugriff auf einen Computer wünschen, wenden sie sich an den Ticketerteilungsdienst in der Domäne des Zielcomputers, stellen ein TGT vor und fordern ein Ticket für den Computer an. Das Ticket kann wiederverwendet werden, bis es abläuft, aber der erste Zugriff auf einen beliebigen Computer erfordert immer eine Fahrt zum Ticketerteilungsdienst in der Kontodomäne des Zielcomputers.

Das KDC für eine Domäne befindet sich auf einem Domänencontroller, ebenso wie das Active Directory für die Domäne. Beide Dienste werden automatisch von der [*lokalen Sicherheitsautorität (Local Security Authority,*](../secgloss/l-gly.md) LSA) des Domänencontrollers gestartet und als Teil des LSA-Prozesses ausgeführt. Keiner der Dienste kann beendet werden. Wenn das KDC für Netzwerkclients nicht verfügbar ist, ist auch das Active Directory nicht verfügbar, und der Domänencontroller steuert die Domäne nicht mehr. Das System stellt die Verfügbarkeit dieser und anderer Domänendienste sicher, indem es jeder Domäne mehrere Domänencontroller und alle Peers ermöglicht. Jeder Domänencontroller kann Authentifizierungsanforderungen und Ticketerteilungsanforderungen akzeptieren, die an das KDC der Domäne adressiert sind.

Der vom KDC in einer beliebigen Domäne verwendete [*Sicherheitsprinzipalname*](../secgloss/s-gly.md) lautet "krbtgt", wie in [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt)angegeben. Ein Konto für diesen Sicherheitsprinzipal wird automatisch erstellt, wenn eine neue Domäne erstellt wird. Das Konto kann weder gelöscht noch der Name geändert werden. Ein zufälliger Kennwortwert wird dem Konto während der Erstellung der Domäne automatisch vom System zugewiesen. Das Kennwort für das Konto des KDC wird verwendet, um einen kryptografischen Schlüssel zum Verschlüsseln und Entschlüsseln der von ihm auszugebenden TGTs abzuleiten. Das Kennwort für ein Domänenvertrauensstellungskonto wird verwendet, um einen bereichsübergreifenden Schlüssel zum Verschlüsseln von Empfehlungstickets abzuleiten.

Alle Instanzen des KDC innerhalb einer Domäne verwenden das Domänenkonto für den Sicherheitsprinzipal "krbtgt". Clients adressieren Nachrichten an das KDC einer Domäne, indem sie sowohl den Prinzipalnamen des Diensts, "krbtgt", als auch den Namen der Domäne einschließen. Beide Informationselemente werden auch in Tickets verwendet, um die ausstellende Stelle zu identifizieren. Informationen zu Namensformularen und Adressierungskonventionen finden Sie unter [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).

 

 
