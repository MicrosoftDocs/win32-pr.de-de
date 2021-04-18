---
title: UX Checkliste für Desktop Anwendungen
description: Im folgenden finden Sie eine Sammlung einiger wichtiger Richtlinien in der UX-Anleitung. Sie können dies als Checkliste verwenden, um sicherzustellen, dass die Benutzeroberfläche des Programms diese wichtigen Elemente Recht erhält.
ms.assetid: 4705a807-5949-4957-8ea6-70871beaf8e0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d1006b7ad9de30941b6ceb4cc7282ec578450840
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/25/2021
ms.locfileid: "106358162"
---
# <a name="ux-checklist-for-desktop-applications"></a>UX Checkliste für Desktop Anwendungen

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Im folgenden finden Sie eine Sammlung einiger wichtiger Richtlinien in der UX-Anleitung. Sie können dies als Checkliste verwenden, um sicherzustellen, dass die Benutzeroberfläche des Programms diese wichtigen Elemente Recht erhält.

## <a name="windows"></a>Windows

-   **Unterstützen Sie die minimale effektive Windows-Auflösung von 800 x 600 Pixel.** Für wichtige Benutzeroberflächen (UIs), die im abgesicherten Modus funktionieren müssen, unterstützen Sie eine [effektive Auflösung](glossary.md) von 640 x 480 Pixeln. Achten Sie darauf, den von der Taskleiste verwendeten Speicherplatz zu berücksichtigen, indem Sie 48 vertikale [relative Pixel](glossary.md) für Windows reservieren, der mit der Taskleiste angezeigt wird.
-   **Optimieren Sie die Größe der Größe der Fensterlayouts für eine effektive Auflösung von 1024 x 768 Pixeln.** Ändern Sie automatisch die Größe dieser Fenster für niedrigere Bildschirmauflösungen auf eine Weise, die noch funktionsfähig ist.
-   **Achten Sie darauf, dass Sie Ihre Fenster in 96 Punkten pro Zoll (dpi) (mit 800 x 600 Pixel), 120 dpi (bei 1024 x 768 Pixel) und 144 dpi-Modi (bei 1200 x 900 Pixeln) testen.** Überprüfen Sie Layoutprobleme, z. b. das Abschneiden von Steuerelementen, Text und Fenstern und das Strecken von Symbolen und Bitmaps.
-   **Für Programme mit Berührungs-und mobilen Verwendungs Szenarien optimieren Sie für 120 dpi.** High-dpi-Bildschirme sind aktuell auf touchpcs und mobilen PCs weit verbreitet.
-   **Wenn es sich bei einem Fenster um ein eigenes Fenster handelt, zeigen Sie es anfänglich oben im Besitzer Fenster an.** Nie unterhalb. In der nachfolgenden Anzeige sollten Sie die Anzeige an der letzten Position (relativ zum Besitzer Fenster) anzeigen, wenn dies wahrscheinlich bequemer ist.
-   **Wenn ein Fenster kontextbezogen ist, sollten Sie es immer in der Nähe des Objekts anzeigen, von dem es gestartet wurde.** Platzieren Sie Sie jedoch (vorzugsweise nach unten und nach rechts), damit das Objekt nicht durch das Fenster abgedeckt wird.

## <a name="layout"></a>Layout

-   **Größen Steuerelemente und Bereiche in einem Fenster entsprechend Ihrem typischen Inhalt.** Vermeiden Sie den abgeschnittene Text und die zugehörigen Ellipsen. Benutzer sollten nie mit einem Fenster interagieren, um den typischen Inhalt anzuzeigen – die Größe der Größe und den Bildlauf für ungewöhnlich große Inhalte reservieren. Prüfen Sie insbesondere Folgendes:
    -   **Steuerelement Größen.** Größe von Steuerelementen an ihren typischen Inhalt anpassen, sodass Steuerelemente bei Bedarf breiter, größer oder mehrzeilige werden. Größen Steuerelemente, um den Bildlauf in Fenstern zu eliminieren, die über ausreichend verfügbaren Speicherplatz verfügen. Außerdem sollten in Fenstern, die über ausreichend verfügbaren Speicherplatz verfügen, nie abgeschnittene Bezeichnungen oder abgeschnittene Text vorhanden sein. Um das Lesen von Text zu vereinfachen, sollten Sie jedoch die Zeilen breiten auf 65 Zeichen beschränken.
    -   **Spaltenbreite.** Stellen Sie sicher, dass die Listen Ansichts Spalten die geeignete Standard-, minimal-und Höchstgröße aufweisen. Wählen Sie Listenansichten Standard Spaltenbreite aus, die nicht zum abgeschnittene Text führen, insbesondere, wenn in der Listenansicht Platz verfügbar ist.
    -   **Layoutsaldo.** Das Layout eines Fensters sollte ungefähr ausgeglichen sein. Wenn das Layout nach links verschoben wird, sollten Sie erwägen, Steuerelemente breiter zu gestalten und einige Steuerelemente nach rechts zu verschieben.
    -   **Layoutgröße ändern.** Wenn ein Fenster in der Größe geändert werden kann und Daten abgeschnitten werden, stellen Sie sicher, dass größere Fenstergrößen mehr Daten anzeigen. Wenn Daten abgeschnitten werden, erwarten Benutzer, dass die Größe von Fenstern geändert wird, um weitere Informationen anzuzeigen.
-   **Legen Sie eine minimale Fenstergröße fest, wenn eine Größe vorhanden ist, unter der der Inhalt nicht mehr verwendbar ist.** Legen Sie für Steuerelemente, die in der Größe geändert werden können, die Element Größen mit minimaler Größe auf die kleinsten funktionsgrößen fest, z. b. die minimale funktionale Spaltenbreite

## <a name="text"></a>Text

