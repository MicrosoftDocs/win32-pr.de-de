---
title: Ballons
description: Eine Sprechblase ist ein kleines Popupfenster, das Benutzer über ein nicht kritisches Problem oder eine besondere Bedingung in einem Steuerelement informiert.
ms.assetid: 67092831-e573-4ad6-b1fc-baa1836031cb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 792974ebaaa946a3e1a4f05d52c8fd9ac32fc87a
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524554"
---
# <a name="balloons"></a>Ballons

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Eine Sprechblase ist ein kleines Popupfenster, das Benutzer über ein nicht kritisches Problem oder eine besondere Bedingung in einem Steuerelement informiert.

![Screenshot: Sprechblasen, der angibt, dass die Caps-Sperre aktiviert ist](images/ctrl-balloons-image1.png)

Ein typischer Balloon.

Sprechblasen verfügen über ein Symbol, einen Titel und Text, die alle optional sind. Im Gegensatz zu QuickInfos und Infotips verfügen Sprechblasen auch über ein Ende, das ihre Quelle identifiziert. In der Regel ist die Quelle ein Steuerelement, wenn dies der Fall ist, wird sie als [Besitzersteuerelement](glossary.md)bezeichnet.

Während Balloons Benutzer über nicht kritische Probleme informieren, verhindern sie probleme nicht, obwohl die Besitzerkontrolle dies möglicherweise tun kann. Alle nicht behandelten Probleme müssen von der Benutzeroberfläche des Besitzers (User Interface, UI) behandelt werden, wenn Benutzer versuchen, einen Commit für die Aktion durchzuführen.

Sprechblasen werden in der Regel mit Textfeldern oder Steuerelementen verwendet, die Textfelder zum Ändern von Werten verwenden, z. B. Kombinationsfelder, Listenansichten und Strukturansichten. Andere Arten von Steuerelementen sind ausreichend eingeschränkt und benötigen keine zusätzlichen Feedbacksprechblasen. Wenn außerdem ein Problem mit anderen Arten von Steuerelementen vorliegt, umfasst dies häufig Inkonsistenzen zwischen mehreren Steuerelementen, für die Sprechblasen nicht geeignet sind. Nur Texteingabesteuerelemente sind sowohl uneingeschränkt als auch eine häufige Quelle für [Single-Point-Fehler.](glossary.md)

Eine Benachrichtigung ist ein bestimmter Typ von Sprechblasen, der von einem [Infobereichssymbol](winenv-notification.md) angezeigt wird.

**Hinweis:** Richtlinien im Zusammenhang mit [Benachrichtigungen,](mess-notif.md) [QuickInfos und Infotips](ctrl-tooltips-and-infotips.md)sowie [Fehlermeldungen](mess-error.md) werden in separaten Artikeln vorgestellt.

**Ist dies das richtige Steuerelement?**

Orientieren Sie sich an folgenden Fragen:

-   **Werden in den Informationen ein Problem oder eine besondere Bedingung beschrieben?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Verwenden Sie keine Sprechblasen, um zusätzliche Informationen für ein Steuerelement anzuzeigen. Erwägen Sie stattdessen die Verwendung von [statischem Text,](glossary.md)[Infotips,](glossary.md) [progressiver Offenlegung](glossary.md)oder Eingabeaufforderungen.
-   **Kann das Problem oder die spezielle Bedingung sofort erkannt werden,** entweder bei der Eingabe oder wenn das Besitzersteuerelement den Eingabefokus verliert? Falls nicht, verwenden Sie eine Fehlermeldung, die in einem [Aufgabendialogfeld](glossary.md) oder [Meldungsfeld](glossary.md)angezeigt wird.
-   **Ist das Problem bei Problemen kritisch?** Verwenden Sie in diesem Falle eine Fehlermeldung, die in einem Aufgabendialogfeld oder Meldungsfeld angezeigt wird. Solche Fehlermeldungen erfordern eine Interaktion (die für kritische Fehler geeignet ist), wohingegen Balloons dies nicht tun.
-   **Ist die Bedingung für besondere Bedingungen gültig, aber wahrscheinlich unbeabsichtigt?** Wenn ja, sind Sprechblasen geeignet. Bei bedingungen, die nicht gültig sind, ist es besser, sie überhaupt zu verhindern. Für wahrscheinlich beabsichtigte Bedingungen ist es nicht erforderlich, etwas zu tun.
-   **Kann das Problem oder die spezielle Bedingung präzise ausgedrückt werden?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Balloons können keine ausführlichen Erklärungen enthalten oder zusätzliche Informationen bereitstellen.
-   **Beschreiben die Informationen das Steuerelement, auf das derzeit mit dem Mauszeiger geworfen wird?** Verwenden Sie in diesem Falle stattdessen einen Tipp, es sei denn, Benutzer müssen möglicherweise mit der Nachricht interagieren.
-   **Beziehen sich die Informationen auf die aktuelle Aktivität des Benutzers?** Andernfalls sollten Sie stattdessen eine [Benachrichtigung](mess-notif.md) oder ein [Dialogfeld](win-dialog-box.md) verwenden. Benutzer werden wahrscheinlich Sprechblasen außerhalb der aktuellen Aktivität übersehen, und standardmäßig tritt bei Sprechblasen nach 10 Sekunden ein Time out auf.
-   **Stammen die Informationen aus einer einzelnen, bestimmten Quelle?** Wenn ein Problem oder eine Bedingung mehrere Quellen oder keine bestimmte Quelle enthält, verwenden Sie stattdessen eine [nachricht](glossary.md) oder ein Dialogfeld.

**Falsch:** ![ Screenshot eines Sprechblasens: Anmeldung nicht erfolgreich](images/ctrl-balloons-image2.png)

In diesem Beispiel kann das Problem mit dem Benutzernamen oder dem Kennwort sein, aber die Meldung des Problems mit einer Sprechblase deutet visuell darauf hin, dass nur das Kennwort das Problem ist. Daher ist das Feedback aus der Eingabe eines falschen Benutzernamens irreführend.

Balloons sind eine Alternative zu Infotips, Dialogfeldern und ortsbezogenen Nachrichten. Im Gegensatz zu QuickInfos und Infotips gilt:

-   Balloons können unabhängig von der aktuellen Zeigerposition angezeigt werden, sodass sie über ein Ende verfügen, das ihre Quelle angibt.
-   Sprechblasen verfügen über einen Titel, Text und ein Symbol.
-   Balloons können interaktiv sein, während es unmöglich ist, auf einen Tipp zu klicken.

Im Gegensatz zu modalen Dialogfeldern:

-   Balloons stehlen den Eingabefokus nicht und erfordern keine Interaktion.
-   Sprechblasen identifizieren eine einzelne, bestimmte Quelle. Modale Dialoge können mehrere Quellen oder gar keine bestimmte Quelle aufweisen.

Im Gegensatz zu ortsbezogenen Nachrichten gilt:

-   Sprechblasen sind deutlich erkennbarer.
-   Für Sprechblasen ist kein verfügbarer Bildschirmbereich oder das dynamische Layout erforderlich, das zum Anzeigen von Nachrichten an Ort und Stelle erforderlich ist.
-   Balloons werden nach einem Timeout automatisch entfernt.

**Verwendungsmuster**

Balloons weisen diese Verwendungsmuster auf:



|   Verwendung                                                                                                                                                            |    Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eingabeproblem** Ein nicht kritisches Benutzereingabeproblem stammt von einem einzelnen Besitzersteuerelement, in der Regel einem Textfeld. <br/>                                               | Die Verwendung von Sprechblasen für Fehlermeldungen stiehlt den Eingabefokus nicht, ist aber dennoch sehr wahrnehmbar, wenn das Besitzersteuerelement über den Eingabefokus verfügt. um das Problem zu beheben, muss der Benutzer möglicherweise die Eingabe ändern oder erneut eingeben. Wenn das Besitzersteuerelement jedoch falsche Eingaben ignoriert, muss der Benutzer möglicherweise überhaupt keine Änderungen vornehmen. da das Problem nicht kritisch ist, ist kein [Fehlersymbol](vis-std-icons.md) erforderlich. <br/> ![Screenshot: Sprechblase, die ein falsches Zeichen angibt](images/ctrl-balloons-image3.png)<br/> Eine Sprechblase, die zum Melden eines nicht kritischen Benutzereingabeproblems verwendet wird.<br/>                                                                                                  |
| **Sonderbedingung** Das Besitzersteuerelement befindet sich in einem Zustand, der sich auf die Eingabe auswirkt. Dieser Zustand ist wahrscheinlich unbeabsichtigt, und der Benutzer erkennt möglicherweise nicht, dass die Eingabe betroffen ist. <br/> | Verwenden Sie Sprechblasen, um Frust zu vermeiden, indem Sie Benutzer über besondere Bedingungen informieren, sobald sie eintreten (z. B. Überschreitung der maximalen Eingabegröße oder versehentliches Festlegen von Obergrenzen). Es ist wichtig, ein solches Feedback zu geben, ohne den Eingabefokus zu stehlen oder die Interaktion zu erzwingen, da diese Bedingungen möglicherweise beabsichtigt sind. Diese Sprechblasen sind besonders wichtig für Kennwort- und Stecknadelfelder, bei denen Benutzer andernfalls mit minimalem Feedback arbeiten. Diese Sprechblasen weisen ein [Warnsymbol auf.](vis-std-icons.md) <br/> ![Screenshot, der Sprechblasen zeigt, die angeben, dass die Caps-Sperre aktiviert ist und ein falsches Zeichen eingegeben wird](images/ctrl-balloons-image4.png)<br/> Eine Sprechblase, die verwendet wird, um eine besondere Bedingung zu melden.<br/> |



 

**Richtlinien**

**Zeitpunkt der Anzeige**

-   **Zeigen Sie den Sprechblasen an, sobald das Problem oder die besondere Bedingung erkannt wird, auch wenn er wiederholt ohne merkliche Verzögerung erkannt wird.**
    -   Bei Problemen mit einzelnen Zeichen oder der maximalen Eingabegröße zeigen Sie den Sprechblasen sofort bei der Eingabe an.
    -   Bei Problemen mit dem Eingabewert (einschließlich der Anforderung eines nicht leeren Werts) zeigen Sie den Sprechblasen an, wenn das Besitzersteuerelement den Eingabefokus verliert. Andernfalls kann das Anzeigen von Sprechblasen, während Benutzer potenziell gültige Eingaben eingeben, ablenkend und nervig sein.
-   **Zeigen Sie jeweils nur einen Sprechblasen an.** Das Anzeigen mehrerer Sprechblasen kann überwältigend sein. Wenn ein einzelnes Ereignis zu mehreren Problemen führt, stellen Sie entweder alle Probleme gleichzeitig dar, oder melden Sie nur das wichtigste Problem.

**Falsch:** ![ Screenshot von zwei Sprechblasen, die auf ein Feld zeigen](images/ctrl-balloons-image5.png)

In diesem Beispiel werden zwei Probleme fälschlicherweise gleichzeitig dargestellt.

**Anzeigedauer**

-   **Entfernen sie eine Sprechblase, wenn:**
    -   Das Problem wurde behoben, oder eine sonderliche Bedingung wird entfernt.
    -   Der Benutzer gibt gültige Daten ein (für Eingabeprobleme).
    -   Die Sprechblase führt zu einem Zeitsendaus. Standardmäßig entfernen sich Sprechblasen nach 10 Sekunden selbst, obwohl Benutzer dies ändern können, indem sie den \_ SPI MESSAGEDURATION-Systemparameter ändern.
-   **Entfernen Sie das Timeout, wenn Benutzer erst fortfahren können, wenn das Problem behoben ist. Entwickler:** In Win32 können Sie die Anzeigezeit mit der TTM \_ SETDELAYTIME-Meldung festlegen.

**Anzeigen**

