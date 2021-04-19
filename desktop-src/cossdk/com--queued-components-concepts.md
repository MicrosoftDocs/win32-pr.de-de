---
description: Konzepte der com+-Warteschlangen
ms.assetid: ff11e251-311f-4612-8f0d-a4cbc5b4d872
title: Konzepte der com+-Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d1a8983e84d817e402454392ce95fc2b07a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341124"
---
# <a name="com-queued-components-concepts"></a>Konzepte der com+-Warteschlangen

Basierend auf [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Diensten bietet der in der Warteschlange befindliche Komponenten Dienst eine einfache Möglichkeit zum asynchronen Aufrufen und Ausführen von-Komponenten. Die Verarbeitung kann ohne Rücksicht auf die Verfügbarkeit oder den Zugriff des Absenders oder des Empfängers erfolgen.

In com-begriffen ist eine *Warteschlange* ein Speicherbereich, der Nachrichten für den späteren Abruf speichert. Queueing bietet einen Mechanismus für die verbindungslose Kommunikation. Das heißt, dass der Absender und der Empfänger nicht direkt verbunden sind und nur über Warteschlangen kommunizieren. Warteschlangen bieten eine Möglichkeit, die Informationen zu speichern, bis der Empfänger zum Abrufen bereit ist. Der Absender und der Empfänger kommunizieren indirekt, sodass jede unabhängig voneinander betrieben werden kann, von der anderen nicht betroffen.

In der Vergangenheit war das Marshalling sehr ausführlich, um asynchrone Nachrichten in die Warteschlange zu stellen, zu senden und zu empfangen. Mithilfe von Methoden aufrufen, die von Komponentenentwicklern leicht verständlich und verwendet werden, marshallt der com+-Dienst für Warteschlangen Komponenten automatisch Daten in Form einer Message Queuing Nachricht. Und da der Dienst für in der Warteschlange befindliche Komponenten integrierte Unterstützung für Transaktionen bietet, kann ein inkonsistenter Status keine Daten beeinträchtigen, wenn ein Server Fehler auftritt.

Die folgenden Themen in diesem Abschnitt enthalten Hintergrundinformationen zum Entwerfen und Schreiben von Komponenten in der Warteschlange.



| Thema                                                                           | BESCHREIBUNG                                                                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Vorteile der Verarbeitung in der Warteschlange](benefits-of-queued-processing.md)<br/>   | Beschreibt die Vorteile der Programmierung mit COM+-Komponenten in der Warteschlange.<br/>                                         |
| [Architektur der Warteschlangen Komponenten](queued-components-architecture.md)<br/> | Beschreibt die Architektur des com+-Dienstanbieter für die Warteschlange.<br/>                                          |
| [Transaktionale Message Queuing](transactional-message-queuing.md)<br/>   | Beschreibt, wie Transaktionen vom com+-Dienst in der Warteschlange verarbeitet werden.<br/>                              |
| [Sicherheit in der Warteschlange befindliche Komponenten](queued-components-security.md)<br/>         | Beschreibt die Richtlinien Optionen für die Authentifizierung von Client Nachrichten und deren Auswirkungen.<br/>                 |
| [Entwickeln von Komponenten in der Warteschlange](developing-queued-components.md)<br/>     | Beschreibt Überlegungen zur Programmierung beim Schreiben von Warteschlangen fähigen Komponenten.<br/>                                     |
| [Komponenten Fehler in der Warteschlange](queued-components-errors.md)<br/>             | Beschreibt die häufigsten Fehlertypen, die auftreten können, wenn Sie den com+-Dienst in der Warteschlange verwenden.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgaben in der com+-Warteschlange](com--queued-components-tasks.md)
</dt> </dl>

 

 




