---
title: Ballons
description: Ein Balloon ist ein kleines Popupfenster, das Benutzer über ein nicht kritisches Problem oder eine besondere Bedingung in einem Steuerelement informiert.
ms.assetid: 67092831-e573-4ad6-b1fc-baa1836031cb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ea95eee6e745dc85dbe7cd354df0906b5df4a7870198fc662effd326c6fbaae9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119818692"
---
# <a name="balloons"></a>Ballons

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Ein Balloon ist ein kleines Popupfenster, das Benutzer über ein nicht kritisches Problem oder eine besondere Bedingung in einem Steuerelement informiert.

![Screenshot, der eine Sprechblase zeigt, die angibt, dass die Sperre für Schließenden ein-/aus ist.](images/ctrl-balloons-image1.png)

Ein typischer Sprechblasen.

Sprechblasen verfügen über ein Symbol, einen Titel und Textkörper, die alle optional sind. Im Gegensatz zu QuickInfos und Infotips verfügen Sprechblasen auch über ein Ende, das ihre Quelle identifiziert. In der Regel handelt es sich bei der Quelle um ein Steuerelement, wenn dies der Fall ist, wird es als [Besitzersteuer steuerelement bezeichnet.](glossary.md)

Zwar informieren Sprechblasen Benutzer über nicht kritische Probleme, sie verhindern jedoch keine Probleme, obwohl die Besitzersteuerung möglicherweise ist. Nicht behandelte Probleme müssen von der Besitzer-Benutzeroberfläche behandelt werden, wenn Benutzer versuchen, sich für die Aktion zu verpflichten.

Sprechblasen werden in der Regel mit Textfeldern oder Steuerelementen verwendet, die Textfelder zum Ändern von Werten verwenden, z. B. Kombinationsfelder, Listenansichten und Strukturansichten. Andere Arten von Steuerelementen sind ausreichend eingeschränkt und benötigen keine zusätzlichen Feedbacksprechblasen. Wenn außerdem ein Problem mit anderen Steuerelementtypen besteht, ist dies häufig mit Inkonsistenz zwischen mehreren Steuerelementen in einer Situation zu tun, in der Sprechblasen nicht geeignet sind. Nur Texteingabesteuerelemente sind sowohl ungeniert als auch eine häufige Quelle für [Single-Point-Fehler.](glossary.md)

Eine Benachrichtigung ist ein bestimmter Sprechblasentyp, der durch ein Symbol für den [Benachrichtigungsbereich angezeigt](winenv-notification.md) wird.

**Hinweis:** Richtlinien im [](mess-notif.md)Zusammenhang mit Benachrichtigungen, [QuickInfos und Infotips](ctrl-tooltips-and-infotips.md)sowie [Fehlermeldungen](mess-error.md) werden in separaten Artikeln vorgestellt.

**Ist dies das richtige Steuerelement?**

Orientieren Sie sich an folgenden Fragen:

-   **Beschreiben die Informationen ein Problem oder eine besondere Bedingung?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Verwenden Sie keine Sprechblasen, um zusätzliche Informationen für ein Steuerelement anzuzeigen. Erwägen Sie stattdessen [die Verwendung von statischem](glossary.md)Text,[Infotips,](glossary.md) [progressiver](glossary.md)Offenlegung oder Eingabeaufforderungen.
-   **Kann das Problem oder die spezielle Bedingung sofort** erkannt werden, entweder bei der Eingabe oder wenn das Besitzersteuerfeld den Eingabefokus verliert? Wenn nicht, verwenden Sie eine Fehlermeldung, die in einem [Aufgabendialogfeld oder Meldungsfeld](glossary.md) [angezeigt wird.](glossary.md)
-   **Ist das Problem bei Problemen von entscheidender Bedeutung?** Wenn ja, verwenden Sie eine Fehlermeldung, die in einem Aufgabendialogfeld oder Meldungsfeld angezeigt wird. Solche Fehlermeldungen erfordern eine Interaktion (die für kritische Fehler geeignet ist), Sprechblasen hingegen nicht.
-   **Ist die Bedingung für spezielle Bedingungen gültig, aber wahrscheinlich unbeabsichtigt?** Wenn ja, sind Sprechblasen geeignet. Bei ungültigen Bedingungen ist es besser, sie von Anfang an zu verhindern. Für wahrscheinlich beabsichtigte Bedingungen ist es nicht notwendig, etwas zu tun.
-   **Kann das Problem oder die spezielle Bedingung präzise ausgedrückt werden?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Balloons können keine ausführlichen Erklärungen enthalten oder zusätzliche Informationen bereitstellen.
-   **Beschreiben die Informationen das Steuerelement, auf das gerade zeigt?** Falls ja, verwenden Sie stattdessen ein Trinkgeld, es sei denn, Benutzer müssen möglicherweise mit der Nachricht interagieren.
-   **Bezieht sich die Information auf die aktuelle Aktivität des Benutzers?** Falls nicht, sollten Sie stattdessen eine [Benachrichtigung](mess-notif.md) [oder ein Dialogfeld](win-dialog-box.md) verwenden. Benutzer werden wahrscheinlich Sprechblasen außerhalb der aktuellen Aktivität übersehen, und standardmäßig wird nach 10 Sekunden ein Time out für Sprechblasen durchgeführt.
-   **Stammen die Informationen aus einer einzelnen, spezifischen Quelle?** Wenn ein Problem oder eine Bedingung über mehrere Quellen oder keine bestimmte Quelle verfügt, verwenden Sie stattdessen eine [in-place-Nachricht](glossary.md) oder ein Dialogfeld.

**Falsch:** ![ Screenshot eines Balloons: Anmeldung nicht erfolgreich](images/ctrl-balloons-image2.png)

In diesem Beispiel könnte das Problem mit dem Benutzernamen oder dem Kennwort sein, aber die Meldung des Problems mit einem Balloon deutet darauf hin, dass nur das Kennwort das Problem ist. Daher ist das Feedback der Eingabe eines falschen Benutzernamens irreführend.

Balloons sind eine Alternative zu Infotips, Dialogfeldern und in-place-Nachrichten. Im Gegensatz zu QuickInfos und Infotips:

-   Sprechblasen können unabhängig von der aktuellen Zeigerposition angezeigt werden, sodass sie über ein Ende verfügen, das ihre Quelle angibt.
-   Sprechblasen verfügen über einen Titel, Textkörper und ein Symbol.
-   Balloons können interaktiv sein, während es unmöglich ist, auf einen Tipp zu klicken.

Im Gegensatz zu modalen Dialogfeldern:

-   Sprechblasen stehlen keinen Eingabefokus oder erfordern eine Interaktion.
-   Balloons identifizieren eine einzelne, spezifische Quelle. Modale Dialoge können mehrere Quellen oder gar keine bestimmte Quelle haben.

Im Gegensatz zu in-place-Nachrichten:

-   Sprechblasen sind deutlicher.
-   Für Sprechblasen ist kein verfügbarer Bildschirmbereich oder das dynamische Layout erforderlich, das zum Anzeigen von meldungen an Ort und Stelle erforderlich ist.
-   Balloons entfernen sich nach einem Timeout automatisch selbst.

**Verwendungsmuster**

Balloons verfügen über die folgenden Verwendungsmuster:



|   Verwendung                                                                                                                                                            |    Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eingabeproblem** Ein nicht kritisches Benutzereingabeproblem, das von einem einzelnen Besitzersteuerfeld (in der Regel einem Textfeld) kommt. <br/>                                               | Die Verwendung von Sprechblasen für Fehlermeldungen stiehlt den Eingabefokus nicht, ist aber immer noch sehr merklich, wenn das Besitzersteuerfeld den Eingabefokus besitzt. um das Problem zu beheben, muss der Benutzer die Eingabe möglicherweise ändern oder erneut eingeben. Wenn das Besitzersteuerfeld jedoch falsche Eingaben ignoriert, muss der Benutzer möglicherweise überhaupt keine Änderungen vornehmen. da das Problem nicht kritisch ist, ist [kein Fehlersymbol](vis-std-icons.md) erforderlich. <br/> ![Screenshot: Sprechblasen mit einem falschen Zeichen](images/ctrl-balloons-image3.png)<br/> Ein Balloon, der verwendet wird, um ein nicht kritisches Benutzereingabeproblem zu melden.<br/>                                                                                                  |
| **Besondere Bedingung** Das Besitzersteuerfeld befindet sich in einem Zustand, der sich auf die Eingabe auswirken kann. Dieser Zustand ist wahrscheinlich unbeabsichtigt, und der Benutzer erkennt möglicherweise nicht, dass die Eingabe betroffen ist. <br/> | Verwenden Sie Sprechblasen, um Frust zu verhindern, indem Sie Benutzer vor besonderen Bedingungen warnen, sobald sie vorkommen (z. B. die maximale Eingabegröße überschreiten oder die Sperre für Obergrenzen aus Versehen festlegen). es ist wichtig, solches Feedback zu geben, ohne den Eingabefokus zu stehlen oder die Interaktion zu erzwingen, da diese Bedingungen möglicherweise absichtlich sind. diese Sprechblasen sind besonders wichtig für Kennwort- und Stecknadelfelder, bei denen Benutzer andernfalls mit minimalem Feedback arbeiten. Diese Sprechblasen verfügen über [ein Warnsymbol.](vis-std-icons.md) <br/> ![Screenshot, der Sprechblasen zeigt, die darauf hinweisen, dass die Sperre für Obergrenzen ein-/aus ist und ein falsches Zeichen eingegeben wird.](images/ctrl-balloons-image4.png)<br/> Ein Sprechblasen, der verwendet wird, um eine besondere Bedingung zu melden.<br/> |



 

**Richtlinien**

**Wann wird angezeigt?**

-   **Zeigen Sie die Sprechblase an, sobald das Problem oder die spezielle Bedingung erkannt wird, auch wenn sie wiederholt und ohne erkennbare Verzögerung angezeigt wird.**
    -   Bei Problemen mit einzelnen Zeichen oder der maximalen Eingabegröße zeigen Sie die Sprechblase sofort bei der Eingabe an.
    -   Bei Problemen mit dem Eingabewert (einschließlich der Anforderung eines nicht leeren Werts) zeigen Sie den Balloon an, wenn das Besitzersteuerfeld den Eingabefokus verliert. Andernfalls kann das Anzeigen von Sprechblasen während der Eingabe potenziell gültiger Eingaben störend und störend sein.
-   **Zeigt immer nur einen Sprechblasen gleichzeitig an.** Das Anzeigen mehrerer Sprechblasen kann überfordernd sein. Wenn ein einzelnes Ereignis zu mehreren Problemen führt, stellen Sie entweder alle Probleme gleichzeitig dar, oder melden Sie nur das wichtigste Problem.

**Falsch:** ![ Screenshot von zwei Sprechblasen, die auf einen Kasten zeigen](images/ctrl-balloons-image5.png)

In diesem Beispiel werden zwei Probleme fälschlicherweise gleichzeitig dargestellt.

**Wie lange wird angezeigt?**

-   **Entfernen Sie eine Sprechblase, wenn:**
    -   Das Problem wurde behoben, oder eine spezielle Bedingung wurde entfernt.
    -   Der Benutzer gibt gültige Daten ein (für Eingabeprobleme).
    -   Der Sprechblasenzeit-Zeitsendzeit. Standardmäßig entfernen sich Sprechblasen nach 10 Sekunden selbst, obwohl Benutzer dies ändern können, indem sie den Systemparameter SPI \_ MESSAGEDURATION ändern.
-   **Entfernen Sie das Timeout, wenn Benutzer nicht fortfahren können, bis das Problem behoben ist. Entwickler:** In Win32 können Sie die Anzeigezeit mit der \_ TTM-Meldung SETDELAYTIME festlegen.

**Anzeigen von**

