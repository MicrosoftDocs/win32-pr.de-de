---
description: Häufigkeitstabellen
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Häufigkeitstabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db832144aedb8f64d18692a30a8e8c7d812c4cbd517b1b9ab31bd9cdc231019b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401258"
---
# <a name="frequency-tables"></a>Häufigkeitstabellen

Der Tv Tuner-Filter (kstvtune.ax) verfügt über eine interne Liste von Häufigkeitstabellen. Jede Häufigkeitstabelle enthält eine Liste der Häufigkeiten und entspricht den Übertragungs- oder Kabelfrequenzen für ein bestimmtes Land/eine bestimmte Region. Eine Anwendung wird auf eine bestimmte Häufigkeit abgestimmt, indem die [**IAMTuner::p ut \_ Channel-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) mit dem Index der gewünschten Häufigkeit aufruft.

Bei einigen Ländern/Regionen werden die Indexnummern der Häufigkeitstabellen direkt den Kanalnummern angezeigt. Feste Kanalnummern sind jedoch nicht für alle Märkte geeignet. Beispielsweise werden die europäischen Kanalnummern von Denkendern nicht tatsächlich verwendet. Stattdessen erwarten Die Verbraucher, dass sie ihre eigenen Kanalnummern für die Frequenzen auswählen und zuweisen, die von den Übertragungs- oder Kabeloperatoren in ihrem Bereich verwendet werden. Für diese Länder/Regionen sollten Anwendungen die Indexnummern nicht direkt für den Benutzer verfügbar machen. Instread sollte die Anwendung eine interne Zuordnung zwischen Kanalnummern (die dem Benutzer angezeigt werden) und Häufigkeitsindizes (zur Optimierung) behalten.

Die meisten Kabeloperatoren, die nicht in den USA sind, können bei häufigkeitsbasierten Übertragungen übertragen, die häufig Frequenzen aus unterschiedlichen Standards in derselben Kanallinie kombinieren. Daher wird eine "Unicable"-Häufigkeitstabelle für jedes Land bzw. jede Region verwendet, in dem bzw. in der keine Standard-Autorität für Kabelkanalstandards vorlädt. Außerdem wird ein Mechanismus bereitgestellt, um einzelne Häufigkeiten in den Häufigkeitstabellen zu überschreiben. Dieser Mechanismus wird im folgenden Abschnitt, Frequency [Overrides , beschrieben.](frequency-overrides.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internationale analoge TV-Optimierung](international-analog-tv-tuning.md)
</dt> </dl>

 

 



