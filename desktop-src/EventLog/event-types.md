---
description: Es gibt fünf Arten von Ereignissen, die protokolliert werden können. Alle diese Verfügen über klar definierte allgemeine Daten und können optional ereignisspezifische Daten enthalten.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Ereignistypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e94ae69445f660e54c630734b93297acad593c127f32b9d3abfa94f9cd2fc06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069560"
---
# <a name="event-types"></a>Ereignistypen

Es gibt fünf Arten von Ereignissen, die protokolliert werden können. Alle diese Verfügen über klar definierte allgemeine Daten und können optional ereignisspezifische Daten enthalten.

Die Anwendung gibt den Ereignistyp an, wenn sie ein Ereignis meldet. Jedes Ereignis muss einen einzelnen Typ haben. Der Ereignisanzeige zeigt ein anderes Symbol für jeden Typ in der Listenansicht des Ereignisprotokolls an.

In der folgenden Tabelle werden die fünf Ereignistypen beschrieben, die in der Ereignisprotokollierung verwendet werden.



| Ereignistyp        | Beschreibung                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fehler**         | Ein Ereignis, das auf ein erhebliches Problem hindeutet, z. B. Datenverlust oder Funktionsverlust. Wenn ein Dienst beispielsweise während des Starts nicht geladen werden kann, wird ein Fehlerereignis protokolliert.                                                                                                                           |
| **Warnung**       | Ein Ereignis, das nicht unbedingt von Bedeutung ist, aber auf ein mögliches zukünftiges Problem hinweisen kann. Wenn beispielsweise wenig Speicherplatz verfügbar ist, wird ein Warnungsereignis protokolliert. Wenn eine Anwendung nach einem Ereignis ohne Funktions- oder Datenverlust wiederhergestellt werden kann, kann sie das Ereignis im Allgemeinen als Warnungsereignis klassifizieren.     |
| **Information**   | Ein Ereignis, das den erfolgreichen Betrieb einer Anwendung, eines Treibers oder eines Diensts beschreibt. Wenn ein Netzwerktreiber beispielsweise erfolgreich geladen wird, kann es sinnvoll sein, ein Informationsereignis zu protokollieren. Beachten Sie, dass es für eine Desktopanwendung im Allgemeinen ungeeignet ist, ein Ereignis bei jedem Start zu protokollieren. |
| **Erfolgsüberwachung** | Ein Ereignis, das einen erfolgreichen überwachten Sicherheitszugriffsversuch auf zeichnet. Beispielsweise wird der erfolgreiche Anmeldeversuch eines Benutzers beim System als Erfolgsüberwachungsereignis protokolliert.                                                                                                                        |
| **Fehlerüberwachung** | Ein Ereignis, das einen überwachten Sicherheitszugriffsversuch auf zeichnet, der fehlschlägt. Wenn ein Benutzer beispielsweise versucht, auf ein Netzwerklaufwerk zu zugreifen, und ein Fehler auftritt, wird der Versuch als Fehlerüberwachungsereignis protokolliert.                                                                                                                   |



 

Ausgewählte Aktivitäten von Benutzern können nachverfolgt werden, indem Sicherheitsereignisse nachverfolgt und dann Einträge im Sicherheitsprotokoll eines Computers platziert werden.

 

 



