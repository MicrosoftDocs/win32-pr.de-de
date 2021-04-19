---
description: Erläutert Überlegungen zur Implementierung von Kenn Wortfilter-Exportfunktionen.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Überlegungen zur Kenn Wort Filter Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad13a52f66c29142248ca07179d8692887b1acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339777"
---
# <a name="password-filter-programming-considerations"></a>Überlegungen zur Kenn Wort Filter Programmierung

Beachten Sie beim Implementieren von Exportfunktionen für Kenn [*Wortfilter*](/windows/desktop/SecGloss/p-gly) Folgendes:

-   Gehen Sie bei der Arbeit mit nur-Text- [*Kenn Wörtern sehr*](/windows/desktop/SecGloss/p-gly) vorsichtig vor. Das Senden von nur-Text-Kenn Wörtern über Netzwerke kann die Sicherheit beeinträchtigen. Netzwerk "Sniffer" kann problemlos auf Klartext-Kenn Wort Datenverkehr achten.
-   Löschen Sie den gesamten Speicher, der zum Speichern von Kenn Wörtern verwendet wird, indem Sie die [**securezeromemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) -Funktion aufrufen, bevor
-   Alle Puffer, die an die Kenn Wort Benachrichtigung und Filter Routinen weitergeleitet werden, sollten als schreibgeschützt behandelt werden. Das Schreiben von Daten in diese Puffer kann ein instabiles Verhalten verursachen.
-   Alle Kenn Wort Benachrichtigungen und Filter Routinen sollten Thread sicher sein. Verwenden Sie wichtige Abschnitte oder andere synchrone Programmiertechniken, um Daten bei Bedarf zu schützen.
-   Kenn Wort Benachrichtigung und-Filterung erfolgen nur auf dem Computer, auf dem sich das Konto befindet.
-   Alle Domänen Controller können beschreibbar sein. Daher müssen Kenn Wortfilter Pakete auf allen Domänen Controllern vorhanden sein.

    **Windows NT 4,0-Domänen:** Die Benachrichtigung über Domänen Konten findet nur auf dem primären Domänen Controller statt. Zusätzlich zum primären Domänen Controller sollten die Kenn Wortfilter Pakete auf allen Sicherungs Domänen Controllern installiert werden, damit Benachrichtigungen bei Änderungen an der Server Rolle fortgesetzt werden können.

-   Alle Kenn Wortfilter-DLLs werden im [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des lokalen System Kontos ausgeführt.



| Informationen über                                                                                                                     | Finden Sie unter                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Installieren und Registrieren Ihrer eigenen Kenn [*Wortfilter*](/windows/desktop/SecGloss/p-gly) -dll. | [Installieren und Registrieren einer Kenn Wort Filter-dll](installing-and-registering-a-password-filter-dll.md) |
| Die von Microsoft bereitgestellte Kenn Wortfilter-dll.                                                                                            | [Starke Kenn Wort Erzwingung und Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)         |
| Export Funktionen, die von einer Kenn Wortfilter-dll implementiert werden.                                                                                    | [Kenn Wort Filter Funktionen](management-functions.md)                          |



 

 

 
