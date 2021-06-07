---
title: Statusleisten
description: Mit einer Statusanzeige können Benutzer den Fortschritt eines längeren Vorgangs verfolgen. Eine Statusanzeige kann entweder einen ungefähren Prozentsatz des Abschlusses anzeigen (determinieren) oder angeben, dass ein Vorgang ausgeführt wird (unbestimmter).
ms.assetid: 067961fa-2fb1-4cd1-99a4-cbe2244c3913
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f0bb693541f40b82c66409b9f6696456491ba687
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444711"
---
# <a name="progress-bars"></a>Statusleisten

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Mit einer Statusanzeige können Benutzer den Fortschritt eines längeren Vorgangs verfolgen. Eine Statusanzeige kann entweder einen ungefähren Prozentsatz des Abschlusses anzeigen (determinieren) oder angeben, dass ein Vorgang ausgeführt wird (unbestimmter).

Benutzerfreundlichkeitsstudien haben ergeben, dass Benutzer die Antwortzeiten von mehr als einer Sekunde kennen. Daher sollten Sie Vorgänge, deren Abschluss zwei Sekunden oder länger dauert, als lang betrachten und ein gewisses Fortschrittsfeedback benötigen.

![Screenshot einer typischen Statusanzeige ](images/progress-bars-image1.png)

Eine typische Statusanzeige.

> [!Note]  
> Richtlinien im Zusammenhang mit [dem Layout](vis-layout.md) werden in einem separaten Artikel vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird der Vorgang in etwa fünf Sekunden oder weniger abgeschlossen?** Wenn ja, verwenden Sie stattdessen einen [Aktivitätsindikator,](inter-mouse.md) da das Anzeigen einer Statusanzeige für eine solche kurze Dauer ablenkend wäre. Wenn der Vorgang in der Regel fünf Sekunden oder weniger dauert, aber manchmal mehr dauert, beginnen Sie mit einem ausgelasteten Zeiger, und konvertieren Sie nach fünf Sekunden in eine Statusanzeige.
-   **Wird eine unbestimmte Statusanzeige verwendet, um zu warten, bis der Benutzer eine Aufgabe abgeschlossen hat?** Wenn ja, zeigen Sie keine Statusleiste an. Statusleisten sind für den Status des Computers gedacht, nicht für den der Benutzer.
-   **Ist eine unbestimmte Statusanzeige mit einer Animation kombiniert?** Wenn ja, verwenden Sie stattdessen nur die Animation. Die unbestimmte Statusanzeige ist im Grunde eine generische Animation und fügt der Animation keinen Wert hinzu.
-   **Handelt es sich bei dem Vorgang um eine sehr lange Hintergrundaufgabe (länger als zwei Minuten), für die Benutzer eher am Abschluss als am Fortschritt interessiert sind?** Verwenden Sie in diesem Falle stattdessen eine [Benachrichtigung.](mess-notif.md) In diesem Fall erledigen Benutzer in der Zwischenzeit andere Aufgaben und überwachen den Fortschritt nicht. Mithilfe einer Benachrichtigung können Benutzer andere Aufgaben ohne Unterbrechung ausführen. Beispiele für solche langwierigen Vorgänge sind Drucken, Sichern, Systemscans und Massendatenübertragungen oder -konvertierungen.
-   **Können Benutzer nach Abschluss des Vorgangs die Ergebnisse wiedergeben?** Verwenden Sie in diesem Falle stattdessen einen Schieberegler. Beispiele für solche Vorgänge sind Video- und Audioaufzeichnung und -wiedergabe.

    ![Screenshot von Media Player und Schieberegler ](images/progress-bars-image2.png)

    In diesem Beispiel wird ein Schieberegler verwendet, um den Fortschritt beim Wiedergeben von Sound anzugeben. Auf diese Weise können Benutzer die Ergebnisse später wiedergeben.

## <a name="design-concepts"></a>Entwurfskonzepte

Während eines längeren Vorgangs benötigen Benutzer eine allgemeine Vorstellung davon, was der Vorgang tut. Außerdem müssen sie wissen:

-   Ein längerer Vorgang wurde gestartet.
-   Dieser Fortschritt wird ausgeführt, und der Vorgang wird schließlich abgeschlossen (und wurde daher nicht gesperrt).
-   Der ungefähre Prozentsatz des abgeschlossenen Vorgangs (und somit der verbleibende Prozentsatz).
-   Wenn sie den Vorgang abbrechen sollten, wenn es sich nicht lohnt, weiter zu warten.
-   Wenn sie weiterhin warten oder etwas anderes tun sollen, während der Vorgang abgeschlossen ist.

