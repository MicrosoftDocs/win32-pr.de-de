---
description: Es gibt fünf Arten von Ereignissen, die protokolliert werden können. Alle diese verfügen über klar definierte allgemeine Daten und können optional ereignisspezifische Daten einschließen.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Ereignistypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3832f90ccdb8dafc676c139f92665efde732533c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864244"
---
# <a name="event-types"></a>Ereignistypen

Es gibt fünf Arten von Ereignissen, die protokolliert werden können. Alle diese verfügen über klar definierte allgemeine Daten und können optional ereignisspezifische Daten einschließen.

Die Anwendung gibt den Ereignistyp an, wenn ein Ereignis gemeldet wird. Jedes Ereignis muss einen einzelnen Typ aufweisen. Die Ereignisanzeige zeigt ein anderes Symbol für jeden Typ in der Listenansicht des Ereignis Protokolls an.

In der folgenden Tabelle werden die fünf bei der Ereignisprotokollierung verwendeten Ereignis Typen beschrieben.



| Ereignistyp        | BESCHREIBUNG                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fehler**         | Ein Ereignis, das auf ein erhebliches Problem hinweist, z. b. Datenverlust oder Funktionsverlust. Wenn beispielsweise ein Dienst beim Starten nicht geladen werden kann, wird ein Fehler Ereignis protokolliert.                                                                                                                           |
| **Warnung**       | Ein Ereignis, das nicht unbedingt wichtig ist, aber möglicherweise auf ein mögliches zukünftiges Problem hinweist. Wenn z. b. Speicherplatz auf dem Datenträger niedrig ist, wird ein Warn Ereignis protokolliert. Wenn eine Anwendung nach einem Ereignis ohne Verlust von Funktionen oder Daten wieder hergestellt werden kann, kann Sie das Ereignis in der Regel als Warn Ereignis klassifizieren.     |
| **Information**   | Ein Ereignis, das den erfolgreichen Betrieb einer Anwendung, eines Treibers oder eines Dienstanbieter beschreibt. Wenn ein Netzwerktreiber z. b. erfolgreich geladen wird, kann es sinnvoll sein, ein Informations Ereignis zu protokollieren. Beachten Sie, dass es für eine Desktop Anwendung grundsätzlich ungeeignet ist, bei jedem Start ein Ereignis zu protokollieren. |
| **Erfolgsüberwachung** | Ein Ereignis, das einen erfolgreichen überwachten Sicherheits Zugriffs Versuch aufzeichnet. Beispielsweise wird der Versuch eines Benutzers, sich am System anzumelden, als Erfolgs Überwachungs Ereignis protokolliert.                                                                                                                        |
| **Fehlerüberwachung** | Ein Ereignis, das einen überwachten Sicherheits Zugriffs Versuch aufzeichnet, der fehlschlägt. Wenn ein Benutzer beispielsweise versucht, auf ein Netzwerklaufwerk zuzugreifen und einen Fehler verursacht, wird der Versuch als Fehler Überwachungs Ereignis protokolliert.                                                                                                                   |



 

Die ausgewählten Aktivitäten von Benutzern können durch die Überwachung von Sicherheits Ereignissen und das anschließende Platzieren von Einträgen im Sicherheitsprotokoll eines Computers verfolgt werden.

 

 



