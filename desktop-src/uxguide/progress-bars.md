---
title: Statusleisten
description: Mit einer Statusleiste können Benutzer den Fortschritt eines längeren Vorgangs verfolgen. Eine Statusleiste kann entweder einen ungefähren Prozentsatz des Abschlusses (determiniert) oder einen laufenden (unbestimmten) Vorgang anzeigen.
ms.assetid: 067961fa-2fb1-4cd1-99a4-cbe2244c3913
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a87ddece61276e5ac651f0610f34409477e18f53
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983943"
---
# <a name="progress-bars"></a>Statusleisten

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Mit einer Statusleiste können Benutzer den Fortschritt eines längeren Vorgangs verfolgen. Eine Statusleiste kann entweder einen ungefähren Prozentsatz des Abschlusses (determiniert) oder einen laufenden (unbestimmten) Vorgang anzeigen.

Benutzerfreundlichkeitsstudien haben ergeben, dass Benutzer Antwortzeiten von mehr als einer Sekunde kennen. Daher sollten Sie Vorgänge, deren Abschluss zwei Sekunden oder länger dauert, als lang halten und eine Art Von Statusfeedback benötigen.

![Screenshot einer typischen Statusleiste ](images/progress-bars-image1.png)

Eine typische Statusleiste.

> [!Note]  
> Richtlinien zum [Layout werden](vis-layout.md) in einem separaten Artikel vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird der Vorgang in etwa fünf Sekunden oder weniger abgeschlossen?** Wenn dies der Wert ist, [verwenden](inter-mouse.md) Sie stattdessen einen Aktivitätsindikator, da das Anzeigen einer Statusanzeige für einen so kurzen Zeitraum störend wäre. Wenn der Vorgang in der Regel fünf Sekunden oder weniger dauert, aber manchmal mehr dauert, beginnen Sie mit einem ausgelastet-Zeiger, und konvertieren Sie nach fünf Sekunden in eine Statusleiste.
-   **Wird eine unbestimmte Statusleiste verwendet, um zu warten, bis der Benutzer eine Aufgabe abgeschlossen hat?** Wenn ja, zeigen Sie keine Statusleiste an. Statusleisten sind für den Status des Computers gedacht, nicht für den der Benutzer.
-   **Wird eine unbestimmte Statusleiste mit einer Animation kombiniert?** Wenn ja, verwenden Sie stattdessen nur die Animation. Die unbestimmte Statusleiste ist praktisch eine generische Animation und fügt der Animation keinen Wert hinzu.
-   **Ist der Vorgang eine sehr lange (mehr als zwei Minuten) hintergrundige Aufgabe, für die Benutzer mehr am Abschluss als am Fortschritt interessiert sind?** Falls ja, verwenden Sie stattdessen [eine Benachrichtigung.](mess-notif.md) In diesem Fall erledigen Benutzer in der Zwischenzeit andere Aufgaben und überwachen den Fortschritt nicht. Mithilfe einer Benachrichtigung können Benutzer andere Aufgaben ohne Unterbrechung ausführen. Beispiele für solche längeren Vorgänge sind Drucken, Sicherungen, Systemscans und Massendatenübertragungen oder -konvertierungen.
-   **Können Benutzer die Ergebnisse nach Abschluss des Vorgangs wiederverspielen?** Falls ja, verwenden Sie stattdessen einen Schieberegler. Beispiele für solche Vorgänge sind Video- und Audioaufzeichnung und -wiedergabe.

    ![Screenshot von Media Player und Schieberegler ](images/progress-bars-image2.png)

    In diesem Beispiel wird ein Schieberegler verwendet, um den Fortschritt während der Wiedergabe von Sound anzugeben. Auf diese Weise können Benutzer die Ergebnisse später wiederverlangen.

## <a name="design-concepts"></a>Entwurfskonzepte

Während eines längeren Vorgangs benötigen Benutzer eine allgemeine Vorstellung davon, was der Vorgang tut. Außerdem müssen sie über Dies wissen:

-   Dass ein längerer Vorgang gestartet wurde.
-   Dieser Fortschritt wird durchgeführt, und der Vorgang wird schließlich abgeschlossen (und wurde daher nicht gesperrt).
-   Der ungefähre Prozentsatz des vorgangs, der abgeschlossen wurde (und somit der verbleibende Prozentsatz).
-   Wenn sie den Vorgang abbrechen sollten, wenn es sich nicht lohnt, weiter zu warten.
-   Wenn sie während des Abschlusses des Vorgangs weiter warten oder eine andere Aktion unternehmen sollten.

