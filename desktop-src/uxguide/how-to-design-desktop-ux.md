---
title: Entwerfen der Benutzererfahrung für Desktopanwendungen
description: Eine hervorragende Desktopanwendung ist leistungsstark und gleichzeitig einfach. Durch sorgfältig ausgewogene Funktionsauswahl und -darstellung können Sie sowohl Leistungsfähigkeit als auch Einfachheit erreichen.
ms.assetid: 0039a3ee-95bc-457f-a1a8-6a036ce22fd2
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a9c191a92ccf6147d37deca191a861220c4a925035bf39c92e7e7d062fa14184
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119221730"
---
# <a name="how-to-design-a-great-user-experience-for-desktop-applications"></a>Entwerfen einer hervorragenden Benutzeroberfläche für Desktopanwendungen

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Eine hervorragende Desktopanwendung ist leistungsstark und gleichzeitig einfach. Durch sorgfältig ausgewogene Funktionsauswahl und -darstellung können Sie sowohl Leistungsfähigkeit als auch Einfachheit erreichen.

**Leistungsstarke:**

![Screenshot des Dialogfelds "Rechtschreibung und Grammatik" ](images/powerful-simple-image1.png)

**Leistungsstark und einfach:**

![Screenshot der Liste möglicher Rechtschreibrevisionen ](images/powerful-simple-image2.png)

Die ideale Windows-basierte Anwendung ist sowohl leistungsstark als auch einfach. Natürlich möchten Sie, dass Ihre Anwendung leistungsstark und natürlich einfach ist, aber können Sie beides erreichen? Zwischen diesen Zielen gibt es eine natürliche Verzehrlichung, aber dies ist alles andere als unversentlich. Sie können sowohl Leistungsfähigkeit als auch Einfachheit durch sorgfältig ausgewogene Funktionsauswahl und -darstellung erreichen.

## <a name="what-makes-an-application-powerful"></a>Was macht eine Anwendung leistungsfähig?

Was bedeutet "Power" in Bezug auf Software wirklich? Eine Anwendung kann als leistungsstark angesehen werden, wenn sie voll mit Features ist, die eine enorme Bandbreite von Funktionen aufweisen, um alle Dinge für alle Benutzer zu sein. Ein solches Design ist wahrscheinlich nicht erfolgreich, da ein nicht festgelegter Featuresatz wahrscheinlich nicht die Anforderungen von Personen erfüllt. Dies ist nicht die Art von Energie, nach der wir uns befinden.

Eine Anwendung ist leistungsstark, wenn sie die richtige Kombination dieser Merkmale aufweist:

-   **Aktivieren.** Die Anwendung erfüllt die Anforderungen der Zielbenutzer, sodass sie Aufgaben ausführen können, die sie andernfalls nicht ausführen und ihre Ziele effektiv erreichen konnten.
-   **Effizient.** Mit der Anwendung können Benutzer Aufgaben mit einem Maß an Produktivität und Skalierung ausführen, das zuvor nicht möglich war.
-   **Vielseitig.** Mit der Anwendung können Benutzer eine Vielzahl von Aufgaben unter verschiedenen Umständen effektiv ausführen.
-   **Direkte.** Die Anwendung scheint Benutzern direkt dabei zu helfen, ihre Ziele zu erreichen, anstatt sich in den Weg zu stellen oder unnötige Schritte zu erfordern. Features wie Tastenkombinationen, Tastaturzugriff und Makros verbessern das Gefühl der Direktheit.
-   **Flexibel.** Die Anwendung ermöglicht Benutzern eine umfassende, differenzierte Kontrolle über ihre Arbeit.
-   **Integrierte.** Die Anwendung ist gut in Microsoft Windows integriert, sodass sie Daten für andere Anwendungen freigeben kann.
-   **Erweitert.** Die Anwendung verfügt über einzigartige, innovative, moderne Features, die in konkurrierenden Lösungen nicht zu finden sind.

Einige dieser Merkmale hängen von der Wahrnehmung des Benutzers ab und sind relativ zu den aktuellen Funktionen der Benutzer. Was als leistungsfähig angesehen wird, kann sich im Laufe der Zeit ändern, sodass das erweiterte Suchfeature von heute morgen häufig verwendet werden kann.

