---
title: Barrierefreiheit (Entwurfsgrundlagen)
description: Das Entwerfen von Software für die Barrierefreiheit bedeutet, sicherzustellen, dass Programme und Funktionen problemlos für die breite palette von Benutzern verfügbar sind, auch für Benutzer mit Behinderungen und Beeinträchtigungen.
ms.assetid: df6947ec-6a1d-4645-ae3e-863839c32588
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e6ff3cdaa9a1a1b2a13025da14c9aed150ee3928
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524464"
---
# <a name="accessibility-design-basics"></a>Barrierefreiheit (Entwurfsgrundlagen)

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Das Entwerfen von Software für die Barrierefreiheit bedeutet, sicherzustellen, dass Programme und Funktionen problemlos für die breite palette von Benutzern verfügbar sind, auch für Benutzer mit Behinderungen und Beeinträchtigungen.

Die Anzahl der Benutzer, die Barrierefreiheitsfeatures helfen können, kann Sie verdauen. Beispielsweise haben Umfragen im USA ergeben, dass mehr als die Hälfte aller Computerbenutzer Schwierigkeiten oder Beeinträchtigungen im Zusammenhang mit der Barrierefreiheit haben und wahrscheinlich von der Verwendung barrierefreier Technologien profitieren. Darüber hinaus führt die Herangehensweise an den Softwareentwurf mit der Flexibilität und Inklusion, die das Merkmal der Barrierefreiheit sind, häufig zu einer insgesamt verbesserten Benutzerfreundlichkeit und Kundenzufriedenheit.

![Screenshot des Dialogfelds "Erleichtertes Zugreifen auf das Center" ](images/inter-accessibility-image1.png)

Die Center für erleicherte Bedienung, die über Systemsteuerung verfügbar ist, bietet einen zentralen Ort, an dem Benutzer die gewünschten Barrierefreiheitsfunktionen auswählen und anpassen können.

**Hinweis:** Richtlinien für [Tastatur,](inter-keyboard.md) [Maus,](inter-mouse.md) [Farbe](vis-color.md)und [Sound](vis-sound.md) werden in separaten Artikeln vorgestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

Viele physische, perzeptive und kognitive Faktoren kommen ins Spiel, wenn Benutzer mit Computerhardware und -software interagieren. Bevor Sie möglichkeiten in Betracht ziehen, die Funktionen Ihres Programms besser zugänglich zu machen, hilft es Ihnen, zu erfahren, welche Arten von Behinderungen und Beeinträchtigungen vorhanden sind und mit welchen Hilfstechnologien diese Benutzer möglicherweise arbeiten, während sie mit Computern interagieren.

### <a name="types-of-impairments"></a>Arten von Beeinträchtigungen

In der folgenden Tabelle werden häufige Benutzerbehinderungen und Beeinträchtigungen beschrieben. Außerdem werden einige der wichtigsten Lösungen aufgeführt, die verwendet werden, um den Zugriff auf Computer zu erleichtern.



| Wertminderung    | BESCHREIBUNG   | Lösungen  |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Grafisches Element<br/>             | Dieser Bereich reicht von 17 Prozent der Benutzer bis hin zu schwerwiegend (9 Prozent der Benutzer).<br/>                                                                                                   | Anpassbare Vergrößerung, Farben und Kontrast; Braorte-Hilfsprogramme; Sprachausgabe.<br/>                                                                                       |
| Hörvermögen<br/>            | Der Bereich reicht von "18 Prozent der Benutzer" bis "schwerwiegend" (2 Prozent der Benutzer).<br/>                                                                                                   | Informationsredundanz: Sound wird nur als Ergänzung zur Text- oder visuellen Kommunikation verwendet.<br/>                                                                                     |
| Geschicklichkeit<br/>          | Der Bereich reicht von "19 Prozent der Benutzer" bis "schwerwiegend" (5 Prozent der Benutzer). Diese Beeinträchtigung bringt häufig Schwierigkeiten mit sich, bestimmte motorische Fähigkeiten mit Tastatur oder Maus auszuführen.<br/> | Eingabemethodenredundanz: Programmfeatures, auf die über Maus- oder Tastaturentsprechungen zugegriffen wird.<br/>                                                                                       |
| Kognitiv<br/>          | Schließt Speicherbehinderung und Wahrnehmungsunterschiede ein. Betrifft 16 Prozent der Benutzer.<br/>                                                                                                         | Hochgradig anpassbare Benutzeroberfläche (UI); Verwendung der [progressiven Offenlegung,](ctrl-progressive-disclosure-controls.md) um die Komplexität auszublenden; Verwendung von Symbolen und anderen visuellen Hilfen.<br/> |
| Beschlagnahme<br/>            | Umfasst visuelle Empfindlichkeit gegenüber Bewegung und Blinken.<br/>                                                                                                                                        | Konservativer Ansatz zum Modulieren von Schnittstellen, z. B. die Verwendung von Animationen; Vermeiden von Bildschirmflimmern im Bereich zwischen 2 Hertz (Hz) und 55 Hz.<br/>                        |
| Sprache oder Sprache<br/> | Umfasst Schwierigkeiten bei der Kommunikation mit Derlexie und der Kommunikation.<br/>                                                                                                                                       | Rechtschreibprüfungs- und Grammatikprüfungs-Hilfsprogramme; Spracherkennung und Spracherkennungstechnologie.<br/>                                                                                 |



 