**Verwenden Sie determinierte Statusanzeigen für Vorgänge, die eine bestimmte Zeitspanne erfordern,** auch wenn diese Zeitspanne nicht genau vorhergesagt werden kann. Unbestimmte Statusanzeigen zeigen an, dass der Fortschritt erfolgt, geben aber keine weiteren Informationen an. Wählen Sie keine unbestimmte Statusanzeige aus, die nur auf der möglichen fehlenden Genauigkeit basiert.

Angenommen, ein Vorgang erfordert fünf Schritte, und jeder dieser Schritte erfordert eine begrenzungs lange Zeit, aber die Zeitspanne für jeden Schritt kann stark variieren. Verwenden Sie in diesem Fall eine bestimmende Statusanzeige, und zeigen Sie den Fortschritt an, wenn jeder Schritt abgeschlossen wird, proportional zur Zeitspanne, die jeder Schritt normalerweise benötigt. Verwenden Sie nur dann eine unbestimmte Statusanzeige, wenn eine bestimmende Statusanzeige dazu führen würde, dass Benutzer fälschlicherweise feststellen, dass der Vorgang gesperrt wurde.

**Wenn Sie nur eine Sache tun...**

Stellen Sie sicher, dass Sie Feedback zum Fortschritt für langwierige Vorgänge geben und dass die oben genannten Informationen eindeutig kommuniziert werden. Verwenden Sie nach Möglichkeit determinate progress bars (Statusanzeigen bestimmen).

## <a name="usage-patterns"></a>Verwendungsmuster

Statusleisten weisen mehrere Verwendungsmuster auf:

### <a name="determinate-progress-bars"></a>Bestimmen von Statusleisten



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Modale Statusanzeigen bestimmen</strong><br/> Geben Sie den Fortschritt eines Vorgangs an, indem Sie von links nach rechts auffüllen und vollständig ausfüllen, wenn der Vorgang abgeschlossen ist. <br/></td>
<td>Da es sich bei diesem Feedback um <a href="glossary.md">ein modales</a>Feedback handelt, können Benutzer erst dann andere Aufgaben im Fenster ausführen (oder das übergeordnete Element, wenn es in einem modalen Dialogfeld angezeigt wird), bis der Vorgang abgeschlossen ist. <br/> <img src="images/progress-bars-image3.png" alt="Screen shot of progress bar in modal window " /><br/> In diesem Beispiel gibt die Statusanzeige während der Konfiguration Feedback. <br/></td>
</tr>
<tr class="even">
<td><strong>Modales Bestimmen von Statusleisten mit einer Schaltfläche "Abbrechen" oder "Beenden"</strong><br/> Erlauben Sie Benutzern, den Vorgang anzuhalten, z. B. weil der Vorgang zu lange dauert oder sich das Warten nicht lohnt.<br/></td>
<td><img src="images/progress-bars-image4.png" alt="Screen shot of progress bar with Stop button " /><br/> In diesem Beispiel können Benutzer auf Beenden klicken, um den Vorgang anzuhalten und die Umgebung im aktuellen Zustand zu belassen.<br/></td>
</tr>
<tr class="odd">
<td><strong>Modales Bestimmen von Statusleisten mit einer Schaltfläche "Abbrechen" oder "Beenden" und animation</strong><br/> Benutzern das Anhalten des Vorgangs und das Einschließen einer Animation ermöglichen, damit Benutzer die Auswirkungen eines Vorgangs visualisieren können.<br/></td>
<td><img src="images/progress-bars-image5.png" alt="Screen shot of progress bar with animation " /><br/> In diesem Beispiel können Benutzer auf Beenden klicken, um den Vorgang anzuhalten und die Umgebung im aktuellen Zustand zu belassen.<br/></td>
</tr>
<tr class="even">
<td><strong>Modales Bestimmen von doppelten Statusleisten</strong><br/> Geben Sie den Fortschritt eines mehrstufigen Vorgangs an, indem Sie den Fortschritt des aktuellen Schritts in der ersten Statusleiste und den Gesamtfortschritt in der zweiten Leiste anzeigen.<br/></td>
<td>Da die erste Statusanzeige nur wenige zusätzliche Informationen enthält und sehr ablenkend sein kann, wird dieses Muster nicht empfohlen. Lassen Sie stattdessen alle Schritte im Vorgang einen Teil des Fortschritts gemeinsam nutzen, und lassen Sie eine einzelne Statusanzeige einmal zum Abschluss wechseln. <br/> <img src="images/progress-bars-image6.png" alt="Screen shot of current and overall progress bars " /><br/> In diesem Beispiel zeigt die erste Statusanzeige den Fortschritt des aktuellen Schritts und die zweite Statusleiste den Gesamtfortschritt an.<br/>
<blockquote>
[!Note]<br />
Dieses Muster ist in der Regel unnötig und sollte vermieden werden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Statusanzeigen ohne Modus bestimmen</strong><br/> Geben Sie den Fortschritt eines Vorgangs an, indem Sie von links nach rechts auffüllen und vollständig ausfüllen, wenn der Vorgang abgeschlossen ist.<br/></td>
<td>Im Gegensatz zu modalen Statusleisten können Benutzer andere Aufgaben ausführen, während der Vorgang ausgeführt wird. Diese Statusanzeigen können im Kontext oder auf einer Statusleiste angezeigt werden. <br/> <img src="images/progress-bars-image7.png" alt="Screen shot of progress bar on status bar " /><br/> In diesem Beispiel zeigt Windows Internet ExplorerWindows Internet Explorer den Fortschritt des Ladens einer Webseite auf der Statusleiste an. Benutzer können andere Aufgaben ausführen, während die Seite geladen wird.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="indeterminate-progress-bars"></a>Unbestimmte Statusanzeigen



