---
title: Benachrichtigungen (Entwurfsgrundlagen)
description: Eine Benachrichtigung informiert Benutzer über Ereignisse, die nicht mit der aktuellen Benutzeraktivität in Zusammenhang stehen, indem kurz eine Sprechblase von einem Symbol im Infobereich angezeigt wird.
ms.assetid: dcac2fb7-e503-4ea3-a2c5-e3cb660c040a
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: be783ac6aac25e818d4ddf3612c726e55efa5fa5
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524514"
---
# <a name="notifications-design-basics"></a>Benachrichtigungen (Entwurfsgrundlagen)

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Eine Benachrichtigung informiert Benutzer über Ereignisse, die nicht mit der aktuellen Benutzeraktivität in Zusammenhang stehen, indem kurz eine Sprechblase von einem Symbol im Infobereich angezeigt wird. Die Benachrichtigung kann sich aus einer Benutzeraktion oder einem signifikanten Systemereignis ergeben oder potenziell nützliche Informationen von Microsoft Windows oder einer Anwendung liefern.

Die Informationen in einer Benachrichtigung sind **nützlich und relevant, aber nie kritisch.** Folglich erfordern Benachrichtigungen keine sofortige Benutzeraktion, und Benutzer können sie frei ignorieren.

![Screenshot der Sprechblase mit "neuen Updates" im Titel ](images/mess-notif-image1.png)

Eine typische Benachrichtigung.

Unter Windows Vista und höher werden Benachrichtigungen für eine feste Dauer von 9 Sekunden angezeigt. Benachrichtigungen werden nicht sofort angezeigt, wenn Benutzer inaktiv sind oder Bildschirmschoner ausgeführt werden. Windows stellt Benachrichtigungen während dieser Zeit automatisch in die Warteschlange und zeigt die Benachrichtigungen in der Warteschlange an, wenn der Benutzer die reguläre Aktivität fortnimmt. Daher müssen Sie nichts unternehmen, um diese besonderen Umstände zu behandeln.

**Entwickler:** Sie können mithilfe der SHQueryUserNotificationState-API ermitteln, wann der Benutzer aktiv ist.

**Hinweis:** Richtlinien im Zusammenhang mit [Benachrichtigungsbereich,](winenv-notification.md) [Taskleiste](winenv-taskbar.md)und [Sprechblasen](ctrl-balloons.md) werden in separaten Artikeln vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Sind die Informationen das unmittelbare direkte Ergebnis der Interaktion der Benutzer mit Ihrer Anwendung?** Wenn ja, zeigen Sie diese synchronen Informationen direkt in Ihrer Anwendung an. Verwenden Sie stattdessen ein [Dialogfeld,](win-dialog-box.md) [ein Meldungsfeld,](glossary.md) [eine Sprechblase](ctrl-balloons.md)oder eine [direkte](glossary.md) Benutzeroberfläche. Benachrichtigungen dienen nur asynchronen Informationen.

![Screenshot der Windows-Sicherheitswarnung ](images/mess-notif-image2.png)

In diesem Beispiel wird das Dialogfeld Windows-Firewallausnahmen als direktes Ergebnis der Benutzerinteraktion angezeigt. Eine Benachrichtigung wäre hier nicht geeignet.

-   **Sind die Informationen nur relevant, wenn Benutzer Ihre Anwendung aktiv verwenden?** Wenn ja, zeigen Sie die Informationen in der [Statusleiste](ctrl-status-bars.md) Ihrer Anwendung oder in einem anderen Statusbereich an.

![Screenshot der Outlook-Statusleiste ](images/mess-notif-image3.png)

In diesem Beispiel zeigt Outlook seinen Verbindungs- und Synchronisierungsstatus auf der Statusleiste an.

-   **Ändern sich die Informationen schnell, kontinuierlich und in Echtzeit?** Beispiele hierfür sind Verarbeitungsfortschritt, Kursnotierungen und Sportbewertungen. Verwenden Sie in diesem Falle keine Benachrichtigungen, da sie nicht für sich schnell ändernde Informationen geeignet sind.
-   **Sind die Informationen nützlich und relevant? Werden Benutzer ihr Verhalten wahrscheinlich ändern oder Beeinträchtigungen aufgrund des Empfangs der Informationen vermeiden?** Andernfalls werden die Informationen entweder nicht angezeigt oder in einem Statusfenster oder in einer Protokolldatei gespeichert.
-   **Sind die Informationen wichtig? Ist sofortige Aktion erforderlich?** Wenn ja, zeigen Sie die Informationen über eine Schnittstelle an, die Aufmerksamkeit erfordert und nicht einfach ignoriert werden kann, z. B. ein modales Dialogfeld oder ein Meldungsfeld. Wenn das Programm nicht aktiv ist, können Sie die Aufmerksamkeit auf die kritischen Informationen lenken, indem Sie [die Taskleistenschaltfläche des Programms](winenv-taskbar.md) dreimal blinken lassen und diese hervorgehoben lassen, bis das Programm aktiv ist.
-   **Sind die IT-Experten der primären Zielbenutzer?** Verwenden Sie in diesem Falle einen alternativen Feedbackmechanismus, z. B. [Protokolldateieinträge](glossary.md) oder E-Mail-Nachrichten. IT-Experten bevorzugen Protokolldateien dringend für nicht kritische Informationen. Darüber hinaus werden Server häufig remote verwaltet und in der Regel ohne angemeldete Benutzer ausgeführt, sodass Benachrichtigungen ineffektiv sind.

## <a name="design-concepts"></a>Entwurfskonzepte

Effektive Benachrichtigungen, die eine gute Benutzererfahrung fördern, sind:

