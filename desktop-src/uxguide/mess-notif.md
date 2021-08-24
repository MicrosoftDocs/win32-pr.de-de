---
title: Benachrichtigungen (Entwurfsgrundlagen)
description: Eine Benachrichtigung informiert Benutzer über Ereignisse, die nicht mit der aktuellen Benutzeraktivität in Zusammenhang stehen, indem kurz eine Sprechblase von einem Symbol im Infobereich angezeigt wird.
ms.assetid: dcac2fb7-e503-4ea3-a2c5-e3cb660c040a
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: caf25d24759826bbd593d7a4fa0763e91d304ac5f1211b00bbd4af55abb6ee71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842131"
---
# <a name="notifications-design-basics"></a>Benachrichtigungen (Entwurfsgrundlagen)

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Eine Benachrichtigung informiert Benutzer über Ereignisse, die nicht mit der aktuellen Benutzeraktivität in Zusammenhang stehen, indem kurz eine Sprechblase von einem Symbol im Infobereich angezeigt wird. Die Benachrichtigung kann sich aus einer Benutzeraktion oder einem signifikanten Systemereignis ergeben oder potenziell nützliche Informationen von Microsoft Windows oder einer Anwendung bieten.

Die Informationen in einer Benachrichtigung sind **nützlich und relevant, aber nie kritisch.** Folglich erfordern Benachrichtigungen keine sofortige Benutzeraktion, und Benutzer können sie frei ignorieren.

![Screenshot der Sprechblase mit "neuen Updates" im Titel ](images/mess-notif-image1.png)

Eine typische Benachrichtigung.

In Windows Vista und höher werden Benachrichtigungen für eine feste Dauer von 9 Sekunden angezeigt. Benachrichtigungen werden nicht sofort angezeigt, wenn Benutzer inaktiv sind oder Bildschirmschoner ausgeführt werden. Windows stellt Benachrichtigungen während dieser Zeit automatisch in die Warteschlange und zeigt die Benachrichtigungen in der Warteschlange an, wenn der Benutzer die reguläre Aktivität fortnimmt. Daher müssen Sie nichts unternehmen, um diese besonderen Umstände zu behandeln.

**Entwickler:** Sie können mithilfe der SHQueryUserNotificationState-API ermitteln, wann der Benutzer aktiv ist.

**Hinweis:** Richtlinien im Zusammenhang mit [Benachrichtigungsbereich,](winenv-notification.md) [Taskleiste](winenv-taskbar.md)und [Sprechblasen](ctrl-balloons.md) werden in separaten Artikeln vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Sind die Informationen das unmittelbare direkte Ergebnis der Interaktion der Benutzer mit Ihrer Anwendung?** Wenn ja, zeigen Sie diese synchronen Informationen direkt in Ihrer Anwendung an. Verwenden Sie stattdessen ein [Dialogfeld,](win-dialog-box.md) [ein Meldungsfeld,](glossary.md) [eine Sprechblase](ctrl-balloons.md)oder eine [direkte](glossary.md) Benutzeroberfläche. Benachrichtigungen dienen nur asynchronen Informationen.

![Screenshot der Windows-Sicherheitswarnung ](images/mess-notif-image2.png)

In diesem Beispiel wird das Dialogfeld Firewallausnahmen Windows als direktes Ergebnis der Benutzerinteraktion angezeigt. Eine Benachrichtigung wäre hier nicht geeignet.

-   **Sind die Informationen nur relevant, wenn Benutzer Ihre Anwendung aktiv verwenden?** Wenn ja, zeigen Sie die Informationen in der [Statusleiste](ctrl-status-bars.md) Ihrer Anwendung oder in einem anderen Statusbereich an.

![Screenshot der Outlook-Statusleiste ](images/mess-notif-image3.png)

In diesem Beispiel zeigt Outlook den Verbindungs- und Synchronisierungsstatus auf der Statusleiste an.

-   **Ändern sich die Informationen schnell, kontinuierlich und in Echtzeit?** Beispiele hierfür sind Verarbeitungsfortschritt, Kursnotierungen und Sportbewertungen. Verwenden Sie in diesem Falle keine Benachrichtigungen, da sie nicht für sich schnell ändernde Informationen geeignet sind.
-   **Sind die Informationen nützlich und relevant? Werden Benutzer ihr Verhalten wahrscheinlich ändern oder Beeinträchtigungen aufgrund des Empfangs der Informationen vermeiden?** Andernfalls werden die Informationen entweder nicht angezeigt oder in einem Statusfenster oder in einer Protokolldatei gespeichert.
-   **Sind die Informationen wichtig? Ist sofortige Aktion erforderlich?** Wenn ja, zeigen Sie die Informationen über eine Schnittstelle an, die Aufmerksamkeit erfordert und nicht einfach ignoriert werden kann, z. B. ein modales Dialogfeld oder Meldungsfeld. Wenn das Programm nicht aktiv ist, können Sie die Aufmerksamkeit auf die kritischen Informationen lenken, indem Sie [die Taskleistenschaltfläche des Programms](winenv-taskbar.md) dreimal blinken lassen und diese hervorgehoben lassen, bis das Programm aktiv ist.
-   **Sind die IT-Experten der primären Zielbenutzer?** Verwenden Sie in diesem Falle einen alternativen Feedbackmechanismus, z. B. [Protokolldateieinträge](glossary.md) oder E-Mail-Nachrichten. IT-Experten bevorzugen Protokolldateien dringend für nicht kritische Informationen. Darüber hinaus werden Server häufig remote verwaltet und in der Regel ohne angemeldete Benutzer ausgeführt, sodass Benachrichtigungen ineffektiv sind.