|   Statusanzeigetyp  | BESCHREIBUNG             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modale unbestimmte Statusleisten**<br/> gibt an, dass ein Vorgang ausgeführt wird, indem eine Animation angezeigt wird, die kontinuierlich von links nach rechts über die Leiste schreitet. <br/>   | Wird nur für Vorgänge verwendet, deren Gesamtfortschritt nicht bestimmt werden kann, sodass keine Vollständigkeit vorliegt. Die Ermittlung von Statusanzeigen ist vorzuziehen, da sie den ungefähren Prozentsatz des abgeschlossenen Vorgangs angeben und Benutzern helfen zu ermitteln, ob der Vorgang sich lohnt, weiter zu warten. sie sind auch weniger visuell ablenkend. <br/> ![Screenshot der modalen, unbestimmten Statusanzeige](images/progress-bars-image8.png)<br/> In diesem Beispiel verwendet Windows Update eine modale unbestimmte Statusanzeige, um den Fortschritt anzugeben, während nach Updates gesucht wird.<br/> |
| **Unbestimmte Statusanzeigen ohne Modus**<br/> gibt an, dass ein Vorgang ausgeführt wird, indem eine Animation angezeigt wird, die kontinuierlich von links nach rechts über die Leiste schreitet.<br/> | Im Gegensatz zu modalen Statusleisten können Benutzer andere Aufgaben ausführen, während die Verarbeitung ausgeführt wird. Diese Statusanzeigen können im Kontext oder auf einer Statusleiste angezeigt werden. <br/> ![Screenshot der schlanken Statusanzeige im Outlook-Fenster ](images/progress-bars-image9.png)<br/> In diesem Beispiel verwendet Microsoft Outlook eine unbestimmte Statusanzeige ohne Modus, während Kontakteigenschaften ausgefüllt werden. Benutzer können das Eigenschaftenfenster weiterhin verwenden, während diese Arbeit ausgeführt wird.<br/>                                                                                                                    |



 

### <a name="meters"></a>Meter



|   Typ                                                                                       |   BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Meter**<br/> gibt einen Prozentsatz an, der nicht mit dem Fortschritt verknüpft ist. <br/> | Dieses Muster ist keine Statusanzeige, wird jedoch mithilfe des Statusanzeige-Steuerelements implementiert. Meter haben ein eindeutiges Aussehen, um sie von echten Statusleisten zu unterscheiden. <br/> ![Screenshot der Verbrauchsmessung mit freiem Speicherplatz ](images/progress-bars-image10.png)<br/> In diesem Beispiel zeigt die Verbrauchsanzeige den Prozentsatz des belegten Speicherplatzes auf dem Laufwerk an.<br/> |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Geben Sie Feedback zum Fortschritt, wenn Sie einen längeren Vorgang ausführen.** Benutzer sollten nie erraten müssen, ob Fortschritte erzielt werden.
-   **Eindeutiger Hinweis auf den tatsächlichen Fortschritt.** Die Statusleiste muss nach vorn angezeigt werden, wenn der Fortschritt erzielt wird. Wenn der Bereich der erwarteten Vervollständigungszeiten groß ist, sollten Sie erwägen, eine nicht lineare Skala zu verwenden, um den Fortschritt für längere Zeiten anzugeben. Sie möchten nicht, dass Benutzer daraus schließen, dass Ihr Programm gesperrt wurde, wenn es dies nicht ist.
-   **Eindeutiger Hinweis auf fehlenden Fortschritt.** Die Statusleiste darf nicht nach vorn angezeigt werden, wenn kein Fortschritt erfolgt. Sie möchten nicht, dass Benutzer unbegrenzt auf einen Vorgang warten, der nie abgeschlossen wird.
-   **Geben Sie nützliche Statusdetails an.** Geben Sie zusätzliche Statusinformationen an, aber nur, wenn Benutzer etwas damit tun können. Stellen Sie sicher, dass der Text lang genug angezeigt wird, damit Benutzer ihn lesen können.

    ![Screenshot der Statusleiste mit Übertragungsrate ](images/progress-bars-image11.png)

    In diesem Beispiel können Benutzer die Übertragungsrate sehen. Die niedrige Übertragungsrate deutet hier darauf hin, dass eine Netzwerkverbindung mit hoher Bandbreite verwendet werden muss.