-   **Asynchronen.** Das Ereignis ist kein unmittelbares direktes Ergebnis der aktuellen Interaktion der Benutzer mit Microsoft Windows oder Ihrer Anwendung.
-   **Nützlich.** Es besteht eine angemessene Wahrscheinlichkeit, dass Benutzer eine Aufgabe ausführen oder ihr Verhalten als Ergebnis der Benachrichtigung ändern.
-   **Relevanten.** Die Benachrichtigung zeigt hilfreiche Informationen an, die Benutzern wichtig sind und die sie nicht bereits kennen.
-   **Nicht kritisch.** Benachrichtigungen sind nicht modal und erfordern keine Benutzerinteraktion, sodass Benutzer sie frei ignorieren können.
-   **Umsetzbare.** Bei Benachrichtigungen, die das Ausführen einer Aktion vorschlagen, wird diese Aktion durch Klicken auf die Benachrichtigung initiiert. Die Aktion kann jedoch immer zurückgestellt werden.
-   **Entsprechend dargestellt.** Die Darstellung der Benachrichtigung (Dauer, Häufigkeit, Text, Symbol und Interaktivität) entspricht ihren Umständen.
-   **Nicht ärmlich!** Es gibt eine fine line zwischen der Informierung von Benutzern über ein Ereignis und derEntschädigung.

Leider gibt es zu viele benachrichtigungen, die unpassend, unpassend, unbrauchbar und irrelevant sind. Beachten Sie diese Benachrichtigungen von der Windows XP Hall of Notifications:

![Screenshot der Benachrichtigung "Tour windows xp" ](images/mess-notif-image4.png)

![Screenshot der Benachrichtigung "Nicht verwendete Symbole" ](images/mess-notif-image5.png)

![Screenshot der Benachrichtigung ".NET Passport hinzufügen" ](images/mess-notif-image6.png)

In diesen Beispielen versucht Windows XP scheinbar, Benutzer bei ihrer Erstkonfiguration zu unterstützen. Diese Benachrichtigungen werden jedoch viel zu oft und gut angezeigt, nachdem sie nützlich sind, sodass sie wenig mehr sind als unaufgeforderte Featureanzeigen.

## <a name="user-flow-must-be-maintained"></a>Der Benutzerflow muss beibehalten werden.

**Im Idealfall sehen Benutzer, die mit ihrer Arbeit gearbeitet haben, ihre Benachrichtigungen überhaupt nicht. Stattdessen werden Ihre Benachrichtigungen nur angezeigt, wenn ihr Flow bereits unterbrochen ist.**

Mihaly Csikszentmihalyi gibt in Flow: The Satisfaction of Optimal Experience an, dass Benutzer in einen Flowzustand gelangen, wenn sie vollständig in Aktivitäten aufgenommen werden, während deren sie ihr Zeiterlebnis verlieren und ein Gefühl großer Zufriedenheit haben.

**Effektive Benachrichtigungen helfen Benutzern, ihren Flow beizubehalten, indem sie nützliche, relevante Informationen präsentieren, die leicht ignoriert werden können.** Die Benachrichtigungen werden auf eine Art und Weise mit geringem Schlüssel und Peripherie dargestellt, und sie erfordern keine Interaktion.

Gehen Sie nicht davon aus, dass Benachrichtigungen keine unterbrechungsfreie Unterbrechung sein können, wenn sie [moduslos](glossary.md) sind. Benachrichtigungen erfordern keine Aufmerksamkeit der Benutzer, aber sie fordern sie auf jeden Fall an. Sie können den Benutzerflow wie folgt unterbrechen:

-   Anzeigen von Benachrichtigungen, die Benutzern egal sind.
-   Eine Benachrichtigung wird zu oft angezeigt.
-   Verwenden mehrerer Benachrichtigungen, wenn eine einzelne Benachrichtigung ausreicht.
-   Verwenden von Sound beim Anzeigen einer Benachrichtigung.

In Windows 7 haben Benutzer die endgültige Kontrolle über Benachrichtigungen. **Wenn Benutzer feststellen, dass die Benachrichtigungen eines Programms zu ängstlich sind, können sie alle Benachrichtigungen von diesem Programm unterdrücken.** Stellen Sie sicher, dass Benutzer dies nicht für Ihr Programm tun, indem Sie nützliche, relevante Informationen präsentieren und diese Richtlinien befolgen.

## <a name="notifications-must-be-ignorable"></a>Benachrichtigungen müssen ignoriert werden können.

**Benachrichtigungen erfordern keine sofortige Benutzeraktion, und Benutzer können sie frei ignorieren.**

Entwickler und Designer möchten ihre Benachrichtigungen häufig so darstellen, dass sie von Benutzern nicht ignoriert werden können. Dieses Ziel macht den Hauptvorteil von Benachrichtigungen vollständig aus, da dadurch der Benutzerflow beeinträchtigt würde. Wenn Benutzer von Ihren Benachrichtigungen ablenkt werden oder sich dazu aufgefordert sehen, sie zu lesen, ist ihr Benachrichtigungsentwurf fehlgeschlagen.

**Wenn Sie Bedenken haben, dass Benutzer Ihre Benachrichtigungen ignorieren, sollten Sie Folgendes berücksichtigen:**

-   Wenn Sie Benachrichtigungen ordnungsgemäß verwenden und sie keine sofortige Benutzeraktion erfordern, ist es entwurfsgemäß, dass Benutzer sie ignorieren möchten. Ändern Sie dies nicht.
-   Wenn für das Ereignis eine sofortige Benutzeraktion erforderlich ist, verwenden Sie eine alternative Benutzeroberfläche , die Benutzer nicht ignorieren können. Weitere Informationen finden Sie unter Ist dies die richtige Benutzeroberfläche? für die Alternativen.