-   **Verwenden Sie die üblichen, Konversations Begriffe, wenn dies möglich ist.** Konzentrieren Sie sich auf die Benutzer Ziele, nicht auf die Technologie. Dies ist insbesondere dann effektiv, wenn Sie ein komplexes technisches Konzept oder eine komplexe Maßnahme erläutern. Stellen Sie sich vor, dass Sie sich die Schulter des Benutzers ansehen und erläutern, wie Sie die Aufgabe erledigen können.
-   **Seien Sie höflich, unterstützend und ermutigend.** Der Benutzer sollte sich niemals an einen oder anderen Benutzer fühlen.
-   **Entfernen Sie den redundanten Text.** Suchen Sie nach redundantem Text in Fenstertiteln, Haupt Anweisungen, ergänzenden Anweisungen, Inhalts Bereichen, Befehls Verknüpfungen und Commit-Schaltflächen. Im Allgemeinen sollten Sie voll Text in den Haupt Anweisungen und interaktiven Steuerelementen belassen und Redundanz von den anderen Orten entfernen.
-   **Verwenden Sie die Titel Format-groß Schreibung für Titel und die Groß-/Kleinschreibung im Satz Format für alle anderen Benutzeroberflächen Elemente.** Dies ist für den Windows-Ton besser geeignet.
    -   **Ausnahme:** Bei älteren Anwendungen können Sie bei Bedarf die Groß-/Kleinschreibung von Titeln für Befehls Schaltflächen, Menüs und Spaltenüberschriften verwenden.
-   **Bei Funktions-und Technologie Namen ist die Groß-und Kleinschreibung konservativ.** In der Regel sollten nur Hauptkomponenten groß geschrieben werden (mithilfe der Groß-/Kleinschreibung im Titel).
-   **Bei Funktions-und Technologie Namen muss die Groß-und Kleinschreibung einheitlich sein.** Wenn der Name mehr als einmal auf einem Bildschirm der Benutzeroberfläche angezeigt wird, sollte er immer auf dieselbe Weise angezeigt werden. Ebenso sollte der Name auf allen UI-Bildschirmen im Programm einheitlich dargestellt werden.
-   Stellen Sie **die Namen generischer Benutzeroberflächen Elemente,** z. b. Symbolleiste, Menü, Scrollleiste, Schaltfläche und Symbol, nicht groß.
    -   **Ausnahmen:** Adressleiste, Verknüpfungs Leiste, Menüband.
-   **Verwenden Sie nicht alle Großbuchstaben für Tastenkombinationen.** Befolgen Sie stattdessen die Groß-/Kleinschreibung, die von Standard Tastaturen verwendet wird, oder Kleinbuchstaben, wenn der Schlüssel nicht auf der Tastatur gekennzeichnet ist.
-   **Ellipsen bedeutet Vollständigkeit.** Verwenden Sie Ellipsen im Benutzeroberflächen Text wie folgt:
    -   **Respekt.** Geben Sie an, dass ein Befehl zusätzliche Informationen benötigt. Verwenden Sie immer dann keine Ellipsen, wenn eine Aktion ein anderes Fenster anzeigt – nur, wenn zusätzliche Informationen erforderlich sind. Befehle, deren implizites Verb ein anderes Fenster anzeigt, nehmen keine Auslassungs Punkte, wie z. b. erweitert, Hilfe, Optionen, Eigenschaften oder Einstellungen.
    -   **Vorrats.** Geben Sie an, dass der Text abgeschnitten wird.
    -   **Kennzeichen.** Geben Sie an, dass eine Aufgabe ausgeführt wird (z. b. "suchen...").

**Tipp:** Abgeschnittener Text in einem Fenster oder auf einer Seite mit nicht verwendetem Speicherplatz zeigt ein schlechtes Layout oder eine zu geringe Standardfenster Größe an. Bemühen Sie sich um Layouts und Standardfenster Größen, die den Umfang des abgeschnittene Texts eliminieren oder verringern. Weitere Informationen finden Sie unter [Layout](vis-layout.md).

-   **Verwenden Sie nicht den blauen Text, der kein Link ist, da Benutzer möglicherweise davon ausgehen, dass es sich um einen Link handelt.** Verwenden Sie Fett oder einen grauen Farbton, in dem Sie andernfalls farbigen Text verwenden würden.
-   **Verwenden Sie fett formatiert, um Aufmerksamkeit auf den Text zu zeichnen, den Benutzer lesen müssen.**
-   **Verwenden Sie die main-Anweisung, um näher zu erklären, welche Benutzer in einem bestimmten Fenster oder einer bestimmten Seite vorgehen sollten.** Gute Haupt Anweisungen vermitteln das Ziel des Benutzers, anstatt sich auf die Bearbeitung der Benutzeroberfläche zu konzentrieren.
-   **Stellen Sie die main-Anweisung in Form einer imperativen Richtung oder einer bestimmten Frage dar.**
-   **Legen Sie keine Punkte am Ende von Steuerelement Bezeichnungen oder Haupt Anweisungen ab.**
-   **Verwenden Sie ein Leerzeichen zwischen Sätzen.** Nicht zwei.

## <a name="controls"></a>Steuerelemente

-   **Allgemein**
    -   **Bezeichnen Sie jedes Steuerelement oder jede Gruppe von Steuerelementen. Ausnahmen**
        -   Text Felder und Dropdown Listen können mithilfe von Eingabe Aufforderungen beschriftet werden.
        -   Untergeordnete Steuerelemente verwenden die Bezeichnung Ihres zugeordneten Steuer Elements. Dreh Steuerelemente sind immer untergeordnete Steuerelemente.
    -   **Wählen Sie für alle Steuerelemente den sichersten aus (um den Verlust von Daten oder den System Zugriff zu verhindern), den sichersten Wert standardmäßig.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie den wahrscheinlichsten oder einfachsten Wert aus.
    -   **Eingeschränkte Steuerelemente bevorzugen.** Verwenden Sie möglichst eingeschränkte Steuerelemente wie Listen und Schieberegler anstelle von nicht eingeschränkten Steuerelementen wie Textfeldern, um den Bedarf an Texteingaben zu verringern.
    -   **Deaktivierte Steuerelemente überdenken** Deaktivierte Steuerelemente können schwer zu verwenden sein, da Benutzer buchstäblich ableiten müssen, warum Sie deaktiviert sind. Deaktivieren Sie ein-Steuerelement, wenn es von den Benutzern erwartet wird, und Sie können leicht ableiten, warum das Steuerelement deaktiviert ist. Entfernen Sie das Steuerelement, wenn Benutzer es nicht aktivieren können, oder wenn es nicht erwartet wird, oder lassen Sie es aktiviert, aber geben Sie eine Fehlermeldung an, wenn es nicht ordnungsgemäß verwendet wird.
        -   **Tipp:** Wenn Sie nicht sicher sind, ob Sie ein Steuerelement deaktivieren oder eine Fehlermeldung bereitstellen sollten, erstellen Sie zunächst die Fehlermeldung, die Sie möglicherweise bereitstellen. Wenn die Fehlermeldung hilfreiche Informationen enthält, die Ziel Benutzer wahrscheinlich nicht schnell ableiten, lassen Sie das Steuerelement aktiviert, und geben Sie den Fehler an. Andernfalls deaktivieren Sie das Steuerelement.
