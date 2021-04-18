---
title: Benachrichtigungen (Entwurfs Grundlagen)
description: Eine Benachrichtigung informiert Benutzer über Ereignisse, die nicht mit der aktuellen Benutzeraktivität in Zusammenhang stehen, indem eine Sprechblase von einem Symbol im Benachrichtigungsbereich kurz angezeigt wird.
ms.assetid: dcac2fb7-e503-4ea3-a2c5-e3cb660c040a
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5de312b33a970245d2f6f410e55a891c286d9aa7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104558775"
---
# <a name="notifications-design-basics"></a>Benachrichtigungen (Entwurfs Grundlagen)

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Eine Benachrichtigung informiert Benutzer über Ereignisse, die nicht mit der aktuellen Benutzeraktivität in Zusammenhang stehen, indem eine Sprechblase von einem Symbol im Benachrichtigungsbereich kurz angezeigt wird. Die Benachrichtigung kann aus einer Benutzeraktion oder einem signifikanten System Ereignis resultieren oder potenziell nützliche Informationen von Microsoft Windows oder einer Anwendung bereitstellen.

Die Informationen in einer Benachrichtigung sind **hilfreich und relevant, aber nie kritisch.** Folglich ist für Benachrichtigungen keine sofortige Benutzeraktion erforderlich, und Benutzer können Sie frei ignorieren.

![Screenshot der Sprechblase mit "neue Updates" im Titel ](images/mess-notif-image1.png)

Eine typische Benachrichtigung.

In Windows Vista und höher werden Benachrichtigungen für eine Dauer von 9 Sekunden angezeigt. Benachrichtigungen werden nicht sofort angezeigt, wenn Benutzer inaktiv sind oder Bildschirmschoner ausgeführt werden. Während dieser Zeit werden Benachrichtigungen von Windows automatisch in die Warteschlange eingereiht und die Benachrichtigungen in der Warteschlange angezeigt, wenn der Benutzer reguläre Aktivitäten fortsetzt. Folglich müssen Sie nichts tun, um diese besonderen Umstände zu behandeln.

**Entwickler:** Mithilfe der shqueryusernotificationstate-API können Sie feststellen, wann der Benutzer aktiv ist.

