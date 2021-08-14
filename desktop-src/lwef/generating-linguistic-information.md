---
title: Generieren linguistischer Informationen
description: Generieren linguistischer Informationen
ms.assetid: 903561f0-89dc-4297-8ea0-3fa150f2e6dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a068153863236b7096b67a976bbcf0654af9c75df87d2f527027830a4df33eb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479308"
---
# <a name="generating-linguistic-information"></a>Generieren linguistischer Informationen

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

Nachdem Sie eine neue Sounddatei aufgezeichnet oder eine vorhandene Sounddatei geladen haben, können Sie phonetische Und Wörterbruchinformationen generieren, indem Sie Text eingeben, der Ihrer Sounddatei im Feld **Textdarstellung entspricht.** Wählen Sie dann im Menü  Bearbeiten oder auf der Symbolleiste den Befehl Linguistische **Informationen** generieren aus. Der Sound-Editor zeigt eine Statusmeldung an und beginnt mit der Verarbeitung Ihrer Sounddatei. Wenn die Generierung linguistischer Informationen abgeschlossen ist, wird eine Zuordnung von Wort- und Phonembezeichnungen für die Sounddatei in Feldern im Feld **Audiodarstellung** angezeigt. Beachten Sie, dass **der Befehl Linguistische Informationen generieren** deaktiviert bleibt, bis Sie eine Textdarstellung für Ihre Sounddatei eingeben.

![Screenshot, der die Bereiche "Textdarstellung" und "Audiodarstellung" im Microsoft Linguistic Information Sound Editing Tool zeigt.](images/f3listlabel.gif)

Wenn der Editor keine akzeptablen Wort- oder Phonembezeichnungen erzeugt, wählen Sie erneut den Befehl **Linguistische Informationen** generieren aus. Wenn der Editor keine linguistischen Informationen generiert, überprüfen Sie Ihre Textdarstellung, um sicherzustellen, dass alle Wörter ordnungsgemäß geordnet und geschrieben sind und dass keine unnötigen Leerzeichen um Satzzeichen entstehen. Wählen Sie dann erneut **den Befehl Linguistische Informationen** generieren aus. Sie können die Textdarstellung bearbeiten, indem Sie text im **Textfeld Textdarstellung** auswählen und im Menü Bearbeiten die Befehle Ausschneiden, Kopieren und  **Einfügen** verwenden.   Wenn Sie nicht sicher sind, welche Wörter die Sounddatei enthält, können  Sie die Sounddatei wiedererlangen, indem Sie im Menü Bearbeiten oder auf der Symbolleiste des Editors auf Wiedergabe klicken.  Wenn der Editor weiterhin keine linguistischen Bezeichnungen erzeugt, versuchen Sie erneut, Ihre Sounddatei aufzeichnen. Eine Aufzeichnung mit schlechter Qualität, insbesondere bei übermäßigem Hintergrundrauschen, verringert wahrscheinlich die Wahrscheinlichkeit, angemessene linguistische Informationen zu generieren.

Sie können auch manuell eigene linguistische Informationen erstellen, indem Sie einen  Teil der Audiodarstellung auswählen und im Menü Bearbeiten die Option **Phoneme** einfügen **oder Wort** einfügen auswählen. Diese Befehle sind auch verfügbar, wenn Sie innerhalb der Auswahl mit der rechten Maustaste klicken.

Um zu sehen, wie die linguistischen Informationen zum Synchronisieren von  Zeichenanimationen mit Microsoft Agent verwendet werden können, klicken Sie auf der Symbolleiste auf die Schaltfläche Wiedergabe, und der Editor gibt Ihre Sounddatei wieder und animiert ein Beispielbild für ein Bild mit einer Bezeichnung basierend auf den generierten Bezeichnungsinformationen.

Sie können die Anzeige der Phonemebezeichnung ändern, um die IPA-Zuweisungen (Internationales  phonetisches Alphabet) anzuzeigen, indem Sie im Menü Bearbeiten den Befehl **Phoneme Label Display (Phoneme-Bezeichnungsanzeige)** und dann den IPA-Befehl auswählen. Dadurch wird der Bytewert für die Phoneme angezeigt. Um wieder zu den beschreibenden Namen zu wechseln, wählen Sie erneut den **Befehl Phoneme Label Display (Phoneme-Bezeichnungsanzeige)** und dann **Name aus.**

### <a name="playing-a-sound-file"></a>Wiederklangen einer Sounddatei

Sie können standardmäßige Windows Sounddateien oder linguistisch verbesserte Sounddateien wiedererlangen, indem Sie im Menü **Audio** oder auf der Symbolleiste des Editors auf den Befehl Wiedergabe klicken.  Mit **den Befehlen Anhalten** und **Beenden** können Sie die Wiedergabe der Sounddatei anhalten oder beenden. Während Sie die Datei wiederverspielen, wird das Beispielbild animiert, um zu zeigen, wie die Informationen zur Synchronisierung von einem Microsoft Agent-Zeichen verwendet werden können.

