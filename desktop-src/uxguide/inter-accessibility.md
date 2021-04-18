---
title: Barrierefreiheit (Entwurfs Grundlagen)
description: Das Entwerfen von Software für Barrierefreiheit bedeutet, sicherzustellen, dass Programme und Funktionen für die größte Anzahl von Benutzern problemlos verfügbar sind, einschließlich derjenigen, die über Behinderungen und Beeinträchtigungen verfügen.
ms.assetid: df6947ec-6a1d-4645-ae3e-863839c32588
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 559d4c18e59c63a428aca1086e57f2ba4e62ae6f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104558567"
---
# <a name="accessibility-design-basics"></a>Barrierefreiheit (Entwurfs Grundlagen)

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Das Entwerfen von Software für Barrierefreiheit bedeutet, sicherzustellen, dass Programme und Funktionen für die größte Anzahl von Benutzern problemlos verfügbar sind, einschließlich derjenigen, die über Behinderungen und Beeinträchtigungen verfügen.

Die Anzahl der Benutzer, die Barrierefreiheits Funktionen unterstützen können, kann Sie überraschen. in den USA haben Umfragen beispielsweise ergeben, dass mehr als die Hälfte aller Computerbenutzer Probleme oder Beeinträchtigungen im Zusammenhang mit der Barrierefreiheit haben und wahrscheinlich von der Verwendung der zugänglichen Technologie profitieren. Darüber hinaus führt der Software Entwurf durch Flexibilität und inklusiv, die die Merkmale der Barrierefreiheit sind, häufig zu einer verbesserten Nutzbarkeit und Kundenzufriedenheit.

![Screenshot des Dialog Felds "Easy Access Center" ](images/inter-accessibility-image1.png)

Das in der Systemsteuerung verfügbare Easy of Access Center bietet einen zentralen Ort, an dem Benutzer die gewünschten Barrierefreiheits Features auswählen und anpassen können.

**Hinweis:** Richtlinien, die sich auf [Tastatur](inter-keyboard.md), [Maus](inter-mouse.md), [Farbe](vis-color.md)und [Sound](vis-sound.md) beziehen, werden in separaten Artikeln dargestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

Wenn Benutzer mit Computer Hardware und-Software interagieren, kommen viele physische, perzeptive und kognitive Faktoren ins Spiel. Bevor Sie überlegen, wie Sie die Funktionen Ihres Programms leichter zugänglich machen können, erfahren Sie, welche Arten von Behinderungen und Beeinträchtigungen vorhanden sind und welche Hilfstechnologien diese Benutzer bei der Interaktion mit Computern möglicherweise bearbeiten.

### <a name="types-of-impairments"></a>Arten von Beeinträchtigungen

In der folgenden Tabelle werden häufige Benutzer Behinderungen und-Beeinträchtigungen beschrieben, und es werden einige der wichtigsten Lösungen aufgelistet, die für die Barrierefreiheit von Computern verwendet werden.



|                               |                                                                                                                                                                                                         |                                                                                                                                                                                       |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Einschränkungen**<br/>     | **Beschreibung**<br/>                                                                                                                                                                              | **Lösungen**<br/>                                                                                                                                                              |
| Grafisches Element<br/>             | Reicht von einem milden (betroffen 17 Prozent der Benutzer) bis zu einem schwerwiegenden Wert (Dies wirkt sich auf 9 Prozent der Benutzer aus)<br/>                                                                                                   | Anpassbare Vergrößerung, Farben und Kontrast Braille-Hilfsprogramme; Sprachausgaben.<br/>                                                                                       |
| Hörvermögen<br/>            | Reicht von milden (von 18 Prozent der Benutzer betroffen) auf schwerwiegende Werte (die sich auf 2 Prozent der Benutzer auswirken).<br/>                                                                                                   | Informations Redundanz: Sound, der nur als Ergänzung zu Text oder visueller Kommunikation verwendet wird.<br/>                                                                                     |
| Beweglichkeit<br/>          | Reicht von milden (die sich auf 19 Prozent der Benutzer auswirken) auf "schwerwiegend" (betrifft 5 Prozent der Benutzer). Diese Beeinträchtigung umfasst oft Schwierigkeiten bei der Durchführung bestimmter Motor Fertigkeiten mit Tastatur oder Maus.<br/> | Redundanz der Eingabemethode: Programm Features, auf die über die Maus-oder Tastatur Entsprechungen<br/>                                                                                       |
| Kognitiv<br/>          | Beinhaltet Arbeitsspeicher Beeinträchtigungen und perzeptive Unterschiede. Wirkt sich auf 16 Prozent der Benutzer aus.<br/>                                                                                                         | Hochgradig anpassbare Benutzeroberfläche (UI); Verwendung von [progressiver Offenlegung](ctrl-progressive-disclosure-controls.md) zum Ausblenden der Komplexität Verwendung von Symbolen und anderen visuellen Hilfen.<br/> |
| Geisel<br/>            | Beinhaltet visuelle Empfindlichkeit für Bewegung und blinken.<br/>                                                                                                                                        | Konservativer Ansatz zum modulieren von Schnittstellen, z. b. die Verwendung von Animationen Vermeiden von Bildschirm Flimmern im Bereich zwischen 2 Hertz (Hz) und 55 Hz.<br/>                        |
| Sprache oder Sprache<br/> | Umfasst Probleme mit der Dyslexia-und der mündlichen Kommunikation.<br/>                                                                                                                                       | Rechtschreibprüfungs-und Grammatik Prüfungs Dienstprogramme; sprach Erkennungs-und Text-zu-Sprache-Technologie.<br/>                                                                                 |



 

