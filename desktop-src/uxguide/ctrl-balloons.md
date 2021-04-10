---
title: Ballons
description: Eine Sprechblase ist ein kleines Popup Fenster, in dem Benutzer über ein nicht kritisches Problem oder eine besondere Bedingung in einem Steuerelement informiert werden.
ms.assetid: 67092831-e573-4ad6-b1fc-baa1836031cb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 348167594db2f7895e185d8d7761832ec5c0c1cb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351059"
---
# <a name="balloons"></a>Ballons

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Eine Sprechblase ist ein kleines Popup Fenster, in dem Benutzer über ein nicht kritisches Problem oder eine besondere Bedingung in einem Steuerelement informiert werden.

![Screenshot, der eine Sprechblase anzeigt, die anzeigt, dass die Feststell Taste eingeschaltet ist](images/ctrl-balloons-image1.png)

Eine typische Sprechblase.

Luftballons verfügen über ein Symbol, einen Titel und einen TextText, die alle optional sind. Im Gegensatz zu Quick Infos und infotips verfügen die Ballons auch über ein Ende, das Ihre Quelle identifiziert. Normalerweise ist die Quelle ein Steuerelement, wenn dies der Fall ist, wird Sie als [Besitzer Steuer](glossary.md)Element bezeichnet.

Wenn die Benutzer über nicht kritische Probleme informiert werden, verhindern Sie Probleme, obwohl das Besitzer Steuerelement dies möglicherweise nicht tut. Alle nicht behandelten Probleme müssen von der Benutzeroberfläche des Besitzers behandelt werden, wenn Benutzer versuchen, ein Commit für die Aktion durchführen.

Ballons werden normalerweise mit Textfeldern oder Steuerelementen verwendet, die Textfelder zum Ändern von Werten verwenden, z. b. Kombinations Felder, Listenansichten und Struktur Ansichten. Andere Arten von Steuerelementen sind ausreichend eingeschränkt und benötigen nicht die zusätzlichen Feedback-ballblasen. Wenn außerdem ein Problem mit anderen Steuerelement Typen vorliegt, umfasst es häufig Inkonsistenzen zwischen mehreren Steuerelementen, eine Situation, in der die Ballons nicht geeignet sind. Nur Texteingabe-Steuerelemente sind nicht eingeschränkt und eine häufige Quelle von [Einzelpunkt Fehlern](glossary.md).

Eine Benachrichtigung ist eine bestimmte Art von Sprechblase, die von einem [Benachrichtigungs Bereichs](winenv-notification.md) Symbol angezeigt wird.

**Hinweis:** Richtlinien für [Benachrichtigungen](mess-notif.md), Quick [Infos und Infotipps](ctrl-tooltips-and-infotips.md)sowie [Fehlermeldungen](mess-error.md) werden in separaten Artikeln dargestellt.

**Ist dies das richtige Steuerelement?**

Orientieren Sie sich an folgenden Fragen:

-   **Beschreiben die Informationen ein Problem oder eine besondere Bedingung?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Verwenden Sie keine Luftballons, um ergänzende Informationen für ein Steuerelement anzuzeigen. Verwenden Sie stattdessen [statischen Text](glossary.md),[Info Tipps](glossary.md), [Progressive Offenlegung](glossary.md)oder Eingabe Aufforderungen.
-   **Kann das Problem oder die besondere Bedingung sofort erkannt werden** , oder wenn das Besitzer Steuerelement den Eingabefokus verliert? Falls nicht, verwenden Sie eine Fehlermeldung, die in einem [Aufgaben Dialogfeld](glossary.md) oder in einem Meldungs [Feld](glossary.md)angezeigt
-   **Ist das Problem für Probleme wichtig?** Wenn dies der Fall ist, verwenden Sie eine Fehlermeldung, die in einem Aufgaben Dialogfeld oder Meldungs Feld Diese Fehlermeldungen erfordern eine Interaktion (die für kritische Fehler geeignet ist), während Luftballons dies nicht tun.
-   **Gilt für besondere Bedingungen, dass die Bedingung gültig ist, aber wahrscheinlich unbeabsichtigt ist?** Wenn dies der Fall ist, sind die Ballons geeignet. Für Bedingungen, die nicht gültig sind, ist es besser, Sie an erster Stelle zu verhindern. Für wahrscheinlich vorgesehene Bedingungen gibt es keine Notwendigkeit, etwas zu tun.
-   **Kann das Problem oder die besondere Bedingung kurz ausgedrückt werden?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Luftballons können keine ausführlichen Erläuterungen haben oder zusätzliche Informationen bereitstellen.
-   **Beschreiben die Informationen das Steuerelement, auf das gerade mit dem Mauszeiger gezeigt wird?** Wenn dies der Fall ist, verwenden Sie stattdessen einen Tipp, sofern die Benutzer möglicherweise nicht mit der Nachricht interagieren müssen.
-   **Beziehen sich die Informationen auf die aktuelle Aktivität des Benutzers?** Falls nicht, sollten Sie stattdessen eine [Benachrichtigung](mess-notif.md) oder ein [Dialogfeld](win-dialog-box.md) verwenden. Benutzer übersehen wahrscheinlich die Ballons außerhalb der aktuellen Aktivität, und standardmäßig wird nach 10 Sekunden ein Timeout für die Ballons angezeigt.
-   **Stammen die Informationen aus einer einzelnen, bestimmten Quelle?** Wenn ein Problem oder eine Bedingung mehrere Quellen oder keine bestimmte Quelle hat, verwenden Sie stattdessen eine direkte [Nachricht](glossary.md) oder ein Dialogfeld.

**Falsch:** ![ Screenshot einer Sprechblase: Anmeldung nicht erfolgreich](images/ctrl-balloons-image2.png)

In diesem Beispiel kann das Problem mit dem Benutzernamen oder dem Kennwort auftreten, aber das Melden des Problems mit einer Sprechblase deutet darauf hin, dass nur das Kennwort das Problem ist. Folglich ist das Feedback der Eingabe eines falschen Benutzernamens irreführend.

Luftballons sind eine Alternative zu Info Tipps, Dialogfeldern und direkten Nachrichten. Im Gegensatz zu Quick Infos und infotips:

-   Ballons können unabhängig von der aktuellen Zeigerposition angezeigt werden, sodass Sie über ein Ende verfügen, das Ihre Quelle angibt.
-   Ballons haben einen Titel, Textkörper und ein Symbol.
-   Luftballons können interaktiv sein, während auf einen Tipp nicht klicke.

Im Gegensatz zu modalen Dialogfeldern:

-   Luftballons stehlen keinen Eingabefokus oder erfordern Interaktionen.
-   Mit Luftballons wird eine einzelne, bestimmte Quelle identifiziert. Modale Dialogfelder können mehrere Quellen oder keine bestimmte Quelle enthalten.

Im Gegensatz zu direkten Nachrichten:

-   Die Ballons sind auffälliger.
-   Für Luftballons ist kein verfügbarer Bildschirmbereich oder das dynamische Layout erforderlich, das zum Anzeigen von direkten Nachrichten erforderlich ist.
-   Ballons entfernen sich automatisch nach einem Timeout.

**Verwendungsmuster**

Luftballons haben folgende Verwendungs Muster:



