---
title: Entwerfen von UX für Desktop Anwendungen
description: Eine großartige Desktop Anwendung ist leistungsstark und zugleich einfach. Durch eine sorgfältig ausgeglichene Funktionsauswahl und-Präsentation können Sie sowohl die Leistung als auch die Einfachheit erreichen.
ms.assetid: 0039a3ee-95bc-457f-a1a8-6a036ce22fd2
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 74433514f61b37ba1c9941c8134767be5458ebc8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351068"
---
# <a name="how-to-design-a-great-user-experience-for-desktop-applications"></a>Entwerfen einer hervorragend benutzerfreundlichen Benutzer Darstellung für Desktop Anwendungen

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Eine großartige Desktop Anwendung ist leistungsstark und zugleich einfach. Durch eine sorgfältig ausgeglichene Funktionsauswahl und-Präsentation können Sie sowohl die Leistung als auch die Einfachheit erreichen.

**Vollen**

![Screenshot des Dialog Felds "Rechtschreibung und Grammatik" ](images/powerful-simple-image1.png)

**Leistungsstark und einfach:**

![Screenshot der Liste möglicher Rechtschreib Überarbeitungen ](images/powerful-simple-image2.png)

Die ideale Windows-basierte Anwendung ist sowohl leistungsfähig als auch einfach. Natürlich möchten Sie, dass Ihre Anwendung leistungsfähig ist, und Sie möchten, dass Sie einfach ist, aber Sie können beides erreichen? Es gibt eine natürliche Spannung zwischen diesen Zielen, aber diese Spannung ist weit von der unversöhnlichen Spannung entfernt. Sie können sowohl die Leistung als auch die Einfachheit durch sorgfältig ausgeglichene Funktionsauswahl und-Präsentation erreichen.

## <a name="what-makes-an-application-powerful"></a>Was ist eine leistungsfähige Anwendung?

Was bedeutet "Leistung" wirklich in Bezug auf Software? Eine Anwendung kann als leistungsstark angesehen werden, wenn Sie eine vollständige Fülle von Features bietet und eine enorme Bandbreite an Funktionalität hat, um allen Benutzern alle Dinge zu erleichtern. Ein solcher Entwurf ist wahrscheinlich nicht erfolgreich, weil ein nicht gezielter Featuresatz unwahrscheinlich ist, dass er die Anforderungen von beliebigen Personen erfüllt. Dabei handelt es sich nicht um die Art der Stromversorgung.

Eine Anwendung ist leistungsstark, wenn Sie über die richtige Kombination dieser Merkmale verfügt:

-   **Genden.** Die Anwendung erfüllt die Anforderungen der Ziel Benutzer, sodass Sie Aufgaben ausführen können, die Sie nicht anderweitig ausführen konnten, und ihre Ziele effektiv erreichen.
-   **Effizient.** Die Anwendung ermöglicht Benutzern das Ausführen von Aufgaben mit einem Maß an Produktivität und Skalierung, die zuvor nicht möglich waren.
-   **Fältig.** Die Anwendung ermöglicht es Benutzern, eine Vielzahl von Aufgaben in unterschiedlichen Situationen effektiv auszuführen.
-   **Unmittelbaren.** Die Anwendung sieht so aus, als würde Sie Benutzern direkt dabei helfen, ihre Ziele zu erreichen, anstatt sich auf den Weg zu bringen oder unnötige Schritte zu erfordern. Features wie Tastenkombinationen, Tastatur Zugriff und Makros verbessern den Sinn der Direktheit.
-   **Flexiblen.** Die Anwendung ermöglicht es Benutzern, eine genaue Kontrolle über ihre Arbeit zu erhalten.
-   **Verbund.** Die Anwendung ist gut in Microsoft Windows integriert und ermöglicht die gemeinsame Nutzung von Daten mit anderen Anwendungen.
-   **Erweitert.** Die Anwendung hat außergewöhnliche, innovative, hochmoderne Features, die in konkurrierenden Lösungen nicht gefunden werden.

