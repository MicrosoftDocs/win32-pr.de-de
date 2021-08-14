---
title: Barrierefreiheit (Grundlagen des Entwurfs)
description: Das Entwerfen von Software für Barrierefreiheit bedeutet, sicherzustellen, dass Programme und Funktionen für eine breite Palette von Benutzern, einschließlich personen mit Behinderungen und Beeinträchtigungen, leicht verfügbar sind.
ms.assetid: df6947ec-6a1d-4645-ae3e-863839c32588
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c38eb3993880d820a4e65fa25a1e910e9e842de823779aaf3ef24dab8635e60e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118212499"
---
# <a name="accessibility-design-basics"></a>Barrierefreiheit (Grundlagen des Entwurfs)

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Das Entwerfen von Software für Barrierefreiheit bedeutet, sicherzustellen, dass Programme und Funktionen für eine breite Palette von Benutzern, einschließlich personen mit Behinderungen und Beeinträchtigungen, leicht verfügbar sind.

Die Anzahl der Benutzer, die Barrierefreiheitsfeatures ihnen helfen können, kann Sie versnannen. Beispielsweise haben Umfragen in der USA ergeben, dass mehr als die Hälfte aller Computerbenutzer Schwierigkeiten oder Beeinträchtigungen im Zusammenhang mit der Barrierefreiheit haben und wahrscheinlich von der Verwendung barrierefreier Technologien profitieren werden. Darüber hinaus führt der Ansatz des Softwareentwurfs mit der Flexibilität und Inklusivität, die das Merkmal der Barrierefreiheit sind, häufig zu einer insgesamt verbesserten Benutzerfreundlichkeit und Kundenzufriedenheit.

![Screenshot des Dialogfelds "Ease of Access Center" ](images/inter-accessibility-image1.png)

Der Center für erleicherte Bedienung, der über Systemsteuerung verfügbar ist, bietet einen zentralen Ort, an dem Benutzer die von ihnen bestimmten Barrierefreiheitsfeatures auswählen und anpassen können.

**Hinweis:** Richtlinien im Zusammenhang [mit Tastatur,](inter-keyboard.md) [Maus,](inter-mouse.md) [Farbe](vis-color.md) [und](vis-sound.md) Sound werden in separaten Artikeln vorgestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

Viele physische, wahrnehmungs- und kognitive Faktoren spielen bei der Interaktion von Benutzern mit Computerhardware und -software eine Rolle. Bevor Sie möglichkeiten in Betracht ziehen, die Funktionen Ihres Programms zugänglicher zu machen, sollten Sie sich darüber informieren, welche Arten von Behinderungen und Beeinträchtigungen vorhanden sind und mit welchen Hilfstechnologien diese Benutzer bei der Interaktion mit Computern arbeiten können.

### <a name="types-of-impairments"></a>Arten von Beeinträchtigungen

In der folgenden Tabelle werden häufige Benutzerbehinderungen und Beeinträchtigungen beschrieben, und es werden einige der wichtigsten Lösungen aufgeführt, die verwendet werden, um den Zugriff auf Computer zu verbessern.



| Wertminderung    | BESCHREIBUNG   | Lösungen  |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Visuelles Element<br/>             | Der Bereich reicht von "17 Prozent der Benutzer" bis zu "schwerwiegend" (von 9 Prozent der Benutzer betroffen).<br/>                                                                                                   | Anpassbare Vergrößerung, Farben und Kontraste; Braille-Hilfsprogramme; Sprachbildschirme.<br/>                                                                                       |
| Hörvermögen<br/>            | Reicht von "18 Prozent der Benutzer" bis zu "schwerwiegend" (von 2 Prozent der Benutzer betroffen).<br/>                                                                                                   | Informationsredundanz: Sound, der nur als Ergänzung zur Text- oder visuellen Kommunikation verwendet wird.<br/>                                                                                     |
| Geschicklichkeit<br/>          | Reicht von "19 Prozent der Benutzer" bis zu "schwerwiegend" (von 5 Prozent der Benutzer betroffen). Diese Beeinträchtigung umfasst häufig Schwierigkeiten beim Ausführen bestimmter motorischer Fähigkeiten mit Tastatur oder Maus.<br/> | Eingabemethoderedundanz: Programmfeatures, auf die per Maus oder Tastaturentsprechungen zugegriffen wird.<br/>                                                                                       |
| Kognitiv<br/>          | Schließt Beeinträchtigungen des Arbeitsspeichers und wahrnehmliche Unterschiede ein. Betrifft 16 Prozent der Benutzer.<br/>                                                                                                         | Stark anpassbare Benutzeroberfläche (UI); Verwendung der [progressiven Offenlegung,](ctrl-progressive-disclosure-controls.md) um die Komplexität auszublenden; Verwendung von Symbolen und anderen visuellen Hilfsmitteln.<br/> |
| Beschlagnahme<br/>            | Schließt visuelle Empfindlichkeit für Bewegung und Blinken ein.<br/>                                                                                                                                        | Konservativer Ansatz zum Modulieren von Schnittstellen, z. B. die Verwendung von Animationen; Vermeiden sie das Flackern des Bildschirms im Bereich zwischen 2 Hertz (Hz) und 55 Hz.<br/>                        |
| Sprache oder Sprache<br/> | Schließt Schwierigkeiten bei der Kommunikation mit Derexie und Derexie ein.<br/>                                                                                                                                       | Hilfsprogramme für Rechtschreib- und Grammatikprüfung; Spracherkennung und Text-zu-Sprache-Technologie.<br/>                                                                                 |



 