## <a name="design-concepts"></a>Entwurfskonzepte

Effektive Benachrichtigungen, die eine gute Benutzererfahrung fördern, sind:

-   **Asynchronen.** Das Ereignis ist kein unmittelbares direktes Ergebnis der aktuellen Interaktion der Benutzer mit Microsoft Windows oder Ihrer Anwendung.
-   **Nützlich.** Es besteht eine angemessene Wahrscheinlichkeit, dass Benutzer eine Aufgabe ausführen oder ihr Verhalten als Ergebnis der Benachrichtigung ändern.
-   **Relevanten.** Die Benachrichtigung zeigt hilfreiche Informationen an, die Benutzern wichtig sind und die sie nicht bereits kennen.
-   **Nicht kritisch.** Benachrichtigungen sind nicht modal und erfordern keine Benutzerinteraktion, sodass Benutzer sie frei ignorieren können.
-   **Umsetzbare.** Bei Benachrichtigungen, die das Ausführen einer Aktion vorschlagen, wird diese Aktion durch Klicken auf die Benachrichtigung initiiert. Die Aktion kann jedoch immer zurückgestellt werden.
-   **Entsprechend dargestellt.** Die Darstellung der Benachrichtigung (Dauer, Häufigkeit, Text, Symbol und Interaktivität) entspricht ihren Umständen.
-   **Nicht ärmlich!** Es gibt eine Feinlinie zwischen der Informierung von Benutzern über ein Ereignis und derEntschädigung.

Leider gibt es zu viele benachrichtigungen, die unpassend, unbrauchbar und irrelevant sind. Beachten Sie diese Benachrichtigungen von der Windows XP Hall of Notifications:

![Screenshot der Benachrichtigung "Tour windows xp" ](images/mess-notif-image4.png)

![Screenshot der Benachrichtigung "Nicht verwendete Symbole" ](images/mess-notif-image5.png)

![Screenshot der Benachrichtigung ".NET Passport hinzufügen" ](images/mess-notif-image6.png)

In diesen Beispielen versucht Windows XP scheinbar, Benutzer bei ihrer Erstkonfiguration zu unterstützen. Diese Benachrichtigungen werden jedoch viel zu oft und gut angezeigt, nachdem sie nützlich sind, sodass sie wenig mehr sind als unaufgeforderte Featureanzeigen.

## <a name="user-flow-must-be-maintained"></a>Der Benutzerflow muss beibehalten werden.

**Im Idealfall sehen Benutzer, die mit ihrer Arbeit gearbeitet haben, ihre Benachrichtigungen überhaupt nicht. Stattdessen werden Ihre Benachrichtigungen nur angezeigt, wenn ihr Flow bereits unterbrochen ist.**

Mihaly Csikszentmihalyi gibt in Flow: The Satisfaction of Optimal Experience an, dass Benutzer in einen Flowzustand gelangen, wenn sie vollständig in Aktivitäten aufgenommen werden, während denen sie das Gefühl der Zeit verlieren und sich sehr zufrieden fühlen.

**Effektive Benachrichtigungen helfen Benutzern, ihren Flow beizubehalten, indem sie nützliche, relevante Informationen präsentieren, die leicht ignoriert werden können.** Die Benachrichtigungen werden auf eine Peripheriegeräte-Weise mit geringem Schlüssel angezeigt, und sie erfordern keine Interaktion.

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

Beispielsweise weist das Windows Energieverwaltungssystem anfänglich auf eine niedrige Akkukapazität hin, indem einfach das Symbol für den Benachrichtigungsbereich geändert wird.

![Screenshot von sechs Symbolen mit Akkustatus ](images/mess-notif-image7.png)

In diesen Beispielen verwendet Windows Energieverwaltung das Symbol für den Benachrichtigungsbereich, um Benutzer über einen zunehmend geringeren Akkubetrieb zu benachrichtigen.

Wenn die Akkuleistung geringer wird, warnt Windows Benutzer mithilfe einer Benachrichtigung vor schwacher Akkuleistung.

![Screenshot der Benachrichtigung über niedrigen Akkubetrieb](images/mess-notif-image8.png)

In diesem Beispiel verwendet Windows Energieverwaltung eine Benachrichtigung, um Benutzer darüber zu informieren, dass ihre Akkuleistung schwach ist.

