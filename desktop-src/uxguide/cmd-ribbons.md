---
title: Menübänder
description: Multifunktionsleisten sind die moderne Methode, um Benutzern die effiziente und direkte Verwendung von Befehlen zu erleichtern 8212, mit einer minimalen Anzahl von Klicks, wobei weniger Anforderungen auf "Test-und Fehler" zurückgegriffen werden müssen und ohne dass auf die Hilfe verwiesen werden muss.
ms.assetid: 8a4699da-9840-4622-9e94-d6d5c4e7708c
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2327a633f02c9d56116367405803c4da56ad5b19
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351028"
---
# <a name="ribbons"></a>Menübänder

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mithilfe von Multifunktionsleisten können Benutzer Befehle effizient und direkt mit einer minimalen Anzahl von Klicks suchen, verstehen und verwenden, ohne dass Sie auf die Testversion zurückgreifen müssen, ohne auf die Hilfe zugreifen zu müssen.

Ein Menüband ist eine Befehlsleiste, die die Funktionen eines Programms in einer Reihe von Registerkarten am oberen Rand eines Fensters organisiert. Die Verwendung eines Menübands steigert die Auffindbarkeit von Features und Funktionen, ermöglicht das schnellere Erlernen des Programms als Ganzes und sorgt dafür, dass Benutzer mehr Kontrolle über Ihre Erfahrung mit dem Programm haben. Ein Menüband kann sowohl die traditionelle Menüleiste als auch die Symbolleisten ersetzen.

![Screenshot eines Menübands ](images/cmd-ribbons-image1.png)

Ein typisches Menüband.

Menüband-Registerkarten bestehen aus Gruppen, bei denen es sich um eine Bezeichnung mit eng verknüpften Befehlen handelt. Neben Registerkarten und Gruppen bestehen auch Menü Bänder aus folgenden Elementen:

- Eine Anwendungs Schaltfläche, die ein Menü mit Befehlen anzeigt, die eine Aktion für ein Dokument oder einen Arbeitsbereich, wie z. b. Datei bezogene Befehle, beinhalten.
- Eine Symbolleiste für den schnell Zugriff, eine kleine, anpassbare Symbolleiste, auf der häufig verwendete Befehle angezeigt werden.
- Kern Registerkarten sind die Registerkarten, die immer angezeigt werden.
- Kontextbezogene Registerkarten, die nur angezeigt werden, wenn ein bestimmter Objekttyp ausgewählt wird. Registerkarten, die immer angezeigt werden, werden als Kern Registerkarten bezeichnet.
- Eine Registerkarten Gruppe ist eine Sammlung von kontextbezogenen Registerkarten für einen einzelnen Objekttyp. Da-Objekte über mehrere Typen verfügen können (z. b. ein Header in einer Tabelle, die ein Bild enthält, sind drei Typen), können mehrere kontextabhängige Registerkarten Sätze gleichzeitig angezeigt werden.
- Modale Registerkarten, bei denen es sich um Kern Registerkarten handelt, die in einem bestimmten temporären Modus angezeigt werden
- Galerien, bei denen es sich um Listen von Befehlen oder Optionen handelt, die grafisch dargestellt werden In einem ergebnisbasierten Katalog werden die Auswirkungen der Befehle oder Optionen anstelle der Befehle selbst veranschaulicht. Ein in-Ribbon-Katalog wird im Gegensatz zu einem Popup Fenster in einem Menüband angezeigt.
- Erweiterte Quick Infos, die ihre zugehörigen Befehle kurz erläutern und die Tastenkombinationen liefern. Sie können auch Grafiken und Verweise enthalten, die Ihnen helfen. Erweiterte Quick Infos reduzieren die Notwendigkeit einer Befehls bezogenen Hilfe.
- Dialogfeld-Launcher, bei denen es sich um Schaltflächen am unteren Rand einiger Gruppen handelt, die Dialogfelder öffnen, die mit der Gruppe verknüpfte Funktionen enthalten.

Menü Bänder wurden ursprünglich mit Microsoft Office 2007 eingeführt. Weitere Informationen zur Verwendung von Multifunktionsleisten und den vielen Problemen bei der Verwendung eines Menübands finden Sie in [der Geschichte der Multifunktionsleiste](/archive/blogs/jensenh/the-story-of-the-ribbon).

> [!Note]  
> Richtlinien, die sich auf [Menüs](cmd-menus.md), [Symbolleisten](cmd-toolbars.md), [Befehls](ctrl-command-buttons.md)Schaltflächen und [Symbole](vis-icons.md) beziehen, werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Um sich für die Verwendung eines Menübands zu entscheiden, sollten Sie die folgenden Fragen

### <a name="program-type"></a>Programmtyp

- **Welche Art von Programm entwerfen Sie?** Der Programmtyp ist ein guter Indikator für die Eignung eines Menübands. Menü Bänder funktionieren gut für die Erstellung und Erstellung von Dokumenten sowie für Dokument-Viewer und Browser. Multifunktionsleisten können für andere Programmtypen verwendet werden, aber andere Formen der Befehls Darstellung sind möglicherweise besser geeignet. Im Allgemeinen sollten Lightweight-Programme über eine vereinfachte Befehls Präsentation verfügen.

### <a name="discoverability-and-learning-issues"></a>Ermittelbarkeits-und Lernprobleme

- **Haben Benutzer Probleme beim Suchen von Befehlen? Fordern Benutzer Funktionen an, die bereits im Programm vorhanden sind?** Wenn dies der Fall ist, werden Befehle mithilfe eines Menübands leichter zu finden, da Sie Überselbst erklärende Bezeichnungen und die Gruppierung verwandter Befehle verfügen. Die Verwendung eines Menübands skaliert auch besser als Menüleisten und Symbolleisten für zukünftiges Wachstum.
- **Haben Benutzer Probleme beim Verständnis der Programm Befehle? Werden Sie häufig auf "Testversion und Fehler" zurückgreifen, um den richtigen Befehl auszuwählen oder zu bestimmen, wie Befehle funktionieren?** Wenn dies der Fall ist, können Befehle mithilfe eines Menübands mit ergebnisorientierten Befehlen auf der Grundlage von Galerien und Live-Vorschauen leichter verständlich werden.

### <a name="command-characteristics"></a>Befehls Merkmale

- **Werden die Befehle an verschiedenen Speicherorten angezeigt? Wenn das Programm bereits vorhanden ist, werden Befehle in Menüleisten, Symbolleisten, Aufgabenbereichen und innerhalb des Arbeitsbereichs selbst angezeigt?** Wenn dies der Fall ist, werden die Befehle mithilfe eines Menübands in einem einzigen Speicherort vereinheitlichen, sodass Sie leichter zu finden sind.
- **Gelten die Befehle für das gesamte Fenster oder nur für bestimmte Bereiche?** Menü Bänder funktionieren am besten für Befehle, die für das gesamte Fenster oder bestimmte Objekte gelten. Direkte Befehle funktionieren besser für einzelne Fensterbereiche.
- **Können die meisten Befehle direkt angezeigt werden? Das heißt, können Benutzer mit Ihnen mit einem einzigen Mausklick interagieren? Wenn auf häufig verwendete Befehle in Menüs und Dialogfeldern zugegriffen wird, können Sie als direkt umgestaltet werden?** Obwohl einige Befehle mithilfe von Menüs und Dialogfeldern angezeigt werden können, wird durch die Darstellung der meisten Befehle auf diese Weise die Effizienz eines Menübands untergraben, was möglicherweise eine Menüleiste besser macht.

### <a name="command-scale"></a>Befehls Skala

- **Gibt es eine kleine Anzahl von Befehlen? Können die am häufigsten verwendeten Befehle auf einer einzelnen, einfachen Symbolleiste problemlos angezeigt werden?** Die Verwendung eines Menübands lohnt sich, wenn das Hinzufügen von Kern-und Kontext Registerkarten zu einer einfachen Registerkarte Home führt, die allein zum Ausführen der gängigsten Aufgaben verwendet werden kann. Wenn dies nicht der Vorteil ist, kann der Vorteil der Verwendung eines Menübands die zusätzliche Gewichtung für eine kleine Anzahl von Befehlen nicht rechtfertigen.
- **Gibt es eine große Anzahl von Befehlen? Erfordert die Verwendung eines Menübands mehr als sieben Kern Registerkarten? Müssten Benutzer die Registerkarten ständig ändern, um häufige Aufgaben auszuführen?** Wenn dies der Fall ist, ist die Verwendung von Symbolleisten (die keine geänderten Registerkarten erfordern) und [palettenfenstern](cmd-toolbars.md) (die möglicherweise das Ändern von Registerkarten erfordern, aber es können mehrere offene gleichzeitig vorhanden sein) eine effizientere Wahl.
- **Neigen Benutzer meistens dazu, eine kleine Anzahl von Befehlen zu verwenden?** Wenn dies der Fall ist, können Sie eine Multifunktionsleiste effizient verwenden, indem Sie diese Befehle auf der Registerkarte Home ablegen. Durch das ständig geänderte ändern von Registerkarten wird ein Menüband zu ineffizient.
- **Hat das Programm den Vorteil, dass der Inhalts Bereich des Programms so groß wie möglich ist?** Wenn dies der Fall ist, ist die Verwendung einer Menüleiste und einer einzelnen Symbolleiste mehr Speicherplatz als ein Menüband. Wenn das Programm jedoch drei oder mehr Zeilen mit Symbolleisten erfordert oder Aufgabenbereiche verwendet, ist die Verwendung eines Menübands mehr platzsparend.
- **Arbeiten Benutzer über einen längeren Zeitraum in einem bestimmten Bereich innerhalb eines großen Fensters im Programm?** Wenn dies der Fall ist, profitieren Sie von der engen Nähe von Mini-Symbolleisten, palettenfenstern und direkten Befehlen. Der Roundtrip aus dem Arbeitsbereich zum Menüband wäre zu ineffizient.
- **Aus Gründen der Effizienz und Flexibilität müssen Benutzer bedeutende Änderungen am Inhalt, an der Position oder der Größe der Befehls Präsentation vornehmen?** Wenn dies der Fall ist, sind anpassbare und erweiterbare Symbolleisten und Palettenfenster eine bessere Wahl. Beachten Sie, dass einige Arten von Symbolleisten nicht angedockt werden können, um Palettenfenster zu werden. Palettenfenster können verschoben, verkleinert und angepasst werden.

Und schließlich sollten Sie diese ultimative Frage beachten: **ist die Verbesserung der Auffindbarkeit, der Einfachheit des Lernens, der Effizienz und der Produktivität die Kosten des zusätzlichen Platzes und die Notwendigkeit von Registerkarten, Befehle zu organisieren?** Wenn dies der Fall ist, ist die Verwendung eines Menübands eine gute Wahl. Wenn Sie nicht sicher sind, sollten Sie die Benutzerfreundlichkeit testen, indem Sie einen Menüband-basierten Entwurf testen und ihn mit der optimalen Alternative vergleichen.

Menü Bänder sind eine neue und ansprechende Form der Befehls Präsentation und eine hervorragend Möglichkeit zum modernisieren eines Programms. Aber so aussagekräftigen wie Sie sind, sind Sie nicht für jedes Programm die richtige Wahl.

**Falsch:**

![Screenshot eines Menübands mit einem Rechner ](images/cmd-ribbons-image2.png)

Bitte machen Sie das nicht!

## <a name="seven-most-important-things"></a>Sieben wichtigsten Dinge

1. Wählen Sie eine für den Programmtyp geeignete Befehls Projekt Mappe aus. Die Verwendung eines Menübands sollte ein Programm einfacher, effizienter und leichter zu verwenden sein. Wenn die Verwendung eines Menübands nicht geeignet ist, sollten Sie stattdessen vielfältige Befehle verwenden.  
2. Unterschätzen Sie nicht die Herausforderung, eine effektive Multifunktionsleiste zu erstellen. Es ist nicht zu erwarten, dass es sich um einen einfachen Port der vorhandenen Menüleisten und Symbolleisten handelt. Nehmen Sie nicht an, dass durch die Verwendung eines Menübands das Programm automatisch verbessert wird. Ein wichtiger Faktor bei der Entscheidung, ein Menüband zu verwenden, ist ein wichtiger Faktor bei der Entscheidung, eine Multifunktionsleiste zu verwenden.  
3. Machen Sie die Befehle sichtbar. Wählen Sie einen Registerkarten Entwurf aus, der eine klare, offensichtliche und eindeutige Zuordnung zwischen den Befehlen und den deskriptiv beschrifteten Registerkarten enthält, auf denen Sie sich befinden. Benutzer sollten in der Lage sein, schnell und zuverlässig zu ermitteln, welche Registerkarte den gesuchten Befehl aufweist, und nur selten die falsche Registerkarte auszuwählen.  
4. Machen Sie die Befehle selbsterklärend. Benutzer sollten die Auswirkung eines Befehls auf die Bezeichnung, das Symbol, die QuickInfo und die Vorschau kennen. Sie sollten kein Hilfethema experimentieren oder lesen, um zu sehen, wie ein Befehl funktioniert.  
5. Verwenden Sie die Befehle effizient:
    - Benutzer sollten den größten Teil ihrer Zeit auf der Registerkarte Home aufwenden.
    - Benutzer sollten die Registerkarten bei häufigen Aufgaben nur selten ändern.
    - Wenn das Fenster maximiert ist und sich die Benutzer auf der korrekten Registerkarte befinden, haben die am häufigsten verwendeten Befehle die größte visuelle Betonung, und Benutzer können Sie mit einem einzigen Mausklick aufrufen. Benutzer können auf der Registerkarte mit höchstens vier Klicks alle anderen Befehle ausführen.
    - Benutzer sollten keine Dialogfelder öffnen müssen, um Befehle und das Ändern von Attributen in allgemeinen Aufgaben zu unterstützen.