-   **Geben Sie keine unnötigen Details an.** Im Allgemeinen sind die Details des ausgeführten Vorgangs für Benutzer nicht von Bennen. Benutzern eines Setupprogramms ist es beispielsweise nicht wichtig, dass die spezifische Datei kopiert wird oder dass Systemkomponenten registriert werden, da sie keine Erwartungen an diese Details haben. In der Regel stellt eine gut beschriftete Statusleiste allein ausreichende Informationen zur Verfügung. Geben Sie daher nur dann zusätzliche Statusinformationen an, wenn Benutzer damit etwas tun können. Das Bereitstellen von Details, die Benutzern egal sind, macht die Benutzererfahrung zu kompliziert und technisch. Wenn Sie ausführlichere Informationen zum Debuggen benötigen, sollten Sie sie nicht in Release builds anzeigen.

    **Richtig:**

    ![Screenshot des Installationsfortschritts ](images/progress-bars-image12.png)

    In diesem Beispiel ist nur die Statusleiste mit der Bezeichnung erforderlich.

    **Richtig:**

    ![Screenshot der Statusleiste mit Übertragungsrate ](images/progress-bars-image11.png)

    In diesem Beispiel kopiert Windows-Explorer dateien, die der Benutzer ausgewählt hat. Daher ist es sinnvoll, die kopierten Dateinamen anzuzeigen.

    **Falsch:**

    ![Screenshot des Fortschritts der Registrierung ](images/progress-bars-image13.png)

    In diesem Beispiel stellt ein Setupprogramm Details zur Verfügung, die für den Benutzer bedeutungslos sind.

-   **Stellen Sie nützliche Animationen zur Verfügung.** Wenn dies gut funktioniert, verbessern Animationen die Benutzerfreundlichkeit, indem sie Benutzern helfen, den Vorgang zu visualisieren. Gute Animationen haben mehr Auswirkungen als Text allein. Die Statusanzeige für den Outlook Delete-Befehl zeigt z. B. die Papierkorb für das Ziel an, wenn die Dateien wiederhergestellt werden können, aber keine Papierkorb, wenn die Dateien nicht wiederhergestellt werden können.

    ![Screenshot des Fortschritts der Löschung ](images/progress-bars-image14.png)

    In diesem Beispiel verstärkt das Fehlen Papierkorb, dass die Dateien dauerhaft gelöscht werden. Diese zusätzlichen Informationen würden nicht als effektiv mithilfe von Text allein kommuniziert werden.

-   **Verwenden Sie keine unnötigen Animationen.** Animationen können irreführend sein, da sie in der Regel in einem separaten Thread von der eigentlichen Aufgabe ausgeführt werden und daher den Fortschritt auch dann vorschlagen können, wenn der Vorgang gesperrt wurde. Wenn der Vorgang langsamer als erwartet ist, gehen Benutzer manchmal davon aus, dass die Animation Teil des Grunds ist. Verwenden Sie daher nur Animationen, wenn eine klare Begründung vor liegt. verwenden Sie sie nicht, um zu versuchen, Benutzer zu besingen.
-   **Positionieren Sie Animationen zentriert über der Statusleiste.** Setzen Sie die Animation über die Statusleistenbeschriftungen, falls sie eine haben. Wenn rechts von der Statusleiste die Schaltfläche Abbrechen oder Beenden angezeigt wird, schließen Sie die Schaltfläche ein, wenn Sie die Mitte bestimmen.
-   **Wiedergabe eines Soundeffekts nach Abschluss eines Vorgangs nur, wenn er sehr lang (länger als zwei Minuten), selten und wichtig ist.** Wenn der Benutzer wahrscheinlich von einem wichtigen Vorgang während der Verarbeitung entfernt wird, wird die Aufmerksamkeit des Benutzers durch einen Soundeffekt wiederhergestellt. Die Verwendung eines Soundeffekts nach Abschluss in anderen Fällen wäre eine ablenkende Verärgerung.
-   **Stehlen Sie den Eingabefokus nicht, um ein Fortschrittsupdate oder einen Abschluss zu zeigen.** Benutzer wechseln häufig zu anderen Programmen, während sie warten, und möchten nicht unterbrochen werden. Hintergrundaufgaben müssen im Hintergrund bleiben.
-   **Machen Sie sich keine Gedanken über den technischen Support.** Da das feedback der Statusleisten nicht unbedingt genau und flüchtig ist, sind Statusleisten kein guter Mechanismus zum Bereitstellen von Informationen für den technischen Support. Wenn der Vorgang fehlschlagen kann (wie bei einem Setupprogramm), sollten Sie daher keine zusätzlichen Statusinformationen bereitstellen, die nur für den technischen Support nützlich sind. Stellen Sie stattdessen einen alternativen Mechanismus wie eine Protokolldatei zum Aufzeichnen von Technischen Supportinformationen zur Verfügung.

    **Falsch:**

    ![Screenshot der Statusleiste mit dem Servernamen ](images/progress-bars-image15.png)

    In diesem Beispiel zeigt die Statusleiste Details für den technischen Support an.