All diese Merkmale können in unserer Definition der Leistung kombiniert werden:

**Eine Anwendung ist leistungsstark, wenn sie es ihren Zielbenutzern ermöglicht, ihr volles Potenzial effizient zu nutzen.**

Daher ist das endgültige Maß für Die Leistung die Produktivität, nicht die Anzahl der Features.

Verschiedene Benutzer benötigen Hilfe, um ihr volles Potenzial auf unterschiedliche Weise zu erreichen. Was für einige Benutzer aktiviert wird, kann für andere Zufälligkeit, Direktheit und Kontrolle beeinträchtigen. Gut entworfene Software muss diese Merkmale entsprechend ausgleichen. Beispielsweise kann ein Desktopveröffentlichungssystem, das für Nichtprofessionen konzipiert ist, Assistenten verwenden, um Benutzer durch komplexe Aufgaben zu durchlaufen. Solche Assistenten ermöglichen es den Zielbenutzern, Aufgaben auszuführen, die sie andernfalls nicht ausführen können. Im Gegensatz dazu kann sich ein Desktopveröffentlichungssystem für Experten auf Direktheit, Effizienz und vollständige Kontrolle konzentrieren. Für Benutzer einer solchen Anwendung können Assistenten einschränkend und frustrierend sein.

**Wenn Sie nur eine Sache durchführen...**

Verstehen Sie die Ziele Ihrer Zielbenutzer, und erstellen Sie einen Featuresatz, mit dem sie diese Ziele produktiv erreichen können.

## <a name="what-makes-a-user-experience-simple"></a>Was vereinfacht die Benutzerfreundlichkeit?

Die Einfachheit wird wie folgt definiert:

**Einfachheit ist die Reduzierung oder Beseitigung eines Attributs eines Entwurfs, das zielorientierte Benutzer kennen und als unerwähnt betrachten.**

In der Praxis wird die Einfachheit erreicht, indem der richtige Featuresatz ausgewählt und die Features auf die richtige Weise dargestellt werden. Dies reduziert die unwichtige, sowohl reale als auch wahrgenommene.

Die Einfachheit hängt von der Wahrnehmung der Benutzer ab. Berücksichtigen Sie, wie die Auswirkung einer automatischen Übertragung von der Perspektive eines Benutzers abhängt:

-   Für den typischen Fahrer (den Zielbenutzer) entfällt durch ein automatisches Schaltwerk die Notwendigkeit einer manuellen Schalt- und Ziehkraft, sodass ein Auto viel einfacher zu fahren ist. Eine manuelle Zahnradverschiebung und Einarbeitung sind für die Aufgabe des Fahrens nicht erforderlich, daher werden sie entfernt, um Einfachheit zu erzielen.
-   Für einen professionellen Fahrer eines Racewagens ist die direkte Kontrolle über das Transmission entscheidend, um wettbewerbsfähig zu sein. Ein autonatives Schaltnetz wirkt sich negativ auf die Leistung des Autos aus, sodass es nicht als Ergebnis der Einfachheit betrachtet wird.
-   Bei einem Riegel ist eine automatische Übertragung ein komplexerer Mechanismus und daher nicht einfacher zu reparieren oder zu warten als eine manuelle Übertragung. Im Gegensatz zum 1:0-Vorgang ist dem Zielbenutzer diese interne Komplexität bewusst.

Obwohl verschiedene Benutzer die automatische Übertragung unterschiedlich betrachten, ist sie erfolgreich, da sie den Zielbenutzern nicht mehr unwichtiges Wissen, Fähigkeiten und Aufwand abnimmt. Für den typischen Treiber ist die automatische Übertragung ein hervorragendes Feature, da sie einfach funktioniert.

### <a name="simplicity-vs-ease-of-use"></a>Einfachheit und Benutzerfreundlichkeit