Weitere Richtlinien zur Unterstützung von Benutzern bei diesen Beeinträchtigungen finden Sie weiter unten in diesem Artikel unter [behandeln bestimmter Beeinträchtigungen](#addressing-particular-impairments) .

### <a name="types-of-assistive-technologies-and-accessibility-features"></a>Typen von Hilfstechnologien und Barrierefreiheits Features

**Sprachausgabe**

Eine Sprachausgabe ermöglicht es Benutzern mit visuellen Behinderungen oder Behinderungen, durch die Umwandlung von visuellen Elementen in Audiodaten durch eine Benutzeroberfläche zu navigieren. Auf diese Weise werden Benutzeroberflächen Text, Steuerelemente, Menüs, Symbolleisten, Grafiken und andere Bildschirmelemente von der Sprachausgabe der Sprachausgabe gesprochen. Um ein Programm zu erstellen, das für die Unterstützung von Bildschirmlesern optimiert ist, müssen Sie planen, wie die Sprachausgabe die einzelnen Benutzeroberflächen Elemente identifizieren soll.

Jedes Benutzeroberflächen Element, mit dem der Benutzer interagieren kann, muss Tastatur zugänglich sein und über eine Barrierefreiheit-Anwendungsprogrammierschnittstelle (Application Programming Interface, API) verfügbar gemacht werden. Wir empfehlen die Verwendung von Benutzeroberflächen Automatisierung, das neue Barrierefreiheits Framework für alle Versionen von Microsoft Windows, die Windows Presentation Foundation (WPF) unterstützen. Die Benutzeroberflächen Automatisierung ermöglicht den programmgesteuerten Zugriff auf die meisten Elemente auf dem Desktop, sodass Hilfstechnologieprodukte, z. b. Bildschirm Sprachausgaben, Informationen zur Benutzeroberfläche für Benutzer bereitstellen und die Benutzeroberfläche auf andere Weise als Standard Eingaben ändern können (z. b. durch sprechen anstelle von oder zusätzlich zur Bearbeitung der Maus oder Tastatur). Weitere Informationen finden Sie unter [Übersicht über die Benutzeroberflächen Automatisierung](/dotnet/framework/ui-automation/ui-automation-overview).

Beachten Sie, dass die Bildschirm Sprachausgabe zwar eine sehr wichtige Hilfstechnologie ist, aber auch andere. Weitere Informationen zu den verfügbaren Technologien finden Sie unter [Typen von Hilfstechnologieprodukten](https://www.microsoft.com/enable/at/types.aspx).

**Spracherkennung**

Die Spracherkennung ist ein Barrierefreiheits Feature in Windows, das es Benutzern ermöglicht, per Spracheingabe mit ihren Computern zu interagieren, was die Notwendigkeit einer Motor Interaktion mit der Maus oder Tastatur reduziert. Benutzer können Dokumente und e-Mails vorschreiben, Sprachbefehle verwenden, um zwischen Programmen zu starten und zwischen diesen zu wechseln, das Betriebssystem zu steuern und sogar Formulare im Web auszufüllen.

**Bildschirmlupe**

Die Vergrößerung unterstützt Benutzer mit Sehfähigkeit durch die Vergrößerung von Elementen auf dem Bildschirm von 2 bis zum 16-fachen des Originals. Benutzer können diese Funktion festlegen, um die Maus zu verfolgen (um eine vergrößerte Version anzuzeigen, auf die die Maus zeigt), die Tastatur (um den Bereich anzuzeigen, in dem sich der Zeiger bei der Tabstopps bewegt) oder die Textbearbeitung (um zu sehen, was Sie typisieren).

**Visuelle Einstellungen und Farbschemas**

Benutzer mit visueller Beeinträchtigung können nicht nur die Dinge auf dem Bildschirm vergrößern, sondern auch von Systemeinstellungen wie dem [Modus für hohe Kontraste](glossary.md) oder der Möglichkeit zum Anpassen von Hintergrund-und Vordergrund Farbschemas profitieren.

**Narrator**

Die Sprachausgabe ist eine herunter skalierte Bildschirmausgabe in Windows, mit der Benutzer auf dem Bildschirm Text und UI-Elemente lesen können, auch wenn einige Ereignisse (einschließlich Fehlermeldungen), die spontan auftreten, angezeigt werden. Der Benutzer kann die Sprachausgabe Menüs hören, ohne das aktive Fenster zu belassen.

![Screenshot des Dialog Felds "Microsoft-Sprachausgabe" ](images/inter-accessibility-image2.png)

Benutzer können den Umfang anpassen, in dem die Microsoft-Sprachausgabe verwendet wird.

**Bildschirmtastatur**

Für Benutzer, die Probleme mit physischen Tastaturen haben und ein alternatives Eingabegerät wie z. b. einen Switch verwenden müssen, sind Bildschirmtastatur erforderlich. Benutzer können Schlüssel mit der Maus oder einem anderen Zeigegerät, einer kleinen Gruppe von Schlüsseln oder nur einem Schlüssel auswählen, je nachdem, wie Sie die Bildschirmtastatur einrichten.

**Tastaturmaus**

Wenn Maustasten aktiviert sind, können Benutzer, die die Tastatur bevorzugen, mithilfe der Pfeiltasten auf der numerischen Tastatur den Mauszeiger bewegen.

Eine umfassende Liste der Barrierefreiheits Funktionen finden Sie unter [Barrierefreiheit in Windows Vista](https://www.microsoft.com/enable/products/windowsvista/default.aspx) auf der Microsoft-Website.

### <a name="keyboard-based-navigation"></a>Tastatur basierte Navigation

Die Tab-Taste, Pfeiltasten, Leertaste und EINGABETASTE sind wichtig für die Tastatur basierte Navigation. Beim Drücken der Tab-Taste wird der [Eingabefokus](glossary.md) durch die verschiedenen Steuerelement Gruppen und durch Drücken der Pfeiltasten innerhalb eines Steuer Elements oder zwischen Steuerelementen innerhalb einer Gruppe verschoben. Das Drücken der Leertaste ist das gleiche wie das Klicken auf das Steuerelement mit dem Eingabefokus, während das Drücken der EINGABETASTE mit dem Klicken auf die Standard Befehls Schaltfläche oder den Befehls Link identisch ist.

![Screenshot des Dialog Felds "Leerer Papierkorb" ](images/inter-accessibility-image3.png)

In diesem Beispiel können Benutzer die Tab-Taste drücken, bis die gewünschte Option den Eingabefokus besitzt, und dann die EINGABETASTE drücken, um das Objekt zu öffnen.

### <a name="access-keys"></a>Zugriffsschlüssel

Mit Zugriffs Schlüsseln können Benutzeroptionen auswählen und Befehle direkt initiieren, ohne zuerst zum Steuerelement navigieren zu müssen. Zugriffsschlüssel werden durch das unterstreichen eines der Zeichen in der Bezeichnung des Steuer Elements angegeben. Benutzer aktivieren dann die Option oder den Befehl, indem Sie die Alt-Taste und das unterstrichene Zeichen drücken. Bei Zugriffs Schlüsseln wird die Groß-/Kleinschreibung

![Screenshot des Menüs "Datei" und "Zugriffsschlüssel" ](images/inter-accessibility-image4.png)

Wenn Sie in diesem Beispiel ALT + O drücken, wird der Befehl "Öffnen" aktiviert.

Die Auswahl logischer Zugriffsschlüssel für Steuerelemente stellt in der Regel keine Schwierigkeit dar. Je mehr Steuerelemente in einem Fenster vorhanden sind, desto größer ist jedoch die Möglichkeit, die Zugriffsschlüssel Optionen zu überschreiten. Weisen Sie in diesem Fall der Steuerungsgruppe anstelle der einzelnen einzelnen Zugriffstasten zu.

![Screenshot von Steuerelement Gruppen und Zugriffs Schlüsseln ](images/inter-accessibility-image5.png)

In diesem Beispiel werden Zugriffsschlüssel Steuerungsgruppen anstelle einzelner Steuerelemente zugewiesen.

Zugriffsschlüssel werden oft mit Tastenkombinationen verwechselt, aber Tastenkombinationen werden von Zugriffs Schlüsseln anders zugewiesen und weisen unterschiedliche Ziele auf. Beispielsweise verwenden Tastenkombinationen STRG und Funktions schlüsselsequenzen und dienen in erster Linie als Verknüpfung für fortgeschrittene Benutzer anstelle von für die Barrierefreiheit.

Weitere Informationen finden Sie unter [Tastatur](inter-keyboard.md).

### <a name="designing-for-accessibility-three-fundamental-practices"></a>Entwerfen für Barrierefreiheit: drei grundlegende Vorgehensweisen

Barrierefreie Programme helfen allen Benutzern auf irgendeine Weise, da sich die Ziele von Barrierefreiheit und Nutzbarkeit überlappen. Beispielsweise sind Features, die für fortgeschrittene Benutzer so effizient wie möglich entwickelt wurden, auch für Benutzer vorteilhaft, die die Tastatur aufgrund der Beweglichkeit-Beeinträchtigung verwenden möchten.

Drei grundlegende Vorgehensweisen helfen Ihnen beim barrierefreien Entwurf: ermöglichen Sie eine gewisse Flexibilität in der Benutzeroberfläche, nehmen Sie in Bezug auf die Benutzer Anforderungen und-Einstellungen eine wichtige Rolle bei Entwurfsentscheidungen, und ermöglichen Sie den programmgesteuerten Zugriff auf Ihre Benutzeroberfläche.

**Bereitstellen flexibler Benutzeroberflächen**

Barrierefreiheits Entwurf ist zumindest teilweise die Möglichkeit, Benutzern Auswahlmöglichkeiten zu bieten. Keine frustrierenden, nicht sehr vielfältigen Auswahlmöglichkeiten, sondern eine begrenzte Anzahl von Optionen, die die Benutzer Anforderungen Intelligent erwartet. "Möchten Sie die Navigation nicht mit der Maus durchlaufen? Hier können Sie mit der Tastatur genau die gleichen Aktionen ausführen. Sie möchten keine physischen Tastaturen? Hier ist ein virtuelles, das Sie auf dem Bildschirm verwenden können. "

Stellen Sie z. b. Flexibilität wie folgt bereit:

-   Bereitstellen von auswählbaren Entsprechungen für nicht-Text-Elemente (z. b. alt-Text für Grafiken und Beschriftungen für Audiodaten).

    ![Screenshot der Anmelde Schaltfläche](images/inter-accessibility-image6.png)

    ![Screenshot von alt-Text für Anmelde Schaltfläche](images/inter-accessibility-image7.png)

    Benutzer, die sich für das Rendering von Grafiken entschieden haben, sollten stattdessen ALT-Text sehen und beschreiben, wie das Steuerelement funktioniert und wie Sie damit interagieren.

-   Bereitstellen von Alternativen für Farbe (z. b. Symbol Differenzierung oder Verwendung von Sounds).

    ![Screenshot der Symbole in Graustufen (Graustufen) ](images/inter-accessibility-image8.png)

    In diesem Beispiel können die Standardsymbole basierend auf ihren Entwürfen leicht unterschieden werden.

-   Sicherstellen des Tastatur Zugriffs (z. b. ein Tabstopp für jedes interaktive Steuerelement), sodass Benutzer die gleichen Elemente in Ihrem Programm mit der Maus oder der Tastatur erreichen können.
-   Stellen Sie sicher, dass Ihr Programm gute Farbkontrast Optionen für Benutzer bietet. Windows stellt eine Option für hohe Kontraste dar, ist aber eigentlich als Lösung für eine strenge visuelle Beeinträchtigung konzipiert. Andere Kontrast Optionen bieten den Benutzern am besten eine milde Beeinträchtigung, z. b. eine geringe Sehfähigkeit und Farbenblindheit.
-   Sicherstellen, dass Benutzer die Größe des Texts in der Benutzeroberfläche des Programms anpassen können (z. b. über ein Schieberegler-Steuerelement oder ein Dropdown Feld für die Schriftgröße). Wenn möglich, unterstützen Sie den Modus für hohe Punkte pro Zoll (dpi).
-   Stellen Sie sicher, dass das Programm Multimodal ist, d. h., wenn der primäre Modus des Programms für einige nicht zugänglich ist, haben diese Benutzer eine Möglichkeit, das Problem zu umgehen. Wenn Animation z. b. angezeigt wird, sollten die Informationen in mindestens einem nicht animierten Präsentationsmodus mit der Option des Benutzers angezeigt werden.

Multimodale Schnittstellen und flexible Navigation bieten dem Benutzer im Grunde die Architektur der Informations Redundanz. Redundanz verfügt manchmal über negative-und-Einschränkungen. Beispielsweise wird in Benutzeroberflächen Text empfohlen, Redundanz zu entfernen, um das Leseverhalten zu optimieren. Im Kontext der Barrierefreiheit werden Redundanz jedoch positive, ausfallsichere Mechanismen und Erfahrungen mit sich bringen.

**Berücksichtigen Ihrer Benutzer**

Im Allgemeinen ist das Leitprinzip wichtig, um barrierefreie Programme zu entwerfen. Selbst als intellektueller Übung sollten Sie sich vorstellen, wie Sie Ihr Programm als Benutzer, der deaktiviert ist, kennenlernen müssen. Nehmen Sie sich die Zeit, die UI-Bildschirme im Modus mit hohem Kontrast und bei verschiedenen Auflösungen zu testen, um sicherzustellen, dass die Benutzeroberfläche für Benutzer mit Sehbehinderung eine gute Lösung ist Testen Sie den Tastatur Zugriff, indem Sie das Kontrollkästchen **Tastenkombinationen und Zugriffstasten unterstreichen** im System Steuerungselement Easy of Access Center aktivieren (damit Zugriffstasten immer sichtbar sind). Sie können sogar über strikte Tests hinausgehen, indem Sie Entwicklern und Designern, die eine natürliche Eignung aufweisen, mit anderen Personen beginnen, damit zu beginnen.

Sie sollten auch die folgenden Schritte veranschaulichen:

-   Verwenden von systemweiten Einstellungen (z. b. System Farbe) anstelle von hardverdrahtungs Einstellungen für das jeweilige Programm. Beachten Sie nicht nur die Parameter, die Benutzer speziell für die Interaktion mit ihren Programmen ausgewählt haben, sondern auch Barrierefreiheits Funktionen, die in das Betriebssystem integriert sind, das der Benutzer unabhängig von dem Programm, das Sie verwenden, in Kraft setzen möchten. Weitere Informationen finden Sie unter Informationen [zu Windows-Barrierefreiheits Funktionen](/previous-versions//ms695605(v=vs.85)).
-   Bevorzugen allgemeiner Steuerelemente für benutzerdefinierte Steuerelemente, da gängige Steuerelemente bereits die Windows-Barrierefreiheits-APIs implementiert haben.
-   Dokumentieren aller Optionen und Features für die Barrierefreiheit (z. b. alle Tastenkombinationen). Benutzer mit Beeinträchtigungen sind stark motiviert, Barrierefreiheits Features zu entdecken, und erwarten häufig, dass umfassende Informationen in der Hilfe gesammelt werden.
-   Erstellen einer zugänglichen Dokumentation in zugänglichen Formaten. Folglich sollte die Dokumentation selbst dieselben Zugriffsregeln wie die primäre Benutzeroberfläche einhalten, einschließlich der Möglichkeit, die Schriftart Größe zu vergrößern, die Verwendung von alt-Text für Grafiken und redundante Informationsarchitektur (z. b. die Verwendung von Farbcodierung als Ergänzung zu Text).

In Softwareprodukten kann sich der Benutzer in Bezug auf Nutzbarkeit und Marktforschung, in effizienten Supportdiensten und Dokumentationen und natürlich in Entwurfsentscheidungen nicht mit der Unterstützung der Benutzer in Zusammenhang bringen. Wenn Sie sich z. b. in Bezug auf das Design für fortgeschrittene Benutzer Gedanken machen: haben Sie diese neue Funktion in, da Sie Sie möchten, oder weil Sie wissen, dass Ihre fortgeschrittenen Benutzer Sie gefragt haben? Der letztere Fall gibt an, dass der Entwurf für die Entscheidungsfindung durch den Wert von "Achtung" gut informiert ist.

**Bereitstellen von programmgesteuerten**

Das Bereitstellen des programmgesteuerten Zugriffs auf die Benutzeroberfläche ist unverzichtbar, damit Hilfstechnologien (z. b. Bildschirm Sprachausgaben, Alternative Eingabegeräte und sprach Erkennungs Programme) den Bildschirm für die Benutzer richtig interpretieren. Indem Sie einen "Map" der einzelnen UI-Bildschirme im Programm erstellen, stellen Sie ihn für Benutzer von Hilfstechnologien zur Verfügung.

Gehen Sie dazu wie folgt vor:

-   Aktivieren des programmgesteuerten Zugriffs auf alle Elemente der Benutzeroberfläche und auf Text (z. b. über die Active Accessibility com-Schnittstelle, [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)).
-   Platzieren von Namen (oder Titeln) und Beschreibungen auf Benutzeroberflächen Objekte, Frames und Seiten (z. b. mit der Eigenschaft " [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Name").
-   Sicherstellen, dass programmgesteuerte Ereignisse von allen Benutzeroberflächen Aktivitäten ausgelöst werden (z. b. bei Fokus Ereignissen für alle UI-Aktivitäten, die die Fokus Bewegung betreffen

**Wenn Sie nur vier Dinge tun...**

1.  Stellen Sie sicher, dass jeder Benutzer das volle Potenzial des Programms nutzen kann.
2.  Stellen Sie sich den Barrierefreiheit als Gelegenheit für eine kreative Problembehebung vor, und eine weitere Möglichkeit, die Gesamt Benutzer Zufriedenheit zu erhöhen.
3.  Beachten Sie die Systemeinstellungen.
4.  Verwenden Sie nach Möglichkeit allgemeine Steuerelemente.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Stören oder deaktivieren Sie die aktivierten Funktionen des Betriebssystems oder anderer Produkte, die als Barrierefreiheits Features identifiziert werden.** Sie können diese Features identifizieren, indem Sie sich auf die Dokumentation des betreffenden Betriebssystems oder des betreffenden Produkts beziehen.
-   **Erzwingen Sie nicht die Interaktion von Benutzern mit Ihrem Programm als oberstes Fenster auf dem Bildschirm.** Wenn eine Funktion oder ein Fenster fortlaufend erforderlich ist, damit Benutzer eine Aufgabe ausführen können, sollte das Fenster immer sichtbar bleiben, wenn der Benutzer dies unabhängig von seiner Position relativ zu anderen Fenstern auswählt. Wenn der Benutzer z. b. eine verschiebbare Bildschirmtastatur hat, die sich auf allen anderen Fenstern befindet, sodass er jederzeit sichtbar ist, sollte das Programm es nie durch die obligatorische Platzierung am Anfang der [Z-Reihenfolge](glossary.md)verschleiern.
-   **Verwenden Sie nach Möglichkeit Systemfarben, Schriftarten und allgemeine Steuerelemente.** Auf diese Weise reduzieren Sie die Anzahl der eintretene Barrierefreiheits Probleme erheblich.

### <a name="addressing-particular-impairments"></a>Adressieren bestimmter Beeinträchtigungen

**Störungen**

-   **Verlassen Sie sich nie allein auf Farbe, um Bedeutungen zu vermitteln.** Verwenden Sie Farbe nur als Mittel zur Verstärkung der Bedeutung von Text, Design, Location oder Sound.

    ![Screenshot des roten Communicator-Symbols und der QuickInfo ](images/inter-accessibility-image9.png)

    Die primäre Kommunikationsmethode in diesem Beispiel ist der präzise QuickInfo-Text. Die Verwendung von Color unterstützt bei der Kommunikation der Bedeutung, aber ist sekundär.

-   **Verwenden Sie alternative Text Info Tipps (alt), um Grafiken zu beschreiben.**
-   **Verwenden Sie Text nicht in Grafiken.** Benutzer mit Sehbehinderung können Grafiken deaktiviert haben (z. b. in einem Webbrowser), oder Sie können Text, der in Grafiken platziert wurde, einfach nicht sehen oder suchen.
-   **Stellen Sie sicher, dass Dialogfelder und Fenster aussagekräftige Namen aufweisen,** damit ein Benutzer, der hört, anstatt den Bildschirm anzuzeigen (z. b. mithilfe eines Bildschirm Readers), entsprechende Kontextinformationen erhält.
-   **Beachten Sie die Benutzereinstellungen für die visuelle Darstellung** , indem Sie immer Schriftart-, Größen-und Farben, Windows-Anzeigeelement Größen und Systemkonfigurations Einstellungen aus den APIs Theme und GetSystemMetrics abrufen.
-   Halten Sie den Sprechblasen **Text kurz** , damit er leichter lesbar ist und die Unterbrechung der Bildschirm Sprachausgaben minimiert.

    ![Screenshot der Sprechblase, die PIN-Code Limits anzeigt ](images/inter-accessibility-image10.png)

    Obwohl die Ballons ggf. zusätzlichen Textkörper Text verwenden können, wird in diesem Beispiel gezeigt, dass der Titel Text in einigen Fällen das gleiche Ziel in einer wirtschaftlicheren und barrierefreien Weise erreicht.

**Hörvermögen**

-   **Verlassen Sie sich nie auf Sound, um Bedeutung zu vermitteln.** Verwenden Sie Sound nur als Mittel zur Verstärkung der Bedeutung von Text, Design, Location oder Color.
-   **Ermöglicht es Benutzern, die Menge der Audioausgabe zu steuern.** Verwenden Sie zu diesem Zweck den Windows-volumemixer. Weitere Informationen finden Sie unter [Sound](vis-sound.md).
-   **Richten Sie den Sound Ihres Programms so ein, dass er in einem Bereich zwischen 500 Hz und 3000 Hz auftritt** oder vom Benutzer problemlos in diesem Bereich angepasst werden soll. Sounds in diesem Bereich sind höchstwahrscheinlich für Personen mit einer Hörbehinderung erkennbar.

**Beweglichkeit**

-   **Nehmen Sie die Timeout Werte für die Benutzeroberfläche in Relation zu getdoubleclicktime (), statt Absolute Zeiten zu verwenden.** Dadurch werden die Timeouts an die Geschwindigkeit des Benutzers angepasst.
-   **Weisen Sie allen Menü Elementen Zugriffstasten zu** , damit Benutzer, die lieber mit der Tastatur arbeiten, die gleiche Fähigkeit haben, in Ihrem Programm als Benutzer zu navigieren, die mit der Maus arbeiten.
-   **Doppelklicken und ziehen Sie nicht die einzige Möglichkeit, um eine Aktion auszuführen.** Dies kann für einige Benutzer schwierig sein.
-   **Entfernen Sie Menüleisten nicht aus dem Programm.** Menüleisten sind einfacher als Symbolleisten, auf die Tastatur Benutzer zugreifen können. Wenn Sie nicht möchten, dass die Menüleiste standardmäßig sichtbar ist, blenden Sie Sie stattdessen aus.
-   **Erleichtern Sie die Hilfe von der Tastatur, indem Sie Tabstopps für Hilfe Schaltflächen und Links bereitstellen.**
-   **Um das Bewusstsein der Zugriffsschlüssel Zuweisungen in Ihrem Programm zu verbessern, können Sie Sie jederzeit anzeigen.** Wechseln Sie in der Systemsteuerung zu Easy of Access Center, und klicken Sie auf **Tastatur leichter zu verwenden**. Aktivieren Sie dann das Kontrollkästchen **Tastenkombinationen und Zugriffstasten unterstreichen** .

**Kognitiv**

-   **Verwenden Sie Progressive Offenlegung** , um die Komplexität auszublenden.

    ![Screenshot der unterteilten Schaltflächen mit nach unten ](images/inter-accessibility-image11.png)

    In diesen Beispielen sind Optionen, die über die Befehls Schaltfläche verfügbar sind, standardmäßig ausgeblendet, und Benutzer können die Optionen anzeigen, indem Sie die Steuerelemente für die Progressive Offenlegung nutzen.

-   **Verwenden Sie Symbole, Symbolleisten und andere visuelle Hilfsmittel** , um das Lesen von Text zu verbrauchen.
-   Stellen Sie nach Möglichkeit eine **automatische Vervollständigung in Textfeldern und in bearbeitbaren Dropdown Listen bereit**, sodass Benutzer nicht den vollständigen Namen der Befehle, Dateinamen oder ähnlichen Optionen aus einem begrenzten Satz von Optionen eingeben müssen. Dadurch wird die kognitive Auslastung für alle Benutzer reduziert, und die Benutzereingaben für Benutzer, für die Rechtschreibung oder Typisierung schwierig, langsam oder mühsam ist, werden reduziert.
-   **Veranschaulichen Sie schwierige Konzepte in der Hilfe, indem Sie Tutorials und Animationen einschließen.** Beachten Sie, dass Animationen für Benutzer mit Beeinträchtigungen der Beeinträchtigung schwierig sein können und daher nur bei Bedarf verwendet werden sollten.

**Geisel**

-   **Verwenden Sie nicht blinkende oder blinkende Text, Objekte oder andere Elemente mit einer Flash-oder Blink Häufigkeit im Bereich zwischen 2-55 Hz.**
-   **Beschränken Sie die Verwendung von Animationen.** Einige Benutzer sind besonders empfindlich für die Bildschirm Bewegung, insbesondere in der Peripherie ihres visuellen Felds. Wenn Sie die Animation verwenden, um etwas zu beachten, stellen Sie sicher, dass die Aufmerksamkeit verdient wird und das Unterbrechen des Benutzers ist.

**Sprache oder Sprache**

-   **Organisieren und schreiben Sie klaren, präzisen und leicht verständlichen Text.** Nutzbarkeits Tests zeigen, dass das Verständnis von Informationen zum durch finden von Schlüsselinformationen am Ende eines Ausdrucks verbessert wird. Weitere Richtlinien finden Sie unter [Style und Tone](text-style-tone.md).

**Falsch:**

Sind drei der nächsten Ziffern?

Klicken Sie zum Starten auf OK.

**Richtig:**

Ist die nächste Ziffer 3?

Klicken Sie zunächst auf OK.

### <a name="access-keys"></a>Zugriffsschlüssel

-   **Zeichen mit breiter Breite** (z. b. w, m und Großbuchstaben) bevorzugen.
-   **Bevorzugen Sie einen unverwechselbaren Konsonanten oder einen vowel,** z. b. "x" in "Exit".
-   **Vermeiden Sie die Verwendung von Zeichen, die die Unterstreichung schwer zu erkennen machen,** wie z. b. (vom problematischsten bis zum geringsten problematischen)
    -   Zeichen, die nur ein Pixel breit sind, z. b. i und l.
    -   Zeichen mit untergeordneten Zeichen, wie z. b. g, j, p, q und y.
    -   Zeichen neben einem Buchstaben mit einem descender.

### <a name="menu-access-keys"></a>Menü Zugriffstasten

-   **Weisen Sie allen Menü Elementen Zugriffstasten zu.** Keine Ausnahmen.
-   **Für dynamische Menü Elemente (z. b. zuletzt verwendete Dateien) weisen Sie Zugriffsschlüssel numerisch zu.**

    ![Screenshot des Menüs "Öffnen" mit zuletzt verwendeten Dateien ](images/inter-accessibility-image12.png)

    In diesem Beispiel weist das Paint-Programm in Windows den kürzlich verwendeten Dateien numerische Zugriffstasten zu.

-   **Zuweisen von eindeutigen Zugriffs Schlüsseln innerhalb einer Menü Ebene.** Sie können Zugriffsschlüssel über verschiedene Menüebenen hinweg wieder verwenden.
-   **Machen Sie Zugriffsschlüssel leicht zu finden:**
    -   Wählen Sie für die am häufigsten verwendeten Menü Elemente die Zeichen am Anfang des ersten oder zweiten Worts der Bezeichnung aus, vorzugsweise das erste Zeichen.
    -   Wählen Sie für weniger häufig verwendete Menü Elemente Buchstaben aus, die eine unterschiedliche konsonante oder einen Vokal in der Bezeichnung darstellen.

### <a name="dialog-box-access-keys"></a>Zugriffsschlüssel für das Dialog Feld

-   **Weisen Sie allen interaktiven Steuerelementen oder deren Bezeichnungen nach Möglichkeit eindeutige Zugriffstasten zu.** Schreibgeschützte [Textfelder](ctrl-text-boxes.md) sind interaktive Steuerelemente (da Benutzer einen Bildlauf durchführen und Text kopieren können), sodass Sie von Zugriffs Schlüsseln profitieren. **Weisen Sie keinen Zugriffsschlüssel zu:**
    -   **Schaltflächen OK, Abbrechen und schließen.** Enter und ESC werden für Ihre Zugriffsschlüssel verwendet. Weisen Sie jedoch immer einen Zugriffsschlüssel einem Steuerelement zu, das "OK" oder "Abbrechen" bedeutet, aber eine andere Bezeichnung hat.

        ![Screenshot der Steuerelemente mit zugewiesenen Zugriffs Schlüsseln ](images/inter-accessibility-image13.png)

        In diesem Beispiel ist der Schaltfläche positiver Commit eine Zugriffstaste zugewiesen.

-   **Gruppen Bezeichnungen.** Normalerweise werden den einzelnen Steuerelementen innerhalb einer Gruppe Zugriffsschlüssel zugewiesen, sodass die Gruppen Bezeichnung keines benötigt. Weisen Sie der Gruppen Bezeichnung jedoch einen Zugriffsschlüssel zu, nicht die einzelnen Steuerelemente, wenn ein Mangel an Zugriffs Schlüsseln vorliegt.
-   **Allgemeine Hilfe** Schaltflächen, auf die mit F1 zugegriffen wird.
-   **Link Bezeichnungen.** Es gibt oft zu viele Verknüpfungen, um eindeutige Zugriffsschlüssel zuzuweisen, und Link-Unterstriche blenden die Zugriffsschlüssel Unterstriche aus. Lassen Sie die Benutzer stattdessen auf Verknüpfungen mit der Tab-Taste zugreifen.
-   **Registerkarten Namen.** Registerkarten werden mithilfe von STRG + TAB und STRG + UMSCHALT + TAB mithilfe von STRG + UMSCHALTTASTE gedrückt.
-   **Durchsuchen von Schaltflächen mit der Bezeichnung "...".** Diese können nicht eindeutig Zugriffs Schlüsseln zugewiesen werden.
-   **Nicht beschriftete Steuerelemente,** wie z. b. Dreh Steuerelemente, grafische Befehls Schaltflächen und unbezeichnete Steuerelemente für progressives
-   **Statischer Text oder Bezeichnungen ohne Bezeichnung für Steuerelemente, die nicht interaktiv sind,** z. b. Status leisten.
-   **Weisen Sie zuerst Zugriffsschlüssel für die Zugriffstaste zu, um sicherzustellen, dass Sie über die Standardschlüssel Zuweisungen verfügen** Wenn keine Standardschlüssel Zuweisung vorhanden ist, verwenden Sie den ersten Buchstaben des ersten Worts. Beispielsweise sollten die Schaltflächen Zugriffsschlüssel für Ja und kein Commit immer "Y" und "N" sein, unabhängig von den anderen Steuerelementen im Dialogfeld.
-   **Für negative Commit-Schaltflächen (außer Abbrechen), die als "nicht" formuliert sind, weisen Sie den Zugriffsschlüssel "n" in "nicht" zu.** Wenn Sie nicht als "nicht" formuliert ist, verwenden Sie die standardmäßige Zugriffsschlüssel Zuweisung, oder weisen Sie den ersten Buchstaben des ersten Worts zu. Dadurch haben alle "TS" und "No" eine konsistente Zugriffstaste.
-   Damit **Zugriffsschlüssel leicht zu finden sind, weisen Sie die Tastenkombinationen einem Zeichen zu, das früh in der Bezeichnung angezeigt wird,** idealerweise das erste Zeichen, auch wenn es ein Schlüsselwort gibt, das später in der Bezeichnung angezeigt wird.

Weitere Richtlinien und Beispiele finden Sie unter [Tastatur](inter-keyboard.md).

## <a name="text"></a>Text

-   **Verwenden Sie Doppelpunkte am Ende externer Steuerelement Bezeichnungen.** Einige Hilfstechnologien suchen nach Doppelpunkten, um Steuerelement Bezeichnungen zu identifizieren.
-   **Positionieren Sie Bezeichnungen einheitlich in Bezug auf die Elemente, die Sie bezeichnen.** Dies hilft der Hilfstechnologie, die Bezeichnungen ordnungsgemäß den entsprechenden Steuerelementen zuzuordnen, und unterstützt Benutzer von Bildschirm Vergrößerungen, wo Sie nach einer Bezeichnung oder einem Steuerelement suchen müssen.

    ![Screenshot der konsistent platzierten Bezeichnungen ](images/inter-accessibility-image14.png)

    In diesem Beispiel werden die Bezeichnungen für jede der Dropdown Listen konsistent platziert, und es werden Doppelpunkte verwendet.

-   **Beschränken Sie den alt-Text auf maximal 150 Zeichen.** Beschreiben Sie die Aktion zum Aktivieren des Steuer Elements (z. b. klicken, klicken Sie mit der rechten Maustaste auf usw.), und beschreiben Sie dann die Funktion des Steuer Elements.

    **Annehmbar:**

    Gedrückt.

    Blaue Hügel.

    **Besserer**

    Klicken Sie hier, um sich bei Ihrem Konto anzumelden.

    Foto von fernen Hügeln, das zeigt, wie Farben über die Distanz ausgeblendet werden.

-   **Verwenden Sie keinen Text zum Zeichnen von Linien, Feldern oder anderen grafischen Symbolen.** Zeichen, die auf diese Weise verwendet werden, können Benutzer von Sprachausgaben verwirren. Beispielsweise wird ein Feld, das mit dem Buchstaben "x" um einen Textbereich gezeichnet wird, von der Bildschirmlesesoftware als "x x x x x x" in der ersten Zeile, gefolgt von "x" und Inhalt und "x" gelesen.

## <a name="documentation"></a>Dokumentation

-   Dokumentieren Sie alle Optionen und Features für die Barrierefreiheit (z. b. alle Tastenkombinationen).
-   Erstellen Sie eine barrierefreie Dokumentation in zugänglichen Formaten. Daher sollte die Dokumentation selbst dieselben Regeln für Barrierefreiheit wie die primäre Benutzeroberfläche einhalten.
-   Beziehen Sie sich auf Zugriffsschlüssel, nicht auf Tastenkombinationen (die eine andere Bedeutung und Verwendung aufweisen), mnetmonische Schlüssel oder Accelerators.
-   Im Allgemeinen beziehen Sie sich auf eine Person mit einer Art von Behinderung, nicht mit deaktivierter Person. Denken Sie zuerst an die Person, nicht an die Bezeichnung.



|                                                               |                                                                                  |
|---------------------------------------------------------------|----------------------------------------------------------------------------------|
| **Diese Begriffe verwenden**<br/>                                | **Statt**<br/>                                                        |
| Hat eingeschränkte Dexterität, hat Bewegungsbehinderungen<br/>     | Lähmt, lahm<br/>                                                        |
| Ohne Behinderungen<br/>                               | Normal, fähig, fehlerfrei<br/>                                          |
| Eingebene, Personen, die mit einer Hand eingeben<br/>          | Einhändig <br/>                                                        |
| Personen mit Behinderungen<br/>                           | Die deaktivierten, deaktivierten Personen, Menschen mit Behinderungen, den Behinderten<br/> |
| Kognitive Behinderungen, entwicklungsbehinderungen<br/> |                                                                                  |



 

