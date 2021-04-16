---
title: Animationen und Übergänge
description: Mithilfe der strategischen Verwendung von Animationen und Übergängen kann Ihr Programm leichter zu verstehen sein, es kann sich als etwas Glätte, natürlicher und von höherer Qualität erweisen und die Benutzerfreundlichkeit verbessern.
ms.assetid: 9e0e9604-f051-47e4-bcd0-59fbfd38b9c1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6d57c696bd78df9c9505bb85453456f10631a00d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104566053"
---
# <a name="animations-and-transitions"></a>Animationen und Übergänge

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mithilfe der strategischen Verwendung von Animationen und Übergängen kann Ihr Programm leichter zu verstehen sein, es kann sich als etwas Glätte, natürlicher und von höherer Qualität erweisen und die Benutzerfreundlichkeit verbessern. Die kostenlose Verwendung von Animationen und Übergängen kann das Programm jedoch ablenkend und sogar lästig machen.

Animationen gestalten die Darstellung von Bewegung oder ändern sich im Laufe der Zeit. Verwenden Sie Animationen, um Feedback zu geben, die Auswirkungen einer Aktion in der Vorschau anzuzeigen, die Beziehung zwischen Objekten anzuzeigen, auf Änderungen aufmerksam zu machen oder eine Aufgabe visuell zu erläutern.

![Abbildung der numerischen Tastatur mit hervorgehobenem Schlüssel ](images/vis-animations-image1.png)

Microsoft Windows verwendet eine Hintergrund-Flash-Animation, um Feedback zu geben, auf das das Objekt geklickt wurde.

Übergänge sind Animationen, die verwendet werden, um die Benutzer auf der Benutzeroberfläche (UI)-Zustandsänderungen und Objekt Manipulationen zu halten und diese Änderungen als Smooth-anstelle von jarringverhalten zu gestalten. Gute Übergänge fühlen sich natürlich, und es wird oft die Illusion angezeigt, dass Benutzer mit echten Objekten interagieren.

![Screenshot, der drei Größen von Wetter Gadgets zeigt.](images/vis-animations-image2.png)

Windows-Desktop-Mini Anwendungen verwenden reibungslose Übergänge zwischen ihren präzisen und Detail Zuständen.

Im Allgemeinen werden die besten Animationen und Übergänge verwendet, um mit den Benutzern nicht verbal zu kommunizieren und Zustandsänderungen natürlicher und weniger bemerkbar zu machen. Im Gegensatz dazu sind die geringsten Nachteile darin, dass Sie keine Inhalte kommunizieren oder unnötige Aufmerksamkeit ziehen. Animationen werden am besten als sekundäre Form der Kommunikation verwendet. Sie sollten Informationen, die hilfreich, aber nicht kritisch sind, übermitteln und darauf zugreifen können, dass Benutzer in der Lage sein sollten, entsprechende Informationen auf andere Weise zu ermitteln.