Diese Benachrichtigung wird angezeigt, während Benutzer noch über mehrere Optionen verfügen. Benutzer können ihre Energieoptionen anschließen, ändern, ihre Arbeit packen und den Computer herunterfahren oder die Benachrichtigung ignorieren und die Arbeit fortsetzen. Wenn der Akkubetrieb weiter abgelassen wird, spiegeln der Text und das Symbol der Benachrichtigung die zusätzliche Dringlichkeit wider. Sobald die Akkuleistung jedoch so niedrig ist, dass Benutzer sofort handeln müssen, benachrichtigt Windows Die Energieverwaltung die Benutzer über ein [modales Meldungsfeld.](glossary.md)

![Screenshot der Warnung zu stark niedriger Akkuleistung](images/mess-notif-image9.png)

In diesem Beispiel verwendet Windows Energieverwaltung ein modales Meldungsfeld, um Benutzer über kritischen Akkustand zu benachrichtigen.

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
<td><strong>Richtig:</strong><br/> <img src="images/mess-notif-image10.png" alt="Screen shot of balloon showing successful updates " /><br/> In diesem Beispiel benachrichtigt Windows Update Benutzer, wenn ihr Computer erfolgreich aktualisiert wurde.<br/> <strong>Falsch:</strong><br/> <img src="images/mess-notif-image11.png" alt="Screen shot of balloon showing file check complete " /><br/> In diesem Beispiel benachrichtigt Microsoft Outlook Benutzer, wenn eine Datendateiprüfung abgeschlossen ist. Was sollen Benutzer jetzt tun? Warum sollten Benutzer vor einem erfolgreichen Abschluss ge warnen?<br/> <strong>Anzeigen, wenn:</strong> Nach Abschluss einer asynchronen Aufgabe. Benachrichtigen Sie Benutzer nur dann über erfolgreiche Aktionen, wenn sie wahrscheinlich auf den Abschluss oder nach kürzlichen Fehlern warten.<br/> <strong>Zeigen Sie, wie:</strong> Verwenden Sie die Echtzeitoption, damit diese Benachrichtigungen nicht in die Warteschlange gestellt werden, wenn Benutzer eine Vollbildanwendung ausführen oder ihren Computer nicht aktiv verwenden.<br/> <strong>Zeigen Sie an, wie oft:</strong> Einmal.<br/> <strong>Verärgerungsfaktor:</strong> Niedrig, wenn der Erfolg aufgrund von kürzlichen Fehlern nicht zu erwarten ist, ist der Erfolg nach einem kritischen oder höchst ungewöhnlichen Fehler, sodass der Benutzer zusätzliches Feedback benötigt oder auf den Abschluss wartet. hoch, wenn dies nicht der Dert ist.<br/> <strong>Alternativen:</strong> Geben Sie bei Bedarf Feedback, indem Sie ein Symbol (oder ein vorhandenes Symbol) im Benachrichtigungsbereich anzeigen, während der Vorgang ausgeführt wird. Entfernen Sie das Symbol (oder stellen Sie das vorherige Symbol wieder auf), wenn der Vorgang &quot; &quot; abgeschlossen ist. <br/></td>
</tr>
<tr class="even">
<td><strong>Aktionsfehler</strong><br/> Benachrichtigt Benutzer, wenn eine asynchrone, vom Benutzer initiierte Aktion fehlschlägt. <br/></td>
<td><strong>Richtig:</strong><br/> <img src="images/mess-notif-image12.png" alt="Screen shot of notification of failure to install " /><br/> In diesem Beispiel benachrichtigt Windows Benutzer über einen Fehler.<br/> <strong>Falsch:</strong><br/> <img src="images/mess-notif-image13.png" alt="Screen shot of notification of failure to update " /><br/> In diesem Beispiel wird Microsoft Outlook verwendet, um Benutzer über einen Fehler zu benachrichtigen, der für sie wahrscheinlich unwahrscheinlich ist.<br/> <strong>Anzeigen, wenn:</strong> Bei Einem Fehler einer asynchronen Aufgabe.<br/> <strong>Zeigen Sie an, wie oft:</strong> Einmal.<br/> <strong>Verärgerungsfaktor:</strong> Niedrig, wenn nützlich und relevant; hoch, wenn sich das Problem sofort selbst löst, oder benutzern andernfalls egal ist.<br/> <strong>Alternativen:</strong> Verwenden Sie ein modales Dialogfeld, wenn Benutzer den Fehler sofort bearbeiten müssen. <br/></td>
</tr>
<tr class="odd">
<td><strong>Nicht kritisches Systemereignis</strong><br/> Benachrichtigt Benutzer über wichtige Systemereignisse oder den Status, die zumindest vorübergehend ignoriert werden können. <br/></td>
<td><img src="images/mess-notif-image8.png" alt="Screen shot of notification of low battery power " /><br/> In diesem Beispiel Windows Benutzer vor wenig Akkustand warnen, aber es gibt noch viel Zeit, bevor sie Maßnahmen ergreifen.<br/> <strong>Anzeigen, wenn:</strong> Wenn ein Ereignis auftritt und der Benutzer aktiv ist oder eine Bedingung weiterhin besteht. Wenn dies auf ein Problem zurückt, entfernen Sie die aktuell angezeigten Benachrichtigungen sofort, sobald das Problem behoben wurde. Wie bei Aktionsbenachrichtigungen benachrichtigen Sie Benutzer nur dann über erfolgreiche Systemereignisse, wenn Benutzer wahrscheinlich auf das Ereignis warten oder nach kürzlichen Fehlern.<br/> <strong>Zeigen Sie an, wie oft:</strong> Einmal, wenn das Ereignis zum ersten Mal auftritt. Wenn dies aus einem Problem resultiert, das Benutzer lösen müssen, zeigen Sie einmal täglich erneut an.<br/> <strong>Verärgerungsfaktor:</strong> Niedrig, solange die Benachrichtigung nicht zu oft angezeigt wird.<br/> <strong>Alternativen:</strong> Wenn Benutzer ein Problem letztendlich lösen müssen, verwenden Sie progressive Eskalation, indem Sie letztendlich ein modales Dialogfeld anzeigen, wenn die Lösung obligatorisch wird. <br/></td>
</tr>
<tr class="even">
<td><strong>Optionale Benutzeraufgabe</strong><br/> Benachrichtigt Benutzer über asynchrone Aufgaben, die sie ausführen sollten. Unabhängig davon, ob die Aufgabe optional oder erforderlich ist, kann sie sicher verschoben werden. <br/></td>
<td><img src="images/mess-notif-image14.png" alt="Screen shot of notification of available updates " /><br/> In diesem Beispiel benachrichtigt Windows Update Benutzer über ein neues Sicherheitsupdate.<br/> <strong>Anzeigen, wenn:</strong> Wenn die Notwendigkeit zum Ausführen einer Aufgabe bestimmt wird und der Benutzer aktiv ist.<br/> <strong>Zeigen Sie an, wie oft:</strong> Einmal täglich für maximal drei Mal.<br/> <strong>Verärgerungsfaktor:</strong> Niedrig, solange Benutzer die Aufgabe als wichtig betrachten und die Benachrichtigung nicht zu häufig angezeigt wird.<br/> <strong>Alternativen:</strong> Wenn Benutzer die Aufgabe letztendlich ausführen müssen, verwenden Sie progressive Eskalation, indem Sie letztendlich ein modales Dialogfeld anzeigen, wenn die Aufgabe obligatorisch wird. <br/></td>
</tr>
<tr class="odd">
<td><strong>Fyi</strong><br/> Benachrichtigt Benutzer über potenziell nützliche, relevante Informationen. Sie können Benutzer über Informationen von marginaler Relevanz benachrichtigen, wenn sie optional sind und benutzer sich dafür entscheiden. <br/></td>
<td><strong>Richtig:</strong><br/> <img src="images/mess-notif-image15.png" alt="Screen shot of notification of new e-mail message " /><br/> In diesem Beispiel werden Benutzer benachrichtigt, wenn eine neue E-Mail-Nachricht empfangen wird.<br/> <strong>Richtig:</strong><br/> <img src="images/mess-notif-image16.png" alt="Screen shot of notification of contact signed in " /><br/> In diesem Beispiel werden Benutzer benachrichtigt, wenn Kontakte online benachrichtigungen, und sie haben sich entschieden, diese optionalen Informationen zu erhalten.<br/> <strong>Falsch:</strong><br/> <img src="images/mess-notif-image17.png" alt="Screen shot of notification for faster performance " /><br/> In diesem Beispiel sind die Informationen nur nützlich, wenn der Benutzer bereits hochgeschwindigkeitsbasierte USB-Anschlüsse installiert hat. Andernfalls wird der Benutzer wahrscheinlich keine anderen Möglichkeiten als das Ergebnis haben.<br/> <strong>Anzeigen, wenn:</strong> Wenn das auslösende Ereignis auftritt.<br/> <strong>Zeigen Sie, wie:</strong> Verwenden Sie die Echtzeitoption, damit diese Benachrichtigungen nicht in die Warteschlange gestellt werden, wenn Benutzer eine Vollbildanwendung ausführen oder ihren Computer nicht aktiv verwenden.<br/> <strong>Zeigen Sie an, wie oft:</strong> Einmal.<br/> <strong>Verärgerungsfaktor:</strong> Mittel bis hoch, je nachdem, wie nützlich und relevant die Benutzer sind. Nicht zu empfehlen, wenn eine geringe Wahrscheinlichkeit von Benutzer interessant ist.<br/> <strong>Alternativen:</strong> Benachrichtigen Sie Benutzer nicht. <br/></td>
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
-   **Verwenden Sie keine Benachrichtigungen während der Windows Benutzererfahrung.** Um die erste Erfahrung zu verbessern, unterdrückt Windows 7 alle Benachrichtigungen, die während der ersten Nutzungsstunden angezeigt werden. Entwerfen Sie Ihr Programm unter der Annahme, dass Benutzern keine solchen Benachrichtigungen angezeigt werden.

