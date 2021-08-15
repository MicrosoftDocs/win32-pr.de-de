---
description: Das Windows sammelt ab dem Start der Arbeitsstation oder des Serverdiensts eine Reihe von Betriebsstatistiken für Arbeitsstationen und Server.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Statistikfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2261f0c4f8f8249b401e658759827d6471d3ac47b6eb10df769ad5f37d8ce7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063590"
---
# <a name="statistics-functions"></a>Statistikfunktionen

Das Windows sammelt ab dem Start der Arbeitsstation oder des Serverdiensts eine Reihe von Betriebsstatistiken für Arbeitsstationen und Server. Um diese Statistiken abzurufen, können Sie die folgende Netzwerkverwaltungsstatistikfunktion aufrufen.



| Funktion                                     | BESCHREIBUNG                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [**NetStatisticsGet**](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | Ruft Betriebsstatistiken für einen Dienst ab. unterstützt die Arbeitsstations- und Serverdienste. |



 

Die **NetStatisticsGet-Funktion** gibt eine [**STAT \_ WORKSTATION \_ 0-Struktur**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) zurück, wenn Arbeitsstationsstatistiken angefordert werden. Die Funktion gibt eine [**STAT SERVER \_ \_ 0-Struktur**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) zurück, wenn Serverstatistiken angefordert werden.

 

 