Weitere Richtlinien zur Unterstützung von Benutzern [](#addressing-particular-impairments) mit diesen Beeinträchtigungen finden Sie weiter unten in diesem Artikel unter Behandlung bestimmter Beeinträchtigungen.

### <a name="types-of-assistive-technologies-and-accessibility-features"></a>Typen von Hilfstechnologien und Barrierefreiheitsfeatures

**Sprachausgabe**

Mit einer Sprachausgabe können Benutzer mit sehbehinderten oder eingeschränkten Elementen in einer Benutzeroberfläche navigieren, indem sie Visuals in Audio transformieren. Daher werden Benutzeroberflächentext, Steuerelemente, Menüs, Symbolleisten, Grafiken und andere Bildschirmelemente von der computerisierten Stimme der Sprachausgabe gesprochen. Um ein für die Sprachausgabe-Hilfstechnologie optimiertes Programm zu erstellen, müssen Sie planen, wie die Sprachausgabe jedes Benutzeroberflächenelement identifiziert.

Auf jedes Benutzeroberflächenelement, mit dem der Benutzer interagieren kann, muss auf die Tastatur zugegriffen werden können, und es muss über eine Barrierefreiheits-API (Application Programming Interface, Anwendungsprogrammierschnittstelle) verfügbar gemacht werden. Es wird empfohlen, Benutzeroberflächenautomatisierung, das neue Barrierefreiheitsframework für alle Versionen von Microsoft Windows, die Windows Presentation Foundation (WPF) unterstützen. Benutzeroberflächenautomatisierung bietet programmgesteuerten Zugriff auf die meisten Elemente auf dem Desktop und ermöglicht es Hilfstechnologieprodukten wie Spracheingaben, Benutzern Informationen über die Benutzeroberfläche zur Verfügung zu stellen und die Benutzeroberfläche mit anderen Als-Standardeingaben zu bearbeiten (z. B. durch Sprechen anstelle von oder zusätzlich zum Bearbeiten der Maus oder Tastatur). Weitere Informationen finden Sie unter Benutzeroberflächenautomatisierung [Übersicht.](/dotnet/framework/ui-automation/ui-automation-overview)

Beachten Sie, dass die Sprachbildschirme zwar eine sehr wichtige Hilfstechnologie sind, es aber auch andere gibt. Weitere Informationen zu den verfügbaren Technologien finden Sie unter [Typen von Hilfstechnologieprodukten.](https://www.microsoft.com/enable/at/types.aspx)

**Spracherkennung**

Die Spracherkennung ist ein Barrierefreiheitsfeature in Windows, mit dem Benutzer per Stimme mit ihren Computern interagieren können, was die Notwendigkeit einer motorischen Interaktion mit der Maus oder Tastatur reduziert. Benutzer können Dokumente und E-Mails vorschreiben, Sprachbefehle verwenden, um Programme zu starten und zwischen ihnen zu wechseln, das Betriebssystem zu steuern und sogar Formulare im Web ausfüllen.

**Bildschirmlupe**

Die Vergrößerung hilft Benutzern mit Sehvermögen, indem elemente auf dem Bildschirm 2- bis 16-mal so oft wie das Original vergrößert werden. Benutzer können diese Funktion so festlegen, dass die Maus nachverfolgt wird (um eine vergrößerte Version des Mauszeigers zu sehen), die Tastatur (um den Bereich zu sehen, in dem sich der Mauszeiger bewegt, wenn die Tabulatortaste gedrückt wird) oder die Textbearbeitung (um zu sehen, was sie eingeben).

**Visuelle Einstellungen und Farbschemas**

Benutzer mit Sehbehinderung können nicht nur die Bildschirmgröße [](glossary.md) vergrößern, sondern auch von Systemeinstellungen wie dem Modus mit hohem Kontrast oder der Möglichkeit, Hintergrund- und Vordergrundfarbschemas anzupassen.

**Narrator**

Die Sprachausgabe ist eine herunterskalierte Sprachausgabe in Windows, mit der Benutzer Text und Benutzeroberflächenelemente auf dem Bildschirm laut hören können, einschließlich einiger Ereignisse (einschließlich Fehlermeldungen), die unerhört geschehen. Der Benutzer kann die Menüs der Sprachausgabe hören, ohne das aktive Fenster zu verlassen.

![Screenshot des Dialogfelds "Microsoft-Sprachausgabe" ](images/inter-accessibility-image2.png)

Benutzer können das Ausmaß anpassen, in dem die Microsoft-Sprachausgabe verwendet wird.

**Bildschirmtastatur**

Für Benutzer, die Schwierigkeiten mit physischen Tastaturen haben und ein alternatives Eingabegerät wie einen Schalter verwenden müssen, sind Bildschirmtastaturen eine Notwendigkeit. Benutzer können Tasten mit der Maus oder einem anderen zeigenden Gerät, einer kleinen Gruppe von Schlüsseln oder nur einer Taste auswählen, je nachdem, wie Sie die Bildschirmtastatur eingerichtet haben.

**Tastaturmaus**

Wenn Die Maustasten aktiviert sind, können Benutzer, die die Tastatur bevorzugen, die Pfeiltasten auf der numerischen Tastatur verwenden, um den Mauszeiger zu bewegen.

Eine vollständige Liste der Barrierefreiheitsfeatures finden Sie unter Barrierefreiheit [in Windows Vista](https://www.microsoft.com/enable/products/windowsvista/default.aspx) auf der Microsoft-Website.

### <a name="keyboard-based-navigation"></a>Tastaturbasierte Navigation

Die TAB-TASTE, die Pfeiltasten, die Leerzeichenleiste und die EINGABETASTE sind für die tastaturbasierte Navigation wichtig. Durch Drücken der [TAB-TASTE](glossary.md) wird der Eingabefokus durch die verschiedenen Steuerelementgruppen bewegt, und durch Drücken der Pfeiltasten wird innerhalb eines Steuerelements oder zwischen Steuerelementen innerhalb einer Gruppe bewegt. Das Drücken der Leerzeichenleiste ist identisch mit dem Klicken auf das Steuerelement mit dem Eingabefokus, während das Drücken der EINGABETASTE mit dem Klicken auf die Standardbefehlsschaltfläche oder den Befehlslink identisch ist, unabhängig vom Eingabefokus.

![Screenshot des Dialogfelds "Leerer Papierkorb" ](images/inter-accessibility-image3.png)

In diesem Beispiel können Benutzer die TAB-TASTE drücken, bis die gewünschte Option den Eingabefokus besitzt, und dann die EINGABETASTE drücken, um das Objekt zu öffnen.

### <a name="access-keys"></a>Zugriffsschlüssel

Mit Zugriffsschlüsseln können Benutzer Optionen auswählen und Befehle direkt initiieren, ohne zuerst zum Steuerelement navigieren zu müssen. Zugriffsschlüssel werden durch Unterschriften eines der Zeichen in der Bezeichnung jedes Steuerelements angegeben. Benutzer aktivieren dann die Option oder den Befehl, indem sie die ALT-TASTE zusammen mit dem unterstrichenen Zeichen drücken. Bei Zugriffsschlüsseln wird die Schreibung nicht beachtet.

![Screenshot des Dateimenüs und der Zugriffsschlüssel ](images/inter-accessibility-image4.png)

In diesem Beispiel wird durch Drücken von ALT+O der Befehl Öffnen aktiviert.

Die Auswahl logischer Zugriffsschlüssel für Steuerelemente stellt in der Regel keine Schwierigkeiten mit sich. Je mehr Steuerelemente es in einem Fenster gibt, desto größer ist jedoch die Wahrscheinlichkeit, dass Ihnen die Zugriffsschlüsseloptionen nicht mehr zur Verfügung stehen. Weisen Sie in diesem Fall Zugriffsschlüssel steuerungsgruppen zu, nicht jeder einzelnen Gruppe.

![Screenshot von Steuerelementgruppen und Zugriffsschlüsseln ](images/inter-accessibility-image5.png)

In diesem Beispiel werden Zugriffsschlüssel Steuerelementgruppen und nicht einzelnen Steuerelementen zugewiesen.

Zugriffsschlüssel werden häufig mit Tastenkombinationen verwechselt, aber Tastenkombinationen werden anders zugewiesen als Zugriffsschlüssel und haben unterschiedliche Ziele. Tastenkombinationen verwenden z. B. STRG- und Funktionstastensequenzen und sind in erster Linie als Verknüpfung für fortgeschrittene Benutzer und nicht als Barrierefreiheit gedacht.

Weitere Informationen finden Sie unter [Tastatur](inter-keyboard.md).

### <a name="designing-for-accessibility-three-fundamental-practices"></a>Entwerfen für Barrierefreiheit: drei grundlegende Methoden

Barrierefreie Programme helfen allen Benutzern in irgendeiner Weise, da sich die Ziele von Barrierefreiheit und Benutzerfreundlichkeit überschneiden. Beispielsweise profitieren Features, die fortgeschrittene Benutzer so effizient wie möglich machen, auch von Benutzern, die die Tastatur aufgrund von Beeinträchtigungen der Dexterität bevorzugen.

Drei grundlegende Vorgehensweisen unterstützen Sie bei barrierefreien Designs: Ermöglichen Sie ein gewisses Maß an Flexibilität in Ihrer Benutzeroberfläche, lassen Sie die Einhaltung von Benutzeranforderungen und -einstellungen eine wichtige Rolle bei Entwurfsentscheidungen spielen, und stellen Sie programmgesteuerten Zugriff auf Ihre Benutzeroberfläche zur Verfügung.

**Bereitstellen einer flexiblen Benutzeroberfläche**

Beim barrierefreien Design geht es zumindest teilweise darum, Benutzern Auswahlmöglichkeiten zu geben. Kein frustrierendes, schwindliges Array von Auswahlmöglichkeiten, sondern eine begrenzte Anzahl von Optionen, die Benutzeranforderungen intelligent voraussehen. "Sie möchten nicht mit der Maus navigieren? Hier können Sie die gleichen Dinge nur mit der Tastatur tun. Sie möchten keine physischen Tastaturen? Hier ist ein virtueller Computer, den Sie auf dem Bildschirm verwenden können."

Bieten Sie z. B. Flexibilität durch Folgendes:

-   Bereitstellen von vom Benutzer auswählbaren Entsprechungen für Nicht-Textelemente (z. B. alternativer Text für Grafiken und Untertitel für Audio).

    ![Screenshot der Anmeldeschaltfläche](images/inter-accessibility-image6.png)

    ![Screenshot des ALT-Texts für die Anmeldeschaltfläche](images/inter-accessibility-image7.png)

    Benutzer, die keine Grafiken rendern möchten, sollten stattdessen den alten Text sehen, der beschreibt, was das Steuerelement tut und wie mit ihm interagiert wird.

-   Bereitstellung von Alternativen zur Farbe (z. B. Symboldifferenzierung oder Verwendung von Sounds).

    ![Screenshot von Symbolen in Graustufen (Graustufen) ](images/inter-accessibility-image8.png)

    In diesem Beispiel sind die Standardsymbole anhand ihrer Entwürfe leicht zu unterscheiden.

-   Sicherstellen des Tastaturzugriffs (z. B. ein Tabstopp für jedes interaktive Steuerelement), damit Benutzer die gleichen Aufgaben in Ihrem Programm mit der Maus oder der Tastatur ausführen können.
-   Stellen Sie sicher, dass Ihr Programm gute Farbkontrastoptionen für Benutzer bietet. Windows bietet eine Option mit hohem Kontrast, aber dies ist wirklich als Lösung für schwerwiegende Sehbehinderung konzipiert. Andere Kontrastoptionen sind für Benutzer mit sehbehinderter Sehfähigkeit und Farbblindheit am besten geeignet.
-   Stellen Sie sicher, dass Benutzer die Größe des Texts auf der Benutzeroberfläche Ihres Programms anpassen können (z. B. über ein Schieberegler-Steuerelement oder ein Dropdownfeld für den Schriftgrad). Unterstützen Sie nach Möglichkeit den DPI-Modus (High Dots per Inch).
-   Stellen Sie sicher, dass Ihr Programm ein paarfach ist. Dies bedeutet, dass diese Benutzer eine Möglichkeit haben, das Problem zu umgehen, wenn auf den primären Modus des Programms für einige Benutzer nicht zugegriffen werden kann. Wenn z. B. animation angezeigt wird, sollten die Informationen in mindestens einem nicht animierten Präsentationsmodus auf Der Option des Benutzers angezeigt werden können.

Über die schnittstellenischen Schnittstellen und die flexible Navigation verfügen Benutzer im Wesentlichen über die Architektur der Informationsredundanz. Redundanz weist manchmal negative Konnotationen auf. Im Text der Benutzeroberfläche empfiehlt es sich beispielsweise, redundanz zu entfernen, um die Leseerfahrung zu optimieren. Im Kontext der Barrierefreiheit stellt redundanz jedoch positive, ausfallsichere Mechanismen und Erfahrungen in Verbindung.

**Berücksichtigen Ihrer Benutzer**

Die Beachtung als allgemeines Leitprinzip ist für das Entwerfen barrierefreier Programme von entscheidender Bedeutung. Stellen Sie sich selbst als geistige Übung vor, wie es aussehen muss, um Ihr Programm als benutzeraktiven Benutzer zu erleben. Nehmen Sie sich zeit, Ui-Bildschirme im Modus mit hohem Kontrast und mit verschiedenen Auflösungen zu testen, um sicherzustellen, dass die Benutzeroberfläche für Benutzer mit Sehbehinderung gut geeignet ist. Testen Sie den Tastaturzugriff, indem Sie das Kontrollkästchen **Tastenkombinationen und Zugriffsschlüssel unterstrichen** im Center für erleicherte Bedienung Systemsteuerung Element aktivieren (damit Die Zugriffsschlüssel immer sichtbar sind). Sie können sogar über strenge Tests hinausgehen, indem Sie Entwickler und Designer einstellen, die eine natürliche Fähigkeit haben, sich mit anderen zu beschäftigen.

Sie sollten auch Denk an den Tag legen, indem Sie:

-   Verwenden von systemweiten Einstellungen (z. B. Systemfarbe) anstelle von Hartverkabelungseinstellungen für Ihr bestimmtes Programm. Berücksichtigen Sie nicht nur die Parameter, die Benutzer speziell für die Interaktion mit ihren Programmen ausgewählt haben, sondern auch die in das Betriebssystem integrierten Barrierefreiheitsfunktionen, die der Benutzer unabhängig davon, welches Programm er verwendet, in Kraft setzen möchte. Weitere Informationen finden Sie unter [Informationen Windows Barrierefreiheitsfunktionen.](/previous-versions//ms695605(v=vs.85))
-   Bevorzugen von allgemeinen Steuerelementen zu benutzerdefinierten Steuerelementen, da allgemeine Steuerelemente bereits die Windows Barrierefreiheits-APIs implementiert haben.
-   Dokumentieren aller Barrierefreiheitsoptionen und -features (z. B. alle Tastenkombinationen). Benutzer mit Beeinträchtigungen sind stark daran interessiert, Barrierefreiheitsfeatures zu entdecken, und erwarten häufig, dass umfassende Informationen in der Hilfe gesammelt werden.
-   Erstellen barrierefreier Dokumentation in barrierefreien Formaten. Daher sollte die Dokumentation selbst die gleichen Regeln für die Barrierefreiheit wie die primäre Benutzeroberfläche einhalten, einschließlich der Möglichkeit, den Schriftgrad zu vergrößern, der Verwendung von alt geschriebenen Text für Grafiken und der redundanten Informationsarchitektur (z. B. die Verwendung von Farbcodierung nur als Ergänzung zu Text).

Bei Softwareprodukten kann sich die Beachtung der Benutzer in Benutzerfreundlichkeit und Marktforschung, in mühsamen Supportdiensten und Dokumentationen und natürlich in Entwurfsentscheidungen manifestieren. Denken Sie beispielsweise noch einmal an den Entwurf für fortgeschrittene Benutzer: Setzen Sie dieses innovative neue Feature in ein, weil Sie es wünschen, oder weil Sie wissen, dass Ihre erweiterten Benutzer nach ihm gefragt haben? Der zweite Fall gibt an, dass Ihr Entscheidungsfindungsprozess für den Entwurf durch den Wert der Beachtung gut informiert ist.

**Bereitstellen von programmgesteuertem Zugriff**

Die Bereitstellung von programmgesteuertem Zugriff auf die Benutzeroberfläche ist wichtig, damit Hilfstechnologien (z. B. Sprachausgaben, alternative Eingabegeräte und Spracherkennungsprogramme) den Bildschirm für ihre Benutzer richtig interpretieren. Indem Sie eine "Karte" der einzelnen Benutzeroberflächenbildschirme in Ihrem Programm erstellen, stellen Sie sie Benutzern von Hilfstechnologien zur Verfügung.

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
-   **Erzwingen Sie nicht, dass Benutzer mit Ihrem Programm als oberes Fenster auf dem Bildschirm interagieren.** Wenn eine Funktion oder ein Fenster kontinuierlich erforderlich ist, damit Benutzer eine Aufgabe ausführen können, sollte dieses Fenster immer sichtbar bleiben, wenn der Benutzer dies wählt, unabhängig von seiner Position relativ zu anderen Fenstern. Wenn der Benutzer beispielsweise über eine verschiebbare Bildschirmtastatur verfügt, die sich über allen anderen Fenstern befindet, sodass sie jederzeit sichtbar ist, sollte ihr Programm sie niemals durch obligatorische Platzierung oben in der [Z-Reihenfolge](glossary.md)verbergen.
-   **Verwenden Sie nach Möglichkeit Systemfarben, Schriftarten und allgemeine Steuerelemente.** Dadurch verringern Sie die Anzahl der Barrierefreiheitsprobleme, die Benutzern auftreten, erheblich.

### <a name="addressing-particular-impairments"></a>Beheben bestimmter Beeinträchtigungen

**Visual**

-   **Verlassen Sie sich niemals auf Farbe allein, um Bedeutung zu vermitteln.** Verwenden Sie Farbe nur als Mittel, um die Bedeutung von Text, Entwurf, Position oder Sound zu verbessern.

    ![Screenshot des roten Kommunikationssymbols und der QuickInfo ](images/inter-accessibility-image9.png)

    Die primäre Kommunikationsmethode in diesem Beispiel ist der präzise QuickInfo-Text. Die Verwendung von Farben hilft bei der Kommunikation der Bedeutung, ist aber sekundär.

-   **Verwenden Sie alternative (alt)-Textinfos, um Grafiken zu beschreiben.**
-   **Verwenden Sie keinen Text in Grafiken.** Benutzer mit Sehbehinderung können Grafiken deaktivieren (z. B. in einem Webbrowser) oder einfach keinen Text sehen oder suchen, der in Grafiken platziert ist.
-   **Stellen Sie sicher, dass Dialogfelder und Fenster aussagekräftige Namen haben,** damit ein Benutzer, der den Bildschirm nicht sieht (z. B. mit einer Sprachausgabe), entsprechende Kontextinformationen erhält.
-   **Beachten Sie die Einstellungen des Benutzers für die visuelle Anzeige,** indem Sie stets Schriftarten, Größen und Farben, Windows Anzeigeelementgrößen und Systemkonfigurationseinstellungen aus den Design- und GetSystemMetrics-APIs abrufen.
-   **Halten Sie den Sprechblasentext präzise,** damit er einfacher zu lesen ist und die Unterbrechung der Sprachausgabe minimiert wird.

    ![Screenshot des Sprechblasens, der Stecknadelcodelimits angibt ](images/inter-accessibility-image10.png)

    Obwohl Sprechblasen bei Bedarf zusätzlichen Text verwenden können, zeigt dieses Beispiel, dass Titeltext allein manchmal das gleiche Ziel auf kostengünstigere und zugänglichere Weise erreicht.

**Hörvermögen**

-   **Verlassen Sie sich niemals allein auf Sound, um Bedeutung zu vermitteln.** Verwenden Sie Sound nur als Mittel, um die Bedeutung von Text, Entwurf, Position oder Farbe zu verbessern.
-   **Ermöglichen Sie Es Benutzern, die Lautstärke der Audioausgabe zu steuern.** Verwenden Sie zu diesem Zweck die Windows Volume Mixer. Weitere Informationen finden Sie unter [Sound](vis-sound.md).
-   Richten Sie den Sound Ihres Programms so ein, dass er **in einem Bereich zwischen 500 Hz und 3.000 Hz auftritt** oder einfach vom Benutzer in diesen Bereich angepasst werden kann. Laute in diesem Bereich sind höchstwahrscheinlich für Personen mit Hörbehinderung erkennbar.

**Geschicklichkeit**

-   **Ändern Sie die Ui-Timeoutwerte relativ zu GetDoubleClickTime(), anstatt absolute Zeiten zu verwenden.** Dadurch werden die Timeouts an die Geschwindigkeit des Benutzers angepasst.
-   **Weisen Sie allen Menüelementen Zugriffsschlüssel zu,** damit Benutzer, die lieber mit der Tastatur arbeiten, in Ihrem Programm genauso navigieren können wie Benutzer, die mit der Maus arbeiten.
-   **Führen Sie kein Doppelklicken und Ziehen aus, um eine Aktion auszuführen.** Dies kann für einige Benutzer schwierig sein.
-   **Entfernen Sie keine Menüleisten aus dem Programm.** Menüleisten sind einfacher als Symbolleisten, auf die Tastaturbenutzer zugreifen können. Wenn die Menüleiste standardmäßig nicht sichtbar sein soll, blenden Sie sie stattdessen aus.
-   **Machen Sie die Hilfe über die Tastatur zugänglich, indem Sie Tabstopps für Hilfeschaltflächen und Links bereitstellen.**
-   **Um das Bewusstsein für die Zuweisungen von Zugriffsschlüsseln in Ihrem Programm zu verbessern, können Sie sie jederzeit anzeigen.** Wechseln Sie in Systemsteuerung zum Center für erleicherte Bedienung, und klicken Sie auf **Die Tastatur ist einfacher zu verwenden.** Aktivieren Sie dann das Kontrollkästchen **Tastenkombinationen und Zugriffsschlüssel unterstrichen.**

**Kognitiv**

-   **Verwenden Sie die progressive Offenlegung,** um die Komplexität auszublenden.

    ![Screenshot der geteilten Schaltflächen mit nach unten geschalteten Dreiecken ](images/inter-accessibility-image11.png)

    In diesen Beispielen sind die über die Befehlsschaltfläche verfügbaren Optionen standardmäßig ausgeblendet, und Benutzer können die Optionen anzeigen, indem sie die Vorteile progressiver Offenlegungskontrollen nutzen.

-   **Verwenden Sie Symbole, Symbolleisten und andere visuelle Hilfen,** um die kognitive Auslastung des Lesens von Text zu reduzieren.
-   Stellen Sie nach Möglichkeit funktionen für die **automatische Vervollständigung in Textfeldern und bearbeitbaren Dropdownlisten** bereit, damit Benutzer nicht den gesamten Namen von Befehlen, Dateinamen oder ähnlichen Optionen aus einem begrenzten Satz von Optionen eingeben müssen. Dies verringert die kognitive Last für alle Benutzer und die Menge der Eingaben für Benutzer, deren Rechtschreibung oder Eingabe schwierig, langsam oder mühsam ist.
-   **Zeigen Sie schwierige Konzepte in der Hilfe, indem Sie Tutorials und Animationen einschließen.** Beachten Sie, dass Animationen für Benutzer mit eingeschränkter Beeinträchtigung schwierig sein können und daher nur bei Bedarf verwendet werden sollten.

**Beschlagnahme**

-   **Verwenden Sie kein Blinken oder Blinken von Text, Objekten oder anderen Elementen mit einer Blitz- oder Blinkfrequenz im Bereich zwischen 2 und 55 Hz.**
-   **Beschränken Sie die Verwendung von Animationen.** Einige Benutzer sind besonders empfindlich auf Bildschirmbewegungen, insbesondere in der Peripherie ihres visuellen Felds. Wenn Sie animation verwenden, um die Aufmerksamkeit auf etwas zu lenken, stellen Sie sicher, dass die Aufmerksamkeit lohnt und der Benutzer unterbrochen wird.

**Sprache oder Sprache**

-   **Organisieren und schreiben Sie klaren, präzisen und leicht verständlichen Text.** Benutzerfreundlichkeitstests zeigen, dass das Aufklappen wichtiger Informationen am Ende eines Ausdrucks das Verständnis verbessert. Weitere Richtlinien finden Sie unter [Stil und Ton](text-style-tone.md).

**Falsch:**

Ist drei die nächste Ziffer?

Klicken Sie auf OK, um zu beginnen.

**Richtig:**

Ist die nächste Ziffer drei?

Klicken Sie zunächst auf OK.

### <a name="access-keys"></a>Zugriffsschlüssel

-   **Bevorzugen Sie Zeichen mit breiter Breite,** z. B. w, m und Großbuchstaben.
-   **Bevorzugen Sie einen typischen Konsonanten oder einen Vokal,** z. B. "x" in "Exit".
-   **Vermeiden Sie die Verwendung von Zeichen, die die Unterstreichung schwierig zu erkennen machen,** z. B. (von den problematischsten bis zu den am wenigsten problematischen):
    -   Zeichen, die nur ein Pixel breit sind, z. B. i und l.
    -   Zeichen mit Nachfolgern wie g, j, p, q und y.
    -   Zeichen neben einem Buchstaben mit einem Nachfolger.

### <a name="menu-access-keys"></a>Menüzugriffsschlüssel

-   **Weisen Sie allen Menüelementen Zugriffsschlüssel zu.** Keine Ausnahmen.
-   **Weisen Sie zugriffstasten für dynamische Menüelemente (z. B. zuletzt verwendete Dateien) numerisch zu.**

    ![Screenshot des geöffneten Menüs mit zuletzt verwendeten Dateien ](images/inter-accessibility-image12.png)

    In diesem Beispiel weist das Paint-Programm in Windows zuletzt verwendeten Dateien numerische Zugriffsschlüssel zu.

-   **Weisen Sie eindeutige Zugriffsschlüssel innerhalb einer Menüebene zu.** Sie können Zugriffsschlüssel auf verschiedenen Menüebenen wiederverwenden.
-   **Einfaches Auffinden von Zugriffsschlüsseln:**
    -   Wählen Sie für die am häufigsten verwendeten Menüelemente Zeichen am Anfang des ersten oder zweiten Worts der Bezeichnung aus, vorzugsweise das erste Zeichen.
    -   Wählen Sie für weniger häufig verwendete Menüelemente Buchstaben aus, die ein eindeutiger Konsonant oder ein Vokal in der Bezeichnung sind.

### <a name="dialog-box-access-keys"></a>Zugriffsschlüssel im Dialogfeld

-   **Weisen Sie nach Möglichkeit allen interaktiven Steuerelementen oder deren Bezeichnungen eindeutige Zugriffsschlüssel zu.** [Schreibgeschützte Textfelder](ctrl-text-boxes.md) sind interaktive Steuerelemente (da Benutzer sie scrollen und Text kopieren können), sodass sie von Zugriffsschlüsseln profitieren. **Weisen Sie folgenden Benutzern keine Zugriffsschlüssel zu:**
    -   **Die Schaltflächen OK, Abbrechen und Schließen.** Eingabe und ESC werden für ihre Zugriffsschlüssel verwendet. Weisen Sie einem Steuerelement jedoch immer einen Zugriffsschlüssel zu, der OK oder Abbrechen bedeutet, aber eine andere Bezeichnung aufweist.

        ![Screenshot der Steuerelemente mit zugewiesenen Zugriffsschlüsseln ](images/inter-accessibility-image13.png)

        In diesem Beispiel ist der Schaltfläche für positive Commits ein Zugriffsschlüssel zugewiesen.

-   **Gruppenbezeichnungen.** Normalerweise werden den einzelnen Steuerelementen innerhalb einer Gruppe Zugriffsschlüssel zugewiesen, sodass die Gruppenbezeichnung keine benötigt. Weisen Sie jedoch der Gruppenbezeichnung und nicht den einzelnen Steuerelementen einen Zugriffsschlüssel zu, wenn es zu einem Mangel an Zugriffsschlüsseln kommt.
-   **Generische Hilfeschaltflächen,** auf die mit F1 zugegriffen wird.
-   **Linkbezeichnungen.** Es gibt häufig zu viele Links, um eindeutige Zugriffsschlüssel zuzuweisen, und Link-Unterstriche blenden die Unterstriche der Zugriffsschlüssel aus. Verwenden Sie stattdessen Benutzerzugriffslinks mit der TAB-TASTE.
-   **Registerkartennamen.** Registerkarten werden mit STRG+TAB und STRG+UMSCHALT+TAB zyklust.
-   **Schaltflächen zum Durchsuchen mit der Bezeichnung "...".** Diesen können keine eindeutigen Zugriffsschlüssel zugewiesen werden.
-   Steuerelemente ohne **Bezeichnung,** z. B. Drehsteuerelemente, Schaltflächen für grafische Befehle und steuerelemente für die progressive Offenlegung ohne Bezeichnungen.
-   **Nicht bezeichnungsbasierter statischer Text oder Bezeichnungen für Steuerelemente, die nicht interaktiv sind,** z. B. Statusleisten.
-   **Weisen Sie zunächst Zugriffsschlüssel für commit-Schaltflächen zu, um sicherzustellen, dass sie über die Standardschlüsselzuweisungen verfügen.** Wenn keine Standardschlüsselzuweisung vorhanden ist, verwenden Sie den ersten Buchstaben des ersten Worts. Beispielsweise sollte der Zugriffsschlüssel für die Schaltflächen Ja und Kein Commit immer "Y" und "N" sein, unabhängig von den anderen Steuerelementen im Dialogfeld.
-   **Weisen Sie für negative Commitschaltflächen (mit Ausnahme von Abbrechen), die als "Nicht" bezeichnet werden, den Zugriffsschlüssel dem "n" in "Don't" zu.** Wenn sie nicht als "Nicht" bezeichnet werden, verwenden Sie die Standardmäßige Zuweisung des Zugriffsschlüssels, oder weisen Sie den ersten Buchstaben des ersten Worts zu. Auf diese Weise verfügen alle Don'ts und Nos über einen konsistenten Zugriffsschlüssel.
-   **Um die Suche nach Zugriffsschlüsseln zu vereinfachen, weisen Sie die Zugriffsschlüssel einem Zeichen zu, das früh in der Bezeichnung angezeigt wird,** idealerweise dem ersten Zeichen, auch wenn ein Schlüsselwort vorhanden ist, das später in der Bezeichnung angezeigt wird.

Weitere Richtlinien und Beispiele finden Sie unter [Tastatur.](inter-keyboard.md)

## <a name="text"></a>Text

-   **Verwenden Sie Doppelpunkte am Ende externer Steuerelementbezeichnungen.** Einige Hilfstechnologien suchen nach Doppelpunkte, um Steuerelementbezeichnungen zu identifizieren.
-   **Positionieren Sie Bezeichnungen konsistent relativ zu den Elementen, die sie bezeichnen.** Dies hilft der Hilfstechnologie, die Bezeichnungen den entsprechenden Steuerelementen ordnungsgemäß zuzuordnen, und benutzern von Bildschirmvergrößerungen zu helfen, zu wissen, wo nach einer Bezeichnung oder einem Steuerelement gesucht werden soll.

    ![Screenshot der konsistent platzierten Bezeichnungen ](images/inter-accessibility-image14.png)

    In diesem Beispiel werden die Bezeichnungen für jede der Dropdownlisten konsistent platziert und verwenden Doppelpunkte.

-   **Beschränken Sie den alt-Text auf maximal 150 Zeichen.** Beschreiben Sie die Aktion zum Aktivieren des Steuerelements (z. B. Klicken, Rechtsklick usw.), und beschreiben Sie dann die Funktion des Steuerelements.

    **Annehmbar:**

    Schaltfläche.

    Blauer Heiter.

    **Besser:**

    Klicken Sie auf diese Schaltfläche, um sich bei Ihrem Konto anzumelden.

    Foto von entfernten Farben, das zeigt, wie Farben über die Entfernung verblassen.

-   **Verwenden Sie keinen Text, um Linien, Felder oder andere grafische Symbole zu zeichnen.** Auf diese Weise verwendete Zeichen können Benutzer von Sprachausgaben verwirren. Beispielsweise wird ein Feld, das mit dem Buchstaben "X" um einen Textbereich gezeichnet wird, von der Sprachausgabesoftware als "X X X X X X" in der ersten Zeile gelesen, gefolgt von "X" und dem Inhalt und "X".

## <a name="documentation"></a>Dokumentation

-   Dokumentieren Sie alle Barrierefreiheitsoptionen und -features (z. B. alle Tastenkombinationen).
-   Erstellen Sie barrierefreie Dokumentation in barrierefreien Formaten. Daher sollte die Dokumentation selbst die gleichen Regeln für die Barrierefreiheit einhalten wie die primäre Benutzeroberfläche.
-   Weitere Informationen finden Sie unter Zugriffsschlüssel, keine Tastenkombinationen (die eine andere Bedeutung haben und verwendet werden), mnemonic-Schlüssel oder Zugriffstasten.
-   Im Allgemeinen bezieht sich auf eine Person mit einer Art von Behinderungen, nicht auf eine deaktivierte Person. Betrachten Sie zuerst die Person, nicht die Bezeichnung.



| Verwenden Sie diese Bedingungen.           | Statt                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------|
| Eingeschränkte Fingerfertigkeit, Bewegungsbeeinträchtigungen<br/>     | Lahm, lahm<br/>                                                        |
| Ohne Behinderungen<br/>                               | Normal, fähig, fehlerfrei<br/>                                          |
| Einhändige Personen, die mit einer Hand eingeben<br/>          | Einzelhändig <br/>                                                        |
| Menschen mit Behinderungen<br/>                           | Die deaktivierten, deaktivierten Personen, Die Menschen mit Schenkungen, die<br/> |
| Kognitive Behinderungen, Entwicklungsbeeinträchtigungen<br/> |                                                                                  |



 