### <a name="what-to-notify"></a>Zu benachrichtigende Informationen

-   **Benachrichtigen Sie nicht über erfolgreiche Vorgänge, außer unter den folgenden Umständen:**
    -   **Sicherheit.** Benutzer betrachten Sicherheitsvorgänge als von größter Wichtigkeit, sodass Benutzer über erfolgreiche Sicherheitsvorgänge benachrichtigt werden.
    -   **Aktueller Fehler.** Benutzer nehmen erfolgreiche Vorgänge nicht als selbstverständlich an, wenn sie unmittelbar zuvor einen Fehler hatten. Benachrichtigen Sie daher die Benutzer über den Erfolg, wenn der Vorgang vor Kurzem fehlgeschlagen ist.
    -   **Vermeiden Sie Beeinträchtigungen.** Wenn Sie erfolgreiche Vorgänge melden, kann dies zu unnötigen Benutzern werden. Benachrichtigen Sie daher Benutzer, wenn ein erfolgreicher Vorgang auf unerwartete Weise ausgeführt wird, z. B. wenn ein Vorgang lang ist oder früher oder später als erwartet abgeschlossen wird.
-   **In anderen Fällen geben Sie entweder kein Feedback für den Erfolg oder feedback "on demand".** Angenommen, Benutzer nehmen erfolgreiche Vorgänge als selbstverständlich an. Sie können bei Bedarf Feedback geben, indem Sie ein Symbol im Benachrichtigungsbereich anzeigen (oder ein vorhandenes Symbol ändern), während der Vorgang ausgeführt wird, und das Symbol entfernen (oder das vorherige Symbol wiederherstellen), wenn der Vorgang abgeschlossen ist.
-   Geben Sie für das FYI-Muster keine Benachrichtigung aus, wenn Benutzer weiterhin normal arbeiten können oder aufgrund **der Benachrichtigung wahrscheinlich keine anderen Benachrichtigungen durchführen werden.**

    **Falsch:**

    ![Screenshot der Benachrichtigung für schnellere Leistung ](images/mess-notif-image17.png)

    In diesem Beispiel sind die Informationen nur nützlich, wenn der Benutzer bereits die Ports installiert hat. Andernfalls ist es wahrscheinlich, dass der Benutzer als Ergebnis nichts anderes tut.

    -   Ausnahme: **Sie können Benutzer über Informationen benachrichtigen, die von fraglicher Relevanz sind, wenn sie optional sind und Benutzer sich dafür entscheiden.**

        **Richtig:**

        ![Screenshot der Benachrichtigung über den angemeldeten Kontakt ](images/mess-notif-image16.png)

        In diesem Beispiel werden Benutzer benachrichtigt, wenn Kontakte online geschaltet werden und diese optionalen Informationen erhalten.

