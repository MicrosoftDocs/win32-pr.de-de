---
title: Optionen verdeutlichen und einschränken
description: Optionen verdeutlichen und einschränken
ms.assetid: 4ec3ca01-231b-4a45-aae1-fba5b2ba0033
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ed5f95c2e516f304ffa28bcca1d9fd67a9169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341878"
---
# <a name="clarify-and-limit-choices"></a>Optionen verdeutlichen und einschränken

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die Spracherkennung wird erfolgreicher, wenn der Benutzer den Bereich der passenden Grammatik lernt. Es funktioniert auch besser, wenn der Bereich der Auswahl begrenzt ist. Wenn die Eingabe weniger offen ist, desto besser kann die Sprach-Engine die Eingabe der akustischen Informationen analysieren.

Der Microsoft-Agent umfasst mehrere integrierte bereit Stellungen, die den Erfolg der Spracheingabe erhöhen. Das erste ist das Befehlsfenster, das angezeigt wird, wenn der Benutzer sagt: "Befehle Öffnen" oder "Was kann ich sagen?". (oder wenn der Benutzer im Popupmenü des Zeichens das Fenster Befehle Öffnen auswählt). Das Befehlsfenster dient als visuelle Anleitung für die aktive Grammatik der Sprach-Engine. Außerdem werden Erkennungs Fehler verringert, indem nur die Sprachgrammatik der Eingabe aktiven Anwendung und der globalen Befehle des Microsoft-Agents aktiviert wird. Aus diesem Grund gilt die aktive Grammatik der Sprach-Engine für den unmittelbaren Kontext. Weitere Informationen zum Fenster "Befehle" finden Sie unter [Übersicht über die Microsoft-Agent-Programmierschnittstelle](microsoft-agent-programming-interface-overview.md).

Wenn Sie sprach aktivierte Befehle von Microsoft-Agent erstellen, können Sie den Beschriftungs Text, der im Fenster "Befehle" angezeigt wird, sowie den zugehörigen sprach Text (Grammatik), die Wörter, die die Engine für den Abgleich mit diesem Befehl verwenden soll, erstellen. Versuchen Sie immer, Ihre Befehle so unverwechselbar wie möglich zu gestalten. Umso größer der Unterschied zwischen dem Wortlaut der Befehle, insbesondere für den sprach Text, desto wahrscheinlicher ist es, dass die Sprach-Engine zwischen gesprochenen Befehlen unterscheiden und eine genaue Entsprechung bereitstellen kann. Vermeiden Sie auch nur-Wort-oder sehr kurze Befehle. Im Allgemeinen bieten mehr akustische Informationen in einer gesprochenen Äußerung der Engine eine bessere Möglichkeit, eine genaue Übereinstimmung zu erzielen.

Wenn Sie den sprach Text für einen Befehl definieren, stellen Sie eine sinnvolle Vielfalt von Formulierungen bereit. Anforderungen, die das gleiche haben, können wie im folgenden Beispiel veranschaulicht ausgesprochen anders formuliert werden:

Fügen Sie einige pfeffoni hinzu.

Ich möchte einen Pfeffer.

Könnten Sie einige pfeffoni hinzufügen?

Pfeffoni, bitte.

Mit dem Microsoft-Agent können Sie problemlos Alternativen oder optionale Wörter für die Sprachgrammatik Ihrer Anwendung angeben. Sie schließen Alternative Wörter oder Ausdrücke in Klammern ein, die durch ein vertikales Balken Zeichen getrennt sind. Sie können optionale Wörter definieren, indem Sie Sie zwischen eckigen Klammer Zeichen einschließen. Außerdem können Alternativen oder optionale Wörter geschachtelt werden. Darüber hinaus können Sie eine Ellipse (...) als Platzhalter für ein beliebiges Wort verwenden. Die Verwendung von Ellipsen zu häufig erschwert jedoch möglicherweise die Unterscheidung zwischen verschiedenen Sprachbefehlen durch die Engine. Stellen Sie in jedem Fall immer sicher, dass der sprach Text mindestens ein eindeutiges Wort für jeden nicht optionalen Befehl enthält. In der Regel sollte dies einem Wort oder Wörtern im Beschriftungs Text entsprechen, den Sie definieren, der im Fenster "Befehle" angezeigt wird.

Obwohl Sie Symbole, Interpunktions Zeichen oder Abkürzungen in den Beschriftungs Text einschließen können, sollten Sie Sie im sprach Text vermeiden. Viele Spracherkennungs-Engines können keine Symbole und Abkürzungen verarbeiten, oder Sie können Sie verwenden, um spezielle Eingabeparameter festzulegen. Benennen Sie außerdem Zahlen um. Dadurch wird auch eine zuverlässigere Erkennungs Unterstützung sichergestellt.