**Hinweis:** Richtlinien im Zusammenhang mit [Software Branding](exper-branding.md), [Sound](vis-sound.md)und [Barrierefreiheit](inter-accessibility.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Beachten Sie die folgenden Fragen, um zu entscheiden.

### <a name="animations"></a>Animationen

Gelten die folgenden Bedingungen?

-   Die Animation kommuniziert visuell etwas Nützliches, wie z. b. das Senden von Feedback, das darstellen von Beziehungen, Gründe und Auswirkungen oder das Zeichnen auf wichtige Änderungen.
-   Das Anzeigen der Animation ist nicht zwingend erforderlich. Äquivalente Informationen können auf andere Weise abgerufen werden. Benutzer profitieren möglicherweise nicht von der Animation, wenn Folgendes gilt:
    -   Sie haben Animationen deaktiviert.
    -   Ihre Aufmerksamkeit ist an anderer Stelle.
    -   Sie sind optisch beeinträchtigt.
    -   Die Animation wird von einem anderen Fenster verdeckt.
    -   Die Animation wird aufgrund unzureichender Systemleistung nicht wiedergegeben.
-   Die Animation wirkt sich nicht auf die Produktivität des Benutzers aus. Entweder:
    -   Dies erfolgt schnell (200 Millisekunden oder weniger).
    -   Dies beeinträchtigt die Interaktion nicht, oder es kann unterbrochen werden.
    -   Der Benutzer muss auf jeden Fall warten.
-   Die Animation wirkt sich nicht auf den Flow des Benutzers aus.
    -   Sie ist entweder im Mittelpunkt des Benutzers, oder Sie bezieht sich auf etwas, das außerhalb der Aufmerksamkeit liegt, das beim Abschließen einer Aufgabe wichtig oder nützlich ist.
    -   Es kann leicht ignoriert werden, nicht ablenkend oder lästig.
    -   Es wird nicht mehr mehr angezeigt. Benutzer finden Sie nach der wiederholten Anzeige auch nach Bedarf.

Wenn dies der Fall ist, sollten Sie eine Animation verwenden.

### <a name="transitions"></a>Transitions

Handelt es sich um einen Objekt-oder Szenenwechsel Zustand, der alle oben genannten Bedingungen für die Verwendung von Animationen und eine der folgenden Bedingungen erfüllt?

-   Die Zustandsänderung ist konzeptionell Disorienting, verwirrend oder anderweitig schwer zu verstehen.
-   Die Statusänderung ist visuell und ohne jegliche Kontinuität oder Glätte. oder ist unnatürlich, unpoliert oder von schlechter Qualität, insbesondere dann, wenn Sie einen großen Bildschirmbereich umfasst.
-   Die Verwendung eines Übergangs führt dazu, dass die Zustandsänderung schneller erscheint.
-   Die Zustandsänderung ist mit besonderer Benutzer Aufmerksamkeit zu tun.

Wenn dies der Fall ist, sollten Sie einen Übergang verwenden.

## <a name="design-concepts"></a>Entwurfskonzepte

Animationen und Übergänge sind eine effektive Möglichkeit, um Informationen visuell zu kommunizieren, die andernfalls Text zur Erläuterung benötigen oder von Benutzern übersehen werden könnten.

**Falsch:**

![Screenshot des Dialog Felds mit der Meldung ](images/vis-animations-image3.png)

**Richtig:**

![Abbildung der visuellen Darstellung der Animation ](images/vis-animations-image4.png)

Die Verwendung einer Animation kommuniziert mit denselben Informationen, aber auf natürliche und unaufdringliche Weise. Was würden Sie eher tausend Mal sehen?

**Animationen und Übergänge müssen keine Aufmerksamkeit erfordern, um erfolgreich zu sein.** Sie werden häufig verwendet, um die Aufmerksamkeit auf Programm Mechanismen zu vermeiden, die Benutzer nicht kennen müssen. Viele erfolgreiche Animationen sind so natürlich, dass Benutzer sich nicht einmal bewusst sind. vielmehr bemerken Benutzer nur ihre Abwesenheit. Die Häufigkeit des Vorkommens erhöht den Bedarf an Feinheiten, sodass Sie Auswirkungen auf seltene Ereignisse haben, die die Aufmerksamkeit wirklich verdienen.

![Screenshot aller Programme, die in den rückwärts Pfeil Wechseln ](images/vis-animations-image5.png)

Ein Start Menü Übergang, der das Zeichnen von Aufmerksamkeit vermeidet.

Wenn Sie das Programm leichter verständlich machen und sich ein glatteres Gefühl machen möchten, **sind gut gestaltete Animationen und Übergänge eine hervorragend Möglichkeit, Ihrem Programm eine Persönlichkeit, ein Zeichen und einen Stil hinzuzufügen.** Sie können die Benutzererfahrung einprägender gestalten, indem Sie Ihr einen natürlichen Eindruck vermitteln.

![Abbildung, die zeigt, wie sich der Mauszeiger auf die ](images/vis-animations-image6.png)

Mit Windows 7 werden die Task leisten Schaltflächen auf der Grundlage der aktuellen Mausposition und der Programmsymbol Farbe hervorgehoben. Diese Vorgehensweise ist visuell ansprechend, aber sehr fein und vermittelt eine bescheidene Persönlichkeit.

**Animationen und Übergänge sind jedoch am effektivsten und willkommen, wenn Sie einen klaren Zweck erfüllen.** Sie sollten verwendet werden, um Benutzerfreundlichkeit, Glätte und Fluss und die Wahrnehmung der Qualität zu verbessern, ohne dass die Leistung erheblich beeinträchtigt wird.

Obwohl einige Arten von Animationen verwendet werden, um die Aufmerksamkeit des Benutzers zu zeichnen, sollten Sie sicherstellen, dass die Aufmerksamkeit durchaus verdient ist und die Schulung des Benutzers unterbricht. Das menschliche Auge ist sensibel an Bewegung, vor allem bei der Peripherie Bewegung. Es ist für die Benutzer schwierig, sich zu konzentrieren, wenn eine blinkende Task leisten Schaltfläche oder ein Symbol für den drehenden Benachrichtigungsbereich vorliegt. **Vermeiden Sie die Verwendung von Animationen, um Benutzer zu unterbrechen oder abzubrechen oder um Punkte zu zeichnen, die die Aufmerksamkeit des Benutzers nicht rechtfertigen.**

**Falsch:**

![Abbildung der Task leisten Schaltfläche aus keinem Grund hervorgehoben ](images/vis-animations-image7.png)

Programme sollten ihre Task leisten Schaltfläche nicht blinken, es sei denn, Benutzer müssen sofort etwas wichtiges ausführen. In diesem Fall muss das Programm nur vom Benutzer aktiviert werden.

**Verwenden Sie Animationen und Übergänge, da Sie von Ihrem Programm benötigt werden, nicht nur, weil Sie dies tun können.** Und für Barrierefreiheit sollten Sie keine Animation als einzige Möglichkeit zum vermitteln wichtiger Informationen verwenden. Stellen Sie sicher, dass Benutzer äquivalente Informationen auf andere Weise abrufen können.

### <a name="attributes-of-good-animations-and-transitions"></a>Attribute von guten Animationen und Übergängen

Gute Animationen und Übergänge treffen das richtige Gleichgewicht zwischen diesen Attributen:

-   **Sind klar zielstrebig.** Gute Animationen sind vorhanden, da Sie sein müssen, ob Sie Informationen übermitteln, eine Interaktion in Echtzeit durchführen oder auf etwas beachtenswertes aufmerksam machen müssen. Und zielgerichtete Animationen sind genau. Wenn eine Animation anzeigt, dass eine Aufgabe durchgeführt wird, liegt dies daran, dass die Aufgabe tatsächlich ausgeführt wird.

**Falsch:**

![Screenshot des Akku Symbols und der Bezeichnung "vollständig abgerechnet" ](images/vis-animations-image8.png)

In diesem Beispiel zeigt die Animation, dass ein vollständig geladener Akku in Rechnung gestellt wird.

-   **Das Aussehen ist reibungslos und kontinuierlich.** Gute Animationen entfernen problemlos die Kontexte zwischen Szenen-oder Element Zustandsänderungen, indem Beziehungen angezeigt werden und ein Sinn von Ort und Kontext bereitgestellt wird. Die Kontinuität hilft Benutzern zu verstehen, wo Sie sich befinden, und wie Sie zu dem Ort zurückkehren, von dem Sie stammen.

![Screenshot der drei Vorschau Versionen des Task leisten Fensters ](images/vis-animations-image9.png)

Das Fenster der Windows 7-Taskleiste wird für die Kontinuität angezeigt, wenn der Benutzer von einem Programm zu einem anderen wechselt.

-   **Sind realistisch.** Gute Animationen simulieren die realen physischen Eigenschaften und das Verhalten eines Objekts. Dadurch können Benutzer die Ergebnisse Ihrer Interaktionen Vorhersagen und verstehen. Sie müssen die reale Welt nicht genau modellieren, aber wenn Sie realistische Animationen verwenden, müssen Sie Sie mit der realen Welt konsistent halten. Benutzer sollten nie durch die Ergebnisse überrascht oder verwirrt werden, insbesondere bei Animationen, die für die direkte Bearbeitung verwendet werden.

![Abbildung der auf die neue Position gezogenen Task leisten Schaltfläche ](images/vis-animations-image10.png)

In diesem Beispiel ist die Animation, die von der Windows 7-Taskleiste verwendet wird, realistischer als eine statische Einfügemarke.

-   **Sind authentisch.** Auch Objekte, die nicht in der realen Welt gefunden werden, können naturgemäß aussehen, indem Sie auf dem realen Verhalten eines anderen, aber verknüpften Objekts basieren. Diese Metapher funktioniert nur, wenn die Beziehung den beabsichtigten Zweck und das Verhalten eindeutig kommuniziert.

![Screenshot der ausgelassenen Auswirkung hinter verschobenem Fenster ](images/vis-animations-image11.png)

In diesem Beispiel ist die von Windows 7 verwendete Animation "Quetschen" authentisch, da Sie mit der Art und Weise, wie sich Glasfenster in der realen Welt Verhalten, konsistent ist.

-   **Verwenden Sie die natürliche Zuordnung.** Natürliche Zuordnungen sind entweder physisch oder Kultur. Eine kulturbasierte natürliche Zuordnung könnte z. b. von der Tatsache ausgehen, dass in westlichen Kulturen Personen von links nach rechts gelesen werden. Folglich ist zum Ausdrücken einer Zeitsequenz von Objekten das mittlere Objekt aktuell, die Objekte auf der linken Seite und die Objekte auf der rechten Seite in der Zukunft. Der Fortschritt wird durch die Bewegung von links nach rechts angezeigt.

![Screenshot der Statusanzeige von Media Player ](images/vis-animations-image12.png)

In diesem Beispiel verfügt das Windows Media Player-Steuerelement über eine natürliche Zuordnung, da die Position von links nach rechts verschoben wird.

-   **Haben Sie eine Persönlichkeit.** Gut ausgewählte Animationen sind hervorragend geeignet, um Ihrem Programm eine Persönlichkeit, ein Zeichen und einen Stil hinzuzufügen. Sie können den Benutzer schneller und ansprechender gestalten. Während der Typ der Animation bestimmt, was er kommuniziert, zeigt die jeweilige Art und Weise, in der die Animation durchgeführt wird, die Persönlichkeit des Programms an. Gute Animationen projizieren die richtige Persönlichkeit für Ihr Programm, egal ob Ernst oder positiv oder irgendwo dazwischen.

![Screenshot der kreativ entworfenen Zune-Schnittstelle ](images/vis-animations-image13.png)

In diesem Beispiel unterstützt die Zune die Verwendung von animiertem Text und dynamischer Perspektive dabei, seine eigene Persönlichkeit zu gestalten.

-   **Aussehen und reaktionsfähig.** Gute Animationen beeinträchtigen die Produktivität des Benutzers nicht, indem Benutzer gegen andere Interaktionen blockiert werden oder Benutzer gezwungen werden, Sie zu überwachen. Unabhängig davon, wie natürlich und mit der Animation der Animationen des Programms zu tun sind, möchte niemand auf diese exklusiv warten. Gute Animationen sind auch reaktionsfähig, ohne dass eine jarringschleife durchlaufen wird. Reaktionsfähige Animationen profitieren auch von der schnellen Kommunikation Ihres zwecks. Benutzer sollten eine Animation nicht lange Zeit ansehen, um herauszufinden, was Sie tut oder wann Sie abgeschlossen ist. Für die direkte Bearbeitung sind reaktionsschnelle Animationen von wesentlicher Bedeutung, um eine direkte und ansprechende reale Darstellung zu gewährleisten. Um sich direkt zu fühlen, müssen die Kontaktpunkte eines Objekts während der Bearbeitung reibungslos unter dem Zeiger bleiben. Jede Verzögerung, eine verpacsantwort oder der Verlust von Kontakten zerstört die Wahrnehmung direkter Manipulationen.

![Abbildung von Finger berühren eines Touchscreens ](images/vis-animations-image14.png)

In diesem Beispiel ist der Touch-Panel-Übergang reaktionsfähig, indem der Kontaktpunkt während der Bearbeitung unter dem Finger des Benutzers gehalten wird.

-   **Ziehen Sie das richtige Maß an Aufmerksamkeit.** Gute Animationen sind normalerweise sehr gering und Zeichnen nur die Aufmerksamkeit aus, die zur Erfüllung ihres Zwecks erforderlich ist. Daher sind Sie nicht ablenkend, lästig, übermäßig Komplex, übermäßig lang oder wiederholt. Sie werden nach dem wiederholten Viewings nicht mehr Überdruss.

![Screenshot der Ausblenden von Hervorhebungen für Dateinamen ](images/vis-animations-image15.png)

In diesem Beispiel zeichnet Windows Search temporär auf übereinstimmende Suchbegriffe und dann auf.

-   **Sehen Sie sich nur besondere Informationen an, wenn wirklich besonders** Die Häufigkeit erhöht die Notwendigkeit von Feinheiten, sodass häufige Interaktionen einfache Animationen erfordern, die eine einfache Idee auf einfache Weise vermitteln. Reservieren Sie besondere, komplexe Animationen für besondere, seltene Umgebungen.

![Screenshot von vier Kreisen mit Windows-Logo ](images/vis-animations-image16.png)

In diesem Beispiel verwendet Windows eine Animations Animation beim Start, um die Erfahrung besonders zu gestalten, aber eine solche Animation wäre an anderer Stelle ungeeignet.

Sie werden feststellen, dass Sie das richtige Gleichgewicht erreicht haben, wenn die Gesamtleistung beeinträchtigt wäre, wenn eines dieser Attribute entfernt wurde.

### <a name="creating-an-animation-vocabulary"></a>Erstellen eines Animations Vokabulars

Gute Animationen sind eine effektive visuelle Kommunikation, und die Konsistenz ist für ihre Effektivität von entscheidender Bedeutung. Wenn Sie einen bestimmten Übergang verwenden, z. b. das Verschieben einer Szene von rechts nach rechts, um zur nächsten Szene zu gelangen, sollte dies der einzige Übergang sein, der für diesen Zweck verwendet wird, und dieser Übergang sollte nicht für andere Zwecke verwendet werden. Das Zuweisen einer anderen Bedeutung zur gleichen Animation schadet der Möglichkeit der Kommunikation. Wenn Sie bestimmte Animationen und Übergänge zu einer bestimmten Bedeutung zuweisen, erstellen Sie ein Animations Vokabular.

Dieses Problem gilt für Animationen und Übergänge, die eine Bedeutung haben, nicht für generische, denen Benutzer wahrscheinlich keine Bedeutung zuweisen, oder für solche, deren Zweck nicht erkennbar ist. Animationen wie z. b. "Fades" und besondere Effekte, wie z. b

Ein gutes Vokabular weist Animationen zu, die das tatsächliche physische Verhalten eines Objekts modellieren. Wenn Sie einem Objekt oder einer Aktion eine Animation zuweisen müssen, die nicht über ein echtes Gegenstück verfügt, wählen Sie eine Animation aus, die zeigt, wie sich das Objekt in der Praxis verhält.

![Screenshot der Art und Weise, wie Hover auf das Windows-Logo leuchtet ](images/vis-animations-image17.png)

Obwohl das Startmenü kein reales Objekt ist, sieht der Hover-Effekt wie ein reales Objekt aus, wenn es aktiviert ist.

Jede Animation in einem Vokabular muss eindeutig verschieden sein. Die Animationen sollten ein ähnliches Verhalten aufweisen, wenn die zugehörigen Aktionen auf ähnliche Weise verknüpft sind. Beispielsweise wird durch Verschiebungs Übergänge die Navigation empfohlen, sodass Sie Verschiebungs Übergänge aus unterschiedlichen Richtungen verwenden können, um unterschiedliche Navigations Typen anzugeben.

Sie wissen, dass Ihre Animationen und Übergänge nicht gut kommunizieren, wenn die Benutzer die Ergebnisse verwirrend, überraschend oder unerwartet finden. Im Allgemeinen ist es besser, einen einzigen Zweck als mehrere Zwecke zu erreichen, nicht so gut.

Im Idealfall sollte Ihr Animations Vokabular in allen Bereichen Ihres Programms umfassend sein, die diese benötigen. Wenn nur einige wenige Interaktionen natürliche Animationen aufweisen, werden Sie darauf aufmerksam gemacht.

Weitere Informationen zum Windows-Animations Vokabular finden Sie in diesem Artikel im Abschnitt [Verwendungs Muster](#usage-patterns) .

### <a name="designing-the-right-personality"></a>Entwerfen der richtigen Persönlichkeit

Während der Typ der Animation bestimmt, was er kommuniziert, wird die jeweilige Art und Weise, in der die Animation ausgeführt wird, mit der Programm Persönlichkeit gesprochen und seine Marke verstärkt.

Die Persönlichkeit Ihres Programms sollte die Art ihrer Aufgaben und die Persönlichkeit ihrer Benutzer widerspiegeln, sodass es keine willkürliche Auswahl ist. Vielmehr sollte sich eine gut entworfene Persönlichkeit als authentisch fühlen. versuchen Sie es niemals zu erzwingen. Die Persönlichkeit sollte eine emotionale Verbindung mit dem Benutzer herstellen. Zu berücksichtigende Faktoren:

-   **Aufgaben:** Ernst oder Spaß; optional oder erforderlich.
-   **Folgen:** Ernsthaft oder neben Version.
-   **Kosten:** Kostenlos oder gekauft; Wenn gekauft, moderat Preis oder aufwendig.
-   **Benutzer Fokus:** Relativ schmale Gruppe von Ziel Benutzern oder Breite, allgemeine Zielgruppe.
-   **Benutzerumgebung:** Professionell, lässig oder privat.
-   **Benutzer Alter:** Jünger oder älter.
-   **Verwendungs Häufigkeit:** Häufig oder selten.

Die Kombination dieser Faktoren hilft dabei, eine passende Persönlichkeit für Ihr Programm zu ermitteln. Im folgenden finden Sie einige geeignete Kombinationen für gängige Programmtypen:

**Produktivitätsanwendungen**

Natürlich müssen Produktivitätsanwendungen auf die Produktivität konzentrieren. Während einige besondere Erfahrungen auftreten können, sollten die meisten anderen Animationen über diese Merkmale verfügen:

-   Klein
-   Natürlich, realistisch
-   Geringfügige, verhaltene
-   Schnell, effizient
-   Gelockert

**Hilfsprogramme**

Hilfsprogramme werden in der Regel kurz verwendet, sodass die Verwendung der Animation aggressiver sein kann:

-   Realistisch, anschaulich, selbsterklärend
-   Safe
-   Einbezieht

**Unterhaltung, Spiele**

Da das Ziel dieser Programme darin besteht, Benutzer zu engagieren und zu begeistern, können die Animationen und Übergänge durch die folgenden Merkmale weitaus aggressiver sein:

-   Groß (möglicherweise zu einem integralen Bestandteil der Darstellung)
-   Künstlich, surreal
-   Impacerend, lebhaft
-   Emotional, spielerisch, positiv
-   Energetische

Eine emotionale Verbindung ist so wichtig für Unterhaltungsprogramme, dass es akzeptabel ist, einige Regeln zu vereinigen, wenn dies dazu beiträgt, dass Benutzer mit dem Programm zufrieden sind. Beispielsweise ist es akzeptabel, wenn eine Animation oder ein Übergang nach der Hundertstel Zeit zu einem Überdruss wird, wenn die meisten Benutzer wahrscheinlich nicht das Programm verwenden, das häufig verwendet wird.

Im Allgemeinen sind Animationen und Übergänge, die klein, natürlich, gedämpft, effizient und dennoch gelockert sind, die sicherste Lösung. Übergänge mit diesen Merkmalen nehmen in der Regel den kürzesten Weg von Anfang bis Ende, schnelles starten, Ende, und lassen sich nicht überschreiben. Außerdem sind gut gestaltete Übergänge so konzipiert, dass Sie für alle Bereiche, in denen Sie verwendet werden, gut funktionieren.

### <a name="animation-performance"></a>Animations Leistung

Stellen Sie beim Entwerfen von Animationen sicher, dass die Benutzer die Möglichkeit haben, Ihr Programm effizient zu verwenden. Im allgemeinen machen Sie Ihre Animationen langsam genug, um ihren Zweck zu erfüllen, aber so schnell, dass Sie sich nicht mit der Reaktionsfähigkeit stören, eine zu hohe Aufmerksamkeit erfordern oder mehr zu tun haben.

**Falsch:**

![Abbildung der Seiten Umwandlung von rechts nach links ](images/vis-animations-image18.png)

Diese Seiten Turn-Animation bietet zwar ein Gefühl für die Benutzerproduktivität, verringert jedoch die Produktivität der Benutzer, indem es länger dauert, Seiten zu drehen.

Kurze Übergänge (200 Millisekunden oder weniger) sind ein Sonderfall (vor allem, wenn Sie häufig von einer Verzögerung aus arbeiten), da Benutzer sich darüber im klaren sein müssen, dass Sie eine geteilte Sekunde darauf warten müssen. Benutzer sind bereit, auf solche Animationen zu warten, wenn Folgendes:

-   Die wahrgenommene Wartezeit ist sehr kurz (200 Millisekunden oder weniger).
-   Der Übergang sorgt für eine reibungslose und natürliche Interaktion.
-   Der Übergang sorgt für eine reaktionsfähigere Interaktion.
-   Jede Verzögerung sorgt dafür, dass der Benutzer die Kontrolle über die Interaktion behält.

![Abbildung der Task leisten Schaltflächen, die an neue Position gezogen werden ](images/vis-animations-image19.png)

Benutzer akzeptieren eine kurze Verzögerung für die Animation der Task leisten Schaltfläche Neuanordnung, da Sie sehr kurz ist, und die Interaktion wird dadurch natürlicher.

Es gibt drei Möglichkeiten, wie sich Animationen nachteilig auf die Leistung auswirken können: Geschwindigkeit, Reaktionsfähigkeit und Wahrnehmung.

Aus Gründen der Geschwindigkeit sind einige Animationen visuelle und sehr CPU-intensive Aufgaben, daher sollten Sie diese Aufgaben mit CPU-intensiven Animationen langsamer machen. Bei den meisten CPU-intensiven Animationen ("Heavy"-Animationen) werden tendenziell folgende Aktionen durchführen:

-   Viele Elemente, die unabhängig voneinander verschoben werden.
-   Wiedergabe für eine lange Dauer oder Entfernung.
-   Sie sollten eine große Menge an Bildschirm Leerraum einschließen.
-   Sind mathematisch intensiv.

Animationen mit geringerer Auswirkung auf die Leistung:

-   Binden Sie ein einzelnes-Objekt ein.
-   Wiedergabe für eine kurze Dauer oder Entfernung.
-   Sie sollten nur einen kleinen Teil des Bildschirm Raums einschließen.
-   Sind nicht mathematisch intensiv.

Um eine gute Leistung zu gewährleisten, sollten große Animationen nur für Aufgaben verwendet werden, die nicht CPU-intensiv sind, während helle Animationen überall verwendet werden können.

Bei der Reaktionsfähigkeit sollten die meisten Animationen und Übergänge so entworfen werden, dass Benutzer während der Ausführung der Animation interagieren können. Wenn eine Animation nicht Teil eines Prozesses ist, machen Sie diese unabhängig von der primären Interaktion des Benutzers, und erlauben Sie Benutzern, Sie zu unterbrechen.

Eine Animation wirkt sich möglicherweise nicht negativ auf die Leistung einer Aufgabe aus, aber Benutzer haben möglicherweise die Wahrnehmung. Verwenden Sie z. b. keine Animation, die für eine langsame, CPU-intensive Aufgabe auch dann sehr schwer erscheint, wenn die Leistung nicht beeinträchtigt wird, da Benutzer möglicherweise den Grund für eine langsame Aufgabe haben. **Wenn etwas langsam aussieht, ist es langsam, daher ist es besser, Animationen zu verwenden, die einfach, einfach und schnell sind.** Die Verwendung von Animationen mit einem Snappy-Anfang für CPU-intensive Aufgaben hilft.

**Diger**

![Screenshot des Dialog Felds "Kopieren" mit Statusanzeige ](images/vis-animations-image20.png)

Während die Animation im Windows-Dialogfeld zum Kopieren von Dateien die Datei Kopier Leistung nicht beeinträchtigt, besteht das Risiko, dass die Benutzer davon ausgehen, dass Sie dies tun.

**Auch riskant:**

![Screenshot des Fortschritts, der in der Adressleiste angezeigt wird ](images/vis-animations-image21.png)

In diesem Beispiel werden einige Aufgaben durch die Animation für langsam aussehende Fortschritte in der Adressleiste von Windows-Explorer sehr langsam aussehen.

Animationen und Übergänge haben keinen Wert, wenn ihre Qualität so schlecht ist, dass Sie die Leistung weniger reibungslos und weniger ansprechend gestalten. Um die Qualität beizubehalten, sollten Animationen so konzipiert werden, dass Sie immer dann ordnungsgemäß herabgestuft werden, wenn ausreichend Systemressourcen nicht verfügbar sind. Animationen können durch Abweichungen, die weniger Ressourcen erfordern (z. b. kürzere Längen oder niedrigere Frameraten) oder gar nicht ausgeführt werden, herabgestuft werden. Unabhängig von den verfügbaren Ressourcen müssen Sie sicherstellen, dass die Animationen hochwertig sind und anstelle von Softwarefehlern Animationen wie Animationen aussehen.

Wenn die Benutzer der Meinung sind, dass die Animationen und Übergänge Ihres Programms von ihrer Produktivität ausgehen, besteht die Möglichkeit, dass einige Benutzer Sie deaktivieren möchten. Um diese Möglichkeit zu unterstützen, achten Sie darauf, dass Sie **alle unnötigen Animationen** aus dem Windows Easy Access Center deaktivieren.

### <a name="attracting-the-right-level-of-attention"></a>Ziehen der richtigen Aufmerksamkeit

Obwohl nur einige Arten von Animationen und Übergängen speziell für die Aufmerksamkeit des Benutzers entworfen wurden, sollten Sie so entworfen werden, dass Sie die richtige Aufmerksamkeit erreichen, um ihren Zweck zu erfüllen. Was sind die verschiedenen Möglichkeiten, um Aufmerksamkeit zu erhalten, und wie können Sie die richtige Auswahl treffen?

**Animationseffekte**

Unterschiedliche Animationseffekte sind mit unterschiedlichen Ebenen identisch. In der folgenden Liste werden die gängigsten Methoden zusammengefasst, beginnend mit der höchsten Aufmerksamkeit:

-   **Schnelles Blinken.** Erfordert sofortige Aufmerksamkeit. Kann die Benutzer Konzentration unabhängig davon unterbrechen, wo das Blinken auftritt.
-   **Mittelmäßiges blinken.** Identisch, erfordert jedoch weniger Aufmerksamkeit mit niedrigerer Häufigkeit.
-   **Sprung.** Bemerkbar in peripheren Visionen und relativ anspruchsvoller Natur. Benutzer werden wahrscheinlich bemerken, können sich jedoch weiterhin an einer anderen Stelle konzentrieren, wenn die Dauer kurz ist.
-   **Entschließungs.** Bemerkbar in peripheren Visionen, aber nicht anspruchsvoll. Komplexe oder 3D-Bewegungen ziehen jedoch mehr Aufmerksamkeit als einfache oder 2D-Bewegungen. Benutzer werden wahrscheinlich bemerken, aber Sie können sich weiter an anderer Stelle konzentrieren.
-   **Mittelmäßiges Pulsing.** Bemerkbar, aber keine ablenkend in der Peripherie Vision. Benutzer können sich weiter an anderer Stelle konzentrieren. Kann Helligkeit, Farben und Größen von Impulsen haben.
-   **Langsames Pulsing/glühen.** Merkliche, aber feine. Zieht mehr Aufmerksamkeit als ein statischer Effekt. Benutzer bemerken die Animation jedoch möglicherweise nicht, es sei denn, Sie sind bereits vorhanden.
-   **Abzuwehren.** Noch weniger bemerkbar. Zieht mehr Aufmerksamkeit als ein statischer Effekt. Benutzer bemerken die Animation jedoch möglicherweise nicht, es sei denn, Sie sind bereits vorhanden.
-   **Statische Hervorhebung/Gleam.** Bemerkbar, wenn Benutzer sich für die Suche entscheiden, aber keine Aufmerksamkeit erfordern, wenn Sie sich an anderer Stelle befindet.
-   **Ambient/Natural.** Absichtlich nicht bemerkbar, wenn eine natürliche Darstellung in der Praxis auftritt.

Um den richtigen Ansatz für Ihr Programm oder Feature zu ermitteln, berücksichtigen Sie, wie sich diese Faktoren auf die Szenarios ihrer Features beziehen.

Nehmen Sie beispielsweise an, Sie entwerfen ein Sofortnachrichten Programm, und jemand hat dem Benutzer soeben eine Nachricht gesendet. Dieses Szenario erfordert die Aufmerksamkeit des Benutzers, es sollte sich an jedem Ort bemerkbar machen, und der Benutzer möchte in der Regel schnell Antworten. Dieses Szenario deutet darauf hin, dass eine moderate blinkende Animation eine gute Wahl wäre. Angenommen, Sie möchten Benutzer darüber informieren, dass ein Druckauftrag abgeschlossen wurde. Benutzer sollten in der Lage sein, sich weiter an anderer Stelle zu konzentrieren und produktiv zu arbeiten. Dies ist akzeptabel, wenn die Benutzer nicht bemerken. Dieses Szenario deutet darauf hin, dass das mittellange bis langsame pulsierender oder glühen eine gute Wahl wäre.

**Dauer**

Die geeignete Dauer für die Animation der Animation hängt von dem Szenario und der Art der verwendeten Animation ab. Wenn Sie einen Animationseffekt mehr beachten, ist die Dauer kürzer. Obwohl sehr feine Effekte, die eine geringe Aufmerksamkeit erfordern (z. b. langsame Pulsing), unbegrenzt wiedergegeben werden können, sollten die Auswirkungen auf die Aufmerksamkeit nur zwischen 1 und 3 Sekunden wiedergegeben werden. Das Risiko, dass die Animation überwältigend und ärgerlich ist, ist länger.

![Screenshot der markierten Task leisten Schaltfläche ](images/vis-animations-image22.png)

In Windows 7 wird die Taskleiste nur für eine Sekunde auf Aufmerksamkeit blinken. Dies wäre eine lästige Weile.

**Effekt Verfall**

Sie sollten Aufmerksamkeit entwerfen, indem Sie Animationen auf der Grundlage der Annahme machen, dass Benutzer nicht sofort reagieren, weil Sie mit einer anderen Aktion beschäftigt sind und nicht unterbrochen werden möchten. Daher sollte Ihr Ziel sein, die Aufmerksamkeit zu erregen, ohne Sie zu fordern.

Um das richtige Gleichgewicht der Aufmerksamkeit zu erhalten, ohne Sie zu fordern, können Sie die Intensität eines Effekts im Laufe der Zeit übernehmen. Wenn Sie z. b. auf Aufmerksamkeit aufmerksam machen möchten, können Sie den Effekt anfänglich stärken, aber die Auswirkungen dann schnell verlangsamen. Auf diese Weise wird die attraktive Leistung größtenteils durch die anfängliche Wirkung bestimmt, aber der Gesamteindruck des Benutzers wird hauptsächlich durch seine Fertigstellung bestimmt.

![Screenshot der reduzierten Flash Rate ](images/vis-animations-image23.png)

In Windows 7 verlangsamt sich der Task leisten-Flash Effekt am Ende.

### <a name="what-about-powerpoint"></a>Was ist mit PowerPoint?

Microsoft PowerPoint-Übergänge verstoßen häufig absichtlich gegen diese Richtlinien, da Sie so konzipiert sind, dass Sie sich auf Folien Übergänge beziehen und erfordern, dass Benutzer darauf warten. Außerdem haben Sie keine bestimmte Bedeutung, sodass Sie nichts über die Tatsache informieren, dass sich eine Folie ändert.

Übergängen im PowerPoint-Stil, wenn diese ordnungsgemäß verwendet werden, haben folgende Zwecke:

-   Sie unterbrechen lange Präsentationen in kleinere Blöcke, indem der Presenter gezwungen wird, anzuhalten.
-   Sie zeichnen die Aufmerksamkeit der Zielgruppe in Bezug auf Änderungen in der Präsentation und unterstützen Menschen dabei, sich auf Ihre Meinung zu konzentrieren.
-   Sie vermitteln der Präsentation einen Rhythmus, sodass Sie nicht monoton oder überwältigend ist.
-   Ihr Stil reflektiert die Persönlichkeit des Präsentators oder des Materials.

Obwohl es sich hierbei um wichtige Ziele für eine Präsentation handelt, würden solche Übergänge in der Benutzeroberfläche der meisten Programmtypen unnötig beachtet werden.

**Untere Zeile:** Verwenden Sie keine Übergängen im PowerPoint-Stil als Modell für Ihr Programm.

**Wenn Sie nur sechs Dinge tun...**

1.  Verwenden Sie Animationen und Übergänge, damit das Programm leichter zu verstehen ist, und fühlen Sie sich leichter und ansprechender. Sie sollten eine klare Aufgabe haben. Verwenden Sie Animationen nicht nur, weil Sie dies tun können, oder um unnötige Aufmerksamkeit auf Ihr Programm zu ziehen.
2.  Definieren Sie ein Animations Vokabular, und verwenden Sie es im gesamten Programm einheitlich. Verwenden Sie bei Bedarf das Animations Vokabular von Windows 7.
3.  Verwenden Sie die Merkmale ihrer Animationen, um Ihre Programm Persönlichkeit zu gestalten und Ihre Marke zu verstärken.
4.  Machen Sie die meisten Animationen einfach, kurz und fein. Beachten Sie, dass Animationen keine Aufmerksamkeit benötigen, um erfolgreich zu sein. Wenn eine Animation geeignet und natürlich ist, bemerken Benutzer nur ihre Abwesenheit.
5.  Sorgen Sie dafür, dass Ihre Animationen schnell und reaktionsfähig sind und Ihnen ein schlankes Gefühl vermitteln. Unabhängig davon, wie Sie Ihre Animationen einbinden, sollte niemand so aussehen, als würden Sie darauf warten. Entwerfen Sie schwerere Animationen für eine ordnungsgemäße Beeinträchtigung.
6.  Entwurf für die lange Ausführung. Wenn eine Animation lästig, ablenkend oder tiresome ist, entwerfen Sie Sie neu, oder entfernen Sie Sie.

## <a name="usage-patterns"></a>Verwendungsmuster

Animationen verfügen über mehrere Verwendungs Muster:



|                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Feedback zu Hover**<br/> , um anzuzeigen, wo der Interaktionspunkt ist. <br/>                                | Gibt an, dass der Interaktionspunkt aktiv ist. Hover kann auch durch einen statischen Effekt angezeigt werden.<br/> Windows-Vokabular: zeigen Sie mit dem Mauszeiger auf den Mauszeiger (Begrenzungs Rechteck, Hervorhebung, Vergrößerung) mit einem einblenden/ausblenden-Effekt für Glätte. <br/> ![Screenshot von einem der sechs markierten Albumcover ](images/vis-animations-image24.png)<br/> Beim Zune Digital Media Player werden Wiedergabe Steuerelemente durch das Album hervorgehoben und hinzugefügt.<br/>                                                                                                                                                                                                                 |
| **Auf Feedback klicken**<br/> , um anzuzeigen, dass ein durch Klicken Aktivier bares Objekt reagiert und einen Klick erhalten hat. <br/>    | Gibt an, dass auf ein Objekt geklickt wurde.<br/> Windows-Vokabular: Hintergrund des Flash Objekts bei Click-Down-Ereignis. um den Berührungs Kontakt anzuzeigen, verwenden Sie einen Ripple-Effekt. <br/> ![Foto des Fingers auf dem Touchbildschirm mit rippeln ](images/vis-animations-image25.png)<br/> "Berühren" zeigt eine Ripple-Animation an, damit der Benutzer weiß, dass die Interaktion erkannt wurde.<br/>                                                                                                                                                                                                                                                                                                         |
| **Auswahl Feedback**<br/> , um anzuzeigen, dass ein Objekt ausgewählt ist. <br/>                                | Gibt an, dass ein Objekt ausgewählt ist. die Auswahl kann auch durch einen statischen Effekt angezeigt werden.<br/> Windows-Vokabular: Zeichnen Sie das Auswahl Rechteck mit einem einblenden/ausblenden-Effekt für Glätte. <br/> ![Abbildung eines ausgewähltem und dann ausgewählten Albumcover ](images/vis-animations-image26.png)<br/> In Zune gibt Album das Blinken bei Click aus und erhält dann ein Auswahl Rechteck bei der Auswahl.<br/>                                                                                                                                                                                                                                                                      |
| **Fortschritts Feedback**<br/> , um anzuzeigen, dass eine Aufgabe ausgeführt wird. <br/>                             | Fortschritts Feedback gibt an, dass eine Aufgabe Fortschritte macht, in der Regel mit Aktivitätsindikatoren, Status anzeigen oder Animationen, die die Aufgabe veranschaulichen. die bestimmte des Fortschritts Feedbacks zeigt ungefähr den Umfang der Aufgabe und den verbleibenden Verlauf, während der unbeendete Fortschritt nur angibt, dass die Aufgabe ausgeführt wird.<br/> Windows-Vokabulare: drehende Aktivitätsindikatoren, Status anzeigen, Fortschritts Hintergründe, Grafik Animationen. <br/> ![Screenshot des Dialog Felds mit dem Text "Signieren" ](images/vis-animations-image27.png)<br/> In diesem Beispiel zeigt Windows Live Messenger während der Anmeldung unbestimmtes Fortschritts Feedback an.<br/> |
| **Attractor**<br/> , um anzuzeigen, dass ein Eingreifen des Benutzers erforderlich ist. <br/>                          | Ziehen Sie die richtige Aufmerksamkeit, wenn wichtige Objekte erstellt werden oder eine Aufmerksamkeit erfordern (häufig aufgrund von Änderungen), oder wenn wichtige oder dringende Ereignisse eintreten. Weitere Informationen finden Sie [unter gewinnen der richtigen Aufmerksamkeit](#attracting-the-right-level-of-attention) für Entwurfs Techniken.<br/> Windows-Vokabular: blinken, verschieben, Pulsing, Leucht End, Glanz. <br/> ![Screenshot der Symbolleisten Animation ](images/vis-animations-image28.png)<br/> Die Windows Live-Symbolleiste wird bei der ersten Darstellung animiert, damit Sie offensichtlich ist, wo Sie sich befindet.<br/>                                                                                                                                 |
| **Relationship**<br/> , um die Beziehung zwischen Objekten oder Kausalität in Effekten anzuzeigen. <br/>        | Anzeigen von Beziehungen, insbesondere dann, wenn die Beziehung möglicherweise nicht verstanden oder erwartet wird, auf eine Weise, die nicht ablenkend oder verwirrend ist.<br/> Windows-Vokabular: morphung, Transport, physische Änderung, z. b. das kippen, Vergrößern von einer Punktquelle, verkleinern zu einem Punkt Ziel. <br/> ![Screenshot der Farbkalibrierung (Dialogfeld)](images/vis-animations-image29.png)<br/> In diesem Beispiel zeigt die Animation die Beziehung zwischen der Gamma-Einstellung und deren Auswirkung auf die Anzeige.<br/>                                                                                                                                                    |
| **Abbildung/Vorschau**<br/> zur visuellen Erläuterung eines Konzepts, einer Aufgabe oder der Auswirkung eines Befehls. <br/> | Eine Animation oder ein Video, in dem ein Konzept oder eine visuelle Darstellung erläutert wird, um eine Text Erklärung zu ergänzen oder zu ersetzen. auf diese Weise können Benutzer Aufgaben ausführen oder Befehle effizient und zuverlässig auswählen. <br/> ![Screenshot des Rechtschreibfehlers bei Stift Korrektur ](images/vis-animations-image30.png)<br/> In diesem Beispiel verwenden die Befehle "Show Me" des Tablet PC-Eingabe Bereichs Abbildungen, um zu veranschaulichen, wie Sie diese korrigieren, löschen, teilen und verknüpfen.<br/>                                                                                                                                                                                                        |



 

Übergänge haben mehrere Verwendungs Muster:



|                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Objekt vergrößern/verkleinern/anzeigen**<br/> , wenn die Größe oder der Zustand eines Objekts reibungslos geändert werden soll. <br/>                                                                                                         | Objektänderungen zwischen Zuständen, möglicherweise während des Verschiebens. durch den Übergang bleiben die Benutzer während der Änderungen orientiert.<br/> Windows-Vokabular: Morph, Größe ändern, Objekt Folien ein-oder ausgehend. <br/> ![Screenshot der drei Größen von Wetter Gadgets ](images/vis-animations-image31.png)<br/> In diesem Beispiel wird die Weather Gadget-Mini Anwendung aus dem präzisen Zustand entfernt, um das Dialogfeld Optionen anzuzeigen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Inhalt anzeigen/ausblenden/ändern**<br/> , um Inhalt reibungslos anzuzeigen, auszublenden oder zu ändern, üblicherweise für die Progressive Offenlegung. <br/>                                                                       | Fenster innere Umgestaltung zum Anzeigen von mehr, weniger oder anderem Inhalt. durch den Übergang bleiben die Benutzer während der Änderungen orientiert.<br/> Windows-Vokabular: der Bereich wird ein-oder ausgeblendet. Flyout-Fenster werden ein-und ausgeblendet. unterschiedliche Inhalte werden ausgeblendet oder durchläuft. <br/> ![Screenshot von drei Größen des Rechners ](images/vis-animations-image32.png)<br/> Der Windows-Rechner bietet einen reibungslosen Übergang zwischen Ansichtsmodi.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Anzeigen/Ausblenden von Steuerelementen oder Kosten**<br/> um das normale visuelle Erscheinungsbild zu vereinfachen oder auszublenden, um Steuerelemente oder Ihre Zuordnungs Elemente auf dem Mauszeiger anzuzeigen oder auszublenden. <br/>                | Anzeigen von Steuerelementen, wenn Benutzer mit dem Mauszeiger auf einen Befehlsbereich zeigen, oder Anzeigen von Kosten, wenn Benutzer auf ein Steuerelement zeigen. der Mauszeiger über diese Bereiche zeigt an, dass der Benutzer interagieren soll. die Kosten können ausgeblendet werden, wenn der Zeiger stationär wird. <br/> ![Screenshot der Ausblenden von Steuerelementen vor dem Mauszeiger ](images/vis-animations-image33.png)<br/> In diesem Beispiel werden die Windows-Media Player Steuerelemente im Vollbildmodus auf dem Mauszeiger ausgeblendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Szenen Übergänge**<br/> , um eine Szene nahtlos und nahtlos zu gestalten, um die Aufmerksamkeit zu vermeiden. <br/>                                                                                   | Abrupte Szenen Änderungen können jarringvorgänge sein, insbesondere bei großen Bildschirm Bereichen. verwenden Sie daher Szenen Übergänge, um Glätte und Kontinuität zu schaffen und Kontext bereitzustellen. Szenen Übergänge werden als natürlicher und niedriger Schlüssel entworfen, um zu vermeiden, dass auf den Prozess des Übergangs selbst geachtet wird.<br/> Windows-Vokabular: einblenden in/aus; Kreuz ausblenden; gleitende in/Left, out/right, up, Down; Pushvorgänge und Cover-Vorgänge. <br/> ![Screenshot eines Fotos, das in eine andere ](images/vis-animations-image34.png)<br/> In diesem Beispiel wird das Hintergrundbild des Windows-Desktops sanft zwischen Bildern durchkreuzt, damit der Übergang reibungslos und gesteuert wird.<br/>                                                                                                                                                                                                                                                                                                                               |
| **Besondere Szenen Übergänge**<br/> um die Aufmerksamkeit auf eine Szenen Änderung aufmerksam zu machen und die Aufmerksamkeit des Benutzers zu erhöhen oder neu zu fokussieren. <br/>                                                               | Während die meisten Szenen Übergänge nicht auf den Übergangsprozess aufmerksam machen sollten, sind einige so konzipiert, dass Sie den Flow unterbrechen und Aufmerksamkeit ziehen, um zu betonen, dass etwas anderes passiert. um Aufmerksamkeit zu erregen, sind besondere Szenen Übergänge so konzipiert, dass Sie unnatürlich sind und eine hohe visuelle Auswirkung haben. <br/> ![Screenshot der Folie zum Verschieben des Zieh Grabens ](images/vis-animations-image35.png)<br/> In diesem Beispiel verwendet PowerPoint Aufmerksamkeit, um die Zielgruppe in die Änderung zu ziehen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Direkte Manipulationen**<br/> , um die Auswirkung von direkten Manipulationen (z. b. verschieben, Scrollen/schwenken, drehen und Zoomen) anzuzeigen. <br/>                                                                   | Der Übergang zeigt die Auswirkung der Bearbeitung in Echtzeit. der Effekt sollte glatt, kontinuierlich und konsistent mit der realen Welt sein. das Verschieben und drehen ist an manchen Stellen möglicherweise nicht fortlaufend, um Einschränkungen oder wahrscheinlich bevorzugte Optionen anzugeben. durch Zoomen wird der Inhalt größer oder kleiner, und möglicherweise wird der Detailgrad entsprechend geändert. <br/> ![Screenshot der drei Größen der Bildschirmlupe ](images/vis-animations-image36.png)<br/> In diesem Beispiel zoomt die Lupe zwischen den Ebenen reibungslos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Falsche direkte Manipulationen**<br/> , um anzugeben, dass eine direkte Manipulation (z. b. Move, Scroll/Pan) versucht wurde, jedoch nicht ausgeführt werden konnte. <br/>                                           | Der Übergang zeigt die zu Versuchs Ende Manipulation, kehrt jedoch wieder in den ursprünglichen Zustand zurück. häufig sieht der Effekt wie die Bearbeitung aufgrund einer realen physischen Einschränkung nicht durchgeführt werden. Diese Animationen werden anstelle von textbasierten Fehlermeldungen verwendet, wodurch die tatsächliche Darstellung der Bearbeitung beeinträchtigt würde.<br/> Windows-Vokabular: Sprung <br/> ![Abbildung der visuellen Darstellung der Animation ](images/vis-animations-image4.png)<br/> In diesem Beispiel springt das Dokument, um anzuzeigen, dass der Benutzer das Ende erreicht hat.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Sortieren, Filtern, Neuordnen von Übergängen**<br/> , um anzugeben, dass die Darstellung oder der Inhalt einer Auflistung von Elementen geändert wurde. <br/>                                                            | Der Übergang zeigt die Auswirkung der Änderung (oder bei komplexen Änderungen). <br/> ![Screenshot der Zeilen Kameras mit drei entfernten ](images/vis-animations-image37.png)<br/> ![ähnlicher Screenshot mit unterschiedlichen Kameras entfernt ](images/vis-animations-image38.png)<br/> ![ähnlicher Screenshot mit anderen Kameras entfernt ](images/vis-animations-image39.png)<br/> in diesem Beispiel verwendet die visuelle Suche in der Suche einen Filter Übergang.<br/> ![Screenshot von Album Abdeckung zum Ändern des Erscheinungs Bilds ](images/vis-animations-image40.png)<br/> In diesem Beispiel verwendet Windows Media Center einen Umstellungs Übergang als besondere Darstellung, während ein Song abgespielt wird.<br/>                                                                                                                                                                                                                                                                                   |
| **Leistungs Übergänge**<br/> damit eine Aktion schneller ausgeführt wird. <br/>                                                                                                              | Obwohl jeder Übergang das Potenzial hat, eine Aktion schneller durchzuführen, besteht der Hauptzweck dieser Übergänge darin, die Wahrnehmung von Leistung und Reaktionsfähigkeit zu verbessern. eine gute Vorgehensweise besteht darin, die ausgeführte Aufgabe in absichtlichen Schritten anzuzeigen. im Gegensatz dazu wird das Verzögern der Aktion, das Rendern der Ergebnisse in einer willkürlichen Weise oder die Verwendung eines Aktivitäts Indikators zu langsam.<br/> Windows-Vokabular: führen Sie eine Aktion in Phasen aus, bei der die Phasen reibungslos verlaufen. <br/> ![Screenshot der Sprung Liste zum Hinzufügen von Zielen ](images/vis-animations-image41.png)<br/> In diesem Beispiel zeigt eine Task leisten-Sprung Liste die Standardelemente sofort an und zeigt dann die Ziele an, sobald die Liste bereit ist. Dadurch wird die Zeit, die zum Erstellen der Liste erforderlich ist, verdeckt. Im Gegensatz dazu würde das Verzögern der anfänglichen Anzeige nicht reaktionsfähig sein, und das Anzeigen einer unvollständigen Liste oder eines Fortschritts Feedbacks würde viel langsamer erscheinen.<br/> |
| **Besondere Erfahrungen**<br/> zum einbinden und begeistern von Benutzern in seltenen Umgebungen [, die](glossary.md) für Ihr Programm wichtig sind und dem Benutzer die volle Aufmerksamkeit schenken. <br/>    | Obwohl jeder Übergang das Potenzial eines besonderen Erlebnisses hat, sind diese Übergänge am besten für seltene Erlebnisse reserviert, die für Ihr Programm wirklich besonders spezifisch sind. benutzerdefinierte Übergänge werden verwendet, um ein besonderes Gefühl zu vermitteln. Branding und Personality sind häufig wichtige Entwurfs Elemente. anders als bei anderen Mustern können besondere Benutzererfahrung Aufmerksamkeit erfordern, sehr hoch sein und erfordern, dass Benutzer einen Moment warten. Folglich werden diese Übergänge bei einer über Auslastung schnell durchgezogen, da die Ober Schreibung nicht mehr besonders besonders ist. <br/> ![Screenshot des Windows-Logos, das in den neuen Bildschirm wechselt ](images/vis-animations-image42.png)<br/> In diesem Beispiel zeigt Windows Media Center eine Animation beim Laden an, um Benutzer sofort einzubinden.<br/>                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Richtlinien

### <a name="effective-communication"></a>Effektive Kommunikation

-   **Definieren und verwenden Sie ein Animations Vokabular** , um sicherzustellen, dass Ihre Animationen und Übergänge eine konsistente Bedeutung haben, und verwenden Sie es im gesamten Programm einheitlich. Die meisten Vokabulare sollten Einträge für Darstellung und verschwinden von Szenen und Objekten, Navigation, grundlegende Interaktion (zeigen, auswählen, klicken), Objekt Bearbeitung und-Interaktion (verschieben, löschen, Ändern der Größe, scrollen, Schwenken, Zoomen, drehen, Filtern) und Aufmerksamkeit berücksichtigen. Eine konsistente Bedeutung ist für die effektive Kommunikation entscheidend.
-   **Verwenden Sie bei Bedarf das Windows-Animations Vokabular.** Obwohl das Programm möglicherweise unterschiedliche Zielgruppen und unterschiedliche Anforderungen hat, überwiegen die Vorteile von Konsistenz und Vertrautheit häufig die Vorteile der Unterschiede. Wenn das Vokabular des Programms unterschiedlich sein muss, verwenden Sie dieselben grundlegenden Animations Typen wie Windows, aber geben Sie Ihnen die richtige Persönlichkeit für Ihr Programm.
-   **Weisen Sie generischen Animationen und Übergängen in einem Animations Vokabular keine bestimmte Bedeutung zu.** Generische Übergänge wie z. b. "Fades" und besondere Effekte, wie z. b.-Aufstellungen, haben keine besondere Bedeutung (über einblenden oder ausblenden hinaus),

    **Falsch:**

    ![Screenshot eines Dialog Felds, das in einem anderen Dialogfeld ausgeblendet wird ](images/vis-animations-image43.png)

    In diesem Beispiel wird ein Kreuz ausblenden fälschlicherweise verwendet, um zum nächsten Element zu navigieren. Da Cross-Fades keine bestimmte Bedeutung haben, bietet dieser Übergang keinen Kontext.

-   **Machen Sie vokabulareinträge eindeutig verschieden.** Verwandte Aktionen können ähnliche Auswirkungen haben (z. b. wenn das Zoomen und Zoomen einen umgekehrten Übergang aufweisen), aber nicht verknüpfte Aktionen sollten deutliche unterschiedliche Effekte aufweisen (z. b. sollte das Zoomen nie mit Drehung verwechselt werden).
-   **Sorgen Sie für realistische und konsistente Effekte in der Praxis.** Wenn Sie realistische Animationen und Übergänge verwenden, halten Sie die Umgebung mit der realen Welt in Einklang. Benutzer sollten nie überrascht, verwirrt oder durch die Ergebnisse in die Irre führen. Und aus Gründen der Konsistenz sollten keine Metaphern kombiniert werden.
-   **Umkehren von umgekehrten Aktionen umgekehrte Animationen.** Dies entspricht den Erwartungen der Benutzer und vereinfacht das Vokabular. Wenn z. b. ein Bereich durch Verschieben in angezeigt wird, entfernen Sie ihn, indem Sie ihn nicht mit einem anderen Effekt auslagern.
-   **Machen Sie Animationen verständlich.** Benutzer sollten in der Lage sein, den Zweck einer Animation schnell nachzuvollziehen. Es ist möglich, eine Animation zu klein, zu kurz (weniger als 50 Millisekunden) zu machen, oder so geringfügig, dass Benutzer ihren Zweck nicht verstehen können. In solchen Fällen müssen Sie entweder umgestaltet werden, um die Bedeutung klar zu machen oder zu entfernen.

    **Falsch:**

    ![Screenshot der Animation beim Löschen (Dialogfeld) ](images/vis-animations-image44.png)

    In diesem Beispiel ist der Effekt so klein, dass nur wenige Benutzer ihren Zweck verstehen können. Bessere Umgestaltung oder Entfernung.

### <a name="patterns"></a>Muster

**Feedback zu Hover**

-   **Um reaktionsfähig zu sein, sollten Sie die Animation innerhalb von 50 Millisekunden nach dem eingeben oder belassen des Hover-Zustands abspielen.**
-   **Um schnell zu erscheinen, legen Sie die Dauer von Hover-Animationen auf weniger als 50 Millisekunden fest.**
-   **Verwenden Sie den Mauszeiger auf ein-/ausblenden.** Auf diese Weise unterscheiden sich die Hover-Effekte deutlich von Klick-und Auswahl Feedback.

**Auf Feedback klicken**

-   **Um reaktionsfähig zu sein, sollten Sie die Animation innerhalb von 50 Millisekunden von Click-Down-Ereignis abspielen.** Klicken Sie auf nach oben, um auf Ereignisse zu klicken.
-   **Um schnell zu erscheinen, legen Sie die Dauer von Klick Animationen auf weniger als 50 Millisekunden fest.**
-   **Verwenden Sie einen Hintergrund Blitz oder blinkffekt.** Wenn Sie dies tun, unterscheiden Sie sich deutlich von Mauszeiger-und Auswahl Feedback. Wenn Sie auf das Klicken auf den Mauszeiger klicken müssen, klicken Sie auf Feedback a Smooth Additions, um Feedback

**Auswahl Feedback**

-   **Um reaktionsfähig zu sein, sollten Sie die Animation innerhalb von 50 Millisekunden der Auswahl oder der Auswahl wiedergeben.**
-   **Um schnell zu erscheinen, legen Sie die Dauer von Auswahl Animationen auf weniger als 50 Millisekunden fest.**
-   **Verwenden Sie die Auswahl des Rechtecks "Ausblenden/ausblenden".** Dadurch wird die Auswahl deutlich von Hover und Click-Feedback unterschieden.

**Fortschritts Feedback**

-   **Verwenden Sie einen Aktivitätsindikator, wenn eine Aktion nicht innerhalb einer Sekunde ausgeführt werden kann.** Dadurch wird angegeben, dass der Befehl empfangen wurde.
-   **Verwenden Sie eine Statusanzeige, wenn eine Aufgabe mehr als fünf Sekunden in Anspruch nimmt.** Weitere Richtlinien finden Sie unter Status [leisten](progress-bars.md).
-   **Verwenden Sie Fortschritts Feedback Animationen, mit denen Benutzer die Auswirkungen von Aufgaben mit langer Ausführungszeit visualisieren können.** Vermeiden Sie unnötige Fortschritts Feedback Animationen, wenn eine Animation etwas Nützliches kommuniziert, verwenden Sie stattdessen eine Statusanzeige.
-   **Sie haben klar identifizierbare Vervollständigungs-und Fehlerzustände.** Benutzer müssen in der Lage sein, diese Endzustände schnell zu ermitteln.
-   **Hiermit wird der Fortschritt nicht mehr angezeigt, wenn die zugrunde liegende Aufgabe nicht fort** Benutzer müssen in der Lage sein, zu bestimmen, ob der Fortschritt nicht durchgeführt wird, und entsprechend zu reagieren.

**Attraktoren**

-   **Verwenden Sie Attraktoren mit Unterhaltung.** Wenn die Informationen nicht dringend, kritisch oder anderweitig das unmittelbare Verhalten des Benutzers beeinflussen, ist es in der Regel besser, den Zustand inauffällig zu ändern und Benutzern zu ermöglichen, die Änderung selbst zu ermitteln. [Lösen Sie Ablenkungen, nicht Auffindbarkeit](/windows/desktop/uxguide/how-to-design-desktop-ux).

    ![Screenshot der Symbole des drahtlos Status ](images/vis-animations-image45.png)

    In diesem Beispiel verwendet das Symbol für das Benachrichtigungsbereich des drahtlos Netzwerks eine Animation für kritische Probleme, aber Benutzer können selbst schwache Signale entdecken.

-   **Wählen Sie eine Animation aus, die die richtige Ebene der Aufmerksamkeit zeichnet.** Attractor-Animationen sollten genau genug darauf achten, um ihren Zweck zu erfüllen, aber noch nicht. Wenn der Benutzer sofort agieren muss, wählen Sie einen Effekt aus, der eine Aufmerksamkeit erfordert, unabhängig davon, wo der Benutzer sucht. Weitere Situationen finden Sie im Abschnitt "einbringen [der richtigen Aufmerksamkeit](#attracting-the-right-level-of-attention) ", um die richtige Kombination aus Aufmerksamkeit, Notiz barkeit und Dringlichkeit zu erhalten.

    **Falsch:**

    ![Screenshot des Taschen Clips im Büro-Assistenten ](images/vis-animations-image46.png)

    Die Microsoft Office-Assistenten haben unnötige Aufmerksamkeit auf sich selbst.

-   **Wenn der Benutzer nicht antwortet, wiederholen Sie die Animation nicht, oder verwenden Sie keine kontinuierlichen Animationen.** Gehen Sie stattdessen davon aus, dass der Benutzer keine Maßnahmen getroffen hat, sondern später agieren kann. Kontinuierliche Animationen erschweren es Benutzern, sich auf alles andere zu konzentrieren.

**Beziehungs Animationen**

-   **Verwenden Sie Beziehungs Animationen, um anzuzeigen, woher die Objekte stammen oder wo Sie sich befinden.**
-   **Beziehungs Animationen müssen mit dem ausgewählten Objekt beginnen oder enden.** Zeigen Sie keine Beziehungen zwischen Objekten an, mit denen der Benutzer derzeit nicht interagiert. Wenn Benutzer überhaupt bemerken, sehen Sie, was Sie bemerken werden.

**Abbildungen/Vorschau**

-   **Verwenden Sie Vorschauen, um die Auswirkung eines Befehls anzuzeigen, ohne dass Benutzer ihn zuerst ausführen müssen.** Durch die Verwendung hilfreicher Vorschau Versionen können Sie die Effizienz und das einfache erlernen Ihres Programms verbessern und die Notwendigkeit von Test-und Fehler Fehlern reduzieren.
-   **Verwenden Sie Abbildungen und Vorschau Versionen, die über eine klare Interpretation verfügen.** Wenn Sie verwirrend sind, haben Sie wenig Wert.
-   **Spielen Sie immer nur eine Abbildung gleichzeitig** , um zu vermeiden, dass Benutzer überwältigend werden. Wenn mehrere gleichzeitige Abbildungen möglich sind, verwenden Sie den Mauszeiger oder die Wiedergabe Schaltfläche, um Benutzern das Anzeigen Ihres Interesses zu ermöglichen.
-   **Eine Abbildung automatisch abspielen, wenn dies der Hauptzweck des Fensters oder der Seite ist.** Wenn die Option optional ist, können Benutzer Sie wiedergeben, wenn Sie bereit sind.
-   Wieder **Gabe von Animationen mit der optimalen Geschwindigkeit**: nicht so schnell, Sie sind schwer zu verstehen, aber nicht so langsam, Sie sind mühsam zu beobachten.

**Vergrößern/Verkleinern von Objekten**

-   **Inhalt während einer Größenänderung nicht abschneiden.** Erweitern Sie Container, bevor Sie Inhalte hinzufügen. Entfernen Sie Inhalte, bevor Sie Container reduzieren.

    **Falsch:**

    ![Screenshot des abgeschnittene Rechners ](images/vis-animations-image47.png)

    In diesem Beispiel wird der Inhalt während der Größenänderung abgeschnitten.

**Inhalt anzeigen/ausblenden/ändern**

-   **Wichtige Informationen statisch anzeigen.** Benutzer sollten nicht über eine progressive Offenlegung auf wichtige Informationen zugreifen müssen.

**Anzeigen/Ausblenden von Steuerelementen oder Kosten**

-   **Zeigen Sie wichtige Steuerelemente an, wenn der Benutzer den Mauszeiger an einer beliebigen Stelle im Fenster oder im Bereich positioniert, oder wenn der Vollbild-Mauszeiger bewegt wird.** Benutzer sollten diese Steuerelemente nicht überprüfen müssen, sodass Sie Ihre Ermittlung sicher machen.

    ![Abbildung, die anzeigt, wie mit dem Mauszeiger ](images/vis-animations-image48.png)

    In diesem Beispiel zeigt Windows Media Center die Steuerelemente an, wenn sich der Mauszeiger über dem Fenster befindet.

-   **Anzeigen sekundärer Steuerelemente oder Steuern von Kosten, wenn der Benutzer den Mauszeiger auf oder in der Nähe der Befehle positioniert.** Um die Auffindbarkeit zu vereinfachen, machen Sie den Standort offensichtlich und das Ziel groß.

    ![Screenshot des Zeigers, der den sekundären Befehl aufzeigt ](images/vis-animations-image49.png)

    In diesem Beispiel zeigt Windows Live Messenger einen sekundären Befehl an, wenn sich der Mauszeiger in der Nähe der oberen rechten Ecke befindet.

**Szenen Übergänge**

-   **Sorgen Sie für physische Szenen Übergänge in Einklang mit der natürlichen Zuordnung.** Personen, die von links nach rechts in westlichen Kulturen gelesen werden, und hierarchische Diagramme fließen von oben nach unten. Folglich wird der Fortschritt in der Zeit durch die Bewegung von links nach rechts angezeigt. Die folgenden physischen Szenen Übergänge haben eine natürliche Zuordnung:



    | Übergang                          | Bedeutung                                     |
    |---------------------------|--------------------------------------|
    | Von Links<br/>      | Zurück in den Aufgaben Fluss<br/>    |
    | Von rechts<br/>     | Vorwärts im Aufgaben Fluss<br/> |
    | Von oben<br/>       | Aufgaben Hierarchie nach oben verschieben<br/>    |
    | Von unten<br/>    | Aufgaben Hierarchie nach unten verschieben<br/>  |



 

-   **Wenn Ihr Programm Sound wieder gibt, entwerfen Sie Szenen Übergänge und audioübergänge.** Wenn eine Szene z. b. schrittweise ausgeblendet wird, sollte jeder Sound allmählich auch ausgeblendet werden. Vermeiden Sie nahtlose visuelle Übergänge durch abrupte Sound Übergänge. Weitere Informationen zu Sound finden Sie unter [Sound](vis-sound.md).

**Direkte Manipulationen**

-   **Wenn Sie physische Gesten in der Interaktion verwenden (z. b. das Umschalten), entwerfen Sie die Animation so, dass Sie wie eine natürliche Reaktion auf die Geste aussieht.** Verknüpfen Sie die Interaktions Ursache mit dem Übergangseffekt. Verleihen Sie der Animation reale physische Merkmale, wie z. b. Beschleunigung, Verlangsamung, Schwung, Widerstandsfähigkeit, Gewichtung, Sprung und Drehung.
-   **Halten Sie die Kontaktpunkte eines Objekts während der Interaktion reibungslos unter dem Zeiger, um ein direktes Gefühl zu erhalten.** Jede Verzögerung, eine verpacsantwort oder der Verlust von Kontakten zerstört die Wahrnehmung direkter Manipulationen. Objekte sollten bei der Manipulation nie verschwinden.

**Übergängen sortieren, Filtern oder Neuanordnen**

-   **Zeigen Sie für einfache Änderungen den gesamten Übergang an.** Benutzer können den gesamten Übergang problemlos durchführen. Einfache Änderungen umfassen vier Elemente oder weniger.
-   **Bei komplexen Änderungen wird das Ende der Bewegung bei der Verlangsamung hervorgehoben, und der Rest wird mit dem Augenblick aufgefüllt.** Auf diese Weise wird das Gefühl der Bewegung viel reaktionsfähiger und geordneter.

**Leistungs Übergänge**

-   **Denken Sie daran, langsame Übergänge in zwei oder drei Phasen auszuführen, damit Sie schneller und interaktiv angezeigt werden.** Verwenden Sie bei Bedarf die folgende Kompositions Reihenfolge:
    -   Externer Frame
    -   Hintergrund
    -   Ursprünglicher Inhalt (bei Bedarf unter Verwendung einer temporären Darstellung)
    -   Primäre Steuerelemente (sodass Benutzer sofort interagieren können)
    -   Sekundäre Steuerelemente und alle verbleibenden Elemente der Benutzeroberfläche
    -   Der endgültige Inhalt (bei Verwendung einer temporären Darstellung) verwenden Sie Übergänge wie "Fades" und "Folien", damit die Komposition reibungslos, ordnungsgemäß und verfeinert erscheint.

![Screenshot der Karte mit einem Satellitenfoto und einem Raster ](images/vis-animations-image50.png)

Wenn Sie einen Bildlauf in der Ansicht "Vogelperspektive" durchführen, wird in "ge Maps" ein temporäres Raster Auf diese Weise können Benutzer weiterhin sofort scrollen, bevor der endgültige Inhalt gerendert wird.

**Besondere Animations Animationen**

-   **Überdenken Sie animierte Begrüßungs Bildschirme (und statische Begrüßungs Bildschirme).** Häufig zeichnen sich die Begrüßungs Bildschirme nur darauf aus, wie lange ein Programm geladen werden muss, und Sie sind schnell dabei, die Willkommensseite zu laden. Obwohl Begrüßungs Bildschirme akzeptabel sind, wenn Sie nur angezeigt werden, wenn eine Benutzerinteraktion nicht möglich ist, ist es immer noch eine bessere Alternative, das Programm so zu entwerfen, dass Benutzer sofort mit dem Programm interagieren können, auch wenn es noch geladen wird.
-   **Geben Sie einen Befehl zum Überspringen der Einführung an, wenn ein animierter Begrüßungsbildschirm mehr als drei Sekunden benötigt.** Wenn Sie auf eine beliebige Stelle im Begrüßungsbildschirm klicken, sollte diese ebenfalls geschlossen werden Verwenden Sie alternativ eine kurze Version der Animation nach einem anfänglichen Zeitraum.

### <a name="performance"></a>Leistung

-   **Nehmen Sie nicht an, dass Benutzer auf Animationen und Übergänge Ihres Programms warten.** Verwenden Sie bei Bedarf kurze Animationen und Übergänge (weniger als 200 Millisekunden). Verwenden Sie schnellere Animationen (100 Millisekunden) für häufigere Vorgänge. Entwerfen Sie längere Animationen (mehr als eine Sekunde, in der Regel Feedback, Illustration und besondere Erfahrungs Muster), damit Benutzer weiterhin arbeiten können, während Sie ausgeführt werden.
-   **Entwerfen Sie Animationen mit langer Laufzeit, um Benutzern zu ermöglichen, dass Sie während der Ausführung der Animation interagieren können.** Benutzer versuchen nicht, die Arbeit fortzusetzen, wenn die visuellen Hinweise darauf hindeuten, dass Sie nicht möglich sind.

    ![Screenshot einer Statusleiste in einer Statusleiste ](images/vis-animations-image51.png)

    In diesem Beispiel aus Windows Internet Explorer schlägt die Statusleiste mit niedriger Tastatur in der Statusleiste vor, dass Benutzer nicht auf den Abschluss warten müssen, bevor Sie interagieren können.

-   **Verwenden Sie für CPU-intensive Aufgaben Lightweight-Animationen.** Dadurch erhalten Sie eine vollständige Verarbeitungsleistung für die Aufgabe. Außerdem bemerken Benutzer nicht, dass die leichte Animation der Grund dafür ist, dass die Aufgabe CPU-intensiv ist.
-   **Während einer Animation oder eines Übergangs wird kein Aktivitätsindikator angezeigt.** Dadurch wird der Effekt zerstört. Entwerfen Sie Animationen und Übergänge, damit Sie sofort loslegen können.
-   **Entwerfen Sie Animationen so, dass Sie immer dann ordnungsgemäß herabgestuft werden, wenn nicht genügend Systemressourcen** Animationen können durch Abweichungen, die weniger Ressourcen erfordern (z. b. kürzere Längen oder niedrigere Frameraten) oder gar nicht ausgeführt werden, herabgestuft werden. Unabhängig von den verfügbaren Ressourcen müssen Sie sicherstellen, dass die Animationen hochwertig sind und anstelle von Softwarefehlern Animationen wie Animationen aussehen.

    **Falsch:**

    ![Screenshot eines verblassten Programm Rahmens über den Desktop ](images/vis-animations-image52.png)

    In diesem Beispiel wird der Übergang der Fenster Wiederherstellung auch dann verwendet, wenn nicht genügend Systemressourcen vorhanden sind, um Sie gut abspielen zu können. Folglich scheint der fixierte Frame ein Fehler zu sein. Wenn die Ressourcen nicht verfügbar sind, ist es besser, das Fenster nur ohne einen Übergang anzuzeigen.

### <a name="animation-characteristics"></a>Animations Merkmale

Gut entworfene Animationen und Übergänge verfügen in der Regel über die folgenden Merkmale:

-   **Kurze Dauer.** Die meisten Animationen sollten zwischen 100 und 300 Millisekunden liegen, vorzugsweise entweder 1/6 Sekunden (167 Millisekunden) oder 1/4 Sekunde (250 Millisekunden). (Besondere Erlebnisse und Fortschritts Feedback können länger sein.) Verwenden Sie schnellere Animations Zeiten für häufigere Vorgänge. Im Allgemeinen nehmen längere Animationen mehr Zeit in Anspruch, nehmen mehr Zeit in Anspruch und können langsam sein.
-   **Digkeit.** Animationen sollten innerhalb von 50 Millisekunden des initiierenden Ereignisses oder der Benutzeraktion gestartet werden. Längere Startzeiten sind nicht reaktionsfähig.
-   **Beschleunigung/Verlangsamung.** Die meisten Animationseffekte müssen beschleunigt werden, wenn Sie beim Beenden Starten und verlangsamen. Um reaktionsfähig zu sein, entwerfen Sie Animationen, damit Sie schnell starten können. Um gesteuert angezeigt zu werden, entwerfen Sie Animationen so, dass Sie am Ende eine weiche Landung haben. Wenngleich dies für Bewegungs Effekte gilt, gilt dies auch für jede Auswirkung, die eine Bewegung vorschlägt, wie z. b. Zoom und sogar die Verweil.

    ![Abbildung eines Diagramms mit reduzierter Geschwindigkeit im Zeitverlauf ](images/vis-animations-image53.png)

    Die meisten Animationen sollten Schnellstarts und weiche Endungen aufweisen, um ein reaktionsfähiges, aber dennoch kontrolliertes Gefühl zu haben.

-   **Entschließungs.** Animationen, die eine bestimmte Bewegung darstellen, müssen beschleunigt und verlangsamt werden. verwenden Sie daher keine lineare Bewegung, es sei denn, die Animations Dauer ist sehr kurz. Bei der Bewegung sollten der Pfad Shorts von Anfang bis Ende ohne Überschreiben übernommen werden. Der vollständige Animations Pfad ist nicht immer erforderlich. Wenn dies der Fall ist, markieren Sie das Ende der Bewegung, wenn es verlangsamt wird, und lassen Sie das Auge den Rest ausfüllen. Auf diese Weise wird das Gefühl der Bewegung viel reaktionsfähiger und geordneter. Wenn Sie die Bewegung mehrerer Objekte gleichzeitig animieren, weisen Sie Ihnen leicht unterschiedliche Pfade mit etwas unterschiedlichen Zeiträumen zu, um natürlichere zu gestalten.
-   **Die Framerate.** Die meisten Animationen sollten eine Framerate von 20 Frames pro Sekunde verwenden. Wenn die Animation eine besondere Ober Linie ist oder mit dem Hauptzweck des Programms verknüpft ist, sollten Sie die Verwendung einer höheren Rate von 24 30 Frames pro Sekunde in Erwägung nehmen, um die glätttheit und den Realismus zu verbessern.
-   **Skalierung.** Entwerfen Sie Animationen so, dass Sie für den gesamten Bereich der vorgesehenen Verwendung gut funktionieren. Seiten Übergänge sollten z. b. so entworfen werden, dass Sie für alle Seitengrößen funktionieren.
-   **Persönlichkeits.** Entwerfen Sie Animationen, um naturgemäß, unterdrückt und effizient und nicht künstlich, positiv oder langsam zu sein.

### <a name="animated-text"></a>Animierter Text

-   Obwohl Sie Text mithilfe eines Übergangs anzeigen können, **animieren Sie den Text nicht fortlaufend.** Animierter Text ist oft ablenkend und schwieriger zu lesen als statischer Text. **Ausnahmen:**
    -   Sie können Text in Situationen animieren, in denen er traditionell animiert ist, und eine barrierefreie Alternative bereitstellen.
    -   Sie können Text animieren, wenn der Zweck des Texts hauptsächlich dekorativ ist.

![Screenshot der kreativ entworfenen Zune-Schnittstelle ](images/vis-animations-image13.png)

In diesem Beispiel animiert Zune den Text, aber sein Zweck ist hauptsächlich dekorativ. Es gibt kein Problem, wenn Benutzer den Text nicht sorgfältig lesen.

### <a name="reducing-power-consumption"></a>Reduzieren des Stromverbrauchs

-   **Entwerfen Sie Ihre Animationen, um den Energieverbrauch zu verringern.** Wenn die Animation ordnungsgemäß entworfen wurde, sollten Animationen den Energieverbrauch nicht signifikant erhöhen So reduzieren Sie den Stromverbrauch:
    -   **Animation beenden, wenn die Anzeige deaktiviert ist.** Die Anzeige ist möglicherweise deaktiviert, um Energie zu sparen.
    -   **Verwenden Sie keine Animationen mit langer Laufzeit, die nicht vom Benutzer initiiert wurden.** Animationen, die periodische Zeit Geber mit hoher Auflösung verwenden, verringern die Effizienz der Prozessor Energie Verwaltung. Achten Sie auch darauf, dass Sie alle regelmäßigen High-Resolution-Timer deaktivieren, wenn die Animationen fertig sind.
    -   **Alle Animationen aussetzen, wenn sich das System im Leerlauf befindet.** Der Zeitraum, in dem die Benutzer Inaktivität in den Leerlauf versetzt wird, wird durch Energieoptionen in der Systemsteuerung bestimmt

### <a name="accessibility"></a>Eingabehilfen

-   **Verwenden Sie Animation nicht als einzige Möglichkeit zum vermitteln wichtiger Informationen.** Animationen sollten nützliche Informationen vermitteln, die für Benutzer mit Sehbehinderung nicht zugänglich sind.
-   **Stellen Sie sicher, dass äquivalente Informationen auf andere Weise verfügbar sind,** z. b.:

    -   **Bei der Überprüfung.** Benutzer können entsprechende Informationen ermitteln, indem Sie sich den Bildschirm oder die an der Animation beteiligten Objekte ansehen.
    -   **Durch einfache Interaktion.** Benutzer können gleichwertige Informationen ermitteln, indem Sie mit der Maus darauf zeigen, klicken oder doppelklicken.

    ![Screenshot der Startseite von Startseite mit Hotspots ](images/vis-animations-image54.png)

    Die Startseite von Start enthält eine erste Animation, die mehrere Hotspots zeigt. Benutzer können die Hotspots auch anzeigen, indem Sie den Cursor in der Nähe bewegen.

    Beachten Sie, dass "äquivalente Informationen" nicht identische Informationen bedeuten. Die Informationen können in einem anderen Format vorliegen oder eine einfache Ableitung erfordern.

-   **Legen Sie bei Bedarf den Eingabefokus auf das Objekt fest, das während eines Übergangs geändert wurde.** Auf diese Weise können Hilfstechnologien erkennen, wo die Änderung aufgetreten ist. Ändern Sie den Eingabefokus jedoch nicht, wenn der Benutzer die Tastatur verwendet.
-   **Verwenden Sie keine Animationen oder Übergänge, die Objekte schnell blinken oder die Größe ändern.** Blinkende und schnelle Bildschirm Änderungen können für Personen mit Beeinträchtigungen und anderen neurologischen Störungen Probleme verursachen.
-   **Ermöglicht Benutzern das Deaktivieren der Animationen und Übergänge Ihres Programms.** Um diese Möglichkeit zu unterstützen, achten Sie darauf, dass Sie die Option alle unnötigen Animationen deaktivieren im Easy of Access Center in Windows berücksichtigen.

    **Entwickler:** Mithilfe der SystemParametersInfo-API können Sie feststellen, ob Animationen aktiviert sind.

-   **Entwerfen Sie Aufgaben, wenn Benutzer die Animation des Programms deaktivieren.** Stellen Sie sicher, dass dadurch der Aufgaben Fluss nicht erheblich unterbrochen wird.

Weitere Richtlinien für Barrierefreiheit finden Sie unter [Barrierefreiheit](inter-accessibility.md).

## <a name="documentation"></a>Dokumentation

-   Vermeiden Sie, wenn möglich, auf Animationen. Verweisen Sie stattdessen auf das zu animierende Objekt und ggf. auf den Typ der Animation.
-   Verweisen Sie nicht auf Übergänge, außer in der technischen Dokumentation. Verweisen Sie stattdessen auf das-Objekt in seinem endgültigen oder ursprünglichen Zustand.
-   Wenn der Benutzer eine Animation explizit initiiert, verwenden Sie das Verb Play. Verwenden Sie andernfalls das Verb use für die technische Dokumentation.

Beispiele:

-   Sie wissen, dass ein Element Ihre Aufmerksamkeit erfordert, wenn das Symbol mit dem springen beginnt.
-   Wählen Sie zunächst die Fotos aus, die Sie drucken möchten (Beachten Sie, dass die Fotos bei der Auswahl vergrößert werden).
-   Verwenden Sie einen Kreuz Fade-Übergang, um den Zustand eines Objekts nahtlos zu ändern.

