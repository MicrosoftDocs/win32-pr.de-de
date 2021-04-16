---
title: Status anzeigen
description: Bei einer Statusanzeige können Benutzer den Fortschritt eines langwierigen Vorgangs verfolgen. In einer Statusanzeige kann entweder der ungefähre Prozentsatz des Abschlusses (determinate) angezeigt werden, oder es wird angegeben, dass ein Vorgang ausgeführt wird (unbestimmt).
ms.assetid: 067961fa-2fb1-4cd1-99a4-cbe2244c3913
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: db8aca7300b309fb6929106cf97329956b7accb0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104566682"
---
# <a name="progress-bars"></a>Status anzeigen

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Bei einer Statusanzeige können Benutzer den Fortschritt eines langwierigen Vorgangs verfolgen. In einer Statusanzeige kann entweder der ungefähre Prozentsatz des Abschlusses (determinate) angezeigt werden, oder es wird angegeben, dass ein Vorgang ausgeführt wird (unbestimmt).

Benutzerfreundlichkeit hat ergeben, dass Benutzer die Antwortzeiten von über eine Sekunde kennen. Folglich sollten Sie Vorgänge in Erwägung ziehen, die zwei Sekunden oder länger dauern, bis Sie lange dauern und einen gewissen Typ von Fortschritts Feedback benötigen.

![Screenshot einer typischen Statusanzeige ](images/progress-bars-image1.png)

Eine typische Statusanzeige.

> [!Note]  
> Richtlinien für das [Layout](vis-layout.md) werden in einem separaten Artikel dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird der Vorgang in ungefähr fünf Sekunden oder weniger ausgeführt?** Wenn dies der Fall ist, verwenden Sie stattdessen einen [Aktivitätsindikator](inter-mouse.md) , da das Anzeigen einer Statusanzeige für eine kurze Dauer ablenkend wäre. Wenn der Vorgang in der Regel fünf Sekunden oder weniger dauert, aber mitunter mehr Zeit in Anspruch nimmt, beginnen Sie mit einem ausgelasteten Zeiger und konvertieren Sie nach fünf Sekunden in eine Statusanzeige.
-   **Ist eine unbestimmende Statusanzeige, mit der gewartet wird, bis der Benutzer eine Aufgabe abgeschlossen hat?** Wenn ja, zeigen Sie keine Statusleiste an. Statusleisten sind für den Status des Computers gedacht, nicht für den der Benutzer.
-   **Ist eine unbeendete Statusanzeige in Kombination mit einer Animation?** Wenn dies der Fall ist, verwenden Sie stattdessen nur die Animation. Bei der unbestimmten Statusanzeige handelt es sich um eine generische Animation, die der Animation keinen Wert hinzufügt.
-   **Handelt es sich bei dem Vorgang um einen sehr langen Hintergrund Task (länger als zwei Minuten), für den Benutzer eher an der Beendigung als der Fortschritt interessiert sind?** Wenn dies der Fall ist, verwenden Sie stattdessen eine [Benachrichtigung](mess-notif.md) . In diesem Fall führen Benutzer in der Zwischenzeit andere Aufgaben aus, die den Fortschritt nicht überwachen. Durch die Verwendung einer Benachrichtigung können Benutzer andere Aufgaben ohne Unterbrechung ausführen. Beispiele für solche langen Vorgänge sind z. b. Druck-, Sicherungs-, System Scans und Massendaten Übertragungen oder-Konvertierungen.
-   **Wenn der Vorgang beendet ist, können Benutzer die Ergebnisse wiedergeben?** Wenn ja, verwenden Sie stattdessen einen Schieberegler. Beispiele für solche Vorgänge sind Video-und Audioaufzeichnung und-Wiedergabe.

    ![Screenshot von Medien Player und Schieberegler ](images/progress-bars-image2.png)

    In diesem Beispiel wird ein Schieberegler verwendet, um den Fortschritt bei der Wiedergabe von Sound anzugeben. Dies ermöglicht es den Benutzern, die Ergebnisse später wiederzugeben.

## <a name="design-concepts"></a>Entwurfskonzepte

Bei längerer Ausführung benötigen Benutzer eine allgemeine Vorstellung davon, was der Vorgang ausführt. Außerdem müssen Sie Folgendes wissen:

-   Ein langwieriger Vorgang wurde gestartet.
-   Der Fortschritt wird vorgenommen, und der Vorgang wird schließlich abgeschlossen (und ist daher noch nicht gesperrt).
-   Der ungefähre Prozentsatz des Vorgangs, der abgeschlossen wurde (und somit der verbleibende Prozentsatz).
-   , Wenn der Vorgang abgebrochen werden soll, wenn der Warte Vorgang nicht fortgesetzt werden soll.
-   , Wenn der Vorgang fortgesetzt werden soll, während der Vorgang abgeschlossen wird.

