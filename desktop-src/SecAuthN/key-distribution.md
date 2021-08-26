---
description: In der Authentifizierungsmethode für geheime Schlüssel wird nicht erläutert, wie Client und Server den geheimen Sitzungsschlüssel erhalten, der in Sitzungen miteinander verwendet werden soll.
ms.assetid: 90ab0359-5079-49e9-809c-0c0005cc61bf
title: Schlüsselverteilung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd39f9cd5e219ac1e6339c0a6c3e7b9a19dc2680c21e948bdb979af791719a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013330"
---
# <a name="key-distribution"></a>Schlüsselverteilung

In der Authentifizierungsmethode für geheime Schlüssel wird [](../secgloss/s-gly.md) nicht erläutert, wie Client und Server den geheimen Sitzungsschlüssel erhalten, der in Sitzungen miteinander verwendet werden soll. Wenn es sich um Personen handelt, könnten sie sich im Geheimen treffen und sich auf den Schlüssel einigen. Wenn der Client jedoch ein Programm ist, das auf einer Arbeitsstation ausgeführt wird, und der Server ein Dienst ist, der auf einem Netzwerkserver ausgeführt wird, funktioniert diese Methode nicht.

Ein Client möchte mit vielen Servern kommunizieren und benötigt jeweils unterschiedliche Schlüssel. Ein Server kommuniziert mit vielen Clients und benötigt für jeden von ihnen unterschiedliche Schlüssel. Wenn jeder Client einen anderen Schlüssel für jeden Server benötigt und jeder Server einen anderen Schlüssel für jeden Client benötigt, wird die Schlüsselverteilung zu einem Problem. Darüber hinaus führt die Notwendigkeit, viele Schlüssel auf vielen Computern zu speichern und zu schützen, zu einem enormen Sicherheitsrisiko.

Der Name des [*Kerberos-Protokolls schlägt*](../secgloss/k-gly.md) seine Lösung für das Problem der Schlüsselverteilung vor. Kerberos (oder Cerberus) war eine Figur im klassischen Griechisch– ein 3-stelliger Hund, der immer wieder in die Unterwelt kam. Wie der wächterische Schutz hat das Kerberos-Protokoll drei Kopf: einen Client, einen Server und einen vertrauenswürdigen Drittanbieter, um zwischen ihnen zu vermitteln. Der vertrauenswürdige Vermittler in diesem Protokoll ist der Schlüsselverteilungscenter (KDC).

Das KDC ist ein Dienst, der auf einem physisch sicheren Server ausgeführt wird. Es verwaltet eine Datenbank mit Kontoinformationen für alle [*Sicherheitsprinzipale*](../secgloss/s-gly.md) in seinem Bereich. Ein Bereich ist das Kerberos-Äquivalent einer Domäne in Windows.

Zusammen mit anderen Informationen zu jedem Sicherheitsprinzipal speichert das KDC einen kryptografischen Schlüssel, der nur dem Prinzipal und dem KDC bekannt ist. Dies ist [*der Hauptschlüssel, der*](../secgloss/m-gly.md) beim Austausch zwischen den einzelnen Sicherheitsprinzipals und dem KDC verwendet wird. In den meisten Implementierungen des Kerberos-Protokolls wird [](../secgloss/h-gly.md) dieser Hauptschlüssel mithilfe einer Hashfunktion aus dem Kennwort eines Sicherheitsprinzipals abgeleitet.

Wenn ein Client eine sichere Verbindung mit einem Server herstellen möchte, sendet der Client zunächst eine Anforderung an das KDC, nicht an den Server, den er erreichen möchte. Das KDC erstellt einen eindeutigen [](../secgloss/s-gly.md) Sitzungsschlüssel für den Client und einen Server und sendet ihn an den Client, um sich gegenseitig zu authentifizieren. Das KDC hat Zugriff sowohl auf den Hauptschlüssel des Clients als auch auf den Hauptschlüssel des Servers. Das KDC verschlüsselt die Kopie des Sitzungsschlüssels des Servers mithilfe des Hauptschlüssels des Servers und die Kopie des Clients mithilfe des Hauptschlüssels des Clients.

Das KDC könnte seine Rolle als vertrauenswürdiger Vermittler erfüllen, indem er den Sitzungsschlüssel direkt an jeden beteiligten Sicherheitsprinzipal sendet. In der Praxis funktioniert dieses Verfahren jedoch aus verschiedenen Gründen nicht. Stattdessen sendet das KDC beide verschlüsselten Sitzungsschlüssel an den Client. Der Sitzungsschlüssel für den Server ist in einem [Sitzungsticket enthalten.](session-tickets.md)

 

 