-   **Zeigen Sie Sprechblasen unterhalb ihres Besitzersteuerelements an.** Auf diese Weise können Benutzer den Kontext anzeigen, einschließlich des Besitzersteuerelements und seiner Bezeichnung. Microsoft Windows passt die Sprechblasenpositionen automatisch so an, dass sie vollständig auf dem Bildschirm angezeigt werden. Das Standardverhalten besteht darin, wie bei Benachrichtigungen eine Sprechblase über dem Besitzersteuerelement anzuzeigen.

**Richtig:** ![ Screenshot eines Sprechblasens, der unterhalb des Steuerelements angezeigt wird](images/ctrl-balloons-image6.png)

**Falsch:** ![ Screenshot einer Sprechblase, die über dem Steuerelement angezeigt wird](images/ctrl-balloons-image7.png)

Im falschen Beispiel wird der Sprechblasen umstaulich über seinem Besitzer-Steuerelement angezeigt.

**Kennwort- und PIN-Textfelder**

-   **Verwenden Sie eine Sprechblase,** um anzugeben, dass die Sperre für Obergrenze auf ist, indem Sie den Text im folgenden Beispiel verwenden:

![Screenshot eines Balloons, der angibt, dass die Sperre für Die Obergrenzen ist](images/ctrl-balloons-image8.png)

In diesem Beispiel gibt eine Sprechblase an, dass die Sperre für Schließnadeln in einem PIN-Textfeld ein-/aus ist.

-   **Verwenden Sie einen Balloon, um anzugeben, wann Benutzer versuchen, die maximale Eingabegröße zu überschreiten.** Das Erreichen der maximalen Eingabegröße ist in Kennwort- und PIN-Textfeldern deutlich weniger offensichtlich als normale Textfelder.

![Screenshot einer Sprechblase, die pin code limits angibt](images/ctrl-balloons-image9.png)

In diesem Beispiel gibt ein Balloon an, dass der Benutzer versucht, die maximale Eingabegröße zu überschreiten.

-   **Verwenden Sie eine Sprechblase, um anzugeben, wenn Benutzer falsche Zeichen eingeben.** Es ist jedoch besser, solche Einschränkungen nicht zu verwenden, da sie die Sicherheit des Kennworts oder der PIN verringern. Um die Veröffentlichung von Informationen zu verhindern, sollte der Balloon nur dokumentierte Fakten zu gültigen Kennwörtern oder PINs enthalten.

![Screenshot eines Balloons, der auf eine falsche Eingabe hinweist](images/ctrl-balloons-image10.png)

In diesem Beispiel gibt ein Balloon an, dass die PIN Zahlen erfordert.

**Andere Textfelder**

-   **Erwägen Sie die Verwendung einer Sprechblase, um anzugeben, wann Benutzer versuchen, die maximale Eingabegröße für kritische, kurze Textfelder zu überschreiten, die auf unerfahrene Benutzer ausgerichtet sind.** Beispiele hierfür sind Benutzernamen und Kontonamen. Textfelder werden angezeigt, wenn Benutzer versuchen, die maximale Eingabe zu überschreiten, aber erfahrene Benutzer die Bedeutung des Signaltons möglicherweise nicht verstehen.

![Screenshot einer Sprechblase, die Zeichengrenzwerte angibt](images/ctrl-balloons-image11.png)

In diesem Beispiel gibt eine Sprechblase an, dass der Benutzer versucht hat, die maximale Eingabegröße zu überschreiten.

**Interaktion**

-   **Wenn Benutzer auf eine Sprechblase klicken, verdringen Sie einfach den Balloon, ohne eine andere Benutzeroberfläche anzuzeigen oder einen anderen Nebeneffekt zu haben.** Im Gegensatz zu Benachrichtigungen sollten Sprechblasen keine Schaltflächen zum Schließen enthalten.

**Symbole**

-   Wählen Sie das Symbol basierend auf dem Verwendungsmuster aus:



    |  Muster |  Symbol                                                                                                                                                       |
    ------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Eingabeproblem | Kein Symbol. Die Verwendung eines [Fehlersymbols](vis-std-icons.md) hier entspricht den [Windows-Tonrichtlinien.](text-style-tone.md) |
    | Besondere Bedingung | Das Standardmäßige Warnsymbol mit 16 x 16 [Pixeln.](vis-std-icons.md)                                                                                  |