-   **Befehls Schaltflächen**
    -   **Bevorzugen spezifischer Bezeichnungen gegenüber generischen Bezeichnungen.** Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen. Benutzer sind viel wahrscheinlicher, dass Befehlszeilen Bezeichnungen als statischer Text gelesen werden.
        -   **Ausnahme:** Benennen Sie die Schaltfläche Abbrechen nicht um, wenn die Bedeutung von Cancel eindeutig ist. Benutzer sollten nicht alle Schaltflächen lesen müssen, um zu bestimmen, welche Schaltfläche eine Aktion abbricht. Umbenennen Sie jedoch abbrechen, wenn unklar ist, welche Aktion abgebrochen wird, z. b. Wenn mehrere ausstehende Aktionen vorhanden sind.
    -   **Wenn Sie eine Frage stellen, verwenden Sie Bezeichnungen, die der Frage entsprechen.** Geben Sie z. b. ja und keine Antworten auf eine yes-oder No-Frage ein.
    -   **Verwenden Sie keine Schaltflächen anwenden in Dialogfeldern, die keine Eigenschaften Blätter oder System Steuerungselemente sind.** Die Schaltfläche anwenden bedeutet, dass die ausstehenden Änderungen übernommen werden, das Fenster jedoch geöffnet lassen. Auf diese Weise können Benutzer die Änderungen auswerten, bevor Sie das Fenster schließen. Dies ist jedoch nur für Eigenschaften Blätter und System Steuerungselemente erforderlich.
    -   Kennzeichnen einer Schaltfläche Abbrechen, wenn der Abbruch die Umgebung in ihren vorherigen Zustand zurückgibt (ohne Nebeneffekt); Andernfalls können Sie die Schaltfläche Schließen (wenn der Vorgang abgeschlossen ist) oder beenden (wenn der Vorgang ausgeführt wird), um anzugeben, dass der aktuelle geänderte Zustand unverändert bleibt.
-   **Befehls Verknüpfungen**
    -   **Befehls Verknüpfungen sollten immer in einem Satz von zwei oder mehr vorhanden sein.** Logisch, es gibt keinen Grund, eine Frage zu stellen, die nur eine Antwort hat.
    -   **Geben Sie eine explizite Schaltfläche Abbrechen an.** Verwenden Sie für diesen Zweck keinen Befehls Link. Häufig erkennen Benutzer, dass Sie keine Aufgabe ausführen möchten. Wenn Sie einen Befehls Link zum Abbrechen verwenden, müssen Benutzer alle Befehls Verknüpfungen sorgfältig lesen, um zu bestimmen, welche Methode abgebrochen werden soll. Durch eine explizite Schaltfläche "Abbrechen" können Benutzer eine Aufgabe effizient abbrechen.
    -   **Wenn die Bereitstellung einer expliziten Schaltfläche Abbrechen einen einzelnen Befehls Link verlässt, geben Sie einen Befehls Link zum Abbrechen und eine Schaltfläche Abbrechen an.** Dadurch wird deutlich, dass Benutzer eine Auswahl treffen. Formulieren Sie diesen Befehls Link in Bezug darauf, wie er sich von der ersten Antwort unterscheidet, anstelle von "Abbrechen" oder einer Abweichung.
-   **Kontrollkästchen "diese Option nicht \<item\> mehr anzeigen"**
    -   **Verwenden Sie \<item\> ggf. die Option "nicht mehr anzeigen", damit Benutzer ein wiederkehrendes Dialogfeld unterdrücken können, wenn es keine bessere Alternative gibt.** Es ist immer besser, das Dialogfeld anzuzeigen, wenn Benutzer es wirklich benötigen, oder es einfach auszuschließen, wenn dies nicht der Fall ist.
    -   **Ersetzen Sie dies \<item\> durch das jeweilige Element.** Diese Erinnerung beispielsweise nicht mehr anzeigen. Wenn Sie auf ein Dialogfeld im Allgemeinen verweisen, verwenden Sie diese Meldung nicht mehr anzeigen.
    -   **Geben Sie eindeutig an, wenn Benutzereingaben für künftige Standardwerte verwendet** werden, indem Sie den folgenden Satz unter der Option hinzufügen: Ihre Auswahl wird in Zukunft standardmäßig verwendet.
    -   **Wählen Sie die Option nicht standardmäßig aus. Wenn das Dialogfeld wirklich nur einmal angezeigt werden soll, sollten Sie dies tun, ohne zu Fragen.** Verwenden Sie diese Option nicht als Entschuldigung, um Benutzer zu belästigen – stellen Sie sicher, dass das Standardverhalten nicht lästig ist.
    -   **Wenn Benutzer die Option auswählen und auf Abbrechen klicken, wird diese Option wirksam.** Diese Einstellung ist eine Meta-Option, sodass Sie nicht dem standardmäßigen Abbruch Verhalten entspricht, bei dem kein Nebeneffekt besteht. Beachten Sie, dass Benutzer, die das Dialogfeld in Zukunft nicht sehen möchten, wahrscheinlich auch abbrechen möchten.
-   **Links**
    -   **Weisen Sie keinen** [Zugriffsschlüssel](glossary.md)zu. Auf Links wird mithilfe der Tab-Taste zugegriffen.
    -   **Fügen Sie dem Linktext weder "Click" noch "Click here" hinzu.** Dies ist nicht erforderlich, da ein Link auf Klicken bedeutet.