6. Helfen Sie Benutzern, Befehle und Optionen zuverlässig auszuwählen, und minimieren Sie die Notwendigkeit von Test-und Fehler Anforderungen. Verwenden Sie bei Bedarf ergebnisorientierte Befehle, häufig in Form von Galerien und Live-Vorschau Versionen.  
7. Stellen Sie sicher, dass das Menüband von der größten Fenstergröße auf das kleinste Fenster skaliert wird.  

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="adapting-a-ribbon-in-an-existing-program"></a>Anpassen eines Menübands in einem vorhandenen Programm

Sie können eine traditionelle Menüleiste und einen Symbolleisten Entwurf eines vorhandenen Programms einfach auf ein Menüband-Format umgestalten. Dadurch wird der größte Teil des Werts der Verwendung eines Menübands verpasst. Menü Bänder haben den größten Wert, wenn Sie zum präsentieren sofortiger, ergebnisorientierter Befehle verwendet werden, häufig in Form von Galerien und Live Vorschau. Ergebnisorientierte Befehle erleichtern das Verständnis von Befehlen, und die Benutzer sind viel effizienter und produktiver. Anstatt die vorhandenen Befehle umzugestalten, ist es besser, vollständig umzugestalten, wie Befehle in Ihrem Programm ausgeführt werden.

Unterschätzen Sie nicht die Herausforderung, eine effektive Multifunktionsleiste zu erstellen. Nehmen Sie nicht an, dass durch die Verwendung eines Menübands das Programm automatisch verbessert wird. Das Erstellen eines effektiven Menübands erfordert viel Zeit und Aufwand. Ein wichtiger Faktor bei der Entscheidung, ein Menüband zu verwenden, ist ein wichtiger Faktor bei der Entscheidung, eine Multifunktionsleiste zu verwenden.

### <a name="the-nature-of-ribbons"></a>Die Art von Menü Bändern

Im Vergleich zu herkömmlichen Menüleisten und Symbolleisten haben Multifunktionsleisten die folgenden Eigenschaften:

- **Eine einzelne Benutzeroberfläche (User Interface, UI) für alle Befehle.** Menüleisten sind umfassend und leicht zu erlernen, und Symbolleisten sind effizient und direkt, aber warum sollten Sie nicht etwas mehr Bildschirmfläche verwenden, um eine einzelne Befehls Benutzeroberfläche zu erstellen, die all diese Elemente erreicht? Mit nur einer Benutzeroberfläche ist es für Multifunktionsleisten nicht erforderlich, dass Benutzer ermitteln, welche Benutzeroberfläche über den gesuchten Befehl verfügt.
- **Sichtbar und selbsterklärend.** Menüleisten Befehle sind durch ihre Bezeichnungen selbsterklärend, sind aber in den meisten Fällen ausgeblendet. Um den Bildschirmbereich zu speichern, werden Symbolleisten Schaltflächen hauptsächlich durch Symbole anstelle von Bezeichnungen dargestellt (obwohl einige Symbolleisten Schaltflächen beide verwenden) und von Quick Infos abhängig sind, wenn das Symbol nicht selbsterklärend ist. Benutzer kennen die Symbole jedoch im Allgemeinen nur für die am häufigsten verwendeten Befehle.
- Durch die Bereitstellung der meisten Befehle mit beschrifteten Symbolen sind Menü Band Befehle sichtbar und selbsterklärend, und Quick Infos werden nur zur Bereitstellung zusätzlicher Informationen verwendet. Es ist kaum notwendig, an einer anderen Stelle (z. b. in der Hilfe) einen Befehl zu verstehen.
- **Bezeichnete Gruppierung.** Während Menü Kategorien bezeichnet werden, sind Gruppen in einem Dropdown Menü nicht, und Sie werden nur mit einem nicht beschrifteten Trennzeichen angezeigt. Gruppen innerhalb von Symbolleisten werden auch mit nicht beschrifteten Trennzeichen gekennzeichnet.
- Durch das Organisieren von Befehlen in gekennzeichneten Gruppen vereinfachen Sie das Auffinden von Befehlen und das Ermitteln Ihres zwecks.
- **Modal, aber nicht hierarchisch.** Menüleisten skalieren, indem Sie eine Hierarchie von Befehlen erstellen. Menüs mit vielen Elementen können eine oder mehrere Ebenen von Untermenüs verwenden, um weitere Befehle bereitzustellen.
- Menü Band Befehle erfordern mehr Speicherplatz als Symbolleisten Befehle, sodass Sie mit Tabstopps skaliert werden. Diese Verwendung von Registerkarten macht Multifunktionsleisten Modal und erfordert, dass Benutzer gelegentlich Modi ändern, um Befehle zu finden. In einer Registerkarte sind die meisten Befehle jedoch entweder direkt, oder Sie verwenden eine einzelne Trenn Schaltfläche oder Menü Schaltfläche, keine Hierarchie.
- **Direkt und direkt.** Ein Befehl ist "Direct", wenn er mit einem einzigen Mausklick aufgerufen wird (d. h. ohne Navigation durch Menüs) und sofort wirksam wird, wenn er sofort wirksam wird (d. h. ohne Dialogfelder, um zusätzliche Eingaben zu erfassen). Menüleisten Befehle sind immer indirekt und oft nicht unmittelbar. Wie Symbolleisten sind die meisten Menü Band Befehle direkt und direkt konzipiert, wobei die am häufigsten verwendeten Befehle mit nur einem Mausklick aufgerufen werden, ohne dass ein Dialogfeld zum Erfassen zusätzlicher Eingaben erforderlich ist.
- **Läufige.** Menüleisten und Symbolleisten sind in erster Linie so konzipiert, dass Sie Speicherplatz effizient sind. Um Ihre Vorteile zu gewährleisten, verbrauchen Multifunktionsleisten möglicherweise mehr vertikalen Raum, und Sie sind ungefähr gleichwertig mit einer Menüleiste plus drei Zeilen von Symbolleisten. Wenn nur wenige Programme über drei oder mehr Zeilen mit Symbolleisten verfügen, verbrauchen Multifunktionsleisten in der Regel mehr Platz als herkömmliche UIs für Befehle.
- **Hat eine Anwendungs Schaltfläche und eine Symbolleiste für den schnell Zugriff** Ein Menüband wird immer mit einer Anwendungs Schaltfläche und einem schnell Zugriffs Symbol angezeigt. Auf diese Weise können Benutzer auf Datei bezogene und häufig verwendete Befehle zugreifen, ohne Registerkarten zu ändern, und die Konsistenz zwischen den Programmen herauf Stufen.
- **Minimale Anpassung.** Während Menüleisten über eine festgelegte Präsentation verfügen, sind viele Symbolleisten Recht anpassbar, sodass Benutzer Orte, Größen und Inhalte festlegen können. Ein Menüband selbst ist nicht anpassbar, aber die Symbolleiste für den schnell Zugriff bietet eingeschränkte Anpassungen.
- **Verbesserter Tastatur Zugriff.** Menüleisten verfügen über eine hervorragende Tastatureingabe, da durch Drücken der Alt-Taste direkt der Eingabefokus der Menüleiste angezeigt wird. Es gibt jedoch keinen Mechanismus für Symbolleisten, da Sie die Tastaturnavigation mit dem Inhalt des Fensters gemeinsam verwenden. Folglich müssen die Benutzer mithilfe der Tab-Taste (die das letzte Tabstopp Symbol erhält) zur Symbolleiste navigieren und dann mithilfe der Pfeiltasten zu einem bestimmten Befehl navigieren.

Im Gegensatz dazu bieten Multifunktionsleisten erweiterte Tastatureingaben durch [KeyTips](glossary.md)(in der Regel mit einem dreistufigen Prozess):

- Drücken Sie alt, um den KeyTip-Modus einzugeben.
- Drücken Sie ein Zeichen, um eine Registerkarte, die Anwendungs Schaltfläche oder einen Befehl in der Symbolleiste für den schnell Zugriff auszuwählen.
- Drücken Sie innerhalb einer Registerkarte einen oder zwei Buchstaben, um einen Befehl auszuwählen.

    Diese Vorgehensweise ist sehr visuell. Sie ist auch flexibler und ermöglicht eine bessere Skalierung und mehr mnemonische Zugriffsschlüssel Zuweisungen.

    Verwechseln Sie Zugriffstasten nicht mit Tastenkombinationen. Obwohl sowohl Zugriffsschlüssel als auch Tastenkombinationen Tastatur Zugriff auf die Benutzeroberfläche bieten, haben Sie unterschiedliche Zwecke und Richtlinien. Weitere Informationen finden Sie unter [Tastatur](inter-keyboard.md).

### <a name="the-nature-of-rich-commands"></a>Die Art von Rich-Befehlen

Rich-Befehle beziehen sich auf die Darstellung und Interaktion von Befehlen, die von Menü Bändern verwendet werden, ohne notwendigerweise einen Multifunktionsleisten Container zu verwenden. Rich-Befehle haben folgende Merkmale:

- **Erungs.** Allen Befehlen werden selbsterklärende Bezeichnungen zugewiesen, mit Ausnahmen nur, wenn die Symbole sehr gut bekannt sind und der Speicherplatz in einem Premium-Bereich liegt.

    **Richtig:**

    ![Screenshot eines Menübands mit Zeichen Formatierung ](images/cmd-ribbons-image3.png)

    Diese Befehle sind sehr gut bekannt, sodass Sie keine Bezeichnungen benötigen.

    **Falsch:**

    ![Screenshot eines Menübands mit selten verwendeten Symbolen ](images/cmd-ribbons-image4.png)

    Diese nicht verständlichen Symbole erfordern Bezeichnungen für Rich-Befehle.