**Verwenden Sie bestimmte-Status leisten für Vorgänge, die einen begrenzten Zeitraum erfordern,** auch wenn diese Zeitspanne nicht genau vorhergesagt werden kann. Unbestimmt Status leisten zeigen an, dass der Fortschritt ausgeführt wird, aber keine weiteren Informationen bereitgestellt werden. Wählen Sie nicht nur basierend auf dem möglichen Mangel an Genauigkeit eine unbestimmte Statusanzeige aus.

Angenommen, ein Vorgang erfordert fünf Schritte, und jeder dieser Schritte erfordert einen begrenzten Zeitraum, aber der Zeitaufwand für jeden Schritt kann stark variieren. Verwenden Sie in diesem Fall eine bestimmte-Statusanzeige, und zeigen Sie den Fortschritt an, wenn jeder Schritt proportional zu dem Zeitraum abgeschlossen ist, den jeder Schritt normalerweise benötigt. Verwenden Sie eine unbestimmte Statusanzeige nur dann, wenn die Statusanzeige für den Benutzer fälschlicherweise beendet werden würde, dass der Vorgang gesperrt wurde.

**Wenn Sie nur eine Aktion ausführen...**

Stellen Sie sicher, dass Sie Fortschritts Feedback für lange Vorgänge bereitstellen und dass die obigen Informationen eindeutig kommuniziert werden. Verwenden Sie nach Möglichkeit die bestimmte von Status leisten.

## <a name="usage-patterns"></a>Verwendungsmuster

Status leisten weisen mehrere Verwendungs Muster auf:

### <a name="determinate-progress-bars"></a>Determinate von Status leisten



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Modale bestimmte-Status leisten</strong><br/> Geben Sie den Fortschritt eines Vorgangs an, indem Sie von links nach rechts auffüllen und vollständig ausfüllen, wenn der Vorgang abgeschlossen ist. <br/></td>
<td>Da es sich um ein <a href="glossary.md">modales</a>Feedback handelt, können Benutzer keine anderen Aufgaben im Fenster (oder das übergeordnete Element, wenn Sie in einem modalen Dialogfeld angezeigt werden) ausführen, bis der Vorgang beendet ist. <br/> <img src="images/progress-bars-image3.png" alt="Screen shot of progress bar in modal window " /><br/> In diesem Beispiel gibt die Statusanzeige während der Konfiguration Feedback. <br/></td>
</tr>
<tr class="even">
<td><strong>Modale bestimmte von Status leisten mit der Schaltfläche Abbrechen oder beenden</strong><br/> Erlauben Sie Benutzern, den Vorgang anzuhalten, weil der Vorgang möglicherweise zu lange dauert oder die Wartezeit nicht lohnt.<br/></td>
<td><img src="images/progress-bars-image4.png" alt="Screen shot of progress bar with Stop button " /><br/> In diesem Beispiel können Benutzer auf Beenden klicken, um den Vorgang anzuhalten und die Umgebung in Ihrem aktuellen Zustand zu belassen.<br/></td>
</tr>
<tr class="odd">
<td><strong>Modale bestimmte von Status leisten mit einer Schaltfläche zum Abbrechen oder beenden und Animation</strong><br/> Erlauben Sie Benutzern, den Vorgang anzuhalten, und schließen Sie eine Animation ein, damit Benutzer die Auswirkungen eines Vorgangs visualisieren können.<br/></td>
<td><img src="images/progress-bars-image5.png" alt="Screen shot of progress bar with animation " /><br/> In diesem Beispiel können Benutzer auf Beenden klicken, um den Vorgang anzuhalten und die Umgebung in Ihrem aktuellen Zustand zu belassen.<br/></td>
</tr>
<tr class="even">
<td><strong>Über modale bestimmte doppelte Status leisten</strong><br/> Geben Sie den Fortschritt eines mehrstufigen Vorgangs an, indem Sie den Status des aktuellen Schritts in der ersten Statusanzeige und den Gesamtstatus in der zweiten Leiste anzeigen.<br/></td>
<td>Da in der ersten Statusanzeige wenig zusätzliche Informationen enthalten sind, wird dieses Muster nicht empfohlen. Nehmen Sie stattdessen an, dass alle Schritte des Vorgangs einen Teil des Fortschritts aufweisen und eine einzelne Statusanzeige einmal abgeschlossen wird. <br/> <img src="images/progress-bars-image6.png" alt="Screen shot of current and overall progress bars " /><br/> In diesem Beispiel wird in der ersten Statusanzeige der Fortschritt des aktuellen Schritts und in der zweiten Statusanzeige der Gesamtstatus angezeigt.<br/>
<blockquote>
[!Note]<br />
Dieses Muster ist in der Regel unnötig und sollte vermieden werden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Status leisten mit nicht modalem determiness</strong><br/> Geben Sie den Fortschritt eines Vorgangs an, indem Sie von links nach rechts auffüllen und vollständig ausfüllen, wenn der Vorgang abgeschlossen ist.<br/></td>
<td>Anders als bei modalen Status leisten können Benutzer andere Aufgaben ausführen, während der Vorgang ausgeführt wird. Diese Status leisten können im Kontext oder auf einer Statusleiste angezeigt werden. <br/> <img src="images/progress-bars-image7.png" alt="Screen shot of progress bar on status bar " /><br/> In diesem Beispiel zeigt Windows Internet ExplorerWindows Internet Explorer seinen Fortschritt beim Laden einer Webseite auf der Statusleiste an. Benutzer können andere Aufgaben ausführen, während die Seite geladen wird.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="indeterminate-progress-bars"></a>Unbestimmte Status leisten