-   Verwenden Sie für nicht kritische Systemereignisse und FYI-Muster **vollständige Benachrichtigungen für ein einzelnes Ereignis.** Stellen Sie nicht mehrere Teilteiler dar.

    **Falsch:**

    ![Screenshot der Benachrichtigungen zu "Gefundene neue Hardware" ](images/mess-notif-image18.png)

    Diese Beispiele zeigen nur vier der acht Benachrichtigungen, die von Windows XP angezeigt wurden, wenn ein Benutzer eine bestimmte USB-Tastatur anfügt, die jeweils inkrementell weitere Informationen darstellen.

    **Richtig:**

    ![Screenshot der Benachrichtigungen zum Installationsstatus ](images/mess-notif-image19.png)

    In diesem Beispiel führt das Anfügen einer USB-Tastatur zu zwei vollständigen Benachrichtigungen.

### <a name="when-to-notify"></a>Zeitpunkt der Benachrichtigung

-   **Zeigen Sie eine Benachrichtigung basierend auf ihrem Entwurfsmuster an:**



| Muster              | Zeitpunkt der Benachrichtigung          |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktion erfolgreich<br/>            | Nach Abschluss einer asynchronen Aufgabe. Benachrichtigen Sie Benutzer nur dann über erfolgreiche Aktionen, wenn sie wahrscheinlich auf den Abschluss oder nach kürzlichen Fehlern warten.<br/>                                             |
| Aktionsfehler<br/>            | Bei einem Fehler einer asynchronen Aufgabe.<br/>                                                                                                                                                                   |
| Nicht kritisches Systemereignis<br/> | Wenn ein Ereignis auftritt und der Benutzer aktiv ist oder die Bedingung weiterhin vorhanden ist. Wenn dies auf ein Problem hinweist, entfernen Sie die aktuell angezeigte Benachrichtigung sofort, sobald das Problem behoben wurde.<br/> |
| Optionale Benutzeraufgabe<br/>        | Wenn die Notwendigkeit zum Ausführen einer Aufgabe bestimmt wird und der Benutzer aktiv ist.<br/>                                                                                                                                   |
| Fyi<br/>                       | Wenn das auslösende Ereignis auftritt.<br/>                                                                                                                                                                       |



 