|                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eingabeproblem** Ein nicht kritisches Benutzereingabe Problem, das von einem einzelnen Besitzer Steuerelement stammt, in der Regel ein Textfeld. <br/>                                               | die Verwendung von Luftballons für Fehlermeldungen stiehlt den Eingabefokus nicht, ist jedoch immer noch sehr bemerkbar, wenn das Besitzer Steuerelement den Eingabefokus besitzt. um das Problem zu beheben, muss der Benutzer die Eingabe möglicherweise ändern oder erneut eingeben. Wenn das Besitzer Steuerelement jedoch falsche Eingaben ignoriert, muss der Benutzer möglicherweise überhaupt keine Änderungen vornehmen. Da das Problem nicht entscheidend ist, ist kein [Fehler Symbol](vis-std-icons.md) erforderlich. <br/> ![Screenshot, der eine Sprechblase mit einem falschen Zeichen anzeigt.](images/ctrl-balloons-image3.png)<br/> Eine Sprechblase, die verwendet wird, um ein nicht kritisches Benutzereingabe Problem zu melden.<br/>                                                                                                  |
| **Besondere Bedingung** Das Besitzer Steuerelement befindet sich in einem Zustand, der sich auf Eingaben auswirkt. Dieser Status ist wahrscheinlich unbeabsichtigt, und der Benutzer hat möglicherweise keine Eingaben erkannt. <br/> | Verwenden Sie Ballons, um Frustrationen zu vermeiden, indem Sie Benutzer über besondere Bedingungen informieren, sobald sie auftreten (z. b. das Überschreiten der maximalen Eingabe Größe oder das Festlegen von Feststell Sperren versehentlich). Es ist wichtig, dieses Feedback zu geben, ohne den Eingabefokus zu stehlen oder die Interaktion zu erzwingen, da diese Bedingungen möglicherweise beabsichtigt sind. Diese Luftballons sind besonders wichtig für Kenn Wörter und PIN-Felder, in denen Benutzer andernfalls mit minimalem Feedback arbeiten. Diese Luftballons weisen ein [Warnsymbol](vis-std-icons.md)auf. <br/> ![Screenshot, in dem die Luftballons angezeigt werden, die die Feststell Sperre anzeigen und ein falsches Zeichen eingegeben wird.](images/ctrl-balloons-image4.png)<br/> Eine Sprechblase, mit der eine besondere Bedingung gemeldet wird.<br/> |



 

**Richtlinien**

**Anzeige Anzeige**

-   **Zeigen Sie die Sprechblase an, sobald das Problem oder die besondere Bedingung erkannt wird, auch wenn Sie wiederholt ohne merkliche Verzögerung erkannt werden.**
    -   Bei Problemen mit einzelnen Zeichen oder der maximalen Eingabe Größe sollten Sie die Sprechblase sofort bei der Eingabe anzeigen.
    -   Bei Problemen, die den Eingabe Wert betreffen (einschließlich der Anforderung eines nicht leeren Werts), wird die Sprechblase angezeigt, wenn das Besitzer Steuerelement den Eingabefokus verliert. Andernfalls kann die Anzeige von Luftballons, während Benutzer potenziell gültige Eingaben eingeben, ablenkend und ärgerlich sein.
-   **Zeigen Sie jeweils nur eine Sprechblase an.** Das Anzeigen mehrerer Luftballons kann überwältigend sein. Wenn ein einzelnes Ereignis zu mehreren Problemen führt, stellen Sie entweder alle Probleme auf einmal vor, oder melden Sie nur das wichtigste Problem.

**Falsch:** ![ Screenshot von zwei Luftballons, die auf ein Feld zeigen](images/ctrl-balloons-image5.png)

In diesem Beispiel werden zwei Probleme fälschlicherweise gleichzeitig angezeigt.

**Anzeigedauer**

-   **Entfernen Sie eine Sprechblase, wenn:**
    -   Das Problem ist behoben, oder eine besondere Bedingung wird entfernt.
    -   Der Benutzer gibt gültige Daten ein (bei Eingabe Problemen).
    -   Timeout bei der Sprechblase. Standardmäßig entfernen sich Luftballons nach 10 Sekunden, obwohl Benutzer dies ändern können, indem Sie den SPI- \_ messageduration-Systemparameter ändern.
-   **Entfernen Sie das Timeout, wenn Benutzer nicht fortfahren können, bis das Problem behoben wurde. Entwickler:** in Win32 können Sie die Anzeigezeit mit der TTM- \_ setdelta-Zeit Nachricht festlegen.

**Vorgehensweise beim Anzeigen**