## <a name="use-progressive-escalation-where-applicable"></a>Verwenden Sie ggf. progressive Eskalation.

Wenn eine Benachrichtigung für ein Ereignis verwendet wird, das Benutzer zunächst problemlos ignorieren können, dies aber letztendlich behoben werden muss, sollte eine alternative Benutzeroberfläche verwendet werden, wenn die Situation kritisch wird. Diese Technik wird als progressive Eskalation bezeichnet.

Beispielsweise weist das Windows-Energieverwaltungssystem anfänglich auf eine niedrige Akkukapazität hin, indem es einfach das Symbol für den Benachrichtigungsbereich ändert.

![Screenshot von sechs Symbolen mit Akkustatus ](images/mess-notif-image7.png)

In diesen Beispielen verwendet die Windows-Energieverwaltung das Symbol für den Infobereich, um Benutzer über einen zunehmend geringeren Akkubetrieb zu benachrichtigen.

Wenn die Akkuleistung geringer wird, warnt Windows Benutzer mithilfe einer Benachrichtigung vor schwacher Akkuleistung.

![Screenshot der Benachrichtigung über niedrigen Akkubetrieb](images/mess-notif-image8.png)

In diesem Beispiel verwendet die Windows-Energieverwaltung eine Benachrichtigung, um Benutzern mitzuteilen, dass ihre Akkuleistung schwach ist.

Diese Benachrichtigung wird angezeigt, während Benutzer noch über mehrere Optionen verfügen. Benutzer können die Benachrichtigungen ignorieren, ihre Energieoptionen ändern, ihre Arbeit abschließen und den Computer herunterfahren oder die Benachrichtigung ignorieren und die Arbeit fortsetzen. Wenn der Akkubetrieb weiter abgelassen wird, spiegeln der Text und das Symbol der Benachrichtigung die zusätzliche Dringlichkeit wider. Sobald die Akkuleistung jedoch so niedrig ist, dass Benutzer sofort agieren müssen, benachrichtigt die Windows-Energieverwaltung Benutzer über ein [modales Meldungsfeld.](glossary.md)

![Screenshot der Warnung zu stark niedriger Akkuleistung](images/mess-notif-image9.png)

In diesem Beispiel verwendet die Windows-Energieverwaltung ein modales Meldungsfeld, um Benutzer über einen kritischen Niedrigen Akkubetrieb zu benachrichtigen.

**Wenn Sie nur drei Dinge tun...**

1.  Verwenden Sie Benachrichtigungen nur, wenn Dies wirklich notwendig ist. Wenn Sie eine Benachrichtigung anzeigen, unterbrechen Sie möglicherweise Benutzer oder stören sie sogar. Stellen Sie sicher, dass die Unterbrechung gerechtfertigt ist.
2.  Verwenden Sie Benachrichtigungen für nicht kritische Ereignisse oder Situationen, die keine sofortige Benutzeraktion erfordern. Verwenden Sie für kritische Ereignisse oder Situationen, die sofortige Benutzeraktion erfordern, eine alternative Benutzeroberfläche (z. B. ein modales Dialogfeld).
3.  Wenn Sie Benachrichtigungen verwenden, machen Sie es zu einer guten Benutzererfahrung. Versuchen Sie nicht, Benutzer zu zwingen, Ihre Benachrichtigungen anzuzeigen. Wenn Benutzer so tief in ihre Arbeit versetzt sind, dass sie Ihre Benachrichtigungen nicht sehen, ist Ihr Entwurf gut.

## <a name="usage-patterns"></a>Verwendungsmuster

