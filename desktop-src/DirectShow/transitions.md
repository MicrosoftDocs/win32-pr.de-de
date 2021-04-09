---
description: Transitions
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fef1cd888293ad83ab1ba9f05ab4bb83ddafa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868263"
---
# <a name="transitions"></a>Transitions

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Mithilfe eines visuellen Effekts, wie z. b. ein ausblenden oder ein Zurücksetzen, kann ein Übergang von einer Videospur zu einer anderen durchlaufen werden. Die folgende Abbildung zeigt eine Zeitachse mit einem Übergang:

![Zeitachse mit Übergang](images/timeline3.png)

Das Übergangs Objekt befindet sich auf der Spur 1 und stellt einen Übergang von der Spur 0 zur Nachverfolgung 1 dar. Zu Beginn des Übergangs ist das gerenderte Video vollständig von Track 0 (Quelle A). Am Ende ist das Video vollständig von Track 1 (Quelle C). Dazwischen geht die Ausgabe von Quelle A in Quelle C über. Beispielsweise wird bei einem Fade-Übergang eine Quelle progressiv zum anderen. Die endgültige Ausgabe wird am Ende der Abbildung schematisiert.

Übergänge können sich nicht innerhalb desselben Titels zeitlich überlappen, Sie können jedoch überlappende Übergänge erstellen, indem Sie das Kompositions Objekt verwenden, wie unter [Komposition und Layering](composition-and-layering.md)beschrieben.

Ein Übergang weist eine Richtung auf. Standardmäßig beginnt Sie mit dem Titel mit niedrigerer Priorität (Quelle A im vorherigen Beispiel) und endet mit der Spur mit höherer Priorität (Quelle C). Zwischen und besteht das Video aus einer Mischung aus den beiden Quellen. Sie können jedoch das Gegenteil Verhalten angeben, wie in der folgenden Abbildung dargestellt:

![ntrack mit zwei Übergängen](images/fade.png)

An dieser Stelle wird der erste Übergang von der Spur 0 verblasst Nachverfolgung 1. Dies ist das Standardverhalten. Der zweite Übergang wird von der Nachverfolgung 1 zurück zur Nachverfolgung 0. Beachten Sie, dass sich beide Übergänge auf Track 1 befinden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einführung in DirectShow-Bearbeitungs Dienste](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Übergänge und Effekte](transitions-and-effects.md)
</dt> <dt>

[Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



