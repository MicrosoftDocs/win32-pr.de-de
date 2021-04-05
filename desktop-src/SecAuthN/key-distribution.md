---
description: Die Authentifizierungsmethode für den geheimen Schlüssel erläutert nicht, wie der Client und der Server den geheimen Sitzungsschlüssel erhalten, der in Sitzungen zueinander verwendet werden soll.
ms.assetid: 90ab0359-5079-49e9-809c-0c0005cc61bf
title: Schlüsselverteilung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f04a2968e8b7b978bc7b325d65b4a2acf08e1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757009"
---
# <a name="key-distribution"></a>Schlüsselverteilung

Die Authentifizierungsmethode für den geheimen Schlüssel erläutert nicht, wie der Client und der Server den geheimen [*Sitzungsschlüssel*](../secgloss/s-gly.md) erhalten, der in Sitzungen zueinander verwendet werden soll. Wenn Sie Personen sind, können Sie im geheimen Schlüssel treffen und den Schlüssel zustimmen. Wenn der Client jedoch ein Programm ist, das auf einer Arbeitsstation ausgeführt wird und es sich bei dem Server um einen Dienst handelt, der auf einem Netzwerkserver ausgeführt wird, funktioniert diese Methode nicht.

Ein Client möchte mit vielen Servern kommunizieren und benötigt jeweils verschiedene Schlüssel. Ein Server kommuniziert mit vielen Clients und benötigt auch jeweils verschiedene Schlüssel. Wenn jeder Client einen anderen Schlüssel für jeden Server benötigt und jeder Server einen anderen Schlüssel für jeden Client benötigt, wird die Schlüsselverteilung zu einem Problem. Außerdem entsteht durch die Notwendigkeit, viele Schlüssel auf vielen Computern zu speichern und zu schützen, ein enormes Sicherheitsrisiko.

Der Name des [*Kerberos-Protokolls*](../secgloss/k-gly.md) weist auf die Lösung des Problems der Schlüsselverteilung hin. Kerberos (oder Cerberus) war eine Abbildung in der klassischen griechischen Mythologie – ein heftiger, dreiköpfiger Hund, der die Menschen in die Unterwelt gewechselt hat. Wie beim mythischen Wächter besteht auch das Kerberos-Protokoll aus drei Köpfen: einem Client, einem Server und einem vertrauenswürdigen Drittanbieter, um zwischen Ihnen zu vermitteln. Der vertrauenswürdige Vermittler in diesem Protokoll ist der Schlüsselverteilungscenter (KDC).

Der KDC ist ein Dienst, der auf einem physisch sicheren Server ausgeführt wird. Sie verwaltet eine Datenbank mit Kontoinformationen für alle [*Sicherheits Prinzipale*](../secgloss/s-gly.md) in Ihrem Bereich. Ein Bereich ist die Kerberos-Entsprechung einer Domäne in Windows.

Zusammen mit anderen Informationen zu den einzelnen Sicherheits Prinzipalen speichert der KDC einen Kryptografieschlüssel, der nur dem Prinzipal und dem KDC bekannt ist. Dies ist der [*Hauptschlüssel*](../secgloss/m-gly.md) , der im Austausch zwischen den einzelnen Sicherheits Prinzipalen und dem KDC verwendet wird. Bei den meisten Implementierungen des Kerberos-Protokolls wird dieser Hauptschlüssel mithilfe einer [*Hash*](../secgloss/h-gly.md) Funktion aus dem Kennwort eines Sicherheits Prinzipals abgeleitet.

Wenn ein Client eine sichere Verbindung mit einem Server herstellen möchte, sendet der Client zunächst eine Anforderung an den KDC und nicht an den Server, der erreicht werden soll. Der KDC erstellt und sendet an den Client einen eindeutigen [*Sitzungsschlüssel*](../secgloss/s-gly.md) für den Client und einen Server, der zum Authentifizieren verwendet wird. Der KDC hat Zugriff auf den Hauptschlüssel des Clients und den Hauptschlüssel des Servers. Der KDC verschlüsselt die Server Kopie des Sitzungsschlüssels mit dem Hauptschlüssel des Servers und der Kopie des Clients mit dem Hauptschlüssel des Clients.

Der KDC könnte seine Rolle als vertrauenswürdigen Vermittler erfüllen, indem er den Sitzungsschlüssel direkt an alle Beteiligten Sicherheits Prinzipale sendet, aber in der Praxis funktioniert dieses Verfahren aus verschiedenen Gründen nicht. Stattdessen sendet der KDC beide verschlüsselten Sitzungsschlüssel an den Client. Der Sitzungsschlüssel für den Server ist in einem [Sitzungs Ticket](session-tickets.md)enthalten.

 

 