Benachrichtigungen haben mehrere Verwendungsmuster:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Aktion erfolgreich</strong><br/> Benachrichtigt Benutzer, wenn eine asynchrone, vom Benutzer initiierte Aktion erfolgreich abgeschlossen wurde. <br/></td>
<td><strong>Richtig:</strong><br/> <img src="images/mess-notif-image10.png" alt="Screen shot of balloon showing successful updates " /><br/> In diesem Beispiel Windows Update Benutzer benachrichtigt, wenn ihr Computer erfolgreich aktualisiert wurde.<br/> <strong>Falsch:</strong><br/> <img src="images/mess-notif-image11.png" alt="Screen shot of balloon showing file check complete " /><br/> In diesem Beispiel benachrichtigt Microsoft Outlook Benutzer, wenn eine Datendateiprüfung abgeschlossen ist. Was sollen Benutzer jetzt tun? Warum sollten Benutzer vor einem erfolgreichen Abschluss ge warnen?<br/> <strong>Anzeigen, wenn:</strong> Nach Abschluss einer asynchronen Aufgabe. Benachrichtigen Sie Benutzer nur dann über erfolgreiche Aktionen, wenn sie wahrscheinlich auf den Abschluss oder nach kürzlichen Fehlern warten.<br/> <strong>Zeigen Sie, wie:</strong> Verwenden Sie die Echtzeitoption, damit diese Benachrichtigungen nicht in die Warteschlange gestellt werden, wenn Benutzer eine Vollbildanwendung ausführen oder ihren Computer nicht aktiv verwenden.<br/> <strong>Zeigen Sie an, wie oft:</strong> Einmal.<br/> <strong>Verärgerungsfaktor:</strong> Niedrig, wenn der Erfolg aufgrund von kürzlichen Fehlern nicht zu erwarten ist, ist der Erfolg nach einem kritischen oder höchst ungewöhnlichen Fehler, sodass der Benutzer zusätzliches Feedback benötigt oder auf den Abschluss wartet. hoch, wenn dies nicht der Dert ist.<br/> <strong>Alternativen:</strong> Geben Sie bei Bedarf Feedback, indem Sie ein Symbol (oder ein vorhandenes Symbol) im Benachrichtigungsbereich anzeigen, während der Vorgang ausgeführt wird. Entfernen Sie das Symbol (oder stellen Sie das vorherige Symbol wieder zurück), wenn der Vorgang &quot; &quot; abgeschlossen ist. <br/></td>
</tr>
<tr class="even">
<td><strong>Aktionsfehler</strong><br/> Benachrichtigt Benutzer, wenn eine asynchrone, vom Benutzer initiierte Aktion fehlschlägt. <br/></td>
<td><strong>Richtig:</strong><br/> <img src="images/mess-notif-image12.png" alt="Screen shot of notification of failure to install " /><br/> In diesem Beispiel benachrichtigt die Windows-Aktivierung Benutzer über einen Fehler.<br/> <strong>Falsch:</strong><br/> <img src="images/mess-notif-image13.png" alt="Screen shot of notification of failure to update " /><br/> In diesem Beispiel hat Microsoft Outlook verwendet, um Benutzer über einen Fehler zu benachrichtigen, der für sie wahrscheinlich unwahrscheinlich ist.<br/> <strong>Anzeigen, wenn:</strong> Bei Einem Fehler einer asynchronen Aufgabe.<br/> <strong>Zeigen Sie an, wie oft:</strong> Einmal.<br/> <strong>Verärgerungsfaktor:</strong> Niedrig, wenn nützlich und relevant; hoch, wenn sich das Problem sofort selbst löst, oder benutzern andernfalls egal ist.<br/> <strong>Alternativen:</strong> Verwenden Sie ein modales Dialogfeld, wenn Benutzer den Fehler sofort bearbeiten müssen. <br/></td>
</tr>
<tr class="odd">
<td><strong>Nicht kritisches Systemereignis</strong><br/> Benachrichtigt Benutzer über wichtige Systemereignisse oder Status, die zumindest vorübergehend ignoriert werden können. <br/></td>
<td><img src="images/mess-notif-image8.png" alt="Screen shot of notification of low battery power " /><br/> In diesem Beispiel warnt Windows Benutzer vor wenig Akkuleistung, aber es gibt noch viel Zeit, bevor sie Maßnahmen ergreifen.<br/> <strong>Anzeigen, wenn:</strong> Wenn ein Ereignis auftritt und der Benutzer aktiv ist, oder eine Bedingung weiterhin vorhanden ist. Wenn dies auf ein Problem zurückt, entfernen Sie die aktuell angezeigten Benachrichtigungen sofort, sobald das Problem behoben wurde. Wie bei Aktionsbenachrichtigungen benachrichtigen Sie Benutzer nur dann über erfolgreiche Systemereignisse, wenn Benutzer wahrscheinlich auf das Ereignis warten oder nach kürzlichen Fehlern.<br/> <strong>Zeigen Sie an, wie oft:</strong> Einmal, wenn das Ereignis zum ersten Mal auftritt. Wenn dies aus einem Problem resultiert, das Benutzer lösen müssen, zeigen Sie einmal täglich erneut an.<br/> <strong>Verärgerungsfaktor:</strong> Niedrig, solange die Benachrichtigung nicht zu oft angezeigt wird.<br/> <strong>Alternativen:</strong> Wenn Benutzer ein Problem letztendlich lösen müssen, verwenden Sie progressive Eskalation, indem Sie letztendlich ein modales Dialogfeld anzeigen, wenn die Lösung obligatorisch wird. <br/></td>
</tr>
<tr class="even">
<td><strong>Optionale Benutzeraufgabe</strong><br/> Benachrichtigt Benutzer über asynchrone Aufgaben, die sie ausführen sollten. Unabhängig davon, ob die Aufgabe optional oder erforderlich ist, kann sie sicher verschoben werden. <br/></td>
<td><img src="images/mess-notif-image14.png" alt="Screen shot of notification of available updates " /><br/> In diesem Beispiel Windows Update Benutzer über ein neues Sicherheitsupdate benachrichtigt.<br/> <strong>Anzeigen, wenn:</strong> Wenn die Notwendigkeit zum Ausführen einer Aufgabe bestimmt wird und der Benutzer aktiv ist.<br/> <strong>Zeigen Sie an, wie oft:</strong> Einmal täglich für maximal drei Mal.<br/> <strong>Verärgerungsfaktor:</strong> Niedrig, solange Benutzer die Aufgabe als wichtig betrachten und die Benachrichtigung nicht zu häufig angezeigt wird.<br/> <strong>Alternativen:</strong> Wenn Benutzer die Aufgabe letztendlich ausführen müssen, verwenden Sie progressive Eskalation, indem Sie letztendlich ein modales Dialogfeld anzeigen, wenn die Aufgabe obligatorisch wird. <br/></td>
</tr>
<tr class="odd">
<td><strong>Fyi</strong><br/> Benachrichtigt Benutzer über potenziell nützliche, relevante Informationen. Sie können Benutzer über Informationen von marginaler Relevanz benachrichtigen, wenn sie optional sind und benutzer sich dafür entscheiden. <br/></td>
<td><strong>Richtig:</strong><br/> <img src="images/mess-notif-image15.png" alt="Screen shot of notification of new e-mail message " /><br/> In diesem Beispiel werden Benutzer benachrichtigt, wenn eine neue E-Mail-Nachricht empfangen wird.<br/> <strong>Richtig:</strong><br/> <img src="images/mess-notif-image16.png" alt="Screen shot of notification of contact signed in " /><br/> In diesem Beispiel werden Benutzer benachrichtigt, wenn Kontakte online benachrichtigungen, und sie haben sich entschieden, diese optionalen Informationen zu erhalten.<br/> <strong>Falsch:</strong><br/> <img src="images/mess-notif-image17.png" alt="Screen shot of notification for faster performance " /><br/> In diesem Beispiel sind die Informationen nur nützlich, wenn der Benutzer bereits hochgeschwindigkeitsbasierte USB-Anschlüsse installiert hat. Andernfalls wird der Benutzer wahrscheinlich keine anderen Möglichkeiten als das Ergebnis haben.<br/> <strong>Anzeigen, wenn:</strong> Wenn das auslösende Ereignis auftritt.<br/> <strong>Zeigen Sie, wie:</strong> Verwenden Sie die Echtzeitoption, damit diese Benachrichtigungen nicht in die Warteschlange gestellt werden, wenn Benutzer eine Vollbildanwendung ausführen oder ihren Computer nicht aktiv verwenden.<br/> <strong>Zeigen Sie an, wie oft:</strong> Einmal.<br/> <strong>Verärgerungsfaktor:</strong> Mittel bis hoch, je nachdem, wie nützlich und relevant die Benutzer sind. Nicht zu empfehlen, wenn eine geringe Wahrscheinlichkeit für benutzerfreundliche Benutzer besteht.<br/> <strong>Alternativen:</strong> Benachrichtigen Sie Benutzer nicht. <br/></td>
</tr>
<tr class="even">
<td><strong>Featureanzeige</strong><br/> Benachrichtigt Benutzer über neu installierte, nicht verwendete System- oder Anwendungsfeatures.<br/></td>
<td><strong>Verwenden Sie keine Benachrichtigungen für Featureanzeigen!</strong> Verwenden Sie stattdessen eine andere Möglichkeit, um das Feature erkennbar zu machen, z. B.: <br/>
<ul>
<li>Entwerfen Sie das Feature so, dass es in Kontexten leichter zu finden ist, in denen es benötigt wird.</li>
<li>Machen Sie nichts Besonderes, und lassen Sie Benutzer das Feature selbst entdecken.</li>
</ul>
<strong>Falsch:</strong><br/> <img src="images/mess-notif-image4.png" alt="Screen shot of notification of new features " /><br/> Verwenden Sie keine Benachrichtigungen für Featureanzeigen.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Wählen Sie das Benachrichtigungsmuster basierend auf seiner Verwendung aus.** Eine Beschreibung der einzelnen Verwendungsmuster finden Sie in der vorherigen Tabelle.
-   **Verwenden Sie während der ersten Windows-Beerfahrung keine Benachrichtigungen.** Um die erste Erfahrung zu verbessern, unterdrückt Windows 7 alle Benachrichtigungen, die während der ersten Nutzungsstunden angezeigt werden. Entwerfen Sie Ihr Programm so, dass Benutzern keine solchen Benachrichtigungen angezeigt werden.

