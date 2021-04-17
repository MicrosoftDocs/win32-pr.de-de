---
description: Problembehandlung bei com+ CRM
ms.assetid: 4d2d9372-b540-4e08-9b57-8687802610b6
title: Problembehandlung bei com+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b04e37d183dbf3df8d017e780917f955e14a033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523864"
---
# <a name="troubleshooting-the-com-crm"></a>Problembehandlung bei com+ CRM

Im folgenden finden Sie die häufigsten Probleme, die bei der Entwicklung und Verwendung von com+ CRM aufgetreten sind:

-   **Ereignisprotokoll Meldungen.** Wenn die CRM-Serveranwendung einen schwerwiegenden internen Fehler feststellt, wird ein faildown durchführt (der Prozess der CRM-Serveranwendung wird beendet) und eine Meldung in das Windows-Ereignisprotokoll geschrieben. Wenn Probleme auftreten, lesen Sie das Ereignisprotokoll.

-   **Ausnahmen vom CRM-kompenator.** Die CRM-Infrastruktur erstellt den CRM-Compensator und übergibt die Transaktions Ergebnis Benachrichtigungen und die Protokolldaten Sätze, die vom CRM-Worker geschrieben wurden. Wenn der CRM-kompenerer einen Fehler zurückgibt oder eine Ausnahme auslöst, wird er von der CRM-Infrastruktur abgefangen und führt zu einem FailFast. Eine Meldung im Ereignisprotokoll zeigt an, dass eine Ausnahme vom CRM-kompenatordienst empfangen wurde. Sie können erzwingen, dass diese Ausnahmen ignoriert werden. (Siehe [com+ CRM-Registrierungs Einstellungen](com--crm-registry-settings.md).) Ausnahmen vom CRM-Compensator bedeuten höchstwahrscheinlich ein Problem in der spezifischen CRM-kompenatorkomponente und nicht in der CRM-Infrastruktur selbst.

-   **Wiederherstellungs Ablauf Verfolgung.** Die Wiederherstellungs Ablauf Verfolgung kann sehr nützlich sein, um Probleme bei der Wiederherstellung zu ermitteln. Weitere Informationen zum Aktivieren der Wiederherstellungs Ablauf Verfolgung finden Sie unter [com+ CRM-Registrierungs Einstellungen](com--crm-registry-settings.md).

-   **Der Versuch, mit dem CRM auszuführen, ist nicht aktiviert.** Es genügt nicht, einfach die CRM-Worker-und CRM-kompenatorkomponenten in der COM+-Serveranwendung zu platzieren. Die Unterstützung von CRMs muss speziell für die jeweilige COM+-Serveranwendung aktiviert werden. verwenden Sie dazu die Option **kompensierende Ressourcen-Manager aktivieren** auf der Registerkarte **erweitert** der Eigenschaften Seiten der com+-Anwendung. (Weitere Informationen finden Sie unter [Konfigurieren von com+ CRM-Komponenten](configuring-com--crm-components.md) .) Wenn versucht wird, ein CRM innerhalb einer Serveranwendung zu verwenden, für die das CRM nicht aktiviert ist, wird ein Fehlercode an den CRM-Worker zurückgegeben.

-   **Es wird versucht, CRMs in Client Prozessen auszuführen.** CRMs werden nicht in Client Prozessen ausgeführt. Sie müssen in einem com+-Server Anwendungsprozess ausgeführt werden. CRM-Komponenten können in ein Bibliothekspaket eingefügt werden, das von mehreren com+-Server Anwendungen verwendet werden kann. Sie sind jedoch nicht für die Verwendung in Client Prozessen verfügbar. Wenn Sie versuchen, die CRM-Schnittstellen innerhalb eines Client Prozesses zu verwenden, wird dem CRM-Worker ein Fehlercode zurückgegeben.

-   **Wiederherstellung wird durchgeführt.** Die Wiederherstellung beginnt, wenn eine CRM-Serveranwendung gestartet wird. Die Wiederherstellung erfolgt jedoch im Hintergrund während der normalen Verarbeitung der CRM-Serveranwendung. Der CRM-Worker kann erstellt werden, bevor die Wiederherstellung abgeschlossen ist. CRMs können erst dann in einem CRM-Server Anwendungsprozess verwendet werden, wenn die Wiederherstellung erfolgreich abgeschlossen wurde. In diesem Fall empfängt der CRM-Worker den Fehlercode "Wiederherstellung in Bearbeitung", während er versucht, den CRM-kompenerer zu registrieren. Der CRM-Worker sollte Abfragen oder anderweitig verzögern, bis die Wiederherstellung abgeschlossen ist. Die Wiederherstellungszeit ist für eine bestimmte Art von CRM spezifisch und sollte beim Entwerfen von CRM berücksichtigt werden. Lange Wiederherstellungen sind nicht wünschenswert.

-   **Sicherheit in der CRM-Protokolldatei.** Wenn der Zugriff auf die CRM-Protokolldatei verweigert wird, finden Sie unter [com+ CRM-Sicherheitsüberlegungen](com--crm-security-considerations.md) eine Beschreibung, wie die Sicherheit für die CRM-Protokolldatei festgelegt wird.

-   **Unsichere Transaktionen.** In seltenen Fällen kann es vorkommen, dass eine DTC-Transaktion in den zweifelhaften Zustand wechselt. Das heißt, der DTC kann das Transaktions Ergebnis nicht ermitteln. In diesen Fällen verwaltet das CRM während der Wiederherstellung die Protokolldaten Sätze für diese Transaktion in der CRM-Protokolldatei. Wenn die unsichere Transaktion vom DTC aufgelöst wurde, wird die Transaktion durch das Ausführen einer anderen CRM-Wiederherstellung abgeschlossen.

-   **Erstellung und Freigabe von CRM Compensator.** Wenn ein CRM-Compensator zum ersten Mal von einem CRM-Worker registriert wird, wird er von der CRM-Infrastruktur erstellt und abgefragt, um zu bestimmen, welche der von ihm unterstützten CRM-compensatorschnittstellen unterstützt werden. Sie wird dann sofort freigegeben. CRM-Kompensatoren müssen die Möglichkeit der Erstellung und Freigabe unterstützen, ohne dass dazwischen liegende Methodenaufrufe vorhanden sind. Wenn der CRM-Compensator nicht ordnungsgemäß erstellt werden kann, möglicherweise aufgrund einer falschen com-Registrierung, oder wenn er nicht mindestens eine der richtigen CRM-kompenatorschnittstellen unterstützt, wird ein Fehlercode an den CRM-Worker zurückgegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompensierende com+-Ressourcen-Manager Konzepte](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



