---
title: Verdeutlichen und Einschränken von Auswahlmöglichkeiten
description: Verdeutlichen und Einschränken von Auswahlmöglichkeiten
ms.assetid: 4ec3ca01-231b-4a45-aae1-fba5b2ba0033
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 953001d706089244d6366c8dab0cdb580a2d72ca
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118475"
---
# <a name="clarify-and-limit-choices"></a>Verdeutlichen und Einschränken von Auswahlmöglichkeiten

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Die Spracherkennung wird erfolgreicher, wenn der Benutzer den Bereich der entsprechenden Grammatik lernt. Es funktioniert auch besser, wenn der Auswahlbereich eingeschränkt ist. Wenn die Eingabe weniger offen ist, desto besser kann die Sprach-Engine die Akustikinformationseingabe analysieren.

Microsoft Agent umfasst mehrere integrierte Bestimmungen, die den Erfolg der Spracheingabe steigern. Die erste ist das Befehlsfenster, das angezeigt wird, wenn der Benutzer "Befehlsfenster öffnen" oder "Was kann ich sagen?" (oder wenn der Benutzer im Popupmenü des Zeichens Auf Befehlsfenster öffnen auswählt). Das Befehlsfenster dient als visuelle Anleitung für die aktive Grammatik der Sprach-Engine. Außerdem werden Erkennungsfehler reduziert, indem nur die Sprachgrammatik der eingabeaktiven Anwendung und die globalen Befehle von Microsoft Agent aktiviert werden. Daher gilt die aktive Grammatik der Sprach-Engine für den unmittelbaren Kontext. Weitere Informationen zum Befehlsfenster finden Sie unter [Übersicht über die Microsoft Agent-Programmierschnittstelle.](microsoft-agent-programming-interface-overview.md)

Wenn Sie sprachfähige Microsoft Agent-Befehle erstellen, können Sie den Untertiteltext, der im Befehlsfenster angezeigt wird, sowie dessen Sprachtext (Grammatik) erstellen, d. h. die Wörter, die die Engine zum Abgleichen dieses Befehls verwenden soll. Versuchen Sie immer, Ihre Befehle so unterschiedlich wie möglich zu gestalten. Je größer der Unterschied zwischen der Formulierung von Befehlen ist, insbesondere für den Sprachtext, desto wahrscheinlicher ist die Sprach-Engine in der Lage, zwischen gesprochenen Befehlen zu unterscheiden und eine genaue Übereinstimmung zu liefern. Vermeiden Sie auch Befehle mit nur einem Wort oder sehr kurz. Im Allgemeinen erhalten mehr Akustikinformationen in einer gesprochenen Äußerung der Engine eine bessere Möglichkeit, eine genaue Übereinstimmung zu finden.

Geben Sie beim Definieren des Sprachtexts für einen Befehl eine sinnvolle Vielzahl von Formulierungen an. Anforderungen, die dasselbe bedeuten, können sehr unterschiedlich formuliert werden, wie im folgenden Beispiel veranschaulicht:

Fügen Sie einige Paprikaoni hinzu.

Ich möchte eine Paprikaoni.

Könnten Sie etwas Paprikaoni hinzufügen?

Paprika, bitte.

Mit Microsoft Agent können Sie ganz einfach Alternativen oder optionale Wörter für die Sprachgrammatik für Ihre Anwendung angeben. Sie schließen alternative Wörter oder Ausdrücke zwischen Klammern ein, die durch ein vertikales Balkenzeichen getrennt sind. Sie können optionale Wörter definieren, indem Sie sie zwischen eckigen Klammern umschließen. Sie können auch Alternativen oder optionale Wörter schachteln. Darüber hinaus können Sie auch auslassungszeichen (...) im Sprachtext als Platzhalter für jedes Wort verwenden. Wenn Ellipsen jedoch zu häufig verwendet werden, kann es für die Engine schwieriger sein, zwischen verschiedenen Sprachbefehlen zu unterscheiden. Stellen Sie in jedem Fall sicher, dass Ihr Stimmtext mindestens ein charakteristisches Wort für jeden Befehl enthält, der nicht optional ist. In der Regel sollte dies mit einem Wort oder Wörtern im von Ihnen definierten Beschriftungstext übereinstimmen, der im Befehlsfenster angezeigt wird.

Obwohl Sie Symbole, Interpunktion oder Abkürzungen in Ihren Untertiteltext einblenden können, vermeiden Sie sie in Ihrem Stimmtext. Viele Spracherkennungs-Engines können keine Symbole und Abkürzungen verarbeiten oder sie zum Festlegen spezieller Eingabeparameter verwenden. Geben Sie außerdem Zahlen ein. Dadurch wird auch eine zuverlässigere Erkennungsunterstützung sichergestellt.

