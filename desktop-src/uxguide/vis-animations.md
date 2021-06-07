---
title: Animationen und Übergänge
description: Die strategische Verwendung von Animationen und Übergängen kann ihr Programm leichter verstehen, reibungsloser, natürlicher und von höherer Qualität sein und ansprechender sein.
ms.assetid: 9e0e9604-f051-47e4-bcd0-59fbfd38b9c1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 546c1d0a59808b54f4ffa12fc7cd034554521ca3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444761"
---
# <a name="animations-and-transitions"></a>Animationen und Übergänge

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Die strategische Verwendung von Animationen und Übergängen kann ihr Programm leichter verstehen, reibungsloser, natürlicher und von höherer Qualität sein und ansprechender sein. Die zufällige Verwendung von Animationen und Übergängen kann das Programm jedoch störend und sogar ängstlich machen.

Animationen geben die Darstellung von Bewegung oder Änderung im Laufe der Zeit an. Verwenden Sie Animationen, um Feedback zu geben, eine Vorschau der Auswirkung einer Aktion anzuzeigen, die Beziehung zwischen Objekten anzuzeigen, die Aufmerksamkeit auf Änderungen zu lenken oder eine Aufgabe visuell zu erklären.

![Abbildung der numerischen Tastatur mit hervorgehobener Taste ](images/vis-animations-image1.png)

Microsoft Windows verwendet eine Hintergrund-Flash-Animation, um Feedback zu geben, dass auf das Objekt geklickt wurde.

Übergänge sind Animationen, mit denen Benutzer während Benutzeroberflächenzustandsänderungen und Objektbearbeitungen ausgerichtet bleiben und diese Änderungen reibungslos und nicht mit Jarringen funktionieren. Gute Übergänge wirken natürlich und vermitteln oft die Vorstellung, dass Benutzer mit realen Objekten interagieren.

![Screenshot, der drei Größen von Wetter-Gadgets zeigt.](images/vis-animations-image2.png)

Windows Desktop-Gadgets verwenden reibungslose Übergänge zwischen ihren präzisen und Detailzuständen.

Im Allgemeinen werden die besten Animationen und Übergänge verwendet, um Benutzer nicht-lyrisch zu kommunizieren und Zustandsänderungen natürlicher und weniger wahrnehmbar zu machen. Im Gegensatz dazu sind die am wenigsten effektiven , da sie nichts kommunizieren oder unnötige Aufmerksamkeit auf sich ziehen. Animationen werden am besten als sekundäre Kommunikationsform verwendet. Sie sollten Informationen kommunizieren, die nützlich, aber nicht kritisch sind, und um darauf zugreifen zu können, sollten Benutzer in der Lage sein, äquivalente Informationen auf andere Weise zu bestimmen.

**Hinweis:** Richtlinien im Zusammenhang mit [Softwarebranding,](exper-branding.md) [Sound](vis-sound.md)und [Barrierefreiheit](inter-accessibility.md) werden in separaten Artikeln vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Berücksichtigen Sie die folgenden Fragen, um die Entscheidung zu treffen.

### <a name="animations"></a>Animationen

Gelten die folgenden Bedingungen?

-   Die Animation kommuniziert visuell etwas Nützliches, z. B. Feedback geben, Beziehungen, Ursachen und Effekte anzeigen oder die Aufmerksamkeit auf wichtige Änderungen lenken.
-   Das Sehen der Animation ist nicht zwingend erforderlich. Äquivalente Informationen können auf andere Weise abgerufen werden. Benutzer profitieren möglicherweise nicht von der Animation, wenn:
    -   Sie haben Animationen deaktiviert.
    -   Ihre Aufmerksamkeit liegt an anderer Stelle.
    -   Sie sind sehbehindert.
    -   Die Animation wird durch ein anderes Fenster verdeckt.
    -   Die Animation wird aufgrund unzureichender Systemleistung nicht wiedergegeben.
-   Die Animation wirkt sich nicht auf die Produktivität des Benutzers aus. Entweder:
    -   Dies geschieht schnell (200 Millisekunden oder weniger).
    -   Die Interaktion wird nicht beeinträchtigt, oder sie kann unterbrochen werden.
    -   Der Benutzer muss trotzdem warten.
-   Die Animation wirkt sich nicht auf den Benutzerflow aus.
    -   Sie befindet sich entweder im Mittelpunkt des Benutzers oder richtet die Aufmerksamkeit auf etwas außerhalb des Mittelpunkts der Aufmerksamkeit, das wichtig oder nützlich ist, um eine Aufgabe abzuschließen.
    -   Dies ist leicht zu ignorieren, nicht ablenkend oder ungärrlich.
    -   Es wird nicht mühsam. Benutzer finden es auch nach wiederholter Anzeige weiterhin geeignet und freuen sich.

Ziehen Sie in diesem Falle die Verwendung einer Animation in Betracht.

### <a name="transitions"></a>Transitions

Ändert sich der Zustand eines Objekts oder einer Szene, und gelten alle oben genannten Bedingungen für die Verwendung von Animationen sowie eine der folgenden Bedingungen?

-   Die Zustandsänderung ist konzeptionell desorientiert, verwirrend oder anderweitig schwer zu verstehen.
-   Die Zustandsänderung ist visuell jarring, fehlt an Kontinuität oder Glättung oder blinkt. oder erscheint unnatürlich, unpoliert oder von schlechter Qualität, insbesondere wenn es sich um einen großen Bildschirmbereich handelt.
-   Wenn Sie einen Übergang verwenden, wird die Zustandsänderung schneller angezeigt.
-   Die Zustandsänderung ist eine besondere Aufmerksamkeit des Benutzers.

In diesem Falle sollten Sie einen Übergang verwenden.

## <a name="design-concepts"></a>Entwurfskonzepte

Animationen und Übergänge sind eine effektive Möglichkeit, Informationen visuell zu kommunizieren, für die andernfalls Text zur Erläuterung erforderlich wäre oder von Benutzern übersehen werden könnte.

**Falsch:**

![Screenshot des Dialogfelds mit Meldung ](images/vis-animations-image3.png)

**Richtig:**

![Abbildung der visuellen Kommunikation von Animationen ](images/vis-animations-image4.png)

Die Verwendung einer Animation kommuniziert die gleichen Informationen, aber auf natürliche, unaufdringliche Weise. Was würden Sie lieber tausendmal sehen?

**Animationen und Übergänge müssen keine Aufmerksamkeit erfordern, um erfolgreich zu sein.** Tatsächlich werden sie häufig verwendet, um die Aufmerksamkeit auf Programmmechanismen zu lenken, die Benutzer nicht kennen müssen. Viele erfolgreiche Animationen sind so natürlich, dass Benutzer sie nicht einmal kennen. stattdessen würden Benutzer nur ihre Abwesenheit bemerken. Die Häufigkeit des Auftretens erhöht den Bedarf an Feinheiten, sodass Effekte gespart werden, die aufmerksamkeitsaufwendige seltene Ereignisse erfordern, die die Aufmerksamkeit wirklich erfordern.

![Screenshot aller Programme, die in den Rückwärtspfeil geändert werden ](images/vis-animations-image5.png)

Ein Startmenü Übergang, der es vermeidet, die Aufmerksamkeit zu lenken.

Neben dem einfacheren Verständnis und Verhalten Ihres Programms sind gut **entworfene Animationen und Übergänge eine hervorragende Möglichkeit, Ihrem Programm Persönlichkeit, Zeichen und Stil hinzuzufügen.** Sie können die Benutzerfreundlichkeit immersiver und ansprechender gestalten, indem sie ihr ein natürliches, echtes Gefühl geben.

![Abbildung, die zeigt, wie sich das Zeigen auf die Schaltflächenfarbe auswirkt ](images/vis-animations-image6.png)

Windows 7 hebt Taskleistenschaltflächen beim Zeigen auf die aktuelle Mausposition und Programmsymbolfarbe hervor. Dieser Ansatz ist visuell ansprechend, aber dennoch dezent und vermittelt eine ungenannte Persönlichkeit.

**Animationen und Übergänge sind jedoch am effektivsten und willkommen, wenn sie einen eindeutigen Zweck erfüllen.** Sie sollten verwendet werden, um die Benutzerfreundlichkeit, die Glätte und den Fluss sowie die Wahrnehmung der Qualität zu verbessern, ohne die Leistung erheblich zu beeinträchtigen.

Während einige Arten von Animationen verwendet werden, um die Aufmerksamkeit des Benutzers zu lenken, stellen Sie sicher, dass die Aufmerksamkeit gut ausgeglichen ist und das Denken des Benutzers unterbrochen wird. Das menschliche Auge reagiert empfindlich auf Bewegung, insbesondere auf die Peripheriebewegung. Es kann für Benutzer schwierig sein, sich zu konzentrieren, wenn eine blinkende Taskleistenschaltfläche oder ein rotierendes Benachrichtigungsbereichssymbol vorhanden ist. **Vermeiden Sie die Verwendung von Animationen, um Benutzer zu unterbrechen oder abzulenken, oder machen Sie die Aufmerksamkeit auf Dinge, die die Aufmerksamkeit des Benutzers nicht rechtfertigen.**

**Falsch:**

![Abbildung der Schaltfläche "Taskleiste" ohne Grund hervorgehoben ](images/vis-animations-image7.png)

Programme sollten ihre Taskleistenschaltfläche nicht blinken lassen, es sei denn, Benutzer müssen sofort etwas Wichtiges tun. In diesem Fall muss der Benutzer nur das Programm aktivieren.

**Verwenden Sie Animationen und Übergänge, da ihr Programm sie benötigt, nicht nur, weil Sie dies können.** Verwenden Sie für die Barrierefreiheit keine Animation als einzige Möglichkeit, wichtige Informationen zu vermitteln. Stellen Sie sicher, dass Benutzer äquivalente Informationen auf andere Weise abrufen können.

### <a name="attributes-of-good-animations-and-transitions"></a>Attribute guter Animationen und Übergänge

Gute Animationen und Übergänge treffen die richtige Balance zwischen diesen Attributen:

-   **Sind eindeutig absichtsvoll.** Gute Animationen sind vorhanden, da sie sein müssen, ob Sie Informationen kommunizieren, eine Interaktion real gestalten oder die Aufmerksamkeit auf etwas Besonderes lenken müssen. Und zielgerichtete Animationen sind genau. Wenn eine Animation zeigt, dass eine Aufgabe ausgeführt wird, liegt dies daran, dass die Aufgabe tatsächlich ausgeführt wird.

**Falsch:**

![Screenshot des Akkusymbols und des vollständig geladenen Labels ](images/vis-animations-image8.png)

