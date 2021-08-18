---
description: LOCALE \_ SDURATION
ms.assetid: 45ffd7ed-f964-4948-8679-cf960b5c1e0e
title: LOCALE_SDURATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb7031c5e9ddc3173fe7f10117eaad8c72820b1d3b81a82da33f6541901a933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147363"
---
# <a name="locale_sduration"></a>LOCALE \_ SDURATION

**Windows Vista und höher:** Zeitdauerformat, das aus Formatbildern besteht, die in der folgenden Tabelle aufgeführt sind. Das Format ähnelt dem Format für [LOCALE \_ STIMEFORMAT](locale-stime-constants.md). Wie bei LOCALE \_ STIMEFORMAT kann dieses Format auch eine beliebige Zeichenfolge enthalten, die in einfache Anführungszeichen eingeschlossen ist. Formate können z.B. "h:mm:ss" oder "d'd 'h'h 'm'm 's.fff's'" enthalten. Im Vergleich zu LOCALE \_ STIMEFORMAT gibt es zusätzliche Formatbilder für Sekundenbruchteile. Da dieses Format für die Dauer und nicht für die Uhrzeit gilt, gibt es weder ein 12- oder 24-Stunden-System an, noch enthält es einen AM/PM-Indikator. Diese Konstante kann z. B. für eine Mehrmedienanwendung verwendet werden, die die Dateizeit anzeigt, oder für eine Ereignisanwendung mit Abschlusszeiten.



| Wert | Bedeutung                                                                                                                                                                                                                             |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| h.     | Stunden ohne führende Nullen für einstellige Stunden                                                                                                                                                                                  |
| hh    | Stunden mit führenden Nullen für einstellige Stunden                                                                                                                                                                                     |
| m     | Minuten ohne führende Nullen für einstellige Minuten                                                                                                                                                                              |
| MM    | Minuten mit führenden Nullen für einstellige Minuten                                                                                                                                                                                 |
| s     | Sekunden ohne führende Nullen für einstellige Sekunden                                                                                                                                                                              |
| ss    | Sekunden mit führenden Nullen für einstellige Sekunden                                                                                                                                                                                 |
| f     | Zehntelsekunde                                                                                                                                                                                                                  |
| ff    | Hundertstelsekunde                                                                                                                                                                                                              |
| fff   | Tausendstel einer Sekunde; Das Zeichen "f" kann bis zu neun aufeinander folgende Male auftreten (fffffffff), obwohl die Unterstützung für Frequenztimer auf 100 Nanosekunden beschränkt ist. Wenn neun Zeichen vorhanden sind, sind die letzten beiden Ziffern immer 0 (null). |



 

 

 