-   Wenn sich das Problem für das Aktionsfehlermuster innerhalb von Sekunden beheben lässt, verzögern Sie **die Fehlerbenachrichtigung um einen angemessenen Zeitraum.** Wenn sich das Problem selbst behebt, melden Sie nichts. Benachrichtigen Sie erst, nachdem genügend Zeit verstrichen ist, dass der Fehler wahrnehmbar ist. Wenn Sie zu früh melden, werden Benutzer das gemeldete Problem wahrscheinlich nicht bemerken, aber sie bemerken die unnötige Benachrichtigung.

**Falsch:**

![Screenshot: Keine Netzwerkverbindungsbenachrichtigung ](images/mess-notif-image20.png)

Wenn unmittelbar darauf Folgendes folgt:

![Screenshot der erfolgreichen Benachrichtigung über die Verbindung ](images/mess-notif-image21.png)

In diesem Beispiel ist in Windows Vista die Benachrichtigung, dass keine Drahtloskonnektivität vorhanden ist, vorzeitig, da häufig unmittelbar darauf eine Benachrichtigung über eine gute Konnektivität folgt.

-   Verwenden Sie für die Aktionserfolgs- und **FYI-Muster die Echtzeitoption, damit veraltete Benachrichtigungen nicht in die Warteschlange eingereiht werden,** wenn Benutzer eine Vollbildanwendung ausführen oder ihren Computer nicht aktiv verwenden.
-   Erstellen Sie für das nicht kritische Systemereignismuster **nicht das Potenzial für Benachrichtigungss storms, indem Sie Ereignisse staffeln, die an bekannte Ereignisse wie die Benutzeranmeldung gebunden sind.** Binden Sie das Ereignis stattdessen an einen Bestimmten Zeitraum nach dem Ereignis. Beispielsweise können Sie Benutzer fünf Minuten nach der Benutzeranmeldung daran erinnern, Ihr Produkt zu registrieren.

### <a name="how-long-to-notify"></a>Benachrichtigungsdauer

In Windows Vista und höher werden Benachrichtigungen für eine feste Dauer von 9 Sekunden angezeigt.

### <a name="how-often-to-notify"></a>Benachrichtigungshäufige Benachrichtigung

-   **Die Anzahl der Anzeigezeiten einer Benachrichtigung basiert auf ihrem Entwurfsmuster:**



| Muster           | Benachrichtigungshäufige Benachrichtigung  |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Aktion erfolgreich<br/>            | Einmal.<br/>                                                                                                            |
| Aktionsfehler<br/>            | Einmal.<br/>                                                                                                            |
| Nicht kritisches Systemereignis<br/> | Einmal, wenn das Ereignis zum ersten Mal auftritt. Wenn dies auf ein Problem resultiert, das Benutzer lösen müssen, sollten Sie es einmal täglich erneut anzeigen.<br/> |
| Optionale Benutzeraufgabe<br/>        | Maximal dreimal pro Tag.<br/>                                                                         |
| Fyi<br/>                       | Einmal.<br/>                                                                                                            |



 

-   **Versuchen Sie bei optionalen Benutzeraufgaben nicht, Benutzer durch ständiges Anzeigen von Benachrichtigungen in die Übermittlung zu überfallen.** Wenn die Aufgabe erforderlich ist, zeigen Sie sofort ein modales Dialogfeld an, anstatt Benachrichtigungen zu verwenden.

### <a name="notification-escalation"></a>Eskalation von Benachrichtigungen

-   **Gehen Sie nicht davon aus, dass Benutzern Ihre Benachrichtigungen angezeigt werden.** Benutzer werden in den folgenden Folgenden nicht angezeigt:
    -   Sie werden in ihrer Arbeit unterstützt.
    -   Sie achten nicht darauf.
    -   Sie sind von ihrem Computer entfernt.
    -   Sie führen eine Vollbildanwendung aus.
    -   Der Administrator hat alle Benachrichtigungen für den Computer deaktiviert.
-   **Wenn Benutzer letztendlich eine Aktion ausführen müssen, verwenden Sie die progressive Eskalation,** um eine alternative Benutzeroberfläche anzuzeigen, die Benutzer nicht ignorieren können.

### <a name="interaction"></a>Interaktion

-   **Aktivieren Sie Benachrichtigungen, wenn:**
    -   **Benutzer sollten eine Aktion ausführen.** Wenn Sie auf die Benachrichtigung klicken, sollte ein Fenster angezeigt werden, in dem Benutzer die Aktion ausführen können. Dieser Ansatz wird für den Aktionsfehler und optionale Entwurfsmuster für Benutzeraufgaben bevorzugt.
    -   **Benutzer möchten möglicherweise weitere Informationen anzeigen.** Wenn Sie auf die Benachrichtigung klicken, sollte ein Fenster angezeigt werden, in dem Benutzer zusätzliche Informationen anzeigen können.