Weitere Richtlinien zur Unterstützung von Benutzern mit diesen Beeinträchtigungen finden Sie weiter unten in diesem Artikel unter [Behandeln bestimmter Beeinträchtigungen.](#addressing-particular-impairments)

### <a name="types-of-assistive-technologies-and-accessibility-features"></a>Typen von Hilfstechnologien und Barrierefreiheitsfunktionen

**Sprachausgabe**

Eine Sprachausgabe ermöglicht Benutzern mit Sehbehinderung oder Beeinträchtigungen die Navigation auf einer Benutzeroberfläche durch Transformieren von Visuals in Audio. Daher werden Benutzeroberflächentext, Steuerelemente, Menüs, Symbolleisten, Grafiken und andere Bildschirmelemente von der computerisierten Stimme der Sprachausgabe gesprochen. Um ein Programm zu erstellen, das für die Sprachausgabe-Hilfstechnologie optimiert ist, müssen Sie planen, wie die Sprachausgabe jedes Benutzeroberflächenelement identifiziert.

Jedes Benutzeroberflächenelement, mit dem der Benutzer interagieren kann, muss über die Tastatur zugänglich sein und über eine Barrierefreiheits-API (Application Programming Interface, Anwendungsprogrammierschnittstelle) verfügbar gemacht werden. Es wird empfohlen, Benutzeroberflächenautomatisierung zu verwenden, das neue Barrierefreiheitsframework für alle Versionen von Microsoft Windows, die Windows Presentation Foundation (WPF) unterstützen. Benutzeroberflächenautomatisierung bietet programmgesteuerten Zugriff auf die meisten Elemente auf dem Desktop, sodass Hilfstechnologieprodukte wie Sprachausgaben Benutzern Informationen über die Benutzeroberfläche bereitstellen und die Benutzeroberfläche mit anderen Mitteln als Standardeingaben bearbeiten können (z. B. durch Sprechen statt oder zusätzlich zum Bearbeiten der Maus oder Tastatur). Weitere Informationen finden Sie in der [Benutzeroberflächenautomatisierung Übersicht.](/dotnet/framework/ui-automation/ui-automation-overview)

Beachten Sie, dass Sprachausgaben zwar eine sehr wichtige Hilfstechnologie sind, es aber auch andere gibt. Weitere Informationen zu den verfügbaren Technologien finden Sie unter [Typen von Hilfstechnologieprodukten.](https://www.microsoft.com/enable/at/types.aspx)

**Spracherkennung**

Die Spracherkennung ist ein Barrierefreiheitsfeature in Windows, mit dem Benutzer per Sprache mit ihren Computern interagieren können, wodurch die Notwendigkeit einer motorischen Interaktion mit der Maus oder Tastatur reduziert wird. Benutzer können Dokumente und E-Mails vorgeben, Sprachbefehle zum Starten und Wechseln zwischen Programmen verwenden, das Betriebssystem steuern und sogar Formulare im Web ausfüllen.

**Bildschirmlupe**

Die Vergrößerung hilft Benutzern mit sehbehinderung, indem Elemente auf dem Bildschirm an einer beliebigen Stelle zwischen dem 2- und dem 16-fachen des Originals vergrößert werden. Benutzer können dieses Feature so festlegen, dass die Maus nachverfolgt wird (um eine vergrößerte Version des Mauszeigers anzuzeigen), die Tastatur (um den Bereich zu sehen, in dem sich der Zeiger beim Tabstopp bewegt), oder die Textbearbeitung (um zu sehen, was sie eingeben).

**Visuelle Einstellungen und Farbschemas**

Benutzer mit Sehbehinderung können nicht nur die Bildschirmfläche vergrößern, sondern auch von Systemeinstellungen wie dem Modus mit [hohem Kontrast](glossary.md) oder der Möglichkeit, Hintergrund- und Vordergrundfarbschemas anzupassen.

**Narrator**

Die Sprachausgabe ist eine herunterskalierte Sprachausgabe in Windows, mit der Benutzer Text auf dem Bildschirm und Benutzeroberflächenelemente laut vorlesen können, einschließlich einiger Ereignisse (einschließlich Fehlermeldungen), die unaufhörlich auftreten. Der Benutzer kann die Sprachausgabemenüs hören, ohne das aktive Fenster zu verlassen.

![Screenshot des Dialogfelds "Microsoft-Sprachausgabe" ](images/inter-accessibility-image2.png)

Benutzer können den Umfang anpassen, in dem die Microsoft-Sprachausgabe verwendet wird.

**Bildschirmtastatur**

Für Benutzer, die Probleme mit physischen Tastaturen haben und ein alternatives Eingabegerät wie einen Schalter verwenden müssen, sind Bildschirmtastaturen erforderlich. Benutzer können Schlüssel mit der Maus oder einem anderen zeigenden Gerät, einer kleinen Gruppe von Tasten oder nur einer Taste auswählen, je nachdem, wie Sie die Bildschirmtastatur einrichten.

**Tastaturmaus**

Wenn Maustasten aktiviert sind, können Benutzer, die die Tastatur bevorzugen, die Pfeiltasten auf der numerischen Tastatur verwenden, um den Mauszeiger zu bewegen.

Eine vollständige Liste der Barrierefreiheitsfunktionen finden Sie auf der Microsoft-Website unter [Barrierefreiheit in Windows Vista.](https://www.microsoft.com/enable/products/windowsvista/default.aspx)

### <a name="keyboard-based-navigation"></a>Tastaturbasierte Navigation

Tabulatortaste, Pfeiltaste, Leertaste und EINGABETASTE sind wichtig für die tastaturbasierte Navigation. Durch Drücken der TAB-TASTE wird der [Eingabefokus](glossary.md) durch die verschiedenen Steuerelementgruppen gekreist, und die Pfeiltasten werden innerhalb eines Steuerelements oder zwischen Steuerelementen innerhalb einer Gruppe bewegt. Das Drücken der Leertaste entspricht dem Klicken auf das Steuerelement mit dem Eingabefokus, während das Drücken der EINGABETASTE dem Klicken auf die Standardbefehlsschaltfläche oder den Befehlslink entspricht, unabhängig vom Eingabefokus.

![Screenshot des Dialogfelds "Leerer Papierkorb" ](images/inter-accessibility-image3.png)

In diesem Beispiel können Benutzer die TAB-TASTE drücken, bis die gewünschte Option den Eingabefokus besitzt, und dann die EINGABETASTE drücken, um das Objekt zu öffnen.

### <a name="access-keys"></a>Zugriffsschlüssel

Mit Zugriffsschlüsseln können Benutzer Optionen auswählen und Befehle direkt initiieren, ohne zuerst zum Steuerelement navigieren zu müssen. Zugriffsschlüssel werden durch Unterstriche eines der Zeichen in der Bezeichnung jedes Steuerelements angegeben. Benutzer aktivieren dann die Option oder den Befehl, indem sie die ALT-TASTE zusammen mit dem unterstrichenen Zeichen drücken. Bei Zugriffsschlüsseln wird die Groß-/Kleinschreibung nicht beachtet.

![Screenshot des Dateimenüs und der Zugriffsschlüssel ](images/inter-accessibility-image4.png)

In diesem Beispiel wird durch Drücken von ALT+O der Befehl Öffnen aktiviert.

Die Auswahl logischer Zugriffsschlüssel für Steuerelemente stellt in der Regel keine Schwierigkeiten dar. Je mehr Steuerelemente in einem Fenster vorhanden sind, desto größer ist jedoch die Wahrscheinlichkeit, dass Ihnen die Auswahl von Zugriffsschlüsseln ausgeht. Weisen Sie in diesem Fall Zugriffsschlüssel zu Steuerelementgruppen zu, anstatt jeder einzelnen Gruppe zuzuweisen.

![Screenshot von Steuerelementgruppen und Zugriffsschlüsseln ](images/inter-accessibility-image5.png)

In diesem Beispiel werden Zugriffsschlüssel Steuerelementgruppen und nicht einzelnen Steuerelementen zugewiesen.

Zugriffsschlüssel werden häufig mit Tastenkombinationen verwechselt, aber Tastenkombinationen werden anders zugewiesen als Zugriffsschlüssel und haben unterschiedliche Ziele. Tastenkombinationen verwenden beispielsweise STRG- und Funktionstastensequenzen und sind in erster Linie als Tastenkombination für fortgeschrittene Benutzer und nicht für Barrierefreiheit vorgesehen.

Weitere Informationen finden Sie unter [Tastatur](inter-keyboard.md).

### <a name="designing-for-accessibility-three-fundamental-practices"></a>Entwerfen für Barrierefreiheit: drei grundlegende Methoden

Barrierefreie Programme unterstützen alle Benutzer in irgendeiner Weise, da sich die Ziele von Barrierefreiheit und Benutzerfreundlichkeit überschneiden. Features, die erweiterte Benutzer so effizient wie möglich gestalten sollen, profitieren beispielsweise auch von Benutzern, die die Tastatur aufgrund einer Beeinträchtigung der Dexterität bevorzugen.

Drei grundlegende Methoden helfen Ihnen beim barrierefreien Entwurf: Ermöglichen Sie ein gewisses Maß an Flexibilität in Ihrer Benutzeroberfläche, lassen Sie die Beachtung der Benutzeranforderungen und -einstellungen eine wichtige Rolle bei Entwurfsentscheidungen spielen, und bieten Sie programmgesteuerten Zugriff auf Ihre Benutzeroberfläche.

**Bereitstellen einer flexiblen Benutzeroberfläche**

Beim barrierefreien Entwurf geht es zumindest teilweise darum, Benutzern Auswahlmöglichkeiten zu geben. Kein frustrierendes, heiteres Auswahlarray, sondern eine begrenzte Anzahl von Auswahlmöglichkeiten, die die Benutzeranforderungen intelligent antizipieren. "Möchten Sie nicht mit der Maus navigieren? Hier können Sie die gleichen Dinge nur über die Tastatur durchführen. Möchten Sie keine physischen Tastaturen? Hier ist ein virtueller Computer, den Sie auf dem Bildschirm verwenden können."

Bieten Sie z. B. Flexibilität durch Folgendes:

-   Bereitstellen von vom Benutzer auswählbaren Entsprechungen für Nicht-Textelemente (z. B. alternativer Text für Grafiken und Untertitel für Audio).

    ![Screenshot der Anmeldeschaltfläche](images/inter-accessibility-image6.png)

    ![Screenshot des ALT-Texts für die Anmeldeschaltfläche](images/inter-accessibility-image7.png)

    Benutzer, die keine Grafiken rendern möchten, sollten stattdessen den alten Text sehen und beschreiben, was das Steuerelement tut und wie mit ihm interagiert werden soll.

-   Bereitstellung von Alternativen zur Farbe (z. B. Symboldifferenzierung oder Verwendung von Sounds).

    ![Screenshot von Symbolen in Graustufen (Graustufen) ](images/inter-accessibility-image8.png)

    In diesem Beispiel sind die Standardsymbole anhand ihrer Entwürfe leicht zu unterscheiden.

-   Sicherstellen des Tastaturzugriffs (z. B. ein Tabstopp für jedes interaktive Steuerelement), damit Benutzer die gleichen Aufgaben in Ihrem Programm mit der Maus oder der Tastatur ausführen können.
-   Stellen Sie sicher, dass Ihr Programm gute Farbkontrastoptionen für Benutzer bietet. Windows bietet eine Option mit hohem Kontrast, die jedoch als Lösung für schwerwiegende Sehbehinderung konzipiert ist. Andere Kontrastoptionen sind für Benutzer mit sehbehinderter Sehfähigkeit und Farbblindheit am besten geeignet.
-   Stellen Sie sicher, dass Benutzer die Größe des Texts auf der Benutzeroberfläche Ihres Programms anpassen können (z. B. über ein Schieberegler-Steuerelement oder ein Dropdownfeld für den Schriftgrad). Unterstützen Sie nach Möglichkeit den DPI-Modus (High Dots per Inch).
-   Stellen Sie sicher, dass Ihr Programm ein paarfach ist. Dies bedeutet, dass diese Benutzer eine Möglichkeit haben, das Problem zu umgehen, wenn auf den primären Modus des Programms für einige Benutzer nicht zugegriffen werden kann. Wenn z. B. Animationen angezeigt werden, sollten die Informationen in mindestens einem nicht animierten Präsentationsmodus auf der Option des Benutzers angezeigt werden können.

Über die schnittstellenischen Schnittstellen und die flexible Navigation verfügen Benutzer im Wesentlichen über die Architektur der Informationsredundanz. Redundanz weist manchmal negative Konnotationen auf. Im Text der Benutzeroberfläche empfiehlt es sich beispielsweise, redundanz zu entfernen, um die Leseerfahrung zu optimieren. Im Kontext der Barrierefreiheit stellt redundanz jedoch positive, ausfallsichere Mechanismen und Erfahrungen in Verbindung.

**Berücksichtigen Ihrer Benutzer**

Die Beachtung als allgemeines Leitprinzip ist für das Entwerfen barrierefreier Programme von entscheidender Bedeutung. Stellen Sie sich auch als geistige Übung vor, wie es aussehen muss, um Ihr Programm als benutzeraktiven Benutzer zu erleben. Nehmen Sie sich zeit, Ui-Bildschirme im Modus mit hohem Kontrast und mit verschiedenen Auflösungen zu testen, um sicherzustellen, dass die Benutzeroberfläche für Benutzer mit Sehbehinderung gut geeignet ist. Testen Sie den Tastaturzugriff, indem Sie das Kontrollkästchen **Tastenkombinationen und Zugriffsschlüssel unterstrichen** im Center für erleicherte Bedienung Systemsteuerung Element aktivieren (damit die Zugriffsschlüssel immer sichtbar sind). Sie können sogar über strenge Tests hinausgehen, indem Sie Entwickler und Designer einstellen, die eine natürliche Fähigkeit haben, sich mit anderen zu beschäftigen.

Außerdem sollten Sie dies durch Dies sollten Sie beachten:

-   Verwenden von systemweiten Einstellungen (z. B. Systemfarbe) anstelle von Hartverkabelungseinstellungen für Ihr bestimmtes Programm. Berücksichtigen Sie nicht nur die Parameter, die Benutzer speziell für die Interaktion mit ihren Programmen ausgewählt haben, sondern auch die in das Betriebssystem integrierten Barrierefreiheitsfunktionen, die der Benutzer unabhängig davon, welches Programm er verwendet, in Kraft setzen möchte. Weitere Informationen finden Sie unter [Informationen zu Windows-Barrierefreiheitsfunktionen.](/previous-versions//ms695605(v=vs.85))
-   Bevorzugen von allgemeinen Steuerelementen zu benutzerdefinierten Steuerelementen, da allgemeine Steuerelemente bereits die Windows-Barrierefreiheits-APIs implementiert haben.
-   Dokumentieren aller Barrierefreiheitsoptionen und -features (z. B. alle Tastenkombinationen). Benutzer mit Beeinträchtigungen sind stark daran interessiert, Barrierefreiheitsfeatures zu entdecken, und erwarten häufig, dass umfassende Informationen in der Hilfe gesammelt werden.
-   Erstellen einer barrierefreien Dokumentation in barrierefreien Formaten. Daher sollte die Dokumentation selbst die gleichen Regeln für die Barrierefreiheit wie die primäre Benutzeroberfläche einhalten, einschließlich der Möglichkeit, den Schriftgrad zu vergrößern, der Verwendung von alt geschriebenen Text für Grafiken und der redundanten Informationsarchitektur (z. B. die Verwendung von Farbcodierung nur als Ergänzung zu Text).

Bei Softwareprodukten kann sich die Beachtung der Benutzer in Benutzerfreundlichkeit und Marktforschung, in mühsamen Supportdiensten und Dokumentationen und natürlich in Entwurfsentscheidungen manifestieren. Denken Sie beispielsweise noch einmal an den Entwurf für fortgeschrittene Benutzer: Setzen Sie dieses innovative neue Feature in ein, weil Sie es wünschen, oder weil Sie wissen, dass Ihre erweiterten Benutzer nach ihm gefragt haben? Der zweite Fall gibt an, dass Ihr Entscheidungsfindungsprozess für den Entwurf durch den Wert der Beachtung gut informiert ist.

**Bereitstellen von programmgesteuertem Zugriff**

Die Bereitstellung von programmgesteuertem Zugriff auf die Benutzeroberfläche ist von entscheidender Bedeutung, damit Hilfstechnologien (z. B. Sprachausgaben, alternative Eingabegeräte und Spracherkennungsprogramme) den Bildschirm für ihre Benutzer richtig interpretieren. Indem Sie eine "Karte" der einzelnen Benutzeroberflächenbildschirme in Ihrem Programm erstellen, stellen Sie sie Benutzern von Hilfstechnologien zur Verfügung.

Gehen Sie wie folgt vor, um dies zu tun:

-   Aktivieren des programmgesteuerten Zugriffs auf alle Benutzeroberflächenelemente und Text (z. B. mithilfe der Active Accessibility COM-Schnittstelle, [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)).
-   Platzieren von Namen (oder Titeln) und Beschreibungen auf Benutzeroberflächenobjekten, Frames und Seiten (z. B. mithilfe der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Name-Eigenschaft).
-   Sicherstellen, dass programmgesteuerte Ereignisse von allen Benutzeroberflächenaktivitäten ausgelöst werden (z. B. Fokusereignisse für alle Aktivitäten der Benutzeroberfläche mit Fokusbewegung).

**Wenn Sie nur vier Dinge tun...**

1.  Stellen Sie sicher, dass jeder Benutzer das volle Potenzial Ihres Programms nutzen kann.
2.  Stellen Sie sich Barrierefreiheit als Chance für die lösungsintensiver Probleme und eine weitere Möglichkeit vor, die Benutzerzufriedenheit insgesamt zu steigern.
3.  Berücksichtigen Sie die Systemeinstellungen.
4.  Verwenden Sie nach Möglichkeit allgemeine Steuerelemente.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Unterbrechen oder deaktivieren Sie keine aktivierten Features des Betriebssystems oder anderer Produkte, die als Barrierefreiheitsfeatures identifiziert werden.** Sie können diese Features anhand der Dokumentation des betreffenden Betriebssystems oder Produkts identifizieren.
-   **Erzwingen Sie nicht, dass Benutzer mit Ihrem Programm als oberes Fenster auf dem Bildschirm interagieren.** Wenn eine Funktion oder ein Fenster kontinuierlich erforderlich ist, damit Benutzer eine Aufgabe ausführen können, sollte dieses Fenster immer sichtbar bleiben, wenn der Benutzer dies wählt, unabhängig von seiner Position relativ zu anderen Fenstern. Wenn der Benutzer beispielsweise über eine verschiebbare Bildschirmtastatur verfügt, die sich über allen anderen Fenstern befindet, sodass sie jederzeit sichtbar ist, sollte ihr Programm sie niemals verbergen, indem sie obligatorisch am oberen Rand der [Z-Reihenfolge](glossary.md)platziert wird.
-   **Verwenden Sie nach Möglichkeit Systemfarben, Schriftarten und allgemeine Steuerelemente.** Dadurch verringern Sie die Anzahl der Barrierefreiheitsprobleme, die Benutzern auftreten, erheblich.

### <a name="addressing-particular-impairments"></a>Beheben bestimmter Beeinträchtigungen

**Visual**

-   **Verlassen Sie sich niemals auf Farbe allein, um Bedeutung zu vermitteln.** Verwenden Sie Farbe nur als Mittel, um die Bedeutung von Text, Entwurf, Position oder Sound zu verbessern.

    ![Screenshot des roten Kommunikationssymbols und der QuickInfo ](images/inter-accessibility-image9.png)

    Die primäre Kommunikationsmethode in diesem Beispiel ist der präzise QuickInfo-Text. Die Verwendung von Farben hilft bei der Kommunikation der Bedeutung, ist aber sekundär.

-   **Verwenden Sie alternative (alt)-Textinfos, um Grafiken zu beschreiben.**
-   **Verwenden Sie keinen Text in Grafiken.** Benutzer mit Sehbehinderung können Grafiken deaktivieren (z. B. in einem Webbrowser) oder einfach keinen Text sehen oder suchen, der in Grafiken platziert ist.
-   **Stellen Sie sicher, dass Dialogfelder und Fenster aussagekräftige Namen haben,** damit ein Benutzer, der den Bildschirm nicht sieht (z. B. mit einer Sprachausgabe), entsprechende Kontextinformationen erhält.
-   **Beachten Sie die Einstellungen des Benutzers für die visuelle Anzeige,** indem Sie stets Schriftarten, Größen und Farben, Windows-Anzeigeelementgrößen und Systemkonfigurationseinstellungen aus den Design- und GetSystemMetrics-APIs abrufen.
-   **Halten Sie Sprechblasentext präzise,** damit er einfacher zu lesen ist, und minimieren Sie die Unterbrechung der Sprachausgabe.

    ![Screenshot des Sprechblasens, der Stecknadelcodelimits angibt ](images/inter-accessibility-image10.png)

    Obwohl Sprechblasen bei Bedarf zusätzlichen Text verwenden können, zeigt dieses Beispiel, dass Titeltext allein manchmal das gleiche Ziel auf kostengünstigere und zugänglichere Weise erreicht.

**Hörvermögen**

-   **Verlassen Sie sich niemals allein auf Sound, um Bedeutung zu vermitteln.** Verwenden Sie Sound nur als Mittel, um die Bedeutung von Text, Entwurf, Position oder Farbe zu verbessern.
-   **Ermöglichen Sie Es Benutzern, die Lautstärke der Audioausgabe zu steuern.** Verwenden Sie zu diesem Zweck den Windows-Volumemixer. Weitere Informationen finden Sie unter [Sound](vis-sound.md).
-   Richten Sie den Sound Ihres Programms so ein, dass er **in einem Bereich zwischen 500 Hz und 3.000 Hz auftritt,** oder lassen Sie sich einfach vom Benutzer in diesen Bereich anpassen. Laute in diesem Bereich sind höchstwahrscheinlich für Personen mit Hörbehinderung erkennbar.

**Geschicklichkeit**

-   **Ändern Sie die Ui-Timeoutwerte relativ zu GetDoubleClickTime(), anstatt absolute Zeiten zu verwenden.** Dadurch werden die Timeouts an die Geschwindigkeit des Benutzers angepasst.
-   **Weisen Sie allen Menüelementen Zugriffsschlüssel zu,** damit Benutzer, die lieber mit der Tastatur arbeiten, in Ihrem Programm genauso navigieren können wie Benutzer, die mit der Maus arbeiten.
-   **Führen Sie kein Doppelklicken und Ziehen aus, um eine Aktion auszuführen.** Dies kann für einige Benutzer schwierig sein.
-   **Entfernen Sie keine Menüleisten aus dem Programm.** Menüleisten sind einfacher als Symbolleisten, auf die Tastaturbenutzer zugreifen können. Wenn die Menüleiste standardmäßig nicht sichtbar sein soll, blenden Sie sie stattdessen aus.
-   **Machen Sie die Hilfe über die Tastatur zugänglich, indem Sie Tabstopps für Hilfeschaltflächen und Links bereitstellen.**
-   **Um das Bewusstsein für die Zuweisungen von Zugriffsschlüsseln in Ihrem Programm zu verbessern, können Sie sie jederzeit anzeigen.** Wechseln Sie in Systemsteuerung zum Center für erleicherte Bedienung, und klicken Sie auf **Die Tastatur einfacher zu verwenden.** Aktivieren Sie dann das Kontrollkästchen **Tastenkombinationen und Zugriffsschlüssel unterstrichen.**

**Kognitiv**

-   **Verwenden Sie die progressive Offenlegung,** um die Komplexität auszublenden.

    ![Screenshot der geteilten Schaltflächen mit nach unten geschalteten Dreiecken ](images/inter-accessibility-image11.png)

    In diesen Beispielen sind die über die Befehlsschaltfläche verfügbaren Optionen standardmäßig ausgeblendet, und Benutzer können die Optionen anzeigen, indem sie die Vorteile progressiver Offenlegungskontrollen nutzen.

-   **Verwenden Sie Symbole, Symbolleisten und andere visuelle Hilfen,** um die kognitive Auslastung des Lesens von Text zu reduzieren.
-   Stellen Sie nach Möglichkeit funktionen für die **automatische Vervollständigung in Textfeldern und bearbeitbaren Dropdownlisten** bereit, sodass Benutzer nicht den gesamten Namen von Befehlen, Dateinamen oder ähnlichen Optionen aus einem begrenzten Satz von Optionen eingeben müssen. Dies reduziert die kognitive Auslastung für alle Benutzer und verringert den Typisierungsaufwand für Benutzer, deren Rechtschreibung oder Eingabe schwierig, langsam oder schwierig ist.
-   **Veranschaulichen Sie schwierige Konzepte in der Hilfe, indem Sie Tutorials und Animationen hinzufügen.** Beachten Sie, dass Animationen für Benutzer mit Sehbehinderung schwierig sein können und daher nur bei Bedarf verwendet werden sollten.

**Beschlagnahme**

-   **Verwenden Sie keinen blinkenden oder blinkenden Text, keine Objekte oder andere Elemente mit einer Flash- oder Blinkfrequenz im Bereich zwischen 2 und 55 Hz.**
-   **Beschränken Sie die Verwendung von Animationen.** Einige Benutzer sind besonders empfindlich auf Bildschirmbewegungen, insbesondere im Visuellen. Wenn Sie Animationen verwenden, um die Aufmerksamkeit auf etwas zu ziehen, stellen Sie sicher, dass die Aufmerksamkeit auf den Benutzer zu achten und nicht unterbrochen werden kann.

**Sprache oder Sprache**

-   **Organisieren und Schreiben von klarem, präzisem, leicht verständlichen Text.** Benutzerfreundlichkeitstests zeigen, dass das Aufklappen wichtiger Informationen am Ende eines Ausdrucks das Verständnis verbessert. Weitere Richtlinien finden Sie unter [Stil und Ton.](text-style-tone.md)

**Falsch:**

Sind drei die nächste Ziffer?

Klicken Sie auf OK, um zu beginnen.

**Richtig:**

Ist die nächste Ziffer drei?

Klicken Sie zunächst auf OK.

### <a name="access-keys"></a>Zugriffsschlüssel

-   **Bevorzugen Sie Zeichen mit breiten Zeichen,** z. B. w, m und Großbuchstaben.
-   **Bevorzugen Sie einen konsonanten Konsonanten oder einen Vokal,** z. B. "x" in "Exit".
-   **Vermeiden Sie die Verwendung von Zeichen, die** die Unterstriche schwer zu erkennen machen, z. B. (von den problematischsten zu den am wenigsten problematischen):
    -   Zeichen, die nur ein Pixel breit sind, z. B. i und l.
    -   Zeichen mit absteigenden Zeichen, z. B. g, j, p, q und y.
    -   Zeichen neben einem Buchstaben mit einem absteigenden Zeichen.

### <a name="menu-access-keys"></a>Menüzugriffsschlüssel

-   **Weisen Sie allen Menüelementen Zugriffsschlüssel zu.** Keine Ausnahmen.
-   **Weisen Sie für dynamische Menüelemente (z. B. zuletzt verwendete Dateien) Zugriffsschlüssel numerisch zu.**

    ![Screenshot des geöffneten Menüs mit zuletzt verwendeten Dateien ](images/inter-accessibility-image12.png)

    In diesem Beispiel weist das Paint-Programm in Windows zuletzt verwendeten Dateien numerische Zugriffsschlüssel zu.

-   **Weisen Sie eindeutige Zugriffsschlüssel innerhalb einer Menüebene zu.** Sie können Zugriffsschlüssel auf verschiedenen Menüebenen wiederverwenden.
-   **Einfaches Aufschlüsseln von Zugriffsschlüsseln:**
    -   Wählen Sie für die am häufigsten verwendeten Menüelemente Zeichen am Anfang des ersten oder zweiten Worts der Bezeichnung aus, vorzugsweise das erste Zeichen.
    -   Wählen Sie für weniger häufig verwendete Menüelemente Buchstaben aus, die in der Bezeichnung ein charakteristischer Konsonant oder Vokal sind.

### <a name="dialog-box-access-keys"></a>Zugriffsschlüssel für Dialogfelder

-   **Weisen Sie nach Möglichkeit allen interaktiven Steuerelementen** oder deren Bezeichnungen eindeutige Zugriffsschlüssel zu. [Schreibgeschützte Textfelder sind](ctrl-text-boxes.md) interaktive Steuerelemente (da Benutzer scrollen und Text kopieren können), sodass sie von Zugriffsschlüsseln profitieren. **Weisen Sie keine Zugriffsschlüssel zu:**
    -   **Schaltflächen OK, Abbrechen und Schließen.** Eingabe und ESC werden für ihre Zugriffsschlüssel verwendet. Weisen Sie einem Steuerelement jedoch immer einen Zugriffsschlüssel zu, der OK oder Abbrechen bedeutet, aber eine andere Bezeichnung hat.

        ![Screenshot von Steuerelementen mit zugewiesenen Zugriffsschlüsseln ](images/inter-accessibility-image13.png)

        In diesem Beispiel ist der Schaltfläche für den positiven Commit ein Zugriffsschlüssel zugewiesen.

-   **Gruppenbezeichnungen.** Normalerweise werden den einzelnen Steuerelementen innerhalb einer Gruppe Zugriffsschlüssel zugewiesen, sodass die Gruppenbezeichnung keinen benötigt. Weisen Sie der Gruppenbezeichnung jedoch einen Zugriffsschlüssel zu, nicht den einzelnen Steuerelementen, wenn es zu einem Mangel an Zugriffsschlüsseln kommt.
-   **Generische Hilfeschaltflächen,** auf die mit F1 zugegriffen wird.
-   **Linkbezeichnungen.** Es gibt häufig zu viele Links, um eindeutige Zugriffsschlüssel zu zuweisen, und Link unterstriche blenden die Unterstriche der Zugriffsschlüssel aus. Lassen Sie benutzer stattdessen mit der TAB-TASTE auf Links zugreifen.
-   **Registerkartennamen.** Tabstopps werden mit STRG+TAB und STRG+UMSCHALT+TAB zyklen.
-   **Schaltflächen mit der Bezeichnung "..." durchsuchen.** Diesen können keine Zugriffsschlüssel eindeutig zugewiesen werden.
-   **Nicht bezeichnete Steuerelemente, z.** B. Drehsteuerelemente, grafische Befehlsschaltflächen und nicht bezeichnete Steuerelemente für die progressive Offenlegung.
-   **Nicht beschriftete statischer Text** oder Bezeichnungen für Steuerelemente, die nicht interaktiv sind, z. B. Statusleisten.
-   **Weisen Sie zuerst Zugriffsschlüssel für commit-Schaltflächen zu, um sicherzustellen, dass sie über die Standardschlüsselzuweisungen verfügen.** Wenn es keine Standardschlüsselzuweisung gibt, verwenden Sie den ersten Buchstaben des ersten Worts. Beispielsweise sollte der Zugriffsschlüssel für die Schaltflächen Ja und Nein commit immer "Y" und "N" sein, unabhängig von den anderen Steuerelementen im Dialogfeld.
-   **Weisen Sie für negative Commitschaltflächen (mit Anderen als Abbrechen), die als "Don't" (Nicht) formuliert sind, den Zugriffsschlüssel dem "n" in "Don't" zu.** Wenn sie nicht als "Nicht" bezeichnet werden, verwenden Sie die Standardzugriffsschlüsselzuweisung, oder weisen Sie den ersten Buchstaben des ersten Worts zu. Auf diese Weise verfügen alle Don'ts und No es über einen konsistenten Zugriffsschlüssel.
-   **Um zugriffsschlüssel** leicht zu finden, weisen Sie die Zugriffsschlüssel einem Zeichen zu, das früh in der Bezeichnung angezeigt wird, idealerweise das erste Zeichen, auch wenn später in der Bezeichnung ein Schlüsselwort angezeigt wird.

Weitere Richtlinien und Beispiele finden Sie unter [Tastatur](inter-keyboard.md).

## <a name="text"></a>Text

-   **Verwenden Sie Doppelpunkte am Ende externer Steuerelementbezeichnungen.** Einige Hilfstechnologien suchen nach Doppelpunkten, um Steuerelementbezeichnungen zu identifizieren.
-   **Positionieren Sie Bezeichnungen konsistent relativ zu den Elementen, die sie beschriften.** Dies hilft der Hilfstechnologie, die Bezeichnungen den entsprechenden Steuerelementen richtig zu zuordnen, und benutzer von Bildschirm vergrößernden Bildschirmen können wissen, wo sie nach einer Bezeichnung oder einem Steuerelement suchen müssen.

    ![Screenshot konsistent platzierter Bezeichnungen ](images/inter-accessibility-image14.png)

    In diesem Beispiel werden die Bezeichnungen für jede der Dropdownlisten konsistent platziert und verwenden Doppelpunkte.

-   **Beschränken Sie den alt-Text auf maximal 150 Zeichen.** Beschreiben Sie die Aktion zum Aktivieren des Steuerelements (z. B. Klicken, Klicken mit der rechten Maustaste und so weiter), und beschreiben Sie dann die Funktion des Steuerelements.

    **Annehmbar:**

    Schaltfläche.

    Blaues Blau.

    **Besser:**

    Klicken Sie auf diese Schaltfläche, um sich bei Ihrem Konto zu anmelden.

    Foto von entfernten Abständen, die zeigen, wie Farben über die Entfernung verblassen.

-   **Verwenden Sie keinen Text zum Zeichnen von Linien, Feldern oder anderen grafischen Symbolen.** Auf diese Weise verwendete Zeichen können Benutzer von Sprachbildschirmen verwirren. Beispielsweise wird ein Feld, das mit dem Buchstaben "X" um einen Textbereich gezeichnet wird, von der Sprachausgabesoftware als "X X X X X X" in der ersten Zeile gelesen, gefolgt von "X" und dem Inhalt und "X".

## <a name="documentation"></a>Dokumentation

-   Dokumentieren Sie alle Optionen und Features für die Barrierefreiheit (z. B. alle Tastenkombinationen).
-   Erstellen Sie barrierefreie Dokumentation in barrierefreien Formaten. Daher sollte die Dokumentation selbst denselben Regeln für die Barrierefreiheit entsprechen wie die primäre Benutzeroberfläche.
-   Weitere Informationen finden Sie unter Zugriffsschlüssel, keine Tastenkombinationen (die eine andere Bedeutung und Verwendung haben), mnemonische Schlüssel oder Zugriffstasten.
-   Im Allgemeinen bezieht sich auf eine Person mit einer Art von Behinderungen, nicht auf eine deaktivierte Person. Betrachten Sie zuerst die Person, nicht die Bezeichnung.



| Verwenden Sie diese Begriffe.           | Statt                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------|
| Hat eingeschränkte Dexterität, hat Bewegungsbehinderungen<br/>     | Crippled, lame<br/>                                                        |
| Ohne Behinderungen<br/>                               | Normal, füllvoll, fehlerfrei<br/>                                          |
| Einhändige Personen, die mit einer Hand eingeben<br/>          | Einhändig <br/>                                                        |
| Personen mit Behinderungen<br/>                           | Die deaktivierten, deaktivierten Personen, Die Mitbehinderten, die Verletzten<br/> |
| Kognitive Behinderungen, Entwicklungsbehinderungen<br/> |                                                                                  |



 