-   **Setzen Sie den Prozentsatz nicht vollständig oder einen anderen Text auf eine Statusleiste.** Auf diesen Text kann nicht zugegriffen werden und ist nicht kompatibel mit der Verwendung von Designs.

    **Falsch:**

    ![Screenshot der Statusleiste mit Text auf der Leiste ](images/progress-bars-image16.png)

    In diesem Beispiel kann nicht auf den Prozenttext auf der Statusleiste zugegriffen werden.

-   **Kombinieren Sie keine Statusleiste mit einem ausgelastet-Zeiger.** Verwenden Sie das eine oder das andere, aber nicht beide gleichzeitig.
-   **Verwenden Sie keine vertikalen Statusleisten.** Horizontale Statusleisten verfügen über eine natürlichere Zuordnung und einen besseren Fluss.

### <a name="determinate-progress-bars"></a>Bestimmen von Statusleisten

-   **Verwenden Sie bestimmte Statusleisten für Vorgänge,** die eine bestimmte Zeit benötigen, auch wenn diese Zeit nicht genau vorhergesagt werden kann. Unbestimmte Statusleisten zeigen an, dass Fortschritt erzielt wird, geben aber keine weiteren Informationen an. Wählen Sie keine unbestimmte Statusleiste nur basierend auf der möglichen fehlenden Genauigkeit aus.
-   **Geben Sie die Fortschrittsphase eindeutig an.** Die Statusleiste muss angeben können, ob sich der Vorgang am Anfang, in der Mitte oder am Ende eines Vorgangs befindet. Statusleisten, die sofort zu 99 Prozent vervollständigt werden und dann für einen längeren Zeitraum dort bleiben, sind beispielsweise besonders uninformativ und lästig. In diesen Fällen sollte die Statusleiste anfänglich auf mindestens 33 Prozent festgelegt werden, um anzugeben, dass sich der Vorgang noch in der Anfangsphase befindet.
-   **Geben Sie die Vervollständigung eindeutig an.** Lassen Sie eine Statusleiste nicht zu 100 Prozent wechseln, es sei denn, der Vorgang wurde abgeschlossen.
-   **Geben Sie eine Schätzung der verbleibenden Zeit an, wenn Sie dies genau tun können.** Die verbleibenden Schätzungen, die genau sind, sind nützlich, aber Schätzungen, die weit von der Markierung abweichen oder erheblich springen, sind nicht hilfreich. Möglicherweise müssen Sie einige Verarbeitungen durchführen, bevor Sie genaue Schätzungen treffen können. Wenn dies der Fall ist, sollten Sie während dieses anfänglichen Zeitraums keine potenziell ungenauen Schätzungen anzeigen.
-   **Starten Sie den Fortschritt nicht neu.** Eine Statusleiste verliert ihren Wert, wenn sie neu gestartet wird (z. B. weil ein Schritt des Vorgangs abgeschlossen wird), da Benutzer nicht wissen können, wann der Vorgang abgeschlossen wird. Lassen Sie stattdessen alle Schritte im Vorgang einen Teil des Fortschritts gemeinsam nutzen, und lassen Sie die Statusleiste einmal zum Abschluss wechseln.

    **Falsch:**

    ![Screenshot der Statusleiste, die neu gestartet wurde ](images/progress-bars-image17.png)

    In diesem Beispiel wurde der Vorgang in den Schritt zum Kopieren von Dateien verschoben und die Statusleiste für diesen Schritt zurückgesetzt. Benutzer haben jetzt keine Vorstellung davon, wie viel Fortschritt erzielt wurde oder wie viel Zeit übrig bleibt.

-   **Sichern Sie den Fortschritt nicht.** Wie bei einem Neustart verliert eine Statusleiste ihren Wert, wenn sie sichern. Erhöhen Sie den Fortschritt immer monoton. Sie können jedoch über eine verbleibende Zeitschätzung verfügen, die sich erhöht (und verringert), da die Fortschrittsrate variieren kann.