-   **Zeigen Sie immer ein Fenster an, wenn Benutzer auf klicken, um eine Aktion auszuführen.** Wenn Sie nicht klicken, führen Sie eine Aktion direkt aus.
-   **Wenn Sie auf klicken, um weitere Informationen anzuzeigen, sollten immer weitere Informationen angezeigt werden.** Rephrase nicht nur die Informationen, die bereits in der Benachrichtigung enthalten sind.

### <a name="icons"></a>Symbole

-   **Verwenden Sie für das Aktionsfehlermuster das Standardfehlersymbol.**
-   **Verwenden Sie für die nicht kritischen Systemereignismuster das Standardwarnungssymbol.**
-   Verwenden Sie für **andere Muster Symbole, die Objekte zeigen, die sich auf das Subjekt beziehen oder vorschlagen,** z. B. einen Schutz für die Sicherheit oder einen Akku für den Strom.
-   **Verwenden Sie Symbole basierend auf Ihrer Anwendung oder Ihrem Unternehmensbranding, wenn Ihre Zielbenutzer sie erkennen und es keine bessere Alternative gibt.**
-   Erwägen Sie für die progressive Eskalation die **Verwendung von Symbolen mit einer zunehmend emphatischen Darstellung, wenn die Situation dringender wird.**
-   **Verwenden Sie nicht das Standardinformationssymbol.** Dass es sich bei Benachrichtigungen um Informationen handelt, ist selbstverständlich.
-   **Erwägen Sie die Verwendung großer Symbole (32 x 32 Pixel), wenn:**
    -   Benutzer werden das Symbol und nicht den Text schnell verstehen.
    -   Die großen Symbole vermitteln ihre Bedeutung eindeutiger und effektiver als die standardmäßigen Symbole mit 16 x 16 Pixeln.
    -   Das Symbol verwendet die [Stilvorlage " "](vis-icons.md)" .

![Screenshot der Benachrichtigung "Wichtige Nachrichten" ](images/mess-notif-image22.png)

In diesem Beispiel können Benutzer die Art der Benachrichtigung mit einem Blick auf das große Symbol schnell nachvollziehen.

### <a name="notification-queuing"></a>Notification Queuing

**Hinweis:** Benachrichtigungen werden in die Warteschlange eingereiht, wenn sie nicht sofort angezeigt werden können, z. B. wenn eine andere Benachrichtigung angezeigt wird, der Benutzer eine Vollbildanwendung ausführt oder der Benutzer den Computer nicht aktiv verwendet. Echtzeitbenachrichtigungen verbleiben nur 60 Sekunden lang in der Warteschlange.

-   **Verwenden Sie für die Aktionserfolgs- und FYI-Muster die Echtzeitoption,** damit die Benachrichtigung nicht lange in die Warteschlange eingereiht wird. Diese Benachrichtigungen haben nur dann einen Wert, wenn sie sofort angezeigt werden können.
-   **Entfernen Sie Benachrichtigungen in der Warteschlange, wenn sie nicht mehr relevant sind.**
-   **Entwickler:** Hierzu können Sie das NIF \_ INFO-Flag in uFlags festlegen und szInfo auf eine leere Zeichenfolge festlegen. Dies kann nicht beeinträchtigt werden, wenn sich die Benachrichtigung nicht mehr in der Warteschlange befindet.

### <a name="system-integration"></a>Systemintegration

-   Wenn Ihre Anwendung während der Ausführung nicht immer über ein Symbol im [Benachrichtigungsbereich](winenv-notification.md) verfügen soll, zeigen Sie **während der asynchronen Aufgabe oder des Ereignisses, die bzw. das die Benachrichtigung verursacht hat, vorübergehend ein Symbol an.**

## <a name="text"></a>Text

### <a name="title-text"></a>Titeltext

-   **Verwenden Sie den Titeltext, der kurz die wichtigsten Informationen zusammenfasst, die Sie für die Kommunikation mit Benutzern in einer eindeutigen, einfachen, präzisen, spezifischen Sprache benötigen.** Benutzer sollten den Zweck der Benachrichtigungsinformationen schnell und mit minimalem Aufwand verstehen können.
-   **Verwenden Sie Textfragmente oder vollständige Sätze ohne endende Interpunktion.**
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
-   **Verwenden Sie nicht mehr als 48 Zeichen (in englischer Sprache), um die Lokalisierung zu ermöglichen.** Der Titel hat eine maximale Länge von 63 Zeichen, aber Sie müssen eine Erweiterung von 30 Prozent zulassen, wenn der englischsprachige Text übersetzt wird.

### <a name="body-text"></a>Textkörper