### <a name="what-to-notify"></a>Zu benachrichtigende Informationen

-   **Benachrichtigen Sie nicht über erfolgreiche Vorgänge, außer unter den folgenden Umständen:**
    -   **Sicherheit.** Benutzer betrachten Sicherheitsvorgänge als von größter Wichtigkeit, sodass Benutzer über erfolgreiche Sicherheitsvorgänge benachrichtigt werden.
    -   **Aktueller Fehler.** Benutzer nehmen erfolgreiche Vorgänge nicht als selbstverständlich an, wenn sie unmittelbar zuvor einen Fehler hatten. Benachrichtigen Sie daher die Benutzer über den Erfolg, wenn der Vorgang vor Kurzem fehlgeschlagen ist.
    -   **Vermeiden Sie Beeinträchtigungen.** Wenn Sie erfolgreiche Vorgänge melden, kann dies zu unnötigen Benutzern werden. Benachrichtigen Sie daher Benutzer, wenn ein erfolgreicher Vorgang auf unerwartete Weise ausgeführt wird, z. B. wenn ein Vorgang lang ist oder früher oder später als erwartet abgeschlossen wird.
-   **In anderen Fällen geben Sie entweder kein Feedback für den Erfolg oder feedback "on demand".** Angenommen, Benutzer nehmen erfolgreiche Vorgänge als selbstverständlich an. Sie können Feedback bei Bedarf geben, indem Sie ein Symbol (oder ein vorhandenes Symbol) im Benachrichtigungsbereich anzeigen, während der Vorgang ausgeführt wird, und das Symbol entfernen (oder das vorherige Symbol wiederherstellen), wenn der Vorgang abgeschlossen ist.
-   Geben Sie für das FYI-Muster keine Benachrichtigung aus, wenn Benutzer weiterhin normal arbeiten können oder sich als Ergebnis der Benachrichtigung wahrscheinlich nicht **anders verhalten.**

    **Falsch:**

    ![Screenshot der Benachrichtigung für schnellere Leistung ](images/mess-notif-image17.png)

    In diesem Beispiel sind die Informationen nur nützlich, wenn der Benutzer die Ports bereits installiert hat. Andernfalls wird der Benutzer wahrscheinlich keine anderen Möglichkeiten als das Ergebnis haben.

    -   Ausnahme: Sie können Benutzer über Informationen benachrichtigen, die von befrager Relevanz sind, wenn sie **optional sind, und benutzer sich dafür entscheiden.**

        **Richtig:**

        ![Screenshot der Benachrichtigung über den angemeldeten Kontakt ](images/mess-notif-image16.png)

        In diesem Beispiel werden Benutzer benachrichtigt, wenn Kontakte online benachrichtigungen, und sie haben sich entschieden, diese optionalen Informationen zu erhalten.