**Verwenden Sie bestimmte Statusleisten für Vorgänge,** die eine bestimmte Zeit benötigen, auch wenn diese Zeit nicht genau vorhergesagt werden kann. Unbestimmte Statusleisten zeigen an, dass Fortschritte erzielt werden, geben aber keine weiteren Informationen an. Wählen Sie keine unbestimmte Statusleiste nur basierend auf der möglichen fehlenden Genauigkeit aus.

Angenommen, ein Vorgang erfordert fünf Schritte, und jeder dieser Schritte erfordert einen bestimmten Zeitraum, aber die Zeit für jeden Schritt kann stark variieren. Verwenden Sie in diesem Fall eine bestimmte Statusleiste, und zeigen Sie den Fortschritt an, wenn jeder Schritt abgeschlossen wird, proportional zur Zeit, die jeder Schritt normalerweise benötigt. Verwenden Sie eine unbestimmte Statusleiste nur, wenn eine bestimmte Statusleiste dazu führen würde, dass Benutzer fälschlicherweise feststellen, dass der Vorgang gesperrt wurde.

**Wenn Sie nur eins tun...**

Stellen Sie sicher, dass Sie Feedback zum Fortschritt für langwierige Vorgänge geben und dass die oben genannten Informationen eindeutig kommuniziert werden. Verwenden Sie nach Möglichkeit bestimmte Statusleisten.

## <a name="usage-patterns"></a>Verwendungsmuster

Statusleisten haben mehrere Verwendungsmuster:

### <a name="determinate-progress-bars"></a>Bestimmen von Statusleisten




| Bezeichnung | Wert |
|--------|-------|
| <strong>Modale, bestimmende Statusleisten</strong><br /> Geben Sie den Fortschritt eines Vorgangs an, indem Sie von links nach rechts ausfüllen und nach Abschluss des Vorgangs vollständig ausfüllen. <br /> | Da dieses Feedback <a href="glossary.md">modal ist,</a>können Benutzer keine anderen Aufgaben im Fenster ausführen (oder das übergeordnete Element, wenn es in einem modalen Dialogfeld angezeigt wird), bis der Vorgang abgeschlossen ist. <br /><img src="images/progress-bars-image3.png" alt="Screen shot of progress bar in modal window " /><br /> In diesem Beispiel gibt die Statusleiste während der Konfiguration Feedback. <br /> | 
| <strong>Modale, bestimmende Statusleisten mit der Schaltfläche "Abbrechen" oder "Beenden"</strong><br /> Erlauben Sie Benutzern, den Vorgang anzuhalten, z. B. weil der Vorgang zu lange oder die Wartezeit nicht wert ist.<br /> | <img src="images/progress-bars-image4.png" alt="Screen shot of progress bar with Stop button " /><br /> In diesem Beispiel können Benutzer auf Beenden klicken, um den Vorgang anzuhalten und die Umgebung im aktuellen Zustand zu be lassen.<br /> | 
| <strong>Modale, bestimmende Statusleisten mit einer Schaltfläche "Abbrechen" oder "Beenden" und Animation</strong><br /> Ermöglichen Sie Es Benutzern, den Vorgang anzuhalten, und fügen Sie eine Animation ein, um Benutzern zu helfen, die Auswirkungen eines Vorgangs zu visualisieren.<br /> | <img src="images/progress-bars-image5.png" alt="Screen shot of progress bar with animation " /><br /> In diesem Beispiel können Benutzer auf Beenden klicken, um den Vorgang anzuhalten und die Umgebung im aktuellen Zustand zu be lassen.<br /> | 
| <strong>Modale bestimmen doppelte Statusleisten</strong><br /> Geben Sie den Fortschritt eines mehrstufigen Vorgangs an, indem Sie den Fortschritt des aktuellen Schritts in der ersten Statusleiste und den Gesamtfortschritt in der zweiten Leiste anzeigen.<br /> | Da die erste Statusleiste wenig zusätzliche Informationen enthält und sehr störend sein kann, wird dieses Muster nicht empfohlen. Lassen Sie stattdessen alle Schritte im Vorgang einen Teil des Fortschritts gemeinsam nutzen, und lassen Sie eine einzelne Statusleiste einmal zum Abschluss wechseln. <br /><img src="images/progress-bars-image6.png" alt="Screen shot of current and overall progress bars " /><br /> In diesem Beispiel zeigt die erste Statusleiste den Fortschritt des aktuellen Schritts und die zweite Statusleiste den Gesamtfortschritt an.<br /><blockquote>[!Note]<br />Dieses Muster ist in der Regel nicht erforderlich und sollte vermieden werden.</blockquote><br /><br /> | 
| <strong>Modeless determinate progress bars (Modusloses Bestimmen von Statusleisten)</strong><br /> Geben Sie den Fortschritt eines Vorgangs an, indem Sie von links nach rechts ausfüllen und nach Abschluss des Vorgangs vollständig ausfüllen.<br /> | Im Gegensatz zu modalen Statusleisten können Benutzer während des Vorgangs andere Aufgaben ausführen. Diese Statusanzeigen können im Kontext oder auf einer Statusleiste angezeigt werden. <br /><img src="images/progress-bars-image7.png" alt="Screen shot of progress bar on status bar " /><br /> In diesem Beispiel zeigt Windows Internet ExplorerWindows-Internet Explorer den Fortschritt beim Laden einer Webseite auf der Statusleiste an. Benutzer können andere Aufgaben ausführen, während die Seite geladen wird.<br /> | 




 