Sie können auch einen ausgewählten Teil einer Sounddatei wieder geben, indem Sie eine Auswahl in die **Audiodarstellung** ziehen oder auf eine Wort- oder Phonembezeichnung klicken und dann **Wieder geben auswählen.** Sie können eine vorhandene Auswahl erweitern, indem Sie umschalten und klicken oder UMSCHALT drücken und an die neue Position in der **Audiodarstellung ziehen.**

### <a name="editing-linguistic-information"></a>Bearbeiten linguistischer Informationen

Sie können die linguistischen Informationen einer Datei auf verschiedene Weise bearbeiten. Beispielsweise können Sie die Begrenzung eines Worts oder einer Phonembezeichnung anpassen, indem Sie den Zeiger an den Rand des Felds bewegen, das den Bereich der Bezeichnung definiert. Wenn sich der Zeiger auf den Begrenzungszeiger zum Verschieben ändert, ziehen Sie nach links oder rechts. Der Editor passt auch automatisch die angrenzende Wort- oder Phonemgrenze an.

![Screenshot: Bearbeitungen der linguistischen Informationen einer Datei](images/f4listadj.gif)

Das Anpassen der Begrenzung einer Phonembezeichnung ändert die Zeitlichkeit eines Phonems, wenn die Audiowiedergabe abläuft. Bei Zeichen, die für die Verwendung mit Microsoft Agent entwickelt wurden, kann das Ändern der Phonembeschriftungsgrenze den Zeitlichen oder die Dauer für ein diesem Phonem zugeordnetes Bild ändern. Das Ändern der Begrenzung einer Wortbezeichnung ändert den Zeitlichen der Darstellung des Worts im Wortsprechblasen des Zeichens.

Sie können eine Phonemzuweisung auch ersetzen, indem Sie die Phonembezeichnung auswählen und im Menü Bearbeiten auf **Phoneme** ersetzen klicken oder mit der rechten Maustaste auf die Phonembezeichnung klicken und im Popupmenü **Phoneme** ersetzen auswählen.  Der Editor zeigt das **Dialogfeld Phoneme ersetzen** an und hebt die aktuelle Phonemzuweisung der Bezeichnung hervor. Sie können ein Ersatztelefon auswählen, indem Sie ein Phonem in der **IPA-Liste** oder einen anderen Eintrag in der **Liste Name** auswählen. Wenn für diesen Namen mehr als eine IPA-Übersetzung verfügbar ist, wählen Sie ein Element in der **IPA-Liste** aus. Geben Sie zum Eingeben einer IPA-Bezeichnung für ein Phonem, das möglicherweise nicht direkt in der Sprache enthalten ist, den Hexadezimalwert oder mehrere Hexadezimalwerte ein, die mit einem Pluszeichen (+) verkettet sind. Nachdem Sie die Informationen zum Ersatztelefon ausgewählt haben, wählen Sie **OK aus,** und der Editor ersetzt die von Ihnen ausgewählte Phonembezeichnung.

![Screenshot des Dialogfelds "Phoneme ersetzen", in dem "<SIL>" als beschreibende Bezeichnung ausgewählt ist](images/f5listphone.gif)

Auf ähnliche Weise können Sie eine Wortbezeichnung ersetzen, indem Sie auf das Feld der Bezeichnung klicken und Word  ersetzen auswählen, oder indem Sie mit der rechten Maustaste auf das Feld der Bezeichnung klicken und im Popupmenü Word ersetzen auswählen. Im Editor wird das **Dialogfeld Word ersetzen** angezeigt. Geben Sie das Ersetzungswort ein, und wählen Sie **OK aus.**

![Screenshot: Dialogfeld "Word ersetzen" mit "Sound" im Textfeld "Word-Text"](images/f6listrep.gif)

Bei Zeichen, die für die Verwendung mit Microsoft Agent entwickelt wurden, kann das Ersetzen einer Phonembezeichnung das Bild ändern, das angezeigt wird, wenn die Sounddatei abspielt. Durch ersetzen eines Worts wird der Text ersetzt, der im Wortsprechblasen des Zeichens angezeigt wird, wenn die [**Speak-Methode**](speak-method.md) aufgerufen wird.

Sie können auch eine neue Phonembezeichnung oder ein neues Wort einfügen, indem  Sie in  der **Audiodarstellung** eine Auswahl treffen und im Menü Bearbeiten die Optionen **Phoneme** einfügen oder Wort einfügen auswählen oder mit der rechten Maustaste in die Auswahl klicken und die Befehle aus dem Popupmenü auswählen. Diese Befehle öffnen Dialogfelder, die den Dialogfeldern **Phoneme** ersetzen und **Word** ersetzen ähneln, mit der Ausnahme, dass der Editor das neue Wort oder phonem einfüge, anstatt die vorhandenen Informationen zu ersetzen.

Schließlich können Sie ein Phonem oder Wort löschen, indem Sie seine Bezeichnung und dann **Phoneme** löschen oder **Wort löschen auswählen.** Dadurch werden die linguistischen Informationen aus der Datei entfernt.

 

 