|                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modale unbestimmte Status anzeigen**<br/> Geben Sie an, dass ein Vorgang ausgeführt wird, indem Sie eine Animation anzeigen, die fortlaufend zwischen den Balken von links nach rechts durchläuft. <br/>   | Wird nur für Vorgänge verwendet, deren gesamter Fortschritt nicht bestimmt werden kann. Daher gibt es keinen Grund für Vollständigkeit. die bestimmte von Status leisten sind vorzuziehen, da Sie den ungefähren Prozentsatz des Vorgangs angeben, der abgeschlossen wurde, und Benutzern dabei helfen, zu bestimmen, ob der Vorgang weiterhin gewartet werden sollte. Sie sind auch weniger visuell stark ablenkend. <br/> ![Screenshot der modalen, unbestimmten Statusanzeige](images/progress-bars-image8.png)<br/> In diesem Beispiel verwendet Windows Update eine modale, unbeendete Statusanzeige, um den Fortschritt während der Suche nach Updates anzuzeigen.<br/> |
| **Unbeendete, unbeendete Status leisten**<br/> Geben Sie an, dass ein Vorgang ausgeführt wird, indem Sie eine Animation anzeigen, die fortlaufend zwischen den Balken von links nach rechts durchläuft.<br/> | Im Gegensatz zu modalen Status leisten können Benutzer andere Aufgaben ausführen, während die Verarbeitung ausgeführt wird. Diese Status leisten können im Kontext oder auf einer Statusleiste angezeigt werden. <br/> ![Screenshot der dünnen Statusanzeige im Outlook-Fenster ](images/progress-bars-image9.png)<br/> In diesem Beispiel verwendet Microsoft Outlook beim Ausfüllen der Kontakt Eigenschaften eine unbeendete, unbeendete Statusanzeige. Benutzer können weiterhin das Eigenschaften Fenster verwenden, während diese Arbeit ausgeführt wird.<br/>                                                                                                                    |



 

### <a name="meters"></a>Meter



|                                                                                          |                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Meter**<br/> Geben Sie einen Prozentsatz an, der nicht mit dem Status verknüpft ist. <br/> | Dieses Muster ist keine Statusanzeige, wird jedoch mit dem Statusanzeige-Steuerelement implementiert. Zähler haben eine eindeutige Anzeige, um Sie von echten Status leisten zu unterscheiden. <br/> ![Screenshot der Verbrauchseinheit, die den freien Speicherplatz anzeigt ](images/progress-bars-image10.png)<br/> In diesem Beispiel zeigt die Verbrauchseinheit den Prozentsatz des verwendeten Festplatten Speicherplatzes.<br/> |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Geben Sie bei längerer Ausführung Fortschritts Feedback an.** Benutzer sollten nie erraten, ob der Fortschritt ausgeführt wird.
-   **Geben Sie einen echten Fortschritt an.** Die Statusanzeige muss fortgesetzt werden, wenn der Fortschritt ausgeführt wird. Wenn der Bereich der erwarteten Abschlusszeiten groß ist, sollten Sie die Verwendung einer nichtlinearen Skala in Erwägung gezogen, um den Fortschritt für längere Zeit anzugeben. Sie möchten nicht, dass die Benutzer die Sperre des Programms abschließen, wenn dies nicht der Fall ist.
-   **Gibt eindeutig an, dass der Fortschritt fehlt.** Die Statusanzeige darf nicht fortgesetzt werden, wenn kein Fortschritt ausgeführt wird. Sie möchten nicht, dass Benutzer unbegrenzt auf einen Vorgang warten, der nie ausgeführt wird.
-   **Geben Sie nützliche Fortschritts Details an.** Geben Sie zusätzliche Statusinformationen an, aber nur, wenn die Benutzer etwas damit tun können. Stellen Sie sicher, dass der Text so lange angezeigt wird, dass er von Benutzern gelesen werden kann.

    ![Screenshot der Statusanzeige mit der Übertragungsrate ](images/progress-bars-image11.png)

    In diesem Beispiel können Benutzer die Übertragungsrate sehen. Die niedrige Übertragungsrate hier deutet darauf hin, dass eine Netzwerkverbindung mit hoher Bandbreite verwendet werden muss.