- **Vermessung.** Anstelle von einheitlicher Größenanpassung werden die Größe der Befehle relativ zu ihrer Verwendungs Häufigkeit und Wichtigkeit gemessen. Zusätzlich zu den am häufigsten verwendeten Befehlen, die leichter zu finden sind, und klicken Sie [darauf.](https://msdn.microsoft.com/library/windows/desktop/cc872774.aspx)

    ![Screenshot von einem großen und drei kleinen Schaltflächen ](images/cmd-ribbons-image5.png)

    In diesem Beispiel ist die am häufigsten verwendete Schaltfläche größer als die anderen.

- **Dynamische Größenanpassung.** Rich-Command-Steuerelemente ändern sich selbst, um den verfügbaren Speicherplatz in vollem Umfang zu nutzen, anstatt eine Größe mit fester Größe zu verwenden und einen Überlauf zu verwenden, wenn die Größe zu klein ist.

    ![Screenshot des breiten Menübands mit Schaltflächen gleicher Größe ](images/cmd-ribbons-image6.png)![Screenshot des kleinen Menübands mit gemischten Schaltflächen ](images/cmd-ribbons-image7.png)

    In diesem Beispiel ändern sich die Befehls Schaltflächen so, dass Sie im verfügbaren Platz ordnungsgemäß funktionieren.

- **Trenn Schaltflächen.** Unterteilte Schaltflächen sind eine gute Möglichkeit, um bei Bedarf eine Reihe von Variationen eines Befehls zu konsolidieren und gleichzeitig die Direktheit für den am häufigsten verwendeten Befehl beizubehalten.

    ![Screenshot des Befehls "Speichern unter" und seiner Optionen ](images/cmd-ribbons-image8.png)

    In diesem Beispiel verwendet der Befehl "Speichern unter" eine Trenn Schaltfläche, bei der die Haupt Schaltfläche die häufigste Variation ausführt und der Menübereich ein Menü mit Variationen des Befehls zeigt.

- **Umfangreiche Dropdown Menüs und Galerien.** Dropdown Menüs, Dropdown Listen und Kataloge belegen den Platz, den Sie für die Kommunikation benötigen, und unterscheiden die Auswirkungen der Auswahl, häufig mithilfe von Grafiken und Textbeschreibungen. Kategorien werden verwendet, um große Mengen von Optionen zu organisieren.

    ![Screenshot der Dropdown Menü Optionen mit Symbolen ](images/cmd-ribbons-image9.png)

    Wenn Sie in diesen Beispielen auf eine Menü Schaltfläche klicken, wird eine Liste der Optionen angezeigt, die ihre Auswirkung anzeigen.

- **Live Vorschau.** Jedes Mal, wenn der Benutzer auf eine Formatierungs Option zeigt, zeigt das Programm an, wie die Ergebnisse mit dieser Formatierung mit dem tatsächlichen Inhalt aussehen würden.

    ![Screenshot der Ergebnisse der Formatierungsoptionen ](images/cmd-ribbons-image10.png)

    Die Live Vorschau zeigt die Ergebnisse der Anwendung einer Formatierungs Option auf den Mauszeiger.

- **Erweiterte Quick Infos.** In diesen Abschnitten werden die zugehörigen Befehle erläutert und die Tastenkombinationen übergeben. Sie können auch Grafiken und Verweise enthalten, die Sie unterstützen (obwohl Sie die Notwendigkeit der Befehls bezogenen Hilfe größtenteils ausschließen).

    ![Screenshot der großen QuickInfo mit Text und Grafik ](images/cmd-ribbons-image11.png)

    Erweiterte Quick Infos erläutern ihre zugehörigen Befehle.

Menü Bänder sind möglicherweise nicht für alle Programme geeignet, aber alle Programme können von umfangreichen Befehlen profitieren.

### <a name="ribbons-always-have-an-application-button-and-quick-access-toolbar"></a>Menü Bänder haben immer eine Anwendungs Schaltfläche und eine Symbolleiste für den

Die Anwendungs Schaltfläche und die Symbolleiste für den schnell Zugriff stellen Befehle bereit, die in einem beliebigen Kontext nützlich sind, wodurch die Notwendigkeit, Registerkarten zu ändern Diese drei Komponenten sind logisch unabhängig, aber ein Menüband muss immer über eine Anwendungs Schaltfläche und eine Symbolleiste für den schnell Zugriff verfügen. Da Befehle entweder in der Multifunktionsleiste oder auf der Anwendungs Schaltfläche ausgeführt werden können, Fragen Sie sich vielleicht, wo Sie Befehle platzieren. Die Auswahl ist nicht willkürlich.

Die Schaltfläche Anwendung wird verwendet, um ein Menü mit Befehlen anzuzeigen, die eine Datei oder eine Datei verwenden, wie z. b. Befehle, die traditionell im Menü Datei zum Erstellen, öffnen und Speichern von Dateien, zum Drucken und zum Senden und Veröffentlichen von Dokumenten verwendet werden.

Im Gegensatz dazu ist das Menüband selbst für Befehle, die den Inhalt des Fensters beeinflussen. Beispiele hierfür sind Befehle, mit denen der Inhalt gelesen, geändert oder verwendet oder die Ansicht geändert wird.

Wenn Sie ein Menüband verwenden, müssen Sie auch dann eine Anwendungs Schaltfläche verwenden, wenn das Programm keine Dokumente oder Dateien umfasst. Verwenden Sie in solchen Fällen das Menü Anwendung, um Befehle zum Drucken, Programmoptionen und zum Beenden des Programms zu präsentieren. Obwohl die Anwendungs Schaltfläche für solche Programme nicht benötigt wird, bietet die Verwendung der Anwendung eine programmübergreifende Konsistenz. Benutzer müssen keine Befehle zum Speichern und rückgängig machen, da Sie sich immer am gleichen Ort befinden.

Die Symbolleiste für den schnell Zugriff ist auch dann erforderlich, wenn das Menüband nur eine Registerkarte verwendet. Obwohl solche Programme zwar nicht eine Symbolleiste für den schnell Zugriff benötigen (da alle Befehle bereits auf der Registerkarte "Single" vorhanden sind), bietet eine anpassbare Symbolleiste für den schnell Zugriff eine programmübergreifende Konsistenz. Wenn Benutzer z. b. in der Lage sind, auf den Befehl Drucken zu klicken, sollten Sie in jedem Programm, das eine Multifunktionsleiste verwendet, in der Lage sein.

### <a name="organization-and-discoverability"></a>Organisation und Auffindbarkeit

Durch die Bereitstellung von Registerkarten und Gruppen können Sie mithilfe von Multifunktionsleisten Ihre Befehle zur besseren Auffindbarkeit organisieren. Die Herausforderung besteht darin, dass die Organisation, wenn die Organisation schlecht ist, die Auffindbarkeit stattdessen erheblich beschädigen kann. Zwischen den Befehlen und den deskriptiv beschrifteten Registerkarten und Gruppen, in denen Sie sich befinden, sollte eine klare, offensichtliche und eindeutige Zuordnung vorhanden sein.

Benutzer bilden ein geistiges Modell des Menübands, nachdem es eine Weile lang verwendet wurde. Wenn dieses geistige Modell für Benutzer nicht sinnvoll ist, ineffizient ist oder falsch ist, führt dies zu Verwirrung und Frustration. **Das wichtigste Ziel beim Entwerfen eines Menübands besteht darin, Befehle schnell und zuverlässig zu finden. Wenn Sie dies nicht erreichen, schlägt das Menüband-Design fehl.** Das Erreichen dieses Ziels erfordert sorgfältige Entwurf, Benutzer Tests und Iterationen. Gehen Sie nicht davon aus, dass es einfach ist.

Es folgen einige häufige Fehler, die vermieden werden sollten:

- **Vermeiden Sie generische Registerkarten-und Gruppennamen.** Ein guter Registerkarten-oder Gruppenname muss seinen spezifischen Inhalt genau beschreiben, vorzugsweise mithilfe der Aufgaben-und Ziel basierten Sprache. Vermeiden Sie generische Registerkarten-und Gruppennamen sowie technologiebasierte Namen. Beispielsweise können fast alle Befehle in einem Dokument, das das Programm erstellt und erstellt, zu den Registerkarten "Bearbeiten", "Format", "Tools", "Optionen", "Erweitert" Verlassen Sie sich auf bestimmte, beschreibende Bezeichnungen und keine memorzation.
- **Vermeiden Sie übermäßig spezifische Registerkarten-und Gruppennamen.** Wenn Sie möchten, dass Registerkarten-und Gruppennamen spezifisch sind, sollten Sie nicht so spezifisch sein, dass Benutzer durch ihren Inhalt überrascht werden. Benutzer suchen häufig nach Dingen, die den Prozess der Löschung verwenden. Daher sollten Sie verhindern, dass Ihre Registerkarten oder Gruppen übersehen werden, da der Name irreführend ist.
- **Vermeiden Sie mehrere Pfade zum gleichen Befehl, insbesondere dann, wenn der Pfad unerwartet ist oder für den Befehl viele Klicks aufgerufen werden müssen.** Es mag so aussehen, als wäre es sinnvoll, einen Befehl über mehrere Pfade zu finden. Denken Sie jedoch daran, dass Benutzer, die Sie suchen, nicht mehr suchen. Benutzer können davon ausgehen, dass der erste Pfad, den Sie finden, der einzige Pfad ist, bei dem es sich um ein schwerwiegendes Problem handelt, wenn dieser Pfad ineffizient oder unerwartet ist. Außerdem erschwert das vorhanden sein doppelter Befehle Benutzern das Auffinden anderer Befehle, nach denen Sie suchen.

![Screenshot des indirekten Pfades zum Rahmen Befehl ](images/cmd-ribbons-image12.png)

In diesem Beispiel können Sie Absatz Rahmen über den Befehl Seitenrahmen ändern, auch wenn auf der Registerkarte Home ein direkter Pfad vorhanden ist. Wenn Benutzer, die nach Absatz Rahmen suchen, über diesen unerwarteten Pfad stolpern würden, können Sie leicht davon ausgehen, dass es sich um den einzigen Pfad handelt.

- **Vermeiden Sie eine willkürliche Befehls Platzierung.** Angenommen, Sie haben einen guten Registerkarten-und Gruppen Entwurf, aber Sie werden feststellen, dass mehrere Befehle einfach nicht in passen. Die Wahrscheinlichkeit ist, dass Ihr Registerkarten-und Gruppen Design nicht so gut ist wie Sie sehen, und Sie müssen es weiter verfeinern. Lösen Sie dieses Problem nicht, indem Sie die Befehle einfügen, die nicht zu gehören. Wenn Sie dies tun, müssen Benutzer wahrscheinlich jede Registerkarte Überprüfen, um Sie zu finden, und dann umgehend vergessen, wo Sie sich befinden.
- **Vermeiden Sie Marketing basierte Platzierung.** Angenommen, Sie haben eine neue Version Ihres Programms, und Ihr Marketing Team möchte seine neuen Features wirklich herauf Stufen. Es könnte verlockend sein, Sie auf der Registerkarte "Home" zu platzieren, aber dies ist ein kostspieliger Fehler, wenn Sie die allgemeine Auffindbarkeit beeinträchtigen. Sehen Sie sich zukünftige Versionen Ihres Produkts an und wie viel Frust eine ständig veränderliche Organisation verursachen wird.

### <a name="tabs"></a>Registerkarten

Der beste erste Schritt ist das Überprüfen der [Standard Registerkarten des Menübands](#standard-ribbon-tabs). Wenn die Befehle Ihres Programms auf natürliche Weise den Standard Registerkarten zugeordnet sind, basieren Sie auf der Registerkarten Organisation auf diesen Standards. Wenn Sie die Befehle des Programms jedoch nicht auf natürliche Weise zuordnen, versuchen Sie nicht, Sie zu erzwingen. Legen Sie eine natürlichere Struktur fest, und stellen Sie sicher, dass Sie viele Benutzer Tests durchführen, um sicherzustellen, dass Sie richtig sind.

Beachten Sie diese Probleme bei nicht standardmäßigen Registerkarten:

- **Jeder Registerkarten Name sollte seinen Inhalt beschreiben.** Wählen Sie aussagekräftige Namen aus, die spezifisch sind, aber nicht zu spezifisch sind. Benutzer sollten nie durch ihren Inhalt überrascht sein.
- **Jeder Registerkarten Name sollte seinen Zweck widerspiegeln.** Sehen Sie sich das Ziel oder die Aufgabe an, die den Befehlen zugeordnet ist
- **Jeder Registerkarten Name sollte sich eindeutig von allen anderen Registerkarten Namen unterscheiden.**

Die Registerkarte Start ist eine Ausnahme von diesen Überlegungen. Obwohl Sie nicht über eine Registerkarte Home verfügen müssen, sollten Sie die meisten Programme ausführen. Die Registerkarte Start ist die erste Registerkarte, die die am häufigsten verwendeten Befehle enthält. Wenn Sie häufig Befehle verwenden, die nicht in die anderen Registerkarten passen, ist die Registerkarte Home die richtige Stelle für Sie.

Wenn Sie einen aussagekräftigen Namen für die Registerkarte nicht ermitteln können, liegt dies wahrscheinlich daran, dass die Registerkarte nicht gut entworfen wurde. Wenn Ihre Multifunktionsleisten-Organisation nicht funktioniert, überdenken Sie das Design der Registerkarte.

### <a name="groups"></a>Gruppen

Durch das Aufteilen von Befehlen in Gruppen werden die Befehle in zugehörige Mengen strukturiert. Die Gruppen Bezeichnung erläutert den allgemeinen Zweck der Befehle.

Es gibt eine Reihe von Faktoren, die beim Bestimmen von Gruppen und deren Präsentation zu berücksichtigen sind:

- **Standard Gruppierung.** Obwohl es bedeutende Unterschiede bei den Programm übergreifenden Befehlen gibt, gibt es [Standard Gruppen](#standard-ribbon-groups) , die in vielen Programmen gemeinsam sind. Wenn diese Befehle mit denselben Namen und ähnlichen Positionen angezeigt werden, verbessert sich die Auffindbarkeit erheblich.

| Richtig                                                                                      | Falsch                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| ![Bildschirm Abbildung von Zoom, getrennt von der Bearbeitungs Gruppe ](images/cmd-ribbons-image13.png)<br/>Die Gruppe "Bearbeitungsbefehle" enthält alle Bearbeitungsbefehle, enthält jedoch nicht den Zoom-Befehl.         | ![Screenshot von Zoom, der in der Bearbeitungs Gruppe enthalten ist ](images/cmd-ribbons-image14.png)<br/>Der Zoom Befehl ist kein Bearbeitungs Befehl, sondern befindet sich in der Bearbeitungs Gruppe. |

- **Granularität.** Einige Strukturen sind gut, aber eine zu hohe Struktur macht Befehle schwerer zu finden. Wenn die Gruppennamen generisch sind, haben Sie möglicherweise nicht genügend Granularität. Wenn Gruppen mit nur einem oder zwei Befehlen vorhanden sind, haben Sie wahrscheinlich zu viele (obwohl Sie über einen in-Ribbon-Katalog verfügen, ohne dass weitere Befehle innerhalb einer Gruppe vorhanden sind).

| Richtig                                                                                                 | Falsch                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![Bildschirm Abbildung von Zoom, getrennt von der Bearbeitungs Gruppe ](images/cmd-ribbons-image13.png)<br/> Die Gruppe "Bearbeitungsbefehle" enthält alle Bearbeitungsbefehle.| ![Screenshot der Bearbeitung der Gruppen Aufteilung in zwei Gruppen ](images/cmd-ribbons-image15.png)<br/>Die Gruppe "Bearbeitungsbefehle" wurde in Abschnitte aufgeteilt, die zu granulär sind. Vermeiden Sie Gruppen mit nur einem oder zwei Befehlen.|

- **Zeichen.** Gute Gruppennamen erläutern den Zweck ihrer Befehle. Wenn die Gruppennamen nicht sind, überdenken Sie den Namen oder die Gruppierung. Wenn Sie einen aussagekräftigen, beschreibenden Namen nicht ermitteln können, liegt dies wahrscheinlich daran, dass die Gruppe nicht gut entworfen wurde.

| Richtig                                                                                                 | Falsch                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![Screenshot der in vier Gruppen unterteilten Befehle ](images/cmd-ribbons-image17.png) <br/> Verwenden Sie Gruppennamen, die spezifisch genug sind, um die in der Gruppe enthaltenen Befehle zu beschreiben. | ![Screenshot der Format Gruppe mit mehreren Befehlen ](images/cmd-ribbons-image16.png) <br/> Dieser Gruppenname ist zu ungenau, um hilfreich zu sein. Ein besserer Ansatz besteht darin, diese Befehle in spezifischeren Gruppen zu organisieren. |

- **Reihenfolge.** Personen, die in der Reihenfolge von links nach rechts (in westlichen Kulturen) lesen, werden Sie vielleicht denken, dass Gruppen auf der linken Seite das auffälligste sind. Der hervorgehobene Registerkarten Name und der Fensterinhalt fungieren jedoch tendenziell als [Mittelpunkte](vis-layout.md), sodass Gruppen in der Mitte der Registerkarte in der Regel mehr Aufmerksamkeit als die linke Gruppe erhalten. Platzieren Sie die am häufigsten verwendeten Gruppen an den wichtigsten Orten, und stellen Sie sicher, dass für die Gruppen auf der Registerkarte ein logischer Fluss vorliegt.

![Screenshot der Zwischenablage Gruppe in ganz links ](images/cmd-ribbons-image18.png)

In diesem Beispiel sind die Schriftart-und Absatz Gruppen merkbarer als die Gruppe der Zwischenablage, da Sie beim Verschieben aus dem Dokument zuerst sehen.

![Screenshot der Überwachungsgruppe auf der Registerkarte "Review" ](images/cmd-ribbons-image19.png)

In diesem Beispiel erhält die nach Verfolgungs Gruppe die größte Aufmerksamkeit, da die markierte Registerkarte Überprüfung als Mittelpunkt fungiert.

- **Einheitlich.** Es kann schwierig sein, Befehle zu erkennen, wenn die Befehls Darstellung alle identisch aussieht. Das Verwenden von Symbolen mit unterschiedlichen Formen und Farben, Gruppen mit unterschiedlichen Formaten und Befehlen mit unterschiedlichen Größen erleichtert Benutzern das Erkennen von Befehls Gruppen. Befehle sollten eine einheitliche Größe aufweisen, wenn das Menüband auf die kleinere Größe herunterskaliert wird.

| Richtig | Falsch |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![Screenshot der Gruppe mit Symbolen mit unterschiedlichen Größen ](images/cmd-ribbons-image20.png)<br/>Verwenden Sie eine Vielzahl von Symbolgrößen, um die Erkennbarkeit zu verbessern.| ![Screenshot der Gruppe mit Symbolen gleicher Größen ](images/cmd-ribbons-image21.png)<br/>Diese Befehle sehen einander ähnlich aus, da Sie die gleiche Größe haben. |

### <a name="previews"></a>Vorschau

Sie können verschiedene Typen von Vorschauen verwenden, um anzuzeigen, was sich aus einem Befehl ergibt. Mithilfe hilfreicher Vorschau Versionen können Sie die Effizienz Ihres Programms verbessern und den Bedarf an Test-und Fehler Lernverfahren verringern. Live Previews laden auch experimentieren ein und fördern Kreativität.

Im folgenden finden Sie einige der verschiedenen Typen von Vorschau Versionen, die Sie verwenden können:

- **Realistische statische Symbole und Grafiken.** Statische Bilder, die einen realistischen Hinweis auf die Auswirkung eines Befehls enthalten. Diese können in Galerien, Dropdown Menüs und erweiterten Quick Infos verwendet werden.

![Screenshot der Dropdown Liste "Schriftart" ](images/cmd-ribbons-image22.png)

In diesem Beispiel zeigt die Dropdown Liste Schriftart jeden Schriftart Namen mithilfe der Schriftart an.

![Screenshot des Wasserzeichen-Miniatur Ansichts Katalogs ](images/cmd-ribbons-image23.png)

In diesem Beispiel werden realistische Miniaturansichten verwendet, um die verschiedenen Wasserzeichen anzuzeigen.

- **Dynamische Symbole und Grafiken.** Symbole und Grafiken, die geändert werden, um den aktuellen Zustand widerzuspiegeln. Solche Symbole sind besonders nützlich für Galerien und unterteilte Schaltflächen, die ihren Standardeffekt ändern, sodass Sie mit der letzten Aktion identisch sind.

![Screenshot des Katalogs "Absatz Stile" ](images/cmd-ribbons-image24.png)

In diesem Beispiel ändert Microsoft Word die Stile Gallery so, dass Sie die aktuellen Stile widerspiegelt.

![Screenshot der Befehls Schaltflächen für die Textformatierung ](images/cmd-ribbons-image25.png)

In diesem Beispiel ändert Word die Text Hervorhebungs Farbe und die Schriftart Farb Befehle, um den aktuellen Effekt anzugeben.

- **Live Vorschau.** Wenn Benutzer mit der Maus auf eine Formatierungs Option zeigen, zeigt die Live Vorschau an, wie die Ergebnisse mit dieser Formatierung aussehen würden. Live-Vorschaufunktionen helfen Benutzern, die Auswahl effizienter und zuverlässiger zu gestalten, basierend auf dem tatsächlichen Kontext des Benutzers.

![Screenshot der Befehls Farbauswahl für die Seiten Farbe ](images/cmd-ribbons-image26.png)

In diesem Beispiel führt der Befehl "page Color" eine Live Vorschau aus, indem die Auswirkung der Farboptionen auf "Hover" angezeigt wird.

Live-Vorschaufunktionen sind eine leistungsstarke Funktion, die die Produktivität Ihrer Benutzer wirklich verbessern kann, aber auch einfache statische Vorschau Versionen können eine große Hilfe sein.

### <a name="scaling-the-ribbon"></a>Skalieren des Menübands

Das Skalieren einer Symbolleiste ist einfach: Wenn ein Fenster zu schmal ist, um eine Symbolleiste anzuzeigen, zeigt die Symbolleiste an, was passt, und macht alles andere über eine Überlauf Schaltfläche zugänglich. Ein Ziel von Rich-Befehlen besteht darin, den verfügbaren Speicherplatz in vollem Umfang zu nutzen, sodass das Skalieren eines Menübands mehr Entwurfs Aufgaben erfordert. Es gibt keine Standardmenü Band Größe, daher sollten Sie kein Menüband mit einer bestimmten Breite entwerfen. Sie müssen Layouts mit einer breiten Palette von breiten entwerfen und feststellen, dass jedes dieser Elemente von den meisten Benutzern erkannt wird. Die Skalierung ist ein grundlegender Bestandteil des Menüband-Entwurfs, nicht der letzte Schritt. Beim Entwerfen einer Registerkarte geben Sie die verschiedenen Layouts für jede Gruppe an (bis zu drei) sowie die Kombinationen, die gleichzeitig verwendet werden können. Im Menüband wird die größte gültige Kombination angezeigt, die der aktuellen Fenstergröße entspricht.

![Screenshot der Format Befehle im Überlauf Menü ](images/cmd-ribbons-image27.png) Symbolleisten Skalieren mit einer Überlauf Schaltfläche.

![Screenshot von Menü Bändern mit unterschiedlichen breiten ](images/cmd-ribbons-image28.png) gibt es keine Standardmenü Band Größe. Die kleinste Größe ist ein einzelnes Popup Gruppensymbol.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

- **Kombinieren Sie keine Menü Bänder mit Menüleisten und Symbolleisten innerhalb eines Fensters.** Menü Bänder müssen anstelle von Menüleisten und Symbolleisten verwendet werden. Ein Menüband kann jedoch mit palettenfenstern und Navigationselementen kombiniert werden, wie z. b. die Schaltflächen "zurück" und "Vorwärts" und eine Adressleiste.
- **Kombinieren Sie immer ein Menüband mit einer Anwendungs Schaltfläche und einem schnell Zugriffs Symbol.**
- **Wählen Sie die Registerkarte Links (normalerweise Startseite) aus, wenn ein Programm gestartet wird.** Legen Sie die letzte ausgewählte Registerkarte nicht zwischen den Programm Instanzen persistent.
- **Hiermit wird das Menüband in seinem normalen Zustand (nicht minimiert) angezeigt, wenn ein Programm zum ersten Mal gestartet wird.** Benutzer lassen die Standardeinstellungen häufig unverändert, sodass es wahrscheinlich ist, dass alle Befehle weniger effizient sind, wenn Sie das Menüband beim Programmstart minimieren. Außerdem kann die Anzeige der anfänglich minimierten Multifunktionsleiste disorierend sein.
- **Sorgen Sie dafür, dass der Menüband-Status zwischen den Programm Instanzen** Wenn ein Benutzer beispielsweise das Menüband minimiert, sollte es beim nächsten Ausführen des Programms minimiert angezeigt werden. Lassen Sie die zuletzt ausgewählte Registerkarte jedoch auf diese Weise persistent speichern.

### <a name="using-tabs"></a>Verwenden von Registerkarten

Im Allgemeinen ist es besser, weniger Registerkarten zu haben, sodass Sie Registerkarten entfernen, die diese Ziele nicht erreichen.

- **Verwenden Sie bei Bedarf Standard Registerkarten.** Die Verwendung von Standard Registerkarten verbessert die Auffindbarkeit erheblich, insbesondere bei Programmen. Weitere Informationen finden Sie weiter unten in diesem Artikel auf den [Registerkarten Standard](#standard-ribbon-tabs)
- **Bezeichnen Sie ggf. die erste Tab-Taste.** Die Registerkarte Start sollte die am häufigsten verwendeten Befehle enthalten. Wenn Sie häufig Befehle verwenden, die nicht in die anderen Registerkarten passen, ist die Registerkarte Home die richtige Stelle für Sie.
- Fügen Sie eine neue Registerkarte hinzu, wenn:
  - **Seine Befehle sind stark auf bestimmte aufgabenbezogen und können von der Registerkarten Bezeichnung genau beschrieben werden.** Wenn Sie die Registerkarte hinzufügen, können Sie Ihre Befehle leichter finden und nicht erschweren.
  - **Seine Befehle sind größtenteils nicht mit Aufgaben auf anderen Registerkarten verknüpft.** Wenn Sie die Registerkarte hinzufügen, sollten Sie bei häufig ausgeführten Aufgaben nicht mehr Registerkarten
  - **Die Registerkarte verfügt über genügend Befehle, um die Verwendung eines zusätzlichen Orts zu rechtfertigen.** Sie haben keine Registerkarten mit nur wenigen Befehlen. **Ausnahme:** Fügen Sie ggf. eine Registerkarte mit einigen Befehlen hinzu, wenn diese stark mit einer bestimmten Aufgabe verknüpft sind. durch das Hinzufügen der Registerkarte wird eine übermäßig komplexe Start Registerkarte erheblich vereinfacht
- **Platzieren Sie für die verbleibenden Registerkarten zuerst die am häufigsten verwendeten Registerkarten, und behalten Sie die logische Reihenfolge auf den Registerkarten bei.**
- **Optimieren Sie den Registerkarten Entwurf, damit Benutzer schnell und zuverlässig Befehle finden.** Alle anderen Überlegungen sind sekundär.
- **Geben Sie keine Hilfe Registerkarte an.** Stellen Sie stattdessen Hilfe mithilfe der Programm weiten Hilfe und erweiterter Quick Infos bereit.
- **Verwenden Sie maximal sieben Kern Registerkarten.** Wenn mehr als sieben vorhanden sind, ist es schwierig, zu bestimmen, welche Registerkarte einen Befehl hat. Obwohl sieben Kern Registerkarten für Anwendungen mit vielen Befehlen akzeptabel sind, sollten die meisten Programme vier oder weniger Registerkarten als Ziel haben.

### <a name="contextual-tabs"></a>Kontextbezogene Registerkarten

- **Verwenden Sie eine Kontext Registerkarte, um eine Auflistung von Befehlen anzuzeigen, die nur relevant sind, wenn Benutzer einen bestimmten Objekttyp auswählen.** Wenn nur einige häufig verwendete Befehle vorhanden sind, ist es möglicherweise bequemer und stabiler, eine reguläre Registerkarte zu verwenden, und die Befehle einfach zu deaktivieren, wenn Sie nicht angewendet werden.
- ![Screenshot der Ausschneide-und Kopier Befehle ausgeblendet ](images/cmd-ribbons-image29.png)<br>Es ist besser, gängige Befehle wie Ausschneiden und kopieren zu deaktivieren, anstatt eine kontextabhängige Registerkarte zu verwenden.
- **Schließen Sie nur die Befehle ein, die für einen bestimmten Objekttyp spezifisch sind.** Fügen Sie Befehle nicht nur auf einer Kontext Registerkarte ein, wenn Benutzer Sie möglicherweise benötigen, ohne zuvor ein Objekt auszuwählen.
- **Einschließen der häufig verwendeten Befehle bei der Arbeit mit einem bestimmten Objekttyp.** Fügen Sie häufig verwendete allgemeine Kontextbezogene Befehle in Kontextmenüs und Mini Symbolleisten ein, um den Wechsel von Registerkarten bei häufig ausgeführten Aufgaben zu vermeiden. Sie können auch allgemeine Befehle redundant auf einer Kontext Registerkarte platzieren, wenn Sie hierdurch einen häufigen Tabulator Wechsel vermeiden. Überschreiben Sie dies jedoch nicht, und versuchen Sie nicht, jeden Befehl aufzunehmen, den ein Benutzer bei der Arbeit mit dem-Objekt benötigt.
- ![Screenshot des Rahmens-Befehls auf der Registerkarte "Entwurf" ](images/cmd-ribbons-image30.png)<br/>In diesem Beispiel ist der Befehl Rahmen auf der Registerkarte Entwurf enthalten, um häufige Registerkarten Wechsel bei häufig ausgeführten Aufgaben zu vermeiden.
- **Wählen Sie eine kontextabhängige Registerkarten Farbe aus, die sich von den aktuell angezeigten Kontext Registerkarten unterscheidet.** Die gleiche Registerkarte kann zu einem späteren Zeitpunkt mit einer anderen Farbe verwendet werden, um dies zu erreichen, aber versuchen Sie, möglichst konsistente Farbzuweisungen zu verwenden.
- Durch die **Auswahl einer Kontext Registerkarte** wird die Auffindbarkeit automatisch unterstützt, die Wahrnehmung der Stabilität wird verbessert, und die Notwendigkeit, Registerkarten zu wechseln Wählen Sie automatisch eine Kontext Registerkarte aus, wenn:
  - **Der Benutzer fügt ein Objekt ein.** Wählen Sie in diesem Fall die erste Kontext Registerkarte in der Gruppe aus.
  - **Der Benutzer doppelklickt auf ein Objekt.** Wählen Sie in diesem Fall die erste Kontext Registerkarte in der Gruppe aus.
  - **Der Benutzer hat eine Kontext Registerkarte ausgewählt, auf das Objekt geklickt und dann sofort auf ein Objekt desselben Typs geklickt.** Kehren Sie in diesem Fall zur zuvor ausgewählten Registerkarte "Kontext" zurück.
- Wenn Sie eine Kontext Registerkarte mit der Registerkarte **aktiv entfernen, legen Sie die Registerkarte Start oder die erste Registerkarte als aktive** Registerkarte fest. Dies wird am stabilsten angezeigt.

### <a name="modal-tabs"></a>Modale Registerkarten

- **Verwenden Sie eine modale Registerkarte, um eine Auflistung von Befehlen anzuzeigen, die für einen bestimmten temporären Modus gelten, und keine der Kern Registerkarten.** Wenn einige der Kern Registerkarten zutreffen, verwenden Sie stattdessen eine Kontext Registerkarte, und deaktivieren Sie die Befehle, die nicht angewendet werden. Da modale Registerkarten sehr eingeschränkt sind, sollten Sie nur verwendet werden, wenn es keine bessere Alternative gibt.
- ![Screenshot der Registerkarte "Druckvorschau" ](images/cmd-ribbons-image31.png)<br/>Die Seitenansicht ist eine häufig verwendete modale Registerkarte.
- **Um eine modale Registerkarte zu schließen, platzieren Sie den <mode> Befehl schließen als letzten Befehl auf der Registerkarte.** Verwenden Sie das Symbol "Schließen", damit der Befehl leicht zu finden ist. Legen Sie den Modus im Befehl ab, um Verwechslungen zu vermeiden, die geschlossen werden.
- ![Screenshot der Schaltfläche "Seitenansicht schließen" ](images/cmd-ribbons-image32.png)<br/>In diesem Beispiel werden beim expliziten bezeichnen des Close-Befehls mit dem-Modus Zweifel daran entfernt, was geschlossen wird.
- **Um eine modale Registerkarte zu schließen, müssen Sie auch die Schaltfläche Schließen auf der Titelleiste des Fensters neu definieren, um den Modus anstelle des Programms zu schließen.** Benutzer Tests haben gezeigt, dass viele Benutzer dieses Verhalten erwarten.

### <a name="standard-ribbon-tabs"></a>Standard Registerkarten

Ordnen Sie bei Bedarf die Befehle Ihres Programms diesen Standard Registerkarten zu, die in Ihrer Standard Reihenfolge angegeben sind.

#### <a name="regular-tabs"></a>Reguläre Registerkarten

- **Traum.** Enthält die am häufigsten verwendeten Befehle. Wenn Sie verwendet wird, ist Sie immer die erste Registerkarte.
- **Setze.** Enthält Befehle zum Einfügen von Inhalt und Objekten in ein Dokument. Wenn Sie verwendet wird, ist Sie immer die zweite Registerkarte.
- **Seitenlayout.** Enthält Befehle, die das Seitenlayout beeinflussen, einschließlich Themen, Seiten Einrichtung, Seiten Hintergründe, einzüden, Abstände und Positionierung. (Beachten Sie, dass sich die Einzug-und Abstands Gruppen stattdessen auf der Registerkarte Home befinden können, wenn ausreichend Platz vorhanden ist.) Wenn Sie verwendet wird, handelt es sich immer um die dritte Registerkarte.
- **Berichts.** Enthält Befehle zum Hinzufügen von Kommentaren, Nachverfolgen von Änderungen und Vergleichen von Versionen.
- **Anschauung.** Enthält Befehle, die sich auf die Dokument Ansicht auswirken, einschließlich Anzeigemodus, Anzeige/Ausblenden von Optionen, Zoomen, Fensterverwaltung und Makros die Befehle, die normalerweise in der Kategorie "Windows-Menü" gefunden wurden. Wenn Sie verwendet wird, ist dies die letzte reguläre Registerkarte, es sei denn, die Registerkarte Entwickler wird angezeigt
- **Trägers.** Enthält Befehle, die nur von Entwicklern verwendet werden. Wenn Sie verwendet wird, wird Sie standardmäßig ausgeblendet und die letzte reguläre Registerkarte, wenn Sie angezeigt wird.

Die meisten Programme benötigen die Registerkarten überprüfen und Entwickler nicht.

#### <a name="standard-contextual-tabs"></a>Standard mäßige Kontext Registerkarten

- **Ges.** Enthält Befehle, die sich auf das Ändern des Formats des ausgewählten Objekt Typs beziehen. Gilt normalerweise für einen Teil eines Objekts.
- **Ausge.** Enthält Befehle, die häufig in Galerien enthalten sind, um Stile auf den ausgewählten Objekttyp anzuwenden. Gilt normalerweise für das gesamte-Objekt.
- **Struktur.** Enthält Befehle, mit denen die Struktur eines komplizierten Objekts geändert werden kann, z. b. eine Tabelle oder ein Diagramm.

Wenn Sie über Kontext Befehle im Zusammenhang mit Format, Entwurf und Layout, aber nicht genug für mehrere Registerkarten verfügen, geben Sie einfach eine Format Registerkarte an.

### <a name="standard-groups"></a>Standard Gruppen

- **Verwenden Sie nach Möglichkeit Standard Gruppen.** Die Verwendung allgemeiner Befehle mit denselben Namen und ähnlichen Positionen verbessert die Auffindbarkeit erheblich. Weitere Informationen finden Sie weiter unten in diesem Artikel unter Standard-Menü [Band Gruppen](#standard-ribbon-groups)
- **Fügen Sie eine neue Gruppe hinzu** , wenn:
  - **Seine Befehle sind stark verwandt und können durch die Gruppen Bezeichnung genau beschrieben werden.** Wenn Sie die Gruppe hinzufügen, können Sie Ihre Befehle leichter finden, nicht schwieriger.
  - **Die Befehle der Befehle in anderen Gruppen weisen eine schwächere Beziehung auf.** Obwohl alle Befehle auf einer Registerkarte stark verknüpft sein sollten, sind einige Befehls Beziehungen stärker als andere.
  - **Die Gruppe verfügt über genügend Befehle, um zu begründen, dass Sie einen zusätzlichen Platz haben.** Zielen Sie 3-5-Befehle für die meisten Gruppen ab. Vermeiden Sie das vorhanden sein von Gruppen mit nur 1-2-Befehlen, obwohl ein in-Ribbon-Katalog ohne weitere Befehle innerhalb einer Gruppe zulässig ist. Wenn viele Gruppen mit einem einzigen Befehl vorhanden sind, wird eine zu große Struktur oder ein Mangel an Befehls Kohäsion vorgeschlagen.
- **Organisieren** Sie sich nicht durch Hinzufügen von Gruppen, in denen Sie nicht benötigt werden.
- **Erwägen Sie, eine Gruppe aufzuteilen** , wenn:
  - ![Screenshot der nicht in der Befehlsgruppe nicht geordneten Befehlsgruppe ](images/cmd-ribbons-image35.png)<br/>Die Gruppe verfügt über viele Befehle verschiedener Größen und benötigt Organisationen.
  - ![Screenshot von zwei langen Absatz Gruppennamen ](images/cmd-ribbons-image33.png)<br>Die Gruppe verfügt über Befehle, die von zusätzlichen Bezeichnungen sehr profitieren.
- **Platzieren Sie die am häufigsten verwendeten Gruppen an den wichtigsten Orten, und stellen Sie sicher, dass die Gruppen auf der Registerkarte logisch angeordnet sind.**
- **Optimieren Sie den Gruppen Entwurf, damit Benutzer schnell und zuverlässig Befehle finden.** Alle anderen Überlegungen sind sekundär.
- **Skalieren Sie keine Gruppen, die eine einzelne Schaltfläche enthalten, zu einem Popup Gruppensymbol.** Beim horizontalen Herunterskalieren lassen Sie diese als einzelne Schaltfläche aus.
- **Maximal sieben Gruppen verwenden.** Wenn mehr als sieben Gruppen vorhanden sind, ist es schwieriger, zu ermitteln, welche Gruppe einen Befehl hat.

### <a name="standard-ribbon-groups"></a>Standard-Menü Band Gruppen

Ordnen Sie die Befehle Ihres Programms diesen Standard Gruppen zu, die in Ihrer Standard Reihenfolge in ihren zugehörigen Registerkarten angegeben werden.

#### <a name="main-tab"></a>Haupt Registerkarte

- Zwischenablage
- Schriftart
- Paragraph
- Bearbeitung läuft

#### <a name="insert-tab"></a>Registerkarte Einfügen

- Tabellen
- Abbildungen

#### <a name="page-layout-tab"></a>Registerkarte Seitenlayout

- Designs
- Seiteneinrichtung
- Anordnen

#### <a name="review-tab"></a>Registerkarte Überprüfen

- Korrektur
- Kommentare

#### <a name="view-tab"></a>Registerkarte Ansicht

- Dokument Sichten
- Anzeigen/Ausblenden
- Zoom
- Fenster

### <a name="commands"></a>Befehle

- ![Screenshot des Befehls "Zeilennummern" auf dem Menüband ](images/cmd-ribbons-image36.png)<br/>**Profitieren Sie von der Auffindbarkeit und Skalierbarkeit von Multifunktionsleisten, indem Sie alle häufig verwendeten Befehle verfügbar machen.** Verschieben Sie ggf. häufig verwendete Befehle aus Dialogfeldern in das Menüband, insbesondere diejenigen, die bekanntermaßen schwer zu finden sind. Im Idealfall sollten Benutzer in der Lage sein, häufige Aufgaben auszuführen, ohne Dialogfelder zu verwenden.

- **Verwenden Sie die Skalierbarkeit von Menü Bändern nicht, um die unnötige Komplexität zu rechtfertigen.** Fortsetzen der Unterhaltung fügen Sie einem Menüband nur dann Befehle hinzu, wenn dies möglich ist. Sorgen Sie dafür, dass die gesamte Befehls Darstellung einfach ist. Im folgenden finden Sie Möglichkeiten zur Vereinfachung der Präsentation:
  - ![Screenshot der Mini Symbolleiste und des Kontextmenüs ](images/cmd-ribbons-image37.png)</br>**Verwenden Sie Kontextmenüs und Mini Symbolleisten für direkte und kontextabhängige Befehle.**
  - **Verschieben (oder beibehalten) selten verwendete Befehle in Dialogfeldern.** Verwenden Sie Dialogfeld-Launcher, um auf diese Befehle zuzugreifen. Dialogfelder können weiterhin mit Menü Bändern verwendet werden. Versuchen Sie einfach, Sie bei häufigen Aufgaben zu verwenden.
  - **Entfernen Sie redundante, selten verwendete Features.**

#### <a name="presentation"></a>Präsentation

- **Stellen Sie jeden Befehl nur auf einer Registerkarte dar. Vermeiden Sie mehrere Pfade zum gleichen Befehl, insbesondere dann, wenn der Befehl zum Aufrufen viele Klicks erfordert.** Es mag so aussehen, als wäre es sinnvoll, einen Befehl über mehrere Pfade zu finden. Denken Sie jedoch daran, dass Benutzer, die Sie suchen, nicht mehr suchen. Benutzer können davon ausgehen, dass der erste Pfad, den Sie finden, der einzige Pfad ist, bei dem es sich um ein schwerwiegendes Problem handelt, wenn dieser Pfad ineffizient ist. **Ausnahme:** Kontext Registerkarten können einige Befehle von den Registerkarten "Home" und "Einfügen" duplizieren, wenn dies verhindert, dass geänderte Registerkarten für gängige kontextbezogene Aufgaben
- **Fügen Sie die Befehle innerhalb einer Gruppe in ihre logische Reihenfolge ein, und geben Sie die am häufigsten verwendeten Befehle an.** Insgesamt sollten die Befehle einen logischen Flow aufweisen, damit Sie problemlos gefunden werden können, während die am häufigsten verwendeten Befehle zuerst angezeigt werden. Im Allgemeinen werden Befehle mit 32 x 32 Pixel Symbolen vor Befehlen mit 16x16 Pixel Symbolen angezeigt, um die übergreifende Überprüfung von Gruppen zu unterstützen.
- **Vermeiden Sie das Platzieren von destruktiven Befehlen neben häufig verwendeten Befehlen.** Ein Befehl gilt als destruktiv, wenn seine Auswirkung weit verbreitet ist und er entweder nicht einfach rückgängig gemacht werden kann oder der Effekt nicht sofort erkennbar ist.
- **Verwenden Sie Trennzeichen, um stark verwandte Befehle anzugeben, z. b. einen Satz von sich gegenseitig ausschließenden Optionen.**
- ![Screenshot der Schriftart-und Absatz Gruppen ](images/cmd-ribbons-image3.png)<br/> **Es empfiehlt sich, im Symbolleisten Stil Gruppen für Sätze stark verbundener, bekannter Befehle zu verwenden, die keine Bezeichnungen benötigen.** Auf diese Weise können Sie viele Befehle in einem kompakten Raum darstellen, ohne die Auffindbarkeit und das einfache lernen zu beeinträchtigen. Um so bekannt zu sein, werden solche Befehle häufig verwendet, sofort erkannt und sind daher tendenziell auf der Registerkarte "Home" zu finden.

- **Verwenden Sie für die am häufigsten verwendeten und wichtigsten beschrifteten Befehle 32 x 32 Pixel Symbole.** Wenn Sie eine Gruppe herunterskalieren, müssen Sie diese Befehle als letzte in 16x16-Pixel-Symbole konvertieren.
- **Vermeiden Sie eine willkürliche Befehls Platzierung.** Überprüfen Sie sorgfältig Ihren Registerkarten-und Gruppen Entwurf, um sicherzustellen, dass Benutzer keine Zeit für die Überprüfung der gewünschten Befehle aufwenden
- **Vermeiden Sie Marketing basierte Platzierung.** Marketing Ziele im Hinblick auf die herauf Stufung neuer Features ändern sich tendenziell im Laufe der Zeit. Sehen Sie sich zukünftige Versionen Ihres Produkts an und wie viel Frust eine ständig veränderliche Organisation verursachen wird.

#### <a name="interaction"></a>Interaktion

- **Deaktivieren Sie Befehle, die nicht auf den aktuellen Kontext angewendet werden oder direkt zu einem Fehler führen.** Verwenden Sie ggf. die [Erweiterte](glossary.md) QuickInfo, um zu erläutern, warum der Befehl deaktiviert ist. Blenden Sie solche Befehle nicht aus, da dies dazu führen kann, dass das Menüband Layout geändert wird
- **Aktualisieren Sie die Befehls Bezeichnungen nicht dynamisch.** Dies kann dazu führen, dass das Registerkarten Layout geändert wird, was zu einer instabilen Darstellung führt. Entwerfen Sie stattdessen Befehle so, dass Sie mit Konstanten Bezeichnungen funktionieren.

    | Richtig                                                                                       | Falsch                                                                 |
    |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | ![Screenshot des einfügenotiz-und Lösch Hinweises ](images/cmd-ribbons-image38.png)<br/> Deaktivieren von Befehlen, wenn Sie nicht verfügbar sind | ![Screenshot der einfügenotiz, kein Lösch Hinweis ](images/cmd-ribbons-image39.png)<br/>Befehle nicht ausblenden, auch wenn Sie nicht verfügbar sind |

- **Direkte Steuerelemente bevorzugen.** Ein Befehl ist direkt, wenn er mit einem einzigen Mausklick aufgerufen wird (d. h. ohne Navigation durch Menüs). Mit Ausnahme von in-Ribbon-Katalogen wird die Live Vorschau von direkten Steuerelementen nicht unterstützt, daher ist die Notwendigkeit der Live Vorschau ebenfalls ein Faktor.
- **Verwenden Sie die Live Vorschau** , um die Auswirkung der Optionen anzuzeigen, wenn ein Befehl eine Reihe verwandter Formatierungsoptionen umfasst und die Live Vorschau wichtig und praktikabel ist, insbesondere, wenn Benutzer wahrscheinlich die falsche Option auswählen.
  - Wenn der Befehl häufig verwendet wird, verwenden Sie für die directheit einen in-Ribbon-Katalog.
  - Wenn der Befehl nur selten verwendet wird, verwenden Sie einen Dropdown Katalog.
- Stellen Sie **direkte Befehle** mithilfe der folgenden Steuerelemente in der folgenden Reihenfolge der Präferenz bereit.
  - **Befehls Schaltflächen, Kontrollkästchen, Options Felder und direkte Kataloge.** Diese sind immer direkt.
  - **Trenn Schaltflächen.** Direkt für den häufigsten Befehl, aber indirekt für die Befehls Variationen.
  - **Menü Schaltflächen.** Dies sind indirekte, aber viele Befehle, die leicht zu finden sind.
  - **Text Felder (mit Dreh Steuerelementen).** Die Text Eingabe erfordert im Allgemeinen mehr Aufwand als die anderen Steuerelement Typen.
- ![Screenshot der Multifunktionsleiste mit nur Menü Schaltflächen ](images/cmd-ribbons-image42.png)</br>Wenn das Menüband hauptsächlich Menü Schaltflächen umfasst, wenn es in voller Größe angezeigt wird, können Sie auch eine Menüleiste verwenden.
- **Sofortige Befehle bevorzugen.** ![Screenshot der Schaltfläche "Druckteilen" und des zugehörigen Untermenüs ](images/cmd-ribbons-image43.png)<br/>Ein Befehl ist sofort, wenn er sofort wirksam wird (d. h. ohne Dialogfelder, um zusätzliche Eingaben zu erfassen). Wenn für einen Befehl eine Eingabe erforderlich ist, sollten Sie die Verwendung einer Trenn Schaltfläche, des unmittelbaren Befehls im Schaltflächen Bereich und der Befehle, die Eingaben erfordern, im Untermenü in Erwägung gezogen werden.

### <a name="galleries"></a>Kataloge

**Verwenden Sie [](glossary.md) einen** Katalog, wenn:

- **Es gibt einen klar definierten, zusammenhängenden Satz von Optionen, die Benutzer in der Regel auswählen.** Möglicherweise gibt es eine unbegrenzte Anzahl von Variationen, aber die wahrscheinliche Auswahl sollte gut enthalten sein. Wenn die Auswahl nicht stark verwandt ist, sollten Sie die Verwendung separater Kataloge in Erwägung gezogen.
- **Die Optionen werden am besten visuell ausgedrückt, z. b. Formatierungs Features.** Die Verwendung von Miniaturansichten vereinfacht das Durchsuchen, verstehen und Treffen von Optionen. Die Auswahl kann zwar gekennzeichnet werden, die Auswahl erfolgt jedoch visuell, und Text Bezeichnungen sollten nicht erforderlich sein, um die Auswahl zu verstehen.
- **Die Auswahl zeigt das Ergebnis, das sofort mit einem einzigen Mausklick erzielt wird.** Es sollte kein nach Verfolgungs Dialogfeld vorhanden sein, um die Absicht des Benutzers oder eine Reihe von Schritten zum Erreichen des angezeigten Ergebnisses genauer zu verdeutlichen. Wenn die Benutzer die Auswahl anpassen möchten, können Sie dies später tun.

**Verwenden Sie einen in-Ribbon-** Katalog, wenn:

- **Die Auswahlmöglichkeiten werden häufig verwendet.** Die Auswahlmöglichkeiten benötigen den Leerraum und den Speicherplatz, der potenziell von anderen Befehlen benötigt wird.
- **Für eine typische Verwendung ist es nicht erforderlich, die dargestellten Optionen zu gruppieren oder zu filtern.**
- **Die Auswahlmöglichkeiten können effektiv innerhalb der Höhe eines Menübands (48 Pixel) angezeigt werden.**

#### <a name="thumbnails-in-galleries"></a>Miniaturansichten in Galerien

**Wählen Sie die kleinste Miniatur** Ansichts Größe des Katalogs aus, die den Auftrag gut erfüllt.

- Verwenden Sie für in-Ribbon-Kataloge Miniaturansichten von 16x16, 48x48 oder 64x48 Pixel.
- Verwenden Sie für Dropdown Galerien Miniaturansichten von 16x16, 32x32, 48x48, 64x48, 72x96, 96x72, 96x96 oder 128 x 128 Pixel.
- Alle Galerie Elemente sollten dieselbe Miniatur Ansichts Größe aufweisen.

Für in-Ribbon-Kataloge:

- **Mindestens drei Optionen anzeigen: Weitere, wenn Platz vorhanden ist.** Wenn nicht genügend Speicherplatz zum Anzeigen von mindestens drei Optionen in der typischen Fenstergröße vorhanden ist, verwenden Sie stattdessen einen Dropdown Katalog.
- **Erweitern Sie in-Ribbon-Kataloge, um den verfügbaren Speicherplatz zu nutzen.** Verwenden Sie den zusätzlichen Bereich, um weitere Elemente anzuzeigen und Sie mit einem einzigen Mausklick leichter auszuwählen.

Für Dropdown Galerien:

- **Zeigen Sie den Katalog entweder über ein Kombinations Feld, eine Dropdown Liste, eine unterteilte Schaltfläche oder eine Menü Schaltfläche an.**
- **Wenn der Benutzer auf das Hauptfenster klickt, um den Dropdown Katalog zu schließen, schließen Sie einfach den Katalog, ohne den Inhalt des Hauptfensters auszuwählen oder zu ändern.**
- **Wenn ein Katalog viele Optionen enthält und einige Optionen selten verwendet werden, vereinfachen Sie den Standardkatalog, indem Sie sich auf die häufig verwendeten Optionen konzentrieren.** Geben Sie für die verbleibenden Befehle einen entsprechenden Befehl unten in der Dropdown-Dropdown-Galerie an.
  - Wenn der Befehl eine Liste mit weiteren Variationen anzeigt, nennen Sie Sie "More `singular feature name` options...".
  - Wenn der Befehl ein Dialogfeld anzeigt, in dem Benutzer ihre eigenen benutzerdefinierten Optionen erstellen können, nennen Sie es "Custom `feature name` ..."
- **Organisieren Sie die Auswahl in Gruppen, wenn Sie dies tun, um das Browsen effizienter zu gestalten.**
- ![Screenshot der Symbol Galerie und Filter ](images/cmd-ribbons-image44.png)<br/>**Wenn ein Katalog viele Elemente enthält, sollten Sie ggf. einen Filter hinzufügen, um Benutzern zu helfen, Entscheidungen effizienter zu finden.** Um Verwirrung zu vermeiden, sollten Sie den Katalog anfänglich ungefiltert anzeigen. Die meisten Kataloge sollten jedoch keinen Filter erfordern, da Sie nicht so viele Optionen aufweisen sollten und die Verwendung von Gruppen ausreichen sollte.

### <a name="command-previews"></a>Befehls Vorschau

- **Verwenden Sie Vorschauen, um die Auswirkung eines Befehls anzuzeigen, ohne dass Benutzer ihn zuerst ausführen müssen.** Durch die Verwendung hilfreicher Vorschau Versionen können Sie die Effizienz und das einfache erlernen Ihres Programms verbessern und die Notwendigkeit von Test-und Fehler Fehlern reduzieren. Informationen zu den verschiedenen Typen der Befehls Vorschau finden Sie im Abschnitt "Entwurfskonzepte [" in diesem](#previews) Artikel.
- **Stellen Sie bei Live-Vorschau Versionen sicher, dass die Vorschauversion angewendet und der aktuelle Zustand innerhalb von 500 Millisekunden wieder hergestellt werden kann.** Hierfür ist es erforderlich, dass Formatierungs Änderungen schnell und auf eine Weise angewendet werden können, die unter brechbar ist. Benutzer müssen in der Lage sein, unterschiedliche Optionen schnell für Live Vorschau zu evaluieren, um Ihre Vorteile zu nutzen.
- **Vermeiden Sie die Verwendung von Text in Vorschau Versionen.** Andernfalls müssen die Vorschaubilder lokalisiert werden.

### <a name="icons"></a>Symbole

- ![Screenshot der Dropdown Liste und der Kontrollkästchen ](images/cmd-ribbons-image45.png)<br/>**Stellen Sie Symbole für alle Menüband-Steuerelemente mit Ausnahme von Dropdown Listen, Kontrollkästchen und Options Feldern bereit.** Die meisten Befehle erfordern sowohl 32 x 32-als auch 16x16-Pixel-Symbole (nur 16x16 Pixel-Symbole werden von der Symbolleiste für den schnell Zugriff verwendet). Galerien verwenden normalerweise 16x16-, 48x48-oder 64x48 Pixel-Symbole.
- **Geben Sie eindeutige Symbole an.** Verwenden Sie nicht das gleiche Symbol für verschiedene Befehle.
- **Stellen Sie sicher, dass Menüband-Symbole für die Hintergrundfarbe des Menübands eindeutig sichtbar sind** Wertet die Menüband-Symbole immer im Kontext und im Modus mit hohem Kontrast aus.
- **Wählen Sie Symbol Entwürfe aus, die ihre Wirkung eindeutig vermitteln,** insbesondere für die am häufigsten verwendeten Befehle. Gut gestaltete Multifunktionsleisten verfügen Überselbst erklärende Symbole, mit denen Benutzer Befehle effizient finden und verstehen können.
- **Wählen Sie Symbole aus, die erkennbar und unterschieden werden können,** insbesondere für die am häufigsten verwendeten Befehle. Stellen Sie sicher, dass die Symbole über unterschiedliche Formen und Farben verfügen. Auf diese Weise können Benutzer die Befehle schnell finden, auch wenn Sie das symbolsymbol nicht merken.

    | Richtig                                                                                                 | Falsch                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![Screenshot von Blue Eye dropperzeichen und Gelber Stift ](images/cmd-ribbons-image46.png)<br/>Verwenden Sie Form und Farbe, um Symbole zu erstellen, die leicht zu unterscheiden sind. | ![Screenshot von Blue Eye dropperzeichen und blauem Stift ](images/cmd-ribbons-image47.png)<br/> Symbole mit derselben Farbe sind schwer zu unterscheiden.|

- ![Screenshot des Befehls "comments" im Popup Container ](images/cmd-ribbons-image48.png)<br/>**Erwägen Sie, Popup Gruppen Symbole zu erstellen, indem Sie das 16x16-Pixel-Symbol des prominentesten Befehls in der Gruppe in einem visuellen 32 x 32 Pixel-Container platzieren.** Sie müssen keine anderen Symbole für Popup Gruppen erstellen.
- ![Screenshot der Befehls Schaltflächen für die Textformatierung ](images/cmd-ribbons-image25.png)<br/>**Wenn nützlich, ändern Sie das Symbol, um den aktuellen Zustand widerzuspiegeln.** Dies ist besonders nützlich für unterteilte Schaltflächen, deren Standard Auswirkung geändert werden kann.
- **Stellen Sie sicher, dass die Menüband-Symbole den Aero-Style-Symbol Richtlinien entsprechen.** Menüband-Symbole werden jedoch direkt angezeigt, anstatt in der Perspektive angezeigt zu werden.

| Richtig                                                                                                 | Falsch                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![Screenshot von zweidimensionalen Befehls Symbolen ](images/cmd-ribbons-image49.png)<br/> Verwenden Sie zweidimensionale Symbole.|![Screenshot von dreidimensionalen Befehls Symbolen ](images/cmd-ribbons-image50.png)<br/> Verwenden Sie keine dreidimensionalen Symbole. |
 
### <a name="enhanced-tooltips"></a>Erweiterte Quick Infos

- **Alle Menü Band Befehle sollten erweiterte** Quick Infos aufweisen, um den Befehlsnamen, die Tastenkombination, die Beschreibung und optionale zusätzliche Informationen zu erhalten. Vermeiden Sie Quick Infos, die die Bezeichnung einfach erneut angeben.

    **Falsch:**

    ![Screenshot der QuickInfo, die den Befehlsnamen wiederholt ](images/cmd-ribbons-image51.png)

    In diesem Beispiel gibt die QuickInfo die Befehls Bezeichnung einfach erneut aus.

- **Wenn dies praktikabel ist, beschreiben Sie den Befehl vollständig mit einer kurzen Beschreibung.** Link zur Hilfe, wenn eine weitere Erläuterung wirklich erforderlich ist.

    **Falsch:**

    ![Screenshot der QuickInfo für den Befehl "Durchgestrichen" ](images/cmd-ribbons-image52.png)

    In diesem Beispiel benötigt der Befehl keine Hilfe.

- **Wenn dies hilfreich ist, veranschaulichen Sie die Auswirkungen des Befehls mithilfe einer Vorschau.**

    ![Screenshot der QuickInfo und des Diagramms für das einfügediagramm ](images/cmd-ribbons-image53.png)

    In diesem Beispiel veranschaulicht das QuickInfo-Bild die Auswirkungen des Befehls.

Informationen zu Bezeichnungs Richtlinien finden Sie unter Erweiterte QuickInfo- [Bezeichnungen](#enhanced-tooltips).

### <a name="access-keys-and-keytips"></a>Zugriffsschlüssel und KeyTips

KeyTips sind der Mechanismus, mit dem Zugriffsschlüssel für Befehle angezeigt werden, die direkt auf einem Menüband angezeigt werden.

Zugriffsschlüssel für Dropdown Menübefehle werden mit einem unterstrichenen Zeichen angegeben. Sie unterscheiden sich von den Menü Zugriffs Schlüsseln wie folgt:

- Es können zwei Zeichen Zugriffsschlüssel verwendet werden. Beispielsweise kann FP verwendet werden, um auf den Befehl "Format-Maler" zuzugreifen.
- Die Zugriffsschlüssel Zuweisungen werden mithilfe von Tipps anstelle von unterstrichen angezeigt, sodass die Zeichenbreite und die Nachfolger Elemente nicht zum Erstellen von Zuweisungen dienen.

- **Zuweisen von Zugriffs Schlüsseln zu allen Menüband-Registerkarten und-Befehlen.** Die einzige mögliche Ausnahme sind Befehle, die von Legacy-Add-ins stammen.
- **Anwendungs Schaltfläche und Symbolleiste für den schnell Zugriff:**
  - Weisen Sie der Anwendungs Schaltfläche F zu. Diese Zuweisung wird verwendet, weil die Anwendungs Schaltfläche mit dem herkömmlichen Menü der Datei Ähnlichkeit ist.
  - ![Screenshot der Befehls Tastatur Tipps in einem Menüband ](images/cmd-ribbons-image54.png)<br/>Weisen Sie für die Symbolleiste für den schnell Zugriff und die zuletzt verwendeten Dateilisten Zugriffsschlüssel numerisch zu.
- ![Screenshot mit KeyTips für Registerkarten ](images/cmd-ribbons-image55.png)<br/>**Für Registerkarten:**
  - H zu Startseite zuweisen.
  - Beginnen Sie mit den am häufigsten verwendeten Registerkarten, und weisen Sie den ersten Buchstaben der Bezeichnung zu.
  - Wählen Sie für alle Registerkarten, die dem ersten Buchstaben nicht zugewiesen werden können, eine Zeichenfolge oder einen Vokal in der Bezeichnung aus.
  - Für Programme, die zur Unterstützung von Menüleisten verwendet werden, ist es sinnvoll, die Zugriffsschlüssel Kompatibilität zu wahren. Vermeiden Sie den Zugriff auf Schlüssel aus den Legacy Menü Kategorien unterschiedliche Bedeutungen. Wenn die Legacy-Menüleisten Version eines Programms z. b. über ein Menü Bearbeiten verfügt, sollten Sie einen E-Access-Schlüssel auf der entsprechenden Registerkarte verwenden. Wenn keine äquivalente Registerkarte vorhanden ist, weisen Sie eine E-Access-Taste keiner Registerkarte zu, um Verwirrung zu vermeiden.
- ![Screenshot mit KeyTips für eine Multifunktionsleiste ](images/cmd-ribbons-image56.png)<br/>**Für Menü Band Befehle, Menüs und Untermenüs:**
  - Zuweisen von eindeutigen Tastenkombinationen auf einer Registerkarte Sie können Zugriffstasten Kombinationen in verschiedenen Registerkarten wieder verwenden.
  - Weisen Sie, wenn möglich, die Standard Zugriffsschlüssel für häufig verwendete Befehle zu. Weitere Informationen finden Sie in der [Tabelle mit Standard Zugriffs Schlüsseln](inter-keyboard.md).
  - Für andere Befehle:
    - Wählen Sie für die am häufigsten verwendeten Befehle am Anfang des ersten oder zweiten Worts der Bezeichnung Buchstaben aus, vorzugsweise den ersten Buchstaben.
    - Wählen Sie für weniger häufig verwendete Befehle Buchstaben aus, die eine unterschiedliche konsonante oder ein Vokal in der Bezeichnung sind, z. b. "x" in "Exit".
    - Verwenden Sie für die am häufigsten verwendeten Befehle und Dialogfeld-Launcher bei Bedarf zwei Buchstaben.
    - Verwenden Sie für Menüs und Untermenüs einen einzelnen Buchstaben, um die Anzahl von Tastatureingaben zu verringern, die für den Complete-Befehl erforderlich sind.
    - Verwenden Sie keine Zugriffsschlüssel, die mit J, Y oder Z beginnen, da Sie für kontextabhängige Registerkarten, nicht zugewiesene KeyTips und Popup Gruppen verwendet werden.
- ![Screenshot der KeyTips für Popup Gruppen ](images/cmd-ribbons-image58.png)<br/>**Für Popup Gruppen:**
  - Verwenden Sie einen aus zwei Buchstaben bestehenden Zugriffsschlüssel, der mit Z beginnt.
  - Beginnen Sie mit den am häufigsten verwendeten Gruppen, und weisen Sie dem ersten Buchstaben der Bezeichnung den zweiten Zugriffsschlüssel Buchstaben zu.
  - Wählen Sie für alle verbleibenden Gruppen einen unverwechselbaren Konsonanten oder einen Vokal in der Bezeichnung aus.

Wichtige Richtlinien für Tastenkombinationen finden Sie unter [Tastatur](inter-keyboard.md).

### <a name="application-buttons"></a>Anwendungs Schaltflächen

- **Verwenden Sie eine Anwendungs Schaltfläche, um ein Menü mit Befehlen anzuzeigen, die eine Datei oder eine Datei enthalten.** Beispiele hierfür sind Befehle, die im Menü Datei traditionell zum Erstellen, öffnen und Speichern von Dateien, zum Drucken und zum Senden und Veröffentlichen von Dokumenten wechseln.
- **Geben Sie bei Verwendung eines Menübands immer eine Anwendungs Schaltfläche an.** Wenn das Programm keine Dateien verwendet, verwenden Sie die Schaltfläche Anwendung, um auf die Programmoptionen und den Befehl exit zuzugreifen. Anwendungs Schaltflächen zeigen immer ein Befehlsmenü an, das nie nur dekorativ ist.
- **Verwenden Sie bei Bedarf die folgenden Menübefehle der Standardanwendung:**
  - Neu  
  - Öffnen  
  - Speichern  
  - Speichern unter...
  - Drucken...
  - Schnell Druck  
  - Seitenansicht  
  - Schließen  
  - Optionen  
  - Beenden  
  
- **Reservieren Sie Befehle, die nur für dieses Menü zum Menü Anwendung gehören.** Platzieren Sie Sie nicht redundant auf einer der Registerkarten.
- Geben Sie für jedes Menü Element Folgendes an:
  - **Eine Bezeichnung mit dem Befehlsnamen.**
  - **Ein 32 x 32 Pixel-Symbol.**
  - **Eine kurze Beschreibung.** Stellen Sie sicher, dass die Beschreibung mit höchstens zwei Textzeilen angezeigt werden kann.
- ![Screenshot der QuickInfo, die die Tastenkombination dokumentiert ](images/cmd-ribbons-image59.png)<br/>**Verwenden Sie Quick Infos, um die Tastenkombinationen zu dokumentieren.** Im Gegensatz zu normalen Menüs dokumentieren Anwendungs Menüs die Tastenkombinationen nicht mithilfe von Bezeichnungen.

### <a name="quick-access-toolbars"></a>Symbolleisten für den schnell Zugriff

- **Verwenden Sie die Symbolleiste für den schnell Zugriff, um Zugriff auf häufig verwendete Befehle bereitzustellen.** Die Befehle können von der Anwendungs Schaltfläche oder der Multifunktionsleiste aus erfolgen.
- **Stellen Sie bei Verwendung eines Menübands immer eine Symbolleiste für den schnell Zugriff bereit** Dies ist auch der Fall, wenn das Menüband eine einzelne Registerkarte hat. Dadurch wird die Konsistenz zwischen allen Programmen gewährleistet.
- **Füllen Sie die Symbolleiste für den schnell Zugriff vorab mit den häufig verwendeten Befehlen im Anwendungsmenü aus.** Stellen Sie speichern und rückgängig bereit, wenn Ihr Programm Sie unterstützt, und öffnen und drucken, falls unterstützt und häufig verwendet.
- **Geben Sie für das Menü Symbol für schnell Zugriff anpassen bis zu 12 der am häufigsten verwendeten unmittelbaren Befehle an.** Sofortige Befehle erfordern keine zusätzlichen Eingaben, bevor Sie wirksam werden, und sind daher für die Symbolleiste für den schnell Zugriff geeignet. Obwohl es sich dabei um beliebige unmittelbare Befehle handeln kann, bevorzugen Sie die Befehle, die sich nicht auf der Registerkarte "Home" befinden, da Benutzer wahrscheinlich diese auswählen.
- **Geben Sie für das Menü Symbol der Symbolleiste für den schnell Zugriff anpassen, wenn ein paar verwandter Befehle vorhanden ist, beides an, unabhängig von der Häufigkeit.** Gemeinsame Paare sind Open/Close, Back/Forward und Undo/Redo.
- **Geben Sie im Dialogfeld Symbolleiste für den schnell Zugriff anpassen eine Möglichkeit zum Hinzufügen eines beliebigen Befehls ein.** Stellen Sie einen gängigen Befehls Filter bereit, der die am häufigsten verwendeten Befehle anzeigt, und wählen Sie diesen Filter standardmäßig aus.

### <a name="dialog-box-launchers"></a>Dialog Feld-Launcher

- ![Screenshot der Schriftart (Dialogfeld) und Schriftart Gruppe ](images/cmd-ribbons-image60.png)<br/>**Stellen Sie eine Gruppe mit einem Dialogfeld-Start Programm bereit, wenn ein verwandtes Dialogfeld mit selten verwendeten Befehlen und Einstellungen vorhanden ist.** Das Dialogfeld sollte alle Befehle in der Gruppe sowie andere nicht vollkommen unterschiedliche Befehle oder dieselben Befehle wie die Gruppe enthalten.
- **Verwenden Sie kein Dialogfeld-Start Programm, um Befehle direkt auszuführen.** Ein Dialogfeld-Start Programm muss ein Dialogfeld anzeigen.
- **Verwenden Sie kein Dialogfeld-Start Programm für den Zugriff auf häufig verwendete Befehle und Einstellungen.** Im Vergleich zu Befehlen, die direkt auf dem Menüband angezeigt werden, sind die Dialogfeld Befehle und Einstellungen relativ nicht auffindbar.
- **Vergleichen Sie den Namen des Dialog Felds mit dem Namen der Gruppe.** Dabei muss es sich nicht um eine genaue Entsprechung handeln, aber die Namen sollten ähnlich genug sein, damit die Benutzer nicht von den Ergebnissen überrascht werden.

    **Falsch:**

    ![Screenshot des Erinnerungs Sounds (Dialogfeld) ](images/cmd-ribbons-image61.png)

    Obwohl es sich bei einem Erinnerungs Sound um eine Erinnerungs Option handelt, ist das Verwenden des Dialogfeld-Start Programms zum Festlegen des Erinnerungs Sounds unerwartet.

- **Hiermit werden nur die Befehle und Einstellungen angezeigt, die sich auf die Gruppe beziehen.** Wenn im Dialogfeld Weitere Aktionen angezeigt werden, können Benutzer möglicherweise darauf schließen, dass dieser Pfad zu diesen anderen Befehlen und Einstellungen der einzige Pfad ist.

    **Falsch:**

    ![Screenshot der Schriftart (Dialogfeld) ](images/cmd-ribbons-image62.png)

    In diesem Beispiel werden im Dialogfeld "Schriftart" Zeichen Abstandseinstellungen angezeigt, die nicht mit der zugehörigen Registerkarte verknüpft sind.

## <a name="labels"></a>Bezeichnungen

### <a name="tab-labels"></a>Registerkarten Bezeichnungen

- **Alle Registerkarten beschriften.**
- Verwenden Sie bei Bedarf **die Standard Registerkarten des Menübands**.
- **Bevorzugen Sie präzise, einfache Wort Bezeichnungen.** Obwohl die Bezeichnung mehrerer Wörter zulässig ist, benötigen Sie mehr Speicherplatz und sind schwieriger zu lokalisieren.
- **Wählen Sie aussagekräftige Registerkarten Namen aus, die ihren Inhalt eindeutig und präzise beschreiben.** Die Namen sollten spezifisch, jedoch nicht übermäßig spezifisch sein. Registerkarten Namen sollten vorhersehbar genug sein, damit die Benutzer nicht durch ihren Inhalt überrascht werden. Beachten Sie, dass die Registerkarte Home generisch benannt ist, da Sie für die am häufigsten verwendeten Befehle verwendet wird.
- Verwenden **Sie keine** Gruppennamen wie "Basic" und "Advanced". Benutzer müssen bestimmen, ob der gesuchte Befehl einfach oder erweitert ist.
- **Wählen Sie Registerkarten Namen aus, die ihren Zweck widerspiegeln** Beachten Sie die Ziele oder Aufgaben, die mit der Registerkarte verknüpft sind.
- **Wählen Sie Registerkarten Namen aus, die sich eindeutig von allen anderen Registerkarten Namen unterscheiden.**
- **Verwenden Sie für Registerkarten entweder Nomen oder Verben.** Für Registerkarten Namen ist kein paralleler Ausdruck erforderlich. Wählen Sie daher die beste Bezeichnung aus, unabhängig davon, ob es sich um ein Substantiv oder Verb handelt.
- **Verwenden Sie keine Gerundien** (Namen, die auf "-ung" enden). Verwenden Sie das Verb, von dem der partizipformen abgeleitet wird. (verwenden Sie z. b. "Draw" anstelle von "Drawing".)
- **Vermeiden Sie Registerkarten Namen mit denselben Anfangsbuchstaben, insbesondere benachbarte Registerkarten.** Wenn das Menüband herunterskaliert wird, haben diese Registerkarten Namen denselben abgeschnittene Text.
- **Einmalige Namen bevorzugen.** Sie können jedoch einen Lösch Namen verwenden, wenn der Singular Name umständlich ist.
- **Verwenden Sie die Groß-/Kleinschreibung.**
- **Verwenden Sie keine Interpunktion am Ende.**

### <a name="contextual-tab-and-tab-set-labels"></a>Kontext Registerkarte und Registerkarten Satz Bezeichnungen

- **Beenden Sie Kontext Registerkarten Sätze mit "Tools".** Dies erleichtert die Identifizierung des zwecks kontextbezogener Registerkarten.
- Verwenden Sie die Groß-/Kleinschreibung.
- Verwenden Sie keine Interpunktion am Ende.

### <a name="group-labels"></a>Gruppen Bezeichnungen

- **Bezeichnen Sie alle Gruppen** , es sei denn, die Gruppe verfügt über einen einzigen Befehl, und die Gruppen-und Befehls Bezeichnungen sind identisch.

- **Verwenden Sie die Standard-Menü Band Gruppen, wenn dies praktikabel ist.**
- **Bevorzugen Sie präzise, einfache Wort Bezeichnungen.** Obwohl die Bezeichnung mehrerer Wörter zulässig ist, benötigen Sie mehr Speicherplatz und sind schwieriger zu lokalisieren.
- **Wählen Sie sinnvolle Gruppennamen aus, die ihren Inhalt eindeutig und präzise beschreiben.** Die Namen sollten spezifisch und nicht generisch sein.
- **Wählen Sie Gruppennamen aus, die ihren Zweck widerspiegeln.** Beachten Sie die Ziele oder Aufgaben, die mit den Befehlen in der Gruppe verknüpft sind.
- **Vermeiden Sie die Verwendung von Gerundien** (Namen, die mit "-ung" enden). Sie können gerunds jedoch verwenden, wenn Sie das Verb verwenden, von dem der partizipformen abgeleitet ist, wäre es verwirrend. Verwenden Sie z. b. "Bearbeiten" und "Nachweis" anstelle von "Bearbeiten" und "Nachweis".
- **Verwenden Sie keine Gruppennamen, die mit den Namen von Registerkarten identisch sind.** Mit dem Registerkarten Namen, auf dem sich die Gruppe befindet, werden keine Informationen angezeigt, und die Verwendung des Namens einer anderen Registerkarte ist verwirrend.
- **Einmalige Namen bevorzugen.** Sie können jedoch einen Lösch Namen verwenden, wenn der Singular Name umständlich ist. 
- **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
- **Verwenden Sie keine Interpunktion am Ende.**

### <a name="command-labels"></a>Befehls Bezeichnungen

- **Alle Befehle bezeichnen.** Durch explizite Text Bezeichnungen können Benutzer Befehle suchen und verstehen. **Ausnahme:** Ein Befehl kann nicht beschriftet werden, wenn sein Symbol sehr gut bekannt ist und sich der Speicherplatz in einer Premium-Umgebung befindet. Höchstwahrscheinlich befinden sich nicht beschriftete Befehle auf der Registerkarte Home. Weisen Sie in diesem Fall die Name-Eigenschaft einer entsprechenden Text Bezeichnung zu. Dadurch können Hilfstechnologieprodukte, z. b. Bildschirm Sprachausgaben, Benutzern alternative Informationen zur Grafik bereitstellen.
- **Verwenden Sie für Befehls Schaltflächen eine präzise, selbsterklärende Bezeichnung.** Verwenden Sie, wenn möglich, ein einzelnes Wort; maximal vier Wörter.
- **Verwenden Sie für Dropdown Listen den aktuellen Wert als Bezeichnung, wenn die Liste immer über einen Wert verfügt.**
- ![Screenshot der Eingabeaufforderung für die Such Adressbücher ](images/cmd-ribbons-image67.png)<br/>Wenn eine [bearbeitbare Dropdown Liste](/windows/desktop/uxguide/ctrl-drop) keinen Wert hat, verwenden Sie eine [Eingabeaufforderung](glossary.md).
- **Dropdown Listen, die nicht selbsterklärend sind oder seltener verwendet werden, benötigen eine explizite Bezeichnung.** Setzen Sie einen Doppelpunkt am Ende der Bezeichnung.
- ![Screenshot von automatisch nach: \[ Sekunden \] ](images/cmd-ribbons-image69.png)<br. >**für Textfelder verwenden Sie eine explizite Bezeichnung.** Setzen Sie einen Doppelpunkt am Ende der Bezeichnung.
- **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.** Dies ist für den Windows- [Ton](text-style-tone.md)besser geeignet.
- **Starten Sie die Bezeichnung mit einem imperativen Verb.** es sei denn, es ist derselbe wie der Registerkarten-oder Gruppenname oder ein gängiges Verb wie anzeigen, erstellen, einfügen oder formatieren.
- **Verwenden Sie keine Interpunktion am Ende.**
- **Um Speicherplatz zu sparen, legen Sie keine Ellipsen auf Menüband-Befehls Bezeichnungen ab.** Allerdings werden Ellipsen von Befehlen in der Anwendungs Schaltfläche und in den Dropdown Menüs verwendet.

### <a name="enhanced-tooltip-labels"></a>Erweiterte QuickInfo-Bezeichnungen

- **Verwenden Sie den Titel, um ggf. den Befehlsnamen und die zugehörige Tastenkombination anzugeben.**
- **Verwenden Sie für den Titel nicht das endinterpunktions Zeichen.**
- **Starten Sie die Beschreibung mit einem Verb.** Verwenden Sie die Beschreibung, um Benutzern zu helfen, zu bestimmen, ob es sich um eine bestimmte Funktion handelt, nach der Sie suchen. Die Beschreibung sollte formuliert werden, um den Satz "Dies ist das richtige Feature, das Sie verwenden möchten..." abzuschließen.
- **Halten Sie die Beschreibung kurz.** Gelangen Sie direkt zu dem Punkt. Der lange Text verhindert das lesen.
-   ![Screenshot der Schaltfläche "teilen" und der zwei Quick Infos ](images/cmd-ribbons-image70.png)<br/>**Verwenden Sie für unterteilte Schaltflächen eine andere QuickInfo, um das Menü für die unterteilte Schaltfläche zu**
- **Verwenden Sie eine optionale zusätzliche Beschreibung, um zu erläutern, wie das-Steuerelement verwendet wird.** Dieser Text kann Informationen über den Zustand des Steuer Elements enthalten (einschließlich der Gründe für die Deaktivierung), wenn das Steuerelement selbst nicht den Zustand angibt. Halten Sie diesen Text kurz, und verwenden Sie ein Hilfethema für ausführlichere Erläuterungen.
- ![Screenshot der QuickInfo mit Grafik und Text ](images/cmd-ribbons-image71.png)**für die Beschreibung und ergänzende Beschreibung. verwenden Sie vollständige Sätze mit endinterpunktions Zeichen.**
- Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.

### <a name="application-button-labels"></a>Anwendungs Schaltflächen Bezeichnungen

- [Screenshot der Option "schnell Druck" ausgewählt ](images/cmd-ribbons-image72.png)<br/>**Verwenden Sie "schnell", um eine sofortige Version eines Befehls anzugeben.**

- **Verwenden Sie ein Auslassungs Zeichen, um anzugeben, dass für einen Befehl weitere Informationen erforderlich sind.**
- **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Menü Bänder:

- Weitere Informationen finden Sie in der Multifunktionsleiste und den zugehörigen Komponenten als Multifunktionsleiste, Registerkarten, Gruppen und Steuerelemente. Diese Begriffe werden nicht groß geschrieben.
- Sehen Sie sich die Schaltfläche Round als Anwendungs Schaltfläche und das Menü an, das Sie als Anwendungsmenü enthält.
- Weitere Informationen finden Sie auf der Symbolleiste.
- Verweisen Sie auf Registerkarten anhand ihrer Bezeichnungen und der Registerkarte Wort. Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-/Kleinschreibung
- Weitere Informationen finden Sie Unterbefehle anhand ihrer Bezeichnungen. Verweisen Sie auf nicht beschriftete Befehle anhand ihrer QuickInfo-Namen. Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, aber nicht die Auslassungs Zeichen. Schließen Sie die Word-Schaltfläche oder den Befehl nicht ein
- Um die Benutzerinteraktion zu beschreiben, verwenden Sie für Registerkarten und Steuerelemente klicken. Verwenden Sie die EINGABETASTE für bearbeitbare Dropdown Listen. Verwenden Sie SELECT, SELECT oder Pick nicht.
- Verweisen Sie auf nicht verfügbare Elemente als nicht verfügbar, nicht als abgeblendet, deaktiviert oder abgeblendet. Verwenden Sie in der Programmier Dokumentation deaktiviert.
- Formatieren Sie die Bezeichnungen nach Möglichkeit mithilfe von fettem Text. Andernfalls sollten Sie die Bezeichnungen nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiele:

- Klicken Sie auf der Registerkarte **Startseite** auf **Special einfügen**.
- Geben Sie auf der Registerkarte **Startseite** im Feld **Schriftart** den Text "Segoe UI" ein.
- Klicken Sie auf der Registerkarte **überprüfen** auf **Markup anzeigen**, und klicken Sie dann auf **Reviewer**.
- Klicken Sie auf der Registerkarte **Format** in **Bild Tools** auf **Bilder komprimieren**.