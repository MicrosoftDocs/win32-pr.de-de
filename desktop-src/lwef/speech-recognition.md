---
title: Spracherkennung
description: Spracherkennung
ms.assetid: cb5ac509-12a4-4ca4-8776-424568cf780d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5c037ced96c386a5e0baf18eeba258422e0193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339845"
---
# <a name="speech-recognition"></a>Spracherkennung

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die Spracherkennung stellt eine sehr natürliche und vertraute Schnittstelle für die Interaktion mit Zeichen bereit. Die Spracheingabe stellt jedoch auch viele Herausforderungen dar. Sprach Triebwerke arbeiten zurzeit ohne wesentliche Teile des sprach Kommunikations Repertoires, wie z. b. Gesten, Intonation und Gesichtsausdrücke. Außerdem ist die natürliche Sprache in der Regel unbegrenzt. Es ist ganz einfach, wenn der Redner das aktuelle Vokabular (oder die *Grammatik*) der Engine überschreitet. Entsprechend kann die Formulierung oder Wort Reihenfolge für jede Anforderung oder Antwort variieren. Außerdem müssen Spracherkennungs-Engines häufig große Variationen in der-Umgebung des Sprechers behandeln. Beispielsweise können Hintergrundgeräusche, Mikrofon Qualität und Standort die Eingabe Qualität beeinflussen. Ebenso ist es eine Herausforderung, die akustischen Daten in darstellbare Grundlagen zu konvertieren, um die unterschiedlichen sprechersprechungen oder sogar dieselben Redner Variationen, z. b. wenn der Redner eine Erkältung hat, zu konvertieren. Und schließlich müssen Sprachmodule auch ähnliche, klingende Wörter oder Ausdrücke in einer Sprache behandeln, wie z. b. "New", "Knew" und "GNU", oder "Wrack a Nice Beach" und "Speech Speech".

Speech ist nicht immer die beste Form der Eingabe für eine Aufgabe. Aufgrund der Tatsache, dass es sich um die Natur der Sprache handelt, kann es häufig langsamer als andere Formen der Eingabe sein. Wie die Tastatur ist die Spracheingabe eine schlechte Oberfläche für die Darstellung, es sei denn, es ist eine Art von mnetmonischen Darstellung vorhanden. Daher sollten Sie immer überprüfen, ob Sprache die geeignetste Eingabe für eine Aufgabe ist. Es empfiehlt sich, die Verwendung von Sprache als exklusive Oberfläche für eine beliebige Aufgabe zu vermeiden. Stellen Sie mithilfe von Methoden wie der Maus oder der Tastatur andere Möglichkeiten für den Zugriff auf grundlegende Funktionen bereit. Profitieren Sie außerdem von der multimodalen Natur der Verwendung von Sprache in der visuellen Oberfläche, indem Sie Spracheingaben mit visuellen Informationen kombinieren, die den Kontext und die Optionen angeben.

Schließlich ist die erfolgreiche Verwendung von Spracheingaben nur teilweise auf die Qualität der Technologie zurückzuführen. Auch die Menschen Erkennung, die alle aktuellen Erkennungstechnologien überschreitet, schlägt manchmal fehl. Bei der menschlichen Kommunikation werden jedoch Strategien verwendet, die die Erfolgswahrscheinlichkeit verbessern und eine Fehlerwiederherstellung bereitstellen, wenn etwas schief geht. Daher hängt die Effektivität der Spracheingabe auch von der Qualität der Benutzeroberfläche ab, die diese darstellt.

Das Untersuchen von menschlichen Modellen der Sprachinteraktion kann beim Entwerfen von natürlicheren Sprachschnittstellen hilfreich sein. Das Aufzeichnen tatsächlicher sprachsprachdialoge für bestimmte Szenarien kann Ihnen helfen, die verwendeten Konstrukte und Muster sowie effektive Formen von Feedback und Fehlerwiederherstellung besser zu verstehen. Sie kann hilfreich sein, um das passende Vokabular zu bestimmen (für die Eingabe und Ausgabe). Es ist besser, eine Sprachschnittstelle zu entwerfen, die darauf basiert, wie Menschen sprechen, als Sie einfach von der grafischen Schnittstelle abzuleiten, in der Sie betrieben wird.

Beachten Sie, dass der Microsoft-Agent die Spracherkennung mithilfe der Microsoft Speech API (SAPI) unterstützt. Dadurch kann der Microsoft-Agent mit einer Vielzahl von kompatiblen Modulen verwendet werden. Obwohl der Microsoft-Agent bestimmte grundlegende Schnittstellen angibt, variieren die Leistungsanforderungen und die Qualität einer Engine möglicherweise.

Die Sprache ist nicht die einzige Möglichkeit, die konvertisierungsschnittstellen zu unterstützen. Sie können auch die natürlicher Sprachverarbeitung von Tastatureingaben anstelle von oder zusätzlich zur Sprache verwenden. In diesen Fällen können Sie weiterhin Richtlinien für die Spracheingabe anwenden.

-   [Lauschen, nicht einfach erkennen](listen--dont-just-recognize.md)
-   [Optionen verdeutlichen und einschränken](clarify-and-limit-choices.md)
-   [Bereitstellen einer guten Fehlerwiederherstellung](provide-good-error-recovery.md)

 

 




