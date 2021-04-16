---
title: Setup
description: Benutzer haben keine Erfahrung mit der Installation von Software, sodass moderne Einrichtungs Umgebungen einfach, effizient und Problem frei sein müssen.
ms.assetid: ed0265a6-4c39-4a1f-9493-e316a6519df7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 4e5de6f15dd797dd1d1362d1b515122b78c770f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104551317"
---
# <a name="setup"></a>Setup

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Benutzer haben keine Erfahrung mit der Installation von Software, sodass moderne Einrichtungs Umgebungen einfach, effizient und Problem frei sein müssen.

Setup bezieht sich in der Regel auf die Installation und das anfängliche Konfigurieren eines Programms. Setup kann jedoch auch auf den gesamten Installations Lebenszyklus verweisen, einschließlich Erstinstallation, inkrementelle Programmaktualisierungen (z. b. Versions Upgrades oder Service Packs), reparieren und Deinstallieren von.

Die meisten Benutzer berücksichtigen das Setup als notwendiges Übel, das so schnell wie möglich ausgeführt werden soll. Der Zeitpunkt der Installation des Programms ist es, es zu verwenden, nicht um unzählige Entscheidungen zur Konfiguration und Verwendung zu treffen, oder noch schlimmer, um viel Zeit damit zu verbringen, persönliche Fragen zu beantworten, die für die Registrierung oder für Marketingzwecke verwendet werden.

![Screenshot, der ein Setup Dialogfeld mit vier Optionen anzeigt.](images/exper-setup-image1.png)

Eine optimierte Einrichtung.

Die Einrichtung der Einrichtung in Kombination mit der ersten Verwendung des Programms wird als erste Möglichkeit bezeichnet. Ihr Programm sollte für Benutzer eine optimierte erste Benutzerfunktion bereitstellen. Jede Frage oder jeder Schritt, die nicht erforderlich ist oder verschoben werden kann, verzögert Sie bei der Verwendung des Programms. Übermäßig komplexe Setup Programme sind Relikte aus einem anderen Alter.

**Hinweis:** Richtlinien, die sich auf die [erste](exper-first-exper.md) Verwendung eines Programms und [Assistenten](win-wizards.md) beziehen, werden in separaten Artikeln vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Obwohl alle Microsoft Windows-Programme eine bestimmte Art von Setup Programm benötigen, können Sie auswählen, wo die Programmeinstellungen abgelegt werden sollen:

-   Setup
-   Erste Verwendung des Programms
-   Zentralisierte Programmoptionen
-   Im Kontext der Verwendung des Features

**Einrichtung**

Einstellungen in Setup anzeigen, wenn Folgendes vorliegt:

-   Die richtigen Einstellungen sind erforderlich, um das Programm zu verwenden, und gelten für alle Benutzer.
-   Die Verwendung von Standardeinstellungen ist nicht zulässig, weil es keine sichere Standardeinstellung gibt, die Benutzer wahrscheinlich Einstellungen auswählen, die nicht die Standardeinstellung sind, oder die Standardeinstellungen erfordern eine Zustimmung des Benutzers.
-   Benutzer sollten nach dem Setup keine wichtigen Einstellungen ändern.

**Erste Verwendung des Programms**

Stellen Sie die Einstellungen für die erste Verwendung des Programms in folgenden Situationen dar:

-   Die richtigen Einstellungen sind erforderlich, um das Programm zu verwenden, und Sie gelten für einzelne Benutzer.
-   Die Verwendung von Standardeinstellungen ist nicht zulässig, weil es keine sichere Standardeinstellung gibt, die Benutzer wahrscheinlich Einstellungen auswählen, die nicht die Standardeinstellung sind, oder die Standardeinstellungen erfordern eine Zustimmung des Benutzers.
-   Benutzer sollten jedoch keine wichtigen Einstellungen mithilfe der Programmoptionen ändern.
-   Mit den Einstellungen wird eine Kern Umgebung oder eine Lösung angepasst, die für die persönliche Identifikation eines Benutzers mit dem Programm entscheidend ist.

Bei solchen Einstellungen treffen Benutzer wahrscheinlich bessere Entscheidungen innerhalb des Programm Kontexts als innerhalb des Setups.

**Zentralisierte Programmoptionen**

Stellen Sie die Einstellungen im [Dialogfeld Optionen](win-property-win.md) des Programms dar, wenn alle der folgenden Bedingungen zutreffen:

-   Es gibt Standardeinstellungen, die für die meisten Benutzer gut funktionieren.
-   Es gibt viele Einstellungen, die Sie über Features und Aufgaben hinweg anwenden können.
-   Benutzer erwarten die Einstellungen eher an einem zentralen Ort.

**Im Kontext der Verwendung des Features**

Stellen Sie Einstellungen im relevanten Kontext dar, wenn alle der folgenden Bedingungen zutreffen:

-   Es gibt Standardeinstellungen, die für die meisten Benutzer gut funktionieren.
-   Es gibt eine kleine Anzahl von eigenständigen Einstellungen für ein bestimmtes Feature.
-   Benutzer erwarten wahrscheinlich, dass die Einstellungen mit der zugehörigen Funktion nicht mit einem zentralen Speicherort zu finden sind.
-   In der Benutzeroberfläche (User Interface, UI) gibt es einen offensichtlichen Speicherort für den Zugriff auf die Einstellungen.

Durch sorgfältige Aufmerksamkeit der Platzierung von Konfigurationseinstellungen können Sie die Belastung der Benutzer während der ersten Benutzerumgebung des Programms verringern.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="design-a-lightweight-setup"></a>Entwerfen eines Lightweight-Setups

Willkommen, weiter, weiter, weiter, weiter, weiter, installieren, Fertigstellen, herzlichen Glückwunsch! Ist das Setup gut vertraut? In der Vergangenheit haben Setup Programme diese Art von ineffizientes Design übernommen: eine lange Abfolge von Bildschirmen, die Benutzer in eine nicht mehr gewünschte Sequenz von Klicks einlädt, um Sie zu durchlaufen.

Wenn Benutzer die Einrichtung des Programms mit Wörtern wie "schneller" und "einfach" beschreiben, loben Sie die Benutzeroberflächen. Sie würden Ihr Programm viel lieber verwenden, als es einrichten zu können.

**Überprüfen Sie den Setup Entwurf auf nicht wesentliche Fragen, Optionen, Seiten und Pfade, und vermeiden Sie es, Sie zu beseitigen.** Führen Sie die Benutzer Forschung aus, um herauszufinden, welche Optionen Benutzer wirklich benötigen, und stellen Sie sicher, dass Sie nicht auf die Schaltfläche "weiter" über alle Seiten klicken. Verschieben Sie alle Optionen oder Fragen, die im Kontext des laufenden Programms besser adressiert sind.