-   **QuickInfos**
    -   **Verwenden Sie Quick Infos, um Bezeichnungen für nicht beschriftete Steuerelemente bereitzustellen.** Sie müssen keine Quick Infos für beschriftete Steuerelemente, sondern nur aus Gründen der Konsistenz erhalten.
    -   **Quick Infos können auch ausführlichere Informationen für Symbolleisten Schaltflächen enthalten, wenn dies hilfreich ist.** Wiederholen Sie nicht nur den Vorgang, oder geben Sie eine verfassen-Anweisung zurück, die bereits in der Bezeichnung ist.
    -   **Vermeiden Sie das abdecken des Objekts, mit dem der Benutzer die Anzeige oder Interaktion durchläuft.** Platzieren Sie den Tipp immer auf der Seite des Objekts, auch wenn dies eine Trennung zwischen dem Zeiger und dem Tipp erfordert. Einige Trennungen sind kein Problem, solange die Beziehung zwischen dem Objekt und dem Tip eindeutig ist.
        -   **Ausnahme:** Quick Infos für vollständige Namen, die in Listen und Strukturen verwendet werden.
    -   **Vermeiden Sie für Auflistungen von Elementen, dass das nächste Objekt abgedeckt wird, mit dem der Benutzer wahrscheinlich die Anzeige oder Interaktion durchläuft.** Vermeiden Sie für horizontal angeordnete Elemente das Platzieren von Tipps auf der rechten Seite. vermeiden Sie bei vertikal angeordneten Elementen das Platzieren von Tipps unten.
-   **Schrittweise Offenlegung**
    -   **Verwenden Sie mehr oder weniger Progressive Offenlegungs Schaltflächen, um erweiterte oder selten verwendete Optionen, Befehle und Details auszublenden, die Benutzer in der Regel nicht benötigen.** Blenden Sie häufig verwendete Elemente nicht aus, da Sie von Benutzern möglicherweise nicht gefunden werden. Stellen Sie jedoch sicher, dass alle ausgeblendeten Werte den Wert
    -   Wenn die Oberfläche immer einige Optionen, Befehle oder Details anzeigt, verwenden Sie die folgenden Bezeichnungs Paare:
        -   **Mehr oder weniger Optionen.** Verwenden Sie für Optionen oder eine Mischung aus Optionen, Befehlen und Details.
        -   **Mehr oder weniger Befehle.** Nur für Befehle verwenden.
        -   **Mehr/weniger Details.** Wird nur für Informationen verwendet.
        -   **Mehr oder weniger \<object name\> .** Verwenden Sie für andere Objekttypen, z. b. Ordner.
    -   Andernfalls:
        -   **Optionen zum ein-/ausblenden.** Verwenden Sie für Optionen oder eine Mischung aus Optionen, Befehlen und Details.
        -   **Befehle anzeigen/ausblenden.** Nur für Befehle verwenden.
        -   **Details anzeigen/ausblenden.** Wird nur für Informationen verwendet.
        -   **Ein-/ausblenden \<object name\> .** Verwenden Sie für andere Objekttypen, z. b. Ordner.
-   **Status anzeigen**
    -   **Verwenden Sie bestimmte-Status leisten für Vorgänge, die einen begrenzten Zeitraum erfordern,** auch wenn diese Zeitspanne nicht genau vorhergesagt werden kann. Unbestimmt Status leisten zeigen an, dass der Fortschritt ausgeführt wird, aber keine weiteren Informationen bereitgestellt werden. Wählen Sie nicht nur basierend auf dem möglichen Mangel an Genauigkeit eine unbestimmte Statusanzeige aus.
    -   **Geben Sie die geschätzte Zeit an, wenn Sie dies genau erreichen können.** Die verbleibenden geschätzten Zeit Werte sind nützlich, aber Schätzungen, die sich auf die Markierung oder den Sprung hin nicht wesentlich bewegen, sind nicht hilfreich. Möglicherweise müssen Sie einige Verarbeitungsschritte durchführen, bevor Sie genaue Schätzungen durchführen können. Wenn dies der Fall ist, werden während dieses anfänglichen Zeitraums keine möglicherweise ungenauen Schätzungen angezeigt.
    -   **Starten Sie den Fortschritt nicht.** Eine Statusanzeige verliert ihren Wert, wenn Sie neu gestartet wird (möglicherweise weil ein Schritt im Vorgang abgeschlossen ist), da Benutzer nicht wissen, wann der Vorgang abgeschlossen wird. Nehmen Sie stattdessen an, dass alle Schritte des Vorgangs einen Teil des Fortschritts aufweisen und die Statusanzeige einmal abgeschlossen werden soll.
    -   **Geben Sie nützliche Fortschritts Details an.** Geben Sie zusätzliche Statusinformationen an, aber nur, wenn die Benutzer etwas damit tun können. Stellen Sie sicher, dass der Text so lange angezeigt wird, dass er von Benutzern gelesen werden kann.
    -   **Kombinieren Sie keine Statusanzeige mit einem ausgelasteten Zeiger.** Verwenden Sie einen oder den anderen, aber nicht beide gleichzeitig.
-   **Eingabeaufforderungen**
    -   **Verwenden Sie eine Eingabeaufforderung, wenn der Bildschirmbereich eine solche Premium-Anweisung ist, die eine Bezeichnung oder Anweisung nicht erwünscht ist,** z. b. auf einer Symbolleiste.
    -   **Bei der Eingabeaufforderung wird in erster Linie der Zweck des Textfelds oder Kombinations Felds auf kompakte Weise identifiziert.** Es darf keine wichtigen Informationen sein, die der Benutzer bei der Verwendung des Steuer Elements sehen muss.
    -   **Der Eingabe Aufforderungs Text darf nicht mit echtem Text verwechselt werden.** Gehen Sie dazu wie folgt vor:
        -   Zeichnen Sie den Eingabe Aufforderungs Text in kursiv grau und den eigentlichen Eingabetext in Roman schwarz.
        -   Der Eingabe Aufforderungs Text sollte nicht bearbeitbar sein und sollte ausgeblendet werden, wenn Benutzer in das Textfeld oder die Tab-Taste klicken.
            -   **Ausnahme:** Wenn das Textfeld den Standardeingabe Fokus besitzt, wird die Eingabeaufforderung angezeigt, und Sie verschwindet, sobald der Benutzer mit der Eingabe beginnt.
    -   Verwenden Sie keine endinterpunktions Zeichen oder Ellipsen.