### <a name="indeterminate-progress-bars"></a>Unbestimmte Statusleisten



|   Statusleistentyp  | BESCHREIBUNG             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modale unbestimmte Statusleisten**<br/> gibt an, dass ein Vorgang in Bearbeitung ist, indem eine Animation angezeigt wird, die kontinuierlich von links nach rechts über den Balken zyklen. <br/>   | Wird nur für Vorgänge verwendet, deren Gesamtfortschritt nicht bestimmt werden kann, sodass es keine Vollständigkeit gibt. Bestimmte Statusleisten sind vorzuziehen, da sie den ungefähren Prozentsatz des abgeschlossenen Vorgangs angeben und Benutzern dabei helfen, zu bestimmen, ob es sich lohnt, den Vorgang weiter zu warten. sie sind auch weniger visuell störend. <br/> ![Screenshot der modalen, unbestimmten Statusleiste](images/progress-bars-image8.png)<br/> In diesem Beispiel verwendet Windows Update eine modale, unbestimmte Statusleiste, um den Fortschritt anzugeben, während nach Updates sucht.<br/> |
| **Unbestimmte Statusleisten ohne Modus**<br/> gibt an, dass ein Vorgang in Bearbeitung ist, indem eine Animation angezeigt wird, die kontinuierlich von links nach rechts über den Balken zyklen.<br/> | Im Gegensatz zu modalen Statusleisten können Benutzer während der Verarbeitung andere Aufgaben ausführen. Diese Statusanzeigen können im Kontext oder auf einer Statusleiste angezeigt werden. <br/> ![Screenshot der schlanken Statusleiste im Outlook-Fenster ](images/progress-bars-image9.png)<br/> In diesem Beispiel verwendet Microsoft Outlook eine moduslose unbestimmte Statusleiste beim Ausfüllen von Kontakteigenschaften. Benutzer können das Eigenschaftenfenster weiterhin verwenden, während diese Arbeit läuft.<br/>                                                                                                                    |



 

### <a name="meters"></a>Meter



|   Typ                                                                                       |   BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Meter**<br/> gibt einen Prozentsatz an, der nicht mit dem Fortschritt verknüpft ist. <br/> | Dieses Muster ist keine Statusanzeige, wird jedoch mithilfe des Statusanzeige-Steuerelements implementiert. Meter weisen ein eindeutiges Aussehen auf, um sie von tatsächlichen Statusanzeigen zu unterscheiden. <br/> ![Screenshot der Verbrauchsmessung mit freiem Speicherplatz ](images/progress-bars-image10.png)<br/> In diesem Beispiel zeigt die Verbrauchsmessung den Prozentsatz des verwendeten Speicherplatzes auf dem Datenträger an.<br/> |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Geben Sie Feedback zum Fortschritt an, wenn Sie einen längeren Vorgang ausführen.** Benutzer sollten nie erraten müssen, ob der Fortschritt erzielt wird.
-   **Zeigen Sie eindeutig den tatsächlichen Fortschritt an.** Die Statusanzeige muss weiter ausgeführt werden, wenn der Fortschritt erfolgt. Wenn der Bereich der erwarteten Abschlusszeiten groß ist, sollten Sie eine nicht lineare Skala verwenden, um den Fortschritt für längere Zeiten anzugeben. Sie möchten nicht, dass Benutzer schlussfolgern, dass Ihr Programm gesperrt wurde, wenn dies noch nicht geschehen ist.
-   **Eindeutiger Hinweis auf fehlenden Fortschritt.** Die Statusanzeige darf nicht weiter ausgeführt werden, wenn kein Fortschritt erfolgt. Sie möchten nicht, dass Benutzer unbegrenzt auf einen Vorgang warten, der nie abgeschlossen wird.
-   **Geben Sie nützliche Statusdetails an.** Geben Sie zusätzliche Statusinformationen an, aber nur, wenn Benutzer damit etwas tun können. Stellen Sie sicher, dass der Text lange genug angezeigt wird, damit Benutzer ihn lesen können.

    ![Screenshot der Statusanzeige mit Übertragungsrate ](images/progress-bars-image11.png)

    In diesem Beispiel können Benutzer die Übertragungsrate sehen. Die hier niedrige Übertragungsrate deutet darauf hin, dass eine Netzwerkverbindung mit hoher Bandbreite verwendet werden muss.