In diesem Beispiel zeigt die Animation, dass ein vollständig geladener Akku geladen wird.

-   **Sieht reibungslos und kontinuierlich aus.** Gute Animationen entfernen Nahten zwischen Szenen- oder Elementzustandsänderungen reibungslos, indem Beziehungen angezeigt werden und ein Gefühl für Ort und Kontext vermittelt wird. Die Kontinuität hilft Benutzern zu verstehen, wie sie dorthin gelangt sind und wie sie zu dem Ort zurückkehren können, von dem sie stammen.

![Screenshot von drei Vorschauversionen des Taskleistenfensters ](images/vis-animations-image9.png)

Die Vorschauversion des Windows 7-Taskleistenfensters wird aus Gründen der Kontinuität geändert, wenn der Benutzer von einem Programm zu einem anderen wechselt.

-   **Sind realistisch.** Gute Animationen simulieren die realen physischen Eigenschaften und das Verhalten eines Objekts. Dies hilft Benutzern, die Ergebnisse ihrer Interaktionen vorherzusagen und zu verstehen. Sie müssen die reale Welt nicht genau modellieren, aber wenn Sie realistische Animationen verwenden, müssen Sie sie mit der realen Welt konsistent halten. Benutzer sollten nie von den Ergebnissen verwirrend oder verwirrend sein, insbesondere mit Animationen, die für die direkte Bearbeitung verwendet werden.

![Abbildung der Taskleistenschaltfläche, die an neue Position gezogen wird ](images/vis-animations-image10.png)

In diesem Beispiel ist die animation "Move out of the way", die von der Windows 7-Taskleiste verwendet wird, realistischer als eine statische Einfügemarke.

-   **Sind authentifiziert.** Selbst Objekte, die in der realen Welt nicht gefunden werden, können natürlich erscheinen, indem sie auf dem realen Verhalten eines anderen, aber verknüpften Objekts basieren. DieseMetapher funktioniert nur, wenn die Beziehung den beabsichtigten Zweck und das Verhalten eindeutig kommuniziert.

![Screenshot des ausgelösten Effekts hinter dem verschobenen Fenster ](images/vis-animations-image11.png)

In diesem Beispiel ist die von Windows 7 verwendete Fensteranimation "Squeegee" authentiert, da sie mit dem Verhalten von Fenstern in der realen Welt konsistent ist.

-   **Verwenden Sie die natürliche Zuordnung.** Natürliche Zuordnungen sind entweder physisch oder kulturbelassen. Eine kulturbasierte natürliche Zuordnung kann z. B. damit beginnen, dass in den Kulturen des Westens Menschen von links nach rechts lesen. Um eine Zeitsequenz von -Objekten auszudrücken, ist das mittlere Objekt daher aktuell, Objekte auf der linken Seite liegen aus der Vergangenheit und Objekte auf der rechten Seite sind in der Zukunft. Die Zukunft in der Zeit wird durch die Bewegung von links nach rechts angezeigt.

![Screenshot der Media Player-Statusleiste ](images/vis-animations-image12.png)

In diesem Beispiel verfügt das Windows Media Player-Steuerelement über eine natürliche Zuordnung, da die Wiedergabe die Position von links nach rechts verschiebt.

-   **Persönlichkeit haben.** Gut ausgewählte Animationen sind hervorragende Möglichkeiten, Ihrem Programm Persönlichkeit, Zeichen und Stil hinzuzufügen. Sie können die Benutzererfahrung immersiver und ansprechender gestalten. Während der Typ der Animation bestimmt, was sie kommuniziert, zeigt die spezifische Art und Weise, wie die Animation ausgeführt wird, die Persönlichkeit des Programms. Gute Animationen zeigen die richtige Persönlichkeit für Ihr Programm an, ob schwerwiegend oder launisch oder irgendwo dazwischen.

![Screenshot der kreativ gestalteten Zune-Schnittstelle ](images/vis-animations-image13.png)

In diesem Beispiel hilft Zunes Verwendung von animiertem Text und dynamischer Perspektive dabei, seine Persönlichkeit zu formen.

-   **Aussehen und Reagieren.** Gute Animationen beeinträchtigen nicht die Produktivität des Benutzers, indem sie Benutzer von anderen Interaktionen aussperren oder benutzer gezwungen werden, zu sehen. Unabhängig davon, wie natürlich und ansprechend die Animationen Ihres Programms sind, möchte niemand ausschließlich auf sie warten. Gute Animationen sehen auch reaktionsschnell aus, ohne durch einen schnellen Start mit einer weichen Landegeschwindigkeit zu jarringen. Dynamische Animationen profitieren auch von der schnellen Kommunikation ihres Zwecks. Benutzer sollten sich eine Animation nicht lange ansehen müssen, nur um herauszufinden, was sie tut oder wann sie fertig ist. Für die direkte Manipulation sind reaktionsfähige Animationen wichtig, um ein direktes und ansprechendes reales Gefühl zu erhalten. Um sich direkt zu fühlen, müssen die Kontaktpunkte eines Objekts während der gesamten Bearbeitung reibungslos unter dem Zeiger bleiben. Jede Verzögerung, abgesenkte Antwort oder ein Verlust des Kontakts zerstört die Wahrnehmung der direkten Manipulation.

![Abbildung des Fingers, der einen Touchscreen berührt ](images/vis-animations-image14.png)

In diesem Beispiel ist der Übergang zum Schwenken von Fingern reaktionsfähig, da der Kontaktpunkt während der gesamten Bearbeitung unter dem Finger des Benutzers hält.

-   **Gewinnen Sie die richtige Aufmerksamkeit.** Gute Animationen sind in der Regel dezent und ziehen nur die Aufmerksamkeit auf sich, die erforderlich ist, um ihren Zweck zu erfüllen. Daher sind sie nicht störend, störend, zu komplex, zu lang oder sich wiederholend. Sie werden nach wiederholten Anzeigen nicht mühsam.

![Screenshot: Hervorhebung von "Fading" bei Dateinamen ](images/vis-animations-image15.png)

In diesem Beispiel lenkt die Windows-Suche vorübergehend die Aufmerksamkeit auf übereinstimmende Suchwörter und wird dann ausgeblendet.

-   **Sehen Sie nur dann besonders aus, wenn es speziell ist.** Die Häufigkeit erhöht die Notwendigkeit von Feinheiten, sodass häufige Interaktionen einfache Animationen erfordern, die eine einfache Idee auf einfache Weise kommunizieren. Reservieren Sie spezielle, komplexe Animationen für besondere, seltene Erfahrungen.

![Screenshot von vier Kreisen, die zu einem Windows-Logo werden ](images/vis-animations-image16.png)

In diesem Beispiel verwendet Windows eine Aufmerksamkeitsanimation beim Start, um die Erfahrung besonders zu machen, aber eine solche Animation wäre an anderer Stelle ungeeignet.

Sie wissen, dass Sie das richtige Gleichgewicht erzielt haben, wenn die Gesamterfahrung geschädigt würde, wenn eines dieser Attribute entfernt würde.

### <a name="creating-an-animation-vocabulary"></a>Erstellen eines Animationsvokabulars

Gute Animationen sind eine effektive visuelle Kommunikation, und Konsistenz ist entscheidend für ihre Effektivität. Wenn Sie einen bestimmten Übergang verwenden, z. B. das Einschieben einer Szene von rechts zur nächsten Szene, sollte dies der einzige Übergang sein, der für diesen Zweck verwendet wird, und dieser Übergang sollte nicht für andere Zwecke verwendet werden. Das Zuweisen unterschiedlicher Bedeutungen zu derselben Animation schadet der Kommunikationsfähigkeit. Indem Sie bestimmte Animationen und Übergänge zu bestimmten Bedeutungen zuweisen, erstellen Sie ein Animationsvokabular.

Dieses Problem gilt für Animationen und Übergänge, die eine Bedeutung haben, nicht für generische Animationen, denen Benutzer wahrscheinlich keine Bedeutung zuweisen, oder für Animationen, deren Zweck unmerklich sein soll. Animationen wie Ausblendungen und Sondereffekte wie z. B. Einblendungen haben z. B. keine besondere Bedeutung, sodass sie frei verwendet werden können.

Ein gutes Vokabular weist Animationen zu, die das physische Verhalten eines Objekts in der realen Welt modellieren. Wenn Sie einem Objekt oder einer Aktion eine Animation zuweisen müssen, die keine entsprechung in der realen Welt hat, wählen Sie eine Animation aus, die zeigt, wie sich das Objekt verhalten könnte, wenn es real wäre.

![Screenshot, in dem gezeigt wird, wie mit dem Zeigen auf das Windows-Logo gezeigt wird ](images/vis-animations-image17.png)

Der Startmenü ist kein objekt aus der realen Welt, aber sein Hovereffekt wird wie ein reales Objekt aufscheinen, wenn es aktiviert wird.

Jede Animation in einem Vokabular muss eindeutig eindeutig sein. Die Animationen sollten nur dann ähnliches Verhalten haben, wenn ihre zugeordneten Aktionen ähnlich verknüpft sind. Beispielsweise schlagen Bewegungsübergänge die Navigation vor, sodass Sie Bewegungsübergänge aus verschiedenen Richtungen verwenden können, um verschiedene Navigationstypen anzugeben.

Sie werden wissen, dass Ihre Animationen und Übergänge nicht gut kommunizieren, wenn Benutzer die Ergebnisse verwirrend, überraschend oder unerwartet finden. Im Allgemeinen ist es besser, einen einzelnen Zweck zu erreichen als mehrere Zwecke, die nicht so gut sind.

Im Idealfall sollte Ihr Animationsvokabular in allen Bereichen Ihres Programms, die sie benötigen, umfassend sein. Wenn nur wenige Interaktionen natürliche Animationen enthalten, wird dies auf diejenigen aufmerksam machen, die dies nicht sind.