Die Einfachheit führt bei korrekter Anwendung zu einer benutzerfreundlichkeit. Einfachheit und Benutzerfreundlichkeit sind jedoch nicht die gleichen Konzepte. Benutzerfreundlichkeit wird erreicht, wenn Benutzer eine Aufgabe innerhalb eines geeigneten Zeitraums ohne Schwierigkeiten oder Verwirrung selbst erfolgreich ausführen können. Es gibt viele Möglichkeiten, die Benutzerfreundlichkeit zu erreichen, und einfachheit – die Reduzierung der unwichtigen – ist nur eine davon.

Alle Benutzer möchten ihre Arbeit unabhängig davon, wie ausgereift sie sind, mit einem minimalen unnötigen Aufwand erledigen. Alle Benutzer – auch fortgeschrittene Benutzer – sind in erster Linie daran ausgerichtet, ihre Arbeit zu erledigen, nicht um mehr über Computer oder Ihre Anwendung zu erfahren.

Einfachheit ist die effektivste Methode, um benutzerfreundlichkeit und Benutzerfreundlichkeit gleich zu erreichen. Komplexe, schwer zu verwendende Features werden einfach nicht verwendet. Im Gegensatz dazu sind einfache, elegante Entwürfe, die ihre Funktion gut erfüllen, ein Sehr gut zu verwenden. Sie rufen eine positive, emotionale Antwort auf.

Betrachten Sie z. B. die Drahtlose Netzwerkunterstützung in Microsoft Windows XP. Microsoft hätte einen Assistenten hinzufügen können, um Benutzer durch den Konfigurationsprozess zu durchlaufen. Dieser Ansatz hätte zu benutzerfreundlichkeit, aber nicht zur Einfachheit geführt, da ein unwichtiges Feature (der Assistent) hinzugefügt worden wäre. Stattdessen hat Microsoft Funknetzwerke entwickelt, um sich automatisch zu konfigurieren. Die Konfigurationsdetails sind den Benutzern letztlich egal, solange sie zuverlässig und sicher funktionieren. Diese Kombination aus Leistung und Einfachheit bei der Funknetzwerktechnologie hat zu ihrer Beliebtheit und schnellen Einführung geführt.

**Wenn Sie nur eine Sache durchführen...**

Starten Sie Ihren Entwurfsprozess mit den einfachsten Entwürfen, die den Auftrag gut erledigen.

Wenn Sie mit Ihrem aktuellen Entwurf nicht zufrieden sind, beginnen Sie damit, alle unwichtigen Elemente zu entpacken. Sie werden feststellen, dass das, was bleibt, in der Regel recht gut ist.

## <a name="obtaining-simplicity-while-maintaining-power"></a>Erhalten von Einfachheit bei gleichzeitiger Beibehaltung der Leistung

### <a name="design-principles"></a>Entwurfsprinzipien

Um einfachheitserlangend zu sein, entwerfen Sie immer für das Wahrscheinliche, nicht für das Mögliche.

Die mögliche

Entwurfsentscheidungen, die auf den möglichen Möglichkeiten basieren, führen zu komplexen Benutzeroberflächen wie dem Registrierungs-Editor, wobei der Entwurf davon ausgeht, dass alle Aktionen gleich möglich sind und daher gleichen Aufwand erfordern. Da alles möglich ist, werden Benutzerziele bei Entwurfsentscheidungen nicht berücksichtigt.

Die wahrscheinliche

Entwurfsentscheidungen, die auf der wahrscheinlichen basieren, führen zu vereinfachten, ziel- und aufgabenbasierten Lösungen, bei denen die wahrscheinlichen Szenarien den Fokus erhalten und nur minimalen Aufwand erfordern.

Das Prinzip des Einfachheitsentwurfs

**Konzentrieren Sie sich auf die Wahrscheinlichkeit, um einfachheitsorientiert zu sein. reduzieren, ausblenden oder entfernen, was unwahrscheinlich ist; und beseitigen, was unmöglich ist.**

Was Benutzer tun werden, ist wesentlich relevanter für den Entwurf als das, was sie tun könnten.

### <a name="design-techniques"></a>Entwurfstechniken