-   **Stellen Sie keine unnötigen Details bereit.** Im Allgemeinen sind die Details des Vorgangs, der ausgeführt wird, für die Benutzer nicht relevant. Beispielsweise ist es für Benutzer eines Setup Programms nicht wichtig, dass die bestimmte Datei kopiert wird oder dass Systemkomponenten registriert werden, da Sie keine Erwartungen an diese Details haben. In der Regel stellt eine gut bezeichnete Statusanzeige allein ausreichend Informationen bereit. Geben Sie daher nur dann zusätzliche Statusinformationen an, wenn Benutzer etwas mit der Funktion ausführen können. Die Angabe von Details, die Benutzern nicht wichtig sind, macht die Benutzer Arbeit übermäßig kompliziert und technisch. Wenn Sie ausführlichere Informationen zum Debuggen benötigen, können Sie es nicht in Releasebuilds anzeigen.

    **Richtig:**

    ![Screenshot des Installations Fortschritts ](images/progress-bars-image12.png)

    In diesem Beispiel ist nur die Statusanzeige mit der Bezeichnung erforderlich.

    **Richtig:**

    ![Screenshot der Statusanzeige mit der Übertragungsrate ](images/progress-bars-image11.png)

    In diesem Beispiel kopiert Windows Explorer Dateien, die der Benutzer ausgewählt hat, sodass das Anzeigen der kopierten Dateinamen sinnvoll ist.

    **Falsch:**

    ![Screenshot des Status der Registrierung ](images/progress-bars-image13.png)

    In diesem Beispiel stellt ein Setup Programm Details bereit, die für den Benutzer bedeutungslos sind.

-   **Stellen Sie hilfreiche Animationen bereit.** Wenn alles richtig ist, verbessern Animationen die Benutzer Leistung, indem Sie Benutzern dabei helfen, den Vorgang visuell darzustellen. Gute Animationen haben mehr Auswirkungen als nur Text. Beispielsweise zeigt die Statusanzeige für den Outlook DELETE-Befehl den Papierkorb für das Ziel an, wenn die Dateien wieder hergestellt werden können, aber keinen Papierkorb, wenn die Dateien nicht wieder hergestellt werden können.

    ![Screenshot des Lösch Status ](images/progress-bars-image14.png)

    In diesem Beispiel verstärkt der Mangel an Papierkorb, dass die Dateien dauerhaft gelöscht werden. Diese zusätzlichen Informationen werden nicht als effektiv mit Text kommuniziert.

-   **Verwenden Sie keine unnötigen Animationen.** Animationen können irreführend sein, da Sie normalerweise in einem separaten Thread von der eigentlichen Aufgabe ausgeführt werden und daher den Fortschritt vorschlagen können, auch wenn der Vorgang gesperrt ist. Auch wenn der Vorgang langsamer als erwartet ist, nehmen Benutzer mitunter an, dass die Animation Teil der Ursache ist. Verwenden Sie daher nur Animationen, wenn eine klare Begründung vorliegt. Verwenden Sie diese nicht, um Benutzer zu unterhalten.
-   **Positionieren Sie Animationen auf der Statusanzeige.** Versetzen Sie die Animation über die Statusanzeige Bezeichnungen, sofern vorhanden. Wenn die Schaltfläche Abbrechen oder beenden rechts neben der Statusleiste angezeigt wird, schließen Sie die Schaltfläche ein, wenn Sie die Mitte ermitteln.
-   **Geben Sie beim Abschluss eines Vorgangs nur dann einen Sound wieder, wenn dieser sehr lang ist (länger als zwei Minuten), selten und wichtig ist.** Wenn der Benutzer bei der Verarbeitung wahrscheinlich von einem wichtigen Vorgang Weg geht, wird die Aufmerksamkeit des Benutzers durch einen Soundeffekt wieder hergestellt. Die Verwendung eines Sound Effekts bei der Beendigung in anderen Fällen wäre ein ablenkend Ärgernis.
-   **Stehlen Sie den Eingabefokus nicht, um eine Statusaktualisierung oder-Beendigung anzuzeigen.** Benutzer wechseln häufig zu anderen Programmen, während Sie warten, und möchten nicht unterbrochen werden. Hintergrundaufgaben müssen im Hintergrund bleiben.
-   **Machen Sie sich keine Sorgen um technischen Support.** Da das Feedback, das von Status anzeigen bereitgestellt wird, nicht notwendigerweise genau ist und flüchtig ist, sind Status leisten keine guten Mechanismen, um technische Unterstützung zu erhalten. Wenn bei diesem Vorgang ein Fehler auftritt (wie bei einem Setup Programm), sollten Sie keine zusätzlichen Statusinformationen bereitstellen, die nur für den technischen Support nützlich sind. Stellen Sie stattdessen einen alternativen Mechanismus, z. b. eine Protokolldatei, bereit, um technische Support Informationen aufzuzeichnen.

    **Falsch:**

    ![Screenshot der Statusanzeige mit dem Servernamen ](images/progress-bars-image15.png)

    In diesem Beispiel zeigt die Statusanzeige Details an, die für den technischen Support vorgesehen sind.