-   **Geben Sie keine unnötigen Details an.** Im Allgemeinen sind die Details des ausgeführten Vorgangs für Benutzer nicht wichtig. Für Benutzer eines Setupprogramms ist es beispielsweise nicht wichtig, dass eine bestimmte Datei kopiert wird oder dass Systemkomponenten registriert werden, da sie keine Erwartungen an diese Details haben. In der Regel stellt eine gut bezeichnete Statusanzeige allein ausreichend Informationen bereit. Geben Sie daher nur dann zusätzliche Statusinformationen an, wenn Benutzer damit etwas tun können. Das Bereitstellen von Details, die Für Benutzer nicht wichtig sind, macht die Benutzererfahrung übermäßig kompliziert und technisch. Wenn Sie ausführlichere Informationen zum Debuggen benötigen, zeigen Sie sie nicht in Releasebuilds an.

    **Richtig:**

    ![Screenshot des Installationsfortschritts ](images/progress-bars-image12.png)

    In diesem Beispiel ist nur die beschriftete Statusanzeige erforderlich.

    **Richtig:**

    ![Screenshot der Statusanzeige mit Übertragungsrate ](images/progress-bars-image11.png)

    In diesem Beispiel kopiert Windows Explorer Dateien, die der Benutzer ausgewählt hat, sodass die Anzeige der kopierten Dateinamen sinnvoll ist.

    **Falsch:**

    ![Screenshot des Registrierungsfortschritts ](images/progress-bars-image13.png)

    In diesem Beispiel stellt ein Setupprogramm Details bereit, die für den Benutzer bedeutungslos sind.

-   **Stellen Sie nützliche Animationen bereit.** Wenn dies gut funktioniert, verbessern Animationen die Benutzerfreundlichkeit, indem sie Benutzern helfen, den Vorgang zu visualisieren. Gute Animationen haben mehr Auswirkungen als Text allein. Beispielsweise zeigt die Statusanzeige für den Befehl Outlook Löschen die Papierkorb für das Ziel an, wenn die Dateien wiederhergestellt werden können, aber keine Papierkorb, wenn die Dateien nicht wiederhergestellt werden können.

    ![Screenshot des Status des Löschvorgangs ](images/progress-bars-image14.png)

    In diesem Beispiel bestätigt das Fehlen eines Papierkorb, dass die Dateien dauerhaft gelöscht werden. Diese zusätzlichen Informationen würden nicht so effektiv mithilfe von Text übermittelt werden.

-   **Verwenden Sie keine unnötigen Animationen.** Animationen können irreführend sein, da sie in der Regel in einem anderen Thread als der tatsächlichen Aufgabe ausgeführt werden und daher den Fortschritt auch dann vorschlagen können, wenn der Vorgang gesperrt wurde. Wenn der Vorgang langsamer als erwartet ist, gehen Benutzer manchmal davon aus, dass die Animation Teil des Grunds ist. Verwenden Sie daher nur Animationen, wenn eine eindeutige Begründung vorliegt. verwenden Sie sie nicht, um benutzerdemittelt zu werden.
-   **Positionieren Sie Animationen, die über der Statusanzeige zentriert sind.** Setzen Sie die Animation über den Statusleistenbeschriftungen, sofern vorhanden. Wenn rechts neben der Statusleiste die Schaltfläche Abbrechen oder Beenden angezeigt wird, schließen Sie die Schaltfläche ein, wenn Sie die Mitte bestimmen.
-   **Wiedergeben eines Soundeffekts nach Abschluss eines Vorgangs nur, wenn er sehr lang (länger als zwei Minuten), selten und wichtig ist.** Wenn der Benutzer wahrscheinlich während der Verarbeitung von einem wichtigen Vorgang abkommt, stellt ein Soundeffekt die Aufmerksamkeit des Benutzers wieder her. Die Verwendung eines sound-Effekts bei Abschluss in anderen Fällen wäre ein ablenkender Verärgerungseffekt.
-   **Stehlen Sie den Eingabefokus nicht, um ein Fortschrittsupdate oder einen Abschluss anzuzeigen.** Benutzer wechseln während des Wartens häufig zu anderen Programmen und möchten nicht unterbrochen werden. Hintergrundaufgaben müssen im Hintergrund bleiben.
-   **Machen Sie sich keine Gedanken über den technischen Support.** Da das Feedback, das von Denkleisten bereitgestellt wird, nicht unbedingt genau und flüchtig ist, sind Statusleisten kein guter Mechanismus zum Bereitstellen von Informationen für den technischen Support. Wenn der Vorgang fehlschlagen kann (wie bei einem Setupprogramm), stellen Sie daher keine zusätzlichen Statusinformationen bereit, die nur für den technischen Support nützlich sind. Stellen Sie stattdessen einen alternativen Mechanismus bereit, z. B. eine Protokolldatei, um Informationen zum technischen Support aufzuzeichnen.

    **Falsch:**

    ![Screenshot der Statusanzeige mit Dem Servernamen ](images/progress-bars-image15.png)

    In diesem Beispiel zeigt die Statusleiste Details an, die für den technischen Support vorgesehen sind.

