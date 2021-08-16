---
title: Menübänder
description: Menübänder sind die moderne Möglichkeit, Benutzern dabei zu helfen, Befehle effizient und direkt und direkt zu finden, zu verstehen und zu verwenden.\ 8212; mit einer Mindestanzahl von Klicks, ohne auf Test-und-Fehler-Anweisungen zurück greifen zu müssen, und ohne auf Hilfe zu verweisen.
ms.assetid: 8a4699da-9840-4622-9e94-d6d5c4e7708c
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: db5a64d50bd225b714c2ff0578145c47c66bedb557dd067e0cdf89f369178b1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118042556"
---
# <a name="ribbons"></a>Menübänder

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Menübänder sind die moderne Methode, um Benutzern dabei zu helfen, Befehle effizient und direkt mit einer minimalen Anzahl von Klicks zu finden, zu verstehen und zu verwenden. Dabei ist es weniger notwendig, auf Test-und-Fehler-Befehle zurück zu setzen, ohne auf Hilfe zu verweisen.

Ein Menüband ist eine Befehlsleiste, die die Funktionen eines Programms in einer Reihe von Registerkarten oben in einem Fenster organisiert. Die Verwendung eines Menübands erhöht die Aufmerkbarkeit von Features und Funktionen, ermöglicht ein schnelleres Lernen des gesamten Programms und sorgt dafür, dass Benutzer mehr Kontrolle über ihre Erfahrung mit dem Programm haben. Ein Menüband kann sowohl die herkömmliche Menüleiste als auch Symbolleisten ersetzen.

![Screenshot eines Menübands ](images/cmd-ribbons-image1.png)

Ein typisches Menüband.

Menübandregisterkarte besteht aus Gruppen, bei denen es sich um bezeichnete Befehle handelt, die eng miteinander verknüpft sind. Zusätzlich zu Registerkarten und Gruppen bestehen Menübänder aus:

- Eine Schaltfläche "Anwendung", die ein Menü mit Befehlen enthält, die ein Dokument oder einen Arbeitsbereich betreffen, z. B. dateibezogene Befehle.
- Eine Symbolleiste für den Schnellzugriff, bei der es sich um eine kleine, anpassbare Symbolleiste handelt, die häufig verwendete Befehle anzeigt.
- Kernregisterkarte sind die Registerkarten, die immer angezeigt werden.
- Kontextbezogene Registerkarten, die nur angezeigt werden, wenn ein bestimmter Objekttyp ausgewählt ist. Registerkarten, die immer angezeigt werden, werden als Kernregisterkarte bezeichnet.
- Ein Registerkartensatz ist eine Auflistung kontextbezogener Registerkarten für einen einzelnen Objekttyp. Da Objekte mehrere Typen haben können (z. B. ist ein Header in einer Tabelle mit einem Bild drei Typen), können mehrere kontextbezogene Registerkartensätze gleichzeitig angezeigt werden.
- Modale Registerkarten, bei denen es sich um Kernregisterkarten handelt, die mit einem bestimmten temporären Modus angezeigt werden, z. B. die Seitenansicht.
- Kataloge, bei denen es sich um Listen von Befehlen oder Optionen handelt, die grafisch dargestellt werden. Ein ergebnisbasierter Katalog veranschaulicht die Auswirkungen der Befehle oder Optionen anstelle der Befehle selbst. Ein Katalog im Menüband wird im Gegensatz zu einem Popupfenster in einem Menüband angezeigt.
- Erweiterte QuickInfos, die ihre zugeordneten Befehle präzise erläutern und die Tastenkombinationen verwenden. Sie können auch Grafiken und Verweise auf die Hilfe enthalten. Erweiterte QuickInfos reduzieren den Bedarf an befehlsbezogener Hilfe.
- Dialogfeldstarter, bei denen es sich um Schaltflächen am unteren Rand einiger Gruppen handelt, die Dialogfelder öffnen, die funktionen im Zusammenhang mit der Gruppe enthalten.

Menübänder wurden ursprünglich mit Microsoft Office 2007 eingeführt. Informationen dazu, warum Office menübands verwenden müssen und die vielen Probleme bei der Verwendung eines Menübands lösen müssen, finden Sie unter The Story of the Ribbon (Die Geschichte [des Menübands).](/archive/blogs/jensenh/the-story-of-the-ribbon)

> [!Note]  
> Richtlinien im Zusammenhang [mit Menüs,](cmd-menus.md) [](vis-icons.md) [Symbolleisten, Befehlsschaltflächen](cmd-toolbars.md)und Symbolen werden in separaten Artikeln dargestellt. [](ctrl-command-buttons.md)

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Berücksichtigen Sie die folgenden Fragen, um sich für die Verwendung eines Menübands zu entscheiden:

### <a name="program-type"></a>Programmtyp

- **Welche Art von Programm entwerfen Sie?** Der Programmtyp ist ein guter Indikator für die Geeignetheit eines Menübands. Menübänder funktionieren gut für Dokumenterstellungs- und -erstellungsprogramme sowie für Dokument-Viewer und Browser. Menübänder funktionieren möglicherweise für andere Arten von Programmen, aber andere Formen der Befehlspräsentation sind möglicherweise besser geeignet. Im Allgemeinen sollten einfache Programme über eine einfache Befehlspräsentation verfügen.

### <a name="discoverability-and-learning-issues"></a>Aufholbarkeits- und Lernprobleme

- **Haben Benutzer Probleme beim Suchen von Befehlen? Fordern Benutzer Features an, die bereits im Programm vorhanden sind?** In diesem Zusammenhang erleichtert die Verwendung eines Menübands die Suche nach Befehlen, indem selbsterklärende Bezeichnungen und eine Gruppierung verwandter Befehle verwendet werden. Die Verwendung eines Menübands wird auch besser skaliert als Menüleisten und Symbolleisten für zukünftiges Wachstum.
- **Haben Benutzer Probleme mit den Befehlen des Programms? Greifen sie häufig auf "Testversion und Fehler" zurück, um den richtigen Befehl auszuwählen oder zu bestimmen, wie Befehle funktionieren?** Wenn ja, ist die Verwendung eines Menübands mit ergebnisorientierten Befehlen, die auf Katalogen und Livevorschauen basieren, einfacher zu verstehen.

### <a name="command-characteristics"></a>Befehlsmerkmale

- **Werden die Befehle an mehreren Stellen angezeigt? Wenn Ihr Programm bereits vorhanden ist, werden Befehle in Menüleisten, Symbolleisten, Aufgabenbereichen und im Aufgabenbereich selbst angezeigt?** Wenn dies der Fehler ist, werden die Befehle mithilfe eines Menübands an einem zentralen Ort vereinheitlichen, sodass sie leichter zu finden sind.
- **Gelten die Befehle für das gesamte Fenster oder nur für bestimmte Bereiche?** Menübänder funktionieren am besten für Befehle, die für das gesamte Fenster oder für bestimmte Objekte gelten. In-place-Befehle funktionieren besser für einzelne Fensterfenster.
- **Können die meisten Befehle direkt angezeigt werden? Das heißt, können Benutzer mit nur einem Klick mit ihnen interagieren? Wenn häufig verwendete Befehle über Menüs und Dialogfelder aufgerufen werden, können sie dann so umgestaltet werden, dass sie direkt sind?** Während einige Befehle mithilfe von Menüs und Dialogfeldern angezeigt werden können, wird durch die Präsentation der meisten Befehle auf diese Weise die Effizienz eines Menübands beeinträchtigt, wodurch eine Menüleiste möglicherweise besser ausgewählt wird.

### <a name="command-scale"></a>Befehlsskalieren

- **Gibt es eine kleine Anzahl von Befehlen? Können die am häufigsten verwendeten Befehle problemlos auf einer einzelnen, einfachen Symbolleiste angezeigt werden?** Die Verwendung eines Menübands lohnt sich, wenn das Hinzufügen von Kern- und Kontextregisterkarte zu einer einfachen Registerkarte Start führt, die allein zum Ausführen der häufigsten Aufgaben verwendet werden kann. Wenn dies nicht der Der Vorteil der Verwendung eines Menübands ist, kann die zusätzliche Gewichtung für eine kleine Anzahl von Befehlen nicht rechtfertigen.
- **Gibt es eine große Anzahl von Befehlen? Erfordert die Verwendung eines Menübands mehr als sieben Registerkarten für Kerne? Müssten Benutzer ständig Registerkarten ändern, um allgemeine Aufgaben auszuführen?** Wenn ja, ist die Verwendung von Symbolleisten (für die keine Registerkarten geändert werden müssen) und Palettenfenster [(die](cmd-toolbars.md) möglicherweise das Ändern von Registerkarten erfordern, aber es können mehrere gleichzeitig geöffnet sein) eine effizientere Wahl.
- **Verwenden Benutzer in der Regel meist eine kleine Anzahl von Befehlen?** Wenn ja, können sie ein Menüband effizient verwenden, indem sie solche Befehle auf der Registerkarte Start eingeben. Wenn Registerkarten ständig geändert werden, wäre ein Menüband zu ineffizient.
- **Profitiert das Programm davon, den Inhaltsbereich des Programms so groß wie möglich zu gestalten?** Wenn ja, ist die Verwendung einer Menüleiste und einer einzelnen Symbolleiste effizienter als ein Menüband. Wenn ihr Programm jedoch drei oder mehr Zeilen mit Symbolleisten erfordert oder Aufgabenbereiche verwendet, ist die Verwendung eines Menübands effizienter.
- **Arbeiten Benutzer in der Regel über einen längeren Zeitraum in einem bestimmten Bereich innerhalb eines großen Fensters im Programm?** Wenn ja, profitieren sie von der nähe von Minisymbolleisten, Palettenfenstern und direkten Befehlen. Der Roundtrip vom Arbeitsbereich zum Menüband wäre zu ineffizient.
- **Müssen Benutzer aus Effizienz- und Flexibilitätssteigerungs-bzw. -flexibilitäts-bzw. -größenänderungen an den Inhalten der Befehlspräsentation, am Speicherort oder an der Größe vornehmen?** Wenn ja, sind anpassbare und erweiterbare Symbolleisten und Palettenfenster die bessere Wahl. Beachten Sie, dass einige Arten von Symbolleisten als Palettenfenster und Palettenfenster verschoben, angepasst und angepasst werden können.

Sehen Sie sich abschließend die letzte Frage an: Ist die Verbesserung der Aufstellbarkeit, der Einfachheit des Lernens, der Effizienz und der Produktivität die Kosten des zusätzlichen Platzes und die Notwendigkeit von Registerkarten zum Organisieren von **Befehlen wert?** Wenn ja, ist die Verwendung eines Menübands eine hervorragende Wahl. Wenn Sie sich nicht sicher sind, sollten Sie die Benutzerfreundlichkeit eines menübandbasierten Entwurfs testen und mit der besten Alternative vergleichen.

Menübänder sind eine neue und ansprechende Form der Befehlspräsentation und eine hervorragende Möglichkeit, ein Programm zu modernisieren. Aber so überzeugend sie auch sind, sie sind nicht die richtige Wahl für jedes Programm.

**Falsch:**

![Screenshot eines Menübands mit einem Rechner ](images/cmd-ribbons-image2.png)

Tun Sie dies nicht!

## <a name="seven-most-important-things"></a>Sieben wichtigste Dinge

1. Wählen Sie eine Befehlslösung aus, die für Ihren Programmtyp geeignet ist. Die Verwendung eines Menübands sollte dazu sorgen, dass sich ein Programm einfacher, effizienter und einfacher anfühlt, ohne das Gegenteil zu verwenden. Wenn die Verwendung eines Menübands nicht geeignet ist, sollten Sie stattdessen umfangreiche Befehle verwenden.  
2. Unterschätzen Sie nicht die Herausforderung, ein effektives Menüband zu erstellen. Erwarten Sie nicht, dass es sich dabei um einen einfachen Port Ihrer vorhandenen Menüleisten und Symbolleisten geht. Es ist nicht selbstverständlich, dass die Verwendung eines Menübands ihr Programm automatisch verbessert. Die Bereitschaft, die erforderliche Zeit und den Aufwand für eine Neugestaltung des Befehls zu verwenden, ist ein wichtiger Faktor bei der Entscheidung, ein Menüband zu verwenden.  
3. Machen Sie die Befehle erkennbar. Wählen Sie einen Registerkartenentwurf aus, der eine klare, offensichtliche, eindeutige Zuordnung zwischen Ihren Befehlen und den beschreibend bezeichneten Registerkarten enthält, in denen sie sich befinden. Benutzer sollten schnell und sicher ermitteln können, auf welcher Registerkarte der gesuchte Befehl angezeigt wird, und selten die falsche Registerkarte auswählen.  
4. Machen Sie die Befehle selbsterklärend. Benutzer sollten die Auswirkungen eines Befehls über seine Bezeichnung, das Symbol, die QuickInfo und die Vorschau verstehen. Sie sollten nicht experimentieren oder ein Hilfethema lesen müssen, um zu sehen, wie ein Befehl funktioniert.  
5. Effiziente Verwendung der Befehle:
    - Benutzer sollten die meiste Zeit auf der Registerkarte Startseite verbringen.
    - Benutzer sollten bei häufigen Aufgaben nur selten Registerkarten ändern müssen.
    - Wenn das Fenster maximiert ist und benutzer sich auf der richtigen Registerkarte befinden, haben die am häufigsten verwendeten Befehle die meisten visuellen Hervorhebungen, und Benutzer können sie mit einem einzigen Klick aufrufen. Benutzer können alle anderen Befehle auf der Registerkarte mit mindestens vier Klicks ausführen.
    - Benutzer sollten keine Dialogfelder öffnen müssen, um Befehle zu geben und Attribute in allgemeinen Aufgaben zu ändern.
