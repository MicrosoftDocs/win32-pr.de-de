---
title: Einrichten
description: Benutzer können keine Software installieren, daher müssen moderne Einrichtungserfahrungen einfach, effizient und problemlos sein.
ms.assetid: ed0265a6-4c39-4a1f-9493-e316a6519df7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 905411c5ae08d2112943088d514ab300abb19ec2b8081158ebdfd896fc2c61ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119818273"
---
# <a name="setup"></a>Einrichten

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Benutzer können keine Software installieren, daher müssen moderne Einrichtungserfahrungen einfach, effizient und problemlos sein.

Setup bezieht sich in der Regel auf die Installation und konfiguration eines Programms. Das Setup kann sich jedoch auch auf den gesamten Installationslebenszyklus beziehen, einschließlich Erstinstallation, inkrementeller Programmupdates (z. B. Versionsupgrades oder Service Packs), Reparatur und Deinstallation.

Die meisten Benutzer betrachten das Setup als notwendig, das so schnell wie möglich durchgeführt werden muss. Bei der Installation des Programms geht es darum, es zu verwenden, nicht aufzählbare Entscheidungen zur Konfiguration und Nutzung zu treffen oder, noch schlechter, viel Zeit mit der Beantwortung persönlicher Fragen zu verbringen, die für Registrierungs- oder Marketingzwecke verwendet werden.

![Screenshot: Dialogfeld "Setup" mit vier Optionen](images/exper-setup-image1.png)

Eine optimierte Einrichtungserfahrung.

Die Einrichtungserfahrung in Kombination mit der ersten Verwendung des Programms wird als erste Erfahrung bezeichnet. Ihr Programm sollte benutzern eine optimierte erste Erfahrung bieten. Jede Frage oder jeder Schritt, die nicht erforderlich ist oder verschoben werden könnte, verzögert die Verwendung Ihres Programms. Zu komplexe Setupprogramme sind Relices aus einem anderen Alter.

**Hinweis:** Richtlinien im Zusammenhang mit [der ersten Erfahrung](exper-first-exper.md) mit einem Programm und Assistenten werden in separaten Artikeln vorgestellt. [](win-wizards.md)

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Während alle Microsoft Windows-Programme eine Art Setupprogramm benötigen, haben Sie die Wahl, wo Sie Programmeinstellungen festlegen möchten:

-   Einrichten
-   Erste Verwendung des Programms
-   Zentralisierte Programmoptionen
-   Im Kontext der Verwendung des Features

**Einrichtung**

Legen Sie einstellungen im Setup in den folgendem Fall vor:

-   Die richtigen Einstellungen sind erforderlich, um das Programm zu verwenden, und sie gelten für alle Benutzer.
-   Die Verwendung von Standardeinstellungen ist nicht akzeptabel, da es keine sichere Standardeinstellung gibt, Benutzer wahrscheinlich Einstellungen auswählen, die nicht die Standardeinstellung sind, oder die Standardeinstellungen erfordern die Zustimmung des Benutzers.
-   Benutzer sollten wichtige Einstellungen nach dem Setup ändern, was jedoch nicht wahrscheinlich ist.

**Erste Verwendung des Programms**

Stellen Sie Einstellungen für die erste Verwendung des Programms vor, wenn:

-   Die richtigen Einstellungen sind erforderlich, um das Programm zu verwenden, und sie gelten für einzelne Benutzer.
-   Die Verwendung von Standardeinstellungen ist nicht akzeptabel, da es keine sichere Standardeinstellung gibt, Benutzer wahrscheinlich Einstellungen auswählen, die nicht die Standardeinstellung sind, oder die Standardeinstellungen erfordern die Zustimmung des Benutzers.
-   Benutzer sollten wichtige Einstellungen mithilfe der Programmoptionen ändern, was jedoch nicht wahrscheinlich ist.
-   Die Einstellungen passen eine Kernerfahrung an oder eine, die für die persönliche Identifikation eines Benutzers mit dem Programm entscheidend ist.

Für solche Einstellungen treffen Benutzer wahrscheinlich bessere Entscheidungen im Kontext des Programms als innerhalb des Setups.

**Zentralisierte Programmoptionen**

Stellen Sie Einstellungen im Dialogfeld "Optionen" des Programms [vor,](win-property-win.md) wenn alle der folgenden Bedingungen zu erfüllen sind:

-   Es gibt Standardeinstellungen, die für die meisten Benutzer gut funktionieren.
-   Es gibt viele Einstellungen, die für alle Features und Aufgaben gelten.
-   Benutzer erwarten wahrscheinlich eher, dass sie die Einstellungen an einem zentralen Ort finden.

**Im Kontext der Verwendung des Features**

Legen Sie Einstellungen im relevanten Kontext vor, wenn alle der folgenden Bedingungen erfüllt sind:

-   Es gibt Standardeinstellungen, die für die meisten Benutzer gut funktionieren.
-   Es gibt eine kleine Anzahl eigenständiger Einstellungen für ein bestimmtes Feature.
-   Benutzer erwarten wahrscheinlich eher, dass sie die Einstellungen mit dem zugeordneten Feature finden als einen zentralisierten Standort.
-   Auf der Benutzeroberfläche (UI) ist ein offensichtlicher Ort für den Zugriff auf die Einstellungen verfügbar.

Durch sorgfältiges Achten auf die Platzierung von Konfigurationseinstellungen können Sie den Aufwand für Benutzer bei der ersten Erfahrung mit Ihrem Programm reduzieren.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="design-a-lightweight-setup"></a>Entwerfen eines einfachen Setups

Willkommen, Weiter, Weiter, Weiter, Weiter, Weiter, Installieren, Fertig stellen, Herzlichen Glückwunsch! Klingt diese Einrichtungserfahrung vertraut? In der Vergangenheit haben Setupprogramme diese Art von ineffizientem Design übernommen: eine lange Abfolge von Bildschirmen, die Benutzer zu einer gedankenlosen Folge von Klicks einlädt, um sie zu durchkommt.

Wenn Benutzer die Einrichtung Ihres Programms mit Wörtern wie schnell und einfach beschreiben, werden sie die Erfahrung mit Sicherheit loben. Sie würden ihr Programm vielmehr verwenden, als es zu einrichten.

**Überprüfen Sie Ihren Setupentwurf auf nicht unerbittliche Fragen, Optionen, Seiten und Pfade, und machen Sie sich keine Sorgen, um sie zu beseitigen.** Führen Sie Benutzerforschung durch, um herauszufinden, welche Optionen Benutzer wirklich benötigen, und stellen Sie sicher, dass sie nicht bedenkenlos über alle Seiten auf die Schaltfläche Weiter klicken. Verzögerung aller Optionen oder Fragen, die im Kontext des ausgeführten Programms besser behandelt werden.