Sie können auch direktivenaufforderungen verwenden, um eine offen gegangene Eingabe zu vermeiden. Direktivenaufforderungen verweisen implizit auf die Auswahl oder geben Sie explizit aus, wie in den folgenden Beispielen gezeigt:



|                                            |                                                     |
|--------------------------------------------|-----------------------------------------------------|
| Was willst du?                          | Zu allgemein, eine geöffnete Anforderung                  |
| Wählen Sie einen Pizza-Stil oder eine-Zutat aus.        | Gut, wenn Auswahlmöglichkeiten sichtbar sind, aber immer noch allgemein     |
| Sagen Sie "Hawaiisch", "Chicago" oder "The Works". | Besser, eine explizite Direktive mit bestimmten Optionen |



 

Dadurch wird der Benutzer zur Ausgabe eines gültigen Befehls geleitet. Wenn Sie die Wörter oder den Ausdruck vorschlagen, ist es wahrscheinlicher, dass Sie den erwarteten Wortlaut in der Rückgabe auslösen. Um eine unnatürliche Wiederholung zu vermeiden, ändern Sie den Wortlaut, oder kürzen Sie den ursprünglichen für die nachfolgende Präsentation, da der Benutzer mit dem Eingabe Stil vertraut wird. Direktivenaufforderungen können auch in Situationen verwendet werden, in denen der Benutzer einen Befehl nicht innerhalb eines vorgeschriebenen Zeitraums ausgibt oder einen erwarteten Befehl nicht bereitstellen kann. Direktivenaufforderungen können mithilfe der Sprachausgabe, ihrer Anwendungsschnittstellen oder beides bereitgestellt werden. Der Schlüssel unterstützt den Benutzer dabei, die entsprechenden Optionen zu kennen.

Der Wortlaut wirkt sich auf den Erfolg einer Eingabeaufforderung aus. Beispielsweise die Eingabeaufforderung "möchten Sie Ihre Pizza bestellen?" kann entweder die Antwort "yes" oder "No" generieren, kann aber auch eine Bestell Anforderung generieren. Definieren Sie die Eingabe Aufforderungen, um nicht mehrdeutig zu sein oder darauf vorbereitet zu sein, eine größere Vielfalt möglicher Antworten zu akzeptieren. Beachten Sie außerdem die Tendenz, dass Personen die Wörter und Konstrukte imitieren, die Sie hören. Dies kann häufig verwendet werden, um eine entsprechende Antwort wie im folgenden Beispiel zu verwenden:



|            |                                 |
|------------|---------------------------------|
| User:      | Alle Nachrichten von Paul anzeigen. |
| Art |                                 |



 

Es ist wahrscheinlicher, dass Sie den vollständigen Namen einer der Parteien mit dem möglichen Präfix "i mean" oder "i mean" lösen.

Da Microsoft-agentzeichen innerhalb der visuellen Oberfläche von Microsoft Windows funktionieren, können Sie mithilfe von visuellen Elementen Anweisungs Aufforderungen für die Spracheingabe bereitstellen. Beispielsweise können Sie die Zeichen Geste in einer Liste von Optionen anzeigen und anfordern, dass der Benutzer eine Auswahl treffen kann, oder Sie können die Auswahl in einem Dialogfeld oder einem Nachrichtenfenster anzeigen. Dies hat zwei Vorteile: Es werden explizit die Wörter vorgeschlagen, die der Benutzer sprechen soll, und es gibt eine alternative Möglichkeit, um den Benutzer zu antworten.

Sie können auch andere Interaktionsmöglichkeiten verwenden, um Benutzern eine angemessene Sprachgrammatik vorzuschlagen, wie im folgenden Beispiel gezeigt:



|            |                                                     |
|------------|-----------------------------------------------------|
| User:      | (Klicken Sie mit der Maus auf eine Pizza-Option im Hawai-Stil) |
| Art | Pizza im hawaienstil.                               |
| User:      | (Klickt mit der Maus auf eine zusätzliche Käse Option)         |
| Art | Fügen Sie "extra Käse" hinzu.                                 |



 

Ein weiterer wichtiger Faktor bei der erfolgreichen Spracheingabe ist das Durchsuchen des Benutzers, wenn die Engine für die Eingabe bereit ist, da viele sprach Triebwerke jeweils nur eine einzelne Äußerung zulassen. Der Microsoft-Agent bietet zwei Möglichkeiten, dies zu unterstützen. Erstens: Wenn die Soundkarte "MIDI" unterstützt, generiert der Microsoft-Agent einen kurzen Ton, um zu signalisieren, wann der Spracheingabe Kanal verfügbar ist. Im zweiten Fall zeigt das Fenster mit der sprechenden Info eine entsprechende Texteingabe Aufforderung an, wenn das Zeichen (Sprech-Engine) auf Eingaben lauscht. Außerdem wird in diesem Tipp angezeigt, was die Engine gehört.

 

 