-   **Legen Sie den Prozentsatz nicht abgeschlossen oder einen anderen Text auf eine Statusanzeige.** Auf diesen Text kann nicht zugegriffen werden, und er ist nicht mit der Verwendung von Designs kompatibel.

    **Falsch:**

    ![Screenshot der Statusanzeige mit Text auf der Leiste ](images/progress-bars-image16.png)

    In diesem Beispiel kann nicht auf den Prozentsatz des Texts auf der Statusleiste zugegriffen werden.

-   **Kombinieren Sie keine Statusanzeige mit einem ausgelasteten Zeiger.** Verwenden Sie das eine oder das andere, aber nicht beide gleichzeitig.
-   **Verwenden Sie keine vertikalen Statusleisten.** Horizontale Statusleisten weisen eine natürlichere Zuordnung und einen besseren Ablauf auf.

### <a name="determinate-progress-bars"></a>Bestimmen von Statusleisten

-   **Verwenden Sie determinierte Statusanzeigen für Vorgänge, die eine bestimmte Zeitspanne erfordern,** auch wenn diese Zeitspanne nicht genau vorhergesagt werden kann. Unbestimmte Statusanzeigen zeigen an, dass der Fortschritt ausgeführt wird, geben aber keine weiteren Informationen an. Wählen Sie keine unbestimmte Statusanzeige aus, die nur auf der möglichen fehlenden Genauigkeit basiert.
-   **Geben Sie die Statusphase eindeutig an.** Die Statusanzeige muss angeben können, ob sich der Vorgang am Anfang, in der Mitte oder am Ende eines Vorgangs befindet. So sind z. B. Statusanzeigen, die sofort auf eine Vervollständigung von 99 Prozent zentrieren und dann für einen längeren Zeitraum dort bleiben, besonders uninformativ und unwahrscheinlich. In diesen Fällen sollte die Statusanzeige anfänglich auf höchstens 33 Prozent festgelegt werden, um anzugeben, dass sich der Vorgang noch in der Anfangsphase befindet.
-   **Geben Sie die Vervollständigung eindeutig an.** Lassen Sie eine Statusanzeige nur dann auf 100 Prozent zu, wenn der Vorgang abgeschlossen wurde.
-   **Geben Sie eine schätzungsweise verbleibende Zeit an, wenn Sie dies genau tun können.** Die geschätzten verbleibenden Zeitangaben sind nützlich, aber Schätzungen, die weit von der Marke entfernt sind oder deutlich abprallen, sind nicht hilfreich. Möglicherweise müssen Sie einige Verarbeitungsaufgaben ausführen, bevor Sie genaue Schätzungen vornehmen können. In diesem Falle sollten Sie während dieses anfänglichen Zeitraums keine potenziell ungenauen Schätzungen anzeigen.
-   **Starten Sie den Fortschritt nicht neu.** Eine Statusanzeige verliert ihren Wert, wenn sie neu gestartet wird (möglicherweise weil ein Schritt im Vorgang abgeschlossen wird), da Benutzer nicht wissen können, wann der Vorgang abgeschlossen wird. Lassen Sie stattdessen alle Schritte im Vorgang einen Teil des Fortschritts teilen, und lassen Sie die Statusanzeige einmal abgeschlossen werden.

    **Falsch:**

    ![Screenshot der Statusanzeige, die neu gestartet wurde ](images/progress-bars-image17.png)

    In diesem Beispiel wurde der Vorgang in den Schritt zum Kopieren von Dateien verschoben und die Statusanzeige für diesen Schritt zurückgesetzt. Benutzer wissen jetzt nicht mehr, wie viel Fortschritt erzielt wurde oder wie viel Zeit noch übrig ist.

-   **Sichern Sie den Fortschritt nicht.** Wie bei einem Neustart verliert eine Statusanzeige ihren Wert, wenn sie gesichert wird. Erhöhen Sie den Fortschritt immer monoton. Sie können jedoch eine verbleibende Zeitschätzung haben, die sich erhöht (und verringert), da die Fortschrittsrate variieren kann.

### <a name="indeterminate-progress-bars"></a>Unbestimmte Statusanzeigen