**Bedienungshilfen**

Bei ordnungsgemäßer Verwendung verbessern Sprechblasen die Barrierefreiheit. Damit auf Sprechblasen zugegriffen werden kann:

-   Zeigt nur Sprechblasen an, die sich auf die aktuelle Aktivität des Benutzers beziehen.
-   Halten Sie den Sprechblasentext kurz. Dadurch ist der Sprechblasentext für Benutzer mit seharmer Sehkraft leichter lesbar und minimiert die Unterbrechung beim Lesen durch Sprachbildschirme.
-   Zeigt den Sprechblasen wieder an, wenn das Problem oder die Bedingung erneut auftritt.

**Text**

**Titeltext**

-   **Verwenden Sie Titeltext, der das Eingabeproblem oder die spezielle Bedingung kurz in einer klar, einfachen, präzisen und spezifischen Sprache zusammenfasst.** Benutzer sollten in der Lage sein, den Zweck des Balloons schnell und mit minimalem Aufwand zu verstehen.
-   **Verwenden Sie Textfragmente oder vollständige Sätze, ohne die Interpunktion zu beenden.**
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.** Weitere Informationen finden Sie im [Glossar](./glossary.md).
-   **Verwenden Sie für die Lokalisierung nicht mehr als 48 Zeichen (auf Englisch).** Der Titel hat eine maximale Länge von 63 Zeichen und muss um mindestens 30 Prozent erweitert werden können, um die Lokalisierung zu bieten.

**Textkörper**

-   **Verwenden Sie den ersten Satz des Textkörpers, um das Problem oder die Bedingung auf eine Weise zu sagen, die für den Benutzer eindeutig relevant ist.** Wiederholen Sie die Informationen im Titel nicht. Lässt dies aus, wenn nichts mehr hinzugefügt werden muss.
-   **Verwenden Sie den zweiten Satz, um zu geben, was der Benutzer tun kann, um das Problem zu beheben oder den Zustand wie zu setzen.** In Übereinstimmung mit den [Richtlinien für Stil](./text-style-tone.md) und Ton ist es nicht notwendig, das Wort Please in dieser Anweisung zu verwenden. Setzen Sie zwei Zeilenumbrüche zwischen dem ersten und zweiten Satz.

![Screenshot einer Sprechblase mit Titel und Textkörper](images/ctrl-balloons-image12.png)

Dieses Beispiel zeigt das Standardmäßige Sprechblasentextlayout.

-   **Erläutern Sie, wie Sie das Problem beheben** oder den Zustand bzw. die Redundanz zwischen der Problem-Anweisung und deren Lösung selbst dann bzw. rückgängig machen, wenn diese Erklärung offensichtlich ist, aber die Redundanz zwischen der Problemerklärung und deren Lösung weglassen. **Ausnahmen:**
    -   Lassen Sie die Auflösung weg, wenn sie nicht präzise oder ohne signifikante Redundanz ausgedrückt werden kann.
    -   Lassen Sie die Auflösung weg, wenn der Benutzer nichts zu tun hat, z. B. wenn falsche Zeichen ignoriert werden.
-   **Verwenden Sie vollständige Sätze mit endender Interpunktion.**
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
-   **Verwenden Sie für die Lokalisierung nicht mehr als 200 Zeichen (auf Englisch).** Der Textkörper hat eine maximale Länge von 255 Zeichen und muss um mindestens 30 Prozent erweitert werden können, um die Lokalisierung zu bieten.

**Dokumentation**

Beim Verweisen auf Sprechblasen:

-   Verwenden Sie den genauen Titeltext, einschließlich der Groß-/Groß-/Groß-/A-
-   Verweisen Sie auf die Komponente als Sprechblasen, nicht als Benachrichtigung oder Warnung.
-   Formatieren Sie den Titeltext nach Möglichkeit fett formatieren. Andernfalls setzen Sie den Titel nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