6. Unterstützen Sie Benutzer bei der sicheren Auswahl von Befehlen und Optionen, und minimieren Sie die Notwendigkeit von Test- und Fehlerversuchen. Verwenden Sie nach Bedarf ergebnisorientierte Befehle, häufig in Form von Katalogen und Livevorschauen.  
7. Stellen Sie sicher, dass das Menüband von den größten Fenstergrößen bis zur kleinsten gut skaliert wird.  

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="adapting-a-ribbon-in-an-existing-program"></a>Anpassen eines Menübands in einem vorhandenen Programm

Sie können zwar einfach einen herkömmlichen Menüleisten- und Symbolleistenentwurf eines vorhandenen Programms in ein Menübandformat umgestalten, dabei fehlt jedoch der größte Teil des Werts der Verwendung eines Menübands. Menübänder haben den größten Nutzen, wenn sie verwendet werden, um sofortige, ergebnisorientierte Befehle darzustellen, häufig in Form von Katalogen und Livevorschau. Ergebnisorientierte Befehle erleichtern das Verständnis von Befehlen und die Produktivität von Benutzern. Anstatt Ihre vorhandenen Befehle umzugestalten, ist es besser, die Art und Weise, wie Befehle in Ihrem Programm ausgeführt werden, vollständig umzugestalten.

Überschätzen Sie nicht die Herausforderung, ein effektives Menüband zu erstellen. Und nehmen Sie nicht als selbstverständlich an, dass die Verwendung eines Menübands ihr Programm automatisch verbessert. Das Erstellen eines effektiven Menübands nimmt viel Zeit und Aufwand in Anspruch. Die Bereitschaft, die Zeit und den Aufwand zu übernehmen, die für die Umgestaltung eines solchen Befehls erforderlich sind, ist ein wichtiger Faktor bei der Entscheidung, ein Menüband zu verwenden.

### <a name="the-nature-of-ribbons"></a>Die Art von Menübändern

Im Vergleich zu herkömmlichen Menüleisten und Symbolleisten weisen Bänder die folgenden Merkmale auf:

- **Eine einzelne Benutzeroberfläche (UI) für alle Befehle.** Menüleisten sind umfassend und leicht zu erlernen, und Symbolleisten sind effizient und direkt, aber warum sollte nicht ein wenig mehr Bildschirmfläche verwendet werden, um eine benutzeroberfläche für einzelne Befehle zu erstellen, die all dies erreicht? Bei nur einer Benutzeroberfläche ist es für Menübänder nicht erforderlich, dass Benutzer herausfinden, welche Benutzeroberfläche über den gesuchten Befehl verfügt.
- **Sichtbar und selbsterklärend.** Menüleistenbefehle sind durch ihre Bezeichnungen selbsterklärend, werden aber meistens nicht angezeigt. Um Platz auf dem Bildschirm zu sparen, werden Symbolleistenschaltflächen in erster Linie durch Symbole anstelle von Bezeichnungen dargestellt (obwohl einige Symbolleistenschaltflächen beide verwenden), und hängen von QuickInfos ab, wenn das Symbol nicht selbsterklärend ist. Benutzer kennen die Symbole jedoch im Allgemeinen nur für die am häufigsten verwendeten Befehle.
- Durch die Darstellung der meisten Befehle mit beschrifteten Symbolen sind Menübandbefehle sowohl sichtbar als auch selbsterklärend und verwenden QuickInfos nur, um zusätzliche Informationen bereitzustellen. Es ist wenig erforderlich, an anderer Stelle zu wechseln (z. B. Hilfe), um einen Befehl zu verstehen.
- **Beschriftete Gruppierung.** Während Menükategorien beschriftet sind, sind Gruppen in einem Dropdownmenü nicht und werden nur mit einem Trennzeichen ohne Bezeichnung angezeigt. Gruppen in Symbolleisten werden auch mit nicht bezeichneten Trennzeichen gekennzeichnet.
- Durch das Organisieren von Befehlen in beschrifteten Gruppen erleichtern Menübänder die Suche nach Befehlen und deren Zweck.
- **Modal, aber nicht hierarchisch.** Menüleisten werden skaliert, indem eine Hierarchie von Befehlen erstellt wird. Menüs mit vielen Elementen können eine oder mehrere Untermenüebenen verwenden, um weitere Befehle bereitzustellen.
- Menübandbefehle benötigen mehr Platz als Symbolleistenbefehle, sodass sie Registerkarten zum Skalieren verwenden. Durch diese Verwendung von Registerkarten werden Menübänder modal, sodass Benutzer die Modi gelegentlich ändern müssen, um Befehle zu suchen. Innerhalb einer Registerkarte sind die meisten Befehle jedoch entweder direkt oder verwenden eine einzelne unterteilte Schaltfläche oder Menüschaltfläche, keine Hierarchie.
- **Direkt und sofort.** Ein Befehl ist direkt, wenn er mit einem einzigen Klick aufgerufen wird (d. b. ohne durch Menüs zu navigieren) und sofort, wenn er sofort wirksam wird (d. b. ohne Dialogfelder, um zusätzliche Eingaben zu erfassen). Menüleistenbefehle sind immer indirekt und oft nicht sofort. Wie Symbolleisten sind die meisten Menübandbefehle so konzipiert, dass sie direkt und direkt sind, wobei die am häufigsten verwendeten Befehle mit einem einzigen Klick aufgerufen werden und kein Dialogfeld erforderlich ist, um zusätzliche Eingaben zu erfassen.
- **Geräumig.** Menüleisten und Symbolleisten sind in erster Linie so konzipiert, dass sie platzeffizient sind. Um ihre Vorteile zu bieten, verbrauchen Menübänder möglicherweise mehr vertikalen Platz, was ungefähr der Entsprechung einer Menüleiste plus drei Zeilen von Symbolleisten entspricht. Da nur wenige Programme über drei oder mehr Symbolleistenzeilen verfügen, belegen Bänder in der Regel mehr Speicherplatz als herkömmliche UIs für Befehle.
- **Verfügt über die Schaltfläche Anwendung und die Symbolleiste für den Schnellzugriff.** Ein Menüband wird immer mit einer Anwendungsschaltfläche und einer Symbolleiste für den Schnellzugriff angezeigt. Auf diese Weise können Benutzer auf dateibezogene und häufig verwendete Befehle zugreifen, ohne Registerkarten zu ändern, und die Konsistenz über Programme hinweg fördern.
- **Minimale Anpassung.** Während Menüleisten eine feste Darstellung aufweisen, sind viele Symbolleisten recht anpassbar, sodass Benutzer Speicherorte, Größen und Inhalte festlegen können. Ein Menüband selbst ist nicht anpassbar, aber die Symbolleiste für den Schnellzugriff bietet eingeschränkte Anpassungsmöglichkeiten.
- **Verbesserte Tastatureingabe.** Menüleisten verfügen über einen hervorragenden Tastaturzugriff, da das Drücken der ALT-TASTE den Eingabefokus der Menüleiste direkt erhält. Es gibt jedoch keinen solchen Mechanismus für Symbolleisten, da sie die Tastaturnavigation mit dem Inhalt des Fensters gemeinsam nutzen. Folglich müssen Benutzer mithilfe der TAB-TASTE (die die letzte Tabstopptaste erhält) zur Symbolleiste navigieren und dann mithilfe der Pfeiltasten zu einem bestimmten Befehl navigieren.

Im Gegensatz dazu bieten Menübänder eine verbesserte Tastatureingabe über [Keytips,](glossary.md)in der Regel mit einem dreistufigen Prozess:

- Drücken Sie ALT, um in den KeyTip-Modus zu wechseln.
- Drücken Sie ein Zeichen, um eine Registerkarte, die Schaltfläche Anwendung oder einen Befehl in der Symbolleiste für den Schnellzugriff auszuwählen.
- Drücken Sie auf einer Registerkarte ein oder zwei Buchstaben, um einen Befehl auszuwählen.

    Dieser Ansatz ist sehr visuell. Außerdem ist sie flexibler, sodass sie besser skaliert werden kann und mehr mnemonische Zugriffsschlüsselzuweisungen erhalten.

    Verwechseln Sie Zugriffsschlüssel nicht mit Tastenkombinationen. Sowohl Zugriffstasten als auch Tastenkombinationen ermöglichen den Tastaturzugriff auf die Benutzeroberfläche, sie haben jedoch unterschiedliche Zwecke und Richtlinien. Weitere Informationen finden Sie unter [Tastatur](inter-keyboard.md).

### <a name="the-nature-of-rich-commands"></a>Die Art von umfangreichen Befehlen

Umfangreiche Befehle beziehen sich auf die Darstellung und Interaktion von Befehlen, die von Menübändern verwendet werden, ohne notwendigerweise einen Menübandcontainer zu verwenden. Umfangreiche Befehle weisen diese Merkmale auf:

- **Kennzeichnung.** Alle Befehle erhalten selbsterklärende Bezeichnungen, mit Ausnahmen nur, wenn die Symbole sehr bekannt sind und der Speicherplatz premium ist.

    **Richtig:**

    ![Screenshot eines Menübands für die Zeichenformatierung ](images/cmd-ribbons-image3.png)

    Diese Befehle sind äußerst bekannt, sodass sie keine Bezeichnungen benötigen.

    **Falsch:**

    ![Screenshot eines Menübands mit selten verwendeten Symbolen ](images/cmd-ribbons-image4.png)

    Diese unverständlichen Symbole erfordern Bezeichnungen für umfangreiche Befehle.