Einige dieser Merkmale hängen von der Wahrnehmung des Benutzers ab und sind relativ zu den aktuellen Funktionen der Benutzer. Was als leistungsstark angesehen wird, kann sich im Laufe der Zeit ändern, sodass die erweiterte Suchfunktion von heute heute möglicherweise üblich ist.

Alle diese Merkmale können mit unserer Power-Definition kombiniert werden:

**Eine Anwendung ist leistungsfähig, wenn Sie Ihren Ziel Benutzern ermöglicht, Ihr vollständiges Potenzial effizient zu realisieren.**

Folglich ist das ultimative Maß an Energieproduktivität und nicht die Anzahl der Features.

Verschiedene Benutzer benötigen unterschiedliche Möglichkeiten, um das volle Potenzial zu erreichen. Was die Aktivierung für einige Benutzer ermöglicht, kann die Flexibilität, die Direktheit und die Kontrolle für andere beeinträchtigen. Gut entworfene Software muss diese Merkmale entsprechend ausgleichen. Beispielsweise kann ein Desktop Publishing System, das für Nichtfachleute entworfen wurde, mithilfe von Assistenten die Benutzer durch komplexe Aufgaben durchlaufen. Diese Assistenten ermöglichen es den Ziel Benutzern, Aufgaben auszuführen, die andernfalls nicht durchgeführt werden könnten. Im Gegensatz dazu kann sich ein Desktop Publishing System für Fachleute auf die Direktheit, Effizienz und umfassende Kontrolle konzentrieren. Für Benutzer einer solchen Anwendung sind Assistenten möglicherweise eingeschränkt und frustrierend.

**Wenn Sie nur eine Aktion ausführen...**

Verstehen Sie die Ziele ihrer Ziel Benutzer, und erstellen Sie eine Featuregruppe, mit der Sie diese Ziele produktiv erreichen können.

## <a name="what-makes-a-user-experience-simple"></a>Was macht eine Benutzer Darstellung einfach?

Die Einfachheit wird wie folgt definiert:

**Einfachheit ist die Reduzierung oder Eliminierung eines Attributs eines Entwurfs, den Ziel Benutzern bekannt sind, und es ist nicht zwingend erforderlich.**

In der Praxis wird die Einfachheit erreicht, indem die richtige Funktion ausgewählt und die Features auf die richtige Weise präsentiert werden. Dadurch wird die nicht erforderliche Bedeutung, sowohl real als auch wahr, reduziert.

Die Einfachheit hängt von der Wahrnehmung von Benutzern ab. Beachten Sie, wie die Auswirkungen einer automatischen Übertragung von der Perspektive eines Benutzers abhängen:

-   Bei einem typischen Treiber (dem Ziel Benutzer) entfällt eine automatische Übertragung darauf, dass ein manueller Zahnrad Wechsel und eine schiebeanlage nicht mehr erforderlich sind. Ein manueller Zahnrad und eine manuelle Ausrüstung sind für die Aufgabe des treibungs nicht zwingend notwendig, sodass Sie entfernt werden, um Einfachheit zu erzielen.
-   Bei einem professionellen Rennwagen-Treiber ist die direkte Kontrolle über die Übertragung für die Wettbewerbsfähigkeit von entscheidender Bedeutung. Eine automatische Übertragung wirkt sich negativ auf die Fahrzeugleistung aus und wird daher nicht als Ergebnis der Einfachheit betrachtet.
-   Bei einem-Mechaniker handelt es sich bei einer automatischen Übertragung um einen komplexeren Mechanismus, der nicht einfacher zu reparieren oder zu warten ist als eine manuelle Übertragung. Im Gegensatz zum-Mechaniker kennt der Ziel Benutzer diese interne Komplexität nicht.

Während unterschiedliche Benutzer die automatische Übertragung anders betrachten, ist Sie erfolgreich, da Sie die Notwendigkeit von nicht wesentlichen Kenntnissen, Kenntnissen und Aufwand von ihren Ziel Benutzern entfällt. Für den typischen Treiber ist die automatische Übertragung ein hervorragend, da Sie einfach funktioniert.

### <a name="simplicity-vs-ease-of-use"></a>Einfachheit und Benutzerfreundlichkeit