### <a name="indeterminate-progress-bars"></a>Unbestimmte Statusleisten

-   **Verwenden Sie unbestimmte Statusleisten nur für Vorgänge, deren Gesamtfortschritt nicht bestimmt werden kann.** Verwenden Sie unbestimmte Statusleisten für Vorgänge, die eine ungebundene Zeit benötigen oder auf eine unbekannte Anzahl von Objekten zugreifen. Verwenden Sie Timeouts, um zeitbasierten Vorgängen Grenzen zu geben.
-   **Konvertieren Sie in eine bestimmte Statusleiste, sobald der Gesamtfortschritt ermittelt werden kann.** Wenn es beispielsweise deutlich länger als zwei Sekunden dauert, die Anzahl der Objekte zu bestimmen, können Sie eine unbestimmte Statusleiste verwenden, während die Objekte gezählt werden, und dann in eine bestimmte Statusleiste konvertieren.
-   **Kombinieren Sie keine unbestimmten Statusleisten mit geschätzten Gesamt- oder Zeitschätzungen in Prozent.** Wenn Sie diese Informationen bereitstellen können, verwenden Sie stattdessen eine bestimmte Statusleiste.
-   **Kombinieren Sie keine unbestimmten Statusleisten mit Animationen.** Eine unbestimmte Statusleiste ist praktisch eine generische Animation, daher sollten Sie die eine oder die andere, aber nie beide verwenden.

    **Richtig:**

    ![Screenshot des Fortschritts beim Erkennen des Servers ](images/progress-bars-image18.png)

    In diesem Beispiel wird nur eine Animation verwendet, um zu zeigen, dass ein Vorgang gerade durchgeführt wird.

### <a name="modeless-progress-bars"></a>Statusleisten ohne Modus

-   **Wenn Benutzer während des Vorgangs produktiv arbeiten können, geben Sie kein Feedback.** Möglicherweise müssen Sie eine Teilmenge der Funktionen deaktivieren, für die der Vorgang abgeschlossen werden muss.
-   **Wenn das Fenster über eine Adressleiste verfügt, zeigen Sie den statuslosen Status in der Adressleiste an.**

    ![Screenshot der Statusleiste als Teil der Adressleiste ](images/progress-bars-image19.png)

    In diesem Beispiel wird der statuslose Status in der Adressleiste angezeigt.

-   Andernfalls wird der statuslose Status **in der Statusleiste angezeigt,** wenn das Fenster über eine Statusleiste verfügt. Legen Sie den entsprechenden Text links in der Statusleiste ab.

    ![Screenshot der Statusleiste als Teil der Statusleiste ](images/progress-bars-image7.png)

    In diesem Beispiel wird der statuslose Fortschritt in der Statusleiste angezeigt.

### <a name="modal-progress-bars"></a>Modale Statusleisten

-   **Platzieren Sie modale Statusleisten auf Statusseiten oder** [Statusdialogfeldern.](win-dialog-box.md)
-   **Geben Sie eine Befehlsschaltfläche an, um den Vorgang anzuhalten, wenn er mehr als einige Sekunden dauert oder das Potenzial hat, nie abgeschlossen zu werden.** Beschriften Sie die Schaltfläche Abbrechen, wenn der Abbricht den vorherigen Zustand der Umgebung zurückgibt (ohne Nebenwirkungen). Beschriften Sie andernfalls die Schaltfläche Beenden, um anzugeben, dass der teilweise abgeschlossene Vorgang intakt bleibt. Sie können die Schaltflächenbezeichnung in der Mitte des Vorgangs von Abbrechen in Beenden ändern, wenn es zu einem bestimmten Zeitpunkt nicht möglich ist, die Umgebung in ihren vorherigen Zustand zurück zu bringen. Zentrieren Sie die Befehlsschaltfläche vertikal mit der Statusleiste, anstatt ihre oberen Seiten auszurichten.

    **Richtig:**

    ![Screenshot des Status des Wartens auf das Netzwerk ](images/progress-bars-image20.png)

    In diesem Beispiel hat das Anhalten der Netzwerkverbindung keine Nebeneffekt, sodass Abbrechen verwendet wird.

    **Richtig:**

    ![Screenshot der Statusleiste mit linker Kopierzeit ](images/progress-bars-image21.png)

    In diesem Beispiel bleiben beim Anhalten der Kopie alle kopierten Dateien erhalten, sodass die Befehlsschaltfläche mit Stop (Beenden) bezeichnet wird.

    **Falsch:**

    ![Screenshot der Suchfortschrittsleiste und Schaltfläche "Beenden" ](images/progress-bars-image22.png)

    In diesem Beispiel hat das Anhalten der Suche keinen Nebeneffekt, sodass die Befehlsschaltfläche mit Abbrechen bezeichnet werden sollte.

