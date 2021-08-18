---
description: Bei einer Transaktion handelt es sich um eine Reihe von Änderungen an einem Datenspeicher (z. B. einer Datenbank oder einem Dateisystem), bei der garantiert wird, dass alle erfolgreich ausgeführt werden oder überhaupt nicht ausgeführt werden.
ms.assetid: 1567d9d3-7839-42f0-9507-7bbf61d8eaf2
title: Transaktionale Message Queuing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3282a95d4f9a3ba451e78fe4d9f17acf007b0007abea4fdb4951de9c1540383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636730"
---
# <a name="transactional-message-queuing"></a>Transaktionale Message Queuing

Bei einer *Transaktion* handelt es sich um eine Reihe von Änderungen an einem Datenspeicher (z. B. einer Datenbank oder einem Dateisystem), bei der garantiert wird, dass alle erfolgreich ausgeführt werden oder überhaupt nicht ausgeführt werden. Um eine Transaktion zu implementieren, wird ein Datensatz des Zustands des Datenspeichers beibehalten, bevor die Transaktion beginnt. Wenn eine der Änderungen fehlschlägt, gibt die Transaktion einen Fehler zurück, und der anfängliche Zustand wird wiederhergestellt (oder ein Rollback ausgeführt). Transaktionen werden verwendet, um die Datenintegrität aufrechtzuerhalten, und spielen daher eine wichtige Rolle bei der Programmierung von Geschäftssoftware.

Anwendungen können häufig mithilfe einer Geschäftstransaktion oder eines Workflows entwickelt werden, die in mehrere kleinere Transaktionen oder Aktivitäten aufgeteilt sind. Diese Aktivitäten werden zeitlich getrennt und dann über zuverlässige Nachrichtenwarteschlangen verbunden.

1.  Die erste Transaktion umfasst die Datenbank für den Auftragseintrag. [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) verschiebt die Nachricht mithilfe von Transaktionsfunktionen genau einmal aus einer Warteschlange in eine andere. Wenn die Datenbank aktualisiert wird, wird eine Meldung in der Warteschlange angezeigt. Wenn die Nachricht die Warteschlange nicht erreicht, wird sie abgebrochen, und für die Datenbank wird ein Rollback ausgeführt.
2.  Zu einem späteren Zeitpunkt ermittelt Message Queuing, dass der Server verfügbar ist. Es gibt keine Anwendungsumfrage, ob der Server vorhanden ist. Dies ist die zweite Transaktion.
3.  Die dritte Transaktion umfasst eine Abfrage der Versanddatenbank und die Aktualisierung der Versanddatenbank. Wenn der Server in der Mitte dieser Transaktion ausfällt, wird für die Änderung ein Rollback ausgeführt, und die Nachricht wird an die Eingabewarteschlange zurückgegeben. Dadurch wird sichergestellt, dass die Integrität der Daten und Datenbanken während der Transaktionen erhalten bleibt.

 

 