-   **Legen Sie den Prozentsatz oder anderen Text nicht in einer Statusanzeige ab.** Auf diesen Text kann nicht zugegriffen werden, und er ist nicht mit Designs kompatibel.

    **Falsch:**

    ![Screenshot der Statusanzeige mit Text auf der Leiste ](images/progress-bars-image16.png)

    In diesem Beispiel ist der Prozentsatz Text auf der Statusanzeige nicht zugänglich.

-   **Kombinieren Sie keine Statusanzeige mit einem ausgelasteten Zeiger.** Verwenden Sie einen oder den anderen, aber nicht beide gleichzeitig.
-   **Verwenden Sie keine vertikalen Status leisten.** Horizontale Status leisten haben eine natürlichere Zuordnung und einen besseren Fluss.

### <a name="determinate-progress-bars"></a>Determinate von Status leisten

-   **Verwenden Sie bestimmte-Status leisten für Vorgänge, die einen begrenzten Zeitraum erfordern,** auch wenn diese Zeitspanne nicht genau vorhergesagt werden kann. Unbestimmt Status leisten zeigen an, dass der Fortschritt ausgeführt wird, aber keine weiteren Informationen bereitgestellt werden. Wählen Sie nicht nur basierend auf dem möglichen Mangel an Genauigkeit eine unbestimmte Statusanzeige aus.
-   **Geben Sie die Status Phase eindeutig an.** Die Statusanzeige muss angeben können, ob sich der Vorgang am Anfang, in der Mitte oder am Ende eines Vorgangs befindet. Beispielsweise sind Status anzeigen, die sofort bis zu 99 Prozent abgeschlossen werden, dann über einen längeren Zeitraum zu warten, besonders uninformativ und lästig. In diesen Fällen sollte die Statusanzeige zunächst auf höchstens 33 Prozent festgelegt werden, um anzugeben, dass der Vorgang noch in der Anfangsphase ist.
-   **Geben Sie den Abschluss eindeutig an.** Lassen Sie eine Statusanzeige nicht zu 100 Prozent wechseln, es sei denn, der Vorgang wurde abgeschlossen.
-   **Geben Sie die geschätzte Zeit an, wenn Sie dies genau erreichen können.** Die verbleibenden geschätzten Zeit Werte sind nützlich, aber Schätzungen, die sich auf die Markierung oder den Sprung hin nicht wesentlich bewegen, sind nicht hilfreich. Möglicherweise müssen Sie einige Verarbeitungsschritte durchführen, bevor Sie genaue Schätzungen durchführen können. Wenn dies der Fall ist, werden während dieses anfänglichen Zeitraums keine möglicherweise ungenauen Schätzungen angezeigt.
-   **Starten Sie den Fortschritt nicht.** Eine Statusanzeige verliert ihren Wert, wenn Sie neu gestartet wird (möglicherweise weil ein Schritt im Vorgang abgeschlossen ist), da Benutzer nicht wissen, wann der Vorgang abgeschlossen wird. Nehmen Sie stattdessen an, dass alle Schritte des Vorgangs einen Teil des Fortschritts aufweisen und die Statusanzeige einmal abgeschlossen werden soll.

    **Falsch:**

    ![Screenshot der Statusanzeige, die neu gestartet wurde ](images/progress-bars-image17.png)

    In diesem Beispiel wurde der Vorgang in den Schritt zum Kopieren von Dateien und zum Zurücksetzen der Statusanzeige für diesen Schritt verschoben. Jetzt haben die Benutzer keine Ahnung, wie viel Fortschritt oder verbleibende Zeit verbleiben.

-   **Sichern Sie den Fortschritt nicht.** Wie bei einem Neustart verliert eine Statusanzeige den Wert, wenn Sie sich sichert. Der Fortschritt wird immer monoton gesteigert. Sie können jedoch eine geschätzte Zeit schätzen, die zunimmt (und abnimmt), da die Rate der Fortschritte variieren kann.

### <a name="indeterminate-progress-bars"></a>Unbestimmte Status leisten