Viele Setup Programme bieten Standardseiten nicht, weil Sie erforderlich oder hilfreich sind, aber weil Sie Standard sind. Beispielsweise werden bei Begrüßungs Seiten, Zusammenfassungs Seiten und herzlichen Glückwunsch Seiten häufig nur Klicks hinzugefügt. Stattdessen sollte das Setup Programm Seiten nur dann hinzufügen, wenn Sie zum Ausführen der Setup Aufgabe benötigt werden. Richtlinien zu den Typen von Setup Seiten und deren Auswertung finden Sie unter [Seiten Typen](#page-types) weiter unten in diesem Artikel.

![Screenshot der ersten Seite des ProClarity-Setups ](images/exper-setup-image2.png)

In diesem Beispiel löscht das Setup Programm die traditionelle Willkommensseite und geht direkt zum Unternehmen über.

Obwohl es möglicherweise erforderlich ist, unterschiedliche Verzweigungs Verzweigungen anzubieten (eine schnelle, typische Benutzer Darstellung und eine besser steuerbare, benutzerdefinierte Darstellung), stellen Sie sicher, dass Sie über ausreichend benutzerdefinierte Optionen verfügen, um die zusätzliche Komplexität zu gewährleisten Fügen Sie branches nur dann hinzu, wenn dies erforderlich ist. Einige unwichtige Optionen in einer benutzerdefinierten Verzweigung deuten darauf hin, dass der Setup Entwurf neu organisiert werden muss.

Ein weiterer Grund für die Optimierung des Setups besteht darin, dass unerfahrene Benutzer manchmal die Optionen überschreiben und befürchten, dass eine falsche Auswahl nicht rückgängig gemacht werden kann. Wenn Sie die Benutzer zwingen, Entscheidungen über Dinge zu treffen, die Sie nicht verstehen oder interessieren, können Sie Sie als ängstlich, inkompetent und sogar frustriert gestalten. Kein guter erster Eindruck. Es ist besser, Sie schnell und einfach zu gestalten, wenn Sie die Features in Ihrem Programm kennenlernen und bessere Entscheidungen zu den Funktions Optionen zu diesem Zeitpunkt treffen. Weitere Richtlinien finden Sie unter [Optimieren des Setups](#streamlining-setup) weiter unten in diesem Artikel.

Legen Sie die Einrichtung Ihrer Einrichtung so [einfach wie möglich, aber nicht einfacher](/previous-versions//dn742474(v=vs.85)). Programme, die auf sehr technische Benutzer abzielen, benötigen möglicherweise eine komplexe Einrichtung. Das Microsoft SQL Server Team hat z. b. ermittelt, dass Datenbankadministratoren die Kontrolle über viele Setup Optionen, wie z. b. Dateispeicher Orte, behalten möchten. Darüber hinaus ist SQL Server eine große Geschäftsanwendung mit einer Reihe von Komponenten, die sich in Bezug auf den Zweck und die Funktionalität stark unterscheiden. Während wir die Dinge einfach halten möchten, muss das Setup die Komplexität des Produkts und die Erwartungen und Anforderungen der Benutzer widerspiegeln.

Dennoch sollte es sich bei solchen komplexen Setup Programmen um die Ausnahme handeln, nicht um die Regel. Die meisten Windows-Programme sollten den Setup Vorgang mit einem einfachen, einzigen Schritt starten.

### <a name="setup-phases"></a>Setup Phasen

Mit gut entworfenen Setup Programmen können Benutzer während der zeitaufwändigen Aufgabe das herunterladen und Kopieren von Dateien andere Aktivitäten ausführen. Zum unbeaufsichtigten Ausführen der Setup Programme sind vier separate Phasen konzipiert:

-   **Die Entscheidungsphase.** Benutzer geben an, wie das Programm installiert und konfiguriert werden soll.
-   **Die Download Phase.** Für Programme, die aus dem Internet heruntergeladen wurden. Wenn das Programm über mehrere Anwendungen oder Versionen verfügt, geben Benutzer an, was während der Entscheidungsphase heruntergeladen werden soll.
-   **Die Installationsphase.** Das Setup Programm kopiert die Dateien und nimmt die entsprechenden Konfigurationsänderungen vor.
-   **Die Abschlussphase.** Alle verbleibenden Details, Schritte oder Probleme werden behoben.

Da die Installationsphase eine lange Zeit in Anspruch nehmen kann, sollte diese Phase so konzipiert werden, dass Sie ohne Benutzereingriff vollständig ausgeführt werden kann. Dies bedeutet, dass alle Fragen während der Entscheidungsphase angefordert werden sollten. alle auftretenden Probleme sollten in der Abschlussphase in die Warteschlange eingereiht und behandelt werden. **Wenn die Installationsphase mehr als eine Minute dauern muss, gehen Sie davon aus, dass Benutzer während der Download-und Installationsphasen etwas anderes tun werden.**

**Falsch:**

![Screenshot von "Installation der automatischen Berichterstellung" Dialog (dialog) ](images/exper-setup-image3.png)

In diesem Beispiel interruptet das Setup Programm den Fortschritt, um eine Frage zu stellen, die während der Entscheidungsphase angefordert worden sein sollte.

### <a name="present-helpful-progress"></a>Hilfreichen Fortschritt

Wenn Benutzer geduldig die Installationsphase der Einrichtung durchlaufen haben, können Sie eine Statusanzeige auf den offensichtlichen Abschluss ansehen, nur um die Statusanzeige zurückzusetzen und neu zu beginnen. Der gemeldete Fortschritt war irreführend und schließlich bedeutungslos.

Eine Variation dieses schwierigen Szenarios ist die "brinksmanship"-Installation: Benutzer sehen, dass der Fortschritt erreicht wird, z.b. 99 Prozent abgeschlossen, aber dennoch gezwungen werden, auf eine unverhältnismäßig lange Zeit zu warten, bevor Sie zu 100 Prozent abgeschlossen werden. Im Hinblick auf das, was für den Benutzer am wichtigsten ist, eine implizite Zusage über den Zeitraum, 99 der gewartet werden muss

Während der Download-und Installationsphasen haben Benutzer in der Regel zwei Dinge, die Sie kennen sollten: sollten Sie warten oder etwas anderes tun, und das Setup wird in Kürze ausgeführt. Während der Setup Vorgang ausreichend Variablen enthält, um zu verhindern, dass Sie vollständig genaue Fortschrittsinformationen bereitstellen, muss das Fortschritts Feedback genau genug sein, um diese beiden Fragen zu beantworten und die richtigen Erwartungen festzulegen. Zusätzlich zu einer Statusanzeige können Sie eine kurze Anweisung über die Gesamtzeit einschließen, die für den Prozess erwartet wird.

![Screenshot des Dialog Felds mit dem Installationsfortschritt ](images/exper-setup-image4.png)

In diesem Beispiel enthält die Seite Status eine kurze allgemeine Erklärung darüber, wie lange die Installation dauern könnte.

Gute Setup Programme verwenden Status Indikatoren effektiv, um Benutzern hilfreiche Informationen zum Fortschritt des Setup Programms bereitzustellen. Weitere Richtlinien finden Sie unter Status [leisten](progress-bars.md).

### <a name="design-for-all-setup-scenarios"></a>Entwurf für alle Setup Szenarien

Moderne Setup Programme müssen für eine Vielzahl von Installationsszenarien entwickelt werden:

-   Der Benutzer des Programms installiert ihn von einer Festplatte oder einer Netzwerkdatei Freigabe.
-   Der Benutzer des Programms lädt ihn aus dem Web herunter.
-   Ein ursprünglicher Gerätehersteller (Original Equipment Manufacturer, OEM) umfasst das Programm auf dem Computer in der Factory.
-   Ein IT-Experte installiert das Programm auf vielen Computern innerhalb eines Unternehmens.
-   Ein anderer Benutzer als der Benutzer installiert das Programm (z. b. ein übergeordnetes Element im Namen eines untergeordneten Elements oder ein Kollege, der denselben Computer wie ein anderer co-worker verwendet).

In Anbetracht dieser Szenarien sollten Sie nicht davon ausgehen, dass Benutzer das Programm immer für sich selbst installieren (indem Sie die Optionen für persönliche Einstellungen ungeeignet machen), den Prozess genau überwachen (die unbeaufsichtigte Installation ist wichtig) oder sogar eine grafische Benutzeroberfläche für die Aufgabe benötigen.

### <a name="dont-forget-the-uninstall-experience"></a>Vergessen Sie nicht die Deinstallation.

Um den Lebenszyklus der Software Einrichtung abzuschließen, müssen Benutzer in der Lage sein, Software zu entfernen, die Sie nicht möchten oder nicht mehr benötigen. Dies ist besonders wichtig, wenn Sie das Programm nicht selbst installiert haben (z. b. wenn es auf dem Computer vorab geladen wurde).

### <a name="handle-technical-support-strategically"></a>Technischer Support strategisch handhaben

Die Installation des Programms ist der einzige Task, den alle Benutzer erfolgreich ausführen müssen. Wenn Benutzer Ihr Programm nicht installieren können, müssen Sie Ihnen entweder einen teuren technischen Support bereitstellen, oder Sie sind nicht mehr für Ihre Benutzer.

Entwerfen Sie das Setup Programm, um dem technischen Support Team die Features und Informationen zur Verfügung zu stellen, die Sie benötigen, um die Benutzer erfolgreich installieren zu können. Diese Details sollten Benutzern normalerweise nicht zur Verfügung gestellt werden, Sie sollten jedoch bei Bedarf problemlos zugänglich sein.

**Falsch:**

![Screenshot der Bezeichnung mit dem Namen des COM-Servers ](images/exper-setup-image5.png)

In diesem Beispiel zeigt die Statusanzeige Details an, die nur für den technischen Support von Bedeutung sind.

Sorgen Sie für die normale Benutzer Darstellung, – nicht mit Informationen, die nur über den technischen Support verfügen. Notieren Sie stattdessen die Unterstützungs Informationen in einer Setup Protokolldatei. Und noch wichtiger ist, Benutzern zu helfen, den technischen Support mit klaren, präzisen Fehlermeldungen zu vermeiden, die Probleme hervorheben und praktische Lösungen bereitstellen. Stellen Sie bei Bedarf Links zu Hilfe Artikeln bereit. Es empfiehlt sich, eine Reparaturoption für das Setup Programm bereitzustellen, um fehlende oder beschädigte Dateien oder Einstellungen zu reparieren.

**Wenn Sie nur drei Dinge tun...**

1.  1. Legen Sie das Setup so einfach und einfach wie möglich zu. Denken Sie daran, dass die Benutzer das Setup nicht nutzen können. Achten Sie sorgfältig auf jede Frage, jede Option, jede Seite und denselben Pfad, und kürzen Sie alle Elemente, die für das Abschließen des Setups nicht unbedingt erforderlich sind.
2.  2. Entwurf für alle Setup Szenarien, einschließlich unbeaufsichtigter Installationen, Skript Installationen und Deinstallation. Stellen Sie für effiziente unbeaufsichtigte Installationen sicher, dass eine saubere Trennung zwischen den Setup Phasen vorliegt.
3.  3. Entwerfen Sie das Setup Programm so, dass Benutzer Setup Probleme selbst lösen können, und protokollieren Sie auch die Informationen, die für den technischen Support benötigt werden. Beachten Sie, dass das Setup die einzige Aufgabe ist, die alle Benutzer erfolgreich ausführen müssen.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Wenden Sie die Richtlinien des Standard-Assistenten für die Assistenten basierten Setup Programme an.** Verwenden Sie diese Richtlinien, um einen guten Seiten Entwurf, eine effektive Navigation, gute Steuerelement Bezeichnungen, die Verwendung von Haupt Anweisungen und die Verwendung der Hilfe zu ermitteln.
-   **Ermöglicht Benutzern das Neustarten des Setup Programms, an dem Sie ausgelassen wurden, wenn viele Benutzereingaben erforderlich sind oder eine lange Zeit in Anspruch nimmt.** Wenn Benutzer das Programm nach Abschluss des Abschlusses neu starten, stellen Sie die vorherige Benutzereingabe wieder her, und starten Sie dort, wo das Setup beendet wurde.
-   **Zeigen Sie die Setup Fenster nicht maximiert an.** Wenn ein Setup Fenster maximiert angezeigt wird, wird davon ausgegangen, dass die Benutzer Ihre ungeteilte Aufmerksamkeit erhalten, was unwahrscheinlich ist. Wählen Sie stattdessen eine Größe aus, die für den Inhalt geeignet ist, um eine einfache Darstellung zu gewährleisten.

### <a name="windows-integration"></a>Windows-Integration

-   **Benennen Sie die Setup Datei mit dem Namen "Setup.exe".** "Install.exe" ist eine akzeptable Alternative. Dies ermöglicht es Windows (und Benutzern), die Datei als Setup Programm zu erkennen.
    -   **Ausnahme:** Bei Programmen, die aus dem Internet heruntergeladen werden, können Benutzer ihren Downloadordner verwalten und organisieren, indem Sie den Namen des Programms in den Namen der Setup Datei einschließen. Beispielsweise SetupVisualStudioExpress2008.exe.
-   **Kopieren Sie Programmdateien an die richtigen Dateisystem Speicherorte.** Auf diese Weise können Benutzer und Fenster die Dateien besser suchen und organisieren. Weitere Informationen finden Sie in den [Windows-Datei System-Namespace-Verwendungs Richtlinien](../fileio/naming-a-file.md#namespaces).

### <a name="user-account-control"></a>Benutzerkontensteuerung

-   **Signieren Sie die ausführbare Datei für das Setup Digital.** Signierte ausführbare Dateien haben viele Vorteile, einschließlich der Verwendung einer spezifischeren Benutzerkontensteuerung, Benutzerkontensteuerung. Weitere Informationen zum Signieren von Dateien finden [Sie unter Einführung in die Code Signatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).
-   **Wenn ein Setup eine Erhöhung der Rechte erfordern kann, erhöhen Sie so spät wie möglich.** Zeigen Sie die Benutzeroberfläche für die Rechte Erweiterung erst an, wenn der Benutzer eine Option für eine Erhöhung der Rechte benötigt hat Normalerweise wird die Benutzeroberfläche für die Rechte Erweiterung während der Installationsphase und nicht in der Entscheidungsphase angezeigt. Wenn ein Setup jedoch immer eine Erhöhung erfordert, erhöhen Sie an seinem Einstiegspunkt.
-   **Erfordert immer erhöhte Rechte für die Deinstallation.** Dadurch wird verhindert, dass Schadsoftware kritische Software deinstalliert, ohne dass Benutzer diese Informationen kennen.
-   **Bleiben Sie nach der Erhöhung der Rechte erhöht, bis erweiterte Berechtigungen nicht mehr benötigt werden.** Benutzer müssen nicht mehrmals herauf Stufen, um eine Programminstallation abzuschließen.
-   **Wenn für die Installation besondere Berechtigungen erforderlich sind, überprüfen Sie die Anmelde Informationen des Benutzers, und melden Sie Probleme auf der ersten oder zweiten Seite.** Erlauben Sie Benutzern nicht, sehr viel Arbeit auszuführen, um zu ermitteln, dass Sie nicht über die richtigen Anmelde Informationen verfügen, um die Installation abzuschließen.
-   **Erfordert die geringstmöglichen Berechtigungen.** Administratoren können beispielsweise nicht nur die Software installieren, die Anmelde Informationen des Domänen Administrators erfordert.

Weitere Richtlinien finden Sie unter [Benutzerkontensteuerung](winenv-uac.md).

### <a name="restarting-windows"></a>Neustarten von Windows

-   **Vermeiden Sie das Neustarten von Windows.** Die meisten Programme sollten installiert werden, ohne dass Windows neu gestartet wird. Der primäre Grund für die Installation oder Aktualisierung von Programmen erfordert einen Systemneustart, da einige der beteiligten Dateien derzeit von einem laufenden Programm verwendet werden. In diesem Fall ist es eine bessere Alternative, Benutzer auf die Situation aufmerksam zu machen, Benutzern zu gestatten, diese Programme zu schließen, und die Aktion zu wiederholen. Weitere Informationen zum Vermeiden von Neustarts finden Sie unter [Neustart-Manager](../rstmgr/restart-manager-portal.md).
-   **Wenn beim Setup Windows neu gestartet werden muss:**
    -   **Verwenden Sie einen einzelnen Neustart.** Verzögern Sie den Neustart, der für alle Voraussetzungen erforderlich ist, bis das Programm und seine Updates vollständig installiert sind.
    -   **Legen Sie fest, wann der Benutzer das passiert.** Starten Sie Windows nicht automatisch neu, da Benutzer möglicherweise die Arbeit verlieren. Stellen Sie sicher, dass es den Benutzern klar ist, dass Sie über eine Auswahl verfügen.

        **Falsch:**

        ![Screenshot des Dialog Felds mit Neustart und Abbruch ](images/exper-setup-image6.png)

        In diesem Beispiel haben Benutzer anscheinend keine Auswahl, wann Windows neu gestartet werden soll.

    -   **Wenn der Benutzer die sofortige Neustarts von Windows auswählt, stellt das endgültige Feedback als Erfolg und nicht als Fehler dar.** Obwohl die Installation technisch gesehen nicht abgeschlossen ist, war sie aus der Sicht des Benutzers erfolgreich.

### <a name="streamlining-setup"></a>Optimieren des Setups

-   **Wenn dies praktikabel ist, starten Sie den Installationsvorgang mit einem einzigen Schritt.** Anstatt beispielsweise eine separate Seite in Setup für die Lizenzbedingungen hinzuzufügen, können Sie stattdessen einen Link zur Verfügung stellen. Wenn Sie mit den Begriffen verknüpfen:
    -   Formulieren Sie die Schaltfläche "Commit" als "zustimmen und installieren", um explizite Zustimmung zum Akzeptieren der Lizenzbedingungen anzufordern.
    -   Stellen Sie sicher, dass der Link für die Lizenzvereinbarung nicht getrennt werden kann, indem Sie anstelle einer Webseite eine Verknüpfung mit einer lokalen Datei erstellen.
    -   Ermöglicht das Drucken der Lizenzvereinbarung aus dem Anzeige Fenster.
-   **Vermeiden Sie unnötige Optionen und Fragen.**
    -   Verschieben Sie Optionen, die für die erste Verwendung des Programms oder Features besser geeignet sind.

        ![Screenshot des Dialog Felds mit der Option "benutzerdefinierte Einstellungen" ](images/exper-setup-image7.png)

        In diesem Beispiel stellt Windows Media Player bei der ersten Verwendung des Programms benutzerspezifische Datenschutzoptionen dar.

    -   Fragen Sie die Benutzer nicht über den Systemstatus. Erkennen Sie diese Informationen automatisch, und fordern Sie die Benutzer auf, nur zu überprüfen, ob ein Grund für die Änderung vorliegt.
    -   Stellen Sie keine Fragen zu wichtigen Details. Beispielsweise kann für typische Windows-Programme sicher angenommen werden, dass Sie Programmdateien in den Ordner "Programme" Kopieren sollten.

        **Falsch:**

        ![Screenshot des Dialog Felds mit dem Installations Speicherort ](images/exper-setup-image8.png)

        In diesem Beispiel sollte das Setup optimiert werden, indem die Anforderung für die Eingabe des Dateispeicher Orts eliminiert wird. Aufgrund der Größe des Programms ist es für die meisten Benutzer nicht wichtig, und klicken Sie einfach auf Weiter.

    -   Fragen Sie nicht, was Sie trotzdem tun sollten. Die meisten Programme sollten z. b. keine Option enthalten, um das Programmsymbol auf dem Desktop zu platzieren.
    -   Bestätigen Sie den Setup Abbruch nicht. Wenn Benutzer während des Setups auf Abbrechen klicken, nehmen Sie an, dass der Abbruch beabsichtigt war, und schließen Sie das Programm ohne Bestätigung. Wenn dadurch eine beträchtliche Zeit oder Mühe verloren geht, können Sie es Benutzern ermöglichen, das Setup Programm neu zu starten und zu übernehmen, wo Sie aufgehört haben.

-   **Optimieren Sie die unbeaufsichtigte Installation.**
    -   Stellen Sie während der Entscheidungsphase alle Optionen und Fragen zur Verfügung.
    -   Bei den Download-und Installationsphasen ist es erforderlich, dass die Benutzereingaben für Probleme, die bis zum Ende der Phase aufgetreten sind, verzögert werden. Auf diese Weise können Benutzer die Installation unbeaufsichtigt lassen, bis Sie zu Ihrem Zweck zurückkehren.
-   **Vermeiden Sie unnötige Seiten.** Wenn die meisten Benutzer auf einer Seite immer einfach auf "weiter" klicken, sollten Sie die Seite entfernen. Richtlinien zum Entfernen bestimmter Seiten Typen finden Sie unter [Page Types](#page-types).
-   **Vermeiden Sie unnötigen Text.**
    -   Entfernen Sie redundanten Text aus Anweisungen und Bezeichnungen.
    -   Erläutern Sie nicht die grundlegenden Konzepte der Windows-Verwendung
        -   Interaktion mit Steuerelementen (Beispiele: Klicken Sie auf "weiter", um zu beginnen. Klicken Sie auf Optionen, um weitere Optionen zu erhalten. Weitere Informationen erhalten Sie, indem Sie auf Hilfe klicken.
        -   Funktionsweise von Assistenten (Beispiel: Wenn Sie Einstellungen überprüfen oder ändern möchten, klicken Sie auf "zurück").
        -   Funktionsweise des Setups (Beispiel: Dieses Programm kopiert die Programmdateien auf die Festplatte...).
-   **Vermeiden Sie unnötigen Aufwand.**
    -   Geben Sie gute Standardwerte an:
        -   Wählen Sie im Allgemeinen die sicherste und private Antwort als Standard aus.
        -   Wenn Sicherheit und Datenschutz keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequeme Antwort aus.

            ![Screenshot des Dialog Felds mit dem angezeigten Namen und Unternehmen ](images/exper-setup-image9.png)

            In diesem Beispiel werden der Benutzername und die Organisation, die standardmäßig bereitgestellt werden, aus der Registrierung abgerufen.

        -   Wenn eine Option dringend empfohlen wird, sollten Sie diese standardmäßig auswählen oder der Bezeichnung "(empfohlen)" hinzufügen.

    -   Seiten werden automatisch fortgesetzt, wenn eine Seite keine Eingabe hat und die Aufgabe erfolgreich ausgeführt wird, z. b. mit den Seiten Download, Installation, Fortschritt und Updates. Wenn der Schritt abgeschlossen ist, bleiben Sie auf diesen Seiten, um Probleme anzuzeigen.
    -   Wenn dies praktikabel ist, starten Sie das Programm automatisch, wenn das Setup abgeschlossen ist, anstatt einen herzlichen Glückwunsch oder eine Abschluss Seite anzuzeigen. Wenn das Setup interaktiv ausgeführt wird, gehen Sie davon aus, dass der Benutzer Ihr Programm installiert, um es sofort auszuführen, sodass das Ausführen des Programms das beste Feedback ist, um zu zeigen, dass das Setup fertiggestellt ist. Das automatische Ausführen des Programms ist nicht praktikabel, wenn beim Setup mehrere Programme installiert werden (z. b. eine Sammlung, die aus vielen Programmen besteht), wenn Setup nicht interaktiv ausgeführt wird oder wenn der Installationsvorgang nach dem Setup nicht ausgeführt werden kann.

### <a name="page-types"></a>Seiten Typen

**Seiten "Willkommen" und "Einstieg"**

-   **Entfernen Sie Willkommens Seiten.** Obwohl es großartig ist, sich zu freuen, klicken Benutzer in der Regel einfach auf Weiter, ohne zu lesen. Und da Benutzer in der Regel diese Seiten überspringen, ohne zu lesen, ist der Text in der Regel nur mit dem Status "offensichtlich".

    **Falsch:**

    ![Screenshot des Begrüßungs Bildschirms mit "Next" und "Cancel" ](images/exper-setup-image10.png)

    In diesem Beispiel gibt es nichts, was der Benutzer tun muss, sondern auf "weiter".

-   **Verwenden Sie die Seite für die ersten Schritte nur, wenn Sie Benutzer über die Voraussetzungen für die Installation informieren müssen.** Zu diesen Voraussetzungen gehört das Installieren erforderlicher Software oder Hardware, das durchführen erforderlicher Systemkonfigurations Änderungen und Updates, das Ausführen einer Systemsicherung zum Schutz vor Datenverlusten oder das Abrufen erforderlicher Informationen, die der Benutzer wahrscheinlich nicht bereits enthält.
-   **Stellen Sie nach Möglichkeit sicher, dass Sie die erforderlichen Komponenten direkt aus dem Setup Programm ausführen können.** Benutzer sollten die Schritte nur manuell ausführen müssen, wenn es keine Alternative gibt.
-   Wenn eine Willkommensseite oder die Seite "erste Schritte" nicht verwendet wird, geben Sie **den Programmnamen und die Beschreibung an, was die erste Seite des Setup Programms ist.** Sie können die begrüßungssprache als einführenden Text verwenden, sofern der Zweck der Seite eindeutig ist.

**Seiten mit Lizenzbedingungen**

-   **Schreiben Sie die Lizenzbedingungen mithilfe von Klartext und präziser Text.** Verwenden Sie die Sprache einfach. Vermeiden Sie "legalesisch".
-   **Wird in einem Format angezeigt, das leicht zu lesen und zu scannen ist.** Verwenden Sie keine langen Passagen von Großbuchstaben.

    **Falsch:**

    ![Screenshot der Lizenzbedingungen in Großbuchstaben ](images/exper-setup-image11.png)

    In diesem Beispiel ist die Schreibweise von Groß-und Kleinbuchstaben für die Begriffe schwierig, sodass der Benutzer mehr als notwendig einen Bildlauf durchführen kann.

-   **Erfordert explizite Zustimmung, um die Lizenzbedingungen zu akzeptieren.** Die Lizenz Annahme sollte nie standardmäßig ausgewählt werden. Wenn options Felder verwendet werden, um die Annahme anzuzeigen, lassen Sie die Optionen standardmäßig deaktiviert, und die Benutzer müssen die Bedingungen akzeptieren, bevor Sie die Schaltfläche weiter aktivieren.

    ![Screenshot des Dialog Felds mit der Schaltfläche "weiter" ](images/exper-setup-image12.png)

    In diesem Beispiel wird die Schaltfläche Weiter deaktiviert, bis die Benutzer die Lizenzbedingungen explizit akzeptiert haben.

-   **Es ist nicht erforderlich, dass Benutzer einen Bildlauf zum unteren Rand des Lizenzvertrags durchführen, bevor die Schaltfläche Weiter aktiviert ist.** Dadurch wird den Benutzern eine unnötige Belastung auferlegt, um zu verstehen, warum die Schaltfläche Weiter deaktiviert ist.
-   **Geben Sie einen Druckbefehl an,** entweder mit einer Befehls Schaltfläche oder mit einem Kontextmenü. Stellen Sie die Begriffe in einem für das Drucken optimierten Format dar.

**Produkt Registrierungsseiten**

-   **Benutzer müssen sich nur registrieren, wenn Sie für die Verwendung des Programms erforderlich sind.** Erläutern Sie eindeutig, warum sich Benutzer registrieren müssen.
-   **Stellen Sie die optionale Registrierung nur dann bereit, wenn ein eindeutiger Benutzer Vorteil vorliegt,** z. b. um Benutzer über Produktupdates zu benachrichtigen. Lassen Sie diese Option standardmäßig deaktiviert.
-   **Ermöglicht Benutzern die spätere Registrierung.** Geben Sie maximal drei Erinnerungen an, und erlauben Sie Benutzern, die Erinnerungen mit einem einzigen Mausklick zu verwerfen.

**Bereichs Seiten (typisch, Benutzer definiert oder minimal)**

-   **Bevorzugen Sie diese Seite, um diese Seite auszuschließen.** Nehmen wir an, dass die meisten Benutzer die typische Einrichtung wünschen (und diese so entwerfen, dass Sie für die meisten Benutzer gut funktioniert).
-   Wenn Sie eine Bereichs Seite einschließen müssen:
    -   **Erläutern Sie die Unterschiede zwischen den Optionen hinsichtlich Funktionalität und Speicherplatz.** Benutzer verlassen sich auf die Übersichtlichkeit der Informationen auf der Bereichs Seite, um sicherzustellen, dass Sie die richtige Wahl treffen.
    -   **Stellen Sie sicher, dass die benutzerdefinierten Optionen nur für einen kleinen Prozentsatz der Benutzer erforderlich sind, während Sie von den meisten Benutzern problemlos ignoriert werden können.** Andernfalls sollten sich die Optionen im typischen Setup Pfad befinden.
    -   **Wenn Benutzer benutzerdefinierte Optionen auswählen, lassen Sie die üblichen Installationsoptionen standardmäßig ausgewählt.** Benutzer berücksichtigen die typische Installation als Baseline und möchten anpassen, indem Sie Optionen für diese Baseline hinzufügen oder entfernen.
-   Wenn Sie eine benutzerdefinierte Installationsoption verwenden müssen, **sollten Sie die Verwendung von relativer Schaltflächen Größe und-Platzierung in Erwägung gezogen, um die meisten Benutzer an die typische Installation**

    ![Screenshot des Dialog Felds mit der Schaltfläche "große Installation" ](images/exper-setup-image13.png)

    In diesem Beispiel verstärkt der Seiten Entwurf die Tatsache, dass die meisten Benutzer die typische Installation entscheiden sollten.

**Eingabe Seiten**

-   **Verringern Sie die Anzahl der Setup Optionen, indem Sie die richtigen Schritte standardmäßig durchgeführt haben.** Möglichkeiten zum Ausschließen von Optionen finden Sie unter [Optimieren der Einrichtung](#streamlining-setup).
-   **Stellen Sie nach Möglichkeit akzeptable Standardwerte bereit.** Wählen Sie Standardwerte aus, die sicher und privat sind und für die meisten Benutzer ohne Änderungen zulässig sind.
-   **Wenn Ihr Programm ungewöhnliche Anforderungen hat, sollten Sie eine einzelne Seite mit Fragen und Optionen haben.** Wenn Ihr Programm jedoch mehrere Seiten mit Fragen und Optionen erfordert, zeigen Sie Sie im Hauptabschnitt der Assistenten Seite an. Versuchen Sie nicht, die Anzahl der Seiten technisch zu verringern, indem Sie Optionen in Dialogfeldern oder mithilfe von Registerkarten platzieren.
-   ![Screenshot des Setup Dialogfelds mit vier Optionen ](images/exper-setup-image14.png)
-   In diesem Beispiel sind die Optionen auf eine einzelne Seite beschränkt.
-   **Überprüfen Sie die Eingabe so bald wie möglich:**
    -   Beim Eintrag sind ungültige Zeichen zulässig.
    -   Verwenden Sie [Ballons](ctrl-balloons.md) , um Probleme mit ungültigen Textfeldern zu melden.
    -   Überprüfen Sie verwandte Felder auf einer Seite, wenn Benutzer auf Weiter klicken.
    -   Überprüfen Sie verwandte Felder auf den Eingabe Seiten, sobald Probleme erkannt werden können.
-   **Gibt die Schaltfläche Durchsuchen für alle bearbeitbaren Dateipfade an.** Ermöglicht Benutzern das Angeben von Netzwerkpfaden.
-   **Geben Sie auf der Seite abschließende Eingabe die Bezeichnung Commit-Schaltfläche Installieren und nicht weiter ein.** Benutzer sollten beim Start der Installation nicht überrascht sein. Stellen Sie vor dem Commit-Punkt sicher, dass Benutzer problemlos Einstellungen ändern können.

**Installations Seiten starten**

-   **Entfernen Sie diese Seite, wenn Sie keine der vorherigen Optionen zusammenfassen und mit der Installation beginnen soll.** Wenn die Eingabe Seiten eindeutig sind und nur wenige sind, sollten Sie Sie nicht zusammenfassen müssen. Stattdessen sollte die letzte Eingabe Seite über die Schaltfläche Installieren verfügen, die direkt zur Seite Status führt.
-   **Stellen Sie für komplexe Installationen, die auf IT-Experten abzielen, eine Installationsseite mit einer umfassenden Liste von Änderungen bereit, die vom Setup Programm durchgeführt werden.** Viele IT-Experten haben strikte Change Management Kontrolle, sodass Sie wissen müssen, welche Auswirkung die Installation des Programms ausführlich hat.

**Fortschritts Seiten**

-   **Geben Sie immer eine Fortschritts Seite an,** selbst wenn das Programm schnell installiert wird. Geben Sie eine separate Fortschritts Seite für [die Download Phase](#setup-phases) an, sofern vorhanden. Deaktivieren Sie die Schaltflächen "zurück&quot; (oder &quot;zurück") und "weiter", während das Setup ausgeführt wird, lassen Sie jedoch die Schaltfläche Abbrechen aktiviert und reagiert

    ![Screenshot des Dialog Felds mit der Statusanzeige ](images/exper-setup-image15.png)

    Eine typische Statusseite.

-   **Verwenden Sie eine einzelne, bestimmte Statusanzeige.** Befolgen Sie die [Richtlinien für die bestimmte der Statusleiste](progress-bars.md), einschließlich:
    -   Geben Sie den Abschluss eindeutig an. Lassen Sie eine Statusanzeige nicht zu 100 Prozent wechseln, es sei denn, der Vorgang wurde abgeschlossen.
    -   Starten Sie den Fortschritt nicht. Eine Statusanzeige verliert ihren Wert, wenn Sie neu gestartet wird (möglicherweise weil ein Schritt im Vorgang abgeschlossen ist), da Benutzer nicht wissen, wann der Vorgang abgeschlossen wird. Nehmen Sie stattdessen an, dass alle Schritte des Vorgangs einen Teil des Fortschritts aufweisen und die Statusanzeige einmal abgeschlossen werden soll.
-   **Geben Sie eine kurze Beschreibung des aktuellen Schritts oberhalb der Statusanzeige an.** Bei schnell Installationen ist dieser Text unnötig. die Statusanzeige ist ausreichend. Bei Installationen, die eine Minute oder länger erfordern, kann Text für Benutzer, die an der Installation teilnehmen, hilfreich sein.
    -   **Verwenden Sie Satzfragmente, die in der Regel mit einem Verb beginnen und mit einem Auslassungs Zeichen enden.** Beispiele: Dateien werden kopiert..., erforderliche Komponenten werden installiert...
    -   **Platzieren Sie Text oberhalb der Leiste, nicht weiter unten.**

        **Falsch:**

        ![Screenshot von Text, der in der Statusanzeige angezeigt wird ](images/exper-setup-image16.png)

        In diesem Beispiel sollte der erläuternde Text oberhalb der Statusanzeige angezeigt werden.

    -   **Verzichten Sie darauf, die Statusseite mit unnötigen Details zu gruppieren.** Diese Seite ist für [technischen Support](#handle-technical-support-strategically)nicht verfügbar, daher ist es nicht erforderlich, Registrierungs-GUIDs oder bestimmte kopierte Dateien anzuzeigen.

        **Falsch:**

        ![Screenshot der GUID, die über der Statusanzeige angezeigt wird ](images/exper-setup-image17.png)

        In diesem Beispiel sind technische Details wie GUIDs für Benutzer bedeutungslos.

**Fehlerseiten**

-   **Wenn beim Setup ein erhebliches Problem auftritt, zeigen Sie eine Fehlerseite an, auf der die Probleme erläutert werden, sowie praktische Schritte, um Sie zu beheben.** Zeigen Sie die Seite mit einem Fehler Symbol an. Verwenden Sie für diesen Zweck kein Dialogfeld.

    ![Screenshot der Fehlerseite und des Symbols ](images/exper-setup-image18.png)

    In diesem Beispiel wird der Installationsfehler auf einer Fehlerseite sowie einige Schritte zum Beheben des Problems erläutert.

-   **Wenn Setup mit einem geringfügigen BEHEB baren Problem abgeschlossen ist, stellen Sie das Problem als zusätzliche Aufgabe dar, anstatt einen Fehler zu beheben.** Verwenden Sie positive, erfolgsorientierte, ermutigende Sprache, keine Begriffe wie Fehler, Fehler oder Problem. Verwenden Sie kein Fehler Symbol.

**Herzlichen Glückwunsch/Vervollständigungs Seiten**

-   **Wenn Sie ein einzelnes Programm interaktiv installieren, starten Sie das Programm (und schließen Sie den Setup-Assistenten), um ein erfolgreiches Setup anzugeben, anstatt eine Abschluss Seite anzuzeigen. Ausnahmen**
    -   Von Setups, die über die Befehlszeile ausgeführt werden, sollten Programme nicht gestartet werden.
    -   Bei automatischen Updates (z. b. Windows Update) sollten Programme nicht gestartet werden.
    -   Bei der Gruppenrichtlinien Installation sollten keine Programme gestartet werden.
    -   Alle IT-Experten-Setup Szenarios (da Sie nicht zur eigenen Verwendung installiert werden).
-   **Wenn nach der Installation nach Verfolgungs Schritte ausgeführt werden sollen, können Sie diese auf der Seite Abschluss des Setups auflisten.** Um jedoch eine Abschluss Seite zu rechtfertigen, stellen Sie sicher, dass die Benutzer wahrscheinlich die Schritte ausführen, und dass die Schritte wirklich angegeben werden müssen (d. h., Sie sind nicht offensichtlich).

    **Falsch:**

    ![Screenshot der Seite mit dem anzeigen, dass das Setup abgeschlossen ist ](images/exper-setup-image19.png)

    In diesem Beispiel gibt eine unnötige Vervollständigungs Seite das offensichtliche an. Windows Update wird automatisch ausgeführt, daher gibt es keinen Grund dafür, dass Benutzer es manuell ausführen können.

-   **Wenn Sie eine Sammlung von Programmen installieren, zeigen Sie eine Abschluss Seite an, um den Erfolg und alle nachfolgenden Schritte anzuzeigen, die möglicherweise erforderlich sind.**

    ![Screenshot der Office Suite-Setup-Endseite ](images/exper-setup-image20.png)

    In diesem Beispiel wurden mehrere Programme installiert, daher ist es nicht sinnvoll, ein bestimmtes Programm automatisch zu starten. Eine Vervollständigungs Seite ist besser geeignet.

### <a name="leaving-users-in-control"></a>Belassen von Benutzern in der Kontrolle

-   **Erfassen Sie keine persönlichen Informationen, z. b. für Marketingzwecke.** Setup bietet keine Gelegenheit, ihre eigene Agenda zu überführen, andere Programmangebote zu verkaufen oder Marktforschung auszuführen. auf diese Weise können Sie die Vertrauensstellung mit ihren Benutzern beschädigen.
-   **Erzwingen Sie nicht, dass Benutzer optionale Features installieren.** Erlauben [Sie stattdessen die](glossary.md) Verwendung von. Benutzer sollten z. b. explizit die Installation einer Windows-Desktop Mini Anwendung auswählen.
-   **Ermöglicht Benutzern das Hinzufügen oder Entfernen optionaler Features mithilfe des Setup Programms nach dem ersten Setup.** Benutzer können diese Aufgabe mithilfe der System Steuerungs Option **Programm deinstallieren oder ändern** ausführen.
-   **Erläutern Sie für Initiativen zur Verbesserung der Benutzerfreundlichkeit, welche Daten übertragen werden, wie Sie verwendet werden und wie lange Sie aufbewahrt werden.** Verwenden Sie für diesen Zweck einen Link zu einem Hilfethema zur Datenschutzerklärung.
-   **Vermeiden Sie die Verwendung von Sound,** da viele Installationsszenarien unbeaufsichtigt sind und der Sound selbst bei beaufsichtigten Installationen unnötig ablenkend sein kann.

### <a name="security"></a>Sicherheit

-   **Bei der Internet basierten Einrichtung sollten Sie während der ersten Installation automatisch Sicherheitsupdates bereitstellen.** Benutzer sollten nicht in einem separaten Schritt aktualisieren müssen.
-   **Vermeiden Sie, dass Benutzer Firewalls als Voraussetzung für die Installation des Programms deaktivieren.**
-   Wenn eine Firewall ausgeschaltet werden muss, gehen Sie wie folgt vor:
    -   **Beschränken Sie die Dauer dieser Bedingung auf so kurz wie möglich.**
    -   **Zeigen Sie explizit an, wenn Benutzer die Firewall wieder einschalten können.**

### <a name="uninstall"></a>Deinstallieren

-   **Bei der Deinstallation sollten alle Ablauf Verfolgungen eines Programms entfernt werden, einschließlich der folgenden:**
    -   Programmdateien, einschließlich des Setup Programms.
    -   Start Menüeinträge.
    -   Desktop Symbole und Schnellstart Symbole (sofern vorhanden).
    -   Registrierungs Einstellungen.
    -   Dateizuordnungen.
-   **Die Deinstallation sollte Folgendes hinter sich gehen:**
    -   Vom Benutzer erstellte Dateien, z. b. Dokument Dateien.
    -   Freigegebene Dynamic-Link-Bibliotheken, die im System Ordner gespeichert sind.

### <a name="help-and-support"></a>Hilfe und Support

-   **Entwerfen Sie das Setup Programm so, dass Sie keine Hilfe benötigen, indem Sie klare, selbsterklärende Fragen stellen.** Reservieren Sie Hilfe für erweiterte Fragen, die wirklich von weiteren Erläuterungen profitieren.
-   **Verwenden Sie keine Info Dateien.** Diese Dateien sind mittlerweile veraltet und können von Benutzern nicht mehr gelesen werden. Geben Sie stattdessen Online Inhalte an, falls erforderlich.
-   **Verknüpfen Sie entsprechende Hilfe Themen oder Informationen zur Problembehandlung in den Setup Fehlermeldungen.** Stellen Sie sicher, dass der Hilfe Inhalt einen klaren Pfad zur Behebung des Problems enthält. Weitere Informationen finden Sie unter [Fehlermeldungen](mess-error.md).
-   **Erstellen Sie Protokolldateien, um Informationen zu erfassen, die für technischen Support hilfreich sind** Überlassen Sie die Setup-Benutzeroberfläche nicht mit technischen Support bezogenen Details, die für die meisten Benutzer bedeutungslos sind. Verwenden Sie stattdessen Protokolldateien für diesen Zweck.

### <a name="text"></a>Text

-   **Seien Sie präzise.** Die Setup-Assistenten überschreiben häufig Features und Optionen und verwenden Textblöcke, die schwer schnell zu scannen sind. **Ausnahmen:**
    -   Benennen Sie alle Akronyme um. Das Setup ist oft das erste Mal für Benutzer mit Ihrem Programm. gehen Sie also nicht davon aus, dass Sie den Fachjargon verstehen, wie z. b.
    -   Erläutern Sie unbekannte Terminologie und Konzepte, vorzugsweise, aber verwenden Sie ggf. Hilfe Themen.
-   **Bevorzugen Sie einen freundlichen, professionellen Ton. vermeiden Sie einen übermäßig technischen Ton.**

**Falsch:**

Beschränken Sie die Installation auf Benutzerbasis.

**Richtig:**

Nur für mich installieren.

-   Verwenden Sie in Befehlszeilen Bezeichnungen nicht jetzt, da die Unmittelbarkeit des Befehls für die Gewährung übernommen werden kann.
    -   **Ausnahme:** Verwenden Sie bei Bedarf jetzt, um Befehle zu unterscheiden, die eine Aufgabe aus Befehlen starten, die eine Aufgabe sofort ausführen.

![Screenshot der Schaltfläche "herunterladen" ](images/exper-setup-image21.png)

Wenn Sie in diesem Beispiel auf die Befehls Schaltfläche klicken, wird ein Fenster oder eine Seite angezeigt, das Benutzern das Herunterladen ermöglicht.

![Screenshot der Schaltfläche "jetzt herunterladen" ](images/exper-setup-image22.png)

Wenn Sie in diesem Beispiel auf die Schaltfläche Befehl klicken, wird der Download sofort durchführt.

Nur ein Befehl in einem Aufgaben Fluss sollte mit "Now" gekennzeichnet werden. So sollte z. b. der Befehl " **jetzt herunterladen** " niemals von einem anderen Befehl " **jetzt herunterladen** " befolgt werden.

-   Verwenden Sie Lizenzbedingungen, nicht Lizenzvertrag, Lizenzierungs Vertrag, Endbenutzer-Lizenzvertrag oder EULA.

Weitere Richtlinien finden Sie unter [Style und Tone](text-style-tone.md).

## <a name="documentation"></a>Dokumentation

-   Als Verb ist das Einrichten von zwei Wörtern: als Adjektiv oder Substantiv ist Setup ein Wort.
-   Das Setup Programm ist groß geschrieben und wird nicht mit einem Bindestrich überschwemmt.
-   Verwenden Sie installieren, um auf das Hinzufügen von Hardware oder Software zu einem Computersystem zu verweisen.
-   Verwenden Sie Install nicht als Substantiv. Verwenden Sie stattdessen die-Installation.
-   Verwenden Sie Neustart, nicht Neustart. Geben Sie an, dass es sich um den Computer handelt, nicht um ein Programm, das neu gestartet wird.

 

 