Viele Setupprogramme bieten Standardseiten nicht, weil sie notwendig oder hilfreich sind, sondern weil sie Standard sind. Beispielsweise fügen Willkommensseiten, Zusammenfassungsseiten und Herzlichen Glückwunschseiten häufig nur Klicks hinzu. Stattdessen sollte das Setupprogramm Seiten nur dann hinzufügen, wenn sie zum Abschließen der Setupaufgabe erforderlich sind. Richtlinien zu Typen von Setupseiten und deren Auswertung finden Sie weiter unten in diesem Artikel unter [Seitentypen.](#page-types)

![Screenshot der ersten Seite des Proclarity-Setups ](images/exper-setup-image2.png)

In diesem Beispiel entfernt das Setupprogramm die herkömmliche Willkommensseite und geht direkt ins Geschäft.

Es kann zwar erforderlich sein, verschiedene Verzweigungen des Setups (eine schnelle, typische Erfahrung und eine besser steuerbare, benutzerdefinierte Erfahrung) zu bieten, aber stellen Sie sicher, dass Sie über genügend benutzerdefinierte Optionen verfügen, um die zusätzliche Komplexität zu gewährleisten. Fügen Sie nur Branches hinzu, wenn Dies der Vor- und Nachzinge ist. Einige unwichtige Optionen in einem benutzerdefinierten Branch deuten darauf hin, dass der Setupentwurf neu organisiert werden muss.

Ein weiterer Grund für die Optimierung des Setups ist, dass unerfahrene Benutzer manchmal die Optionen überanalysten und fürchteten, dass eine falsche Auswahl nicht rückgängig gemacht oder destruktiv sein könnte. Wenn Benutzer gezwungen werden, Entscheidungen über Dinge zu treffen, die sie nicht verstehen oder für die sie sich nicht sorgen, kann dies dazu sorgen, dass sie sich verärgert, inkompetent und sogar frustriert fühlen. Kein guter erster Eindruck. Es ist besser, einfach schnell los zu sein, sich beim Erkunden der Features in Ihrem Programm zu fühlen und bessere Entscheidungen über Featureoptionen zu treffen. Weitere Richtlinien finden Sie unter [Optimieren der Einrichtung](#streamlining-setup) weiter unten in diesem Artikel.

Versuchen Sie, Ihre Einrichtungserfahrung so einfach wie [möglich zu gestalten, aber nicht einfacher.](/previous-versions//dn742474(v=vs.85)) Programme für stark technische Benutzer benötigen möglicherweise ein komplexes Setup. Beispielsweise hat das Microsoft SQL Server festgestellt, dass Datenbankadministratoren die Kontrolle über viele Setupoptionen behalten möchten, z. B. Dateistandorte. Darüber hinaus ist SQL Server eine große Geschäftsanwendung mit einer Reihe von Komponenten, die sich in Zweck und Funktionalität stark unterscheiden. Obwohl wir die Dinge einfach halten möchten, muss das Setup die Komplexität des Produkts und die Erwartungen und Anforderungen der Benutzer widerspiegeln.

Dennoch sollten solche komplexen Setupprogramme die Ausnahme sein, nicht die Regel. Die Windows-Programme sollten versuchen, den Setupprozess mit einem einfachen, einzigen Schritt zu starten.

### <a name="setup-phases"></a>Setupphasen

Mit gut entworfenen Setupprogrammen können Benutzer während der zeitaufwändigen Aufgabe des Herunterladens und Kopierens von Dateien andere Aktivitäten ausführen. Um unbeaufsichtigt ausgeführt zu werden, sind Setupprogramme auf vier separate Phasen ausgelegt:

-   **Die Entscheidungsphase.** Benutzer geben an, wie das Programm installiert und konfiguriert werden soll.
-   **Die Downloadphase.** Für Programme, die aus dem Internet heruntergeladen werden. Wenn das Programm über mehrere Anwendungen oder Versionen verfügt, geben Benutzer an, was während der Entscheidungsphase heruntergeladen werden soll.
-   **Die Installationsphase.** Das Setupprogramm kopiert die Dateien und macht die entsprechenden Konfigurationsänderungen.
-   **Die Abschlussphase.** Alle verbleibenden Details, Schritte oder Probleme werden behandelt.

Da die Installationsphase sehr lange dauern kann, sollte diese Phase so konzipiert sein, dass sie ohne Benutzereinständigung bis zum Abschluss ausgeführt wird. Dies bedeutet, dass alle Fragen während der Entscheidungsphase gestellt werden sollten, und alle probleme, die auftreten, in die Warteschlange gestellt und in der Abschlussphase behandelt werden sollten. **Wenn die Installationsphase länger als eine Minute dauert, gehen Sie davon aus, dass Benutzer während der Download- und Installationsphase etwas anderes tun.**

**Falsch:**

![Screenshot der automatischen Berichterstellung für die Installation von € Dialog (dialog) ](images/exper-setup-image3.png)

In diesem Beispiel unterbricht das Setupprogramm den Fortschritt, um eine Frage zu stellen, die während der Entscheidungsphase gestellt werden sollte.

### <a name="present-helpful-progress"></a>Hilfreichen Fortschritt präsentieren

Wenn Benutzer die Installationsphase der Einrichtungserfahrung sehr lange warten, vielleicht eine Statusleiste bis zum offensichtlichen Abschluss beobachten, nur um das Zurücksetzen der Statusleiste zu beobachten und von vorn zu beginnen, ist dies ein echtes Gefühl für Eindrückung. Der gemeldete Fortschritt war irreführend und letztlich bedeutungslos.

Eine Variante dieses qualvollen Szenarios ist die Installation der "Wächterverwaltung": Benutzer sehen, dass der Fortschritt erreicht ist, z. B. 99 Prozent abgeschlossen, aber sie müssen unverhältnismäßig lange warten, bevor sie schließlich zu 100 Prozent abgeschlossen werden. Im Hinblick auf das, was für den Benutzer am wichtigsten ist, eine implizite Zusage über die Wartezeit, ist der Anspruch von 99 Prozent abgeschlossen also ungeniert.

Während der Download- und Installationsphasen haben Benutzer in der Regel zwei Dinge, die sie wissen möchten: sollten sie warten oder etwas anderes tun, und wird das Setup in Kürze durchgeführt. Während im Setupprozess genügend Variablen vorhanden sind, um zu verhindern, dass Sie perfekt genaue Statusinformationen bereitstellen, muss das Fortschrittsfeedback genau genug sein, um diese beiden Fragen zu beantworten und entsprechende Erwartungen festzulegen. Zusätzlich zu einer Statusanzeige können Sie eine kurze Anweisung zur Gesamtzeit einfügen, die für den Prozess erwartet wird.

![Screenshot des Dialogfelds mit dem Setupfortschritt ](images/exper-setup-image4.png)

In diesem Beispiel enthält die Statusseite eine kurze allgemeine Aussage darüber, wie lange die Installation dauern könnte.

Gute Setupprogramme verwenden effektiv Statusanzeigen, um Benutzern hilfreiche Informationen zum Fortschritt des Setupprogramms bereitzustellen. Weitere Richtlinien finden Sie unter [Statusleisten.](progress-bars.md)

### <a name="design-for-all-setup-scenarios"></a>Entwurf für alle Setupszenarien

Moderne Setupprogramme müssen für eine Vielzahl von Installationsszenarien konzipiert sein:

-   Der Benutzer des Programms installiert es von einem Datenträger oder einer Netzwerkdateifreigabe.
-   Der Benutzer des Programms lädt es aus dem Web herunter.
-   Ein Originalgerätehersteller (Original Equipment Manufacturer, OEM) schließt das Programm auf dem Computer am Werk ein.
-   Ein IT-Mitarbeiter installiert das Programm auf vielen Computern in einer Organisation.
-   Eine andere Person als der Benutzer installiert das Programm (z. B. ein übergeordnetes Element im Namen eines untergeordneten Elements oder ein Mitarbeiter, der denselben Computer wie ein anderer Mitarbeiter verwendet).

In diesen Szenarien sollten Sie nicht davon ausgehen, dass Benutzer das Programm immer für sich selbst installieren (was Optionen zu persönlichen Einstellungen unpassend macht), den Prozess genau überwachen (was das unbeaufsichtigte Setup wichtig macht) oder sogar eine grafische Benutzeroberfläche für die Aufgabe wünschen.

### <a name="dont-forget-the-uninstall-experience"></a>Vergessen Sie nicht die Deinstallationserfahrung.

Um den Lebenszyklus der Softwareeinrichtung abzuschließen, müssen Benutzer Software entfernen können, die sie nicht mehr benötigen oder nicht mehr benötigen. Dies ist besonders wichtig, wenn das Programm nicht selbst installiert wurde (z. B. wenn es vorab auf dem Computer geladen wurde).

### <a name="handle-technical-support-strategically"></a>Strategisches Behandeln des technischen Supports

Die Installation des Programms ist die einzige Aufgabe, die alle Benutzer erfolgreich abschließen müssen. Wenn Benutzer Ihr Programm nicht installieren können, müssen Sie ihnen entweder kostspieligen technischen Support bieten, oder sie sind nicht mehr Ihre Benutzer.

Entwerfen Sie Ihr Setupprogramm, um Ihrem technischen Supportteam die Features und Informationen bereitzustellen, die sie benötigen, um Benutzer bei der erfolgreichen Installation zu unterstützen. Diese Details sollten normalerweise nicht für Benutzer verfügbar gemacht werden, aber sie sollten bei Bedarf leicht zugänglich sein.

**Falsch:**

![Screenshot der Bezeichnung mit dem Namen des Com-Servers ](images/exper-setup-image5.png)

In diesem Beispiel zeigt die Statusleiste Nur für den technischen Support aussagekräftige Details an.

Halten Sie die normale Benutzererfahrung einfach– überladen Sie sie nicht mit Informationen, die nur für den technischen Support von Nutzen sind. Notieren Sie stattdessen Unterstützungsinformationen in einer Setupprotokolldatei. Und noch wichtiger ist, dass Benutzer die Notwendigkeit von technischem Support mit eindeutigen, präzisen Fehlermeldungen vermeiden können, die Probleme gut erklären und praktische Lösungen bereitstellen. Stellen Sie bei Bedarf Links zu Hilfeartikeln bereit. Erwägen Sie die Bereitstellung einer Reparaturoption für Ihr Setupprogramm, um fehlende oder beschädigte Dateien oder Einstellungen zu reparieren.

**Wenn Sie nur drei Dinge tun...**

1.  1. Gestalten Sie die Einrichtung so einfach und einfach wie möglich. Denken Sie daran, dass die Benutzer das Setup nicht gerne nutzen. Sehen Sie sich jede Frage, Option, Seite und jeden Pfad sorgfältig an, und kürzen Sie alles, was für den Abschluss des Setups nicht erforderlich ist.
2.  2. Entwurf für alle Setupszenarien, einschließlich unbeaufsichtigter Installationen, Skriptinstallationen und Deinstallation. Stellen Sie für effiziente unbeaufsichtigte Installationen sicher, dass die Setupphasen sauber voneinander getrennt sind.
3.  3. Entwerfen Sie Ihr Setupprogramm so, dass Benutzer Setupprobleme eigenständig beheben können, aber auch die für den technischen Support erforderlichen Informationen nur für den Fall protokollieren können. Beachten Sie, dass das Setup die einzige Aufgabe ist, die alle Benutzer erfolgreich abschließen müssen.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Wenden Sie die Standardrichtlinien des Assistenten für assistentenbasierte Setupprogramme an.** Verwenden Sie diese Richtlinien, um einen guten Seitenentwurf, eine effektive Navigation, gute Steuerelementbezeichnungen, die Verwendung von Hauptanweisungen und die Verwendung von Hilfe zu bestimmen.
-   **Erlauben Sie Benutzern, das Setupprogramm dort neu zu starten, wo sie aufgehört haben, wenn es viel Benutzereingaben erfordert oder lange dauert.** Wenn Benutzer das Programm nach dem Schließen vor Abschluss neu starten, stellen Sie vorherige Benutzereingaben wieder her, und starten Sie es an der Stelle neu, an der das Setup beendet wurde.
-   **Setupfenster nicht maximiert anzeigen.** Beim Anzeigen eines maximierten Setupfensters wird davon ausgegangen, dass Benutzer dem Setup ihre ungeteilte Aufmerksamkeit gewähren, was unwahrscheinlich ist. Wählen Sie stattdessen eine Größe aus, die für den Inhalt geeignet ist, um eine einfache Darstellung zu erhalten.

### <a name="windows-integration"></a>Windows Integration

-   **Nennen Sie die Setupdatei "Setup.exe".** "Install.exe" ist eine akzeptable Alternative. Dadurch können Windows (und Benutzer) die Datei als Setupprogramm erkennen.
    -   **Ausnahme:** Bei Programmen, die aus dem Internet heruntergeladen werden, können Benutzer ihren Ordner Downloads verwalten und organisieren, indem Sie den Namen des Programms in den Namen der Setupdatei einschließen. Beispiel: SetupVisualStudioExpress2008.exe.
-   **Kopieren Sie Programmdateien an die richtigen Dateisystemspeicherorte.** Auf diese Weise können Benutzer und Windows die Dateien besser finden und organisieren. Weitere Informationen finden Sie in den [Windows Namespace-Nutzungsrichtlinien](../fileio/naming-a-file.md#namespaces)für Dateisystem.

### <a name="user-account-control"></a>Benutzerkontensteuerung

-   **Signieren Sie die ausführbare Setupdatei digital.** Signierte ausführbare Dateien haben viele Vorteile, einschließlich der Verwendung einer spezifischeren Benutzeroberfläche für die Benutzerkontensteuerung. Informationen zum Signieren von Dateien finden Sie unter [Einführung in die Codesignierung](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))von .
-   **Wenn für ein Setup erhöhte Rechte erforderlich sind, erhöhen Sie die Rechte so spät wie möglich.** Zeigen Sie die Benutzeroberfläche für erhöhte Rechte erst an, nachdem der Benutzer sich für eine Option entschieden hat, die eine Erhöhung erfordert. In der Regel wird die Benutzeroberfläche für erhöhte Rechte während der Installationsphase und nicht in der Entscheidungsphase angezeigt. Wenn ein Setup jedoch immer erhöhte Rechte erfordert, erhöhen Sie die Rechte an seinem Einstiegspunkt.
-   **Für die Deinstallation ist immer erhöhte Rechte erforderlich.** Auf diese Weise wird verhindert, dass Schadsoftware kritische Software deinstalliert, ohne dass Benutzer dies wissen.
-   **Bleiben Sie nach der Erhöhung erhöht, bis erhöhte Berechtigungen nicht mehr erforderlich sind.** Benutzer sollten nicht mehrmals erhöht werden müssen, um eine Programminstallation abzuschließen.
-   **Wenn für die Installation spezielle Berechtigungen erforderlich sind, überprüfen Sie die Anmeldeinformationen des Benutzers, und melden Sie probleme auf der ersten oder zweiten Seite.** Lassen Sie nicht zu, dass Benutzer viel Arbeit ausführen, nur um zu ermitteln, dass sie nicht über die richtigen Anmeldeinformationen verfügen, um die Installation abzuschließen.
-   **Fordern Sie die geringstmöglichen Berechtigungen an.** Administratoren sind z. B. nicht in der Lage, Software zu installieren, die Anmeldeinformationen des Domänenadministrators erfordert.

Weitere Richtlinien finden Sie unter [Benutzerkontensteuerung.](winenv-uac.md)

### <a name="restarting-windows"></a>Neustarten Windows

-   **Vermeiden Sie es, Windows neu zu starten.** Die meisten Programme sollten ohne Neustart von Windows installiert werden. Programminstallationen oder -updates erfordern einen Systemneustart, weil einige der beteiligten Dateien derzeit von einem ausgeführten Programm verwendet werden. In diesem Fall besteht eine bessere Alternative darin, Benutzer auf die Situation aufmerksam zu machen, Benutzern das Schließen dieser Programme zu ermöglichen und die Aktion erneut zu wiederholen. Weitere Informationen zum Vermeiden von Neustarts finden Sie unter [Neustart-Manager.](../rstmgr/restart-manager-portal.md)
-   **Wenn Das Setup Windows neu starten muss:**
    -   **Verwenden Sie einen einzelnen Neustart.** Verzögern Sie den Neustart, der für alle erforderlichen Komponenten erforderlich ist, bis das Programm und seine Updates vollständig installiert sind.
    -   **Lassen Sie Benutzer bestimmen, wann dies geschieht.** Starten Sie Windows nicht automatisch neu, da Benutzer möglicherweise ihre Arbeit verlieren. Stellen Sie sicher, dass benutzern klar ist, dass sie eine Auswahl haben.

        **Falsch:**

        ![Screenshot des Dialogfelds mit Neustart und Abbruch ](images/exper-setup-image6.png)

        In diesem Beispiel haben Benutzer anscheinend keine Wahl darüber, wann Windows neu gestartet werden soll.

    -   **Wenn sich der Benutzer dafür entscheidet, Windows nicht sofort neu zu starten, geben Sie ein endgültiges Feedback als Erfolg und nicht als Fehler an.** Obwohl die Installation technisch gesehen erst nach dem Neustart abgeschlossen ist, war sie aus Sicht des Benutzers erfolgreich.

### <a name="streamlining-setup"></a>Streamlining-Setup

-   **Starten Sie den Installationsvorgang nach Möglichkeit mit einem einzigen Schritt.** Anstatt z. B. eine separate Seite im Setup für die Lizenzbedingungen hinzuzufügen, können Sie stattdessen einen Link zu ihnen bereitstellen. Wenn Sie einen Link zu den Bedingungen erstellen:
    -   Geben Sie die Commitschaltfläche als "Zustimmen und installieren" ein, um eine explizite Zustimmung zum Akzeptieren der Lizenzbedingungen zu erzwingen.
    -   Stellen Sie sicher, dass die Lizenzvereinbarungsverknüpfung nicht unterbrochen werden kann, indem Sie anstelle einer Webseite eine Verknüpfung mit einer lokalen Datei für das Setup herstellen.
    -   Bieten Sie die Möglichkeit, den Lizenzvertrag aus dem Anzeigefenster auszudrucken.
-   **Vermeiden Sie unnötige Optionen und Fragen.**
    -   Verschieben Sie Optionen, die für die erste Verwendung des Programms oder Features besser geeignet sind.

        ![Screenshot des Dialogfelds mit benutzerdefinierter Einstellungsoption ](images/exper-setup-image7.png)

        In diesem Beispiel Windows Media Player benutzerspezifische Datenschutzoptionen bei der ersten Verwendung des Programms.

    -   Stellen Sie Benutzern keine Fragen zum Systemstatus. Erkennen Sie diese Informationen stattdessen automatisch, und bitten Sie die Benutzer, dies nur zu überprüfen, wenn ein Grund für eine Änderung vor liegt.
    -   Stellen Sie keine Fragen zu unwichtigen Details. Bei typischen Windows ist es beispielsweise sicher, davon auszugehen, dass Sie Programmdateien in den Ordner Programme kopieren sollten.

        **Falsch:**

        ![Screenshot des Dialogfelds mit Installationsspeicherort ](images/exper-setup-image8.png)

        In diesem Beispiel sollte das Setup optimiert werden, indem die Anforderung von Dateispeicherorteingaben beseitigt wird. Angesichts der Größe des Programms ist es den meisten Benutzern egal, und klicken Sie einfach auf Weiter.

    -   Fragen Sie die Berechtigung nicht, das zu tun, was Sie ohnehin nicht tun sollten. Beispielsweise sollten die meisten Programme keine Option enthalten, um das Programmsymbol auf dem Desktop zu installieren.
    -   Bestätigen Sie den Setupabbruch nicht. Wenn Benutzer während des Setups auf Abbrechen klicken, gehen Sie davon aus, dass der Abbruch beabsichtigt war, und schließen Sie das Programm ohne Bestätigung. Wenn dies zu einem erheblichen Zeit- oder Aufwandsverlust kommt, können Benutzer Ihr Setupprogramm neu starten und dort auf dem Weg zur Verfügung stellen.

-   **Optimieren sie für die unbeaufsichtigte Installation.**
    -   Stellen Sie alle Optionen und Fragen während der Entscheidungsphase vor.
    -   Verzögern Sie für die Download- und Installationsphasen das Erfordern von Benutzereingaben für alle aufgetretenen Probleme bis zum Ende der Phase. Dadurch können Benutzer die Installation unbeaufsichtigt lassen, bis sie ihrer Einfachheit halber zurückkehren.
-   **Vermeiden Sie unnötige Seiten.** Wenn die meisten Benutzer immer einfach auf einer Seite auf Weiter klicken, sollten Sie die Seite wieder los werden. Richtlinien zum Entfernen bestimmter Seitentypen finden Sie unter [Seitentypen.](#page-types)
-   **Vermeiden Sie unnötigen Text.**
    -   Entfernen Sie redundanten Text aus Anweisungen und Bezeichnungen.
    -   Erläutern Sie keine grundlegenden Windows Verwendungskonzepte, z. B.:
        -   Interagieren mit Steuerelementen (Beispiele: Klicken Sie zum Starten auf Weiter; Klicken Sie auf Optionen, um weitere Optionen zu erhalten. Klicken Sie auf Hilfe, um weitere Informationen zu erhalten.
        -   Funktionsweise von Assistenten (Beispiel: Wenn Sie Einstellungen überprüfen oder ändern möchten, klicken Sie auf Zurück).
        -   Funktionsweise des Setups (Beispiel: Dieses Programm kopiert die Programmdateien auf Ihre Festplatte...).
-   **Vermeiden Sie unnötigen Aufwand.**
    -   Geben Sie gute Standardwerte an:
        -   Wählen Sie im Allgemeinen die sicherste und private Antwort als Standard aus.
        -   Wenn Sicherheit und Datenschutz keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequemste Antwort aus.

            ![Screenshot des Dialogfelds mit angezeigten Namen und Unternehmen ](images/exper-setup-image9.png)

            In diesem Beispiel werden der standardmäßig bereitgestellte Benutzername und die Organisation aus der Registrierung ermittelt.

        -   Wenn eine Option dringend empfohlen wird, sollten Sie sie standardmäßig auswählen oder ihrer Bezeichnung "(empfohlen)" hinzufügen.

    -   Seiten werden automatisch aktualisiert, wenn eine Seite keine Eingaben enthält und die Aufgabe erfolgreich abgeschlossen wurde, z. B. mit Download-, Installations-, Fortschritts- und Aktualisierungsseiten. Sobald der Schritt durchgeführt ist, bleiben Sie auf diesen Seiten, um Probleme zu zeigen.
    -   Wenn dies praktisch ist, starten Sie das Programm automatisch, wenn das Setup abgeschlossen ist, anstatt die Seite Herzlichen Glückwunsch oder Abschluss anzuzeigen. Wenn das Setup interaktiv ausgeführt wird, gehen Sie davon aus, dass der Benutzer Ihr Programm installiert, um es sofort ausführen zu können. Daher ist die Ausführung des Programms das beste Feedback, um zu zeigen, dass das Setup abgeschlossen ist. Die automatische Ausführung des Programms ist nicht praktikabel, wenn das Setup mehr als ein Programm installiert (z. B. eine Suite, die aus vielen Programmen besteht), wenn das Setup nicht interaktiv ausgeführt wird oder der Installationsvorgang nach dem Setup nicht abgeschlossen ist.

### <a name="page-types"></a>Seitentypen

**Willkommens- und Erste Schritte Seiten**

-   **Vermeiden Sie Willkommensseiten.** Es ist zwar toll, sich willkommen zu fühlen, aber Benutzer klicken in der Regel einfach auf Weiter, ohne zu lesen. Und da Benutzer diese Seiten in der Regel überspringen, ohne zu lesen, ist der Text nicht mehr als das offensichtliche, entwurfsweise.

    **Falsch:**

    ![Screenshot des Begrüßungsbildschirms mit "Weiter" und "Abbrechen" ](images/exper-setup-image10.png)

    In diesem Beispiel ist für den Benutzer nichts anderes zu tun, als auf Weiter zu klicken.

-   **Verwenden Sie Erste Schritte Seite nur, wenn Sie Benutzer über die Voraussetzungen für die Installation informieren müssen.** Zu diesen Voraussetzungen gehören die Installation der erforderlichen Software oder Hardware, das Ausführen der erforderlichen Änderungen und Updates für die Systemkonfiguration, das Ausführen einer Systemsicherung zum Schutz vor Datenverlust oder das Abrufen erforderlicher Informationen, die der Benutzer wahrscheinlich noch nicht hat.
-   **Geben Sie nach Möglichkeit die Möglichkeit, die Voraussetzungen direkt über das Setupprogramm durchzuführen.** Benutzer sollten die Schritte nur manuell ausführen müssen, wenn es keine Alternative gibt.
-   Wenn keine Willkommensseite oder Erste Schritte verwendet wird, geben Sie den Programmnamen und die Beschreibung auf der ersten Seite des **Setupprogramms an.** Sie können die Begrüßungssprache als Einführungstext verwenden, solange der Zweck der Seite klar ist.

**Seiten mit Lizenzbedingungen**

-   **Schreiben Sie die Lizenzbedingungen mit klarem, präzisem Text.** Verwenden Sie Nur-Sprache. Vermeiden Sie "legalese".
-   **Stellen Sie mit einem Format vor, das leicht zu lesen und zu scannen ist.** Verwenden Sie keine langen Gängen mit Großbuchstaben.

    **Falsch:**

    ![Screenshot der Lizenzbedingungen in Großbuchstaben ](images/exper-setup-image11.png)

    In diesem Beispiel erschweren groß geschriebener Text und großer Schriftgrad das Lesen der Begriffe, sodass Benutzer mehr als nötig scrollen müssen.

-   **Fordern Sie die explizite Zustimmung zum Akzeptieren der Lizenzbedingungen an.** Die Zustimmung zur Lizenz sollte nicht standardmäßig ausgewählt werden. Wenn Optionsfelder verwendet werden, um die Zustimmung anzugeben, lassen Sie die Optionen standardmäßig deaktiviert, und fordern Sie die Benutzer auf, die Bedingungen zu akzeptieren, bevor Sie die Schaltfläche Weiter aktivieren.

    ![Screenshot des Dialogfelds mit abgeblendeter Schaltfläche "Weiter" ](images/exper-setup-image12.png)

    In diesem Beispiel ist die Schaltfläche Weiter deaktiviert, bis Benutzer die Lizenzbedingungen explizit akzeptiert haben.

-   **Benutzer müssen nicht bis zum Ende des Lizenzbedingungentexts scrollen, bevor die Schaltfläche Weiter aktiviert ist.** Dies stellt eine unnötige Belastung für Benutzer dar, um zu verstehen, warum die Schaltfläche Weiter deaktiviert ist.
-   **Geben Sie einen Druckbefehl an,** entweder mit einer Befehlsschaltfläche oder einem Kontextmenü. Präsentieren Sie die Begriffe in einem Format, das für den Druck optimiert ist.

**Produktregistrierungsseiten**

-   **Benutzer müssen sich nur registrieren, wenn sie das Programm verwenden müssen.** Erläutern Sie eindeutig, warum Benutzer sich registrieren müssen.
-   **Geben Sie eine optionale Registrierung nur an, wenn es einen eindeutigen Benutzervorteil gibt,** z. B. um Benutzer über Produktupdates zu benachrichtigen. Lassen Sie diese Option standardmäßig deaktiviert.
-   **Erlauben Sie Benutzern, sich später zu registrieren.** Geben Sie maximal drei Erinnerungen an, und ermöglichen Sie Es Benutzern, die Erinnerungen mit einem einzigen Klick zu verziehen.

**Bereichsseiten (typisch, benutzerdefiniert oder minimal)**

-   **Vermeiden Sie diese Seite lieber.** Angenommen, die meisten Benutzer wünschen sich die typische Einrichtungserfahrung (und entwerfen sie so, dass sie für die meisten Benutzer gut funktioniert).
-   Wenn Sie eine Bereichsseite hinzufügen müssen:
    -   **Erläutern Sie die Unterschiede zwischen den Optionen in Bezug auf Funktionalität und Speicherplatz.** Benutzer verlassen sich auf die Übersichtlichkeit der Informationen auf der Bereichsseite, um sicherzustellen, dass sie die richtige Wahl treffen.
    -   **Stellen Sie sicher, dass die benutzerdefinierten Optionen nur für einen kleinen Prozentsatz von Benutzern erforderlich sind, während die meisten Benutzer sie problemlos ignorieren können.** Falls nicht, sollten die Optionen im typischen Setuppfad enthalten sein.
    -   **Wenn Benutzer benutzerdefinierte Optionen auswählen, haben Sie standardmäßig die typischen Installationsoptionen ausgewählt.** Benutzer betrachten die typische Installation als Baseline und möchten sie anpassen, indem sie Optionen zu dieser Baseline hinzufügen oder daraus entfernen.
-   Wenn Sie eine benutzerdefinierte Installationsoption verwenden müssen, sollten Sie die relative Größen- und Platzierungsoption für Schaltflächen verwenden, um die meisten Benutzer zur **typischen Installation zu führen.**

    ![Screenshot des Dialogfelds mit großer Installationsschaltfläche ](images/exper-setup-image13.png)

    In diesem Beispiel verstärkt der Seitenentwurf visuell die Tatsache, dass sich die meisten Benutzer für die typische Installation entscheiden sollten.

**Eingabeseiten**

-   **Reduzieren Sie die Anzahl der Setupoptionen, indem Sie standardmäßig das Richtige tun.** Möglichkeiten zum Beseitigen von Optionen finden Sie unter [Optimieren des Setups.](#streamlining-setup)
-   **Geben Sie nach Möglichkeit akzeptable Standardwerte an.** Wählen Sie Standardwerte aus, die sicher und privat sind und für die meisten Benutzer ohne Änderungen akzeptabel sind.
-   **Wenn Ihr Programm keine ungewöhnlichen Anforderungen hat, sollten Sie eine einzelne Seite mit Fragen und Optionen verwenden.** Wenn ihr Programm jedoch mehrere Seiten mit Fragen und Optionen erfordert, zeigen Sie diese im Hauptflow der Assistentenseite an. Versuchen Sie nicht, die Anzahl der Seiten technisch zu reduzieren, indem Sie Optionen in Dialogfeldern oder registerkarten verwenden.
-   ![Screenshot des Setupdialogfelds mit vier Optionen ](images/exper-setup-image14.png)
-   In diesem Beispiel sind Optionen auf eine einzelne Seite beschränkt.
-   **Überprüfen Sie die Eingabe so schnell wie möglich:**
    -   Unzulässige Zeichen beim Eintrag.
    -   Verwenden Sie [Sprechblasen,](ctrl-balloons.md) um Probleme mit ungültigen Textfeldern zu melden.
    -   Überprüfen Sie verwandte Felder auf einer Seite, wenn Benutzer auf Weiter klicken.
    -   Überprüfen Sie verwandte Felder über Eingabeseiten hinweg, sobald Probleme erkannt werden können.
-   **Geben Sie allen bearbeitbaren Dateipfaden die Schaltfläche Durchsuchen.** Benutzern das Angeben von Netzwerkpfaden gestatten.
-   **Bezeichnen Sie für die letzte Eingabeseite die Commitschaltfläche Installieren, nicht Weiter.** Benutzer sollten sich nicht über den Start der Installation wundern. Stellen Sie vor dem Commitpunkt sicher, dass Benutzer alle Einstellungen leicht ändern können.

**Installationsseiten starten**

-   **Entfernen Sie diese Seite, wenn sie keinen anderen Zweck hat, als die vorherigen Optionen zusammenzufassen und mit der Installation zu beginnen.** Wenn die Eingabeseiten klar und nur wenige sind, sollten sie nicht zusammengefasst werden müssen. Stattdessen sollte die letzte Eingabeseite über die Schaltfläche Installieren verfügen, die direkt zur Statusseite führt.
-   **Stellen Sie für komplexe Installationen, die für IT-Experten vorgesehen sind, eine Seite Installation mit einer umfassenden Liste der Änderungen bereit, die das Setupprogramm ausführt.** Viele IT-Experten verfügen über eine strenge Steuerung des Change Managements, daher müssen sie die Auswirkungen der Installation des Programms im Detail kennen.

**Statusseiten**

-   **Stellen Sie immer eine Statusseite bereit,** auch wenn das Programm schnell installiert wird. Geben Sie eine separate Statusseite für [die Downloadphase](#setup-phases) an, sofern vorhanden. Deaktivieren Sie die Schaltflächen Zurück (oder Zurück) und Weiter, während das Setup ausgeführt wird, lassen Sie die Schaltfläche Abbrechen jedoch aktiviert und reaktionsfähig.

    ![Screenshot des Dialogfelds mit Statusanzeige ](images/exper-setup-image15.png)

    Eine typische Statusseite.

-   **Verwenden Sie eine einzelne, bestimmende Statusanzeige.** Befolgen Sie die Richtlinien für die [statusbestimmte Statusanzeige,](progress-bars.md)einschließlich:
    -   Geben Sie die Vervollständigung eindeutig an. Lassen Sie eine Statusanzeige nur dann auf 100 Prozent zu, wenn der Vorgang abgeschlossen wurde.
    -   Starten Sie den Fortschritt nicht neu. Eine Statusanzeige verliert ihren Wert, wenn sie neu gestartet wird (möglicherweise weil ein Schritt im Vorgang abgeschlossen wird), da Benutzer nicht wissen können, wann der Vorgang abgeschlossen wird. Lassen Sie stattdessen alle Schritte im Vorgang einen Teil des Fortschritts teilen, und lassen Sie die Statusanzeige einmal abgeschlossen werden.
-   **Geben Sie eine kurze Beschreibung des aktuellen Schritts oberhalb der Statusanzeige an.** Für schnelle Installationen ist dieser Text nicht erforderlich. die Statusanzeige allein ist ausreichend. Bei Installationen, die eine Minute oder länger dauern, kann Text für Benutzer hilfreich sein, die am Setup teilnehmen.
    -   **Verwenden Sie Satzfragmente, die in der Regel mit einem Verb beginnen und mit auslassungszeichen enden.** Beispiele: Kopieren von Dateien..., Installieren der erforderlichen Komponenten...
    -   **Platzieren Sie Text über der Leiste, nicht darunter.**

        **Falsch:**

        ![Screenshot des Texts, der unter der Statusleiste angezeigt wird ](images/exper-setup-image16.png)

        In diesem Beispiel sollte der erläuternde Text über der Statusleiste angezeigt werden.

    -   **Vermeiden Sie es, die Statusseite mit unnötigen Details zu überladen.** Diese Seite ist nicht für [den technischen Support](#handle-technical-support-strategically)vorgesehen. Daher ist es nicht erforderlich, registrierende GUIDs oder kopierte Dateien anzuzeigen.

        **Falsch:**

        ![Screenshot der GUID, die über der Statusleiste angezeigt wird ](images/exper-setup-image17.png)

        In diesem Beispiel sind technische Details wie GUIDs für Benutzer bedeutungslos.

**Fehlerseiten**

-   **Wenn das Setup mit einem erheblichen Problem fehlschlägt, zeigen Sie eine Fehlerseite an, auf der die Probleme zusammen mit den praktischen Schritten zur Behebung erläutert werden.** Zeigen Sie die Seite mit einem Fehlersymbol an. Verwenden Sie zu diesem Zweck kein Dialogfeld.

    ![Screenshot der Fehlerseite und des Symbols ](images/exper-setup-image18.png)

    In diesem Beispiel wird der Setupfehler auf einer Fehlerseite zusammen mit einigen Schritten zum Beheben des Problems erläutert.

-   **Wenn das Setup mit einem geringfügigen wiederherstellbaren Problem abgeschlossen wird, stellen Sie das Problem als zusätzliche Aufgabe anstelle eines Fehlers dar.** Verwenden Sie positive, erfolgsorientierte, fördernde Sprache, nicht Begriffe wie Fehler, Fehler oder Problem. Verwenden Sie kein Fehlersymbol.

**Herzlichen Glückwunsch/Abschlussseiten**

-   **Wenn Sie ein einzelnes Programm interaktiv installieren, starten Sie das Programm (und schließen Sie den Setup-Assistenten), um eine erfolgreiche Einrichtung anzugeben, anstatt eine Abschlussseite anzuzeigen. Ausnahmen:**
    -   Setups, die über die Befehlszeile ausgeführt werden, sollten keine Programme starten.
    -   Automatische Updates (z.B. Windows Update) sollten keine Programme starten.
    -   Die Installation von Gruppenrichtlinien sollte keine Programme starten.
    -   Alle Setupszenarien für IT-Experten (da sie nicht für ihre eigene Verwendung installiert werden).
-   **Wenn das Setup Nachverfolgungsschritte nach der Installation enthält, listen Sie sie auf einer Seite Abschluss auf.** Stellen Sie jedoch sicher, dass Benutzer die Schritte wahrscheinlich ausführen, und dass die Schritte tatsächlich angegeben werden müssen (d. b. sie sind nicht offensichtlich), um eine Abschlussseite zu rechtfertigen.

    **Falsch:**

    ![Screenshot der Seite mit abgeschlossener Einrichtung ](images/exper-setup-image19.png)

    In diesem Beispiel wird auf einer unnötigen Seite Vervollständigung die offensichtliche angezeigt. Windows Das Update wird automatisch ausgeführt, sodass es keinen Grund für Benutzer gibt, es manuell auszuführen.

-   **Wenn Sie eine Suite von Programmen installieren, zeigen Sie eine Seite Vervollständigung an, um den Erfolg und ggf. erforderliche Folgeschritte anzuzeigen.**

    ![Screenshot der letzten Seite zum Einrichten der Office-Suite ](images/exper-setup-image20.png)

    In diesem Beispiel hat setup mehrere Programme installiert, sodass es nicht sinnvoll ist, ein bestimmtes Programm automatisch zu starten. Eine Vervollständigungsseite ist besser geeignet.

### <a name="leaving-users-in-control"></a>Benutzern die Kontrolle überlassen

-   **Sammeln Sie keine persönlichen Informationen, z. B. die für Marketingzwecke verwendeten.** Setup ist keine Möglichkeit, Ihre eigene Programmpläne zu pushen, andere Programmangebote zu verkaufen oder Marktforschung durchzuführen. Sie können die Vertrauensstellung mit Ihren Benutzern auf diese Weise beschädigen.
-   **Erzwingen Sie nicht, dass Benutzer die Installation optionaler Features deaktivieren.** Erlauben Sie es ihnen stattdessen, sich zu [entscheiden.](glossary.md) Benutzer sollten beispielsweise explizit ein Windows Desktop-Gadget installieren.
-   **Benutzern das Hinzufügen oder Entfernen optionaler Features mithilfe des Setupprogramms nach dem anfänglichen Setup gestatten.** Benutzer können diese Aufgabe mit dem Systemsteuerungselement **Deinstallieren oder Ändern eines Programms** ausführen.
-   **Erläutern Sie für Initiativen zur Verbesserung der Benutzerfreundlichkeit, welche Daten übertragen werden, wie sie verwendet werden und wie lange sie aufbewahrt werden.** Verwenden Sie zu diesem Zweck einen Link zu einem Hilfethema zur Datenschutzerklärung.
-   **Vermeiden Sie die Verwendung von Sound,** da viele Installationsszenarien unbeaufsichtigt sind und der Sound selbst bei installationslosen Installationen unnötig störend sein kann.

### <a name="security"></a>Sicherheit

-   **Stellen Sie für das internetbasierte Setup alle Sicherheitsupdates während der ersten Einrichtung automatisch bereit.** Benutzer sollten nicht als separaten Schritt aktualisieren müssen.
-   **Vermeiden Sie die Empfehlung, dass Benutzer Firewalls als Voraussetzung für die Installation Ihres Programms deaktivieren.**
-   Wenn eine Firewall deaktiviert werden muss, gehen Sie folgendermaßen vor:
    -   **Begrenzen Sie die Dauer dieser Bedingung auf so kurz wie möglich.**
    -   **Weisen Sie explizit darauf hin, wann Benutzer die Firewall wieder aktivieren können.**

### <a name="uninstall"></a>Deinstallieren

-   **Bei der Deinstallation sollten alle Ablaufverfolgungen eines Programms entfernt werden, einschließlich der folgenden:**
    -   Programmdateien, einschließlich des Setupprogramms.
    -   Startmenü Einträge.
    -   Desktopsymbole und Schnellstart Symbole (sofern vorhanden).
    -   Registrierungseinstellungen
    -   Dateizuordnungen.
-   **Bei der Deinstallation sollte Folgendes zurückbleiben:**
    -   Vom Benutzer erstellte Dateien, z. B. Dokumentdateien.
    -   Freigegebene Dynamic Link-Bibliotheken, die im Ordner System gespeichert sind.

### <a name="help-and-support"></a>Hilfe und Support

-   **Entwerfen Sie Ihr Setupprogramm, um keine Hilfe zu benötigen, indem Sie klare, selbsterklärende Fragen stellen.** Reservieren Sie Hilfe für erweiterte Fragen, die wirklich von weiteren Erläuterungen profitieren.
-   **Verwenden Sie keine Readme-Dateien.** Diese Dateien sind jetzt veraltet, und Benutzer lesen sie sowieso nicht. Stellen Sie stattdessen bei Bedarf Onlineinhalte zur Verfügung.
-   **Link zu entsprechenden Hilfethemen oder Problembehandlungsinhalten aus Setupfehlermeldungen.** Stellen Sie sicher, dass der Hilfeinhalt einen eindeutigen Pfad zum Beheben des Problems bietet. Weitere Informationen finden Sie unter [Fehlermeldungen.](mess-error.md)
-   **Erstellen Sie Protokolldateien, um informationen zu erfassen, die für den technischen Support nützlich sind.** Überladen Sie die Setupbenutzeroberfläche nicht mit Details zum technischen Support, die für die meisten Benutzer bedeutungslos sind. Verwenden Sie stattdessen Protokolldateien für diesen Zweck.

### <a name="text"></a>Text

-   **Seien Sie präzise.** Setup-Assistenten überdeexplainieren häufig Features und Optionen, indem sie Textblöcke verwenden, die schwer schnell überprüft werden können. **Ausnahmen:**
    -   Geben Sie alle Akronyme an. Setup ist häufig die erste Erfahrung von Benutzern mit Ihrem Programm. Gehen Sie daher nicht davon aus, dass sie Jargon wie Akronyme verstehen.
    -   Erläutern Sie unbekannte Terminologie und Konzepte, vorzugsweise vor Ort, aber verwenden Sie bei Bedarf Hilfethemen.
-   **Bevorzugen Sie einen benutzerfreundlichen, professionellen Ton. vermeiden Sie einen zu technischen Ton.**

**Falsch:**

Beschränken Sie die Installation auf Benutzerbasis.

**Richtig:**

Nur für mich installieren.

-   Verwenden Sie jetzt nicht in Befehlsschaltfläche-Bezeichnungen, da die Unmittelbarkeit des Befehls selbstverständlich ist.
    -   **Ausnahme:** Verwenden Sie bei Bedarf jetzt , um Befehle, die eine Aufgabe starten, von Befehlen zu unterscheiden, die eine Aufgabe sofort ausführen.

![Screenshot der Downloadschaltfläche ](images/exper-setup-image21.png)

In diesem Beispiel wird durch Klicken auf die Befehlsschaltfläche ein Fenster oder eine Seite geöffnet, auf der Benutzer herunterladen können.

![Screenshot der Schaltfläche "Jetzt herunterladen" ](images/exper-setup-image22.png)

Wenn Sie in diesem Beispiel auf die Befehlsschaltfläche klicken, wird der Download sofort ausgeführt.

Nur ein Befehl in einem Taskfluss sollte jetzt mit bezeichnet werden. Beispielsweise sollte auf den Befehl **Jetzt** herunterladen nie ein weiterer Befehl Jetzt herunterladen **folgen.**

-   Verwenden Sie Lizenzbedingungen, keine Lizenzbedingungen, Lizenzbedingungen, Endbenutzer-Lizenzbedingungen oder Lizenzbedingungen.

Weitere Richtlinien finden Sie unter [Stil und Ton.](text-style-tone.md)

## <a name="documentation"></a>Dokumentation

-   Als Verb besteht die Einrichtung aus zwei Wörtern. als Adjektiv oder Nomen ist setup ein Wort.
-   Das Setupprogramm ist groß und nicht mit Bindestrichen.
-   Verwenden Sie "Installieren", um auf das Hinzufügen von Hardware oder Software zu einem Computersystem zu verweisen.
-   Verwenden Sie install nicht als Nomen. Verwenden Sie stattdessen die -Installation.
-   Verwenden Sie neustart, nicht reboot. Geben Sie an, dass es sich um den Computer handelt, nicht um ein Programm, das neu gestartet wird.

 

 