-   **Verwenden Sie unbestimmt Status leisten nur für Vorgänge, deren Gesamtfortschritt nicht bestimmt werden kann.** Verwenden Sie für Vorgänge, die einen unbegrenzten Zeitraum erfordern oder auf eine unbekannte Anzahl von Objekten zugreifen, unbeschränkte Status leisten. Verwenden Sie Timeouts, um zeitbasierte Vorgänge zu Grenzen.
-   **Konvertieren Sie in eine bestimmte-Statusanzeige, sobald der allgemeine Fortschritt bestimmt werden kann.** Wenn z. b. die Anzahl der Objekte deutlich länger als zwei Sekunden dauert, können Sie eine unbestimmte Statusanzeige verwenden, während die Objekte gezählt werden, und dann in eine bestimmte-Statusanzeige konvertieren.
-   **Kombinieren Sie keine unbestimmten Status anzeigen mit der geschätzten prozentualen oder Zeit geschätzten Schätzung.** Wenn Sie diese Informationen bereitstellen können, verwenden Sie stattdessen eine bestimmte-Statusanzeige.
-   **Keine unbestimmten Status leisten mit Animationen kombinieren.** Eine unbestimmende Statusanzeige ist praktisch eine generische Animation, daher sollten Sie eine oder die andere, aber nie beide verwenden.

    **Richtig:**

    ![Screenshot des Fortschritts bei der Server Erkennung ](images/progress-bars-image18.png)

    In diesem Beispiel wird nur eine Animation verwendet, um anzuzeigen, dass ein Vorgang fortgeführt wird.

### <a name="modeless-progress-bars"></a>Nicht modante Status leisten

-   **Wenn Benutzer während des Vorgangs eine produktive Aktion ausführen können, geben Sie nicht modalem Feedback.** Möglicherweise müssen Sie eine Teilmenge der Funktionen deaktivieren, für die der Vorgang ausgeführt werden muss.
-   **Wenn das Fenster über eine Adressleiste verfügt, zeigen Sie den nicht modalstatus in der Adressleiste an.**

    ![Screenshot der Statusanzeige als Teil der Adressleiste ](images/progress-bars-image19.png)

    In diesem Beispiel wird der nicht modalstatus in der Adressleiste angezeigt.

-   **Wenn das Fenster über eine Statusleiste verfügt, zeigen Sie andernfalls den nicht modalstatus in der Statusleiste an.** Fügen Sie den entsprechenden Text in der Statusleiste auf der linken Seite ein.

    ![Screenshot der Statusanzeige als Teil der Statusleiste ](images/progress-bars-image7.png)

    In diesem Beispiel wird der nicht modalstatus in der Statusleiste angezeigt.

### <a name="modal-progress-bars"></a>Modale Status leisten

-   **Platzieren Sie modale Status anzeigen auf den Statusseiten oder in den** [Dialogfeldern für Fortschritte](win-dialog-box.md)
-   **Stellen Sie eine Befehls Schaltfläche bereit, um den Vorgang anzuhalten, wenn der Vorgang länger als ein paar Sekunden dauert, oder wenn das Potenzial nie fertiggestellt werden kann.** Kennzeichnen Sie die Schaltfläche "Abbrechen", wenn der Abbruch die Umgebung in ihren vorherigen Zustand zurückgibt (ohne Nebeneffekte), andernfalls bezeichnen Sie die Schaltfläche "beenden", um anzugeben, dass der teilweise abgeschlossene Vorgang intakt bleibt. Sie können die Schaltflächen Bezeichnung von Abbrechen ändern, um in der Mitte des Vorgangs anzuhalten, wenn Sie an einem beliebigen Punkt nicht in der Lage ist, die Umgebung in ihren vorherigen Zustand zurückzukehren. Zentrieren Sie die Befehls Schaltfläche vertikal mit der Statusanzeige, anstatt deren Spitze auszurichten.

    **Richtig:**

    ![Screenshot des Status beim Warten auf das Netzwerk ](images/progress-bars-image20.png)

    In diesem Beispiel hat das Anhalten der Netzwerkverbindung keinen Nebeneffekt, daher wird "Abbrechen" verwendet.

    **Richtig:**

    ![Screenshot der Statusanzeige mit der Kopierzeit ](images/progress-bars-image21.png)

    Wenn Sie in diesem Beispiel die Kopie anhalten, bleiben alle kopierten Dateien erhalten, sodass die Befehls Schaltfläche "anhalten" lautet.

    **Falsch:**

    ![Screenshot der Suchstatus Anzeige und der Schaltfläche "Abbrechen" ](images/progress-bars-image22.png)

    Wenn in diesem Beispiel das Anhalten der Suche keinen Nebeneffekt hat, sollte die Befehls Schaltfläche "Abbrechen" lauten.

### <a name="time-remaining"></a>Verbleibende Zeit