Die Einfachheit ist, wenn Sie ordnungsgemäß angewendet wird, einfacher zu verwenden. Einfachheit und einfache Verwendung sind jedoch nicht die gleichen Konzepte. Benutzerfreundlichkeit wird erzielt, wenn Benutzer eine Aufgabe ohne Schwierigkeiten oder Verwirrung innerhalb eines angemessenen Zeitraums erfolgreich ausführen können. Es gibt viele Methoden, um die Benutzerfreundlichkeit zu vereinfachen, und Einfachheit – die Verringerung der unwesentlichen – ist nur eine davon.

Alle Benutzer, unabhängig davon, wie ausgereift Sie Ihre Arbeit mit minimalem Aufwand erledigen möchten. Alle Benutzer – auch erweiterte Benutzer – sind hauptsächlich motiviert, ihre Arbeit zu erledigen, ohne sich über Computer oder Ihre Anwendung zu informieren.

Einfachheit ist die effektivste Methode, um die Benutzerfreundlichkeit zu vereinfachen und Benutzerfreundlichkeit zu verwenden. Komplexe, schwer zu verwendende Features werden einfach nicht verwendet. Im Gegensatz dazu sind einfache, elegante Entwürfe, die ihre Funktionsweise ausführen, eine Freude zu verwenden. Sie rufen eine positive, emotionale Reaktion auf.

Sehen Sie sich beispielsweise die Unterstützung für drahtlose Netzwerke in Microsoft Windows XP an. Microsoft könnte einen Assistenten hinzugefügt haben, um die Benutzer durch den Konfigurationsprozess zu durchlaufen. Diese Vorgehensweise würde zu einer einfachen Verwendung, aber nicht zur Vereinfachung führen, da ein nicht wesentliches Feature (der Assistent) hinzugefügt worden wäre. Stattdessen hat Microsoft drahtloses Netzwerk entworfen, um sich automatisch selbst zu konfigurieren. Der Benutzer kümmert sich letztendlich nicht um die Konfigurationsdetails, solange er zuverlässig und sicher funktioniert. Diese Kombination aus Leistung und Einfachheit in drahtlosen Netzwerktechnologien hat zu seiner Beliebtheit und schnellen Akzeptanz geführt.

**Wenn Sie nur eine Aktion ausführen...**

Starten Sie Ihren Entwurfsprozess mit den einfachsten Entwürfen, die den Auftrag gut machen.

Wenn Sie mit dem aktuellen Design nicht zufrieden sind, können Sie zunächst alle nicht wesentlichen Elemente entfernen. Sie werden feststellen, dass es in der Regel sehr gut bleibt.

## <a name="obtaining-simplicity-while-maintaining-power"></a>Einfachheit der Vereinfachung und Aufrechterhaltung der Leistung

### <a name="design-principles"></a>Entwurfsprinzipien

Um die Einfachheit zu erhalten, entwerfen Sie immer für die wahrscheinliche, nicht für die Möglichkeit.

Der mögliche

Entwerfen Sie Entscheidungen auf der Grundlage der möglichen Ergebnisse komplexer Benutzeroberflächen, wie z. b. des Registrierungs-Editors, wobei beim Entwurf davon ausgegangen wird, dass alle Aktionen gleichermaßen möglich sind und somit der gleiche Aufwand erforderlich ist. Da alles möglich ist, werden Benutzer Ziele bei Entwurfsentscheidungen nicht berücksichtigt.

Das wahrscheinliche

Entwurfsentscheidungen auf der Grundlage des wahrscheinlichen Leads zu vereinfachten, Ziel-und aufgabenbasierten Lösungen, bei denen die wahrscheinlichen Szenarien den Fokus erhalten und einen minimalen Aufwand benötigen.

Das Entwurfs Prinzip der Einfachheit

**Um Einfachheit zu erzielen, konzentrieren Sie sich auf das, was wahrscheinlich ist. reduzieren, ausblenden oder entfernen, was unwahrscheinlich ist. und vermeiden Sie, was unmöglich ist.**

Was Benutzer tun werden, ist weitaus relevanter für den Entwurf, als dies möglich wäre.