-   **Benachrichtigungen**
    -   **Verwenden Sie Benachrichtigungen für Ereignisse, die nicht mit der aktuellen Benutzeraktivität in Zusammenhang stehen, keine sofortige Benutzeraktion erfordern und Benutzer frei ignorieren können.**
    -   **Benachrichtigungen nicht missbrauchen:**
        -   **Verwenden Sie Benachrichtigungen nur, wenn dies erforderlich ist.** Wenn Sie eine Benachrichtigung anzeigen, unterbrechen Sie möglicherweise Benutzer, oder Sie können Sie sogar stören. Stellen Sie sicher, dass die Unterbrechung gerechtfertigt ist.
        -   **Verwenden Sie Benachrichtigungen für nicht kritische Ereignisse oder Situationen, in denen keine sofortige Benutzeraktion erforderlich ist.** Verwenden Sie bei kritischen Ereignissen oder Situationen, in denen eine sofortige Benutzeraktion erforderlich ist, ein alternatives Benutzeroberflächen Element (z. b. ein modales Dialogfeld).
        -   **Verwenden Sie keine Benachrichtigungen für featureankündigungen!**

## <a name="keyboard"></a>Tastatur

-   **Weisen Sie dem Steuerelement den anfänglichen Eingabefokus zu, bei** dem es sich meist um das erste interaktive Steuerelement handelt. Wenn das erste interaktive Steuerelement keine gute Wahl ist, sollten Sie das Layout des Fensters ändern.
-   **Das Zuweisen von Registerkarten wird allen interaktiven Steuerelementen, einschließlich Schreib geschützter Bearbeitungsfelder, angehalten. Ausnahmen**
    -   Gruppen von verknüpften Steuerelementen, die sich als ein einzelnes Steuerelement Verhalten, z. b. Options Felder. Diese Gruppen verfügen über einen einzelnen Tabstopp.
    -   Enthält ordnungsgemäß Gruppen, sodass die Pfeiltasten in der Gruppe vorwärts und rückwärts und in der Gruppe bleiben.
-   **Die Aktivier Reihenfolge sollte von links nach rechts und von oben nach unten fließen.** Im Allgemeinen sollte die Aktivier Reihenfolge der Lesefolge folgen. Sie sollten Ausnahmen für häufig verwendete Steuerelemente erstellen, indem Sie Sie zuvor in der Aktivier Reihenfolge platzieren. Die Registerkarte sollte alle Tabstopps in beide Richtungen durchlaufen, ohne zu beenden. Innerhalb einer Gruppe sollte die Aktivier Reihenfolge ohne Ausnahmen in sequenzieller Reihenfolge angegeben werden.
-   **Innerhalb einer Tabstopp Taste sollte die Reihenfolge der Pfeiltasten von links nach rechts, von oben nach unten und** ohne Ausnahmen abgeleitet werden. Die Pfeiltasten sollten alle Elemente in beiden Richtungen durchlaufen, ohne zu beenden.
-   **Stellen Sie die Commit-Schaltflächen in der folgenden Reihenfolge bereit:**
    -   OK/ \[ do \] /Yes
    -   \[Nicht \] /No
    -   Abbrechen
    -   Anwenden (falls vorhanden)

dabei \[ handelt es sich nicht \] \[ \] um spezielle Antworten auf die main-Anweisung.

-   **Verwechseln Sie Zugriffstasten nicht mit Tastenkombinationen.** Obwohl sowohl Zugriffsschlüssel als auch Tastenkombinationen Tastatur Zugriff auf die Benutzeroberfläche bieten, haben Sie unterschiedliche Zwecke und Richtlinien.
-   **Weisen Sie allen interaktiven Steuerelementen oder deren Bezeichnungen nach Möglichkeit eindeutige Zugriffstasten zu.** Schreibgeschützte [Textfelder](ctrl-text-boxes.md) sind interaktive Steuerelemente (da Benutzer einen Bildlauf durchführen und Text kopieren können), sodass Sie von Zugriffs Schlüsseln profitieren. **Weisen Sie keinen Zugriffsschlüssel zu:**
    -   Schaltflächen OK, Abbrechen und schließen. Enter und ESC werden für Ihre Zugriffsschlüssel verwendet. Weisen Sie jedoch immer einen Zugriffsschlüssel einem Steuerelement zu, das "OK" oder "Abbrechen" bedeutet, aber eine andere Bezeichnung hat.
-   **Weisen Sie den am häufigsten verwendeten Befehlen Tastenkombinationen zu.** Nicht häufig verwendete Programme und Funktionen benötigen keine Tastenkombinationen, da Benutzer stattdessen Zugriffstasten verwenden können.
-   **Stellen Sie keine Tastenkombination als einzige Möglichkeit zum Ausführen einer Aufgabe dar.** Benutzer sollten auch die Maus oder die Tastatur mit Tab, Pfeil und Zugriffstasten verwenden können.
-   **Weisen Sie bekannten Tastenkombinationen keine unterschiedlichen Bedeutungen zu.** Da Sie gespeichert werden, sind nicht konsistente Bedeutungen für bekannte Verknüpfungen frustrierend und fehleranfällig.
-   **Versuchen Sie nicht, systemweite Programm-Tastenkombinationen zuzuweisen.** Die Tastenkombinationen des Programms werden nur wirksam, wenn das Programm den Eingabefokus besitzt.

## <a name="mouse"></a>Maus

-   **Benutzer müssen niemals auf ein Objekt klicken, um festzustellen, ob es klickbar ist.** Benutzer müssen in der Lage sein, die klickbarkeit allein bei der visuellen Prüfung zu bestimmen.
    -   Die primäre Benutzeroberfläche (z. b. "Commit"-Schaltflächen) muss über ein statisches Click- Benutzer müssen nicht darauf zeigen, um die primäre Benutzeroberfläche zu ermitteln.
    -   Bei der sekundären Benutzeroberfläche (z. b. sekundäre Befehle oder progressives Offenlegung) können Ihre Klick Möglichkeiten angezeigt werden.
    -   Text Verknüpfungen sollten den Linktext statisch vorschlagen und dann mit dem Mauszeiger auf den Mauszeiger zeigen.
    -   Grafik links zeigen nur einen Hand Zeiger auf den Mauszeiger.
-   **Verwenden Sie den Zeiger "Hand" (oder "Link Select") nur für Text-und Grafik links.** Andernfalls müssten Benutzer auf Objekte klicken, um zu bestimmen, ob es sich um Verknüpfungen handelt.

## <a name="dialog-boxes"></a>Dialogfelder