Um einfachheitshalber die Leistungsfähigkeit beizubehalten, wählen Sie die **richtigen Features** aus, suchen Sie die Features **an den richtigen Stellen,** und reduzieren Sie den Aufwand für **deren** Verwendung. In diesem Abschnitt werden einige gängige Verfahren zum Erreichen dieser Ziele beschrieben.

Auswählen des richtigen Featuresets

"Dies wird erreicht, nicht, wenn nichts mehr hinzugefügt werden muss.

aber wenn nichts mehr weggelassen werden muss." – Beim De-Saint-Exupery

Die folgenden Entwurfstechniken bieten Ihren Benutzern die Features, die sie benötigen, und erreichen gleichzeitig Einfachheit durch tatsächliche Reduzierung oder Entfernung:

-   **Bestimmen Sie die Features, die Ihre Benutzer benötigen.** Machen Sie sich mit den Anforderungen Ihrer Benutzer durch Ziel-, Szenario- und Aufgabenanalyse klar. Bestimmen Sie eine Reihe von Features, die diese Ziele erreichen.
-   **Entfernen Sie unnötige Elemente.** Entfernen Sie Elemente, die wahrscheinlich nicht verwendet werden oder über bevorzugte Alternativen verfügen.
-   **Entfernen sie unnötige Redundanz.** Es gibt möglicherweise mehrere effektive Möglichkeiten, eine Aufgabe auszuführen. Treffen Sie der Einfachheit halber die schwierige Entscheidung, und wählen Sie die beste Entscheidung für Ihre Zielbenutzer aus, anstatt alle Benutzer zur Verfügung zu stellen und die Auswahl zu einer Option zu machen.
-   **Sorgen Sie dafür, dass es automatisch funktioniert.** Das -Element ist erforderlich, aber jede Benutzerinteraktion, damit es funktioniert, liegt nicht daran, dass es ein akzeptables Standardverhalten oder eine akzeptable Konfiguration gibt. Sorgen Sie zur Vereinfachung dafür, dass die Anwendung automatisch funktioniert, und blenden Sie sie entweder vollständig vor dem Benutzer aus, oder verringern Sie die Gefährdung erheblich.

Optimieren der Präsentation

"Die Möglichkeit der Vereinfachung bedeutet, unnötige

damit das erforderliche sprechen kann." – Hans Hans

Verwenden Sie die folgenden Entwurfstechniken, um die Leistung zu erhalten und gleichzeitig Einfachheit durch die Wahrnehmung von Reduzierung oder Entfernung zu erreichen:

-   **Kombinieren Sie, was kombiniert werden soll.** Legen Sie die wesentlichen Features, die eine Aufgabe unterstützen, zusammen, damit eine Aufgabe an einem Ort ausgeführt werden kann. Die Schritte der Aufgabe sollten einen einheitlichen, optimierten Ablauf haben. Unterlegen Sie komplexe Aufgaben in eine Reihe einfacher, klarer Schritte, sodass ein Ort aus mehreren Benutzeroberflächenoberflächen bestehen kann, z. B. einem Assistenten.
-   **Trennen Sie, was getrennt werden soll.** Nicht alles kann an einem Ort dargestellt werden, daher verfügen Sie immer über klare, gut ausgewählte Grenzen. Machen Sie Features, die Kernszenarien unterstützen, zentral und offensichtlich, und blenden Sie optionale Funktionen aus, oder machen Sie sie zu Peripheriegeräten. Trennen Sie einzelne Aufgaben, und stellen Sie Links zu verwandten Aufgaben zur Verfügung. Beispielsweise sollten Aufgaben im Zusammenhang mit der Bearbeitung von Fotos klar von Aufgaben im Zusammenhang mit der Verwaltung von Sammlungen von Fotos getrennt werden, aber sie sollten leicht voneinander zugänglich sein.
-   **Beseitigen Sie, was beseitigt werden kann.** Nehmen Sie einen Ausdruck Ihres Entwurfs vor, und markieren Sie die Elemente, die zum Ausführen der wichtigsten Aufgaben verwendet werden. Markieren Sie sogar die einzelnen Wörter im Benutzeroberflächentext, die nützliche Informationen kommunizieren. Überprüfen Sie nun, was nicht hervorgehoben ist, und ziehen Sie in Betracht, es aus dem Entwurf zu entfernen. Wenn Sie das Element entfernen, würde etwas Schlechtes passieren? Wenn nicht, entfernen Sie es!
-   Konsistenz, Konfigurierbarkeit und Generalisierung sind häufig wünschenswerte Qualitäten, können aber zu unnötiger Komplexität führen. Überprüfen Sie Ihren Entwurf auf fehlgeleitete Konsistenzbemühungen (z. B. redundanten Text), Generalisierung (z. B. eine beliebige Anzahl von Zeitzonen, wenn zwei ausreichend sind) und Konfigurierbarkeit (z. B. Optionen, die Benutzer wahrscheinlich nicht ändern werden), und beseitigen Sie, was beseitigt werden kann.
-   **Platzieren Sie die Elemente an der richtigen Stelle.** Innerhalb eines Fensters sollte die Position eines Elements seinem Hilfsprogramm folgen. Wichtige Steuerelemente, Anweisungen und Erklärungen sollten alle in logischer Reihenfolge im Kontext sein. Wenn weitere Optionen erforderlich sind, machen Sie sie im Kontext verfügbar, indem Sie auf ein Chevron oder einen ähnlichen Mechanismus klicken. Wenn weitere Informationen erforderlich sind, zeigen Sie eine Infotip an, wenn Sie mit dem Mauszeiger darauf zeigen. Platzieren Sie weniger wichtige Aufgaben, Optionen und Hilfeinformationen außerhalb des Hauptflusses in einem separaten Fenster oder einer separaten Seite. Die Technik, bei Bedarf zusätzliche Details anzuzeigen, wird als progressive Offenlegung bezeichnet.
-   **Verwenden Sie aussagekräftige Kombinationen auf hoher Ebene.** Häufig ist es einfacher und skalierbarer, Gruppen verwandter Elemente auszuwählen und zu bearbeiten als einzelne Elemente. Beispiele für Kombinationen auf hoher Ebene sind Ordner, Designs, Stile und Benutzergruppen. Solche Kombinationen sind häufig einem Benutzerziel oder einer Absicht zuordnen, die in den einzelnen Elementen nicht offensichtlich ist. Beispielsweise ist die Absicht hinter dem farblich hoher Kontrast Schwarz viel offensichtlicher als die eines schwarzen Fensterhintergrunds.
-   **Wählen Sie die richtigen Steuerelemente aus.** Entwurfselemente werden durch die Steuerelemente repräsentiert, die Sie zur Darstellung verwenden. Daher ist die Auswahl des richtigen Steuerelements entscheidend für eine effiziente Darstellung. Beispielsweise zeigt das von Microsoft Word verwendete Schriftartauswahlfeld sowohl eine Vorschau der Schriftart als auch die zuletzt verwendeten Schriftarten an. Ebenso ist die Art und Weise, wie Word potenzielle Rechtschreib- und Grammatikfehler zeigt, wesentlich einfacher als die Dialogfeldalternative, wie am Anfang dieses Artikels gezeigt.

Reduzieren des Aufwands

"Einfache Dinge sollten einfach sein.

Komplexe Dinge sollten möglich sein." —Durch eine 10-0-

Die folgenden Entwurfstechniken führen zu weniger Aufwand für Benutzer:

