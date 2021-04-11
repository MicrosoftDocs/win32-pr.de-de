---
description: Bei einer Transaktion handelt es sich um eine Reihe von Änderungen eines Datenspeicher (z. b. einer Datenbank oder eines Dateisystems), die garantiert, dass Sie entweder erfolgreich ausgeführt werden oder überhaupt nicht ausgeführt werden.
ms.assetid: 1567d9d3-7839-42f0-9507-7bbf61d8eaf2
title: Transaktionale Message Queuing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4730b20f4014cdf7c76462d3f2cae272695d907
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041401"
---
# <a name="transactional-message-queuing"></a>Transaktionale Message Queuing

Bei einer *Transaktion* handelt es sich um eine Reihe von Änderungen eines Datenspeicher (z. b. einer Datenbank oder eines Dateisystems), die garantiert, dass Sie entweder erfolgreich ausgeführt werden oder überhaupt nicht ausgeführt werden. Zum Implementieren einer Transaktion wird ein Datensatz vor Beginn der Transaktion mit dem Zustand des Datenspeicher verbleibt. Wenn eine der Änderungen fehlschlägt, gibt die Transaktion einen Fehler zurück, und der ursprüngliche Zustand wird wieder hergestellt (oder Rollback). Transaktionen werden verwendet, um die Datenintegrität beizubehalten und somit eine wichtige Rolle bei der Programmierung von Geschäftssoftware zu spielen.

Anwendungen können häufig mithilfe einer Geschäftstransaktion oder eines Workflows entwickelt werden, der in verschiedene kleinere Transaktionen oder Aktivitäten aufgeteilt ist. Diese Aktivitäten werden zeitlich getrennt und dann mithilfe zuverlässiger Nachrichten Warteschlangen verbunden.

1.  Die erste Transaktion umfasst die Auftrags Eintrags Datenbank. [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) verschiebt die Nachricht genau einmal mithilfe von Transaktionsfunktionen aus einer Warteschlange in eine andere Warteschlange. Wenn die Datenbank aktualisiert wird, wird eine Meldung in der Warteschlange angezeigt. Wenn die Nachricht die Warteschlange nicht erreicht, wird Sie abgebrochen, und für die Datenbank wird ein Rollback ausgeführt.
2.  Zu einem späteren Zeitpunkt stellt Message Queuing fest, dass der Server verfügbar ist. Es gibt keinen Anwendungs Abruf für das vorhanden sein des Servers. Dies ist die zweite Transaktion.
3.  Die dritte Transaktion umfasst eine Versanddaten Bank Abfrage und das Update der Versand Datenbank. Wenn der Server in der Mitte der Transaktion ausfällt, wird für die Änderung ein Rollback ausgeführt, und die Nachricht wird an die Eingabe Warteschlange zurückgegeben. Dadurch wird sichergestellt, dass die Integrität der Daten und Datenbanken während der Transaktionen beibehalten wird.

 

 



