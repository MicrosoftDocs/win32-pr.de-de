---
description: COM+-Nachverfolgung
ms.assetid: ad3bdeb5-f303-411a-abfb-ccde3f9a86b9
title: COM+-Nachverfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069d910f0c559776125342b861e71566fb20f45231f960b1c1dcb18262171926
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029490"
---
# <a name="com-tracking"></a>COM+-Nachverfolgung

Mit dem COM+-Nachverfolgungsdienst können Sie eigene Verwaltungs- und Diagnoseprogramme erstellen, die den Status und die Leistung ausgeführter COM+-Anwendungen nachverfolgen. Die COM+-Nachverfolgung bietet statistische Informationen zur Verwendung von COM+-Anwendungen sowie Statusinformationen, z. B. ob eine COM+-Serveranwendungsinstanz angehalten oder wiederverwendet wurde. Tools können Nachverfolgungsinformationen in der Diagnoseüberwachung oder zu Anzeigezwecken verwenden. Beispielsweise verwendet das Verwaltungstool komponentendienste die COM+-Nachverfolgung, um den Status von COM+-Anwendungsinstanzen in den Ordnern COM+-Anwendungen und Ausgeführte Prozesse anzuzeigen.

Die COM+-Nachverfolgung berechnet und aktualisiert in regelmäßigen Abständen einen Satz häufig verwendeter Metriken, wodurch diese Informationen für Programme verfügbar sind, die sie benötigen. Dies ähnelt der COM+-Instrumentierung, da beide Dienste automatisch Daten von COM+-Anwendungsinstanzen sammeln und für Kunden verfügbar machen. Es gibt jedoch einige wichtige Unterschiede zwischen diesen Diensten, sowohl in der bereitgestellten Funktionalität als auch in der typischen Verwendung. In der folgenden Tabelle werden diese Unterschiede zusammengefasst.



| COM+-Instrumentierung                                                                                                                                                                                                   | COM+-Nachverfolgung                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fein abgrenzende Daten. Der COM+-Instrumentierungsdienst benachrichtigt registrierte Abonnenten über einzelne diskrete Ereignisse (z. B. methode namens , Objekt zerstört), die in einer COM+-Anwendungsinstanz auftreten.<br/> | Aggregierte Daten. Die COM+-Nachverfolgung berechnet und aktualisiert regelmäßig häufig verwendete Metriken für den Status und die Leistung von COM+-Anwendungsinstanzen.<br/> |
| Ereignisabonnenten berechnen Metriken in der Regel selbst mithilfe von Ad-hoc-Algorithmen und -Richtlinien.<br/>                                                                                                           | Metriken werden automatisch vom COM+-Nachverfolgungsdienst berechnet. Alle Benutzer erhalten dieselben Daten, ohne dass benutzerdefinierte Metriken unterstützt werden.<br/>                |
| Nach der Registrierung eines Abonnements erhält der Consumer erst dann Informationen zu einer COM+-Anwendungsinstanz, wenn ein Ereignis eintritt.<br/>                                                                    | Überwachungsdaten für alle COM+-Anwendungsinstanzen können jederzeit abgerufen werden.<br/>                                                                         |
| Unterstützt nur einen com+-ereignisbasierten Abonnementmechanismus für Kunden.<br/>                                                                                                                                     | Unterstützt sowohl einen com+-ereignisbasierten Abonnementmechanismus als auch das Abrufen auf einer lokalen COM-Serverschnittstelle.<br/>                                                  |
| Beispiele                                                                                                                                                                                                               |                                                                                                                                                                   |
| Benachrichtigungen, wenn eine Methode aufgerufen oder zurückgegeben wird.<br/>                                                                                                                                                           | Durchschnittliche Antwortzeit für Aufrufe, Anzahl von Methodenaufrufen, die in einem kürzlichen Zeitraum erfolgreich waren oder fehlgeschlagen sind, Anzahl von Objekten, die derzeit in einem Methodenaufruf enthalten sind.<br/>     |
| Benachrichtigungen, wenn ein Objekt dem Objektpool hinzugefügt oder daraus erhalten wird.<br/>                                                                                                                                  | Anzahl der Objekte im Pool, Gesamtzahl der Objekte.<br/>                                                                                                |
| Benachrichtigungen, wenn eine COM+-Serveranwendung gestartet, angehalten oder wiederverwendet wird.<br/>                                                                                                                               | Status des COM+-Serveranwendungsprozesses (z. B. ob er angehalten oder wiederverwendet wird).<br/>                                                         |
| Benachrichtigungen zu Transaktionsstart-, Vorbereitungs-, Abbruch- und Commitereignissen.<br/>                                                                                                                                      | Keine Entsprechung<br/>                                                                                                                                         |
| Benachrichtigungen über erfolgreiche und fehlgeschlagene Authentifizierungsversuche auf Methodenaufrufebene.<br/>                                                                                                                           | Keine Entsprechung<br/>                                                                                                                                         |



 

