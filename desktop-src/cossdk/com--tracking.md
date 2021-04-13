---
description: Com+-Nachverfolgung
ms.assetid: ad3bdeb5-f303-411a-abfb-ccde3f9a86b9
title: Com+-Nachverfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 828cc87b5a24363fd814d37c29e61a3ce204d988
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483062"
---
# <a name="com-tracking"></a>Com+-Nachverfolgung

Der com+-Überwachungsdienst ermöglicht es Ihnen, eigene administrative und Diagnoseprogramme zu erstellen, die den Status und die Leistung der Ausführung von com+-Anwendungen nachverfolgen. Die COM+-Nachverfolgung bietet statistische Informationen zur Verwendung von com+-Anwendungen sowie Statusinformationen, z. b. ob eine com+-Server Anwendungs Instanz angehalten oder wieder verwendet wurde. Tools können Überwachungsinformationen in der Diagnose Überwachung oder zu Anzeige Zwecken verwenden. Das Verwaltungs Programmkomponenten Dienste verwendet beispielsweise die com+-Überwachung, um den Status der com+-Anwendungs Instanzen in den Ordnern com+-Anwendungen und ausgestellte Prozesse anzuzeigen.

Bei der com+-Nachverfolgung wird eine Reihe häufig verwendeter Metriken berechnet und regelmäßig aktualisiert, sodass diese Informationen für Programme zur Verfügung stehen, die Sie benötigen. Es ähnelt der com+-Instrumentation darin, dass beide Dienste automatisch Daten aus com+-Anwendungs Instanzen sammeln und diese Daten für Consumer verfügbar machen. Es gibt jedoch einige wichtige Unterschiede zwischen diesen Diensten, sowohl in der bereitgestellten Funktionalität als auch in der typischen Verwendung. In der folgenden Tabelle werden diese Unterschiede zusammengefasst.



| Com+-Instrumentation                                                                                                                                                                                                   | Com+-Nachverfolgung                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenzierte Daten. Der com+-Instrumentations Dienst benachrichtigt registrierte Abonnenten über einzelne diskrete Ereignisse (z. b. die Methode, die als Objekt zerstört bezeichnet wird), die in einer com+-Anwendungs Instanz auftreten.<br/> | Aggregierte Daten. Mit der com+-Nachverfolgung werden häufig verwendete Metriken für den Status und die Leistung von com+-Anwendungs Instanzen berechnet und regelmäßig aktualisiert.<br/> |
| Ereignis Abonnenten berechnen Metriken in der Regel selbst mithilfe von Ad-hoc-Algorithmen und-Richtlinien.<br/>                                                                                                           | Metriken werden automatisch vom com+-Überwachungsdienst berechnet. Alle Consumer erhalten dieselben Daten, ohne dass benutzerdefinierte Metriken unterstützt werden.<br/>                |
| Nachdem ein Abonnement registriert wurde, empfängt der Consumer keine Informationen über eine com+-Anwendungs Instanz, bis ein Ereignis eintritt.<br/>                                                                    | Überwachungsdaten für alle com+-Anwendungs Instanzen können jederzeit abgerufen werden.<br/>                                                                         |
| Unterstützt nur einen com+-ereignisbasierten Abonnement Mechanismus für Consumer.<br/>                                                                                                                                     | Unterstützt sowohl einen auf COM+-Ereignissen basierenden Abonnement Mechanismus als auch einen Abruf auf einer lokalen com-Server Schnittstelle.<br/>                                                  |
| Beispiele                                                                                                                                                                                                               |                                                                                                                                                                   |
| Benachrichtigungen, wenn eine Methode aufgerufen wird oder zurückgibt.<br/>                                                                                                                                                           | Durchschnittliche Antwortzeit des Aufrufs, Anzahl der Methodenaufrufe, die in einem letzten Zeitraum erfolgreich oder fehlerhaft waren, Anzahl der Objekte, die zurzeit in einem Methodenaufruf ausgeführt werden.<br/>     |
| Benachrichtigungen, wenn dem Objekt Pool ein Objekt hinzugefügt oder aus diesem abgerufen wird.<br/>                                                                                                                                  | Anzahl von Objekten im Pool, Gesamtzahl der Objekte.<br/>                                                                                                |
| Benachrichtigungen, wenn eine COM+-Serveranwendung gestartet, angehalten oder wieder verwendet wird.<br/>                                                                                                                               | Status des com+-Server Anwendungsprozesses (z. b. ob er angehalten oder wieder verwendet wird).<br/>                                                         |
| Benachrichtigungen zu Start-, Vorbereitungs-, Abbruch-und Commit-Ereignissen für Transaktionen.<br/>                                                                                                                                      | Keine Entsprechung<br/>                                                                                                                                         |
| Benachrichtigungen über erfolgreiche und fehlgeschlagene Authentifizierungs Versuche auf Methodenaufrufe.<br/>                                                                                                                           | Keine Entsprechung<br/>                                                                                                                                         |



 