-   Verwenden Sie für das nicht kritische Systemereignis und die FYI-Muster vollständige **Benachrichtigungen für ein einzelnes Ereignis.** Geben Sie nicht mehrere teilielle an.

    **Falsch:**

    ![Screenshot der Benachrichtigungen zu "Neue Hardware gefunden" ](images/mess-notif-image18.png)

    Diese Beispiele zeigen nur vier der acht Benachrichtigungen, die von Windows XP angezeigt wurden, wenn ein Benutzer eine bestimmte USB-Tastatur anfügen, von denen jede inkrementell weitere Informationen enthält.

    **Richtig:**

    ![Screenshot der Benachrichtigungen zum Installationsstatus ](images/mess-notif-image19.png)

    In diesem Beispiel führt das Anfügen einer USB-Tastatur zu zwei vollständigen Benachrichtigungen.

### <a name="when-to-notify"></a>Benachrichtigungs wann

-   **Anzeigen einer Benachrichtigung basierend auf dem Entwurfsmuster:**



| Muster              | Benachrichtigungs wann          |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktion erfolgreich<br/>            | Nach Abschluss einer asynchronen Aufgabe. Benachrichtigen Sie Benutzer nur dann über erfolgreiche Aktionen, wenn sie wahrscheinlich auf den Abschluss oder nach kürzlichen Fehlern warten.<br/>                                             |
| Aktionsfehler<br/>            | Bei Einem Fehler einer asynchronen Aufgabe.<br/>                                                                                                                                                                   |
| Nicht kritisches Systemereignis<br/> | Wenn ein Ereignis auftritt und der Benutzer aktiv ist oder die Bedingung weiterhin besteht. Wenn dies auf ein Problem hinweist, entfernen Sie die aktuell angezeigte Benachrichtigung sofort, sobald das Problem behoben wurde.<br/> |
| Optionale Benutzeraufgabe<br/>        | Wenn die Notwendigkeit zum Ausführen einer Aufgabe bestimmt wird und der Benutzer aktiv ist.<br/>                                                                                                                                   |
| Fyi<br/>                       | Wenn das auslösende Ereignis auftritt.<br/>                                                                                                                                                                       |



 

-   Wenn das Problem innerhalb von Sekunden behoben werden kann, verzögern Sie die Fehlerbenachrichtigung für das Aktionsfehlermuster um einen **angemessenen Zeitraum.** Wenn sich das Problem selbst korrigiert, melden Sie nichts. Benachrichtigen Sie erst, wenn genügend Zeit verstrichen ist, dass der Fehler erkennbar ist. Wenn Sie zu früh melden, werden Benutzer das gemeldete Problem wahrscheinlich nicht bemerken, aber sie werden die unnötige Benachrichtigung bemerken.

**Falsch:**

![Screenshot: Benachrichtigung über keine Netzwerkverbindung ](images/mess-notif-image20.png)

Wenn unmittelbar darauf folgt:

![Screenshot der Benachrichtigung zur erfolgreichen Verbindung ](images/mess-notif-image21.png)

In diesem Beispiel ist in Windows Vista die Benachrichtigung über keine drahtlose Konnektivität vorzeitig, da häufig unmittelbar darauf eine Benachrichtigung über eine gute Konnektivität folgt.

-   Verwenden Sie für den Erfolg der Aktion und die **FYI-Muster** die Echtzeitoption, damit veraltete Benachrichtigungen nicht in die Warteschlange gestellt werden, wenn Benutzer eine Vollbildanwendung ausführen oder ihren Computer nicht aktiv verwenden.
-   Für das nicht kritische Systemereignismuster schaffen Sie nicht das Potenzial für **Benachrichtigungss storms,** indem Sie Ereignisse staffeln, die an bekannte Ereignisse wie die Benutzeranmeldung gebunden sind. Binden Sie stattdessen das Ereignis an einen bestimmten Zeitraum nach dem Ereignis. Beispielsweise können Sie Benutzer daran erinnern, Ihr Produkt fünf Minuten nach der Benutzeranmeldung zu registrieren.

### <a name="how-long-to-notify"></a>Wie lange die Benachrichtigung dauern soll

In Windows Vista und höher werden Benachrichtigungen für eine feste Dauer von 9 Sekunden angezeigt.

### <a name="how-often-to-notify"></a>Benachrichtigungs häufig

-   **Die Anzahl der Anzeigezeiten für eine Benachrichtigung basiert auf dem Entwurfsmuster:**



| Muster           | Benachrichtigungs häufig  |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Aktion erfolgreich<br/>            | Einmal.<br/>                                                                                                            |
| Aktionsfehler<br/>            | Einmal.<br/>                                                                                                            |
| Nicht kritisches Systemereignis<br/> | Einmal, wenn das Ereignis zum ersten Mal auftritt. Wenn dies aus einem Problem resultiert, das Benutzer lösen müssen, zeigen Sie einmal täglich erneut an.<br/> |
| Optionale Benutzeraufgabe<br/>        | Einmal täglich für maximal drei Mal.<br/>                                                                         |
| Fyi<br/>                       | Einmal.<br/>                                                                                                            |



 

-   **Versuchen Sie bei optionalen Benutzeraufgaben nicht, Benutzer durch ständiges Anzeigen von Benachrichtigungen in die Übermittlung zu lässig zu machen.** Wenn die Aufgabe erforderlich ist, zeigen Sie sofort ein modales Dialogfeld an, anstatt Benachrichtigungen zu verwenden.