Für bestimmte-Status anzeigen:

-   **Verwenden Sie die folgenden Zeitformate.** Beginnen Sie mit dem ersten der folgenden Formate, wobei die größte Zeiteinheit nicht NULL ist, und wechseln Sie dann zum nächsten Format, sobald die größte Zeiteinheit zu 0 (null) wird.

    **Für Status anzeigen:**

    **Wenn verwandte Informationen in einem Doppelpunkt Format angezeigt werden:**

    Verbleibende Zeit: h Stunden, m Minuten

    Verbleibende Zeit: m Minuten, s Sekunden

    Verbleibende Zeit: s Sekunden

    **Wenn der Bildschirmbereich eine Premium-Kapazität hat:**

    h Std. min. min. min.

    m min. Sek. verbleibende Sek.

    Verbleibende Sekunden

    **Andernfalls:**

    h Stunden, m Minuten verbleiben

    m Minuten, verbleibende Sekunden

    Verbleibende Sekunden

    **Für Titelleisten:**

    hh: mm Verb leibend

    mm: verbleibende SS

    0: verbleibende SS

    In diesem Compact-Format werden die wichtigsten Informationen zuerst angezeigt, sodass Sie nicht auf der Taskleiste abgeschnitten werden.

-   **Schätzen Sie die Schätzungen, aber geben Sie keine falsche Genauigkeit an.** Wenn die größte Einheit Stunden ist, sollten Sie Minuten (falls sinnvoll), aber keine Sekunden angeben.

    **Falsch:**

    HH Stunden, mm Minuten, SS Sekunden

-   **Halten Sie die Schätzung auf dem neuesten Stand.** Die verbleibenden Updates verbleiben mindestens alle 5 Sekunden.
-   **Konzentrieren Sie sich auf die verbleibende Zeit** , da es sich dabei um die Informationen handelt, die Benutzern am meisten Geben Sie die gesamte verstrichene Zeit nur dann an, wenn es Szenarien gibt, in denen die verstrichene Zeit hilfreich ist (z. b., wenn die Aufgabe wahrscheinlich Wenn die geschätzte verbleibende Zeit mit einer Statusanzeige verknüpft ist, haben Sie keinen Prozentsatz für vollständigen Text, da diese Informationen von der Statusanzeige selbst übermittelt werden.
-   **Stimmen Sie ab.** Verwenden Sie Singular Einheiten, wenn die Zahl 1 ist.

    **Falsch:**

    1 Minute, 1 Sekunde

-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**

### <a name="progress-bar-colors"></a>Status leisten Farben

-   **Verwenden Sie rote oder gelbe Status leisten nur, um den Status Status anzugeben, nicht die abschließenden Ergebnisse einer Aufgabe.** Eine rote oder gelbe Statusleiste zeigt an, dass Benutzer einige Maßnahmen ergreifen müssen, um die Aufgabe abzuschließen. Wenn die Bedingung nicht wiederherstellbar ist, lassen Sie die Statusanzeige grün, und zeigen Sie eine Fehlermeldung an.
-   **Aktivieren Sie die Statusanzeige rot, wenn eine vom Benutzer wiederherstellbare Bedingung vorliegt, die einen weiteren Fortschritt verhindert.** Zeigen Sie eine Meldung an, um das Problem zu erläutern und eine Lösung zu empfehlen.
-   Legen **Sie die Statusanzeige gelb fest, um entweder anzugeben, dass der Benutzer die Aufgabe angehalten hat, oder ob eine Bedingung vorliegt, die den Fortschritt behindert, der** Fortschritt jedoch noch stattfindet (z. b. mit schlechter Netzwerk Konnektivität). Wenn der Benutzer angehalten wurde, ändern Sie die Bezeichnungs Schaltfläche, um fortzufahren. Wenn der Fortschritt behindert wird, zeigen Sie eine Meldung an, um das Problem zu erläutern und eine Lösung zu empfehlen.

### <a name="meters"></a>Meter

-   **Verwenden Sie Status leisten nur für den Fortschritt.** Verwenden Sie Zähler, um Prozentsätze anzugeben, die nicht mit dem Status verknüpft sind

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Diagramm, das die Größe und den Abstand der Statusleiste anzeigt ](images/progress-bars-image23.png)

Empfohlene Größe und Abstände für Status leisten.

-   Verwenden Sie immer die empfohlene Höhe der Statusanzeige.
    -   **Ausnahme:** Sie können eine andere Höhe verwenden, wenn das übergeordnete Fenster die empfohlene Höhe nicht unterstützt.
-   Verwenden Sie die minimale Breite, wenn Sie die Statusanzeige unaufdringlich machen möchten.
-   Verwenden Sie keine breiten, die länger sind als der empfohlene Höchstwert. Die Statusanzeige muss den verfügbaren Speicherplatz nicht ausfüllen.
-   Zentrieren Sie die Statusanzeige horizontal, wenn das Fenster wesentlich breiter als die maximale empfohlene Breite ist.

