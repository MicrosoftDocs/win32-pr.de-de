---
title: Spracherkennung
description: Spracherkennung
ms.assetid: cb5ac509-12a4-4ca4-8776-424568cf780d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd36ea5754d53ceda2761635ecb838fdfb0328617827ca90fc969af915b4ea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960850"
---
# <a name="speech-recognition"></a>Spracherkennung

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Die Spracherkennung bietet eine sehr natürliche und vertraute Schnittstelle für die Interaktion mit Zeichen. Die Spracheingabe stellt jedoch auch viele Herausforderungen dar. Sprach-Engines funktionieren derzeit ohne wesentliche Teile der menschlichen Sprachkommunikation, z. B. Gesten, Intonation und Gesichtsausdrücke. Darüber hinaus ist natürliche Sprache in der Regel ungebunden. Es ist für den Sprecher einfach, das aktuelle Vokabular oder die *Grammatik* der Engine zu überschreiten. Ebenso kann der Wortlaut oder die Wortreihenfolge für jede Anforderung oder Antwort variieren. Darüber hinaus müssen Spracherkennungs-Engines häufig große Variationen in der Umgebung des Sprechers behandeln. Hintergrundgeräusche, Mikrofonqualität und Standort können sich beispielsweise auf die Eingabequalität auswirken. Auf ähnliche Weise machen unterschiedliche Sprecheraussprechungen oder sogar Variationen des gleichen Sprechers, z. B. wenn der Sprecher eine Kalte hat, eine Herausforderung, die Akustikdaten in darstellungsbezogenes Verständnis zu konvertieren. Schließlich müssen Sprach-Engines auch mit ähnlich klingenden Wörtern oder Ausdrücken in einer Sprache umgehen, z. B. "neu", "kannte" und "gnu" oder "einen guten Beach" und "Sprache erkennen".

Sprache ist nicht immer die beste Form der Eingabe für eine Aufgabe. Aufgrund der turn-taking-Natur der Sprache kann sie oft langsamer als andere Eingabeformen sein. Wie die Tastatur ist die Spracheingabe eine schlechte Schnittstelle zum Zeigen, es sei denn, es wird eine mnemonic-Darstellung bereitgestellt. Berücksichtigen Sie daher immer, ob Sprache die am besten geeignete Eingabe für eine Aufgabe ist. Es ist am besten, die Verwendung von Sprache als exklusive Schnittstelle für jede Aufgabe zu vermeiden. Stellen Sie andere Möglichkeiten bereit, mithilfe von Methoden wie Maus oder Tastatur auf alle grundlegenden Funktionen zuzugreifen. Nutzen Sie außerdem die mehr modale Art der Verwendung von Sprache in der grafischen Benutzeroberfläche, indem Sie Spracheingaben mit visuellen Informationen kombinieren, die ihnen helfen, den Kontext und die Optionen anzugeben.

Schließlich ist die erfolgreiche Verwendung der Spracheingabe nur teilweise auf die Qualität der Technologie zurückzuführen. Selbst die menschliche Erkennung, die jede aktuelle Erkennungstechnologie überschreitet, schlägt manchmal fehl. In der menschlichen Kommunikation verwenden wir jedoch Strategien, die die Wahrscheinlichkeit eines Erfolgs verbessern und eine Fehlerwiederherstellung ermöglichen, wenn ein Fehler auftritt. Daher hängt die Effektivität der Spracheingabe auch von der Qualität der Benutzeroberfläche ab, die sie darstellt.

Die Untersuchung menschlicher Modelle der Sprachinteraktion kann nützlich sein, wenn sie natürlichere Sprachschnittstellen entwerfen. Das Aufzeichnen von menschlichen Sprachdialogen für bestimmte Szenarien kann Ihnen dabei helfen, die verwendeten Konstrukte und Muster sowie effektive Formen von Feedback und Fehlerwiederherstellung besser zu verstehen. Sie kann dabei helfen, das zu verwendende Vokabular (für Eingabe und Ausgabe) zu bestimmen. Es ist besser, eine Sprachschnittstelle basierend darauf zu entwerfen, wie Menschen tatsächlich sprechen, als sie einfach von der grafischen Schnittstelle abzuleiten, in der sie arbeitet.

Beachten Sie, dass der Microsoft-Agent die Microsoft Speech-API (SAPI) zur Unterstützung der Spracherkennung verwendet. Dies ermöglicht die Verwendung des Microsoft-Agents mit einer Vielzahl kompatibler Engines. Obwohl Microsoft Agent bestimmte grundlegende Schnittstellen angibt, können die Leistungsanforderungen und die Qualität einer Engine variieren.

Sprache ist nicht die einzige Möglichkeit, Konversationsschnittstellen zu unterstützen. Sie können auch die Verarbeitung von Tastatureingaben in natürlicher Sprache anstelle von oder zusätzlich zur Sprache verwenden. In diesen Situationen können Sie weiterhin im Allgemeinen Richtlinien für die Spracheingabe anwenden.

-   [Lauschen, Nicht nur erkennen](listen--dont-just-recognize.md)
-   [Verdeutlichen und Einschränken von Auswahlmöglichkeiten](clarify-and-limit-choices.md)
-   [Bereitstellen einer guten Fehlerwiederherstellung](provide-good-error-recovery.md)

 

 