-   **Für modale Dialogfelder ist eine Interaktion erforderlich. verwenden Sie diese daher für Elemente, auf die Benutzer Antworten müssen, bevor Sie Ihre Aufgabe fortsetzen.** Stellen Sie sicher, dass die Unterbrechung gerechtfertigt ist, z. b. bei kritischen oder seltenen, einmaligen Aufgaben, die abgeschlossen werden müssen. Andernfalls sollten Sie nicht modante Alternativen in Erwägung gezogen.
-   **Nicht modante Dialogfelder erfordern keine Interaktion. verwenden Sie diese daher, wenn Benutzer zwischen einem Dialogfeld und dem Besitzer Fenster wechseln müssen.** Sie eignen sich am besten für häufige, wiederkehrende oder laufende Aufgaben. Menü Bänder, Symbolleisten und Palettenfenster sind jedoch oft besser geeignet.

## <a name="property-sheets"></a>Eigenschaftenblätter

-   **Stellen Sie sicher, dass die Eigenschaften erforderlich sind.** Überladen Sie Ihre Eigenschafts Seiten nicht mit unnötigen Eigenschaften, um zu vermeiden, dass Sie harte Entwurfsentscheidungen treffen.
-   **Stellen Sie Eigenschaften in Bezug auf die Benutzer Ziele anstelle der Technologie dar.** Nur weil eine Eigenschaft eine bestimmte Technologie konfiguriert, bedeutet das nicht, dass Sie die Eigenschaft in Bezug auf diese Technologie darstellen müssen.
    -   Wenn Sie Einstellungen in Bezug auf die Technologie darstellen müssen (möglicherweise, weil Ihre Benutzer den Namen der Technologie erkennen), sollten Sie eine kurze Beschreibung des Benutzer Vorteils angeben.
-   **Verwenden Sie bestimmte, aussagekräftige Registerkarten Bezeichnungen.** Vermeiden Sie generische Registerkarten Bezeichnungen, die auf eine beliebige Registerkarte (z. b. Allgemein, erweitert oder Einstellungen) angewendet werden können.
-   **Vermeiden Sie allgemeine Seiten.** Sie benötigen keine Seite "Allgemein". Nur eine allgemeine Seite verwenden, wenn:
    -   Die Eigenschaften gelten für mehrere Aufgaben und sind für die meisten Benutzer von Bedeutung. Legen Sie auf der Seite Allgemein keine spezialisierten oder erweiterten Eigenschaften auf, aber Sie können auf der Seite Allgemein über eine Befehls Schaltfläche auf Sie zugreifen.
    -   Die Eigenschaften passen nicht zu einer spezifischeren Kategorie. Wenn dies der Fall ist, verwenden Sie stattdessen den Namen für die Seite.
-   **Vermeiden Sie erweiterte Seiten.** Erweiterte Seite nur verwenden, wenn:
    -   Die Eigenschaften gelten für ungewöhnliche Aufgaben und sind hauptsächlich für fortgeschrittene Benutzer von Bedeutung.
    -   Die Eigenschaften passen nicht zu einer spezifischeren Kategorie. Wenn dies der Fall ist, verwenden Sie stattdessen den Namen für die Seite.
-   **Verwenden Sie keine Registerkarten, wenn ein Eigenschaften Fenster nur eine einzige Registerkarte hat und nicht erweiterbar ist.** Verwenden Sie stattdessen ein reguläres Dialogfeld mit OK, Abbrechen und einer optionalen Schaltfläche anwenden. Erweiterbare Eigenschaften Fenster (die von Drittanbietern erweitert werden können) müssen jedoch Registerkarten verwenden.

## <a name="wizards"></a>Assistenten

-   **Sie sollten zuerst einfache Alternativen in Erwägung gezogen werden, z. b. Dialogfelder, Aufgabenbereiche oder einzelne Seiten.** Bei den Assistenten handelt es sich um eine hohe Benutzeroberfläche, die am besten für selten ausgeführte mehrstufige Aufgaben verwendet wird. Sie müssen keine Assistenten verwenden – Sie können hilfreiche Informationen und Unterstützung in jeder beliebigen Benutzeroberfläche bereitstellen.
-   **Verwenden Sie Next nur, wenn Sie ohne Verpflichtung zur nächsten Seite übergehen.** Der Fortschritt der nächsten Seite wird als Verpflichtung betrachtet, wenn der Effekt nicht rückgängig gemacht werden kann, indem Sie auf zurück oder Abbrechen klicken.
-   **Verwenden Sie zurück, um Fehler zu beheben.** Abgesehen von der Behebung von Fehlern dürfen Benutzer nicht auf "zurück" klicken, um den Fortschritt in einer Aufgabe fortzusetzen.
-   **Wenn Benutzer ein Commit für eine Aufgabe ausführen, verwenden Sie eine Commit-Schaltfläche, die eine bestimmte Antwort auf die Haupt Anweisung ist (z. b. Print, Connect oder Start).** Verwenden Sie keine generischen Bezeichnungen wie Next (was keine Verpflichtung impliziert) oder Fertigstellen (was nicht spezifisch ist) zum Ausführen eines Commits für eine Aufgabe. Die Bezeichnungen auf diesen Commit-Schaltflächen sollten selbst sinnvoll sein. Startet immer Commit-Schaltflächen Bezeichnungen mit einem Verb. **Ausnahmen:**
    -   Verwenden Sie Fertigstellen, wenn die spezifischen Antworten weiterhin generisch sind, z. b. speichern, auswählen, auswählen oder Get.
    -   Verwenden Sie "Fertigstellen", um eine bestimmte Einstellung oder eine Sammlung von Einstellungen zu ändern.