### <a name="design-techniques"></a>Entwurfs Techniken

Um die Einfachheit zu gewährleisten und gleichzeitig die Leistung aufrechtzuerhalten, wählen Sie den **richtigen Satz von Features**, suchen Sie die Features **an den richtigen Stellen**, und **reduzieren Sie den Aufwand** für deren Verwendung. Dieser Abschnitt enthält einige gängige Verfahren zum Erreichen dieser Ziele.

Auswählen des richtigen Funktions Satzes

"Perfektion wird erzielt, nicht, wenn keine weiteren Elemente hinzugefügt werden müssen.

aber wenn es noch nichts zu tun hat. " – Antoine de Saint-Exupery

Mithilfe der folgenden Entwurfs Techniken erhalten Ihre Benutzer die Features, die Sie benötigen, während Sie durch die tatsächliche Reduzierung oder Entfernung eine Vereinfachung erreichen:

-   **Bestimmen Sie die Funktionen, die Ihre Benutzer benötigen.** Verstehen Sie die Anforderungen Ihrer Benutzer durch Ziel, Szenario und Aufgabenanalyse. Legen Sie eine Reihe von Features fest, mit denen diese Ziele realisiert werden.
-   **Entfernen Sie unnötige Elemente.** Entfernen Sie Elemente, die wahrscheinlich nicht verwendet werden oder eine bevorzugte Alternative sind.
-   **Entfernen Sie unnötige Redundanz.** Es gibt möglicherweise mehrere effektive Möglichkeiten, um eine Aufgabe auszuführen. Um die Einfachheit zu vereinfachen, treffen Sie die harte Entscheidung, und wählen Sie die beste Entscheidung für Ihre Ziel Benutzer, anstatt alle Optionen bereitzustellen und die Auswahl einer Option zu treffen.
-   **Legen Sie den Wert "just work" automatisch ab.** Das-Element ist erforderlich, aber es ist nicht möglich, eine Benutzerinteraktion zu erreichen, da es ein akzeptables Standardverhalten oder eine akzeptable Konfiguration gibt. Um Einfachheit zu gewährleisten, machen Sie es automatisch, und blenden Sie es entweder vollständig vom Benutzer aus, oder verringern Sie die Verfügbarkeit erheblich.

Optimieren der Präsentation

"Die Möglichkeit zur Vereinfachung der Vermeidung der unnötigen

Dies ist möglich, damit die erforderliche Sprache " – Hans Hofmann

Verwenden Sie die folgenden Entwurfs Techniken, um die Leistung aufrechtzuerhalten, während Sie die Einfachheit durch die Wahrnehmung von Reduzierungs-oder Entfernungs Möglichkeiten erzielen