**Hinweis:** Die Richtlinien im Zusammenhang mit dem [Benachrichtigungsbereich](winenv-notification.md), der [Taskleiste](winenv-taskbar.md)und den [Ballons](ctrl-balloons.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Handelt es sich bei den Informationen um das unmittelbare, direkte Ergebnis der Interaktion von Benutzern mit Ihrer Anwendung?** Wenn dies der Fall ist, können Sie diese synchronen Informationen direkt in der Anwendung [anzeigen, indem](ctrl-balloons.md)Sie stattdessen ein [Dialogfeld](win-dialog-box.md), ein Meldungs [Feld](glossary.md), eine Sprech [Blase oder eine](glossary.md) Benutzer Benachrichtigungen sind nur für asynchrone Informationen vorgesehen.

![Screenshot der Windows-Sicherheitswarnung ](images/mess-notif-image2.png)

In diesem Beispiel wird das Dialogfeld Windows-Firewall-Ausnahmen als direktes Ergebnis der Benutzerinteraktion angezeigt. Eine Benachrichtigung wäre hier nicht angebracht.

-   **Sind die Informationen nur relevant, wenn Benutzer Ihre Anwendung aktiv verwenden?** Wenn dies der Fall ist, zeigen Sie die Informationen in der [Statusleiste](ctrl-status-bars.md) Ihrer Anwendung oder in einem anderen Statusbereich an.

![Screenshot der Outlook-Statusleiste ](images/mess-notif-image3.png)

In diesem Beispiel zeigt Outlook seine Verbindung und den Synchronisierungs Status in der Statusleiste an.

-   **Ändern sich die Informationen schnell, kontinuierlich Echtzeitinformationen?** Beispiele hierfür sind der Verarbeitungs Fortschritt, Aktienkurse und Sportergebnisse. Wenn dies der Fall ist, verwenden Sie keine Benachrichtigungen, da Sie sich nicht für schnell veränderliche Informationen eignen.
-   **Sind die Informationen hilfreich und relevant? Können Benutzer ihr Verhalten wahrscheinlich ändern oder Unannehmlichkeiten vermeiden, wenn Sie die Informationen erhalten?** Wenn dies nicht der Fall ist, werden die Informationen entweder nicht angezeigt, oder Sie werden nicht in einem Statusfenster oder einer Protokolldatei abgelegt
-   **Sind die Informationen wichtig? Ist eine sofortige Aktion erforderlich?** Wenn dies der Fall ist, zeigen Sie die Informationen unter Verwendung einer Schnittstelle an, die eine Aufmerksamkeit erfordert und nicht leicht ignoriert werden kann, wie z. b. ein modales Dialogfeld Wenn das Programm nicht aktiv ist, können Sie auf die kritischen Informationen aufmerksam machen, indem Sie [die Task leisten Schaltfläche des Programms dreimal blinkt](winenv-taskbar.md) und so lange hervorgehoben lassen, bis das Programm aktiv ist.
-   **Sind die primären Ziel Benutzer IT-Experten?** Wenn dies der Fall ist, verwenden Sie einen alternativen Feedback Mechanismus wie [Protokolldatei](glossary.md) Einträge oder e-Mail-Nachrichten. IT-Experten bevorzugen Protokolldateien für nicht wichtige Informationen. Außerdem werden Server häufig remote verwaltet und in der Regel ohne angemeldete Benutzer ausgeführt, sodass Benachrichtigungen nicht wirksam werden.

## <a name="design-concepts"></a>Entwurfskonzepte

Effektive Benachrichtigungen, die eine gute Benutzer Leistung bieten, sind folgende:

-   **Asynchronen.** Das Ereignis ist kein unmittelbares direktes Ergebnis der aktuellen Interaktion von Benutzern mit Microsoft Windows oder Ihrer Anwendung.
-   **Lichem.** Es besteht die Möglichkeit, dass Benutzer eine Aufgabe ausführen oder Ihr Verhalten im Ergebnis der Benachrichtigung ändern.
-   **Dienliche.** In der Benachrichtigung werden hilfreiche Informationen angezeigt, die für Benutzer wichtig sind und die Sie nicht bereits kennen.
-   **Nicht kritisch.** Benachrichtigungen sind nicht modal und erfordern keine Benutzerinteraktion, sodass Sie von Benutzern frei ignoriert werden können.
-   **Verwertbare.** Für Benachrichtigungen, die die Durchführung einer Aktion vorschlagen, wird diese Aktion initiiert, indem Sie auf die Benachrichtigung klicken. Die Aktion kann jedoch immer verschoben werden.
-   **Entsprechend dargestellt.** Die Darstellung der Benachrichtigung (Dauer, Häufigkeit, Text, Symbol und Interaktivität) entspricht den Bedingungen.
-   **Nicht ärgerlich!** Es gibt eine feine Linie zwischen dem Hinweis, dass Benutzer über ein Ereignis informiert werden und ein Abgleich erfolgt.

Leider gibt es zu viele lästige, ungeeignete und nutzlose, irrelevante Benachrichtigungen. Beachten Sie diese Benachrichtigungen aus der Windows XP-Hall:

![Screenshot der "Tour Windows XP"-Benachrichtigung ](images/mess-notif-image4.png)

![Screenshot der Benachrichtigung "nicht verwendete Symbole" ](images/mess-notif-image5.png)

![Screenshot der Benachrichtigung ".NET Passport hinzufügen" ](images/mess-notif-image6.png)

In diesen Beispielen versucht Windows XP, Benutzer bei der Erstkonfiguration zu unterstützen. Diese Benachrichtigungen werden jedoch viel zu häufig und auch nach Ihren nützlichen Anforderungen angezeigt, sodass Sie nicht mehr als unerwünschte Merkmals Ankündigungen sind.

## <a name="user-flow-must-be-maintained"></a>Der benutzerflow muss gewartet werden.

**Im Idealfall sehen Benutzer, die in Ihre Arbeit eintauchen, Ihre Benachrichtigungen überhaupt nicht. Stattdessen werden Ihre Benachrichtigungen nur angezeigt, wenn Ihr Flow bereits beschädigt ist.**

Im Flow: die Psychologie der optimalen Darstellung, Mihaly Csikszentmihalyi, besagt, dass Benutzer einen Flow-Status eingeben, wenn Sie vollständig in Aktivität aufgenommen werden, in der Sie Ihren Zeitverlust verlieren und eine hohe Zufriedenheit aufweisen.

**Effektive Benachrichtigungen helfen Benutzern, Ihren Flow aufrechtzuerhalten, indem Sie nützliche, relevante Informationen darstellen, die leicht ignoriert werden können.** Die Benachrichtigungen werden mit niedriger Schlüssel und Peripherie dargestellt, und Sie erfordern keine Interaktion.

Gehen Sie nicht davon aus, dass bei Benachrichtigungen [nicht eine lästige Unterbrechung](glossary.md) auftreten kann. Benachrichtigungen erfordern keine Aufmerksamkeit von Benutzern, Sie fordern Sie aber sicherlich an. Sie können den Flow von Benutzern durch folgende Aktionen unterbrechen:

-   Anzeigen von Benachrichtigungen, die Benutzern nicht wichtig sind.
-   Eine zu oft angezeigte Benachrichtigung.
-   Verwenden mehrerer Benachrichtigungen, wenn eine einzelne Benachrichtigung ausreicht.
-   Verwenden von Sound beim Anzeigen einer Benachrichtigung.

In Windows 7 haben Benutzer eine ultimative Kontrolle über Benachrichtigungen. **Wenn Benutzer feststellen, dass die Benachrichtigungen eines Programms zu lästig sind, können Sie auswählen, dass alle Benachrichtigungen von diesem Programm unterdrückt werden sollen.** Stellen Sie sicher, dass Benutzer dies nicht für Ihr Programm tun, indem Sie nützliche, relevante Informationen und die folgenden Richtlinien befolgen.

## <a name="notifications-must-be-ignorable"></a>Benachrichtigungen müssen Ignorable sein.

**Benachrichtigungen erfordern keine sofortige Benutzeraktion und können von Benutzern frei ignoriert werden.**

Entwickler und Designer möchten Ihre Benachrichtigungen häufig auf eine Weise präsentieren, die Benutzer nicht ignorieren können. Dieses Ziel unterbricht den primären Vorteil von Benachrichtigungen vollständig, da der Benutzer den Fluss beeinträchtigen würde. Wenn Benutzer durch Ihre Benachrichtigungen abgelenkt sind oder sich dazu verpflichtet sind, Sie zu lesen, ist Ihr Benachrichtigungs Entwurf fehlgeschlagen.

**Wenn Sie Bedenken haben, dass Benutzer Ihre Benachrichtigungen ignorieren, berücksichtigen Sie Folgendes:**

-   Wenn Sie Benachrichtigungen ordnungsgemäß verwenden und keine sofortige Benutzeraktion erforderlich sind, ist das Ignorieren der Benutzer die Möglichkeit, Sie zu ignorieren. Ändern Sie dies nicht.
-   Wenn das Ereignis sofortige Benutzeraktionen erfordert, verwenden Sie eine alternative Benutzeroberfläche (UI), die Benutzer nicht ignorieren können. Weitere Informationen finden Sie unter ist dies die richtige Benutzeroberfläche? für die Alternativen.

## <a name="use-progressive-escalation-where-applicable"></a>Verwenden Sie ggf. Progressive Eskalation

Wenn eine Benachrichtigung für ein Ereignis verwendet wird, das von Benutzern zuerst sicher ignoriert werden kann, aber letztendlich behoben werden muss, sollte eine alternative Benutzeroberfläche verwendet werden, wenn die Situation kritisch wird. Diese Technik wird als Progressive Eskalation bezeichnet.

Das Windows-Energie Verwaltungssystem gibt z. b. anfänglich eine geringe Akkukapazität an, indem einfach das Benachrichtigungs Bereichs Symbol geändert wird.

![Screenshot von sechs Symbolen mit dem Akku Status ](images/mess-notif-image7.png)

In diesen Beispielen verwendet die Windows-Energie Verwaltung das Benachrichtigungs Bereichs Symbol, um Benutzer über eine progressiver Stromversorgung zu benachrichtigen.

Da der Akku Betrieb niedriger wird, warnt Windows mithilfe einer Benachrichtigung bei den Benutzern der schwachen Akkuleistung.

![Screenshot der Benachrichtigung über eine geringe Akkuleistung](images/mess-notif-image8.png)

In diesem Beispiel verwendet die Windows-Energie Verwaltung eine Benachrichtigung, um Benutzer darüber zu informieren, dass die Akkuleistung schwach ist.

Diese Benachrichtigung wird angezeigt, während die Benutzer immer noch über mehrere Optionen verfügen. Benutzer können Plug-ins, ihre Energieoptionen ändern, ihre Arbeit einbinden und den Computer Herunterfahren oder die Benachrichtigung ignorieren und die Arbeit fortsetzen. Da der Akku Betrieb weiterhin abläuft, entsprechen der Text und das Symbol der Benachrichtigung der zusätzlichen Dringlichkeit. Sobald der Akku Betrieb jedoch so gering ist, dass Benutzer sofort agieren müssen, benachrichtigt die Windows-Energie Verwaltung Benutzer über ein [modales](glossary.md) Meldungs Feld.

![Screenshot von sehr wenig Akku Strom (Warnung)](images/mess-notif-image9.png)

In diesem Beispiel verwendet die Windows-Energie Verwaltung ein modales Meldungs Feld, um Benutzer über eine äußerst geringe Akkuleistung zu benachrichtigen.

**Wenn Sie nur drei Dinge tun...**

1.  Verwenden Sie Benachrichtigungen nur, wenn dies wirklich erforderlich ist. Wenn Sie eine Benachrichtigung anzeigen, unterbrechen Sie möglicherweise Benutzer, oder Sie können Sie sogar stören. Stellen Sie sicher, dass die Unterbrechung gerechtfertigt ist.
2.  Verwenden Sie Benachrichtigungen für nicht kritische Ereignisse oder Situationen, in denen keine sofortige Benutzeraktion erforderlich ist. Verwenden Sie bei kritischen Ereignissen oder Situationen, in denen eine sofortige Benutzeraktion erforderlich ist, eine alternative Benutzeroberfläche (z. b. ein modales Dialogfeld).
3.  Wenn Sie Benachrichtigungen verwenden, machen Sie eine gute Benutzer Leistung. Versuchen Sie nicht, Benutzer zu zwingen, Ihre Benachrichtigungen anzuzeigen. Wenn Benutzer so in Ihre Arbeit eintauchen, dass Ihre Benachrichtigungen nicht angezeigt werden, ist Ihr Entwurf gut.

## <a name="usage-patterns"></a>Verwendungsmuster

Benachrichtigungen weisen mehrere Verwendungs Muster auf:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Aktion erfolgreich</strong><br/> Benachrichtigt Benutzer, wenn eine asynchrone, vom Benutzer initiierte Aktion erfolgreich abgeschlossen wird. <br/></td>
<td><strong>Richtig:</strong><br/> <img src="images/mess-notif-image10.png" alt="Screen shot of balloon showing successful updates " /><br/> In diesem Beispiel werden Benutzer von Windows Update benachrichtigt, wenn Ihr Computer erfolgreich aktualisiert wurde.<br/> <strong>Falsch:</strong><br/> <img src="images/mess-notif-image11.png" alt="Screen shot of balloon showing file check complete " /><br/> In diesem Beispiel werden Benutzer von Microsoft Outlook benachrichtigt, wenn eine Datendatei Überprüfung beendet ist. Was sollen Benutzer jetzt tun? Und warum sollten Benutzer vor erfolgreichem Abschluss gewarnt werden?<br/> <strong>Anzeigen in:</strong> Bei Abschluss einer asynchronen Aufgabe. Benachrichtigen von Benutzern über erfolgreiche Aktionen nur, wenn Sie wahrscheinlich auf den Abschluss warten oder nach dem letzten Fehler.<br/> <strong>Zeigen</strong> Sie Folgendes an: Verwenden Sie die Echt Zeit Option, sodass diese Benachrichtigungen nicht in die Warteschlange eingereiht werden, wenn Benutzer eine Vollbildanwendung ausführen oder nicht aktiv Ihren Computer verwenden.<br/> Häufigkeit <strong>anzeigen:</strong> Einmal.<br/> <strong>Ärgernisfaktor:</strong> Niedrig, wenn der Erfolg aufgrund aktueller Fehler nicht erwartet wird. der Erfolg liegt nach einem kritischen oder sehr ungewöhnlichen Fehler, sodass der Benutzer zusätzliches Feedback benötigt oder der Benutzer auf den Abschluss wartet. hoch, wenn nicht.<br/> <strong>Alternativen:</strong> Geben &quot; Sie Feedback bei Bedarf an &quot; , indem Sie ein Symbol (oder ein vorhandenes Symbol) im Benachrichtigungsbereich anzeigen, während der Vorgang ausgeführt wird. entfernen Sie das Symbol (oder stellen Sie das vorherige Symbol wieder her), wenn der Vorgang beendet ist. <br/></td>
</tr>
<tr class="even">
<td><strong>Aktions Fehler</strong><br/> Benachrichtigt Benutzer, wenn eine asynchrone, vom Benutzer initiierte Aktion fehlschlägt. <br/></td>
<td><strong>Richtig:</strong><br/> <img src="images/mess-notif-image12.png" alt="Screen shot of notification of failure to install " /><br/> In diesem Beispiel werden Benutzer von der Windows-Aktivierung benachrichtigt, wenn ein Fehler aufgetreten ist.<br/> <strong>Falsch:</strong><br/> <img src="images/mess-notif-image13.png" alt="Screen shot of notification of failure to update " /><br/> In diesem Beispiel wurde Microsoft Outlook verwendet, um Benutzer über einen Fehler zu benachrichtigen, der für Sie wahrscheinlich nicht relevant ist.<br/> <strong>Anzeigen in:</strong> Bei einem Fehler bei einer asynchronen Aufgabe.<br/> Häufigkeit <strong>anzeigen:</strong> Einmal.<br/> <strong>Ärgernisfaktor:</strong> Niedrig, wenn hilfreich und relevant; hoch, wenn sich das Problem sofort selbst löst, oder wenn es für Benutzer keine Rolle spielt.<br/> <strong>Alternativen:</strong> Verwenden Sie ein modales Dialogfeld, wenn Benutzer den Fehler sofort beheben müssen. <br/></td>
</tr>
<tr class="odd">
<td><strong>Nicht kritisches System Ereignis</strong><br/> Benachrichtigt Benutzer über wichtige Systemereignisse oder den Status, die ohne weiteres ignoriert werden können, zumindest vorübergehend. <br/></td>
<td><img src="images/mess-notif-image8.png" alt="Screen shot of notification of low battery power " /><br/> In diesem Beispiel warnt Windows die Benutzer mit geringer Akkuleistung, aber es gibt noch viel Zeit, bevor Sie Maßnahmen ergreifen können.<br/> <strong>Anzeigen in:</strong> Wenn ein Ereignis auftritt und der Benutzer aktiv ist oder eine Bedingung weiterhin vorhanden ist. Wenn ein Problem vorliegt, entfernen Sie die derzeit angezeigten Benachrichtigungen sofort, sobald das Problem behoben ist. Benachrichtigen Sie wie bei Aktions Benachrichtigungen auch Benutzer über erfolgreiche Systemereignisse, wenn Benutzer wahrscheinlich auf das Ereignis oder nach den letzten Fehlern warten.<br/> Häufigkeit <strong>anzeigen:</strong> Wenn das Ereignis das erste Mal auftritt. Wenn dies ein Problem ergibt, das von Benutzern gelöst werden muss, müssen Sie einmal am Tag eine erneute Anzeige durchführen.<br/> <strong>Ärgernisfaktor:</strong> Niedrig, solange die Benachrichtigung nicht zu häufig angezeigt wird.<br/> <strong>Alternativen:</strong> Wenn Benutzer ein Problem schließlich beheben müssen, verwenden Sie die Progressive Eskalation, indem Sie letztendlich ein modales Dialogfeld anzeigen, wenn die Auflösung obligatorisch wird. <br/></td>
</tr>
<tr class="even">
<td><strong>Optionale Benutzer Aufgabe</strong><br/> Benachrichtigt Benutzer über asynchrone Aufgaben, die Sie ausführen sollten. Ob optional oder erforderlich, der Task kann problemlos verschoben werden. <br/></td>
<td><img src="images/mess-notif-image14.png" alt="Screen shot of notification of available updates " /><br/> In diesem Beispiel benachrichtigt Windows Update Benutzer über ein neues Sicherheits Update.<br/> <strong>Anzeigen in:</strong> Die Notwendigkeit, eine Aufgabe auszuführen, wird bestimmt, und der Benutzer ist aktiv.<br/> Häufigkeit <strong>anzeigen:</strong> Einmal pro Tag für maximal drei Mal.<br/> <strong>Ärgernisfaktor:</strong> Niedrig, solange die Benutzer die Aufgabe als wichtig betrachtet haben und die Benachrichtigung nicht zu häufig angezeigt wird.<br/> <strong>Alternativen:</strong> Wenn Benutzer die Aufgabe letztendlich ausführen müssen, verwenden Sie die Progressive Eskalation, indem Sie letztendlich ein modales Dialogfeld anzeigen, wenn der Task obligatorisch wird. <br/></td>
</tr>
<tr class="odd">
<td><strong>Zur Kenntnisnahme</strong><br/> Benachrichtigt Benutzer über potenziell nützliche, relevante Informationen. Sie können Benutzer über Informationen über die marginale Relevanz Benachrichtigen, wenn dies optional ist und Benutzer sich anmelden. <br/></td>
<td><strong>Richtig:</strong><br/> <img src="images/mess-notif-image15.png" alt="Screen shot of notification of new e-mail message " /><br/> In diesem Beispiel werden Benutzer benachrichtigt, wenn eine neue e-Mail-Nachricht empfangen wird.<br/> <strong>Richtig:</strong><br/> <img src="images/mess-notif-image16.png" alt="Screen shot of notification of contact signed in " /><br/> In diesem Beispiel werden Benutzer benachrichtigt, wenn Kontakte online geschaltet werden, und Sie haben sich entschieden, diese optionalen Informationen zu erhalten.<br/> <strong>Falsch:</strong><br/> <img src="images/mess-notif-image17.png" alt="Screen shot of notification for faster performance " /><br/> In diesem Beispiel sind die Informationen nur hilfreich, wenn für den Benutzer bereits Hochgeschwindigkeits-USB-Anschlüsse installiert sind. Andernfalls führt der Benutzer wahrscheinlich nichts anderes als das Ergebnis aus.<br/> <strong>Anzeigen in:</strong> Wenn das auslösende Ereignis auftritt.<br/> <strong>Zeigen</strong> Sie Folgendes an: Verwenden Sie die Echt Zeit Option, sodass diese Benachrichtigungen nicht in die Warteschlange eingereiht werden, wenn Benutzer eine Vollbildanwendung ausführen oder nicht aktiv Ihren Computer verwenden.<br/> Häufigkeit <strong>anzeigen:</strong> Einmal.<br/> <strong>Ärgernisfaktor:</strong> Mittel bis hoch, abhängig von der Wahrnehmung von Nützlichkeit und Relevanz der Benutzer. Dies wird nicht empfohlen, wenn eine geringe Wahrscheinlichkeit eines Benutzer Interesses vorliegt.<br/> <strong>Alternativen:</strong> Benutzer nicht benachrichtigen. <br/></td>
</tr>
<tr class="even">
<td><strong>Funktions Ankündigung</strong><br/> Benachrichtigt Benutzer über neu installierte, nicht verwendete System-oder Anwendungs Features.<br/></td>
<td><strong>Verwenden Sie keine Benachrichtigungen für featureankündigungen!</strong> Verwenden Sie stattdessen eine andere Möglichkeit, um das Feature erkennbar zu machen, z. b.: <br/>
<ul>
<li>Entwerfen Sie die Funktion so, dass Sie in Kontexten, in denen Sie benötigt wird, einfacher zu erkennen ist.</li>
<li>Machen Sie nichts besonderes, und lassen Sie die Benutzer die Funktion selbst ermitteln.</li>
</ul>
<strong>Falsch:</strong><br/> <img src="images/mess-notif-image4.png" alt="Screen shot of notification of new features " /><br/> Verwenden Sie keine Benachrichtigungen für featureankündigungen.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Wählen Sie basierend auf der Verwendung das Benachrichtigungs Muster aus.** Eine Beschreibung der einzelnen Verwendungs Muster finden Sie in der vorherigen Tabelle.
-   **Verwenden Sie während der anfänglichen Windows-Darstellung keine Benachrichtigungen.** Um die erste Umgebung zu verbessern, unterdrückt Windows 7 alle Benachrichtigungen, die während der ersten Stunden der Nutzung angezeigt werden. Entwerfen Sie Ihr Programm, vorausgesetzt, Benutzer werden keine Benachrichtigungen erhalten.

### <a name="what-to-notify"></a>Was soll benachrichtigt werden?

-   **Benachrichtigen Sie nicht über erfolgreiche Vorgänge, außer in den folgenden Situationen:**
    -   **Sicherheit.** Benutzer sollten Sicherheitsvorgänge als höchste Wichtigkeit in Erwägung gezogen haben, sodass die Benutzer über erfolgreiche Sicherheitsvorgänge benachrichtigt werden.
    -   **Aktueller Fehler.** Benutzer nehmen keine erfolgreichen Vorgänge für die Gewährung vor, wenn Sie unmittelbar zuvor einen Fehler bestanden haben
    -   **Vermeiden Sie Unannehmlichkeiten.** Melden Sie erfolgreiche Vorgänge, wenn Sie dies tun, vermeiden Sie inbequemere Benutzer. Folglich Benachrichtigen Sie Benutzer, wenn ein erfolgreicher Vorgang auf unerwartete Weise durchgeführt wird, z. b. Wenn ein Vorgang lange oder später als erwartet abgeschlossen ist.
-   **In anderen Fällen können Sie entweder kein Feedback für Erfolg geben oder "Bedarfs gesteuert" Feedback geben.** Nehmen Sie an, dass Benutzer erfolgreiche Vorgänge für die Gewährung durchführen. Sie können Feedback zu Bedarf senden, indem Sie im Benachrichtigungsbereich ein Symbol anzeigen (oder ein vorhandenes Symbol ändern), während der Vorgang ausgeführt wird, und das Symbol entfernen (oder das vorherige Symbol wiederherstellen), wenn der Vorgang beendet ist.
-   Für das FYI-Muster **sollten Sie keine Benachrichtigung erhalten, wenn Benutzer weiterhin normal arbeiten oder wahrscheinlich nichts anderes als das Ergebnis der Benachrichtigung ausführen.**

    **Falsch:**

    ![Screenshot der Benachrichtigung zur schnelleren Leistung ](images/mess-notif-image17.png)

    In diesem Beispiel sind die Informationen nur hilfreich, wenn der Benutzer bereits über die installierten Ports verfügt. Andernfalls führt der Benutzer wahrscheinlich nichts anderes als das Ergebnis aus.

    -   Ausnahme: **Sie können Benutzer mit Informationen über die fragwürdige Relevanz Benachrichtigen, wenn dies optional ist und Benutzer sich anmelden.**

        **Richtig:**

        ![Screenshot der Benachrichtigung über den angemeldeten Kontakt ](images/mess-notif-image16.png)

        In diesem Beispiel werden Benutzer benachrichtigt, wenn Kontakte online geschaltet werden, und Sie haben sich entschieden, diese optionalen Informationen zu erhalten.

-   Verwenden Sie für das nicht kritische System Ereignis und FYI-Muster die **Complete-Benachrichtigungen für ein einzelnes Ereignis.** Es sind nicht mehrere partielle vorhanden.

    **Falsch:**

    ![Screenshot der Benachrichtigungen "neue Hardware gefunden" ](images/mess-notif-image18.png)

    In diesen Beispielen werden nur vier der acht Benachrichtigungen angezeigt, die von Windows XP angezeigt wurden, wenn ein Benutzer eine bestimmte USB-Tastatur anfügt, die jeweils inkrementelle Weitere Informationen anzeigt.

    **Richtig:**

    ![Screenshot der Benachrichtigungen über den Installationsstatus ](images/mess-notif-image19.png)

    In diesem Beispiel führt das Anfügen einer USB-Tastatur zu zwei kompletten Benachrichtigungen.

### <a name="when-to-notify"></a>Benachrichtigungs Zeitpunkt

-   **Anzeigen einer Benachrichtigung auf der Grundlage des Entwurfs Musters:**



|                                      |                                                                                                                                                                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Muster**<br/>               | **Benachrichtigungs Zeitpunkt**<br/>                                                                                                                                                                                      |
| Aktion erfolgreich<br/>            | Bei Abschluss einer asynchronen Aufgabe. Benachrichtigen von Benutzern über erfolgreiche Aktionen nur, wenn Sie wahrscheinlich auf den Abschluss warten oder nach dem letzten Fehler.<br/>                                             |
| Aktions Fehler<br/>            | Bei einem Fehler bei einer asynchronen Aufgabe.<br/>                                                                                                                                                                   |
| Nicht kritisches System Ereignis<br/> | Wenn ein Ereignis auftritt und der Benutzer aktiv ist oder die Bedingung weiterhin vorhanden ist. Wenn dies zu einem Problem führt, entfernen Sie die derzeit angezeigte Benachrichtigung sofort, sobald das Problem behoben ist.<br/> |
| Optionale Benutzer Aufgabe<br/>        | Die Notwendigkeit, eine Aufgabe auszuführen, wird bestimmt, und der Benutzer ist aktiv.<br/>                                                                                                                                   |
| Zur Kenntnisnahme<br/>                       | Wenn das auslösende Ereignis auftritt.<br/>                                                                                                                                                                       |



 

-   Wenn das Problem für das Aktions Fehlermuster **innerhalb von Sekunden behoben werden kann, verzögern Sie die Fehler Benachrichtigung für einen angemessenen Zeitraum.** Wenn sich das Problem selbst korrigiert, melden Sie nichts. Benachrichtigen Sie erst, nachdem genug Zeit vergangen ist, dass der Fehler erkennbar ist. Wenn Sie zu früh melden, bemerken die Benutzer wahrscheinlich nicht, dass das Problem gemeldet wird, aber Sie bemerken die unnötige Benachrichtigung.

**Falsch:**

![Screenshot der Netzwerk Verbindungs Benachrichtigung ](images/mess-notif-image20.png)

Wenn unmittelbar gefolgt von:

![Screenshot der erfolgreichen Verbindungs Benachrichtigung ](images/mess-notif-image21.png)

In diesem Beispiel ist in Windows Vista die Benachrichtigung, dass keine drahtlose Konnektivität vorliegt, da häufig eine Benachrichtigung über eine gute Konnektivität folgt.

-   Verwenden Sie für die Aktion Erfolg und FYI **-Muster die Option Echt Zeit, damit veraltete Benachrichtigungen nicht in die Warteschlange eingereiht** werden, wenn Benutzer eine Vollbildanwendung ausführen oder den Computer nicht aktiv verwenden.
-   Erstellen Sie für das nicht kritische System Ereignis Muster **nicht das Potenzial für Benachrichtigungs Stürme durch Ereignisse, die an bekannte Ereignisse wie z. b. die Benutzeranmeldung gebunden sind.** Binden Sie das Ereignis stattdessen an einen Zeitraum nach dem Ereignis. Beispielsweise können Sie Benutzer daran erinnern, Ihr Produkt fünf Minuten nach der Benutzeranmeldung zu registrieren.

### <a name="how-long-to-notify"></a>Dauer der Benachrichtigung

In Windows Vista und höher werden Benachrichtigungen für eine Dauer von 9 Sekunden angezeigt.

### <a name="how-often-to-notify"></a>Häufigkeit der Benachrichtigung

-   **Die Häufigkeit, mit der eine Benachrichtigung angezeigt wird, basiert auf dem Entwurfsmuster:**



|                                      |                                                                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **Muster**<br/>               | **Häufigkeit der Benachrichtigung**<br/>                                                                                          |
| Aktion erfolgreich<br/>            | Einmal.<br/>                                                                                                            |
| Aktions Fehler<br/>            | Einmal.<br/>                                                                                                            |
| Nicht kritisches System Ereignis<br/> | Wenn das Ereignis das erste Mal auftritt. Wenn dies ein Problem ergibt, das von Benutzern gelöst werden muss, müssen Sie einmal am Tag eine erneute Anzeige durchführen.<br/> |
| Optionale Benutzer Aufgabe<br/>        | Einmal pro Tag für maximal drei Mal.<br/>                                                                         |
| Zur Kenntnisnahme<br/>                       | Einmal.<br/>                                                                                                            |



 

-   **Bei optionalen Benutzer Aufgaben sollten Sie nicht versuchen, Benutzer zu übermitteln, indem Sie ständig Benachrichtigungen anzeigen.** Wenn die Aufgabe erforderlich ist, zeigen Sie sofort ein modales Dialogfeld an, anstatt Benachrichtigungen zu verwenden.

### <a name="notification-escalation"></a>Benachrichtigungs Ausweitung

-   **Gehen Sie nicht davon aus, dass Benutzern Ihre Benachrichtigungen angezeigt werden.** Benutzern werden Sie nicht angezeigt, wenn:
    -   Sie werden in Ihre Arbeit eingebettet.
    -   Sie werden nicht beachtet.
    -   Sie sind nicht mehr von Ihrem Computer entfernt.
    -   Sie führen eine Vollbildanwendung aus.
    -   Ihr Administrator hat alle Benachrichtigungen für Ihren Computer deaktiviert.
-   **Wenn Benutzer letztendlich eine Aktion ausführen müssen, verwenden Sie die Progressive Eskalation** , um eine alternative Benutzeroberfläche anzuzeigen, die Benutzer nicht ignorieren können.

### <a name="interaction"></a>Interaktion

-   **Aktivieren Sie die Benachrichtigungen, wenn Sie Folgendes ausführen:**
    -   **Benutzer sollten eine Aktion ausführen.** Wenn Sie auf die Benachrichtigung klicken, wird ein Fenster angezeigt, in dem Benutzer die Aktion ausführen können. Diese Vorgehensweise wird für den Aktions Fehler und optionale Entwurfsmuster für Benutzer Aufgaben bevorzugt.
    -   **Benutzer möchten möglicherweise weitere Informationen anzeigen.** Wenn Sie auf die Benachrichtigung klicken, wird ein Fenster angezeigt, in dem Benutzer zusätzliche Informationen anzeigen können.
-   **Zeigt immer ein Fenster an, wenn Benutzer auf klicken, um eine Aktion auszuführen.** Klicken Sie nicht darauf, eine Aktion direkt auszuführen.
-   **Wenn Sie auf klicken, um weitere Informationen anzuzeigen, sollten immer weitere Informationen angezeigt werden** Geben Sie nicht nur die Informationen ein, die bereits in der Benachrichtigung vorhanden sind.

### <a name="icons"></a>Symbole

-   **Verwenden Sie für das Aktions Fehlermuster das Standardfehler Symbol.**
-   **Verwenden Sie für die nicht kritischen System Ereignis Muster das Standard Warnsymbol.**
-   **Verwenden Sie bei anderen Mustern Symbole, die Objekte darstellen, die den Betreff betreffen oder vorschlagen**, wie z. b. ein Schild für die Sicherheit oder einen Akku für Strom.
-   **Verwenden Sie Symbole auf der Grundlage Ihrer Anwendung oder Ihres Unternehmens Brandings, wenn Sie von ihren Ziel Benutzern erkannt werden und es keine bessere Alternative gibt.**
-   Bei progressiver Eskalation **sollten Sie Symbole mit einer progressiveren Darstellung verwenden, da die Situation dringender wird.**
-   **Verwenden Sie das Symbol "Standardinformationen" nicht.** Diese Benachrichtigungen sind Informationen, ohne zu sagen.
-   **Verwenden Sie große Symbole (32 x 32 Pixel), wenn Folgendes gilt:**
    -   Benutzer werden das Symbol und nicht den Text schnell verstehen.
    -   Die großen Symbole vermitteln ihre Bedeutung deutlicher und effektiver als die standardmäßigen 16x16-Pixel Symbole.
    -   Das Symbol verwendet den [Aero-Stil](vis-icons.md).

![Screenshot der Benachrichtigung "wichtige Nachrichten" ](images/mess-notif-image22.png)

In diesem Beispiel können Benutzer die Art der Benachrichtigung mit einem Blick auf das Symbol "groß" schnell verstehen.

### <a name="notification-queuing"></a>Benachrichtigungs Warteschlange

**Hinweis:** Benachrichtigungen werden in die Warteschlange eingereiht, wenn Sie nicht sofort angezeigt werden können, z. b. Wenn eine andere Benachrichtigung angezeigt wird, der Benutzer eine Vollbildanwendung oder der Benutzer den Computer nicht aktiv verwendet. Echt Zeit Benachrichtigungen verbleiben nur für 60 Sekunden in der Warteschlange.

-   **Verwenden Sie für die Aktion Erfolg und FYI-Muster die Option Echt Zeit,** damit die Benachrichtigung nicht lange in die Warteschlange eingereiht wird. Diese Benachrichtigungen verfügen nur über einen Wert, wenn Sie sofort angezeigt werden können.
-   **Entfernen Sie Benachrichtigungen in Warteschlangen, wenn Sie nicht mehr relevant sind.**
-   **Entwickler:** Legen Sie hierzu das NIF \_ -infoflag in uFlags fest, und legen Sie szinfo auf eine leere Zeichenfolge fest. Dies hat keinen Schaden, wenn sich die Benachrichtigung nicht mehr in der Warteschlange befindet.

### <a name="system-integration"></a>Systemintegration

-   Wenn die Anwendung nicht immer über ein Symbol im [Benachrichtigungsbereich](winenv-notification.md) verfügt, wenn Sie ausgeführt wird, können Sie **ein Symbol temporär während der asynchronen Aufgabe oder des Ereignisses anzeigen, das die Benachrichtigung verursacht hat.**

## <a name="text"></a>Text

### <a name="title-text"></a>Titeltext

-   **Verwenden Sie Titeltext, der die wichtigsten Informationen, die Sie für die Kommunikation mit Benutzern benötigen, in klarer, Klartext und präziser Sprache zusammenfasst.** Benutzer sollten in der Lage sein, den Zweck der Benachrichtigungs Informationen schnell und mit minimalem Aufwand zu verstehen.
-   **Verwenden Sie Textfragmente oder vollständige Sätze ohne das Beenden der Interpunktions Zeichen**
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
-   **Verwenden Sie nicht mehr als 48 Zeichen (in englischer Sprache), um die Lokalisierung zu ermöglichen.** Der Titel hat eine maximale Länge von 63 Zeichen, aber Sie müssen eine Erweiterung von 30% zulassen, wenn der Text in englischer Sprache übersetzt wird.

### <a name="body-text"></a>Textkörper

-   **Verwenden Sie Textkörper Text, der eine Beschreibung (ohne Wiederholung der Informationen im Titel) enthält, und optional, der bestimmte Details zur Benachrichtigung enthält. Außerdem können Benutzer wissen, welche Aktion verfügbar ist.**
-   **Verwenden Sie vollständige Sätze mit endinterpunktions Zeichen.**
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
-   **Verwenden Sie nicht mehr als 200 Zeichen (in englischer Sprache), um die Lokalisierung zu ermöglichen.** Der Textkörper Text hat eine maximale Länge von 255 Zeichen, aber Sie müssen eine Erweiterung von 30% zulassen, wenn der Text in englischer Sprache übersetzt wird.
-   **Fügen Sie wichtige Informationen in den Textkörper Text ein, z. b. bestimmte Objektnamen.** (Beispiele: Benutzernamen, Dateinamen oder URLs.) Benutzer müssen kein anderes Fenster öffnen, um diese Informationen zu finden.
-   **Fügen Sie die Objektnamen in doppelte Anführungszeichen ein.**
    -   **Ausnahme:** Verwenden Sie in folgenden Anführungszeichen nicht:
        -   Der Objektname verwendet immer die Groß-/Kleinschreibung im [Titel](glossary.md), z. b. mit Benutzernamen.
        -   Der Objektname ist mit einem Doppelpunkt (z. b. Druckername: Mein Drucker) versetzt.
        -   Der Objektname kann leicht aus dem Kontext bestimmt werden.
-   **Wenn Sie Objektnamen auf eine maximale maximale Größe kürzen müssen, um die Lokalisierung zu ermöglichen, verwenden Sie ein Auslassungs Zeichen, um das Abschneiden anzugeben.**

    ![Screenshot der Nachricht mit einem verkürzten Namen ](images/mess-notif-image23.png)

    In diesem Beispiel wird ein Objektname mithilfe eines Ellipsen abgeschnitten.

-   **Verwenden Sie die folgende Ausdrucks Phrase, wenn die Benachrichtigung handlungsfähig ist:**
    -   Wenn Benutzer auf die Benachrichtigung klicken können, um eine Aktion auszuführen:

        < kurze Beschreibung wichtiger Informationen>

        <optional details>

        Klicken Sie auf <do something> .

        ![Screenshot der Meldung: "klicken Sie, um den Fortschritt anzuzeigen" ](images/mess-notif-image24.png)

        In diesem Beispiel können Benutzer auf klicken, um eine Aktion auszuführen.

    -   Wenn Benutzer auf die Benachrichtigung klicken können, um weitere Informationen anzuzeigen:

        < kurze Beschreibung wichtiger Informationen>

        <optional details>

        Klicken Sie auf Weitere Informationen.

        ![Screenshot der Meldung: Klicken Sie, um weitere Informationen anzuzeigen. ](images/mess-notif-image25.png)

        In diesem Beispiel können Benutzer auf klicken, um weitere Informationen zu erhalten.

-   **Nehmen Sie nicht an, dass der Benutzer eine Aktion in einer Benachrichtigung ausführen muss.** Benachrichtigungen sind für nicht kritische Informationen vorgesehen, die von Benutzern frei ignoriert werden können. Wenn Benutzer wirklich eine Aktion ausführen müssen, verwenden Sie keine Benachrichtigungen.
-   **Wenn Benutzer eine Aktion ausführen sollten, legen Sie die Wichtigkeit fest.**
-   Bei Aktions Fehlern und nicht kritischen System Ereignis Mustern **beschreiben Sie Probleme in der Sprache "einfach".**

    **Falsch:**

    ![Screenshot von längerer, komplexer Nachricht ](images/mess-notif-image26.png)

    In diesem Beispiel wird das Problem durch eine übermäßig technische, aber nicht spezifische Sprache beschrieben.

    **Richtig:**

    ![Screenshot der klaren, präzisen Nachricht ](images/mess-notif-image27.png)

    In diesem Beispiel wird das Problem in Klartext beschrieben.

-   **Beschreiben Sie das Ereignis auf eine Weise, die für die Ziel Benutzer relevant ist.** Eine Benachrichtigung ist relevant, wenn die Benutzer eine Aufgabe ausführen oder Ihr Verhalten im Ergebnis der Benachrichtigung ändern können. Dies kann häufig durch die Beschreibung von Benachrichtigungen im Hinblick auf Benutzer Ziele anstelle von technologischen Problemen erreicht werden.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Benachrichtigungen:

-   Verwenden Sie den genauen Titeltext, einschließlich der Groß-/Kleinschreibung.
-   Verweisen Sie auf die Komponente als Benachrichtigung, nicht als Sprechblase oder Warnung.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie klicken.
-   Formatieren Sie den Titeltext nach Möglichkeit mithilfe von fettem Text. Andernfalls sollten Sie den Titel nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Wenn die **Bereitstellung der kritischen Updates bereit für die Installation** von angezeigt wird, klicken Sie auf die Benachrichtigung, um den Prozess zu starten.

Wenn Sie auf den Benachrichtigungsbereich verweisen:

-   Informationen zum Benachrichtigungsbereich finden Sie im Benachrichtigungsbereich und nicht in der Taskleiste.

 