-   **Verwenden Sie unbestimmte Statusanzeigen nur für Vorgänge, deren Gesamtfortschritt nicht bestimmt werden kann.** Verwenden Sie unbestimmte Statusanzeigen für Vorgänge, die eine unbegrenzte Zeit erfordern oder auf eine unbekannte Anzahl von Objekten zugreifen. Verwenden Sie Timeouts, um zeitbasierten Vorgängen Grenzen zu geben.
-   **Konvertieren Sie in eine bestimmende Statusanzeige, sobald der Gesamtfortschritt ermittelt werden kann.** Wenn es beispielsweise deutlich länger als zwei Sekunden dauert, die Anzahl der Objekte zu bestimmen, können Sie eine unbestimmte Statusanzeige verwenden, während die Objekte gezählt werden, und dann in eine bestimmende Statusanzeige konvertieren.
-   **Kombinieren Sie keine unbestimmten Statusanzeigen mit prozentigen Abschluss- oder Zeitschätzungen.** Wenn Sie diese Informationen angeben können, verwenden Sie stattdessen eine bestimmende Statusanzeige.
-   **Kombinieren Sie keine unbestimmten Statusanzeigen mit Animationen.** Eine unbestimmte Statusanzeige ist im Grunde eine generische Animation, daher sollten Sie die eine oder die andere, aber nie beide verwenden.

    **Richtig:**

    ![Screenshot des Fortschritts bei der Servererkennung ](images/progress-bars-image18.png)

    In diesem Beispiel wird nur eine Animation verwendet, um zu zeigen, dass ein Vorgang gerade durchgeführt wird.

### <a name="modeless-progress-bars"></a>Statusanzeigen ohne Modus

-   **Wenn Benutzer während des Vorgangs produktiv arbeiten können, senden Sie uns feedbacklos.** Möglicherweise müssen Sie eine Teilmenge der Funktionen deaktivieren, für die der Vorgang abgeschlossen werden muss.
-   **Wenn das Fenster über eine Adressleiste verfügt, zeigen Sie den statuslosen Status in der Adressleiste an.**

    ![Screenshot der Statusanzeige als Teil der Adressleiste ](images/progress-bars-image19.png)

    In diesem Beispiel wird der statuslose Status in der Adressleiste angezeigt.

-   Wenn das Fenster über eine Statusleiste verfügt, zeigen Sie andernfalls **den statuslosen Status in der Statusleiste an.** Legen Sie den entsprechenden Text links in die Statusleiste ein.

    ![Screenshot der Statusanzeige als Teil der Statusleiste ](images/progress-bars-image7.png)

    In diesem Beispiel wird der statuslose Status in der Statusleiste angezeigt.

### <a name="modal-progress-bars"></a>Modale Statusleisten

-   **Platzieren Sie modale Statusleisten auf Statusseiten oder** [Statusdialogfeldern.](win-dialog-box.md)
-   **Geben Sie eine Befehlsschaltfläche an, um den Vorgang anzuhalten, wenn der Vorgang mehr als ein paar Sekunden dauert oder möglicherweise nie abgeschlossen werden kann.** Beschriften Sie die Schaltfläche Abbrechen, wenn der Abbruch den vorherigen Zustand der Umgebung zurückgibt (ohne Nebeneffekte). Bezeichnen Sie andernfalls die Schaltfläche Beenden, um anzugeben, dass der teilweise abgeschlossene Vorgang intakt bleibt. Sie können die Schaltflächenbezeichnung in der Mitte des Vorgangs von Abbrechen in Beenden ändern, wenn es zu einem bestimmten Zeitpunkt nicht möglich ist, die Umgebung in den vorherigen Zustand zurückzuversetzen. Zentrieren Sie die Befehlsschaltfläche vertikal mit der Statusleiste, anstatt ihre Oberen auszurichten.

    **Richtig:**

    ![Screenshot des Fortschritts des Wartens auf das Netzwerk ](images/progress-bars-image20.png)

    In diesem Beispiel hat das Anhalten der Netzwerkverbindung keine Nebeneffekte, daher wird Abbrechen verwendet.

    **Richtig:**

    ![Screenshot der Statusanzeige mit linker Kopierzeit ](images/progress-bars-image21.png)

    In diesem Beispiel bleiben beim Anhalten der Kopie alle kopierten Dateien übrig, sodass die Befehlsschaltfläche mit Beenden bezeichnet wird.

    **Falsch:**

    ![Screenshot der Suchfortschrittsleiste und der Schaltfläche "Beenden" ](images/progress-bars-image22.png)

    In diesem Beispiel hat das Anhalten der Suche keine Nebeneffekte, daher sollte die Befehlsschaltfläche mit Abbrechen bezeichnet werden.

### <a name="time-remaining"></a>Verbleibende Zeit