Obwohl die COM+-Nachverfolgung im Hinblick auf den Datenbereich und die Flexibilität zum Berechnen von Metriken stärker eingeschränkt ist, sollten die von ihr bereitgestellten Metriken für eine Vielzahl von Verwaltungs-und Diagnose Programmen ausreichen. Wenn möglich, kann die Verwendung der com+-Nachverfolgung den Entwurf dieser Programme vereinfachen. Außerdem kann die Verwendung der com+-Nachverfolgung in Produktionssystemen zu einer erheblich geringeren Beeinträchtigung der Leistung führen, sodass Sie für echt Zeit Überwachungstools besser geeignet ist.

## <a name="how-com-tracking-collects-data"></a>Sammeln von Daten durch die COM+-Nachverfolgung

Wenn ein com+-Server Anwendungsprozess gestartet wird, registriert com+ den Prozess bei dem *Tracker-Server*, einer Komponente der Systemanwendung. Komponenten in COM+-Bibliotheksanwendungen und-Diensten ohne Komponenten (austauschen) unterstützen auch die Nachverfolgung. Wenn eine Bibliotheks Komponente oder ein Austausch Vorgang in einem Prozess erstellt wird, registriert com+ den Prozess bei dem Tracker-Server, wenn er nicht bereits registriert wurde.

Com+ aktualisiert Statistiken für einen nach verfolgten Prozess, wenn bestimmte Ereignisse im Prozess auftreten, z. b. das Erstellen eines Objekts oder der Abschluss eines Methoden Aufrufes. Aktualisierte Daten werden in regelmäßigen Abständen an den Tracker-Server übermittelt. zu diesem Zeitpunkt steht sie für Consumer zur Verfügung. Der Tracker-Server ist auch für die Berechnung einiger der Metriken verantwortlich, die von den Funktionen der com+-Anwendungs Wiederverwendung und-Überwachung verwendet werden. Diese Daten sind auch für Consumer verfügbar.

Überwachungsdaten werden nach dem Prozess organisiert, der die Daten generiert hat. Daten auf der Ebene einzelner com+-Anwendungen oder-Komponenten im Prozess sind auch für Consumer verfügbar, die diese Informationen benötigen.

## <a name="events-versus-polling"></a>Ereignisse im Vergleich zu Abfragen

Die COM+-Nachverfolgung unterstützt zwei Mechanismen für einen Consumer, um Überwachungsdaten vom Tracker-Server, einen com+-ereignisbasierten Abonnement Mechanismus und eine lokale com-Server Schnittstelle zu erhalten.

Programme, die in regelmäßigen Abständen mit aktualisierten Überwachungsdaten benachrichtigt werden müssen, können ein Abonnement für die [**icomtrackinginfoevents**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfoevents) -Ereignis Schnittstelle registrieren. Ungefähr alle drei Sekunden ruft der Tracker-Server die [**icomtrackinginfoevents:: onnewtrackinginfo**](/windows/desktop/api/ComSvcs/nf-comsvcs-icomtrackinginfoevents-onnewtrackinginfo) -Methode jedes Abonnenten auf und sendet die neuesten Überwachungsdaten in Form eines Auflistungs Objekts. Dieses Objekt implementiert die [**icomtrackinginfocollection**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfocollection) -Schnittstelle, und Abonnenten können durch diese Auflistung navigieren, um die für Sie interessanten Daten zu suchen.

Aus verschiedenen Gründen ist es möglicherweise sinnvoller, dass ein Programm nach Verfolgungs Server nach Daten abruft. Ein Überwachungs Tool benötigt z. b. möglicherweise weniger häufig Updates als ein Programm, das den Status auf einer Benutzeroberfläche anzeigt. Außerdem kann ein Programm nur einen kleinen Teil der für das System verfügbaren Überwachungsdaten verwenden (z. b. kann ein Tool nur die Leistung von Instanzen einer einzelnen COM+-Anwendung überwachen). Das Abonnement Modell sendet jeden Abonnenten die Überwachungsdaten für alle com+-Anwendungen in jeder Benachrichtigung, und der Abonnent muss die gewünschten Daten finden. Und schließlich handelt es sich bei com+-Ereignissen um einen bewährten Ereignis Benachrichtigungs Mechanismus. Es wurden keine zuverlässigen Nachrichtenübermittlungs Dienste bereitgestellt, und ein Abonnent kann nicht erkennen, dass der Tracker Server eine Benachrichtigung nicht senden konnte.

Ein Programm, das eine bessere Kontrolle über das Abrufen von Überwachungsdaten benötigt, kann die [**igetapptrackerdata**](/windows/desktop/api/ComSvcs/nn-comsvcs-igetapptrackerdata) -Schnittstelle des Tracker-Servers verwenden.

 

 




