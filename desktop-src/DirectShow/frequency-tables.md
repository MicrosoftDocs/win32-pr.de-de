---
description: Häufigkeits Tabellen
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Häufigkeits Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933152c7ac38eefe91468aff8bc3a8eb3ced05df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123560"
---
# <a name="frequency-tables"></a>Häufigkeits Tabellen

Der TV-Tuner-Filter (kstvtune.ax) verfügt über eine interne Liste der Häufigkeits Tabellen. Jede Häufigkeits Tabelle enthält eine Liste von Frequenzen und entspricht den Übertragungs-oder Kabel Frequenzen für ein bestimmtes Land bzw. eine bestimmte Region. Eine Anwendung optimiert auf eine bestimmte Häufigkeit, indem Sie die Methode [**iamtuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) mit dem Index der gewünschten Häufigkeit aufruft.

Für einige Länder/Regionen werden die Indexnummern der Häufigkeits Tabellen direkt den Kanalnummern zugeordnet. Die Anzahl fester channelnummern eignet sich jedoch nicht für alle Märkte. Beispielsweise werden die europäischen channelnummern von Consumern nicht verwendet. Stattdessen erwarten Consumer, dass Sie Ihre eigenen channelnummern für die Frequenzen auswählen und zuweisen, die von den Broadcast-oder Kabel Operatoren in Ihrem Bereich verwendet werden. Für diese Länder/Regionen sollten Anwendungen die Indexnummern nicht direkt für den Benutzer verfügbar machen. Instread: die Anwendung sollte eine interne Zuordnung zwischen den channelnummern (die dem Benutzer präsentiert werden) und Häufigkeits Indizes (für die Optimierung) beibehalten.

Die meisten nicht-US-Kabel Operatoren können in Häufigkeits Häufigkeit übertragen werden, wobei häufig Häufigkeiten aus verschiedenen Standards in dieselbe channelauflistung gemischt werden. Daher wird für jedes Land bzw. jede Region eine "Unicable"-Häufigkeits Tabelle verwendet, die über keine standardmäßige Kabelkanal-Standard Autorität verfügt. Außerdem wird ein Mechanismus bereitgestellt, um einzelne Frequenzen in den Häufigkeits Tabellen zu überschreiben. Dieser Mechanismus wird im folgenden Abschnitt, [Häufigkeits Überschreitungen](frequency-overrides.md), beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internationale Analog-TV-Optimierung](international-analog-tv-tuning.md)
</dt> </dl>

 

 