Für bestimmende Statusanzeigen:

-   **Verwenden Sie die folgenden Zeitformate.** Beginnen Sie mit dem ersten der folgenden Formate, bei dem die größte Zeiteinheit nicht 0 (null) ist, und wechseln Sie dann in das nächste Format, sobald die größte Zeiteinheit 0 (null) wird.

    **Für Statusleisten:**

    **Wenn verwandte Informationen in einem Doppelpunktformat angezeigt werden:**

    Verbleibende Zeit: h Stunden, m Minuten

    Verbleibende Zeit: m Minuten, s Sekunden

    Verbleibende Zeit: s Sekunden

    **Wenn der Bildschirmbereich premium ist:**

    h hrs, m mins remaining

    m Minuten, s Sekunden verbleibend

    s verbleibende Sekunden

    **Andernfalls:**

    h Stunden, m Minuten verbleibend

    m Minuten, s Sekunden verbleibend

    s verbleibende Sekunden

    **Für Titelleisten:**

    hh:mm verbleibend

    mm:ss verbleibend

    0:ss verbleibend

    Dieses kompakte Format zeigt zuerst die wichtigsten Informationen an, damit sie nicht auf der Taskleiste abgeschnitten werden.

-   **Treffen Sie Schätzungen genau, geben Sie jedoch keine falsche Genauigkeit an.** Wenn die größte Einheit Stunden ist, geben Sie Minuten (sofern sinnvoll), aber nicht Sekunden ein.

    **Falsch:**

    hh hours, mm minutes, ss seconds

-   **Halten Sie die Schätzung auf dem neuesten Stand.** Die verbleibende Aktualisierungszeit wird mindestens alle 5 Sekunden geschätzt.
-   **Konzentrieren Sie sich auf die verbleibende Zeit,** da dies die Informationen sind, die den Benutzern am meisten interessieren. Geben Sie die insgesamt verstrichene Zeit nur dann an, wenn es Szenarien gibt, in denen die verstrichene Zeit hilfreich ist (z. B. wenn die Aufgabe wahrscheinlich wiederholt wird). Wenn die verbleibende Zeitschätzung einer Statusanzeige zugeordnet ist, verfügen Sie nicht über vollständigen Text in Prozent, da diese Informationen von der Statusleiste selbst übermittelt werden.
-   **Seien Sie grammatisch korrekt.** Verwenden Sie singulare Einheiten, wenn die Zahl 1 ist.

    **Falsch:**

    1 Minuten, 1 Sekunden

-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**

### <a name="progress-bar-colors"></a>Statusleistenfarben

-   **Verwenden Sie rote oder gelbe Statusleisten nur, um den Status anzugeben, nicht die Endergebnisse einer Aufgabe.** Eine rote oder gelbe Statusanzeige gibt an, dass Benutzer maßnahmen müssen, um die Aufgabe abzuschließen. Wenn die Bedingung nicht wiederhergestellt werden kann, lassen Sie die Statusleiste grün, und zeigen Sie eine Fehlermeldung an.
-   **Rotieren Sie die Statusanzeige, wenn eine vom Benutzer wiederherstellbare Bedingung vorliegt, die einen weiteren Fortschritt verhindert.** Zeigen Sie eine Meldung an, um das Problem zu erläutern und eine Lösung zu empfehlen.
-   **Drehen Sie die Statusleiste gelb, um anzugeben, dass der Benutzer die Aufgabe angehalten hat oder dass eine Bedingung vorhanden ist, die den Fortschritt einbezieht,** aber der Fortschritt weiterhin stattfindet (z. B. bei schlechter Netzwerkkonnektivität). Wenn der Benutzer angehalten wurde, ändern Sie die Bezeichnung der Schaltfläche Anhalten in Fortsetzen. Wenn der Fortschritt beeinträchtigt ist, zeigen Sie eine Meldung an, um das Problem zu erklären und eine Lösung zu empfehlen.

### <a name="meters"></a>Meter

-   **Verwenden Sie statusleisten nur für den Fortschritt.** Verwenden Sie Meter, um Prozentsätze anzugeben, die sich nicht auf den Fortschritt beziehen.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größen- und Abstände

![Diagramm, das die Größen- und Abstandsanzeige zeigt ](images/progress-bars-image23.png)

Empfohlene Größen- und Abstandsanzeigen.

-   Verwenden Sie immer die empfohlene Statusanzeigehöhe.
    -   **Ausnahme:** Sie können eine andere Höhe verwenden, wenn das übergeordnete Fenster die empfohlene Höhe nicht unterstützt.