- **Größenanpassung.** Anstatt eine einheitliche Größe zu verwenden, werden Befehle relativ zu ihrer Häufigkeit der Verwendung und Wichtigkeit angepasst. Die am häufigsten verwendeten Befehle lassen sich nicht nur leichter finden und klicken, sondern sie sind auch [leichter zu berühren.](https://msdn.microsoft.com/library/windows/desktop/cc872774.aspx)

    ![Screenshot einer großen und drei kleinen Schaltfläche ](images/cmd-ribbons-image5.png)

    In diesem Beispiel ist die am häufigsten verwendete Schaltfläche größer als die anderen.

- **Dynamische Größen.** Umfangreiche Befehlssteuerelemente ändern die Größe selbst, um den verfügbaren Speicherplatz voll zu nutzen, anstatt eine feste Größe zu verwenden und entweder abgeschnitten oder einen Überlauf zu verwenden, wenn die Größe zu klein ist.

    ![Screenshot des breiten Menübands mit Schaltflächen gleicher Größe ](images/cmd-ribbons-image6.png)![Screenshot eines kleinen Menübands mit gemischten Schaltflächen ](images/cmd-ribbons-image7.png)

    In diesem Beispiel wird die Größe der Befehlsschaltflächen so geändert, dass sie im verfügbaren Bereich gut funktionieren.

- **Unterteilte Schaltflächen.** Geteilte Schaltflächen sind eine gute Möglichkeit, eine Reihe von Variationen eines Befehls bei Bedarf zu konsolidieren und gleichzeitig die Direktheit für den am häufigsten verwendeten Befehl beizubehalten.

    ![Screenshot des Befehls "Speichern unter" und der zugehörigen Optionen ](images/cmd-ribbons-image8.png)

    In diesem Beispiel verwendet der Befehl Speichern unter eine unterteilte Schaltfläche, bei der die Hauptschaltfläche die gängigste Variante ausführt und der Menüteil ein Menü mit Variationen des Befehls zeigt.

- **Umfangreiche Dropdownmenüs und Kataloge.** Dropdownmenüs, Dropdownlisten und Kataloge nehmen den Platz ein, den sie für die Kommunikation benötigen, und unterscheiden die Auswirkungen der Auswahl, häufig mithilfe von Grafiken und Textbeschreibungen. Kategorien werden verwendet, um große Mengen von Optionen zu organisieren.

    ![Screenshot der Dropdownmenüoptionen mit Symbolen ](images/cmd-ribbons-image9.png)

    In diesen Beispielen wird durch Klicken auf eine Menüschaltfläche eine Liste von Auswahlmöglichkeiten angezeigt, die ihre Auswirkungen anzeigen.

- **Livevorschau** Wenn der Benutzer auf eine Formatierungsoption zeigt, zeigt das Programm mithilfe des tatsächlichen Inhalts an, wie die Ergebnisse mit dieser Formatierung aussehen würden.

    ![Screenshot der Ergebnisse der Formatierungsoptionen ](images/cmd-ribbons-image10.png)

    Livevorschau zeigen die Ergebnisse der Anwendung einer Formatierungsoption beim Bewegen des Mauszeigers an.

- **Erweiterte QuickInfos.** Diese erläutern ihre zugeordneten Befehle präzise und geben die Tastenkombinationen an. Sie können auch Grafiken und Verweise auf Die Hilfe enthalten (obwohl sie die Notwendigkeit der befehlsbezogenen Hilfe weitgehend entfällt).

    ![Screenshot einer großen QuickInfo mit Text und Grafik ](images/cmd-ribbons-image11.png)

    Erweiterte QuickInfos erläutern die zugehörigen Befehle präzise.

Menübänder sind möglicherweise nicht für alle Programme geeignet, aber alle Programme können möglicherweise von umfangreichen Befehlen profitieren.

### <a name="ribbons-always-have-an-application-button-and-quick-access-toolbar"></a>Menübänder verfügen immer über eine Anwendungsschaltfläche und eine Symbolleiste für den Schnellzugriff.

Die Schaltfläche Anwendung und die Symbolleiste für den Schnellzugriff stellen Befehle zur Verfügung, die in jedem Kontext nützlich sind, wodurch das Ändern von Registerkarten reduziert wird. Obwohl diese drei Komponenten logisch unabhängig sind, muss ein Menüband immer über die Schaltfläche Anwendung und die Symbolleiste für den Schnellzugriff verfügen. Da Befehle entweder über das Menüband oder die Schaltfläche Anwendung ausgeführt werden können, fragen Sie sich möglicherweise, wo Befehle zu platzieren sind. Die Auswahl ist nicht willkürlich.

Die Schaltfläche Anwendung wird verwendet, um ein Menü mit Befehlen anzuzeigen, in denen etwas für eine Datei oder mit einer Datei ausgeführt wird, z. B. Befehle, die normalerweise im Menü Datei zum Erstellen, Öffnen und Speichern von Dateien, Drucken und Senden und Veröffentlichen von Dokumenten verwendet werden.

Im Gegensatz dazu ist das Menüband selbst für Befehle, die sich auf den Inhalt des Fensters auswirken. Beispiele hierfür sind Befehle, die zum Lesen, Ändern oder Verwenden des Inhalts oder zum Ändern der Ansicht verwendet werden.

Wenn Sie ein Menüband verwenden, müssen Sie auch eine Anwendungsschaltfläche verwenden, auch wenn Ihr Programm keine Dokumente oder Dateien enthält. Verwenden Sie in solchen Fällen das Menü Anwendung, um Befehle zum Drucken, Programmoptionen und Beenden des Programms anzuzeigen. Die Schaltfläche Anwendung ist für solche Programme zwar nicht erforderlich, aber ihre Verwendung sorgt für Programmkonsistenz. Benutzer müssen nicht nach Speichern und Rückgängig-Befehlen oder Programmoptionen suchen, da sie sich immer am gleichen Ort befinden.

Die Symbolleiste für den Schnellzugriff ist auch dann erforderlich, wenn das Menüband nur eine Registerkarte verwendet. Auch wenn solche Programme keine Symbolleiste für den Schnellzugriff benötigen (da alle Befehle bereits auf der einzelnen Registerkarte vorhanden sind), sorgt eine anpassbare Symbolleiste für den Schnellzugriff für Programmkonsistenz. Wenn Benutzer beispielsweise in der Lage sind, auf den Befehl Drucken zu klicken, sollten sie dies in jedem Programm tun können, das ein Menüband verwendet.

### <a name="organization-and-discoverability"></a>Organisation und Aufholbarkeit

Durch die Bereitstellung von Registerkarten und Gruppen können Sie mithilfe von Menübändern Ihre Befehle organisieren, um die Aufholbarkeit zu verbessern. Die Herausforderung besteht darin, dass die Aufmerkbarkeit der Organisation stark schaden kann, wenn sie schlecht gemacht wird. Es sollte eine klare, offensichtliche und eindeutige Zuordnung zwischen Ihren Befehlen und den beschreibend bezeichneten Registerkarten und Gruppen geben, in denen sie sich befinden.

Benutzer bilden ein mentales Modell des Menübands, nachdem sie es für eine Weile verwendet haben. Wenn dieses mentale Modell für Benutzer nicht sinnvoll, ineffizient oder falsch ist, führt dies zu Verwirrung und Frust. **Ihr wichtigstes Ziel beim Entwerfen eines Menübands besteht in der schnellen und sicheren Suche nach Befehlen. Wenn Sie dies nicht erreichen, ist ihr Menübandentwurf nicht verfügbar.** Um dieses Ziel zu erreichen, sind sorgfältiger Entwurf, Benutzertests und Iterationen erforderlich. Gehen Sie nicht davon aus, dass dies einfach sein wird.

Hier sind einige häufige Fehler zu vermeiden:

- **Vermeiden Sie generische Registerkarten- und Gruppennamen.** Ein guter Registerkarten- oder Gruppenname muss seinen spezifischen Inhalt genau beschreiben, vorzugsweise mithilfe der aufgaben- und zielbasierten Sprache. Vermeiden Sie generische Registerkarten- und Gruppennamen sowie technologiebasierte Namen. Beispielsweise könnte fast jeder Befehl in einem Dokument, das ein Dokument erstellt und erstellt, zu Registerkarten mit der Bezeichnung Bearbeiten, Formatieren, Tools, Optionen, Erweitert und Mehr gehören. Verlassen Sie sich auf bestimmte, beschreibende Bezeichnungen, nicht auf Merken.
- **Vermeiden Sie zu spezifische Registerkarten- und Gruppennamen.** Obwohl Registerkarten- und Gruppennamen spezifisch sein sollen, sollten sie nicht so spezifisch sein, dass Benutzer von ihren Inhalten überraschend sind. Benutzer suchen häufig nach Dingen, die den Prozess der Beseitigung verwenden, um zu verhindern, dass sie Ihre Registerkarten oder Gruppen übersehen, da der Name irreführend ist.
- **Vermeiden Sie mehrere Pfade zum gleichen Befehl, insbesondere wenn der Pfad unerwartet ist oder der Befehl viele Klicks zum Aufrufen erfordert.** Es mag praktisch erscheinen, einen Befehl über mehrere Pfade zu finden. Denken Sie jedoch daran, dass Benutzer nicht mehr suchen, wenn sie das suchen, was sie suchen. Es ist für Benutzer zu einfach, davon auszugehen, dass der erste Pfad, den sie finden, der einzige Pfad ist, der ein schwerwiegendes Problem darstellt, wenn dieser Pfad ineffizient oder unerwartet ist. Darüber hinaus wird es benutzern aufgrund doppelter Befehle schwieriger, andere Befehle zu finden, nach denen sie suchen.

![Screenshot des Befehls "Indirekter Pfad zu Rahmen" ](images/cmd-ribbons-image12.png)

In diesem Beispiel können Sie Absatzränder über den Befehl Seitenränder ändern, auch wenn auf der Registerkarte Startseite ein direkterer Pfad angezeigt wird. Wenn Benutzer, die nach Absatzrändern suchen, über diesen unerwarteten Pfad stürzten, könnten sie leicht davon ausgehen, dass dies der einzige Pfad ist.

- **Vermeiden Sie eine beliebige Befehlsplatzierung.** Angenommen, Sie denken, sie verfügen über ein gutes Registerkarten- und Gruppendesign, aber stellen Sie fest, dass mehrere Befehle einfach nicht passen. Wahrscheinlich ist ihr Registerkarten- und Gruppenentwurf nicht so gut, wie Sie denken, und Sie müssen ihn weiter optimieren. Lösen Sie dieses Problem nicht, indem Sie diese Befehle an den Ort setzen, zu dem sie nicht gehören. Wenn Sie dies tun, müssen Benutzer wahrscheinlich jede Registerkarte überprüfen, um sie zu finden, und dann sofort vergessen, wo sie sich befinden.
- **Vermeiden Sie marketingbasierte Platzierungen.** Angenommen, Sie verfügen über eine neue Version Ihres Programms, und Ihr Marketingteam möchte seine neuen Features wirklich bewerben. Es kann verlockend sein, sie auf die Registerkarte Startseite zu setzen, aber dies ist ein kostspieliger Fehler, wenn dies die allgemeine Aufholbarkeit schadet. Berücksichtigen Sie zukünftige Versionen Ihres Produkts und wie viel Frust eine sich ständig ändernde Organisation verursachen wird.

### <a name="tabs"></a>Registerkarten

Der beste erste Schritt besteht in der Überprüfung der [Standardregisterkarte des Menübands.](#standard-ribbon-tabs) Wenn die Befehle Ihres Programms natürlich den Standardregisterkarten entsprechen, sollten Sie Ihre Registerkartenorganisation auf diesen Standards stützen. Wenn die Befehle des Programms jedoch nicht natürlich zuordnen, versuchen Sie nicht, dies zu erzwingen. Ermitteln Sie eine natürlichere Struktur, und stellen Sie sicher, dass Sie viele Benutzertests durchführen, um sicherzustellen, dass sie richtig sind.

Berücksichtigen Sie bei nicht standardmäßigen Registerkarten die folgenden Probleme:

- **Jeder Registerkartenname sollte seinen Inhalt beschreiben.** Wählen Sie aussagekräftige Namen aus, die spezifisch, aber nicht zu spezifisch sind. Benutzer sollten nie von ihren Inhalten überraschend sein.
- **Jeder Registerkartenname sollte seinen Zweck widerspiegeln.** Betrachten Sie das Ziel oder die Aufgabe, die den Befehlen zugeordnet ist.
- **Jeder Registerkartenname sollte sich eindeutig von allen anderen Registerkartennamen unterscheiden.**

Die Registerkarte Start ist eine Ausnahme zu diesen Überlegungen. Sie müssen zwar nicht über eine Registerkarte Start verfügen, die meisten Programme sollten jedoch verwendet werden. Die Registerkarte Start ist die erste Registerkarte und enthält die am häufigsten verwendeten Befehle. Wenn Sie häufig Befehle verwendet haben, die nicht in die anderen Registerkarten passen, ist die Registerkarte Start der richtige Ort für sie.

Wenn Sie keinen aussagekräftigen, beschreibenden Registerkartennamen bestimmen können, liegt dies wahrscheinlich daran, dass die Registerkarte nicht gut entworfen wurde. Wenn Ihre Menübandorganisation einfach nicht funktioniert, sollten Sie ihren Registerkartenentwurf neu gestalten.

### <a name="groups"></a>Gruppen

Das Aufteilen von Befehlen in Gruppen strukturiert die Befehle in verwandte Sätze. Die Gruppenbezeichnung erläutert den allgemeinen Zweck ihrer Befehle.

Es gibt eine Vielzahl von Faktoren, die beim Bestimmen von Gruppen und ihrer Darstellung zu berücksichtigen sind:

- **Standardgruppen.** Es gibt zwar erhebliche Unterschiede bei befehlsübergreifenden Programmen, aber es gibt [Standardgruppen,](#standard-ribbon-groups) die in vielen Programmen üblich sind. Wenn diese Befehle mit den gleichen Namen und ähnlichen Speicherorten angezeigt werden, wird die Aufholbarkeit erheblich verbessert.

| Richtig                                                                                      | Falsch                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| ![Screenshot des Zooms getrennt von der Bearbeitungsgruppe ](images/cmd-ribbons-image13.png)<br/>Die Gruppe "Bearbeitungsbefehle" umfasst alle Bearbeitungsbefehle, jedoch nicht den Befehl Zoom.         | ![Screenshot des Zoomfaktors, der in der Bearbeitungsgruppe enthalten ist ](images/cmd-ribbons-image14.png)<br/>Der Befehl Zoom ist kein Bearbeitungsbefehl, befindet sich jedoch in der Bearbeitungsgruppe. |

- **Granularität.** Einige Strukturen sind gut, aber zu viele Strukturen erschweren die Suche nach Befehlen. Wenn die Gruppennamen generisch sind, verfügen Sie möglicherweise nicht über genügend Granularität. Wenn Es Gruppen mit jeweils nur einem oder zwei Befehlen gibt, ist wahrscheinlich zu viel (obwohl ein Katalog im Menüband ohne andere Befehle innerhalb einer Gruppe akzeptabel ist).

| Richtig                                                                                                 | Falsch                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![Screenshot des Zooms getrennt von der Bearbeitungsgruppe ](images/cmd-ribbons-image13.png)<br/> Die Gruppe "Befehle bearbeiten" umfasst alle Bearbeitungsbefehle.| ![Screenshot der Bearbeitungsgruppe, unterteilt in zwei Gruppen ](images/cmd-ribbons-image15.png)<br/>Die Bearbeitungsbefehlsgruppe wurde in Abschnitte aufgeteilt, die zu präzise sind. Vermeiden Sie Gruppen mit nur einem oder zwei Befehlen.|

- **Namen.** Gute Gruppennamen erläutern den Zweck ihrer Befehle. Wenn ihre Gruppennamen dies nicht sind, überprüfen Sie den Namen oder die Gruppierung. Wenn Sie keinen aussagekräftigen, beschreibenden Namen bestimmen können, liegt dies wahrscheinlich daran, dass die Gruppe nicht gut entworfen wurde.

| Richtig                                                                                                 | Falsch                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![Screenshot von Befehlen, unterteilt in vier Gruppen ](images/cmd-ribbons-image17.png) <br/> Verwenden Sie Gruppennamen, die spezifisch genug sind, um die in der Gruppe enthaltenen Befehle zu beschreiben. | ![Screenshot der Formatgruppe mit mehreren Befehlen ](images/cmd-ribbons-image16.png) <br/> Dieser Gruppenname ist zu ungenau, um hilfreich zu sein. Ein besserer Ansatz wäre, diese Befehle in spezifischere Gruppen neu zu organisieren. |

- **Bestellung.** Menschen lesen in einer Reihenfolge von links nach rechts (in älteren Kulturen), sodass Sie denken könnten, dass Gruppen ganz links am deutlichsten sind. Der hervorgehobene Registerkartenname und der Fensterinhalt fungieren jedoch tendenziell als [Fokuspunkte,](vis-layout.md)sodass Gruppen in der Mitte der Registerkarte in der Regel mehr Aufmerksamkeit erhalten als die gruppe ganz links. Platzieren Sie die am häufigsten verwendeten Gruppen an den prominentesten Stellen, und stellen Sie sicher, dass es einen logischen Ablauf für die Gruppen auf der Registerkarte gibt.

![Screenshot der Zwischenablagegruppe ganz links ](images/cmd-ribbons-image18.png)

In diesem Beispiel sind die Gruppen Schriftart und Absatz wahrnehmbarer als die Gruppe Zwischenablage, da sie das Erste sind, was das Auge sieht, wenn es aus dem Dokument nach oben bewegt wird.

![Screenshot der Nachverfolgungsgruppe auf der Registerkarte "Überprüfung" ](images/cmd-ribbons-image19.png)

In diesem Beispiel erhält die Gruppe Nachverfolgung teilweise die größte Aufmerksamkeit, da die hervorgehobene Registerkarte Überprüfen als Schwerpunkt fungiert.

- **Einheitlichkeit.** Es kann schwierig sein, Befehle zu erkennen, wenn die Befehlspräsentation alle gleich aussieht. Die Verwendung von Symbolen mit unterschiedlichen Formen und Farben, Gruppen mit unterschiedlichen Formaten und Befehlen mit unterschiedlichen Größen erleichtert Benutzern die Erkennung von Befehlsgruppen. Befehle sollten nur dann eine einheitliche Größe aufweisen, wenn das Menüband auf seine kleineren Größen herunterskaliert wird.

| Richtig | Falsch |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![Screenshot der Gruppe mit Symbolen unterschiedlicher Größe ](images/cmd-ribbons-image20.png)<br/>Verwenden sie eine Vielzahl von Symbolgrößen, um die Erkennung zu verbessern.| ![Screenshot der Gruppe mit Symbolen gleicher Größe ](images/cmd-ribbons-image21.png)<br/>Diese Befehle sehen zu ähnlich aus, da sie alle die gleiche Größe haben. |

### <a name="previews"></a>Vorschau

Sie können verschiedene Arten von Vorschauversionen verwenden, um anzuzeigen, was sich aus einem Befehl ergibt. Durch die Verwendung hilfreicher Vorschauversionen können Sie die Effizienz Ihres Programms verbessern und den Test- und Fehlerlernansatz reduzieren. Livevorschau laden auch zum Experimentieren ein und fördern die Kreativität.

Hier sind einige der verschiedenen Vorschautypen, die Sie verwenden können:

- **Realistische statische Symbole und Grafiken.** Statische Bilder, die einen realistischen Hinweis auf die Auswirkung eines Befehls liefern. Diese können in Katalogen, Dropdownmenüs und erweiterten QuickInfos verwendet werden.

![Screenshot der Dropdownliste "Schriftart" ](images/cmd-ribbons-image22.png)

In diesem Beispiel zeigt die Dropdownliste Schriftart jeden Schriftartnamen mit der Schriftart selbst an.

![Screenshot des Miniaturansichtskatalogs für Wasserzeichen ](images/cmd-ribbons-image23.png)

In diesem Beispiel werden realistische Miniaturansichten verwendet, um die verschiedenen Wasserzeichen anzuzeigen.

- **Dynamische Symbole und Grafiken.** Symbole und Grafiken, die geändert werden, um den aktuellen Zustand widerzuspiegeln. Solche Symbole sind besonders nützlich für Kataloge sowie für geteilte Schaltflächen, die ihren Standardeffekt so ändern, dass sie mit der letzten Aktion identisch sind.

![Screenshot des Katalogs für Absatzformate ](images/cmd-ribbons-image24.png)

In diesem Beispiel ändert Microsoft Word den Stilkatalog, um die aktuellen Stile widerzuspiegeln.

![Screenshot der Befehlsschaltflächen für die Textformatierung ](images/cmd-ribbons-image25.png)

In diesem Beispiel ändert Word die Befehle Text hervorhebungsfarbe und Schriftfarbe, um ihren aktuellen Effekt anzugeben.

- **Livevorschau** Wenn Benutzer auf eine Formatierungsoption zeigen, wird in der Livevorschau angezeigt, wie die Ergebnisse mit dieser Formatierung aussehen würden. Livevorschau unterstützen Benutzer dabei, die Auswahl basierend auf dem tatsächlichen Kontext des Benutzers effizienter und zuverlässiger zu treffen.

![Screenshot des Farbauswahlbefehls für die Seitenfarbe ](images/cmd-ribbons-image26.png)

In diesem Beispiel führt der Befehl Seitenfarbe eine Livevorschau durch, indem die Auswirkung der Farboptionen auf den Mauszeiger angezeigt wird.

Livevorschau sind ein leistungsstarkes Feature, das die Produktivität Ihrer Benutzer verbessern kann, aber selbst einfache statische Vorschauen können eine große Hilfe sein.

### <a name="scaling-the-ribbon"></a>Skalieren des Menübands

Das Skalieren einer Symbolleiste ist einfach: Wenn ein Fenster zu schmal ist, um eine Symbolleiste anzuzeigen, zeigt die Symbolleiste an, was passt, und macht alles andere über eine Überlaufschaltfläche zugänglich. Ein Ziel umfangreicher Befehle ist es, den verfügbaren Speicherplatz voll zu nutzen, sodass die Skalierung eines Menübands mehr Entwurfsarbeit erfordert. Es gibt keine Standardbandgröße, daher sollten Sie kein Menüband mit einer bestimmten Breite entwerfen. Sie müssen Layouts mit einer vielzahl von Breiten entwerfen und erkennen, dass eines der Layouts das sein kann, das den meisten Benutzern angezeigt wird. Die Skalierung ist ein grundlegender Bestandteil des Menübandentwurfs, nicht der letzte Schritt. Geben Sie beim Entwerfen einer Registerkarte die verschiedenen Layouts für jede Gruppe (bis zu drei) sowie die Kombinationen an, die zusammen verwendet werden können. Das Menüband zeigt die größte gültige Kombination an, die der aktuellen Fenstergröße entspricht.

![Screenshot der Formatbefehle im Überlaufmenü ](images/cmd-ribbons-image27.png) Symbolleisten skalieren mithilfe einer Überlaufschaltfläche.

![Screenshot von Menübändern mit verschiedenen Breiten ](images/cmd-ribbons-image28.png) Es gibt keine Standardbandgröße. Die kleinste Größe ist ein einzelnes Popupgruppensymbol.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

- **Kombinieren Sie keine Menübänder mit Menüleisten und Symbolleisten innerhalb eines Fensters.** Bänder müssen anstelle von Menüleisten und Symbolleisten verwendet werden. Ein Menüband kann jedoch mit Palettenfenstern und Navigationselementen kombiniert werden, z. B. den Schaltflächen Zurück und Vorwärts und einer Adressleiste.
- **Kombinieren Sie immer ein Menüband mit einer Anwendungsschaltfläche und der Symbolleiste für den Schnellzugriff.**
- **Wählen Sie die Registerkarte ganz links (in der Regel Start) aus, wenn ein Programm gestartet wird.** Sorgen Sie nicht dafür, dass die zuletzt ausgewählte Registerkarte über Programminstanzen hinweg beibehalten wird.
- **Zeigt das Menüband im normalen Zustand (nicht minimiert) an, wenn ein Programm zum ersten Mal gestartet wird.** Benutzer lassen die Standardeinstellungen häufig unverändert, sodass die Minimierung des Menübands beim Programmstart wahrscheinlich dazu führt, dass alle Befehle weniger effizient sind. Darüber hinaus kann das Anzeigen des anfänglich minimierten Menübands desorientierend sein.
- **Sorgen Sie dafür, dass der Menübandzustand über Programminstanzen hinweg beibehalten wird.** Wenn ein Benutzer beispielsweise das Menüband minimiert, sollte es beim nächsten Ausführen des Programms minimiert angezeigt werden. Lassen Sie die zuletzt ausgewählte Registerkarte jedoch nicht auf diese Weise erhalten.

### <a name="using-tabs"></a>Verwenden von Registerkarten

Im Allgemeinen ist es besser, weniger Registerkarten zu haben. Entfernen Sie daher Registerkarten, die nicht helfen, diese Ziele zu erreichen.

- **Verwenden Sie nach Möglichkeit Standardregisterkarten.** Die Verwendung von Standardregisterkarten verbessert die Auffindbarkeit erheblich, insbesondere programmübergreifend. Weitere Informationen finden Sie in den [Standardregisterkarten des Menübands](#standard-ribbon-tabs) weiter unten in diesem Artikel.
- **Beschriften Sie ggf. die erste Registerkarte Home.** Die Registerkarte Startseite sollte die am häufigsten verwendeten Befehle enthalten. Wenn Sie häufig Befehle verwendet haben, die nicht in die anderen Registerkarten passen, ist die Registerkarte Startseite der richtige Ort für sie.
- Fügen Sie eine neue Registerkarte hinzu, wenn:
  - **Die Befehle sind stark mit bestimmten Aufgaben verknüpft und können durch die Registerkartenbezeichnung genau beschrieben werden.** Das Hinzufügen der Registerkarte sollte dazu beitragen, die Suche nach Befehlen zu vereinfachen und nicht zu erschweren.
  - **Die Befehle stehen größtenteils nicht im Zusammenhang mit Aufgaben auf anderen Registerkarten.** Das Hinzufügen der Registerkarte sollte bei häufig ausgeführten Aufgaben nicht mehr Wechseln von Registerkarten erfordern.
  - **Die Registerkarte verfügt über genügend Befehle, um einen zusätzlichen Ort zum Suchen zu rechtfertigen.** Verwenden Sie keine Registerkarten mit nur wenigen Befehlen. **Ausnahme:** Erwägen Sie, eine Registerkarte mit einigen wenigen Befehlen hinzuzufügen, wenn sie stark mit einer bestimmten Aufgabe verknüpft sind, und das Hinzufügen der Registerkarte vereinfacht eine zu komplexe Registerkarte Start erheblich.
- **Platzieren Sie für die verbleibenden Registerkarten zuerst die am häufigsten verwendeten Registerkarten, und behalten Sie dabei eine logische Reihenfolge über die Registerkarten hinweg bei.**
- **Optimieren Sie den Registerkartenentwurf, sodass Benutzer befehle schnell und sicher finden.** Alle anderen Überlegungen sind sekundär.
- **Geben Sie keine Registerkarte Hilfe an.** Stellen Sie stattdessen Unterstützung bereit, indem Sie programmweite Hilfe und erweiterte QuickInfos verwenden.
- **Verwenden Sie maximal sieben Kernregisterkarten.** Wenn mehr als sieben vorhanden sind, ist es schwierig zu bestimmen, welche Registerkarte über einen Befehl verfügt. Während sieben Kernregisterkarten für Anwendungen mit vielen Befehlen akzeptabel sind, sollten die meisten Programme auf vier oder weniger Registerkarten abzielen.

### <a name="contextual-tabs"></a>Kontextbezogene Registerkarten

- **Verwenden Sie eine kontextbezogene Registerkarte, um eine Sammlung von Befehlen anzuzeigen, die nur relevant sind, wenn Benutzer einen bestimmten Objekttyp auswählen.** Wenn nur wenige, häufig verwendete Befehle vorhanden sind, ist es möglicherweise bequemer und stabiler, eine reguläre Registerkarte zu verwenden und Befehle einfach zu deaktivieren, wenn sie nicht angewendet werden.
- ![Screenshot der Ausschneide- und Kopierbefehle abgeblendet ](images/cmd-ribbons-image29.png)<br>Es ist besser, allgemeine Befehle wie Ausschneiden und Kopieren zu deaktivieren, als eine kontextbezogene Registerkarte zu verwenden.
- **Schließen Sie nur die Befehle ein, die für einen bestimmten Objekttyp spezifisch sind.** Legen Sie Befehle nicht nur auf einer kontextbezogenen Registerkarte ab, wenn Benutzer sie möglicherweise benötigen, ohne zuvor ein Objekt auszuwählen.
- **Schließen Sie die Befehle ein, die häufig beim Arbeiten mit einem bestimmten Objekttyp verwendet werden.** Setzen Sie häufig verwendete allgemeine kontextbezogene Befehle in Kontextmenüs und Minisymbolleisten, um das Wechseln von Registerkarten während häufig ausgeführter Aufgaben zu vermeiden. Alternativ können Sie auch erwägen, allgemeine Befehle redundant auf einer kontextbezogenen Registerkarte zu verwenden, wenn dadurch häufiges Wechseln von Registerkarten vermieden wird. Aber übertreiben Sie dies nicht. Versuchen Sie nicht, jeden Befehl einzubeziehen, den ein Benutzer beim Arbeiten mit dem Objekt möglicherweise benötigt.
- ![Screenshot des Rahmenbefehls auf der Entwurfsregisterkarte ](images/cmd-ribbons-image30.png)<br/>In diesem Beispiel ist der Befehl Rahmen auf der Registerkarte Entwurf enthalten, um häufiges Wechseln von Registerkarten während häufig ausgeführter Aufgaben zu vermeiden.\
- **Wählen Sie eine Kontextregisterkartenfarbe aus, die sich von den aktuell angezeigten kontextbezogenen Registerkarten unterscheidet.** Die gleiche Registerkartenmenge kann zu einem späteren Zeitpunkt mit einer anderen Farbe angezeigt werden, um dies zu erreichen. Versuchen Sie jedoch, nach Möglichkeit konsistente Farbzuweisungen über Aufrufe hinweg zu verwenden.
- **Die Auswahl einer kontextbezogenen Registerkarte** hilft automatisch bei der Auffindbarkeit, verbessert die Wahrnehmung der Stabilität und reduziert die Notwendigkeit zum Wechseln von Registerkarten. Wählen Sie automatisch eine kontextbezogene Registerkarte aus, wenn:
  - **Der Benutzer fügt ein -Objekt ein.** Wählen Sie in diesem Fall die erste kontextbezogene Registerkarte in der Gruppe aus.
  - **Der Benutzer doppelklickt auf ein Objekt.** Wählen Sie in diesem Fall die erste kontextbezogene Registerkarte in der Gruppe aus.
  - **Der Benutzer hat eine kontextbezogene Registerkarte ausgewählt, auf das Objekt geklickt und dann sofort auf ein Objekt desselben Typs geklickt.** Kehren Sie in diesem Fall zur zuvor ausgewählten kontextbezogenen Registerkarte zurück.
- **Wenn Sie eine kontextbezogene Registerkarte entfernen, die die aktive Registerkarte ist, machen Sie die Registerkarte Start oder die erste Registerkarte zur aktiven Registerkarte.** Dies erscheint am stabilsten.

### <a name="modal-tabs"></a>Modale Registerkarten

- **Verwenden Sie eine modale Registerkarte, um eine Sammlung von Befehlen anzuzeigen, die für einen bestimmten temporären Modus gelten, und keine der Kernregisterkarten wird angewendet.** Wenn einige der Kernregisterkarten angewendet werden, verwenden Sie stattdessen eine kontextbezogene Registerkarte, und deaktivieren Sie die Befehle, die nicht angewendet werden. Da modale Registerkarten sehr begrenzt sind, sollten sie nur verwendet werden, wenn es keine bessere Alternative gibt.
- ![Screenshot der Registerkarte "Druckvorschau" ](images/cmd-ribbons-image31.png)<br/>Die Seitenansicht ist eine häufig verwendete modale Registerkarte.
- **Um eine modale Registerkarte zu schließen, legen Sie den Befehl Schließen <mode> als letzten Befehl auf der Registerkarte ab.** Verwenden Sie das Symbol Schließen, um den Befehl leicht zu finden. Geben Sie den Modus im Befehl an, um Verwirrung darüber zu vermeiden, was geschlossen wird.
- ![Screenshot der Schaltfläche "Druckvorschau schließen" ](images/cmd-ribbons-image32.png)<br/>In diesem Beispiel wird durch die explizite Bezeichnung des Befehls Schließen mit dem Modus jeder Zweifel daran beseitigt, was geschlossen wird.
- **Um eine modale Registerkarte zu schließen, definieren Sie auch die Schaltfläche Schließen auf der Titelleiste des Fensters neu, um den Modus anstelle des Programms zu schließen.** Benutzertests haben ergeben, dass viele Benutzer dieses Verhalten erwarten.

### <a name="standard-ribbon-tabs"></a>Registerkarten des Standardmenübands

Ordnen Sie nach Möglichkeit die Befehle Ihres Programms diesen Standardregisterkarten zu, die in der Standarddarstellungsreihenfolge angegeben sind.

#### <a name="regular-tabs"></a>Reguläre Registerkarten

- **Startseite.** Enthält die am häufigsten verwendeten Befehle. Bei Verwendung ist dies immer die erste Registerkarte.
- **Einfügen.** Enthält Befehle zum Einfügen von Inhalt und Objekten in ein Dokument. Bei Verwendung ist dies immer die zweite Registerkarte.
- **Seitenlayout.** Enthält Befehle, die sich auf das Seitenlayout auswirken, einschließlich Designs, Seiteneinrichtung, Seitenhintergrund, Einzug, Abstand und Positionierung. (Beachten Sie, dass sich die Einzugs- und Abstandsgruppen stattdessen auf der Registerkarte Start befinden können, wenn genügend Platz vorhanden ist.) Bei Verwendung ist dies immer die dritte Registerkarte.
- **Bewertung.** Enthält Befehle zum Hinzufügen von Kommentaren, Nachverfolgen von Änderungen und Vergleichen von Versionen.
- **ansehen.** Enthält Befehle, die sich auf die Dokumentansicht auswirken, einschließlich Ansichtsmodus, Optionen zum Ein-/Ausblenden, Zoomen, Fensterverwaltung und Makros, die üblicherweise in der Menükategorie Windows gefunden werden. Bei Verwendung ist dies die letzte reguläre Registerkarte, es sei denn, die Registerkarte Entwickler wird angezeigt.
- **Entwickler.** Enthält Befehle, die nur von Entwicklern verwendet werden. Wenn sie verwendet wird, wird sie standardmäßig ausgeblendet, und die letzte reguläre Registerkarte wird angezeigt.

Die meisten Programme benötigen die Registerkarten Überprüfen und Entwickler nicht.

#### <a name="standard-contextual-tabs"></a>Standardkontextregisterkarten

- **Format.** Enthält Befehle zum Ändern des Formats des ausgewählten Objekttyps. Gilt in der Regel für einen Teil eines Objekts.
- **Design.** Enthält Befehle, häufig in Katalogen, um Stile auf den ausgewählten Objekttyp anzuwenden. Gilt in der Regel für das gesamte Objekt.
- **Layout.** Enthält Befehle zum Ändern der Struktur eines komplizierten Objekts, z. B. einer Tabelle oder eines Diagramms.

Wenn Sie kontextbezogene Befehle im Zusammenhang mit Format, Entwurf und Layout haben, aber nicht für mehrere Registerkarten ausreichen, geben Sie einfach eine Registerkarte Format an.

### <a name="standard-groups"></a>Standardgruppen

- **Verwenden Sie nach Möglichkeit Standardgruppen.** Wenn allgemeine Befehle mit den gleichen Namen und ähnlichen Speicherorten angezeigt werden, wird die Auffindbarkeit erheblich verbessert. Weitere Informationen finden Sie in den [Standardbandgruppen](#standard-ribbon-groups) weiter unten in diesem Artikel.
- **Fügen Sie eine neue Gruppe hinzu,** wenn:
  - **Die Befehle sind stark verknüpft und können von der Gruppenbezeichnung genau beschrieben werden.** Das Hinzufügen der Gruppe sollte dazu beitragen, die Suche nach Befehlen zu vereinfachen und nicht zu erschweren.
  - **Die Befehle weisen eine schwächere Beziehung zu den Befehlen in anderen Gruppen auf.** Während alle Befehle auf einer Registerkarte stark verknüpft sein sollten, sind einige Befehlsbeziehungen stärker als andere.
  - **Die Gruppe verfügt über genügend Befehle, um zu rechtfertigen, dass ein zusätzlicher Ort zum Suchen vorhanden ist.** Zielen Sie für die meisten Gruppen auf 3 bis 5 Befehle ab. Vermeiden Sie Gruppen mit nur 1 bis 2 Befehlen, obwohl ein Katalog im Menüband ohne andere Befehle innerhalb einer Gruppe akzeptabel ist. Das Verwenden vieler Gruppen mit einem einzigen Befehl deutet auf eine zu große Struktur oder fehlende Befehlsaufforderung hin.
- **Führen Sie keine Überorganisation** durch, indem Sie Gruppen hinzufügen, für die sie nicht benötigt werden.
- **Erwägen Sie das Aufteilen einer Gruppe,** wenn:
  - ![Screenshot der nicht organisierten Befehlsgruppe ](images/cmd-ribbons-image35.png)<br/>Die Gruppe verfügt über viele Befehle unterschiedlicher Größe und erfordert Organisation.
  - ![Screenshot von zwei langen Absatzgruppennamen ](images/cmd-ribbons-image33.png)<br>Die Gruppe verfügt über Befehle, die stark von zusätzlichen Bezeichnungen profitieren.
- **Platzieren Sie die am häufigsten verwendeten Gruppen an den prominentesten Stellen, und stellen Sie sicher, dass es eine logische Reihenfolge für die Gruppen auf der Registerkarte gibt.**
- **Optimieren Sie den Gruppenentwurf, sodass Benutzer schnell und sicher Befehle finden.** Alle anderen Überlegungen sind sekundär.
- **Skalieren Sie Gruppen, die eine einzelne Schaltfläche enthalten, nicht auf ein Popupgruppensymbol.** Lassen Sie sie beim herunterskalieren als einzelne Schaltfläche.
- **Verwenden Sie maximal sieben Gruppen.** Wenn mehr als sieben Gruppen vorhanden sind, wird es schwieriger zu bestimmen, welche Gruppe über einen Befehl verfügt.

### <a name="standard-ribbon-groups"></a>Standardbandgruppen

Ordnen Sie die Befehle Ihres Programms nach Möglichkeit diesen Standardgruppen zu, die auf den zugeordneten Registerkarten in der Standarddarstellungsreihenfolge angegeben werden.

#### <a name="main-tab"></a>Registerkarte "Main"

- Zwischenablage
- Schriftart
- Paragraph
- Bearbeitung läuft

#### <a name="insert-tab"></a>Registerkarte Einfügen

- Tabellen
- Abbildungen

#### <a name="page-layout-tab"></a>Registerkarte "Seitenlayout"

- Teilziele
- Seiteneinrichtung
- Anordnen

#### <a name="review-tab"></a>Registerkarte "Überprüfen"

- Korrektur
- Kommentare

#### <a name="view-tab"></a>Registerkarte Ansicht

- Dokumentansichten
- Anzeigen/Ausblenden
- Zoom
- Fenster

### <a name="commands"></a>Befehle

- ![Screenshot des Befehls "Zeilennummern" im Menüband ](images/cmd-ribbons-image36.png)<br/>**Nutzen Sie die Auffindbarkeit und Skalierbarkeit von Menübändern, indem Sie alle häufig verwendeten Befehle verfügbar machen.** Verschieben Sie bei Bedarf häufig verwendete Befehle aus Dialogfeldern in das Menüband, insbesondere solche, die bekanntermaßen schwer zu finden sind. Im Idealfall sollten Benutzer in der Lage sein, allgemeine Aufgaben ohne Dialogfelder auszuführen.

- **Verwenden Sie nicht die Skalierbarkeit von Menübändern, um unnötige Komplexität zu rechtfertigen.** Fahren Sie mit der Übung fort, fügen Sie einem Menüband keine Befehle hinzu, nur weil Sie dies tun können. Halten Sie die allgemeine Befehlserfahrung einfach. Im Folgenden finden Sie Möglichkeiten, die Präsentation zu vereinfachen:
  - ![Screenshot der Minisymbolleiste und des Kontextmenüs ](images/cmd-ribbons-image37.png)</br>**Verwenden Sie Kontextmenüs und Minisymbolleisten für direkt kontextbezogene Befehle.**
  - **Verschieben (oder Beibehalten) selten verwendeter Befehle in Dialogfeldern.** Verwenden Sie Dialogfeldstarter, um auf diese Befehle zuzugreifen. Sie können weiterhin Dialogfelder mit Menübändern verwenden. Versuchen Sie einfach, die Notwendigkeit zu reduzieren, sie während allgemeiner Aufgaben zu verwenden.
  - **Beseitigen sie redundante, selten verwendete Features.**

#### <a name="presentation"></a>Präsentation

- **Zeigen Sie jeden Befehl nur auf einer Registerkarte an. Vermeiden Sie mehrere Pfade zum gleichen Befehl, insbesondere, wenn für den Befehl viele Klicks erforderlich sind.** Es scheint praktisch zu sein, einen Befehl über mehrere Pfade zu finden. Denken Sie jedoch daran, dass Benutzer nicht mehr suchen, wenn sie das gesuchte Suchen finden. Es ist für Benutzer zu einfach, davon auszugehen, dass der erste Pfad, den sie finden, der einzige Pfad ist, der ein schwerwiegendes Problem darstellt, wenn dieser Pfad ineffizient ist. **Ausnahme:** Kontextbezogene Registerkarten können einige Befehle aus den Registerkarten Start und Einfügen duplizieren, wenn dadurch das Ändern von Registerkarten für allgemeine kontextbezogene Aufgaben verhindert wird.
- **Legen Sie innerhalb einer Gruppe die Befehle in ihrer logischen Reihenfolge ab, während Sie den am häufigsten verwendeten Befehlen den Vorrang geben.** Insgesamt sollten die Befehle über einen logischen Flow verfügen, damit sie leicht zu finden sind, während immer noch die am häufigsten verwendeten Befehle zuerst angezeigt werden. Im Allgemeinen werden Befehle mit 32 x 32 Pixel-Symbolen vor Befehlen mit 16 x 16 Pixel-Symbolen angezeigt, um das Gruppenübergreifende Scannen zu unterstützen.
- **Vermeiden Sie es, destruktive Befehle neben häufig verwendeten Befehlen zu platzieren.** Ein Befehl gilt als destruktiv, wenn seine Auswirkung weit verbreitet ist und entweder nicht einfach rückgängig zu machen ist oder der Effekt nicht sofort erkennbar ist.
- **Verwenden Sie Trennzeichen, um stark verwandte Befehle anzugeben, z. B. eine Reihe von sich gegenseitig ausschließenden Optionen.**
- ![Screenshot von Schriftart- und Absatzgruppen ](images/cmd-ribbons-image3.png)<br/> **Erwägen Sie die Verwendung von Gruppen im Symbolleistenstil für Sätze stark verwandter, bekannter Befehle, die keine Bezeichnungen benötigen.** Auf diese Weise können Sie viele Befehle in einem kompakten Bereich darstellen, ohne die Auffindbarkeit und das einfache Lernen zu beeinträchtigen. Um so bekannt zu sein, werden solche Befehle häufig verwendet, sofort erkannt und befinden sich daher in der Regel auf der Registerkarte Start.

- **Verwenden Sie 32 x 32 Pixel-Symbole für die am häufigsten verwendeten und wichtigsten bezeichneten Befehle.** Wenn Sie eine Gruppe herunterskalieren, legen Sie diese Befehle als letzte fest, um sie in Symbole mit 16 x 16 Pixeln zu konvertieren.
- **Vermeiden Sie willkürliche Befehlsplatzierung.** Denken Sie sorgfältig an ihren Registerkarten- und Gruppenentwurf, um sicherzustellen, dass Benutzer nicht zeitaufwendige Überprüfungen auf jeder Registerkarte ausführen, um den gewünschten Befehl zu finden.
- **Vermeiden Sie marketingbasierte Platzierung.** Marketingziele für die Heraufstufung neuer Features ändern sich tendenziell im Laufe der Zeit. Berücksichtigen Sie zukünftige Versionen Ihres Produkts und wie viel Frust eine sich ständig ändernde Organisation verursachen wird.

#### <a name="interaction"></a>Interaktion

- **Deaktivieren Sie Befehle, die nicht für den aktuellen Kontext gelten oder direkt zu einem Fehler führen würden.** Falls hilfreich, verwenden Sie die [erweiterte QuickInfo,](glossary.md) um zu erläutern, warum der Befehl deaktiviert ist. Blenden Sie solche Befehle nicht aus, da dies dazu führen kann, dass sich das Menübandlayout ändert, wodurch die Menübandpräsentation instabil wird.
- **Aktualisieren Sie Befehlsbezeichnungen nicht dynamisch.** Dies kann wiederum dazu führen, dass sich das Registerkartenlayout ändert, was zu einer instabilen Darstellung führt. Entwerfen Sie stattdessen Befehle so, dass sie mit konstanten Bezeichnungen funktionieren.

    | Richtig                                                                                       | Falsch                                                                 |
    |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | ![Screenshot der Einfüge- und Löschnotiz ](images/cmd-ribbons-image38.png)<br/> Deaktivieren von Befehlen, wenn sie nicht verfügbar sind | ![Screenshot der Einfügenotiz, kein Löschhinweis ](images/cmd-ribbons-image39.png)<br/>Befehle nicht ausblenden, auch wenn sie nicht verfügbar sind |

- **Direkte Steuerelemente bevorzugen.** Ein Befehl ist direkt, wenn er mit einem einzigen Klick aufgerufen wird (d. b. ohne Menüs zu navigieren). Mit Ausnahme von Katalogen im Menüband unterstützen direkte Steuerelemente jedoch keine Livevorschau, sodass die Notwendigkeit einer Livevorschau ebenfalls ein Faktor ist.
- Verwenden Sie die **Livevorschau,** um die Auswirkungen der Optionen anzugeben, wenn ein Befehl zu einem verwandten Satz von Formatierungsoptionen gehört und live preview wichtig und praktisch ist, insbesondere wenn Benutzer wahrscheinlich die falsche Option wählen.
  - Wenn der Befehl häufig verwendet wird, verwenden Sie aus Gründen der Direktität einen Katalog im Menüband.
  - Wenn der Befehl selten verwendet wird, verwenden Sie einen Dropdownkatalog.
- Direkte Befehle mit den folgenden **Steuerelementen** in der folgenden Einstellungsreihenfolge verfügbar machen
  - **Befehlsschaltflächen, Kontrollkästchen, Optionsfelder und Kataloge an Ort und Stelle.** Diese sind immer direkt.
  - **Unterteilte Schaltflächen.** Direkt für den gängigsten Befehl, aber indirekt für die Befehlsvariationen.
  - **Menüschaltflächen.** Diese sind indirekt, stellen aber viele Befehle dar, die leicht zu finden sind.
  - **Textfelder (mit Drehsteuerelementen).** Texteingaben erfordern im Allgemeinen mehr Aufwand als die anderen Steuerelementtypen.
- ![Screenshot des Menübands mit nur Menüschaltflächen ](images/cmd-ribbons-image42.png)</br>Wenn das Menüband größtenteils aus Menüschaltflächen besteht, wenn es in voller Größe angezeigt wird, können Sie auch eine Menüleiste verwenden.
- **Sofortige Befehle bevorzugen.** ![Screenshot der Geteilte Druckschaltfläche und des zugehörigen Untermenüs ](images/cmd-ribbons-image43.png)<br/>Ein Befehl ist sofort, wenn er sofort wirksam wird (d. b. ohne Dialogfelder, um zusätzliche Eingaben zu erfassen). Wenn für einen Befehl möglicherweise eine Eingabe erforderlich ist, sollten Sie eine unterteilte Schaltfläche mit dem unmittelbaren Befehl im Schaltflächenteil und den Befehlen verwenden, die Eingaben im Untermenü erfordern.

### <a name="galleries"></a>Kataloge

**Verwenden Sie einen [Katalog,](glossary.md)** wenn:

- **Es gibt einen klar definierten, verwandten Satz von Auswahlmöglichkeiten, aus denen Benutzer in der Regel wählen.** Möglicherweise gibt es eine unbegrenzte Anzahl von Variationen, aber die wahrscheinliche Auswahl sollte gut enthalten sein. Wenn die Auswahlmöglichkeiten nicht stark zusammenhängen, sollten Sie separate Kataloge verwenden.
- **Die Auswahlmöglichkeiten werden am besten visuell ausgedrückt, z. B. Formatierungsfunktionen.** Die Verwendung von Miniaturansichten erleichtert das Durchsuchen, Verstehen und Treffen von Entscheidungen. Die Auswahl kann zwar bezeichnet werden, die Auswahl erfolgt jedoch visuell, und Textbeschriftungen sollten nicht erforderlich sein, um die Auswahl zu verstehen.
- **Die Auswahlmöglichkeiten zeigen das Ergebnis an, das sofort mit einem einzigen Klick erzielt wird.** Es sollte kein Nachverfolgungsdialogfeld vorhanden sein, um die Absicht des Benutzers genauer zu verdeutlichen, oder eine Reihe von Schritten, um das angegebene Ergebnis zu erzielen. Wenn Benutzer die Auswahl möglicherweise anpassen möchten, lassen Sie sie dies später tun.

**Verwenden Sie einen Katalog im Menüband,** wenn:

- **Die Auswahlmöglichkeiten werden häufig verwendet.** Die Auswahlmöglichkeiten benötigen den Speicherplatz und sind den Speicherplatz wert, der möglicherweise von anderen Befehlen übernommen wird.
- **Für die typische Verwendung ist es nicht erforderlich, die angezeigten Optionen zu gruppieren oder zu filtern.**
- **Die Auswahlmöglichkeiten können effektiv innerhalb der Höhe eines Menübands (48 Pixel) angezeigt werden.**

#### <a name="thumbnails-in-galleries"></a>Miniaturansichten in Katalogen

**Wählen Sie die kleinste Miniaturansichtsgröße des Standardkatalogs** aus, die den Auftrag gut erfüllt.

- Verwenden Sie für Kataloge im Menüband Miniaturansichten von 16 x 16, 48 x 48 oder 64 x 48 Pixel.
- Verwenden Sie für Dropdown-Kataloge Miniaturansichten von 16 x 16, 32 x 32, 48 x 48, 64 x 48, 72 x 96, 96 x 72, 96 x 96 oder 128 x 128 Pixel.
- Alle Katalogelemente sollten die gleiche Miniaturansichtsgröße aufweisen.

Für Kataloge im Menüband:

- **Zeigen Sie mindestens drei Optionen an. mehr, wenn Platz vorhanden ist.** Wenn nicht genügend Speicherplatz vorhanden ist, um mindestens drei Auswahlmöglichkeiten in der typischen Fenstergröße anzuzeigen, verwenden Sie stattdessen einen Dropdownkatalog.
- **Erweitern Sie Kataloge im Menüband, um den verfügbaren Speicherplatz zu nutzen.** Verwenden Sie den zusätzlichen Platz, um weitere Elemente anzuzeigen und die Auswahl mit einem einzigen Klick zu vereinfachen.

Für Dropdown-Kataloge:

- **Zeigen Sie den Katalog entweder über ein Kombinationsfeld, eine Dropdownliste, eine unterteilte Schaltfläche oder eine Menüschaltfläche an.**
- **Wenn der Benutzer auf das Hauptfenster klickt, um den Dropdownkatalog zu schließen, schließen Sie einfach den Katalog, ohne den Inhalt des Hauptfensters auszuwählen oder zu ändern.**
- **Wenn ein Katalog viele Auswahlmöglichkeiten hat und einige Auswahlmöglichkeiten selten verwendet werden, vereinfachen Sie den Standardkatalog, indem Sie sich auf die häufig verwendeten Optionen konzentrieren.** Geben Sie für die verbleibenden Befehle einen entsprechenden Befehl am unteren Rand der Dropdownseite des Katalogs an.
  - Wenn der Befehl eine Liste mit weiteren Variationen anzeigt, nennen Sie sie "Weitere `singular feature name` Optionen...".
  - Wenn der Befehl ein Dialogfeld darstellt, in dem Benutzer ihre eigenen benutzerdefinierten Optionen erstellen können, nennen Sie es "Benutzerdefiniert..." `feature name`
- **Organisieren Sie die Auswahlmöglichkeiten in Gruppen, wenn dies das Durchsuchen effizienter macht.**
- ![Screenshot des Symbolkatalogs und der Filter ](images/cmd-ribbons-image44.png)<br/>**Wenn ein Katalog viele Elemente enthält, sollten Sie einen Filter hinzufügen, um Benutzern zu helfen, entscheidungen effizienter zu finden.** Um Verwirrung zu vermeiden, zeigen Sie den Katalog zunächst ungefiltert an. Die meisten Kataloge sollten jedoch keinen Filter benötigen, da sie nicht so viele Auswahlmöglichkeiten haben sollten, und die Verwendung von Gruppen sollte ausreichend sein.

### <a name="command-previews"></a>Befehlsvorschau

- **Verwenden Sie Vorschauen, um die Auswirkungen eines Befehls anzuzeigen, ohne dass Benutzer ihn zuerst ausführen müssen.** Durch die Verwendung hilfreicher Vorschauversionen können Sie die Effizienz und das einfache Lernen Ihres Programms verbessern und die Notwendigkeit von Testversionen und Fehlern reduzieren. Die verschiedenen Typen von Befehlsvorschauversionen finden Sie im Abschnitt Entwurfskonzepte dieses Artikels unter [Vorschauversionen.](#previews)
- **Stellen Sie für Livevorschau sicher, dass die Vorschau angewendet und der aktuelle Zustand innerhalb von 500 Millisekunden wiederhergestellt werden kann.** Dies erfordert die Möglichkeit, Formatierungsänderungen schnell und unterbrechungsfähig anzuwenden. Benutzer müssen in der Lage sein, verschiedene Optionen schnell auszuwerten, damit Livevorschauversionen ihren vollen Nutzen haben.
- **Vermeiden Sie die Verwendung von Text in Vorschauversionen.** Andernfalls müssen die Vorschaubilder lokalisiert werden.

### <a name="icons"></a>Symbole

- ![Screenshot der Dropdownliste und Kontrollkästchen ](images/cmd-ribbons-image45.png)<br/>**Stellen Sie Symbole für alle Menübandsteuerelemente außer Dropdownlisten, Kontrollkästchen und Optionsfeldern bereit.** Die meisten Befehle erfordern Symbole mit 32 x 32 und 16 x 16 Pixeln (nur Symbole mit 16 x 16 Pixeln werden von der Symbolleiste für den Schnellzugriff verwendet). Kataloge verwenden in der Regel Symbole mit 16 x 16, 48 x 48 oder 64 x 48 Pixeln.
- **Geben Sie eindeutige Symbole an.** Verwenden Sie nicht das gleiche Symbol für verschiedene Befehle.
- **Stellen Sie sicher, dass Menübandsymbole für die Hintergrundfarbe des Menübands deutlich sichtbar sind.** Werten Sie Menübandsymbole immer im Kontext und im Modus mit hohem Kontrast aus.
- **Wählen Sie Symbolentwürfe aus, die ihre Auswirkungen deutlich kommunizieren,** insbesondere für die am häufigsten verwendeten Befehle. Gut entworfene Menübänder verfügen über selbsterklärende Symbole, mit denen Benutzer Befehle effizient finden und verstehen können.
- **Wählen Sie Symbole aus, die erkennbar und unterscheidbar sind,** insbesondere für die am häufigsten verwendeten Befehle. Stellen Sie sicher, dass die Symbole unterschiedliche Formen und Farben aufweisen. Auf diese Weise können Benutzer die Befehle schnell finden, auch wenn sie sich das Symbol nicht merken.

    | Richtig                                                                                                 | Falsch                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![Screenshot des blauen Augen-Droppers und des gelben Stifts ](images/cmd-ribbons-image46.png)<br/>Verwenden Sie Form und Farbe, um Symbole zu erstellen, die leicht zu unterscheiden sind. | ![Screenshot: Blauer Augen-Dropper und blauer Stift ](images/cmd-ribbons-image47.png)<br/> Symbole mit der gleichen Farbe sind schwer zu unterscheiden|

- ![Screenshot des Kommentarbefehls im Popupcontainer ](images/cmd-ribbons-image48.png)<br/>**Erwägen Sie das Erstellen von Popupgruppensymbolen, indem Sie das 16 x 16 Pixel große Symbol des prominentesten Befehls in der Gruppe in einem visuellen Container mit 32 x 32 Pixeln platzieren.** Sie müssen keine verschiedenen Symbole für Popupgruppen erstellen.
- ![Screenshot der Befehlsschaltflächen für die Textformatierung ](images/cmd-ribbons-image25.png)<br/>**Ändern Sie ggf. das Symbol, um den aktuellen Zustand widerzuspiegeln.** Dies ist besonders nützlich für geteilte Schaltflächen, deren Standardeffekt geändert werden kann.
- **Stellen Sie sicher, dass Die Menübandsymbole den Richtlinien für Symbole im Stil von Styles entsprechen.** Menübandsymbole werden jedoch direkt angezeigt, anstatt in der Perspektive dargestellt zu werden.

| Richtig                                                                                                 | Falsch                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![Screenshot von zweidimensionalen Befehlssymbolen ](images/cmd-ribbons-image49.png)<br/> Verwenden Sie zweidimensionale Symbole.|![Screenshot von dreidimensionalen Befehlssymbolen ](images/cmd-ribbons-image50.png)<br/> Verwenden Sie keine dreidimensionalen Symbole. |
 
### <a name="enhanced-tooltips"></a>Erweiterte QuickInfos

- **Alle Menübandbefehle sollten erweiterte QuickInfos aufweisen,** um den Befehlsnamen, die Tastenkombination, die Beschreibung und optionale zusätzliche Informationen anzugeben. Vermeiden Sie QuickInfos, die einfach die Bezeichnung neu erstellen.

    **Falsch:**

    ![Screenshot der QuickInfo, die den Befehlsnamen wiederholt ](images/cmd-ribbons-image51.png)

    In diesem Beispiel gibt die QuickInfo einfach die Befehlsbezeichnung erneut an.

- **Wenn dies praktisch ist, beschreiben Sie den Befehl vollständig mit einer präzisen Beschreibung.** Link zur Hilfe nur, wenn eine weitere Erklärung wirklich erforderlich ist.

    **Falsch:**

    ![Screenshot der QuickInfo für den Befehl "Durchgestrichen" ](images/cmd-ribbons-image52.png)

    In diesem Beispiel benötigt der Befehl keine Hilfe.

- **Wenn Sie hilfreich sind, veranschaulichen Sie die Auswirkungen des Befehls mithilfe einer Vorschau.**

    ![Screenshot von QuickInfo und Diagramm für Einfügediagramm ](images/cmd-ribbons-image53.png)

    In diesem Beispiel veranschaulicht das QuickInfo-Bild die Auswirkung des Befehls.

Informationen zu Bezeichnungsrichtlinien finden Sie unter [Erweiterte QuickInfo-Bezeichnungen.](#enhanced-tooltips)

### <a name="access-keys-and-keytips"></a>Zugriffsschlüssel und KeyTips

Keytips sind der Mechanismus, mit dem Zugriffsschlüssel für Befehle angezeigt werden, die direkt auf einem Menüband angezeigt werden.

Zugriffsschlüssel für Dropdownmenübefehle werden mit einem unterstrichenen Zeichen angezeigt. Sie unterscheiden sich von Menüzugriffsschlüsseln wie folgt:

- Es können zwei Zeichenzugriffsschlüssel verwendet werden. Fp kann beispielsweise verwendet werden, um auf den Befehl Format command (Formatieren) zuzugreifen.
- Die Zuweisungen von Zugriffsschlüsseln werden mithilfe von Tipps anstelle von Unterstreichungen angezeigt, sodass die Zeichenbreite und die Nachfolger kein Faktor bei der Erstellung von Zuweisungen sind.

- **Weisen Sie allen Menübandregisterkarten und Befehlen Zugriffsschlüssel zu.** Die einzige mögliche Ausnahme ist für Befehle, die aus Legacy-Add-Ins stammen.
- **Für die Schaltfläche Anwendung und die Symbolleiste für den Schnellzugriff:**
  - Weisen Sie der Schaltfläche Anwendung F zu. Diese Zuweisung wird aufgrund der Ähnlichkeit der Schaltfläche Anwendung mit dem herkömmlichen Menü Datei verwendet.
  - ![Screenshot der Befehlstastentipps auf einem Menüband ](images/cmd-ribbons-image54.png)<br/>Weisen Sie zugriffsschlüsseln für die Symbolleiste für den Schnellzugriff und die zuletzt verwendeten Dateilisten numerisch zu.
- ![Screenshot mit KeyTips für Registerkarten ](images/cmd-ribbons-image55.png)<br/>**Für Registerkarten:**
  - Weisen Sie "H" zu "Home" zu.
  - Weisen Sie ab den am häufigsten verwendeten Registerkarten den ersten Buchstaben der Bezeichnung zu.
  - Wählen Sie für registerkarten, die dem ersten Buchstaben nicht zugewiesen werden können, einen eindeutigen Konsonanten oder vokalen In der Bezeichnung aus.
  - Bei Programmen, die zur Unterstützung von Menüleisten verwendet wurden, ist es sinnvoll, die Kompatibilität des Zugriffsschlüssels so weit wie möglich aufrechtzuerhalten. Vermeiden Sie es, unterschiedliche Bedeutungen für den Zugriff auf Schlüssel aus älteren Menükategorien zuzuweisen. Wenn die ältere Menüleistenversion eines Programms beispielsweise über ein Menü Bearbeiten verfügt, sollten Sie einen E-Zugriffsschlüssel für die entsprechende Registerkarte verwenden. Wenn keine entsprechende Registerkarte vorhanden ist, weisen Sie keiner Registerkarte eine E-Zugriffsschlüssel zu, um Verwechslungen zu vermeiden.
- ![Screenshot mit KeyTips für ein Menüband ](images/cmd-ribbons-image56.png)<br/>**Für Menübandbefehle, Menüs und Untermenüs:**
  - Weisen Sie eindeutige Tastenkombinationen innerhalb einer Registerkarte zu. Sie können Zugriffstastenkombinationen auf verschiedenen Registerkarten wiederverwenden.
  - Weisen Sie nach Möglichkeit die Standardzugriffsschlüssel für häufig verwendete Befehle zu. Weitere Informationen finden [Sie in der Standardzugriffsschlüsseltabelle.](inter-keyboard.md)
  - Für andere Befehle:
    - Wählen Sie für die am häufigsten verwendeten Befehle Buchstaben am Anfang des ersten oder zweiten Worts der Bezeichnung aus, vorzugsweise den ersten Buchstaben.
    - Wählen Sie bei weniger häufig verwendeten Befehlen Buchstaben aus, die in der Bezeichnung ein unterschiedlicher Konsonant oder Vokal sind, z. B. "x" in "Exit".
    - Verwenden Sie für die am wenigsten häufig verwendeten Befehle und Dialogfeldstarter nach Bedarf zwei Buchstaben.
    - Verwenden Sie für Menüs und Untermenüs einen einzelnen Buchstaben, um die Anzahl der Tastatureingaben zu reduzieren, die für den vollständigen Befehl erforderlich sind.
    - Verwenden Sie keine Zugriffsschlüssel ab J, Y oder Z, da sie für kontextbezogene Registerkarten, nicht zugewiesene Keytips und Popupgruppen verwendet werden.
- ![Screenshot der Keytips für Popupgruppen ](images/cmd-ribbons-image58.png)<br/>**Für Popupgruppen:**
  - Verwenden Sie einen zweibuchstabenbasierten Zugriffsschlüssel, der mit Z beginnt.
  - Weisen Sie ab den am häufigsten verwendeten Gruppen dem ersten Buchstaben der Bezeichnung den zweiten Zugriffsschlüsselbuchstaben zu.
  - Wählen Sie für alle verbleibenden Gruppen einen bestimmten Konsonanten oder einen Vokal in der Bezeichnung aus.

Richtlinien für Tastenkombinationen finden Sie unter [Tastatur](inter-keyboard.md).

### <a name="application-buttons"></a>Anwendungsschaltflächen

- **Verwenden Sie eine Anwendungsschaltfläche, um ein Menü mit Befehlen anzuzeigen, in denen eine Datei ausgeführt wird.** Beispiele hierfür sind Befehle, die normalerweise im Menü Datei zum Erstellen, Öffnen und Speichern von Dateien, Drucken und Senden und Veröffentlichen von Dokumenten verwendet werden.
- **Geben Sie immer eine Anwendungsschaltfläche an, wenn Sie ein Menüband verwenden.** Wenn das Programm keine Dateien verwendet, greifen Sie mithilfe der Schaltfläche Anwendung auf die Programmoptionen und den Befehl Beenden zu. Anwendungsschaltflächen zeigen immer ein Befehlsmenü an, das nie einfach nur verzierend ist.
- **Verwenden Sie gegebenenfalls die folgenden Standardbefehle für das Anwendungsmenü:**
  - Neu  
  - Öffnen  
  - Speichern  
  - Speichern unter...
  - Drucken...
  - Schnelldruck  
  - Seitenansicht  
  - Schließen  
  - Optionen  
  - Beenden  
  
- **Reservieren Sie Befehle, die zum Menü Anwendung gehören, nur für dieses Menü.** Platzieren Sie sie nicht redundant auf einer der Registerkarten.
- Geben Sie für jedes Menüelement Dies an:
  - **Eine Bezeichnung mit dem Befehlsnamen.**
  - **Ein 32 x 32 Pixel großes Symbol.**
  - **Eine kurze Beschreibung.** Stellen Sie sicher, dass die Beschreibung mit mindestens zwei Textzeilen angezeigt werden kann.
- ![Screenshot der QuickInfo, die die Tastenkombination dokumentiert ](images/cmd-ribbons-image59.png)<br/>**Verwenden Sie QuickInfos, um die Tastenkombinationen zu dokumentieren.** Im Gegensatz zu normalen Menüs dokumentieren Anwendungsmenüs die Tastenkombinationen nicht mithilfe von Bezeichnungen.

### <a name="quick-access-toolbars"></a>Symbolleisten für den Schnellzugriff

- **Verwenden Sie die Symbolleiste für den Schnellzugriff, um Zugriff auf häufig verwendete Befehle zu ermöglichen.** Die Befehle können über die Schaltfläche Anwendung oder das Menüband ausgeführt werden.
- **Stellen Sie bei Verwendung eines Menübands immer eine Symbolleiste für den Schnellzugriff zur Verfügung.** Tun Sie dies auch, wenn das Menüband über eine einzelne Registerkarte verfügt. dies sorgt für Programmkonsistenz.
- **Geben Sie in der Symbolleiste für den Schnellzugriff vorab die häufig verwendeten Befehle im Menü Anwendung ein.** Geben Sie Speichern und Rückgängig an, wenn ihr Programm sie unterstützt, und Öffnen und Drucken, wenn dies unterstützt und häufig verwendet wird.
- **Geben Sie im Menü Schnellzugriffssymbolleiste anpassen bis zu 12 der am häufigsten verwendeten direkt verwendeten Befehle an.** Sofortige Befehle erfordern keine zusätzlichen Eingaben, bevor sie wirksam werden, und eignen sich daher gut für die Symbolleiste für den Schnellzugriff. Obwohl dies alle unmittelbaren Befehle sein können, bevorzugen Sie die Befehle, die sich nicht auf der Registerkarte Start befinden, da Benutzer diese eher auswählen.
- **Wenn im Menü Schnellzugriffssymbolleiste anpassen ein Paar verwandter Befehle enthalten ist, geben Sie unabhängig von der Häufigkeit beides an.** Gängige Paare sind "Öffnen/Schließen", "Zurück/Vorwärts" und "Rückgängig/Wiederholen".
- **Geben Sie im Dialogfeld Schnellzugriffssymbolleiste anpassen eine Möglichkeit zum Hinzufügen eines beliebigen Befehls an.** Geben Sie einen Filter für beliebte Befehle an, der die am häufigsten verwendeten Befehle anzeigt, und wählen Sie diesen Filter standardmäßig aus.

### <a name="dialog-box-launchers"></a>Dialogfeldstarter

- ![Screenshot des Schriftartdialogfelds und der Schriftartgruppe ](images/cmd-ribbons-image60.png)<br/>**Stellen Sie einer Gruppe ein Dialogfeld-Startfeld zur Verfügung, wenn ein verwandtes Dialogfeld mit selten verwendeten Befehlen und Einstellungen verfügbar ist.** Das Dialogfeld sollte alle Befehle in der Gruppe sowie andere nicht vollständig andere Befehle oder dieselben Befehle wie die Gruppe enthalten.
- **Verwenden Sie kein Dialogfeldstartfeld, um Befehle direkt auszuführen.** Ein Dialogfeld-Startfeld muss ein Dialogfeld anzeigen.
- **Verwenden Sie kein Dialogfeldstartfeld, um auf häufig verwendete Befehle und Einstellungen zu zugreifen.** Im Vergleich zu Befehlen direkt im Menüband sind die Dialogfeldbefehle und -einstellungen relativ nicht behebbar.
- **Übereinstimmung mit dem Namen des Dialogfelds mit dem Namen der Gruppe.** Es muss keine genaue Übereinstimmung sein, aber die Namen sollten ähnlich genug sein, damit Benutzer von den Ergebnissen nicht überraschend sind.

    **Falsch:**

    ![Screenshot des Dialogfelds "Erinnerungssound" ](images/cmd-ribbons-image61.png)

    Während ein Erinnerungssound eine Erinnerungsoption ist, ist die Verwendung des Dialogfeld-Startfelds zum Festlegen des Erinnerungssounds unerwartet.

- **Zeigt nur die Befehle und Einstellungen an, die sich auf die Gruppe beziehen.** Wenn im Dialogfeld andere Dinge angezeigt werden, können Benutzer daraus schließen, dass dieser Pfad zu diesen anderen Befehlen und Einstellungen der einzige Pfad ist.

    **Falsch:**

    ![Screenshot des Dialogfelds "Schriftart" ](images/cmd-ribbons-image62.png)

    In diesem Beispiel zeigt das Dialogfeld Schriftart Einstellungen für den Zeichenabstand an, die nicht mit der zugeordneten Registerkarte verknüpft sind.

## <a name="labels"></a>Bezeichnungen

### <a name="tab-labels"></a>Registerkartenbezeichnungen

- **Beschriften Sie alle Registerkarten.**
- Verwenden Sie nach **Möglichkeit die Standardregisterkarte des Menübands**.
- **Prägnante, einzelne Wortbezeichnungen bevorzugen.** Obwohl Bezeichnungen mit mehreren Wörtern akzeptabel sind, nehmen sie mehr Platz ein und sind schwieriger zu lokalisieren.
- **Wählen Sie aussagekräftige Registerkartennamen aus, die ihren Inhalt eindeutig und genau beschreiben.** Die Namen sollten spezifisch, aber nicht zu spezifisch sein. Registerkartennamen sollten vorhersagbar genug sein, damit Benutzer nicht von ihren Inhalten überraschend sind. Beachten Sie, dass die Registerkarte Start generisch benannt wird, da sie für die am häufigsten verwendeten Befehle verwendet wird.
- **Verwenden Sie** keine Gruppennamen wie "Basic" und "Advanced". Benutzer müssen bestimmen, ob der gesuchte Befehl einfach oder erweitert ist.
- **Wählen Sie Registerkartennamen aus, die ihren Zweck widerspiegeln.** Berücksichtigen Sie die Ziele oder Aufgaben, die der Registerkarte zugeordnet sind.
- **Wählen Sie Registerkartennamen aus, die sich eindeutig von allen anderen Registerkartennamen unterscheiden.**
- **Verwenden Sie entweder Nomen oder Verben für Registerkarten.** Registerkartennamen erfordern keinen parallelen Ausdruck. Wählen Sie daher die beste Bezeichnung aus, unabhängig davon, ob es sich um ein Substantiv oder ein Verbhandelt.
- **Verwenden Sie keine Gerunds** (Namen, die auf "-ing" enden). Verwenden Sie stattdessen das Verb, von dem der Gerund abgeleitet wird. (Verwenden Sie z. B. "Draw" anstelle von "Drawing".)
- **Vermeiden Sie Registerkartennamen mit den gleichen Anfangsbuchstaben, insbesondere angrenzenden Registerkarten.** Wenn das Menüband herunterskaliert wird, haben diese Registerkartennamen denselben abgeschnittenen Text.
- **Singuläre Namen bevorzugen.** Sie können jedoch einen pural-Namen verwenden, wenn der Singularname unwendlich ist.
- **Verwenden Sie die Groß-/Groß-/Formatvorlage.**
- **Verwenden Sie keine Interpunktion am Ende.**

### <a name="contextual-tab-and-tab-set-labels"></a>Kontextbezogene Bezeichnungen für Registerkarten und Registerkarten

- **Beenden Sie kontextbezogene Registerkartensatzbezeichnungen mit "Tools".** Auf diese Weise kann der Zweck kontextbezogener Registerkarten identifiziert werden.
- Verwenden Sie die Groß-/Groß-/Formatvorlage.
- Verwenden Sie keine Interpunktion am Ende.

### <a name="group-labels"></a>Gruppenbezeichnungen

- **Beschriften Sie alle Gruppen,** es sei denn, die Gruppe verfügt über einen einzelnen Befehl, und die Gruppen- und Befehlsbezeichnungen sind identisch.

- **Verwenden Sie die StandardbandgruppenWenn dies praktikabel ist.**
- **Prägnante, einzelne Wortbezeichnungen bevorzugen.** Obwohl Bezeichnungen mit mehreren Wörtern akzeptabel sind, nehmen sie mehr Platz ein und sind schwieriger zu lokalisieren.
- **Wählen Sie aussagekräftige Gruppennamen aus, die ihren Inhalt eindeutig und genau beschreiben.** Die Namen sollten spezifisch und nicht generisch sein.
- **Wählen Sie Gruppennamen aus, die ihren Zweck widerspiegeln.** Berücksichtigen Sie die Ziele oder Aufgaben, die den Befehlen in der Gruppe zugeordnet sind.
- **Vermeiden Sie die Verwendung von Gerunds** (Namen, die auf "-ing" enden). Sie können jedoch Gerunds verwenden, wenn die Verwendung des Verbs, von dem der Gerund abgeleitet ist, verwirrend wäre. Verwenden Sie beispielsweise "Editing" und "Proofing" anstelle von "Bearbeiten" und "Proof".
- **Verwenden Sie keine Gruppennamen, die mit Registerkartennamen identisch sind.** Die Verwendung des Registerkartennamens, auf dem sich die Gruppe befindet, liefert keine Informationen, und die Verwendung des Namens einer anderen Registerkarte ist verwirrend.
- **Singuläre Namen bevorzugen.** Sie können jedoch einen pural-Namen verwenden, wenn der Singularname umstauend ist. 
- **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
- **Verwenden Sie keine Interpunktion am Ende.**

### <a name="command-labels"></a>Befehlsbezeichnungen

- **Beschriften Sie alle Befehle.** Explizite Textbezeichnungen helfen Benutzern, Befehle zu finden und zu verstehen. **Ausnahme:** Die Beschriftung eines Befehls kann nicht angegeben werden, wenn sein Symbol äußerst bekannt ist und der Speicherplatz einen Premium-Bereich auft. Höchstwahrscheinlich werden befehle ohne Beschriftung auf der Registerkarte Start angezeigt. Weisen Sie in diesem Fall die Name-Eigenschaft einer entsprechenden Textbezeichnung zu. Auf diese Weise können Hilfstechnologieprodukte wie Sprachbildschirme Benutzern alternative Informationen zur Grafik bereitstellen.
- **Verwenden Sie für Befehlsschaltflächen eine präzise, selbsterklärende Bezeichnung.** Verwenden Sie nach Möglichkeit ein einzelnes Wort. Maximalwert von vier Wörtern.
- **Wenn die Liste immer über einen Wert verfügt, verwenden Sie für Dropdownlisten den aktuellen Wert als Bezeichnung.**
- ![Screenshot der Eingabeaufforderung für suchadressenbücher ](images/cmd-ribbons-image67.png)<br/>Wenn eine [bearbeitbare Dropdownliste](/windows/desktop/uxguide/ctrl-drop) keinen Wert hat, verwenden Sie eine [Eingabeaufforderung.](glossary.md)
- **Dropdownlisten, die nicht selbsterklärend sind oder selten verwendet werden, benötigen eine explizite Bezeichnung.** Setzen Sie einen Doppelpunkt am Ende der Bezeichnung.
- ![Screenshot von automatisch nach: Sekunden<br.>Verwenden Sie für Textfelder \[ \] ](images/cmd-ribbons-image69.png) **eine explizite Bezeichnung.** Setzen Sie einen Doppelpunkt am Ende der Bezeichnung.
- **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.** Dies ist für den Windows [besser geeignet.](text-style-tone.md)
- **Starten Sie die Bezeichnung mit einem imperativen Verb.** es sei denn, es ist identisch mit dem Registerkarten- oder Gruppennamen oder einem allgemeinen Verb wie Show, Create, Insert oder Format.
- **Verwenden Sie keine Interpunktion am Ende.**
- **Um Platz zu sparen, sollten Sie keine Ausellipsen auf Menüband-Befehlsbezeichnungen setzen.** Ausellipsen werden jedoch von Befehlen in der Schaltfläche Anwendung und in den Dropdownmenüs verwendet.

### <a name="enhanced-tooltip-labels"></a>Erweiterte QuickInfo-Bezeichnungen

- **Verwenden Sie den Titel, um ggf. den Befehlsnamen und seine Tastenkombination zu geben.**
- **Verwenden Sie für den Titel keine Endzeichen.**
- **Starten Sie die Beschreibung mit einem Verb.** Verwenden Sie die Beschreibung, damit Benutzer bestimmen können, ob es sich bei einem bestimmten Feature um das gesuchte Feature handelt. Die Beschreibung sollte so formuliert werden, dass sie den Satz "This is the right feature to use if you want..." (Dies ist das richtige Feature, wenn Sie möchten...) vervollständigen.
- **Halten Sie die Beschreibung kurz.** Kommen Sie direkt auf den Punkt. Längerer Text rät vom Lesen ab.
-   ![Screenshot der Teilungsschaltfläche zum Einfügen und zwei QuickInfos ](images/cmd-ribbons-image70.png)<br/>**Verwenden Sie für geteilte Schaltflächen eine andere QuickInfo, um das Menü für geteilte Schaltflächen zu erläutern.**
- **Verwenden Sie eine optionale ergänzende Beschreibung, um die Verwendung des Steuerelements zu erläutern.** Dieser Text kann Informationen zum Zustand des Steuerelements enthalten (einschließlich der Gründe, warum es deaktiviert ist), wenn das Steuerelement selbst keinen Zustand anknut. Halten Sie diesen Text kurz, und verwenden Sie ein Hilfethema, um ausführlichere Erläuterungen zu erhalten.
- ![Screenshot der QuickInfo mit Grafik und Text: Verwenden Sie vollständige Sätze mit endender ](images/cmd-ribbons-image71.png)**Interpunktion.**
- Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.

### <a name="application-button-labels"></a>Bezeichnungen der Anwendungsschaltfläche

- [Screenshot der ausgewählten Schnelldruckoption ](images/cmd-ribbons-image72.png)<br/>**Verwenden Sie "Quick", um eine sofortige Version eines Befehls anzugeben.**

- **Verwenden Sie Auslassungsellipsen, um anzugeben, dass ein Befehl weitere Informationen erfordert.**
- **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Menübänder:

- Verweisen Sie auf das Menüband und seine Komponenten als Menüband, Registerkarten, Gruppen und Steuerelemente. Diese Begriffe sind nicht groß.
- Verweisen Sie auf die schaltfläche "Runde" als Schaltfläche Anwendung und das enthaltene Menü als Menü Anwendung.
- Verweisen Sie auf die Symbolleiste als Symbolleiste für den Schnellzugriff.
- Verweisen Sie auf Registerkarten nach ihren Bezeichnungen und der Wortregisterkarte. Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Groß-/Groß-/A-
- Verweisen Sie auf Befehle nach ihren Bezeichnungen. Verweisen Sie auf Befehle ohne Bezeichnung über ihre QuickInfo-Namen. Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Unterschrift, aber schließen Sie die Auslassungszeichen nicht ein. Fügen Sie nicht die Wortschaltfläche oder den Befehl ein.
- Verwenden Sie zum Beschreiben der Benutzerinteraktion den Klick für Registerkarten und Steuerelemente. Verwenden Sie die EINGABETASTE für bearbeitbare Dropdownlisten. Verwenden Sie nicht auswählen, auswählen oder auswählen.
- Verweisen Sie auf nicht verfügbare Elemente als nicht verfügbar, nicht als abgeblendet, deaktiviert oder abgeblendet. Verwenden Sie in der Programmierdokumentation deaktiviert.
- Formatieren Sie die Bezeichnungen nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnungen nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiele:

- Klicken Sie **auf der** Registerkarte Startseite auf **Spezielle einfügen.**
- Geben Sie **auf der** Registerkarte Startseite im Feld **Schriftart** "Segoe UI" ein.
- Klicken Sie **auf der** Registerkarte Überprüfen auf **Markup anzeigen,** und klicken Sie dann **auf Prüfer**.
- Klicken Sie **auf der** Registerkarte Format unter **Bildtools** auf **Bilder komprimieren.**