-   **Verwenden Sie Text, der eine Beschreibung enthält (ohne die Informationen im Titel zu wiederholen), und optional , der bestimmte Details zur Benachrichtigung liefert und Benutzer darüber informiert, welche Aktion verfügbar ist.**
-   **Verwenden Sie vollständige Sätze mit endender Interpunktion.**
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
-   **Verwenden Sie nicht mehr als 200 Zeichen (auf Englisch), um die Lokalisierung zu ermöglichen.** Der Textkörper hat eine maximale Länge von 255 Zeichen, aber Sie müssen eine Erweiterung von 30 Prozent zulassen, wenn der englischsprachige Text übersetzt wird.
-   **Fügen Sie wichtige Informationen in den Textkörper ein, z. B. bestimmte Objektnamen.** (Beispiele: Benutzernamen, Dateinamen oder URLs.) Benutzer sollten kein weiteres Fenster öffnen müssen, um solche Informationen zu finden.
-   **Setzen Sie Objektnamen in doppelte Anführungszeichen.**
    -   **Ausnahme:** Verwenden Sie keine Anführungszeichen, wenn:
        -   Der Objektname verwendet immer [die Groß-/Großschreibung im Titelformat,](glossary.md)z. B. mit Benutzernamen.
        -   Der Objektname wird durch einen Doppelpunkt versetzt (Beispiel: Druckername: Mein Drucker).
        -   Der Objektname kann leicht aus dem Kontext bestimmt werden.
-   **Wenn Sie Objektnamen auf eine feste maximale Größe abschneiden müssen, um die Lokalisierung zu ermöglichen, verwenden Sie eine Auslassungszeichen, um auf abgeschnittene Daten hinzuweisen.**

    ![Screenshot der Meldung, die den verkürzten Namen enthält ](images/mess-notif-image23.png)

    In diesem Beispiel wird ein Objektname mithilfe von Auslassungszeichen abgeschnitten.

-   **Verwenden Sie den folgenden Ausdruck, wenn die Benachrichtigung umsetzbar ist:**
    -   Wenn Benutzer auf die Benachrichtigung klicken können, um eine Aktion auszuführen:

        < kurze Beschreibung der grundlegenden Informationen>

        <optional details>

        Klicken Sie auf <do something> .

        ![Screenshot der Meldung: "Klicken Sie, um den Fortschritt anzuzeigen". ](images/mess-notif-image24.png)

        In diesem Beispiel können Benutzer auf klicken, um eine Aktion auszuführen.

    -   Wenn Benutzer auf die Benachrichtigung klicken können, um weitere Informationen anzuzeigen:

        < kurze Beschreibung der grundlegenden Informationen>

        <optional details>

        Klicken Sie auf , um weitere Informationen zu erfahren.

        ![Screenshot der Meldung: Klicken Sie auf , um weitere Informationen zu erhalten. ](images/mess-notif-image25.png)

        In diesem Beispiel können Benutzer auf klicken, um weitere Informationen zu erhalten.

-   **Geben Sie nicht an, dass der Benutzer eine Aktion in einer Benachrichtigung ausführen muss.** Benachrichtigungen sind für nicht kritische Informationen vorgesehen, die Benutzer frei ignorieren können. Wenn Benutzer wirklich eine Aktion ausführen müssen, verwenden Sie keine Benachrichtigungen.
-   **Wenn Benutzer eine Aktion ausführen sollen, machen Sie die Wichtigkeit deutlich.**
-   Beschreiben Sie Probleme für Aktionsfehler und nicht kritische Systemereignismuster **in einfacher Sprache.**

    **Falsch:**

    ![Screenshot der langen, komplexen Meldung ](images/mess-notif-image26.png)

    In diesem Beispiel wird das Problem mit einer zu technischen, aber nicht spezifischen Sprache beschrieben.

    **Richtig:**

    ![Screenshot: klare, präzise Meldung ](images/mess-notif-image27.png)

    In diesem Beispiel wird das Problem in einfacher Sprache beschrieben.

-   **Beschreiben Sie das Ereignis auf eine Weise, die für die Zielbenutzer relevant ist.** Eine Benachrichtigung ist relevant, wenn es eine angemessene Wahrscheinlichkeit gibt, dass Benutzer eine Aufgabe ausführen oder ihr Verhalten als Ergebnis der Benachrichtigung ändern. Sie können dies häufig erreichen, indem Sie Benachrichtigungen in Bezug auf Benutzerziele anstelle von technologischen Problemen beschreiben.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Benachrichtigungen:

-   Verwenden Sie den genauen Titeltext, einschließlich der Groß-/Großschreibung.
-   Verweisen Sie auf die Komponente als Benachrichtigung, nicht als Sprechblase oder Warnung.
-   Um die Benutzerinteraktion zu beschreiben, klicken Sie auf .
-   Formatieren Sie den Titeltext nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie den Titel nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

Beispiel: Wenn die Benachrichtigung **Kritische Updates sind installationsbereit** angezeigt wird, klicken Sie auf die Benachrichtigung, um den Prozess zu starten.

Beim Verweisen auf den Benachrichtigungsbereich:

-   Verweisen Sie auf den Infobereich als Infobereich, nicht auf die Taskleiste.

 