Obwohl die COM+-Nachverfolgung hinsichtlich des Datenumfangs und der Flexibilität bei der Berechnung von Metriken stärker eingeschränkt ist, sollten die bereitgestellten Metriken für eine Vielzahl von Verwaltungs- und Diagnoseprogrammen ausreichend sein. Die Verwendung der COM+-Nachverfolgung kann nach Möglichkeit den Entwurf dieser Programme vereinfachen. Darüber hinaus kann die Verwendung der COM+-Nachverfolgung in Produktionssystemen erheblich geringere Auswirkungen auf die Leistung haben, wodurch sie für Überwachungstools in Echtzeit besser geeignet ist.

## <a name="how-com-tracking-collects-data"></a>Sammeln von Daten durch die COM+-Nachverfolgung

Wenn ein COM+-Serveranwendungsprozess gestartet wird, registriert COM+ den Prozess beim *Trackerserver,* einer Komponente der Systemanwendung. Komponenten in COM+-Bibliotheksanwendungen und -Diensten ohne Komponentenkontexte (SWC) unterstützen ebenfalls die Nachverfolgung. Wenn eine Bibliothekskomponente oder ein SWC-Kontext in einem Prozess erstellt wird, registriert COM+ den Prozess beim Trackerserver, sofern er noch nicht registriert wurde.

COM+ aktualisiert Statistiken für einen nachverfolgten Prozess, wenn bestimmte Ereignisse im Prozess auftreten, z. B. die Erstellung eines Objekts oder das Ende eines Methodenaufrufs. Aktualisierte Daten werden in regelmäßigen Abständen an den Trackerserver übermittelt, an dem sie den Kunden zur Verfügung stehen. Der Trackerserver ist auch für die Berechnung einiger der Metriken verantwortlich, die von den Überwachungsfeatures für das Wiederverwerten und Hängen von COM+-Anwendungen verwendet werden. Diese Daten sind auch für Kunden verfügbar.

Nachverfolgungsdaten sind nach dem Prozess organisiert, der die Daten generiert hat. Daten auf der Ebene einzelner COM+-Anwendungen oder -Komponenten im Prozess sind auch für Benutzer verfügbar, die diese Informationen benötigen.

## <a name="events-versus-polling"></a>Ereignisse im Vergleich zu Abruf

Die COM+-Nachverfolgung unterstützt zwei Mechanismen für einen Consumer, um Nachverfolgungsdaten vom Trackerserver zu erhalten: einen COM+-ereignisbasierten Abonnementmechanismus und eine lokale COM-Serverschnittstelle.

Programme, die regelmäßig mit aktualisierten Nachverfolgungsdaten benachrichtigt werden müssen, können ein Abonnement für die [**IComTrackingInfoEvents-Ereignisschnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfoevents) registrieren. Ungefähr alle drei Sekunden ruft der Trackerserver die [**IComTrackingInfoEvents::OnNewTrackingInfo-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-icomtrackinginfoevents-onnewtrackinginfo) jedes Abonnenten auf und sendet die neuesten Nachverfolgungsdaten in Form eines Sammlungsobjekts. Dieses Objekt implementiert die [**IComTrackingInfoCollection-Schnittstelle,**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfocollection) und Abonnenten können in dieser Sammlung navigieren, um die Daten zu finden, an denen sie interessiert sind.

Aus verschiedenen Gründen kann es sinnvoller sein, dass ein Programm den Trackerserver nach Daten abruft. Beispielsweise benötigt ein Überwachungstool möglicherweise wesentlich seltener Updates als ein Programm, das den Status auf einer Benutzeroberfläche anzeigt. Außerdem kann ein Programm nur einen kleinen Teil der für das System verfügbaren Nachverfolgungsdaten verwenden (beispielsweise kann ein Tool nur die Leistung von Instanzen einer einzelnen COM+-Anwendung überwachen). Das Abonnementmodell sendet jedem Abonnenten die Nachverfolgungsdaten für alle COM+-Anwendungen in jeder Benachrichtigung, und der Abonnent ist dafür verantwortlich, die daten zu finden, die er möchte. Com+-Ereignisse sind schließlich ein bestmöglicher Mechanismus für Ereignisbenachrichtigungen. Zuverlässige Nachrichtenbereitstellungsdienste werden nicht bereitgestellt, und ein Abonnent kann nicht erkennen, dass der Trackerserver ihm keine Benachrichtigung senden konnte.

Ein Programm, das mehr Kontrolle über den Abruf von Nachverfolgungsdaten benötigt, kann die [**IGetAppTrackerData-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-igetapptrackerdata) des Trackerservers verwenden.

 

 