### <a name="notification-escalation"></a>Benachrichtigungseskalation

-   **Gehen Sie nicht davon aus, dass Benutzern Ihre Benachrichtigungen angezeigt werden.** Benutzer sehen sie nicht in den:
    -   Sie sind in ihrer Arbeit versunken.
    -   Sie achten nicht auf sie.
    -   Sie sind von ihrem Computer weg.
    -   Es wird eine Vollbildanwendung ausgeführt.
    -   Der Administrator hat alle Benachrichtigungen für seinen Computer deaktiviert.
-   **Wenn Benutzer irgendwann eine Aktion ergreifen müssen,** verwenden Sie progressive Eskalation, um eine alternative Benutzeroberfläche anzuzeigen, die Benutzer nicht ignorieren können.

### <a name="interaction"></a>Interaktion

-   **Machen Sie Benachrichtigungen klickbar, wenn:**
    -   **Benutzer sollten eine Aktion ausführen.** Wenn Sie auf die Benachrichtigung klicken, sollte ein Fenster angezeigt werden, in dem Benutzer die Aktion ausführen können. Dieser Ansatz wird für den Aktionsfehler und optionale Entwurfsmuster für Benutzeraufgabe bevorzugt.
    -   **Benutzer möchten möglicherweise weitere Informationen anzeigen.** Wenn Sie auf die Benachrichtigung klicken, sollte ein Fenster angezeigt werden, in dem Benutzer zusätzliche Informationen anzeigen können.
-   **Zeigt immer ein Fenster an, wenn Benutzer klicken, um eine Aktion durchzuführen.** Klicken Sie nicht direkt auf Aktion ausführen.
-   **Wenn Sie auf klicken, um weitere Informationen anzeigen zu können, sollten immer weitere Informationen enthalten sein.** Umformulieren Sie nicht nur die Informationen, die bereits in der Benachrichtigung enthalten sind.

### <a name="icons"></a>Symbole

-   **Verwenden Sie für das Aktionsfehlermuster das Standardfehlersymbol.**
-   **Verwenden Sie für die nicht kritischen Systemereignismuster das Standardwarnungssymbol.**
-   **Verwenden Sie für andere Muster Symbole,** die Objekte anzeigen, die sich auf das Subjekt beziehen oder vorschlagen, z. B. ein Schild für die Sicherheit oder eine Stromakku.
-   **Verwenden Sie Symbole basierend auf Ihrer Anwendung oder Ihrem Unternehmensbranding, wenn Ihre Zielbenutzer sie erkennen und es keine bessere Alternative gibt.**
-   Erwägen Sie bei einer progressiven Eskalation die Verwendung von Symbolen mit einer progressiv stärkeren Darstellung, **wenn die Situation dringender wird.**
-   **Verwenden Sie nicht das Standardinformationssymbol.** Dass es sich bei Benachrichtigungen um Informationen handelt, versteht sich von selbst.
-   **Erwägen Sie die Verwendung großer Symbole (32 x 32 Pixel), wenn Folgendes zu beachten ist:**
    -   Benutzer werden das Symbol schnell und nicht den Text verstehen.
    -   Die großen Symbole vermitteln ihre Bedeutung eindeutiger und effektiver als die standardmäßigen Symbole mit 16 x 16 Pixeln.
    -   Das Symbol verwendet [das Stilsymbol](vis-icons.md).

![Screenshot der Benachrichtigung "Wichtige Nachrichten" ](images/mess-notif-image22.png)

In diesem Beispiel können Benutzer die Art der Benachrichtigung schnell mit einem Blick auf das große Symbol nachvollziehen.

### <a name="notification-queuing"></a>Benachrichtigungswarteschlange

**Hinweis:** Benachrichtigungen werden immer dann in die Warteschlange gestellt, wenn sie nicht sofort angezeigt werden können, z. B. wenn eine andere Benachrichtigung angezeigt wird, der Benutzer eine Vollbildanwendung ausgeführt oder der Benutzer den Computer nicht aktiv verwendet. Echtzeitbenachrichtigungen verbleiben nur 60 Sekunden lang in der Warteschlange.

-   Verwenden Sie für den Erfolg der Aktion und die **FYI-Muster** die Echtzeitoption, damit die Benachrichtigung nicht lange in die Warteschlange gestellt wird. Diese Benachrichtigungen haben nur dann einen Wert, wenn sie sofort angezeigt werden können.
-   **Entfernen Sie Benachrichtigungen in der Warteschlange, wenn sie nicht mehr relevant sind.**
-   **Entwickler:** Hierzu können Sie das FLAG NIF \_ INFO in uFlags festlegen und szInfo auf eine leere Zeichenfolge festlegen. Dies hat keinen Schaden, wenn sich die Benachrichtigung nicht mehr in der Warteschlange befindet.

### <a name="system-integration"></a>Systemintegration

-   Wenn Ihre Anwendung während der Ausführung [](winenv-notification.md) nicht immer über ein Symbol im Benachrichtigungsbereich verfügen, zeigen Sie während der asynchronen Aufgabe oder des Ereignisses, das die Benachrichtigung verursacht hat, vorübergehend **ein Symbol an.**

## <a name="text"></a>Text

### <a name="title-text"></a>Titeltext

