---
description: Das Windows-Betriebssystem sammelt eine Reihe von Betriebs Statistiken für Arbeitsstationen und Server ab dem Zeitpunkt, zu dem die Arbeitsstation oder der Server Dienst gestartet wurde.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Statistikfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce62e12f3c4894ba86ff5e5aaaa38801d272195c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352451"
---
# <a name="statistics-functions"></a>Statistikfunktionen

Das Windows-Betriebssystem sammelt eine Reihe von Betriebs Statistiken für Arbeitsstationen und Server ab dem Zeitpunkt, zu dem die Arbeitsstation oder der Server Dienst gestartet wurde. Zum Abrufen dieser Statistiken können Sie die folgende Funktion zur Netzwerk Verwaltungs Statistik aufrufen.



| Funktion                                     | BESCHREIBUNG                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [**Netstatisticsget**](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | Ruft Betriebs Statistiken für einen Dienst ab. unterstützt die Arbeitsstations-und Server Dienste. |



 

Die **netstatisticsget** -Funktion gibt eine [**stat-Arbeitsstation \_ \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) -Struktur zurück, wenn Arbeitsstations Statistiken angefordert werden. die Funktion gibt eine [**stat \_ Server \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) -Struktur zurück, wenn Server Statistiken angefordert werden.

 

 