-   **Kombinieren Sie, was kombiniert werden soll.** Fügen Sie die wesentlichen Features, die eine Aufgabe unterstützen, so ein, dass eine Aufgabe an einem Ort ausgeführt werden kann. Die Schritte der Aufgabe sollten über einen einheitlichen, optimierten Flow verfügen. Unterbrechen Sie komplexe Aufgaben in eine Reihe einfacher, klarer Schritte, damit "One" von mehreren Benutzeroberflächen Oberflächen, wie z. b. einem Assistenten, bestehen kann.
-   **Trennen Sie, was getrennt werden soll.** Es kann nicht alles an einem Ort dargestellt werden, sodass Sie immer über klare, gut ausgewählte Grenzen verfügen. Stellen Sie Features zur Unterstützung von Kern Szenarien zentral und offensichtlich dar, und blenden Sie optionale Funktionen aus, oder machen Sie Sie Peripherie Trennen Sie einzelne Aufgaben, und stellen Sie Links zu verwandten Aufgaben bereit. Beispielsweise sollten Tasks, die sich auf die Bearbeitung von Fotos beziehen, eindeutig von Aufgaben im Zusammenhang mit der Verwaltung von Fotos getrennt werden, Sie sollten jedoch problemlos voneinander zugänglich sein.
-   **Vermeiden Sie, was entfernt werden kann.** Erstellen Sie einen Ausdruck für den Entwurf, und markieren Sie die Elemente, die zum Ausführen der wichtigsten Aufgaben verwendet werden. Markieren Sie sogar die einzelnen Wörter im Benutzeroberflächen Text, die nützliche Informationen vermitteln. Überprüfen Sie nun, was nicht hervorgehoben ist, und entfernen Sie es aus dem Design. Würde es passieren, wenn Sie das Element entfernen? Wenn nicht, entfernen Sie Sie!
-   Konsistenz, Konfigurierbarkeit und Generalisierung sind häufig wünschenswert, aber Sie können zu unnötiger Komplexität führen. Überprüfen Sie den Entwurf auf unkonsistente Anstrengungen (z. b. mit redundantem Text), Generalisierung (z. b. eine beliebige Anzahl von Zeitzonen, wenn zwei ausreichen), und konfigurieren Sie die Konfiguration (z. b. Optionen, die Benutzer wahrscheinlich nicht ändern), und beseitigen Sie, was beseitigt werden kann.
-   **Platzieren Sie die Elemente an der richtigen Stelle.** Innerhalb eines Fensters sollte die Position eines Elements dem-Hilfsprogramm folgen. Wichtige Steuerelemente, Anleitungen und Erläuterungen sollten alle in der logischen Reihenfolge zueinander stehen. Wenn weitere Optionen erforderlich sind, machen Sie diese im Kontext verfügbar, indem Sie auf ein Chevron oder einen ähnlichen Mechanismus klicken. Wenn weitere Informationen erforderlich sind, zeigen Sie mit der Maus auf einen InfoTipp. Legen Sie weniger wichtige Aufgaben, Optionen und Hilfe Informationen außerhalb des Hauptflusses in einem separaten Fenster oder einer separaten Seite ab. Das Verfahren, bei Bedarf weitere Details anzuzeigen, wird als Progressive Offenlegung bezeichnet.
-   **Verwenden Sie sinnvolle allgemeine Kombinationen.** Es ist häufig einfacher und skalierbarer, Gruppen verwandter Elemente auszuwählen und zu bearbeiten, als einzelne Elemente. Beispiele für allgemeine Kombinationen sind Ordner, Designs, Stile und Benutzergruppen. Solche Kombinationen sind häufig einem Benutzer Ziel oder einer Absicht zugeordnet, das nicht aus den einzelnen Elementen ersichtlich ist. Beispielsweise ist die Absicht hinter dem hoher Kontrast Black-Farbschema weitaus deutlicher als die des Hintergrunds eines schwarzen Fensters.
-   **Wählen Sie die richtigen Steuerelemente aus.** Entwurfs Elemente werden durch die Steuerelemente, die Sie zur Darstellung verwenden, verkörpert. Daher ist die Auswahl des richtigen Steuer Elements für eine effiziente Darstellung von entscheidender Bedeutung. Das von Microsoft Word verwendete Feld Schriftart Auswahl zeigt beispielsweise sowohl eine Vorschau der Schriftart als auch die zuletzt verwendeten Schriftarten an. Ebenso ist die Art und Weise, in der Word potenzielle Rechtschreibung und Grammatikfehler anzeigt, viel einfacher als die Alternative zum Dialogfeld, wie am Anfang dieses Artikels zu sehen ist.

Verringern des Aufwands

"Einfache Dinge sollten einfach sein.

Komplexe Dinge sollten möglich sein. " – Alan Kay

Die folgenden Entwurfs Techniken führen zu einem geringeren Aufwand für Benutzer:

-   **Machen Sie Aufgaben erkennbar und sichtbar.** Alle Tasks, aber besonders häufige Aufgaben, sollten in der Benutzeroberfläche problemlos auffallen. Die Schritte, die zum Ausführen von Aufgaben erforderlich sind, sollten sichtbar sein und sollten sich nicht auf die Speicherung verlassen.
-   **Stellen Sie Aufgaben in der Domäne des Benutzers dar.** Komplexe Software erfordert, dass Benutzer ihre Probleme der Technologie zuordnen. Einfache Software führt diese Zuordnung für Sie durch, indem Sie die Natur darstellt. Beispielsweise wird ein Feature für die Red-Eye-Reduzierung direkt dem Problembereich zugeordnet, und es ist nicht erforderlich, dass Benutzer in Bezug auf Details wie Farben und Farbverläufe suchen.
-   **Fügen Sie das Domänen Wissen in das Programm ein.** Es ist nicht erforderlich, dass Benutzer auf externe Informationen zugreifen müssen, um die Anwendung erfolgreich zu verwenden. Domänen wissen können aus komplexen Daten und Algorithmen reichen, um einfach zu klären, welche Art von Eingabe gültig ist.
-   **Verwenden Sie Text, den Benutzer verstehen.** Gut erstellter Text ist für die effektive Kommunikation mit Benutzern von entscheidender Bedeutung. Verwenden Sie Konzepte und Begriffe, die Ihren Benutzern vertraut sind. Erläutern Sie vollständig, was in Klartext gefordert wird, damit Benutzer intelligente, fundierte Entscheidungen treffen können.
-   **Verwenden Sie sichere, sichere, wahrscheinliche Standardwerte.** Wenn eine Einstellung einen Wert hat, der für die meisten Benutzer in den meisten Fällen gilt und diese Einstellung sicher und sicher ist, verwenden Sie Sie als Standardwert. Legen Sie fest, dass Benutzer nur bei Bedarf Werte angeben.
-   **Verwenden Sie Einschränkungen.** Wenn es viele Möglichkeiten gibt, eine Aufgabe auszuführen, aber nur einige richtig sind, schränken Sie die Aufgabe auf die richtigen Arten ein. Benutzer sollten nicht berechtigt sein, leicht vermeidende Fehler zu machen.

### <a name="simplicity-does-not-mean-simplistic"></a>Einfachheit bedeutet nicht vereinfachtes

"Alles sollte so einfach wie möglich gemacht werden,

aber nicht einfacher. " – Albert Einstein

Wir sind der Meinung, dass die Einfachheit für eine effektive, wünschenswerte Benutzerfreundlichkeit entscheidend ist – aber es ist immer möglich, eine gute Sache zu haben. Der Einfachheit halber ist die Verringerung oder Beseitigung der unwesentlichen Bedeutung. Durch das Entfernen der Essentials wird nur ein schlechter Entwurf erzeugt. Wenn Ihre "Vereinfachung" dazu führt, dass Benutzer frustriert, verwirrt, nicht sicher oder nicht erfolgreich abgeschlossen werden können, haben Sie zu viele entfernt.

### <a name="simplicity-does-mean-more-effort-for-you"></a>Einfachheit bedeutet mehr Aufwand für Sie

"Ich habe diesen Buchstaben nur noch länger gemacht, weil ich

nicht die Zeit, um sie kürzer zu machen. " – Blaise Pascal

Die Einfachheit der Vereinfachung und Beibehaltung der Leistung erfordert häufig eine erhebliche interne Komplexität. Es ist in der Regel einfacher, Software zu entwerfen, die alle Technologieanlagen bereitstellt, als eine solche Technologie zu entwerfen, die Sie verbirgt – das zweite erfordert ein hervorragendes Verständnis Ihrer Ziel Benutzer und ihrer Ziele. Das Entfernen eines Features erfordert Disziplin, da es sich nicht um das Hinzufügen dieses coolen Features handelt, das wirklich nicht praktikabel ist. Der Einfachheit halber müssen Sie feststellen, dass Sie nicht alles konfigurierbare gestalten Komplexe Software resultiert häufig aus einer Fehldarstellung der Benutzer: Sie nutzen nicht verwendete Features oder übermäßig komplexe Features, die Sie nicht verstehen.

## <a name="powerful-and-simple"></a>Leistungsstark und einfach

Bei der Energieversorgung geht es um das Aktivieren Ihrer Benutzer und die Produktivität. Einfachheit geht es darum, das unwesentliche zu entfernen und Features auf die richtige Weise darzustellen. Wenn Sie Ihre Ziel Benutzer verstehen und das richtige Gleichgewicht von Features und Präsentationen erzielen, können Sie Windows-basierte Anwendungen entwickeln, die beides tun.

 

 