Weitere Informationen zum Windows-Animationsvokabular finden Sie im Abschnitt [Verwendungsmuster](#usage-patterns) dieses Artikels.

### <a name="designing-the-right-personality"></a>Entwerfen der richtigen Persönlichkeit

Während der Typ der Animation bestimmt, was sie kommuniziert, spricht die spezifische Art und Weise, wie die Animation ausgeführt wird, die Persönlichkeit des Programms und verstärkt seine Marke.

Die Persönlichkeit Ihres Programms sollte die Art ihrer Aufgaben und die Persönlichkeit ihrer Benutzer widerspiegeln, sodass es keine willkürliche Wahl ist. Stattdessen sollte sich eine gut entworfene Persönlichkeit authentifizieren. Versuchen Sie nie, dies zu erzwingen. Die Persönlichkeit sollte eine emotionale Verbindung mit dem Benutzer herstellen. Zu berücksichtigende Faktoren:

-   **Aufgaben:** Schwerwiegend oder spaßig; optional oder erforderlich.
-   **Folgen:** Schwerwiegend oder minder schwerwiegend.
-   **Kosten:** Kostenlos oder erworben; , wenn erworben, moderat oder teuer.
-   **Benutzerfokus:** Relativ kleine Gruppe von Zielbenutzern oder eine breite, allgemeine Zielgruppe.
-   **Benutzerumgebung:** Professional, locker oder zu Hause.
-   **Benutzeralter:** Älter oder älter.
-   **Nutzungshäufigkeit:** Häufig oder selten.

Die Kombination dieser Faktoren hilft dabei, eine geeignete Persönlichkeit für Ihr Programm zu bestimmen. Im Folgenden finden Sie einige geeignete Kombinationen für gängige Programmtypen:

**Produktivitätsanwendungen**

Produktivitätsanwendungen müssen sich natürlich auf die Produktivität konzentrieren. Während sich einige besondere Erfahrungen aufdringen können, sollten die meisten anderen Animationen die folgenden Merkmale aufweisen:

-   Small
-   Natürlich, realistisch
-   Dezent, dezent
-   Schnell, effizient
-   Gelockert

**Hilfsprogramme**

Hilfsprogramme werden in der Regel kurz verwendet, sodass ihre Verwendung von Animationen aggressiver sein kann:

-   Realistisch, veranschaulichend, selbsterklärend
-   Safe
-   ansprechend

**Unterhaltung, Spiele**

Da das Ziel dieser Programme ist, Benutzer zu binden und zu unterstützen, können die Animationen und Übergänge durch die folgenden Merkmale viel aggressiver sein:

-   Groß (wird möglicherweise zu einem integralen Bestandteil der Erfahrung)
-   Künstlicher, besens
-   Einflussreich, dynamisch
-   Emotional, Heiter, Launen
-   Energetische

Das Herstellen einer emotionalen Verbindung ist für Unterhaltungsprogramme so wichtig, dass es akzeptabel ist, einige Regeln zu über sichten, wenn dies dazu bei trägt, dass sich Benutzer in das Programm verlieben. Beispielsweise ist es akzeptabel, wenn eine Animation oder ein Übergang nach dem hundertsten Mal lästig wird, wenn die meisten Benutzer das Programm wahrscheinlich nicht so oft verwenden.

Im Allgemeinen sind Animationen und Übergänge, die klein, natürlich, dedudiert, effizient, aber gelockert sind, die sicherste Lösung. Übergänge mit diesen Merkmalen nehmen in der Regel den kürzesten Weg von Anfang bis Ende ein, beginnen schnell, enden weich und überdrehen sich nicht. Außerdem sind gut entworfene Übergänge so konzipiert, dass sie über den gesamten Bereich der Entfernungen, in denen sie verwendet werden, gut funktionieren.

### <a name="animation-performance"></a>Animationsleistung

Stellen Sie beim Entwerfen von Animationen sicher, dass sie sich nicht auf die Fähigkeit der Benutzer auswirken, Ihr Programm effizient zu verwenden. Machen Sie Ihre Animationen im Allgemeinen langsam genug, um ihren Zweck zu erfüllen, aber schnell genug, dass sie die Reaktionsfähigkeit nicht beeinträchtigen, zu viel Aufmerksamkeit erfordern oder ermüdend werden.

**Falsch:**

![Abbildung des Seitendrehens von rechts nach links ](images/vis-animations-image18.png)

Diese Animation zum Drehen von Seiten hat zwar ein ansprechendes, reales Gefühl, aber sie mindert die Produktivität der Benutzer, da es länger dauert, Seiten zu drehen.

Kurze Übergänge (200 Millisekunden oder weniger) sind ein Sonderfall (insbesondere, wenn sie sich häufig von einer Verzögerung abarbeiten), da Benutzer wissen, dass sie eine Teilsekunde auf sie warten müssen. Benutzer sind bereit, auf solche Animationen zu warten, wenn:

-   Die wahrgenommene Wartezeit ist extrem kurz (200 Millisekunden oder weniger).
-   Durch den Übergang wird die Interaktion reibungsloser und natürlicher.
-   Durch den Übergang wird die Interaktion reaktionsfähiger.
-   Jede Verzögerung hilft dem Benutzer, die Kontrolle über die Interaktion zu behalten.

![Abbildung der Taskleistenschaltflächen, die an eine neue Position gezogen werden ](images/vis-animations-image19.png)

Benutzer akzeptieren eine kurze Verzögerung für die Animation zur Neuanordnung der Taskleistenschaltfläche, da sie sehr kurz ist und die Interaktion natürlicher anfühlt.

Es gibt drei Möglichkeiten, wie Animationen sich negativ auf die Leistung auswirken können: Geschwindigkeit, Reaktionsfähigkeit und Wahrnehmung.

Aus Speed-Sicht sind einige Animationen visuelle Lässer für CPU-intensive Aufgaben, daher sollten Sie diese Aufgaben mit CPU-intensiven Animationen langsamer machen. Die cpuintensivsten Animationen ("intensive" Animationen) tendieren zu:

-   Binden Sie viele Elemente ein, die sich unabhängig voneinander bewegen.
-   Spielen Sie für eine lange Dauer oder Entfernung.
-   Beziehen Sie eine große Menge an Bildschirmbereich ein.
-   Sind rechenintensiv.

Animationen mit geringeren Auswirkungen auf die Leistung:

-   Beziehen Sie ein einzelnes -Objekt ein.
-   Spielen Sie für eine kurze Dauer oder Entfernung.
-   Beziehen Sie eine kleine Menge an Bildschirmraum ein.
-   Sie sind nicht rechenintensiv.

Um eine gute Leistung zu gewährleisten, sollten intensive Animationen nur für Aufgaben verwendet werden, die nicht CPU-intensiv sind, wohingegen helle Animationen überall verwendet werden können.

Für die Reaktionsfähigkeit sollten die meisten Animationen und Übergänge so entworfen werden, dass Benutzer interagieren können, während die Animation ausgeführt wird. Wenn eine Animation nicht Teil eines Prozesses ist, machen Sie sie unabhängig von der primären Interaktion des Benutzers, und erlauben Sie Benutzern, sie zu unterbrechen.

Eine Animation wirkt sich möglicherweise nicht negativ auf die Leistung einer Aufgabe in der Realität aus, aber Benutzer haben möglicherweise die Wahrnehmung, dass sie dies tut. Verwenden Sie z. B. keine Animation, die für eine langsame, CPU-intensive Aufgabe stark erscheint, auch wenn dies die Leistung nicht beeinträchtigen würde, da Benutzer möglicherweise schlussfolgern, dass die Animation der Grund dafür ist, dass die Aufgabe langsam ist. **Wenn etwas langsam aussieht, wird es langsam, daher ist es besser, Animationen zu verwenden, die sich einfach, einfach und schnell anfühlen.** Die Verwendung von Animationen mit Snappy-Anfangs- für CPU-intensive Aufgaben ist hilfreich.

**Riskant:**

![Screenshot des Dialogfelds "Kopieren" mit Statusleiste ](images/vis-animations-image20.png)

Obwohl die Animation im Dialogfeld zum Kopieren von Windows-Dateien die Leistung beim Kopieren von Dateien nicht beeinträchtigen kann, besteht das Risiko, dass Benutzer dies glauben.

**Außerdem riskant:**

![Screenshot des Fortschritts, der in der Adressleiste angezeigt wird ](images/vis-animations-image21.png)

In diesem Beispiel sorgt die langsam aussehende Fortschrittsanimation in der Adressleiste Windows-Explorer, dass einige Aufgaben sehr langsam aussehen.

Animationen und Übergänge haben keinen Nutzen, wenn ihre Qualität so schlecht ist, dass sie die Erfahrung weniger reibungslos und weniger ansprechend machen. Um ihre Qualität zu gewährleisten, sollten Animationen so entworfen werden, dass sie ordnungsgemäß beeinträchtigt werden, wenn keine ausreichenden Systemressourcen verfügbar sind. Animationen können durch Variationen beeinträchtigt werden, die weniger Ressourcen erfordern (z. B. kürzere Längen oder niedrigere Frameraten) oder überhaupt nicht ausgeführt werden. Stellen Sie unabhängig von den verfügbaren Ressourcen sicher, dass die Animationen eine hohe Qualität haben und wie Animationen anstelle von Softwarefehlern aussehen.

Wenn Benutzer schließlich der Meinung sind, dass die Animationen und Übergänge Ihres Programms ihre Produktivität beeinträchtigen, besteht eine gute Wahrscheinlichkeit, dass einige Benutzer sie deaktivieren möchten. Um diese Möglichkeit zu unterstützen, sollten Sie die Option **alle** unnötigen Animationen deaktivieren, die im Windows-Fenster gefunden Center für erleicherte Bedienung.

### <a name="attracting-the-right-level-of-attention"></a>Gewinnen der richtigen Aufmerksamkeit

Obwohl nur einige Arten von Animationen und Übergänge speziell entwickelt wurden, um die Aufmerksamkeit des Benutzers zu gewinnen, sollten sie so entworfen werden, dass sie die richtige Aufmerksamkeit erhalten, um ihren Zweck gut zu erfüllen. Welche Möglichkeiten gibt es, um Aufmerksamkeit zu gewinnen, und wie wählen Sie die richtige aus?

**Animationseffekte**

Verschiedene Animationseffekte ziehen unterschiedliche Aufmerksamkeitsebenen auf sich. In der folgenden Liste sind die gängigsten Methoden zusammengefasst, beginnend mit den wichtigsten Maßnahmen:

-   **Schnelles Flashen.** Erfordert sofortige Aufmerksamkeit. Kann die Aufmerksamkeit der Benutzer unabhängig davon, wo das Flashen auftritt, unterbricht.
-   **Moderates Blinken.** Identisch, erfordert jedoch weniger Aufmerksamkeit mit geringerer Häufigkeit.
-   **Bouncing.** Wahrnehmbar beim sehenden Peripheriegerät und relativ anspruchsvoller Natur. Benutzer werden es wahrscheinlich bemerken, können sich aber nur dann an anderer Stelle konzentrieren, wenn die Dauer kurz ist.
-   **Bewegung.** Wahrnehmbar beim sehenden Peripheriegerät, aber nicht anspruchsvoll. Komplexe oder 3D-Bewegungen gewinnen jedoch mehr Aufmerksamkeit als einfache oder 2D-Bewegungen. Benutzer werden es wahrscheinlich bemerken, können sich aber weiterhin an anderer Stelle konzentrieren.
-   **Moderates Pulsing.** Wahrnehmbar, aber nicht störend beim sehenden Peripheriegerät. Benutzer können sich weiterhin auf andere Regionen konzentrieren. Kann Helligkeit, Farben und Größen des Pulses anpassen.
-   **Langsames Pulsieren/Leuchten.** Wahrnehmbar, aber dezent. Zieht mehr Aufmerksamkeit als ein statischer Effekt auf sich, aber Benutzer bemerken die Animation möglicherweise nur, wenn sie bereits suchen.
-   **Verblassen.** Noch weniger wahrnehmbar. Zieht mehr Aufmerksamkeit als ein statischer Effekt auf sich, aber Benutzer bemerken die Animation möglicherweise nur, wenn sie bereits suchen.
-   **Statische Hervorhebung/gleam.** Wahrnehmbar, wenn benutzer sich für die Suche entscheiden, aber keine Aufmerksamkeit erfordert, wenn es sich an anderer Stelle befindet.
-   **Umgebung/natürlich.** Durch ein natürliches, reales Aussehen ist dies nicht erkennbar.

Um den richtigen Ansatz für Ihr Programm oder Feature zu bestimmen, überlegen Sie, wie sich diese Faktoren auf die Szenarios Ihres Features beziehen.

Angenommen, Sie entwerfen ein Sofortnachrichtenprogramm, und jemand hat dem Benutzer gerade eine Nachricht gesendet. Dieses Szenario erfordert die Aufmerksamkeit des Benutzers, sollte überall wahrnehmbar sein, und normalerweise möchte der Benutzer schnell reagieren. Dieses Szenario deutet darauf hin, dass eine moderate Blinkanimation eine gute Wahl wäre. Angenommen, Sie möchten Benutzer darüber informieren, dass ein Druckauftrag abgeschlossen wurde. Benutzer sollten sich weiter auf andere Regionen konzentrieren und produktiv arbeiten können, und es ist akzeptabel, wenn benutzer dies nicht bemerken. Dieses Szenario deutet darauf hin, dass moderates bis langsames Pulsen oder Leuchten eine gute Wahl wäre.

**Dauer**

Die geeignete Dauer für das Abrufen einer Animation durch eine Aufmerksamkeit hängt vom Szenario und dem jeweiligen verwendeten Animationstyp ab. Desto mehr Aufmerksamkeit ein Animationseffekt erfordert, desto kürzer sollte die Dauer sein. Obwohl sehr subtile Effekte, die wenig Aufmerksamkeit erfordern (z. B. langsames Pulsen), unbegrenzt spielen können, sollten aufmerksamkeitserlangende Effekte nur zwischen 1 und 3 Sekunden abgespielt werden. Alles, was länger ist, birgt das Risiko, dass die Animation überfordert und lästig wird.

![Screenshot der hervorgehobenen Taskleistenschaltfläche ](images/vis-animations-image22.png)

Unter Windows 7 blinkt die Taskleiste nur eine Sekunde. Mehr wäre lästig.

**Effektverfall**

Sie sollten Animationen entwerfen, die auf aufmerksamkeitsorientierte Animationen basieren und davon ausgehen, dass Benutzer, die nicht sofort reagieren, mit anderen Maßnahmen beschäftigt sind und nicht unterbrochen werden möchten. Daher sollte ihr Ziel sein, die Aufmerksamkeit zu gewinnen, ohne sie zu fordern.

Um das richtige Gleichgewicht zu finden, um Aufmerksamkeit zu gewinnen, ohne sie zu fordern, zerfällt die Intensität eines Effekts im Laufe der Zeit. Um z. B. Aufmerksamkeit zu gewinnen, können Sie den Effekt anfänglich stark machen, aber dann den Effekt schnell verlangsamen. Dadurch wird die attraktive Leistung größtenteils durch den anfänglichen Effekt bestimmt, aber der Gesamteindruck des Benutzers wird größtenteils durch seinen Abschluss bestimmt.

![Screenshot mit reduzierter Flashrate ](images/vis-animations-image23.png)

Unter Windows 7 verlangsamt sich der Flasheffekt der Taskleiste am Ende.

### <a name="what-about-powerpoint"></a>Was ist mit PowerPoint?

Microsoft PowerPoint-Übergänge verstoßen häufig absichtlich gegen diese Richtlinien, da sie darauf ausgelegt sind, die Aufmerksamkeit auf Schiebeübergänge zu ziehen und zu verlangen, dass Benutzer darauf warten. Darüber hinaus haben sie keine besondere Bedeutung, sodass sie nichts über die Tatsache hinaus kommunizieren, dass sich eine Folie ändert.

Übergänge im PowerPoint-Stil haben bei ordnungsgemäßer Verwendung die folgenden Zwecke:

-   Sie unterbricht lange Präsentationen in kleinere Block, indem sie die Präsentation zum Anhalten zwingen.
-   Sie gewinnen die Aufmerksamkeit der Zielgruppe auf Änderungen in der Präsentation und helfen den Menschen, sich neu zu konzentrieren, wenn sie sich gefragt haben.
-   Sie geben der Präsentation einen Rhythmus, damit sie sich nicht monoton oder überfordert anfühlt.
-   Ihr Stil spiegelt die Persönlichkeit des Moderators oder des Materials wider.

Obwohl dies wichtige Ziele für eine Präsentation sind, würden solche Übergänge unnötige Aufmerksamkeit auf der Benutzeroberfläche der meisten Arten von Programmen auf sich ziehen und schnell mühsam werden.

**Unterm Strich:** Verwenden Sie Übergänge im PowerPoint-Stil nicht als Modell für Ihr Programm.

**Wenn Sie nur sechs Dinge tun...**

1.  Verwenden Sie Animationen und Übergänge, um Ihr Programm leichter zu verstehen und sich reibungsloser und ansprechender zu gestalten. Sie sollten einen eindeutigen Zweck haben. Verwenden Sie Animationen nicht nur, weil Sie dies können, oder um unnötige Aufmerksamkeit auf Ihr Programm zu ziehen.
2.  Definieren Sie ein Animationsvokabular, und verwenden Sie es konsistent im gesamten Programm. Verwenden Sie gegebenenfalls das Windows 7-Animationsvokabular.
3.  Verwenden Sie die Merkmale Ihrer Animationen, um Ihrem Programm Persönlichkeit zu verleihen und seine Marke zu stärken.
4.  Machen Sie die meisten Animationen einfach, kurz und dezent. Denken Sie daran, dass Animationen keine Aufmerksamkeit erfordern müssen, um erfolgreich zu sein. Wenn eine Animation geeignet und natürlich ist, bemerken Benutzer nur deren Fehlen.
5.  Sorgen Sie dafür, dass Ihre Animationen schnell und reaktionsfähig sind, und geben Sie ihnen ein einfaches Gefühl. Unabhängig davon, wie ansprechend Ihre Animationen sind, möchte niemand das Gefühl haben, dass er auf sie wartet. Entwerfen Sie größere Animationen, um eine graceful-Beeinträchtigung zu erhalten.
6.  Entwurf für die langfristige Ausführung. Wenn eine Animation störend, störend oder mühsam ist, gestalten Sie sie neu, oder entfernen Sie sie.

## <a name="usage-patterns"></a>Verwendungsmuster

Animationen haben mehrere Verwendungsmuster:



|   Verwendung                                                                                                               |   BESCHREIBUNG                                     |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hoverfeedback**<br/> , um zu zeigen, wo sich der Interaktionspunkt befindet. <br/>                                | Gibt an, dass der Interaktionspunkt aktiv ist. Der Hover kann auch durch einen statischen Effekt angezeigt werden.<br/> Windows-Vokabular: Anzeige des Hovereffekts (umhingendes Rechteck, Hervorhebung, Verblendung) mit einem Ein-/Ausblenden-Effekt für die Glätte. <br/> ![Screenshot eines von sechs hervorgehobenen Albumabdeckungen ](images/vis-animations-image24.png)<br/> Im digitalen Zune-Medienplayer wird das Album cover hervorhebt und Wiedergabesteuerelemente beim Zeigen hinzugefügt.<br/>                                                                                                                                                                                                                 |
| **Klicken Sie auf Feedback.**<br/> , um zu zeigen, dass ein klickbares Objekt reaktionsfähig ist und einen Klick empfangen hat. <br/>    | Gibt an, dass auf ein Objekt geklickt wurde.<br/> Windows-Vokabular: Flashobjekthintergrund beim Click-Down-Ereignis. Verwenden Sie zum Anzeigen des Berührungskontakts einen Effekt vom z.B. "Effect". <br/> ![Foto des Fingers auf dem Touchscreen mit Denkeffekten ](images/vis-animations-image25.png)<br/> Touch zeigt eine Wellenanimation an, damit der Benutzer weiß, dass die Interaktion erkannt wurde.<br/>                                                                                                                                                                                                                                                                                                         |
| **Feedback zur Auswahl**<br/> , um zu zeigen, dass ein Objekt ausgewählt ist. <br/>                                | Gibt an, dass ein Objekt ausgewählt ist. Die Auswahl kann auch durch einen statischen Effekt angezeigt werden.<br/> Windows-Vokabular: Zeichnen des Auswahlrechtecks mit einem ein- und ausblendenden Effekt für die Glätte. <br/> ![Abbildung eines Albumcovers, auf das geklickt und dann ausgewählt wurde ](images/vis-animations-image26.png)<br/> In Zune blinkt das Album beim Klicken, und dann wird ein Auswahlrechteck für die Auswahl angezeigt.<br/>                                                                                                                                                                                                                                                                      |
| **Statusfeedback**<br/> , um zu zeigen, dass eine Aufgabe ausgeführt wird. <br/>                             | Statusfeedback gibt an, dass eine Aufgabe Fortschritte macht, in der Regel mit Aktivitätsindikatoren, Statusanzeigen oder Animationen, die die Aufgabe veranschaulichen. Das Feedback zum Bestimmen des Fortschritts zeigt ungefähr, wie viel der Aufgabe durchgeführt wurde und wie viel übrig bleibt, wohingegen ein unbestimmter Fortschritt nur darauf hinweist, dass die Aufgabe durchgeführt wird.<br/> Windows-Vokabular: Rotierende Aktivitätsindikatoren, Statusanzeigen, Fortschrittshintergrund, Illustrationsanimationen. <br/> ![Screenshot des Dialogfelds mit dem Text "Anmelden" ](images/vis-animations-image27.png)<br/> In diesem Beispiel zeigt Windows Live Messenger unbestimmtes Statusfeedback während der Anmeldung an.<br/> |
| **Attraktor**<br/> , um zu zeigen, dass etwas die Aufmerksamkeit des Benutzers erfordert. <br/>                          | Gewinnen Sie die richtige Aufmerksamkeit, wenn wichtige Objekte erstellt werden oder Aufmerksamkeit erfordern (häufig aufgrund von Änderungen), oder wenn wichtige oder dringende Ereignisse passieren. sehen [Sie, wie Sie die richtige Aufmerksamkeit für](#attracting-the-right-level-of-attention) Entwurfstechniken gewinnen.<br/> Windows-Vokabular: blinkend, bewegend, pulsierend, leuchtend, blinkend. <br/> ![Screenshot der Symbolleistenanimation ](images/vis-animations-image28.png)<br/> Die Windows Live-Symbolleiste wird bei der ersten Darstellung animiert, um deutlich zu machen, wo sie sich befindet.<br/>                                                                                                                                 |
| **Beziehung**<br/> , um die Beziehung zwischen Objekten oder Kausalität in Effekten zu zeigen. <br/>        | Anzeigen von Beziehungen, insbesondere wenn die Beziehung möglicherweise nicht verstanden oder erwartet wird, auf eine Weise, die nicht störend oder verwirrend ist.<br/> Windows-Vokabular: Morphing, Transport, physische Änderungen, z. B. Umkippen, Wachsen von einer Punktquelle, Verkleinern auf ein Punktziel. <br/> ![Screenshot des Dialogfelds "Farb kalibrierung"](images/vis-animations-image29.png)<br/> In diesem Beispiel zeigt die Animation die Beziehung zwischen der Gammaeinstellung und ihren Auswirkungen auf die Anzeige.<br/>                                                                                                                                                    |
| **Abbildung/Vorschau**<br/> , um ein Konzept, eine Aufgabe oder die Auswirkung eines Befehls visuell zu erklären. <br/> | Eine Animation oder ein Video, in der ein Konzept oder die visuelle Funktionsweise erläutert wird, um eine Texterklärung zu ergänzen oder zu ersetzen. Auf diese Weise können Benutzer Aufgaben effizient und sicher ausführen oder Befehle auswählen. <br/> ![Screenshot: Rechtschreibfehler beim Korrigieren des Stifts ](images/vis-animations-image30.png)<br/> In diesem Beispiel verwenden die Befehle des Tablet PC-Eingabebereichs "show me" Abbildungen, die zeigen, wie Sie korrigieren, löschen, aufteilen und joinen.<br/>                                                                                                                                                                                                        |



 

Übergänge haben mehrere Verwendungsmuster:



|      Verwendung                                                                                                                                                                                                      |    BESCHREIBUNG                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Objektverkleinerung/-verkleinern/angezeigt**<br/> , um die Größe oder den Zustand eines Objekts reibungslos zu ändern. <br/>                                                                                                         | Objektänderungen zwischen Zuzuständen, möglicherweise während des Verschiebens. Transition sorgt dafür, dass benutzerorientierte Änderungen vorgenommen werden.<br/> Windows-Vokabular: Morph, Größe ändern, Objektfolien ein- oder aus. <br/> ![Screenshot von drei Größen von Wetter-Gadgets ](images/vis-animations-image31.png)<br/> In diesem Beispiel wird das Wetter-Gadget aus seinem präzisen Zustand gewandelt, um das Dialogfeld Optionen anzuzeigen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Inhalt ein-/ausblenden/ändern**<br/> , um Inhalte reibungslos anzuzeigen, auszublenden oder zu ändern, in der Regel für die progressive Offenlegung. <br/>                                                                       | Das Innere des Fensters wird so umgestaltet, dass mehr, weniger oder andere Inhalte angezeigt werden. Transition sorgt dafür, dass benutzerorientierte Änderungen vorgenommen werden.<br/> Windows-Vokabular: Ein- oder Ausschieben des Bereichs. Flyoutfenster werden ein- und ausgeblendet. unterschiedliche Inhalte werden ausgeblendet oder eingerollt. <br/> ![Screenshot mit drei Größen des Rechners ](images/vis-animations-image32.png)<br/> Die Windows-Rechner einen reibungslosen Übergang zwischen den Ansichtsmodi.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Ein-/Ausblenden von Steuerelementen oder Bieten**<br/> , um Steuerelemente oder deren Bezahlbarkeiten beim Zeigen oder Bewegen der Maus reibungslos ein- oder auszublenden, um die normale visuelle Darstellung zu vereinfachen. <br/>                | Anzeigen von Steuerelementen, wenn Benutzer mit dem Zeiger auf einen Befehlsbereich zeigen, oder Anzeigeanzeigen, wenn Benutzer auf ein Steuerelement zeigen. Wenn Sie auf diese Bereiche zeigen, bedeutet dies, dass der Benutzer interagieren möchte. Affordances können ausgeblendet werden, wenn der Zeiger stationär wird. <br/> ![Screenshot von ausgeblendeten Steuerelementen vor dem Zeigen ](images/vis-animations-image33.png)<br/> In diesem Beispiel werden die Windows Media Player-Steuerelemente ausgeblendet, wenn sie im Vollbildmodus mit dem Mauszeiger darauf zeigen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Szenenübergänge**<br/> , um einen reibungslosen und nahtlosen Szenenübergang zu ermöglichen, um Aufmerksamkeit zu vermeiden. <br/>                                                                                   | Plötzliche Szenenänderungen können vor allem für große Bildschirmbereiche unbrauchbar sein. Verwenden Sie daher Szenenübergänge, um Glätte und Kontinuität zu schaffen und Kontext bereitzustellen. Szenenübergänge sind so konzipiert, dass sie natürlich und niedrig sind, um zu vermeiden, dass der Prozess des Übergangs selbst beachtet wird.<br/> Windows-Vokabular: Ein-/Ausblenden; Kreuzblenden; Ein-/Links-Schieben, nach außen/rechts, nach oben, unten; pusht und deckt ab. <br/> ![Screenshot eines Fotos, das in ein anderes eingeblendet wird ](images/vis-animations-image34.png)<br/> In diesem Beispiel wird der Hintergrund des Windows-Desktops zwischen Bildern überblendet, damit der Übergang reibungslos und gesteuert wird.<br/>                                                                                                                                                                                                                                                                                                                               |
| **Besondere Szenenübergänge**<br/> , um die Aufmerksamkeit auf eine Szenenänderung zu lenken, um sie speziell zu gestalten oder die Aufmerksamkeit des Benutzers neu zu konzentrieren. <br/>                                                               | Während die meisten Szenenübergänge die Aufmerksamkeit nicht auf den Übergangsprozess lenken sollten, sind einige so konzipiert, dass sie den Flow unterbrechen und die Aufmerksamkeit auf sich ziehen, um zu verdeutlichen, dass etwas anderes passieren wird. Um die Aufmerksamkeit zu lenken, sind spezielle Szenenübergänge so konzipiert, dass sie unnatürlich sind und eine hohe visuelle Auswirkung haben. <br/> ![Screenshot der Schieberegler für den Übergang zur Aufmerksamkeit ](images/vis-animations-image35.png)<br/> In diesem Beispiel verwendet PowerPoint aufmerksamkeitsorientierte Übergänge, um die Zielgruppe in die Änderung zu ziehen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Direkte Bearbeitungen**<br/> , um die Auswirkungen direkter Bearbeitungen anzuzeigen (z. B. Verschieben, Scrollen/Schwenken, Drehen und Zoomen). <br/>                                                                   | Der Übergang zeigt die Auswirkungen der Bearbeitung in Echtzeit. der Effekt sollte reibungslos, kontinuierlich und mit der realen Welt konsistent sein. Das Verschieben und Rotieren kann an einigen Stellen nicht kontinuierlich sein, um Einschränkungen oder wahrscheinlich bevorzugte Optionen anzugeben. Durch das Zoomen wird der Inhalt größer oder kleiner, wodurch möglicherweise die Detailebene entsprechend geändert wird. <br/> ![Screenshot mit drei Bildschirmlupegrößen ](images/vis-animations-image36.png)<br/> In diesem Beispiel zoomt die Bildschirmlupe gleichmäßig zwischen ebenen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Falsche direkte Manipulationen**<br/> , um anzugeben, dass eine direkte Bearbeitung (z. B. Verschieben, Scrollen/Schwenken) versucht wurde, aber nicht durchgeführt werden konnte. <br/>                                           | Der Übergang zeigt an, dass versucht wird, die Bearbeitung zu versuchen, aber wieder in den ursprünglichen Zustand zurückgesetzt wird. oft sieht der Effekt so aus, als ob die Manipulation aufgrund einer realen physischen Einschränkung nicht durchgeführt werden kann. Diese Animationen werden anstelle von textbasierten Fehlermeldungen verwendet, die das reale Gefühl der Manipulation stören würden.<br/> Windows-Vokabular: Bounce <br/> ![Abbildung der visuellen Kommunikation von Animationen ](images/vis-animations-image4.png)<br/> In diesem Beispiel springt das Dokument, um zu zeigen, dass der Benutzer das Ende erreicht hat.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Sortieren, Filtern, Neuanordnen von Übergängen**<br/> , um anzugeben, dass sich die Darstellung oder der Inhalt einer Auflistung von Elementen geändert hat. <br/>                                                            | Der Übergang zeigt (oder bei komplexen Änderungen schlägt vor), wie sich die Änderung auswirkt. <br/> ![Screenshot von Zeilenkameras mit drei entfernten ](images/vis-animations-image37.png)<br/> ![Ähnliche Screenshots mit verschiedenen entfernten Kameras ](images/vis-animations-image38.png)<br/> ![Ähnlicher Screenshot mit entfernten anderen Kameras ](images/vis-animations-image39.png)<br/> In diesem Beispiel verwendet die visuelle Bing-Suche einen Filterübergang.<br/> ![Screenshot des Albumcovers, das seine Darstellung ändert ](images/vis-animations-image40.png)<br/> In diesem Beispiel verwendet Windows Media Center einen Übergang zur Neuanordnung als besonderes Erlebnis, während ein Titel wiedergegeben wird.<br/>                                                                                                                                                                                                                                                                                   |
| **Leistungsübergänge**<br/> , damit eine Aktion schneller geschieht. <br/>                                                                                                              | Während jeder Übergang das Potenzial hat, eine Aktion schneller zu gestalten, besteht der Hauptzweck dieser Übergänge darin, die Wahrnehmung von Leistung und Reaktionsfähigkeit zu verbessern. Eine gute Methode besteht darin, die Aufgabe in absichtlichen Schritten zu zeigen. Im Gegensatz dazu wirkt das Verzögern der Aktion, das Rendern der Ergebnisse auf zufällige Weise oder die Verwendung eines Aktivitätsindikators langsam.<br/> Windows-Vokabular: Führen Sie Aktionen in Phasen mit reibungslosen Übergängen zwischen den Phasen aus. <br/> ![Screenshot der Sprungliste zum Hinzufügen von Zielen ](images/vis-animations-image41.png)<br/> In diesem Beispiel zeigt eine Taskleiste Sprungliste sofort die Standardelemente an und schiebet dann auf, um die Ziele anzuzeigen, sobald die Liste bereit ist. Dies vergeht in der Zeit, die zum Erstellen der Liste erforderlich ist. Im Gegensatz dazu würde das Verzögern der ersten Anzeige nicht reagieren, und das Anzeigen einer unvollständigen Liste oder eines Fortschrittsfeedbacks würde sich viel langsamer anfühlen.<br/> |
| **Besondere Erfahrungen**<br/> um Benutzer bei seltenen, [besonderen Erfahrungen,](glossary.md) die für Ihr Programm wichtig sind und die volle Aufmerksamkeit des Benutzers haben, zu ansprechen und zu freuen. <br/>    | Während jeder Übergang das Potenzial hat, eine besondere Erfahrung zu sein, sind diese Übergänge am besten für seltene Erfahrungen reserviert, die wirklich speziell für Ihr Programm sind. Benutzerdefinierte Übergänge werden verwendet, um ein besonderes Gefühl zu vermitteln. Branding und Persönlichkeit sind häufig wichtige Entwurfselemente. Im Gegensatz zu anderen Mustern können besondere Erfahrungen Aufmerksamkeit erfordern, stark sein und erfordern, dass Benutzer einen Moment warten müssen. folglich werden diese Übergänge bei übermäßiger Überschreitung schnell abnutzungsfähig, da die Erfahrung nicht mehr sonderlich ist. <br/> ![Screenshot des Windows-Logos, das in einen neuen Bildschirm geändert wird ](images/vis-animations-image42.png)<br/> In diesem Beispiel zeigt Windows Media Center beim Laden eine Animation an, um Benutzer sofort einzubinden.<br/>                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Richtlinien

### <a name="effective-communication"></a>Effektive Kommunikation

-   **Definieren und verwenden Sie ein Animationsvokabular,** um sicherzustellen, dass Ihre Animationen und Übergänge eine konsistente Bedeutung haben, und verwenden Sie es konsistent im gesamten Programm. Die meisten Vokabulars sollten Einträge für Szenen- und Objektdarstellung und -darstellung, Navigation, grundlegende Interaktion (Zeigen, Auswählen, Klicken), Objektbearbeitung und Interaktion (Verschieben, Ablegen, Ändern der Größe, Scrollen, Schwenken, Zoomen, Drehen, Filtern) und Aufmerksamkeit umfassen. Konsistente Bedeutung ist entscheidend für eine effektive Kommunikation.
-   **Verwenden Sie nach Möglichkeit das Windows-Animationsvokabular.** Obwohl Ihr Programm möglicherweise eine andere Zielgruppe und unterschiedliche Anforderungen hat, überwiegen oft die Vorteile der Konsistenz und Vertrautheit die Vorteile der Unterschiedlichkeit. Wenn das Vokabular Ihres Programms unterschiedlich sein muss, verwenden Sie die gleichen grundlegenden Animationstypen wie Windows, aber geben Sie ihnen die richtige Persönlichkeit für Ihr Programm.
-   **Weisen Sie generischen Animationen und Übergängen in einem Animationsvokabular keine bestimmten Bedeutungen zu.** Generische Übergänge wie Einblendungen und Sondereffekte wie z.B. Effekte haben keine bestimmte Bedeutung (über das Erscheinen oder Verschwinden hinaus), sodass sie frei verwendet werden können.

    **Falsch:**

    ![Screenshot eines Dialogfelds, das in ein anderes eingeblendet wird ](images/vis-animations-image43.png)

    In diesem Beispiel wird fälschlicherweise eine Kreuzblendung verwendet, um zum nächsten Element zu navigieren. Da Kreuzblendungen keine besondere Bedeutung haben, bietet dieser Übergang keinen Kontext.

-   **Machen Sie Vokabulareinträge eindeutig eindeutig.** Verwandte Aktionen können ähnliche Auswirkungen haben (z. B. sollte das Vergrößern und Verkleinern umgekehrte Übergänge aufweisen), aber nicht verknüpfte Aktionen sollten eindeutig unterschiedliche Auswirkungen haben (z. B. sollte das Zoomen nie mit dem Drehen verwechselt werden).
-   **Halten Sie reale Effekte realistisch und konsistent.** Wenn Sie realistische Animationen und Übergänge verwenden, halten Sie die Erfahrung mit der realen Welt konsistent. Benutzer sollten sich nie über die Ergebnisse verunsichern, verwirren oder verführen lassen. Mischen Sie aus Konsistenzgründen keine Metaphern.
-   **Geben Sie inverse Aktionen inverse Animationen an.** Dies erfüllt die Erwartungen der Benutzer und vereinfacht das Vokabular. Wenn z. B. ein Bereich durch Einschieben angezeigt wird, entfernen Sie ihn, indem Sie ihn entfernen, nicht mit einem anderen Effekt.
-   **Sorgen Sie dafür, dass Animationen greifbar werden.** Benutzer sollten in der Lage sein, den Zweck einer Animation schnell zu verstehen. Es ist möglich, eine Animation zu klein, zu kurz (weniger als 50 Millisekunden) oder so dezent zu gestalten, dass Benutzer ihren Zweck nicht verstehen können. In solchen Fällen entweder umgestalten, um die Bedeutung klar zu machen, oder entfernen.

    **Falsch:**

    ![Screenshot der Animation beim Löschen des Dialogfelds ](images/vis-animations-image44.png)

    In diesem Beispiel ist der Effekt so klein und dezent, dass nur wenige Benutzer seinen Zweck verstehen können. Besser umgestalten oder entfernen.

### <a name="patterns"></a>Muster

**Feedback mit dem Mauszeiger**

-   **Um reaktionsfähig zu sein, versuchen Sie, Animationen innerhalb von 50 Millisekunden nach dem Eintreten oder Verlassen des Hoverzustands wiederzugeben.**
-   **Um schnell zu sein, sollte die Dauer von Animationen mit dem Mauszeiger weniger als 50 Millisekunden betragen.**
-   **Verwenden Sie einen Effekt zum Ein- bzw. Ausblenden des Hovereffekts.** Dadurch unterscheiden sich Hovereffekte deutlich vom Klick- und Auswahlfeedback.

**Klicken Sie auf Feedback.**

-   **Um reaktionsfähig zu sein, versuchen Sie, Animationen innerhalb von 50 Millisekunden nach dem Click-Down-Ereignis wiederzuspielen.** Click up events don't need click feedback .
-   **Um schnell zu erscheinen, geben Sie die Dauer von Klickanimationen auf weniger als 50 Millisekunden an.**
-   **Verwenden Sie einen Flash- oder Blinkeffekt im Hintergrund.** Dadurch unterscheiden sich Klickeffekte deutlich vom Zeigen und Auswahlfeedback. Da das Klicken mit dem Hovern erforderlich ist, machen Sie Click Feedback zu einer reibungslosen Ergänzung zum Hoverfeedback.

**Feedback zur Auswahl**

-   **Um reaktionsfähig zu sein, sollten Sie Animationen innerhalb von 50 Millisekunden nach Auswahl oder Deselektion wiedererlangen.**
-   **Um schnell zu erscheinen, geben Sie die Dauer von Auswahlanimationen auf weniger als 50 Millisekunden an.**
-   **Verwenden Sie einen Ein-/Ausblenden-Auswahlrechteckeffekt.** Dadurch unterscheidet sich die Auswahl deutlich vom Zeigen und Klicken auf Feedback.

**Statusfeedback**

-   **Verwenden Sie einen Aktivitätsindikator, wenn eine Aktion nicht innerhalb einer Sekunde ausgeführt werden kann.** Dies gibt an, dass der Befehl empfangen wurde.
-   **Verwenden Sie eine Statusleiste, wenn eine Aufgabe mehr als fünf Sekunden dauert.** Weitere Richtlinien finden Sie unter [Statusleisten](progress-bars.md).
-   **Verwenden Sie Statusfeedbackanimationen, mit denen Benutzer die Auswirkungen von Aufgaben mit langer Ausführungslauf visualisieren können.** Vermeiden Sie unnötige Statusfeedbackanimationen, wenn eine Animation nichts Hilfreiches kommuniziert. Verwenden Sie stattdessen eine Statusleiste.
-   **Klar erkennbare Vervollständigungs- und Fehlerzustände.** Benutzer müssen in der Lage sein, diese Endzustände schnell zu bestimmen.
-   **Der Fortschritt wird nicht mehr angezeigt, wenn die zugrunde liegende Aufgabe keinen Fortschritt erzielt.** Benutzer müssen ermitteln können, ob kein Fortschritt erzielt wird, und entsprechend reagieren.

**Attraktoren**

-   **Verwenden Sie Gewinnungserziehende mit Nehmern.** Sofern die Informationen nicht dringend, kritisch oder anderweitig wahrscheinlich auf das unmittelbare Verhalten des Benutzers auswirken, ist es in der Regel besser, den Zustand unauffällig zu ändern und den Benutzern die Änderung selbst zu ermöglichen. [Lösen Sie Ableitungen, nicht auf erkennbar.](/windows/desktop/uxguide/how-to-design-desktop-ux)

    ![Screenshot der Drahtlosen Statussymbole ](images/vis-animations-image45.png)

    In diesem Beispiel verwendet das Symbol für den Benachrichtigungsbereich des Drahtlosnetzwerks eine Animation für kritische Probleme, ermöglicht benutzern jedoch, selbst schwache Signale zu erkennen.

-   **Wählen Sie eine Animation aus, die die richtige Aufmerksamkeit auf sich zieht.** Zieheranimationen sollten nur genügend Aufmerksamkeit auf sich selbst ziehen, um ihren Zweck zu erfüllen, aber nicht mehr. Wenn der Benutzer sofort reagieren muss, wählen Sie einen Effekt aus, der Aufmerksamkeit erfordert, unabhängig davon, wo der Benutzer sucht. Informationen zu anderen Situationen finden Sie im Abschnitt [Gewinnen](#attracting-the-right-level-of-attention) der richtigen Aufmerksamkeitsebene, um die richtige Kombination aus Aufmerksamkeit, Aufsehen und Dringendkeit zu erhalten.

    **Falsch:**

    ![Screenshot des Büroassistenten für Büroclips ](images/vis-animations-image46.png)

    Die Microsoft Office-Assistenten erfordern unnötige Aufmerksamkeit für sich selbst.

-   **Wenn der Benutzer nicht antwortet, wiederholen Sie die Animation nicht, und verwenden Sie keine kontinuierlichen Animationen.** Gehen Sie stattdessen davon aus, dass der Benutzer sich entschieden hat, jetzt nicht zu handeln, sondern später handeln kann. Kontinuierliche Animationen erschweren es Benutzern, sich auf etwas anderes zu konzentrieren.

**Beziehungsanimationen**

-   **Verwenden Sie Beziehungsanimationen, um zu zeigen, woher Objekte stammten oder wo sie hinkamen.**
-   **Beziehungsanimationen müssen mit dem ausgewählten Objekt beginnen oder enden.** Zeigen Sie keine Beziehungen zwischen Objekten an, mit denen der Benutzer derzeit nicht interagiert. Wenn Benutzer überhaupt bemerken, wird ihnen die Ableitung aufgefallen.

**Abbildungen/Vorschauen**

-   **Verwenden Sie Vorschauversionen, um die Auswirkungen eines Befehls anzuzeigen, ohne dass Benutzer ihn zuerst ausführen müssen.** Mit hilfreichen Vorschauversionen können Sie die Effizienz und Einfachheit des Lernens Ihres Programms verbessern und den Bedarf an Test- und Fehlerversuchen reduzieren.
-   **Verwenden Sie Abbildungen und Vorschauen, die eine klare Interpretation haben.** Sie haben wenig Wert, wenn sie verwirrend sind.
-   **Geben Sie immer nur eine Abbildung nach der anderen wieder,** um zu vermeiden, dass Benutzer überfordert werden. Wenn mehrere gleichzeitige Abbildungen möglich sind, verwenden Sie den Mauszeiger oder eine Wiedergabeschaltfläche, damit Benutzer ihr Interesse angeben können.
-   **Gibt eine Abbildung automatisch wieder, wenn dies der Hauptzweck des Fensters oder der Seite ist.** Wenn dies optional ist, können Benutzer dies auch wieder geben, wenn sie bereit sind.
-   **Wiedergabeanimationen mit der optimalen Geschwindigkeit:** Nicht so schnell, dass sie schwer zu verstehen sind, aber nicht so langsam sind, dass sie mühsam zu beobachten sind.

**Objektverkleinerung/-verkleinerung**

-   **Beschneiden Sie inhalte während einer Größenvergrößerung nicht.** Erweitern Sie Container, bevor Sie Inhalt hinzufügen. Entfernen Sie Inhalt, bevor Sie Container reduzieren.

    **Falsch:**

    ![Screenshot des abgeschnittenen Rechners ](images/vis-animations-image47.png)

    In diesem Beispiel wird der Inhalt während einer Größenvergrößerung abgeschnitten.

**Inhalt ein-/ausblenden/ändern**

-   **Zeigen Sie wichtige Informationen statisch an.** Benutzer sollten nicht durch progressive Offenlegung auf wichtige Informationen zugreifen müssen.

**Ein-/Ausblenden von Steuerelementen oder Vorhaltungen**

-   **Zeigen Sie wichtige Steuerelemente an, wenn der Benutzer den Mauszeiger an einer beliebigen Stelle im Fenster oder Bereich oder, wenn der Vollbildmodus angezeigt wird, während der Mauszeiger bewegt wird.** Benutzer sollten nicht nach diesen Steuerelementen suchen müssen. Stellen Sie daher sicher, dass ihre Ermittlung sicher ist.

    ![Abbildung, die zeigt, wie steuerelemente mit dem Zeigen angezeigt werden ](images/vis-animations-image48.png)

    In diesem Beispiel zeigt Windows Media Center seine Steuerelemente immer dann an, wenn sich der Zeiger über dem Fenster befindet.

-   **Zeigen Sie sekundäre Steuerelemente oder Steuerelementen an, wenn der Benutzer den Zeiger auf die Befehle oder in der Nähe der Befehle positioniert.** Machen Sie den Standort offensichtlich und das Ziel groß, um die Aufholbarkeit zu verbessern.

    ![Screenshot des Zeigers, der den sekundären Befehl zeigt ](images/vis-animations-image49.png)

    In diesem Beispiel zeigt Windows Live Messenger einen sekundären Befehl an, wenn sich der Zeiger in der Nähe der oberen rechten Ecke befindet.

**Szenenübergänge**

-   **Sorgen Sie dafür, dass physische Szenenübergänge mit der natürlichen Zuordnung konsistent sind.** In westen Kulturen lesen Menschen von links nach rechts, und hierarchische Diagramme fließen von oben nach unten. Folglich wird die Zukunft in der Zeit durch die Bewegung von links nach rechts angezeigt. Die folgenden physischen Szenenübergänge haben eine natürliche Zuordnung:



    | Übergang                          | Bedeutung                                     |
    |---------------------------|--------------------------------------|
    | Von links<br/>      | Zurück in Den Taskfluss verschieben<br/>    |
    | Von rechts<br/>     | Weiter im Aufgabenfluss<br/> |
    | Von oben<br/>       | Taskhierarchie nach oben verschieben<br/>    |
    | Von unten<br/>    | Taskhierarchie nach unten verschieben<br/>  |



 

-   **Wenn Ihr Programm Sound abspielt, werden Szenenübergänge und Audioübergänge zusammen gewendet.** Wenn eine Szene z. B. allmählich ausblendet, sollte jeder Sound auch schrittweise ausgeblendet werden. Lassen Sie nahtlose visuelle Übergänge nicht durch plötzliche Soundübergänge zu. Weitere Soundrichtlinien finden Sie unter [Sound](vis-sound.md).

**Direkte Manipulationen**

-   **Wenn Sie physische Gesten in der Interaktion verwenden (z. B. Bewegungen), entwerfen Sie die Animation so, dass sie sich wie eine natürliche Antwort auf die Geste anfühlt.** Verknüpfen Sie die Interaktionsursache mit dem Übergangseffekt. Geben Sie der Animation reale physische Merkmale wie Beschleunigung, Verlangsamung, Bewegung, Widerstand, Gewicht, Bounce und Drehung.
-   **Um ein direktes Gefühl zu erhalten, halten Sie die Kontaktpunkte eines Objekts während der gesamten Interaktion reibungslos unter dem Zeiger.** Jede Verzögerung, abgesenkte Antwort oder ein Verlust des Kontakts zerstört die Wahrnehmung der direkten Manipulation. Objekte sollten nie verschwinden, während sie bearbeitet werden.

**Sortieren, Filtern oder Neuordnen von Übergängen**

-   **Zeigen Sie bei einfachen Änderungen den gesamten Übergang an.** Benutzer können den gesamten Übergang problemlos verfolgen. Einfache Änderungen umfassen vier Elemente oder weniger.
-   **Heben Sie bei komplexen Änderungen das Ende der Bewegung hervor, wenn sie verlangsamt wird, und lassen Sie das Auge auffüllen.** Dadurch wird die Bewegung viel reaktionsfähiger und geordneter.

**Leistungsübergänge**

-   **Erwägen Sie die Durchführung langsamer Übergänge in zwei oder drei Phasen, damit sie schneller und sofort interaktiv angezeigt werden.** Verwenden Sie gegebenenfalls die folgende Kompositions reihenfolge:
    -   Externer Frame
    -   Hintergrund
    -   Ursprünglicher Inhalt (bei Bedarf mithilfe einer temporären Darstellung)
    -   Primäre Steuerelemente (sodass Benutzer sofort interagieren können)
    -   Sekundäre Steuerelemente und alle verbleibenden Benutzeroberflächenelemente
    -   Final content (if a temporary representation was used) Use transitions like fades and slides to make the composition appear smooth, orderly, and refined.

![Screenshot der Karte mit Satellitenfoto und Raster ](images/vis-animations-image50.png)

Beim Scrollen in der Ansicht "Aus den Augen des Auges" zeigen Bing-Karten einen temporären Rasterhintergrund an. Auf diese Weise können Benutzer sofort scrollen, bevor der endgültige Inhalt gerendert wird.

**Animationen mit besonderer Erfahrung**

-   **Animierte Begrüßungsbildschirme (sowie statische Begrüßungsbildschirme) animieren.** Begrüßungsbildschirme machen häufig nur darauf aufmerksam, wie lange das Laden eines Programms dauert, und die Begrüßung wird schnell verschleieren. Begrüßungsbildschirme sind zwar akzeptabel, wenn sie nur angezeigt werden, wenn eine Benutzerinteraktion nicht möglich ist, aber wenn möglich, ist es eine bessere Alternative, Ihr Programm so zu entwerfen, dass Benutzer sofort damit interagieren können, auch wenn es noch geladen wird.
-   **Geben Sie den Befehl Einführung überspringen an, wenn ein animierter Begrüßungsbildschirm länger als drei Sekunden dauert.** Wenn Sie auf eine beliebige Stelle auf dem Begrüßungsbildschirm klicken, sollte sie ebenfalls verworfen werden. Alternativ können Sie nach einem anfänglichen Zeitraum eine kurze Version der Animation verwenden.

### <a name="performance"></a>Leistung

-   **Sorgen Sie nicht dafür, dass Benutzer auf die Animationen und Übergänge Ihres Programms warten.** Verwenden Sie nach Möglichkeit kurze Animationen und Übergänge (weniger als 200 Millisekunden). Verwenden Sie schnellere Animationen (100 Millisekunden) für häufigere Vorgänge. Entwerfen Sie längere Animationen (in der Regel mehr als eine Sekunde das Statusfeedback, die Abbildung und spezielle Erfahrungsmuster), damit Benutzer weiterhin arbeiten können, während sie ausgeführt werden.
-   **Entwerfen Sie Animationen mit langer Laufzeit, um Benutzern klar zu machen, dass sie interagieren können, während die Animation ausgeführt wird.** Benutzer versuchen nicht, weiter zu arbeiten, wenn die visuellen Hinweise darauf hindeuten, dass sie dies nicht können.

    ![Screenshot einer Statusleiste in einer Statusleiste ](images/vis-animations-image51.png)

    In diesem Beispiel aus Windows Internet Explorer die Statusleiste mit geringem Schlüssel in der Statusleiste darauf hin, dass Benutzer nicht auf den Abschluss warten müssen, bevor sie interagieren können.

-   **Verwenden Sie einfache Animationen für CPU-intensive Aufgaben.** Dadurch erhält die Aufgabe volle Verarbeitungsleistung. Darüber hinaus werden Benutzer nicht erkennen, dass die einfache Animation der Grund dafür ist, dass die Aufgabe CPU-intensiv ist.
-   **Zeigen Sie während einer Animation oder eines Übergangs keinen Aktivitätsindikator an.** Dadurch wird der Effekt zerstört. Entwerfen Sie Animationen und Übergänge, damit sie sofort beginnen können.
-   **Entwerfen Sie Animationen so, dass sie ordnungsgemäß heruntergestuft werden, wenn nicht genügend Systemressourcen verfügbar sind.** Animationen können durch Variationen beeinträchtigt werden, die weniger Ressourcen erfordern (z. B. kürzere Längen oder niedrigere Frameraten) oder überhaupt nicht ausgeführt werden. Stellen Sie unabhängig von den verfügbaren Ressourcen sicher, dass die Animationen eine hohe Qualität haben und wie Animationen anstelle von Softwarefehlern aussehen.

    **Falsch:**

    ![Screenshot des ausgeblendeten Programmrahmens über dem Desktop ](images/vis-animations-image52.png)

    In diesem Beispiel wird der Übergang zur Fensterwiederherstellung verwendet, obwohl nicht genügend Systemressourcen vorhanden sind, um ihn gut zu spielen. Folglich scheint der fixierte Frame ein Fehler zu sein. Wenn die Ressourcen nicht verfügbar sind, ist es besser, einfach das Fenster ohne Übergang anzuzeigen.

### <a name="animation-characteristics"></a>Animationsmerkmale

Gut entworfene Animationen und Übergänge haben im Allgemeinen die folgenden Merkmale:

-   **Kurze Dauer.** Die meisten Animationen sollten zwischen 100 und 300 Millisekunden liegen, vorzugsweise entweder 1/6 Sekunde (167 Millisekunden) oder 1/4 Sekunde (250 Millisekunden). (Spezielle Erfahrungen und Feedback zum Fortschritt können länger sein.) Verwenden Sie schnellere Animationszeiten für häufigere Vorgänge. Im Allgemeinen dauert es länger, dass längere Animationen abgeschlossen sind, sich mehr Zeit für das Verständnis nehmen und sich langsam anfühlen.
-   **Reaktionsfähigkeit.** Animationen sollten innerhalb von 50 Millisekunden nach dem initiierenden Ereignis oder der Benutzeraktion beginnen. Längere Startzeiten reagieren nicht.
-   **Beschleunigung/Verlangsamung.** Um natürlich aus aussehen zu können, müssen die meisten Animationseffekte beim Starten beschleunigt und beim Beenden verlangsamt werden. Entwerfen Sie Animationen für schnelle Starts, um reaktionsfähig zu sein. Um kontrolliert zu erscheinen, entwerfen Sie Animationen, um am Ende soft Landings zu erhalten. Dies gilt zwar für Bewegungseffekte, gilt aber auch für alle Effekte, die Bewegungen vorschlägt, z. B. Zooms und sogar Verblassungen.

    ![Abbildung eines Diagramms, das eine geringere Geschwindigkeit im Laufe der Zeit zeigt ](images/vis-animations-image53.png)

    Die meisten Animationen sollten schnelle Starts und weiche Endungen haben, um ein reaktionsfähiges, aber kontrolliertes Gefühl zu haben.

-   **Bewegung.** Insbesondere Animationen, die bewegungen, müssen beschleunigt und verlangsamt werden. Verwenden Sie daher keine lineare Bewegung, es sei denn, die Animationsdauer ist sehr kurz. Bewegungen sollten den Shorts-Pfad von Anfang bis Ende nehmen, ohne zu überdrehen. Der vollständige Bewegungspfad ist nicht immer erforderlich. Heben Sie gegebenenfalls das Ende der Bewegung hervor, wenn es verlangsamt wird, und lassen Sie das Auge auffüllen. Dadurch wird die Bewegung viel reaktionsfähiger und geordneter. Wenn Sie die Bewegung mehrerer Objekte gleichzeitig animieren, geben Sie ihnen leicht unterschiedliche Pfade mit etwas unterschiedlichen Zeitsteuerungen, um sich natürlicher anfühlen zu können.
-   **Bildrate.** Die meisten Animationen sollten eine Bildfrequenz von 20 Bildern pro Sekunde verwenden. Wenn die Animation für eine besondere Erfahrung ist oder mit dem Hauptzweck des Programms zusammenhing, sollten Sie erwägen, eine höhere Rate von 24 30 Frames pro Sekunde zu verwenden, um die Glätte und Realität zu verbessern.
-   **Skalierung.** Entwerfen Sie Animationen so, dass sie für den gesamten vorgesehenen Verwendungsbereich gut funktionieren. Beispielsweise sollten Seitenübergänge so entworfen werden, dass sie für alle Seitengrößen funktionieren.
-   **Persönlichkeit.** Entwerfen Sie Animationen so, dass sie sich natürlich, dedudiert und effizient und nicht wie künstliche, launische oder langsame Animationen verhalten.

### <a name="animated-text"></a>Animierter Text

-   Sie können Text zwar mithilfe eines Übergangs anzeigen, **aber nicht kontinuierlich Animieren von Text.** Animierter Text ist oft abgelenkt und schwieriger zu lesen als statischer Text. **Ausnahmen:**
    -   Sie können Text in Situationen animieren, in denen er traditionell animiert ist, und Sie stellen eine barrierefreie Alternative zur Verfügung.
    -   Sie können Text animieren, wenn der Zweck des Texts hauptsächlichdekorativ ist.

![Screenshot der kreativ gestalteten Zune-Schnittstelle ](images/vis-animations-image13.png)

In diesem Beispiel animiert Zune Text, aber sein Zweck ist in erster Linie dekohativ. Es gibt kein Problem, wenn Benutzer den Text nicht sorgfältig lesen.

### <a name="reducing-power-consumption"></a>Reduzieren des Energieverbrauchs

-   **Entwerfen Sie Ihre Animationen, um den Energieverbrauch zu reduzieren.** Bei ordnungsgemäßer Entwicklung sollten Animationen den Energieverbrauch nicht erheblich erhöhen. So reduzieren Sie den Energieverbrauch:
    -   **Beenden Sie die Animation, wenn die Anzeige deaktiviert ist.** Die Anzeige ist möglicherweise ausgeschaltet, um Energie zu sparen.
    -   **Verwenden Sie keine Animationen mit langer Laufzeit, die nicht vom Benutzer initiiert wurden.** Animationen, die regelmäßige Timer mit hoher Auflösung verwenden, verringern die Effizienz der Prozessorleistungsverwaltung. Achten Sie außerdem darauf, dass Sie alle periodischen Timer mit hoher Auflösung deaktivieren, wenn die Animationen abgeschlossen sind.
    -   **Alle Animationen werden angehalten, wenn sich das System im Leerlauf befindet.** Der Zeitraum der Benutzerinaktivität, der in den Leerlauf übergedauert werden soll, wird durch Energieoptionen in Systemsteuerung.

### <a name="accessibility"></a>Zugriff

-   **Verwenden Sie Animationen nicht als einzige Möglichkeit, wichtige Informationen zu vermitteln.** Animationen sollten Informationen kommunizieren, die nützlich, aber nicht kritisch sind, da sie für Benutzer mit sehbehinderten Funktionen nicht zugänglich sind.
-   **Stellen Sie sicher, dass gleichwertige Informationen auf andere Mittel verfügbar sind, z.** B.:

    -   **Nach Überprüfung.** Benutzer können äquivalente Informationen ermitteln, indem sie sich den Bildschirm oder die Objekte ansehen, die an der Animation beteiligt sind.
    -   **Durch einfache Interaktion.** Benutzer können entsprechende Informationen ermitteln, indem sie mit dem Mauszeiger zeigen, klicken oder doppelklicken.

    ![Screenshot der Bing-Startseite mit Hotspots ](images/vis-animations-image54.png)

    Die Bing-Startseite enthält eine anfängliche Animation, die mehrere Hotspots aufdecken kann. Benutzer können die Hotspots auch anzeigen, indem sie den Cursor in ihrer Nähe bewegen.

    Beachten Sie, dass "äquivalente Informationen" keine identischen Informationen bedeutet. Die Informationen können in einem anderen Format vorliegen oder erfordern eine einfache Ableitung.

-   **Legen Sie ggf. den Eingabefokus auf das Objekt fest, das während eines Übergangs geändert wurde.** Auf diese Weise können Hilfstechnologien erkennen, wo die Änderung stattgefunden hat. Ändern Sie den Eingabefokus jedoch nicht, wenn der Benutzer die Tastatur verwendet.
-   **Verwenden Sie keine Animationen oder Übergänge, die Objekte schnell flashen oder deren Größe ändern.** Flashing und schnelle Bildschirmänderungen können zu Problemen für Personen mit Sehbehinderung und anderen Störungen führen.
-   **Benutzern das Deaktivieren der Animationen und Übergänge Ihres Programms gestatten.** Um diese Funktion zu unterstützen, beachten Sie die Option Alle unnötigen Animationen deaktivieren im Center für erleicherte Bedienung in Windows.

    **Entwickler:** Sie können mithilfe der SystemParametersInfo-API ermitteln, ob Animationen aktiviert sind.

-   **Entwurfsaufgaben unter der Annahme, dass Benutzer die Animationen Ihres Programms deaktivieren.** Stellen Sie sicher, dass der Taskflow dadurch nicht erheblich unterbrochen wird.

Weitere Richtlinien zur Barrierefreiheit finden Sie unter [Barrierefreiheit](inter-accessibility.md).

## <a name="documentation"></a>Dokumentation

-   Vermeiden Sie es nach Möglichkeit, auf Animationen zu verweisen. Verweisen Sie stattdessen auf das Objekt, das animiert wird, und ggf. auf den Animationstyp.
-   Beziehen Sie sich nicht auf Übergänge, außer in der technischen Dokumentation. Verweisen Sie stattdessen auf das Objekt im endgültigen oder anfänglichen Zustand.
-   Wenn der Benutzer explizit eine Animation initiiert, verwenden Sie die Verbwiedergabe. Verwenden Sie andernfalls die Verbverwendung für die technische Dokumentation.

Beispiele:

-   Sie werden wissen, dass ein Element Ihre Aufmerksamkeit benötigt, wenn sein Symbol mit dem Springen beginnt.
-   Wählen Sie zunächst die Fotos aus, die Sie drucken möchten (beachten Sie, dass die Fotos bei der Auswahl vergrößert werden).
-   Verwenden Sie einen Überblendungsübergang, um den Zustand eines Objekts nahtlos zu ändern.