Sie können auch Anweisungseingabeaufforderungen verwenden, um Eingaben mit offenem Ende zu vermeiden. Anweisungsaufforderungen verweisen implizit auf die Optionen oder geben sie explizit an, wie in den folgenden Beispielen gezeigt:



| Prompt                                           | Auswertung                                                    |
|--------------------------------------------|-----------------------------------------------------|
| Was willst du?                          | Zu allgemein, eine Anforderung mit offenem Ende                  |
| Wählen Sie eine Pizzaart oder einen Pizzastil aus.        | Gut, wenn Auswahlmöglichkeiten sichtbar sind, aber trotzdem allgemein     |
| Sagen Sie "Mayaan", "Chicago" oder "The Works". | Besser, eine explizite Direktive mit bestimmten Optionen |



 

Dadurch wird der Benutzer auf die Ausgabe eines gültigen Befehls umleiten. Wenn Sie die Wörter oder Ausdrücke vorschlagen, ist es wahrscheinlicher, dass Sie im Gegenzug erwartete Formulierungen erhüren. Um unnatürliche Wiederholungen zu vermeiden, ändern Sie die Formulierung, oder kürzen Sie das Original für die nachfolgende Präsentation, wenn der Benutzer mehr Erfahrung mit dem Eingabestil hat. Anweisungsaufforderungen können auch in Situationen verwendet werden, in denen der Benutzer einen Befehl nicht innerhalb eines vorgeschriebenen Zeitpunkts ausspricht oder einen erwarteten Befehl nicht bereitstellen kann. Anweisungsaufforderungen können über die Sprachausgabe, Ihre Anwendungsschnittstellen oder beides bereitgestellt werden. Der Schlüssel hilft dem Benutzer, die entsprechenden Optionen zu kennen.

Die Formulierung wirkt sich auf den Erfolg einer Eingabeaufforderung aus. Beispiel: "Möchten Sie Ihre Pizza bestellen?" kann entweder eine "Ja"- oder "Nein"-Antwort generieren, aber es kann auch eine Bestellanforderung generiert werden. Definieren Sie Eingabeaufforderungen, um nicht mehrdeutig zu sein oder darauf vorbereitet zu sein, eine größere Anzahl möglicher Antworten zu akzeptieren. Beachten Sie außerdem die Neigung von Menschen, Wörter und Konstrukte zu imitieren, die sie hören. Dies kann häufig verwendet werden, um eine geeignete Antwort zu geben, wie im folgenden Beispiel:

**Benutzer:** Zeige mir alle Nachrichten von Paul.

**Charakter:**

Dies ist wahrscheinlicher, um den vollständigen Namen einer der Parteien mit dem möglichen Präfix "I mean" oder "I meant" zu erhalten.

Da Microsoft Agent-Zeichen innerhalb der grafischen Benutzeroberfläche von Microsoft Windows ausgeführt werden, können Sie visuelle Elemente verwenden, um Anweisungseingabeaufforderungen für die Spracheingabe zur Verfügung zu stellen. Beispielsweise können Sie die Zeichengeste in einer Liste von Auswahlmöglichkeiten verwenden und anfordern, dass der Benutzer eine Auswahl auswählt, oder Sie können Optionen in einem Dialogfeld oder Meldungsfenster anzeigen. Dies hat zwei Vorteile: Es schlägt explizit die Wörter vor, die der Benutzer sprechen soll, und bietet dem Benutzer eine alternative Möglichkeit, zu antworten.

Sie können auch andere Interaktionsmodi verwenden, um Benutzern die entsprechende Sprachgrammatik zu empfehlen, wie im folgenden Beispiel gezeigt:

**Benutzer:** (Klickt mit der Maus auf eine Pizzaoption im Stil von ):)

**Zeichen:** Pizza im Stil von Einer-/Einer-Pizza.)

**Benutzer:** (Klickt mit der Maus auf die Option Extra Cheese)

**Zeichen:** Fügen Sie "Extra Cheese" hinzu.

Ein weiterer wichtiger Faktor bei der erfolgreichen Spracheingabe ist das Aufbereiten des Benutzers, wenn die Engine für die Eingabe bereit ist, da viele Sprach-Engines immer nur eine einzelne Äußerung gleichzeitig zulassen. Microsoft Agent bietet dafür zwei Möglichkeiten. Erstens: Wenn die Soundkarte DIE -Audiokarte unterstützt, generiert Microsoft Agent einen kurzen Ton, um zu signalisieren, wenn der Spracheingabekanal verfügbar ist. Zweitens zeigt das Fenster Trinkgeld lauschen eine entsprechende Texteingabeaufforderung an, wenn das Zeichen (Sprach-Engine) auf Eingaben lausst. Darüber hinaus zeigt dieser Tipp an, was die Engine gehört hat.

 

 