-   **Machen Sie Aufgaben erkennbar und sichtbar.** Alle Aufgaben, aber insbesondere häufige Aufgaben, sollten innerhalb der Benutzeroberfläche leicht erkennbar sein. Die schritte, die zum Ausführen von Aufgaben erforderlich sind, sollten sichtbar sein und dürfen sich nicht auf einPräzisieren verlassen.
-   **Stellen Sie Aufgaben in der Domäne des Benutzers vor.** Komplexe Software erfordert, dass Benutzer ihre Probleme der Technologie zuordnen. Einfache Software übernimmt diese Zuordnung für sie, indem sie das Natürliche präsentiert. Beispielsweise wird eine Red Eye-Reduzierungsfunktion direkt dem Problembereich zu entnehmen und erfordert nicht, dass Benutzer in Bezug auf Details wie Farbtons und Farbverläufe denken.
-   **Legen Sie Domänenwissen in das Programm ein.** Benutzer sollten nicht auf externe Informationen zugreifen müssen, um Ihre Anwendung erfolgreich zu verwenden. Domänenwissen kann von komplexen Daten und Algorithmen bis zur einfachen Eindeutigung reichen, welche Art von Eingabe gültig ist.
-   **Verwenden Sie Text, den Benutzer verstehen.** Gut gestalteter Text ist entscheidend für die effektive Kommunikation mit Benutzern. Verwenden Sie Konzepte und Begriffe, die Ihren Benutzern vertraut sind. Erläutern Sie vollständig, was in einfacher Sprache gefragt wird, damit Benutzer intelligente, fundierte Entscheidungen treffen können.
-   **Verwenden Sie sichere, wahrscheinliche Standardwerte.** Wenn eine Einstellung über einen Wert verfügt, der in den meisten Fällen für die meisten Benutzer gilt und diese Einstellung sowohl sicher als auch sicher ist, verwenden Sie sie als Standardwert. Legen Sie fest, dass Benutzer Nur bei Bedarf Werte angeben.
-   **Verwenden Sie Einschränkungen.** Wenn es viele Möglichkeiten gibt, eine Aufgabe auszuführen, aber nur einige korrekt sind, schränken Sie die Aufgabe auf diese richtigen Methoden ein. Benutzern sollte nicht gestattet werden, leicht vermeidbare Fehler zu machen.

### <a name="simplicity-does-not-mean-simplistic"></a>Einfachheit bedeutet nicht einfach

"Alles sollte so einfach wie möglich gemacht werden.

aber nicht einfacher." —Beim Ansingen von

Wir sind der Meinung, dass Die Einfachheit entscheidend für eine effektive, wünschenswerte Benutzererfahrung ist, aber es ist immer möglich, eine gute Sache zu weit zu gehen. Das Wesentliche der Einfachheit ist die Reduzierung oder Beseitigung der unerlädlichen . Das Entfernen des grundlegenden -Konzepts führt lediglich zu einem schlechten Design. Wenn Ihre "Vereinfachung" dazu führt, dass Benutzer frustriert, verwirrend, unauffällig sind oder aufgaben nicht erfolgreich abgeschlossen werden können, haben Sie zu viel entfernt.

### <a name="simplicity-does-mean-more-effort-for-you"></a>Einfachheit bedeutet mehr Aufwand für Sie

"Ich habe diesen Buchstaben nur länger gemacht, weil ich

nicht die Zeit, um sie kürzer zu machen." – Blaise Pascal

Um einfachheit zu erhalten und gleichzeitig die Leistung zu erhalten, ist häufig eine erhebliche interne Komplexität erforderlich. In der Regel ist es einfacher, Software zu entwerfen, die die ganze Technologie zur Verfügung stellt, als eine zu entwerfen, die sie ausblendet. Letzteres erfordert ein hervorragendes Verständnis ihrer Zielbenutzer und ihrer Ziele. Das Entfernen eines Features erfordert Disziplin, ebenso wie die Entscheidung gegen das Hinzufügen dieses coolen Features, das eigentlich nicht praktikabel ist. Der Einfachheit halber müssen Sie schwierige Entwurfsentscheidungen treffen, anstatt alles konfigurierbar zu machen. Komplexe Software resultiert häufig aus einem Missverständnis von Benutzern: dass sie nicht verwendete Features oder zu komplexe Features schätzen, die sie nicht verstehen können.

## <a name="powerful-and-simple"></a>Leistungsfähig und einfach

Bei Power geht es darum, Ihre Benutzer zu aktivieren und produktiv zu machen. Bei der Einfachheit geht es darum, die unerlässlichen Features zu entfernen und features auf die richtige Weise zu präsentieren. Indem Sie Ihre Zielbenutzer verstehen und das richtige Gleichgewicht zwischen Features und Präsentation erreichen, können Sie Windows-basierten Anwendungen entwerfen, die beides tun.

 

 