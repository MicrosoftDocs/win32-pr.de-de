---
description: Der Schlüsselverteilungscenter (KDC) wird als Domänen Dienst implementiert. Dabei werden die Active Directory als Konto Datenbank und der globale Katalog zum Weiterleiten von verweisen an KDCs in anderen Domänen verwendet.
ms.assetid: f2a7c87c-9be7-4fd8-8ecd-4edf1f2336ef
title: Schlüsselverteilungscenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f473fc3b84fed05e157fa700e7549f025979a90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042382"
---
# <a name="key-distribution-center"></a>Schlüsselverteilungscenter

Der Schlüsselverteilungscenter (KDC) wird als Domänen Dienst implementiert. Dabei werden die Active Directory als Konto Datenbank und der globale Katalog zum Weiterleiten von verweisen an KDCs in anderen Domänen verwendet.

Wie bei anderen Implementierungen des [*Kerberos-Protokolls*](../secgloss/k-gly.md)ist das KDC ein einzelner Prozess, der zwei Dienste bereitstellt:

-   Authentifizierungsdienst (as)

    Dieser Dienst gibt Tickets zum Gewähren von Tickets (TGTs) für die Verbindung mit dem Ticket Erteilungs Dienst in seiner eigenen Domäne oder in einer vertrauenswürdigen Domäne aus. Bevor ein Client ein Ticket an einen anderen Computer anfordern kann, muss ein TGT vom Authentifizierungsdienst in der Konto Domäne des Clients angefordert werden. Der Authentifizierungsdienst gibt ein TGT für den Dienst zur Ticket Gewährung in der Domäne des Ziel Computers zurück. Das TGT kann wieder verwendet werden, bis es abläuft, aber der erste Zugriff auf den Dienst für die Ticket Gewährung einer Domäne erfordert stets eine Fahrt zum Authentifizierungsdienst in der Konto Domäne des Clients.

-   Ticket-Granting Dienst (TGS)

    Dieser Dienst gibt Tickets für die Verbindung mit Computern in der eigenen Domäne aus. Wenn Clients auf einen Computer zugreifen möchten, wenden Sie sich an den Dienst für die Ticket Gewährung in der Domäne des Ziel Computers, stellen einen TGT vor und bitten um ein Ticket für den Computer. Das Ticket kann bis zum Ablauf wieder verwendet werden, aber für den ersten Zugriff auf jeden Computer ist immer eine Fahrt zum Dienst für die Ticket Gewährung in der Konto Domäne des Ziel Computers erforderlich.

Der KDC für eine Domäne befindet sich auf einem Domänen Controller, ebenso wie der Active Directory für die Domäne. Beide Dienste werden automatisch von der [*lokalen Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) des Domänen Controllers gestartet und als Teil des LSA-Prozesses ausgeführt. Keiner der Dienste kann beendet werden. Wenn der KDC für Netzwerk Clients nicht verfügbar ist, ist der Active Directory ebenfalls nicht verfügbar – und der Domänen Controller wird die Domäne nicht mehr Steuern. Das System stellt sicher, dass diese und andere Domänen Dienste verfügbar sind, indem jede Domäne mehrere Domänen Controller, alle Peers, zulässt. Alle Domänen Controller können Authentifizierungsanforderungen und Ticket Erteilungs Anforderungen akzeptieren, die an den KDC der Domäne adressiert sind.

Der [*Sicherheits Prinzipal*](../secgloss/s-gly.md) Name, der vom KDC in einer beliebigen Domäne verwendet wird, ist "krbtgt", wie in [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt)angegeben. Ein Konto für diesen Sicherheits Prinzipal wird automatisch erstellt, wenn eine neue Domäne erstellt wird. Das Konto kann nicht gelöscht werden, und der Name kann nicht geändert werden. Beim Erstellen der Domäne wird dem Konto automatisch ein zufälliger Kenn Wort Wert zugewiesen. Das Kennwort für das Konto des KDC wird zum Ableiten eines Kryptografieschlüssels zum Verschlüsseln und Entschlüsseln der von ihm ausgestellten TGTs verwendet. Das Kennwort für ein Domänen Vertrauensstellungs Konto wird verwendet, um einen bereichsübergreifenden Schlüssel zum Verschlüsseln von verweistickets abzuleiten.

Alle Instanzen des KDC innerhalb einer Domäne verwenden das Domänen Konto für den Sicherheits Prinzipal "krbtgt". Clients können Nachrichten mit dem Prinzipal Namen der Domäne, "krbtgt" und dem Namen der Domäne an die KDC einer Domäne richten. Beide Informationselemente werden auch in Tickets verwendet, um die ausstellende Zertifizierungsstelle zu identifizieren. Weitere Informationen zu namens Formularen und Adressierungs Konventionen finden Sie unter [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).

 

 
