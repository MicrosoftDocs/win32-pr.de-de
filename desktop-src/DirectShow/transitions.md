---
description: Transitions
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7511a010de60cdd87907b4ad7faa59963d3f0c6037dce3adc8fc58fa1c0a67a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078700"
---
# <a name="transitions"></a>Transitions

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Ein Übergang ist eine Möglichkeit, von einer Videospur zu einer anderen zu segue zu gehen, indem ein visueller Effekt wie ein Ausblenden oder ein Zurücksetzungseffekt verwendet wird. Die folgende Abbildung zeigt eine Zeitachse mit einem Übergang:

![Zeitachse mit Übergang](images/timeline3.png)

Das Übergangsobjekt befindet sich auf Spur 1 und stellt einen Übergang von Track 0 zu Track 1 dar. Zu Beginn des Übergangs stammt das gerenderte Video vollständig aus Track 0 (Quelle A). Am Ende stammt das Video vollständig aus Track 1 (Quelle C). Zwischendurch geht die Ausgabe von Quelle A zu Quelle C über. Bei einem Überblendungsübergang wird z. B. eine Quelle progressiv zur anderen ausgeblendet. Die endgültige Ausgabe wird am unteren Rand der Abbildung schematisiert.

Übergänge können sich innerhalb desselben Titels nicht zeitlich überlappen, aber Sie können überlappende Übergänge erstellen, indem Sie das Kompositionsobjekt verwenden, wie unter [Composition and Layering (Komposition und Ebenen) beschrieben.](composition-and-layering.md)

Ein Übergang hat eine Richtung. Standardmäßig beginnt sie mit der Spur mit niedrigerer Priorität (Quelle A im vorherigen Beispiel) und endet bei der Spur mit höherer Priorität (Quelle C). Dazwischen ist das Video eine Mischung aus den beiden Quellen. Sie können jedoch das gegenteilige Verhalten angeben, wie in der folgenden Abbildung gezeigt:

![ntrack mit zwei Übergängen](images/fade.png)

Hier wird der erste Übergang von Track 0 ausgeblendet. Dies ist das Standardverhalten. Der zweite Übergang wird von Track 1 zurück zu Track 0 ausgeblendet. Beachten Sie, dass sich beide Übergänge auf Track 1 befinden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit DirectShow-Bearbeitungsdiensten](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Übergänge und Effekte](transitions-and-effects.md)
</dt> <dt>

[Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