-   **Verwenden Sie Befehls Verknüpfungen nur für Auswahlmöglichkeiten, keine Verpflichtungen.** Bestimmte Commit-Schaltflächen weisen auf eine wesentlich bessere Verpflichtung als Befehls Verknüpfungen in einem Assistenten hin.
-   **Wenn Sie Befehls Verknüpfungen verwenden, blenden Sie die Schaltfläche weiter aus, aber lassen Sie die Schaltfläche Abbrechen.**
-   **Verwenden Sie Close für Follow-Up-und Abschluss Seiten.** Verwenden Sie "Abbrechen" nicht, da das Schließen des Fensters Änderungen oder Aktionen, die zu diesem Zeitpunkt ausgeführt wurden, nicht verwerfen Verwenden Sie done nicht, da es kein Imperatives Verb ist.
-   **Verwenden Sie "Wizard" nicht in den Namen des Assistenten.** Verwenden Sie beispielsweise "Verbindung mit einem Netzwerk herstellen" anstelle von "Assistent für die Netzwerk Einrichtung". Es ist jedoch akzeptabel, als Assistenten auf Assistenten zu verweisen. Beispiel: "Wenn Sie ein Netzwerk zum ersten Mal einrichten, können Sie mithilfe des Assistenten zum Herstellen einer Verbindung mit einem Netzwerk Hilfe erhalten."
-   **Beibehalten der Benutzer Auswahl durch Navigation.** Wenn der Benutzer z. b. Änderungen vornimmt und auf Zurück klickt, dann sollten diese Änderungen beibehalten werden. Benutzer erwarten nicht, dass die Änderungen erneut eingegeben werden müssen, es sei denn, Sie haben explizit entschieden, Sie zu löschen.

## <a name="wizard-pages"></a>Seiten des Assistenten

-   **Konzentrieren Sie sich auf die effiziente Entscheidungsfindung.** Reduzieren Sie die Anzahl der Seiten, um sich auf Essentials zu konzentrieren. Konsolidieren Sie verwandte Seiten, und verwenden Sie optionale Seiten aus dem Hauptflow. Wenn Benutzer die vollständige Durchführung des Assistenten auf Weiter klicken, erscheint Ihnen möglicherweise zunächst ein guter Eindruck, aber wenn Benutzer die Standardeinstellungen nicht ändern müssen, sind die Seiten wahrscheinlich unnötig.
-   **Verwenden Sie keine Willkommens Seiten – erstellen Sie die erste Seite immer, wenn dies möglich ist.** Verwenden Sie nur dann eine optionale Seite mit den ersten Schritten, wenn:
    -   Der Assistent verfügt über erforderliche Komponenten, die erforderlich sind, um den Assistenten erfolgreich abzuschließen.
    -   Benutzer können den Zweck des Assistenten aufgrund der ersten Auswahl Seite nicht verstehen, und es gibt keinen Platz für weitere Erläuterungen.
    -   Die Haupt Anweisung für die Seite "erste Schritte" lautet "Vorbereitung:".
-   **Auf Seiten, bei denen Benutzer aufgefordert werden, Entscheidungen zu treffen, optimieren Sie in den wahrscheinlichsten Fällen.** Diese Arten von Seiten sollten tatsächliche Optionen, nicht nur Anweisungen, darstellen.
    -   Wenn Sie keine Seite "erste Schritte" verwenden, erläutern Sie den Zweck des Assistenten am Anfang der ersten Seite der Auswahl.
-   **Verwenden Sie Commit Pages, um den Benutzer zu bestätigen, wenn Benutzer einen Commit für die Aufgabe ausführen.** In der Regel ist die commitseite die letzte Seite der Auswahl, und die Schaltfläche Weiter wird neu klassifiziert, um die Aufgabe anzugeben, für die ein Commit ausgeführt wird.
    -   Verwenden Sie keine Zusammenfassungs Seiten, die nur die vorherige Auswahl des Benutzers zusammenfassen, es sei denn, die Aufgabe ist riskant (bei der Sicherheit oder beim Verlust der Zeit oder des Geldes), oder es besteht eine gute Wahrscheinlichkeit, dass die Benutzer Ihre Auswahl nicht verstehen und diese überprüfen müssen.
-   **Verwenden Sie keine Herzlichen Glückwunsch Seiten, die nichts tun, sondern den Assistenten beenden.** Wenn den Benutzern die Ergebnisse offensichtlich offensichtlich sind, schließen Sie einfach den Assistenten auf der Schaltfläche letztes Commit.
    -   Verwenden Sie Follow-Up Seiten, wenn Verwandte Aufgaben vorhanden sind, die Benutzer wahrscheinlich als Nachverfolgung durchführen. Vermeiden Sie vertraute nach Verfolgungs Aufgaben, wie z. b. "Senden einer e-Mail-Nachricht".
    -   Verwenden Sie Vervollständigungs Seiten nur dann, wenn die Ergebnisse nicht angezeigt werden und keine bessere Möglichkeit zum Bereitstellen von Feedback für den Abschluss der Aufgabe vorliegt.
    -   Assistenten, die Statusseiten haben, müssen eine Vervollständigungs Seite oder Follow-Up Seite verwenden, um den Abschluss der Aufgabe anzuzeigen. Schließen Sie für Aufgaben mit langer Ausführungszeit den Assistenten auf der Seite Commit, und verwenden Sie Benachrichtigungen, um Feedback zu geben.

## <a name="error-messages"></a>Fehlermeldungen

-   **Geben Sie keine Fehlermeldungen an, wenn Benutzer wahrscheinlich keine Aktion ausführen oder Ihr Verhalten** als Ergebnis der Nachricht ändern. Wenn keine Aktion ausgeführt werden kann, die Benutzer ausführen können, oder wenn das Problem nicht signifikant ist, unterdrücken Sie die Fehlermeldung.
-   **Wenn möglich, sollten Sie eine Lösung vorschlagen, damit Benutzer das Problem beheben können.** Stellen Sie jedoch sicher, dass die vorgeschlagene Lösung das Problem wahrscheinlich löst. Verschwenden Sie die Zeit der Benutzer nicht, indem Sie mögliche, aber unwahrscheinliche Lösungen vorschlagen.
-   **Sie sollten spezifisch sein.** Vermeiden Sie eine vage Formulierung, wie z. b. Syntax Fehler und ungültigen Vorgang. Geben Sie bestimmte Namen, Speicherorte und Werte der betroffenen Objekte an.
-   **Verwenden Sie keinen Ausdruck, der den Benutzer BLT oder einen Benutzerfehler impliziert.** Vermeiden Sie die Verwendung von und ihrer in der Formulierung. Obwohl die aktive Stimme in der Regel bevorzugt ist, verwenden Sie die passive Stimme, wenn der Benutzer der Betreff ist, und könnten sich für den Fehler verantwortlich machen, wenn die aktive Stimme verwendet wurde.
-   **Verwenden Sie für Fehlermeldungen nicht "OK".** Benutzer sehen keine Fehler als OK an. Wenn die Fehlermeldung keine direkte Aktion aufweist, verwenden Sie stattdessen close.
-   **Verwenden Sie nicht die folgenden Wörter:**
    -   Fehler, Fehler (verwenden Sie stattdessen Problem)
    -   Fehler bei (Verwendung nicht möglich).
    -   Ungültig, ungültig, ungültig (verwenden Sie stattdessen falsch oder nicht gültig)
    -   Abbrechen, beenden, beenden (verwenden Sie stattdessen "beenden")
    -   Katastrophal, schwerwiegend (verwenden Sie stattdessen Ernst)