-   **Anzeigen von Sprechblasen unterhalb des Besitzer-Steuerelements.** Auf diese Weise können Benutzer den Kontext anzeigen, einschließlich des Besitzersteuerzeichens und seiner Bezeichnung. Microsoft Windows automatisch Sprechblasenpositionen so an, dass sie vollständig auf dem Bildschirm angezeigt werden. Das Standardverhalten besteht in der Anzeige eines Balloons über seinem Besitzer-Steuerelement, wie es bei Benachrichtigungen erfolgt.

**Richtig:** ![ Screenshot eines Balloons, der unter seinem Steuerelement angezeigt wird](images/ctrl-balloons-image6.png)

**Falsch:** ![ Screenshot einer Sprechblase, die über dem Steuerelement angezeigt wird](images/ctrl-balloons-image7.png)

Im falschen Beispiel wird die Sprechblase umstaulich über dem Besitzer-Steuerelement angezeigt.

**Kennwort- und PIN-Textfelder**

-   **Verwenden Sie eine Sprechblase,** um anzugeben, dass die Sperre für Obergrenze auf ist, indem Sie den Text im folgenden Beispiel verwenden:

![Screenshot eines Balloons, der angibt, dass die Sperre für Die Obergrenzen ist](images/ctrl-balloons-image8.png)

In diesem Beispiel gibt eine Sprechblase an, dass die Sperre für Schließnadeln in einem PIN-Textfeld ein-/aus ist.

-   **Verwenden Sie einen Balloon, um anzugeben, wann Benutzer versuchen, die maximale Eingabegröße zu überschreiten.** Das Erreichen der maximalen Eingabegröße ist in Kennwort- und PIN-Textfeldern deutlich weniger offensichtlich als normale Textfelder.

![Screenshot einer Sprechblase, die pin code limits angibt](images/ctrl-balloons-image9.png)

In diesem Beispiel gibt eine Sprechblase an, dass der Benutzer versucht, die maximale Eingabegröße zu überschreiten.

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
    | Eingabeproblem | Kein Symbol. Die Verwendung eines [Fehlersymbols](vis-std-icons.md) hier entspricht den richtlinien für Windows [Tonfall.](text-style-tone.md) |
    | Besondere Bedingung | Das Standardmäßige Warnsymbol mit 16 x 16 [Pixeln.](vis-std-icons.md)                                                                                  |

**Bedienungshilfen**

Bei ordnungsgemäßer Verwendung verbessern Sprechblasen die Barrierefreiheit. Damit auf Sprechblasen zugegriffen werden kann:

-   Zeigt nur Sprechblasen an, die sich auf die aktuelle Aktivität des Benutzers beziehen.
-   Halten Sie den Sprechblasentext kurz. Dadurch wird der Sprechblasentext für Benutzer mit seharmer Sehkraft leichter lesbar, und die Unterbrechung beim Lesen durch Sprachlesegeräte wird minimiert.
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

-   **Erläutern Sie, wie Sie das Problem beheben** oder den Zustand bzw. die Redundanz zwischen der Problemerklärung und ihrer Lösung bzw. der Problemerklärung bzw. -lösung bzw. -anweisungen **Ausnahmen:**
    -   Lassen Sie die Auflösung weg, wenn sie nicht präzise oder ohne signifikante Redundanz ausgedrückt werden kann.
    -   Lassen Sie die Auflösung weg, wenn der Benutzer nichts zu tun hat, z. B. wenn falsche Zeichen ignoriert werden.
-   **Verwenden Sie vollständige Sätze mit endender Interpunktion.**
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
-   **Verwenden Sie nicht mehr als 200 Zeichen (auf Englisch), um die Lokalisierung zu bieten.** Der Textkörper hat eine maximale Länge von 255 Zeichen und muss zur Lokalisierung um mindestens 30 Prozent erweitert werden können.

**Dokumentation**

Beim Verweisen auf Sprechblasen:

-   Verwenden Sie den genauen Titeltext, einschließlich der Groß-/Groß-/Groß-/A-
-   Verweisen Sie auf die Komponente als Sprechblasen, nicht als Benachrichtigung oder Warnung.
-   Formatieren Sie den Titeltext nach Möglichkeit fett formatieren. Andernfalls setzen Sie den Titel nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