### <a name="time-remaining"></a>Verbleibende Zeit

Für bestimmte Statusleisten:

-   **Verwenden Sie die folgenden Zeitformate.** Beginnen Sie mit dem ersten der folgenden Formate, bei denen die größte Zeiteinheit nicht 0 (null) ist, und wechseln Sie dann zum nächsten Format, sobald die größte Zeiteinheit 0 (null) wird.

    **Für Statusleisten:**

    **Wenn verwandte Informationen in einem Doppelpunktformat angezeigt werden:**

    Verbleibende Zeit: h Stunden, m Minuten

    Verbleibende Zeit: m Minuten, s Sekunden

    Verbleibende Zeit: s Sekunden

    **Wenn der Bildschirmbereich premium ist:**

    h hrs, m mins remaining

    m mins, s secs remaining

    verbleibende Sekunden

    **Andernfalls:**

    h Stunden, verbleibende m Minuten

    m Minuten, verbleibende Sekunden

    verbleibende Sekunden

    **Für Titelleisten:**

    hh:mm remaining

    mm:ss verbleibende

    Verbleibende 0:ss

    In diesem kompakten Format werden zuerst die wichtigsten Informationen angezeigt, damit sie nicht auf der Taskleiste abgeschnitten werden.

-   **Machen Sie Schätzungen präzise, aber geben Sie keine falsche Genauigkeit.** Wenn die größte Einheit Stunden ist, geben Sie Minuten an (sofern sinnvoll), aber keine Sekunden.

    **Falsch:**

    hh hours, mm minutes, ss seconds

-   **Halten Sie die Schätzung auf dem neuesten Stand.** Die verbleibende Zeit wird mindestens alle 5 Sekunden aktualisiert.
-   **Konzentrieren Sie sich auf die verbleibende Zeit,** da dies die Informationen sind, die benutzern am wichtigsten sind. Geben Sie die gesamte verstrichene Zeit nur dann an, wenn es Szenarien gibt, in denen verstrichene Zeit hilfreich ist (z. B. wenn die Aufgabe wahrscheinlich wiederholt wird). Wenn die verbleibende Zeitschätzung einer Statusleiste zugeordnet ist, sollten Sie keinen vollständigen Prozenttext haben, da diese Informationen von der Statusleiste selbst übermittelt werden.
-   **Grammatikalisch korrekt sein.** Verwenden Sie Singulareinheiten, wenn die Zahl eins ist.

    **Falsch:**

    1 Minuten, 1 Sekunde

-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**

### <a name="progress-bar-colors"></a>Statusleistenfarben

-   **Verwenden Sie rote oder gelbe Statusleisten nur, um den Status anzugeben, nicht die Endergebnisse einer Aufgabe.** Eine rote oder gelbe Statusleiste gibt an, dass Benutzer eine Aktion ergreifen müssen, um die Aufgabe auszuführen. Wenn die Bedingung nicht wiederhergestellt werden kann, lassen Sie die Statusanzeige grün, und zeigen Sie eine Fehlermeldung an.
-   **Aktivieren Sie die Statusleiste rot, wenn eine vom Benutzer wiederherstellbare Bedingung vorstellbar ist, die weitere Fortschritte verhindert.** Zeigen Sie eine Meldung an, um das Problem zu erläutern und eine Lösung zu empfehlen.
-    Aktivieren Sie die Statusleiste gelb, um anzugeben, dass der Benutzer die Aufgabe angehalten hat oder dass eine Bedingung vorgelegen hat, die den Fortschritt eintut, aber der Fortschritt weiterhin stattfindet (z. B. bei schlechter Netzwerkkonnektivität). Wenn der Benutzer angehalten hat, ändern Sie die Bezeichnung der Schaltfläche Anhalten in Fortsetzen. Wenn der Fortschritt beeinträchtigt wird, zeigen Sie eine Meldung an, um das Problem zu erläutern und eine Lösung zu empfehlen.

### <a name="meters"></a>Meter

-   **Verwenden Sie Statusleisten nur für den Fortschritt.** Verwenden Sie Meter, um Prozentsätze anzugeben, die sich nicht auf den Fortschritt bezogen haben.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstand

![Diagramm: Größen- und Abstandsdiagramm der Statusleiste ](images/progress-bars-image23.png)

Empfohlene Größe und Abstand für Statusleisten.

-   Verwenden Sie immer die empfohlene Statusleistenhöhe.
    -   **Ausnahme:** Sie können eine andere Höhe verwenden, wenn das übergeordnete Fenster die empfohlene Höhe nicht unterstützt.