## <a name="labels"></a>Bezeichnungen

### <a name="progress-bar-labels"></a>Statusanzeige Bezeichnungen

-   **Verwenden Sie eine präzise Bezeichnung mit einem statischen Text Steuerelement, um anzugeben, was der Vorgang bewirkt.** Starten Sie die Bezeichnung mit einem Verb (z. b. Kopieren), und enden Sie mit einem Auslassungs Zeichen. Diese Bezeichnung kann sich dynamisch ändern, wenn der Vorgang mehrere Schritte umfasst oder mehrere Objekte verarbeitet.
-   Weisen Sie keinen eindeutigen [Zugriffsschlüssel](glossary.md) zu, da das Steuerelement nicht interaktiv ist.
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Wenn der Vorgang nicht direkt vom Benutzer initiiert wurde, können Sie eine zusätzliche Bezeichnung einschließen, um den Kontext anzugeben und die Unterbrechung zu entschuldigen. Starten Sie diese zusätzliche Bezeichnung mit dem Ausdruck, bitte warten Sie. Diese Bezeichnung sollte während des Vorgangs nicht geändert werden.

    ![Screenshot der Statusanzeige mit Bezeichnung ](images/progress-bars-image24.png)

    In diesem Beispiel wird der Benutzer aufgefordert zu warten, da der Benutzer den Vorgang nicht direkt initiiert hat.

-   Positionieren Sie die Bezeichnung oberhalb der Statusanzeige, und richten Sie die Bezeichnung am linken Rand der Statusanzeige aus.

### <a name="progress-bar-details"></a>Details zur Statusanzeige

-   Geben Sie Details in statischem Text an, der den Daten vorangestellt ist, deren Bezeichnung mit einem Doppelpunkt endet. Geben Sie die Einheiten (Sekunden, Kilobytes usw.) nach dem Detail Text an.

    **Richtig:**

    ![Screenshot der Statusanzeige mit der Übertragungsrate ](images/progress-bars-image11.png)

    In diesem Beispiel werden die Details ordnungsgemäß bezeichnet.

    **Falsch:**

    ![Screenshot der Statusanzeige ohne ordnungsgemäße Bezeichnung ](images/progress-bars-image25.png)

    In diesem Beispiel werden die Details nicht bezeichnet, sodass Benutzer ihre Bedeutung ermitteln müssen.

-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Positionieren Sie die Details unterhalb der Statusanzeige, und richten Sie die Bezeichnung am linken Rand der Statusanzeige aus.
-   Lassen Sie den Prozentsatz nicht abgeschlossen oder verbleiben, da diese Informationen von der Statusanzeige selbst übermittelt werden.

### <a name="cancel-button"></a>Schaltfläche „Abbrechen“

-   Kennzeichnen Sie die Schaltfläche "Abbrechen", wenn der Abbruch die Umgebung in ihren vorherigen Zustand zurückgibt (ohne Nebeneffekt). Andernfalls bezeichnen Sie die Schaltfläche "Abbrechen", um anzugeben, dass der teilweise abgeschlossene Vorgang unverändert bleibt.
-   Sie können die Schaltflächen Bezeichnung von Abbrechen ändern, um in der Mitte des Vorgangs anzuhalten, wenn Sie an einem beliebigen Punkt nicht in der Lage ist, die Umgebung in ihren vorherigen Zustand zurückzukehren.

### <a name="progress-dialog-box-titles"></a>Titel des Fortschritts Dialogfelds

-   Wenn die Statusanzeige in einem modalen Dialogfeld angezeigt wird, muss der Dialogfeld Titel der Name des Programms oder der Name des Vorgangs sein. Verwenden Sie nicht, was die Statusanzeige Bezeichnung für den Dialogfeld Titel sein soll.

    **Richtig:**

    ![Screenshot des Fortschrittsanzeige Titels mit dem Tasknamen ](images/progress-bars-image26.png)

    In diesem Beispiel wird der Name der Aufgabe für den Dialogfeld Titel verwendet.

    **Falsch:**

    ![Screenshot des redundanten Dialogfeld Titels ](images/progress-bars-image27.png)

    In diesem Beispiel ist der Text des Dialogfeld Titels eine erneute Anweisung der Statusanzeige Bezeichnung. Stattdessen sollte der Programmname verwendet werden.

-   Wenn die Statusanzeige in einem nicht Modaldialogfeld angezeigt wird, optimieren Sie den Titel für die Anzeige auf der Taskleiste, indem Sie die Unterscheidungs Informationen an erster Stelle platzieren. Beispiel: "66% Complete".

 