Diese Begriffe sind unnötig und im Gegensatz zum ermutigenden Ton von Windows. Stattdessen wird [bei ordnungsgemäßer Verwendung](vis-std-icons.md)eines Fehler Symbols ausreichend kommuniziert, dass ein Problem vorliegt.

-   **Sie sollten keine Fehlermeldungen mit Soundeffekten begleiten.** Dabei handelt es sich um jarringverfahren und unnötig.

## <a name="warning-messages"></a>Warnmeldungen

-   **Warnungen beschreiben eine Bedingung, die in der Zukunft ein Problem verursachen kann.** Warnungen sind keine Fehler oder Fragen. formulieren Sie daher keine Routine Fragen als Warnungen.
-   **Geben Sie keine Warnmeldungen an, wenn Benutzer wahrscheinlich keine Aktion ausführen oder Ihr Verhalten als Ergebnis der Nachricht ändern.** Wenn keine Aktion ausgeführt werden kann, die Benutzer verwenden können, oder wenn die Bedingung nicht signifikant ist, unterdrücken Sie die Warnmeldung.

## <a name="confirmations"></a>Bestätigungen

-   **Verwenden Sie keine unnötigen Bestätigungen.** Nur Bestätigungen verwenden, wenn:
    -   Es gibt einen eindeutigen Grund, den Vorgang nicht fortzusetzen, und eine angemessene Wahrscheinlichkeit, dass Benutzer manchmal nicht.
    -   Die Aktion hat bedeutende Konsequenzen oder kann nicht einfach rückgängig gemacht werden.
    -   Die Aktion hat Konsequenzen, die Benutzer möglicherweise nicht kennen.
    -   Wenn Sie mit der Aktion fortfahren, müssen Benutzer eine Auswahl treffen, die nicht über einen geeigneten Standard verfügt.
    -   Aufgrund des aktuellen Kontexts haben Benutzer wahrscheinlich eine Fehler Aktion ausgeführt.
-   **Ausdrucks Bestätigungen als Ja oder keine Frage und stellen yes oder No Answers bereit.** Im Gegensatz zu anderen Dialogfeldern sind Bestätigungen so konzipiert, dass Benutzer keine schnellen Entscheidungen treffen können. Wenn Benutzer nicht in Ihre Antwort versetzt werden, hat eine Bestätigung keinen Wert.

## <a name="icons"></a>Symbole

-   **Alle Symbole sollten den** [Richtlinien des Aero-Style-Symbols](vis-icons.md)entsprechen. Ersetzen Sie alle Symbole im Windows XP-Stil.
-   **Wählen Sie Standardsymbole basierend auf dem Nachrichtentyp und nicht mit dem Schweregrad des zugrunde liegenden Problems aus:**
    -   **Zeit.** Ein Fehler oder ein Problem, der aufgetreten ist.
    -   **Davor.** Eine Bedingung, die in der Zukunft ein Problem verursachen kann.
    -   **Informationen.** Nützliche Informationen.

Wenn ein Problem verschiedene Nachrichten Typen kombiniert, konzentrieren Sie sich auf den wichtigsten Aspekt, auf den Benutzer reagieren müssen.

-   **Symbole müssen immer mit der Main-Anweisung oder einem anderen entsprechenden Text übereinstimmen.**
-   **Fehler Symbole sind für nicht kritische Probleme bei der Benutzereingabe nicht erforderlich.** Symbole werden jedoch für direkte Fehler benötigt, da dieses kontextbezogene Feedback zu leicht zu übersehen wäre.
-   **Verwenden Sie keine Warn Symbole, um nicht schwerwiegende Fehler zu "weichen".** Fehler sind keine Warnungen. wenden Sie stattdessen die Fehler Symbol Richtlinien an.
-   **Verwenden Sie für Frage Dialogfelder Warnungs Symbole nur für Fragen mit erheblichen Konsequenzen.** Verwenden Sie keine Warn Symbole für Routine Fragen.

## <a name="help"></a>Hilfe

-   **Link zu bestimmten, relevanten Hilfe Themen.** Keine Verknüpfung mit der Startseite der Hilfe, dem Inhaltsverzeichnis, einer Liste von Suchergebnissen oder einer Seite, die nur mit anderen Seiten verknüpft ist. Vermeiden Sie das Verknüpfen mit Seiten, die als eine große Liste häufig gestellter Fragen strukturiert sind, da Benutzer gezwungen werden, nach der Datei zu suchen, die dem Link entspricht, auf den Sie geklickt haben Verknüpfen Sie nicht mit bestimmten Hilfe Themen, die für die vorliegende Aufgabe nicht relevant und hilfreich sind. Niemals mit leeren Seiten verknüpfen.
-   **Fügen Sie keine Hilfe Verknüpfungen für jedes Fenster oder jede Seite ein, um die Konsistenz zu gewährleisten.** Wenn Sie einen Hilfelink an einem Ort bereitstellen, bedeutet das nicht, dass Sie Sie überall bereitstellen müssen.
-   **Wenn möglich, wird Text in Bezug auf die primäre Frage, die vom Hilfe Inhalt beantwortet wird, von der Ausdrucks Hilfe verknüpft.** Verwenden Sie nicht die Ausdrücke "Weitere Informationen zu" oder "Hilfe zu diesem Ausdruck erhalten".
-   **Verwenden Sie den gesamten Hilfelink für den Linktext,** nicht nur für die Schlüsselwörter.
-   **Verwenden Sie vollständige Sätze.**
-   **Verwenden Sie keine endpunktierungen oder Ellipsen, mit Ausnahme von Fragezeichen.**
-   **Wenn der Hilfe Inhalt online ist, legen Sie diesen im Linktext fest.** Dadurch wird das Ergebnis der Verknüpfungen vorhersagbar.

