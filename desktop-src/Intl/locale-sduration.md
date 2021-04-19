---
description: LOCALE \_ sduration
ms.assetid: 45ffd7ed-f964-4948-8679-cf960b5c1e0e
title: LOCALE_SDURATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00740d2f041794b36e8f0e0d8ad2d25723bc12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354240"
---
# <a name="locale_sduration"></a>LOCALE \_ sduration

**Windows Vista und höher:** Das Zeitdauer-Format, das aus den in der folgenden Tabelle aufgeführten Format Abbildungen besteht. Das Format ähnelt dem Format für das [locale \_ stimeformat](locale-stime-constants.md). Wie bei locale \_ stimeformat kann dieses Format auch eine beliebige Zeichenfolge enthalten, die in einfache Anführungszeichen eingeschlossen ist. Formate können z. b. "h:mm: SS" oder "d 'd ' has. fff '" enthalten. Im Vergleich zum locale \_ stimeformat gibt es zusätzliche Format Abbildungen für Bruchteile einer Sekunde. Da dieses Format für die Dauer und nicht für die Zeit gilt, wird kein 12-oder 24-Stunden-System angegeben, oder es ist ein am/pm-Indikator enthalten. Diese Konstante kann z. b. für eine Anwendung mit mehreren Medien verwendet werden, die Datei Zeit oder eine Sportereignis Anwendung anzeigt, in der die Endzeit angezeigt wird.



| Wert | Bedeutung                                                                                                                                                                                                                             |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| h.     | Stunden ohne führende Nullen für Einstellige Stunden                                                                                                                                                                                  |
| hh    | Stunden mit führenden Nullen für Einstellige Stunden                                                                                                                                                                                     |
| m     | Minuten ohne führende Nullen für Einstellige Minuten                                                                                                                                                                              |
| MM    | Minuten mit führenden Nullen für Einstellige Minuten                                                                                                                                                                                 |
| s     | Sekunden ohne führende Nullen für Einstellige Sekunden                                                                                                                                                                              |
| ss    | Sekunden mit führenden Nullen für Einstellige Sekunden                                                                                                                                                                                 |
| f     | Zehntelsekunden                                                                                                                                                                                                                  |
| ff    | Hundertstel Sekunden                                                                                                                                                                                                              |
| fff   | Tausendstel Sekunde; das Zeichen "f" kann bis zu neun aufeinanderfolgende Zeit (fffffffff) vorkommen, auch wenn die Unterstützung für Häufigkeits Timer auf 100 Nanosekunden beschränkt ist. Wenn neun Zeichen vorhanden sind, sind die letzten zwei Ziffern immer 0 (null). |



 

 

 