-   Verwenden Sie die Mindestbreite, wenn Sie die Statusleiste unaufdringlich machen möchten.
-   Verwenden Sie keine Breiten, die länger als das empfohlene Maximum sind. Die Statusleiste muss den verfügbaren Platz nicht ausfüllen.
-   Zentriert die Statusleiste horizontal, wenn das Fenster viel breiter als die maximal empfohlene Breite ist.

## <a name="labels"></a>Bezeichnungen

### <a name="progress-bar-labels"></a>Statusleistenbezeichnungen

-   **Verwenden Sie eine präzise Bezeichnung mit einem statischen Textsteuerfeld, um anzugeben, was der Vorgang tut.** Starten Sie die Bezeichnung mit einem Verb (z. B. Kopieren), und enden Sie mit auslassungszeichen. Diese Bezeichnung kann sich dynamisch ändern, wenn der Vorgang mehrere Schritte auf sich hat oder mehrere Objekte verarbeitet.
-   Weisen Sie keinen eindeutigen [Zugriffsschlüssel zu,](glossary.md) da das Steuerelement nicht interaktiv ist.
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   Wenn der Vorgang nicht direkt vom Benutzer initiiert wurde, können Sie eine zusätzliche Bezeichnung für den Kontext enthalten und sich für die Unterbrechung entlogen. Beginnen Sie diese zusätzliche Bezeichnung mit dem Ausdruck Bitte warten Sie, während. Diese Bezeichnung sollte sich während des Vorgangs nicht ändern.

    ![Screenshot der Statusleiste mit Bezeichnung ](images/progress-bars-image24.png)

    In diesem Beispiel wird der Benutzer aufgefordert, zu warten, da der Benutzer den Vorgang nicht direkt initiiert hat.

-   Positionieren Sie die Bezeichnung über der Statusleiste, und richten Sie die Bezeichnung am linken Rand der Statusleiste aus.

### <a name="progress-bar-details"></a>Statusleistendetails

-   Geben Sie Details in statischem Text an, und stellen Sie den Daten eine Bezeichnung voran, die auf einen Doppelpunkt endet. Geben Sie einheiten (Sekunden, Kilobytes und so weiter) nach dem Detailtext an.

    **Richtig:**

    ![Screenshot der Statusleiste mit Übertragungsrate ](images/progress-bars-image11.png)

    In diesem Beispiel sind die Details ordnungsgemäß gekennzeichnet.

    **Falsch:**

    ![Screenshot der Statusleiste ohne richtige Bezeichnung ](images/progress-bars-image25.png)

    In diesem Beispiel werden die Details nicht bezeichnet, sodass Benutzer ihre Bedeutung bestimmen müssen.

-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   Positionieren Sie die Details unterhalb der Statusleiste, und richten Sie die Bezeichnung am linken Rand der Statusleiste aus.
-   Geben Sie den prozentsatz abgeschlossenen oder verbleibenden Prozentsatz nicht an, da diese Informationen von der Statusleiste selbst übermittelt werden.

### <a name="cancel-button"></a>Schaltfläche „Abbrechen“

-   Beschriften Sie die Schaltfläche Abbrechen, wenn der Abbricht den vorherigen Zustand der Umgebung zurückgibt (ohne Nebeneffekt). Beschriften Sie andernfalls die Schaltfläche Beenden, um anzugeben, dass der teilweise abgeschlossene Vorgang intakt bleibt.
-   Sie können die Schaltflächenbezeichnung in der Mitte des Vorgangs von Abbrechen in Beenden ändern, wenn es zu einem bestimmten Zeitpunkt nicht möglich ist, die Umgebung in den vorherigen Zustand zurück zu bringen.

### <a name="progress-dialog-box-titles"></a>Titel des Statusdialogfelds

-   Wenn die Statusanzeige in einem modalen Dialogfeld angezeigt wird, sollte der Titel des Dialogfelds der Name des Programms oder der Name des Vorgangs sein. Verwenden Sie nicht, was die Statusleistenbezeichnung für den Titel des Dialogfelds sein sollte.

    **Richtig:**

    ![Screenshot des Statusleistentitels mit Aufgabenname ](images/progress-bars-image26.png)

    In diesem Beispiel wird der Aufgabenname für den Titel des Dialogfelds verwendet.

    **Falsch:**

    ![Screenshot des redundanten Dialogfeldtitels ](images/progress-bars-image27.png)

    In diesem Beispiel ist der Titeltext des Dialogfelds eine Neuform der Statusleistenbezeichnung. Stattdessen sollte der Programmname verwendet werden.

-   Wenn die Statusanzeige in einem nicht moduslosen Dialogfeld angezeigt wird, optimieren Sie den Titel für die Anzeige auf der Taskleiste, indem Sie die unterscheidenden Informationen präzise an erster Stelle platzieren. Beispiel: "66 % abgeschlossen".

 