-   **Zeigt die untergeordneten Steuerelemente des Besitzers an.** Auf diese Weise können Benutzer den Kontext anzeigen, einschließlich des Besitzer Steuer Elements und seiner Bezeichnung. Die Sprechblasen Positionen werden von Microsoft Windows automatisch an den Bildschirm angepasst. Das Standardverhalten besteht darin, eine Sprechblase oberhalb ihres Besitzer Steuer Elements anzuzeigen, wie dies bei Benachrichtigungen der Fall ist.

**Richtig:** ![ Screenshot eines sprechenden unter seinem Steuerelement](images/ctrl-balloons-image6.png)

**Falsch:** ![ Screenshot einer Sprechblase oberhalb ihres Steuer Elements](images/ctrl-balloons-image7.png)

Im falschen Beispiel wird die Sprechblase unkorrekt oberhalb des Besitzer Steuer Elements angezeigt.

**Textfelder für Kennwort und PIN**

-   Verwenden Sie eine Sprechblase, um anzugeben, dass die Feststell **Sperre auf ON fest steht**. verwenden Sie dazu den Text im folgenden Beispiel

![Screenshot eines sprechenden, der angibt, dass die Feststell Taste ein ist](images/ctrl-balloons-image8.png)

In diesem Beispiel gibt eine Sprechblase an, dass die Feststell Sperre in einem Pin-Textfeld eingeschaltet ist.

-   **Verwenden Sie eine Sprechblase, um anzugeben, wann Benutzer versuchen, die maximale Eingabe Größe zu überschreiten.** Das Erreichen der maximalen Eingabe Größe ist im Kennwort und in den PIN-Textfeldern deutlich weniger offensichtlich als normale Textfelder.

![Screenshot einer Sprechblase, die PIN-Code Limits anzeigt](images/ctrl-balloons-image9.png)

In diesem Beispiel gibt eine Sprechblase an, dass der Benutzer versucht, die maximale Eingabe Größe zu überschreiten.

-   **Verwenden Sie eine Sprechblase, um anzugeben, wenn Benutzer falsche Zeichen eingeben.** Es ist jedoch besser, solche Einschränkungen zu vermeiden, da Sie die Sicherheit des Kennworts oder der PIN verringern. Um die Offenlegung von Informationen zu verhindern, sollte die Sprechblase nur dokumentierte Fakten über gültige Kenn Wörter oder Pins erwähnen.

![Screenshot einer Sprechblase, die falsche Eingaben anzeigt](images/ctrl-balloons-image10.png)

In diesem Beispiel gibt eine Sprechblase an, dass für die Pin Zahlen erforderlich sind.

**Andere Textfelder**

-   **Verwenden Sie ggf. eine Sprechblase, um anzugeben, wenn Benutzer versuchen, die maximale Eingabe Größe für kritische, kurze Textfelder zu überschreiten, die auf Einsteiger abzielen** Beispiele hierfür sind Benutzernamen und Kontonamen. Text Felder werden angezeigt, wenn Benutzer versuchen, die maximal zulässige Eingabe zu überschreiten, aber die Bedeutung des Signal-Benutzers ist möglicherweise nicht von den Einsteiger zu verstehen.

![Screenshot eines sprechenden, der Zeichen Limits anzeigt](images/ctrl-balloons-image11.png)

In diesem Beispiel gibt eine Sprechblase an, dass der Benutzer versucht hat, die maximale Eingabe Größe zu überschreiten.

**Interaktion**

-   **Wenn Benutzer auf eine Sprechblase klicken, schließen Sie einfach die Sprechblase, ohne eine andere Benutzeroberfläche anzuzeigen oder einen anderen Nebeneffekt zu haben.** Im Gegensatz zu Benachrichtigungen sollten die Ballons keine Schaltflächen schließen haben.

**Symbole**

-   Wählen Sie das Symbol basierend auf dem Verwendungs Muster aus:



    |  Muster |  Symbol                                                                                                                                                       |
    ------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Eingabeproblem | Kein Symbol. Die Verwendung eines [Fehler Symbols](vis-std-icons.md) ist hier mit den [Windows-Ton](text-style-tone.md) Richtlinien konsistent. |
    | Besondere Bedingung | Das standardmäßige 16x16-Pixel- [Warnsymbol](vis-std-icons.md).                                                                                  |