-   **Verwenden Sie Titeltext, der kurz die wichtigsten Informationen zusammenfasst, die Sie für die Kommunikation mit Benutzern in einer klaren, einfachen, präzisen und spezifischen Sprache benötigen.** Benutzer sollten in der Lage sein, den Zweck der Benachrichtigungsinformationen schnell und mit minimalem Aufwand zu verstehen.
-   **Verwenden Sie Textfragmente oder vollständige Sätze, ohne die Interpunktion zu beenden.**
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
-   **Verwenden Sie für die Lokalisierung nicht mehr als 48 Zeichen (auf Englisch).** Der Titel hat eine maximale Länge von 63 Zeichen, aber Sie müssen eine Erweiterung von 30 Prozent zulassen, wenn der englischsprachige Text übersetzt wird.

### <a name="body-text"></a>Textkörper

-   **Verwenden Sie Texttext, der eine Beschreibung enthält (ohne die Informationen im Titel zu wiederholen) und optional spezifische Details zur Benachrichtigung enthält und Benutzer darüber informiert, welche Aktion verfügbar ist.**
-   **Verwenden Sie vollständige Sätze mit endender Interpunktion.**
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
-   **Verwenden Sie für die Lokalisierung nicht mehr als 200 Zeichen (auf Englisch).** Der Textkörper hat eine maximale Länge von 255 Zeichen, aber Sie müssen eine Erweiterung von 30 Prozent zulassen, wenn der englischsprachige Text übersetzt wird.
-   **Fügen Sie wichtige Informationen in den Text ein, z. B. bestimmte Objektnamen.** (Beispiele: Benutzernamen, Dateinamen oder URLs.) Benutzer sollten kein weiteres Fenster öffnen müssen, um solche Informationen zu finden.
-   **Setzen Sie Objektnamen in doppelte Anführungszeichen.**
    -   **Ausnahme:** Verwenden Sie keine Anführungszeichen, wenn:
        -   Der Objektname verwendet immer [die Groß-/Formatvorlage](glossary.md), z. B. mit Benutzernamen.
        -   Der Objektname wird durch einen Doppelpunkt versetzt (Beispiel: Druckername: Mein Drucker).
        -   Der Objektname kann einfach über den Kontext bestimmt werden.
-   **Wenn Sie Objektnamen auf eine feste maximale Größe abschneiden müssen, um die Lokalisierung zu bieten, verwenden Sie eine Auslassungszeichen, um das Abschneiden anzugeben.**

    ![Screenshot der Nachricht, die einen verkürzten Namen enthält ](images/mess-notif-image23.png)

    In diesem Beispiel wird ein Objektname mithilfe von Auslassungsellipsen abgeschnitten.

-   **Verwenden Sie den folgenden Ausdruck, wenn die Benachrichtigung umsetzbar ist:**
    -   Wenn Benutzer auf die Benachrichtigung klicken können, um eine Aktion durchzuführen:

        < kurze Beschreibung wichtiger Informationen>

        <optional details>

        Klicken Sie auf <do something> .

        ![Screenshot der Meldung: "Click to view progress" ](images/mess-notif-image24.png)

        In diesem Beispiel können Benutzer klicken, um eine Aktion durchzuführen.

    -   Wenn Benutzer auf die Benachrichtigung klicken können, um weitere Informationen zu erhalten:

        < kurze Beschreibung wichtiger Informationen>

        <optional details>

        Klicken Sie auf , um weitere Informationen zu erhalten.

        ![Screenshot der Nachricht: Klicken Sie auf , um weitere Informationen zu erhalten. ](images/mess-notif-image25.png)

        In diesem Beispiel können Benutzer auf klicken, um weitere Informationen zu erhalten.

-   **Sagen Sie nicht, dass der Benutzer eine Aktion in einer Benachrichtigung ausführen muss.** Benachrichtigungen gelten für nicht kritische Informationen, die Benutzer frei ignorieren können. Wenn Benutzer wirklich eine Aktion ausführen müssen, verwenden Sie keine Benachrichtigungen.
-   **Wenn Benutzer eine Aktion ausführen sollten, machen Sie die Wichtigkeit deutlich.**
-   Beschreiben Sie Probleme bei Aktionsfehlern und nicht kritischen Systemereignismustern **in einfacher Sprache.**

    **Falsch:**

    ![Screenshot einer langen, komplexen Nachricht ](images/mess-notif-image26.png)

    In diesem Beispiel wird das Problem mit einer zu technischen, aber unspezifischen Sprache beschrieben.

    **Richtig:**

    ![Screenshot einer klaren, präzisen Nachricht ](images/mess-notif-image27.png)

    In diesem Beispiel wird das Problem in einfacher Sprache beschrieben.

-   **Beschreiben Sie das Ereignis auf eine Weise, die für die Zielbenutzer relevant ist.** Eine Benachrichtigung ist relevant, wenn die Wahrscheinlichkeit angemessen ist, dass Benutzer eine Aufgabe ausführen oder ihr Verhalten als Ergebnis der Benachrichtigung ändern. Sie können dies häufig erreichen, indem Sie Benachrichtigungen in Bezug auf Benutzerziele statt technologischer Probleme beschreiben.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Benachrichtigungen:

-   Verwenden Sie den genauen Titeltext, einschließlich der Groß-/Groß-/Groß-/A-
-   Verweisen Sie auf die Komponente als Benachrichtigung, nicht als Sprechblasen oder Warnung.
-   Verwenden Sie click, um die Benutzerinteraktion zu beschreiben.
-   Formatieren Sie den Titeltext nach Möglichkeit fett formatieren. Andernfalls setzen Sie den Titel nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Wenn die **Benachrichtigung Kritische Updates sind bereit zur Installation** angezeigt wird, klicken Sie auf die Benachrichtigung, um den Prozess zu starten.

Beim Verweisen auf den Benachrichtigungsbereich:

-   Verweisen Sie auf den Benachrichtigungsbereich als Benachrichtigungsbereich, nicht auf die Taskleiste.

 