-   Verwenden Sie die Mindestbreite, wenn Sie die Statusanzeige unaufdringlich machen möchten.
-   Verwenden Sie keine Breiten, die länger sind als die maximal empfohlene. Die Statusanzeige muss den verfügbaren Platz nicht ausfüllen.
-   Zentren Sie die Statusanzeige horizontal, wenn das Fenster wesentlich breiter als die maximal empfohlene Breite ist.

## <a name="labels"></a>Bezeichnungen

### <a name="progress-bar-labels"></a>Statusanzeigebeschriftungen

-   **Verwenden Sie eine präzise Bezeichnung mit einem statischen Textsteuerelement, um anzugeben, was der Vorgang tut.** Starten Sie die Bezeichnung mit einem Verb (z. B. Kopieren), und enden Sie mit einem Auslassungszeichen. Diese Bezeichnung kann sich dynamisch ändern, wenn der Vorgang über mehrere Schritte verfügt oder mehrere Objekte verarbeitet.
-   Weisen Sie keinen eindeutigen [Zugriffsschlüssel](glossary.md) zu, da das Steuerelement nicht interaktiv ist.
-   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
-   Wenn der Vorgang nicht direkt vom Benutzer initiiert wurde, können Sie eine zusätzliche Bezeichnung einfügen, um den Kontext zu geben und sich für die Unterbrechung zu bitten. Starten Sie diese zusätzliche Bezeichnung mit dem Ausdruck Please wait while . Diese Bezeichnung sollte sich während des Vorgangs nicht ändern.

    ![Screenshot der Statusanzeige mit Bezeichnung ](images/progress-bars-image24.png)

    In diesem Beispiel wird der Benutzer aufgefordert, zu warten, da der Benutzer den Vorgang nicht direkt initiiert hat.

-   Positionieren Sie die Bezeichnung über der Statusleiste, und richten Sie die Bezeichnung am linken Rand der Statusleiste aus.

### <a name="progress-bar-details"></a>Statusanzeigedetails

-   Geben Sie Details im statischen Text an, wobei den Daten eine Bezeichnung vorangestellt wird, die mit einem Doppelpunkt endet. Geben Sie Einheiten (Sekunden, Kilobyte usw.) nach dem Detailtext an.

    **Richtig:**

    ![Screenshot der Statusanzeige mit Übertragungsrate ](images/progress-bars-image11.png)

    In diesem Beispiel werden die Details ordnungsgemäß bezeichnet.

    **Falsch:**

    ![Screenshot der Statusanzeige ohne richtige Bezeichnung ](images/progress-bars-image25.png)

    In diesem Beispiel werden die Details nicht bezeichnet, sodass Benutzer ihre Bedeutung bestimmen müssen.

-   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
-   Positionieren Sie die Details unter der Statusleiste, und richten Sie die Bezeichnung am linken Rand der Statusleiste aus.
-   Geben Sie den prozentsatz abgeschlossenen oder verbleibenden Prozentsatz nicht an, da diese Informationen von der Statusanzeige selbst übermittelt werden.

### <a name="cancel-button"></a>Schaltfläche „Abbrechen“

-   Beschriften Sie die Schaltfläche Abbrechen, wenn beim Abbrechen die Umgebung in den vorherigen Zustand zurückgesetzt wird (ohne Nebeneffekt). Beschriften Sie andernfalls die Schaltfläche Beenden, um anzugeben, dass der teilweise abgeschlossene Vorgang intakt bleibt.
-   Sie können die Schaltflächenbezeichnung in der Mitte des Vorgangs von Abbrechen in Beenden ändern, wenn es zu einem bestimmten Zeitpunkt nicht möglich ist, die Umgebung in den vorherigen Zustand zurückzuversetzen.

### <a name="progress-dialog-box-titles"></a>Titel des Statusdialogfelds

-   Wenn die Statusanzeige in einem modalen Dialogfeld angezeigt wird, sollte der Titel des Dialogfelds der Name des Programms oder der Name des Vorgangs sein. Verwenden Sie nicht die Statusleistenbezeichnung für den Titel des Dialogfelds.

    **Richtig:**

    ![Screenshot des Statusleistentitels mit Aufgabenname ](images/progress-bars-image26.png)

    In diesem Beispiel wird der Aufgabenname für den Titel des Dialogfelds verwendet.

    **Falsch:**

    ![Screenshot des redundanten Dialogfeldtitels ](images/progress-bars-image27.png)

    In diesem Beispiel ist der Titeltext des Dialogfelds eine Neuformierung der Statusleistenbezeichnung. Stattdessen sollte der Programmname verwendet werden.

-   Wenn die Statusanzeige in einem moduslosen Dialogfeld angezeigt wird, optimieren Sie den Titel für die Anzeige auf der Taskleiste, indem Sie zuerst die Unterscheidungsinformationen präzise platzieren. Beispiel: "66 % Abgeschlossen".

 