**Bedienungshilfen**

Wenn Sie richtig verwendet werden, verbessern die Barrierefreiheit. Für den Zugriff auf die Ballons:

-   Hiermit werden nur die Ballons angezeigt, die sich auf die aktuelle Aktivität des Benutzers beziehen.
-   Halten Sie den Text für die Sprechblase kurz. Dadurch wird der Sprechblasen Text für Benutzer mit Sehbehinderung leichter lesbar, und die Unterbrechung wird minimiert, wenn er von Sprachausgaben gelesen wird.
-   Die Sprechblase immer dann erneut anzeigen, wenn das Problem oder die Bedingung wiederholt wird.

**Text**

**Titeltext**

-   **Verwenden Sie den Titeltext, der das Eingabeproblem oder die besondere Bedingung kurz in Klartext zusammenfasst.** Benutzer sollten in der Lage sein, den Zweck der Sprechblase schnell und mit minimalem Aufwand zu verstehen.
-   **Verwenden Sie Textfragmente oder vollständige Sätze ohne das Beenden der Interpunktions Zeichen**
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.** Weitere Informationen finden Sie im [Glossar](./glossary.md).
-   **Verwenden Sie nicht mehr als 48 Zeichen (in englischer Sprache), um die Lokalisierung zu ermöglichen.** Der Titel hat eine maximale Länge von 63 Zeichen und muss in der Lage sein, um mindestens 30 Prozent zu erweitern, um die Lokalisierung zu ermöglichen.

**Textkörper**

-   **Verwenden Sie den ersten Satz des Text Texts, um das Problem oder die Bedingung auf eine Weise festzustellen, die für den Benutzer eindeutig relevant ist.** Wiederholen Sie die Informationen im Titel nicht. Lassen Sie diese Angabe aus, wenn nichts mehr hinzugefügt werden muss.
-   **Mit dem zweiten Satz können Sie angeben, welche Aktionen der Benutzer durchführen kann, um das Problem zu beheben oder den Zustand zurückzusetzen.** In Übereinstimmung mit den Richtlinien für [Stil und Ton](./text-style-tone.md) muss das Wort in dieser Anweisung nicht verwendet werden. Legen Sie zwei Zeilenumbrüche zwischen dem ersten und dem zweiten Satz ab.

![Screenshot einer Sprechblase mit Titel und TextText](images/ctrl-balloons-image12.png)

Dieses Beispiel zeigt das standardmäßige Text Layout der Sprechblase.

-   **Erläutern Sie, wie Sie das Problem beheben oder den Zustand wiederherstellen können, auch wenn diese Erklärung offensichtlich ist,** aber Redundanz zwischen der Problem Anweisung und der Auflösung weglassen. **Ausnahmen:**
    -   Lassen Sie die Auflösung Weg, wenn Sie nicht oder ohne beträchtliche Redundanz ausgedrückt werden kann.
    -   Lassen Sie die Auflösung Weg, wenn für den Benutzer nichts zu tun ist, z. b. wenn falsche Zeichen ignoriert werden.
-   **Verwenden Sie vollständige Sätze mit endinterpunktions Zeichen.**
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
-   **Verwenden Sie nicht mehr als 200 Zeichen (in englischer Sprache), um die Lokalisierung zu ermöglichen.** Der Textkörper Text hat eine maximale Länge von 255 Zeichen und muss in der Lage sein, um mindestens 30 Prozent zu erweitern, um die Lokalisierung zu ermöglichen.

**Dokumentation**

Beim Verweis auf Luftballons:

-   Verwenden Sie den genauen Titeltext, einschließlich der Groß-/Kleinschreibung.
-   Verweisen Sie auf die Komponente als Sprechblase, nicht als Benachrichtigung oder Benachrichtigung.
-   Formatieren Sie den Titeltext nach Möglichkeit mithilfe von fettem Text. Andernfalls sollten Sie den Titel nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

