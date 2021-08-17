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

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Nachdem Sie eine neue Sounddatei aufgezeichnet oder eine vorhandene Sounddatei geladen haben, können Sie phonetische und Wörterbruchinformationen generieren, indem Sie Text eingeben, der Ihrer Sounddatei entspricht, in das Feld **Textdarstellung.** Wählen Sie dann im Menü **Bearbeiten** oder auf der Symbolleiste den Befehl **Linguistische Informationen generieren** aus. Der Sound-Editor zeigt eine Statusmeldung an und beginnt mit der Verarbeitung Ihrer Sounddatei. Wenn das Generieren linguistischer Informationen abgeschlossen ist, wird eine Zuordnung von Wort- und Phonemebezeichnungen für die Sounddatei in Feldern im Feld **Audiodarstellung angezeigt.** Beachten Sie, dass der Befehl **Linguistische Info generieren** deaktiviert bleibt, bis Sie eine Textdarstellung für Ihre Sounddatei eingeben.

![Screenshot der Bereiche "Textdarstellung" und "Audiodarstellung" im Microsoft Linguistic Information Sound Editing Tool](images/f3listlabel.gif)

Wenn der Editor keine akzeptablen Wort- oder Phonemebezeichnungen erzeugt, wählen Sie erneut den Befehl **Linguistische Info generieren** aus. Wenn der Editor keine linguistischen Informationen generiert, überprüfen Sie Ihre Textdarstellung, um sicherzustellen, dass alle Wörter richtig sortiert und geschrieben sind und dass Keine unnötigen Leerzeichen um Satzzeichen herum vorhanden sind. Wählen Sie dann erneut den Befehl **Linguistische Informationen generieren** aus. Sie können die Textdarstellung bearbeiten, indem Sie Text im Textfeld **Textdarstellung** auswählen und die Befehle **Ausschneiden,** **Kopieren** und **Einfügen** im Menü **Bearbeiten** verwenden. Wenn Sie unsicher sind, welche Wörter die Sounddatei enthält, können Sie die Sounddatei wiedergeben, indem Sie im Menü **Bearbeiten** oder auf der Symbolleiste des Editors auf **Wiedergabe** klicken. Wenn der Editor weiterhin keine linguistischen Bezeichnungen erstellen kann, versuchen Sie erneut, die Sounddatei aufzuzeichnen. Eine Aufzeichnung mit schlechter Qualität, insbesondere bei übermäßigem Hintergrundrauschen, verringert wahrscheinlich die Wahrscheinlichkeit, angemessene linguistische Informationen zu generieren.

Sie können auch manuell eigene linguistische Informationen erstellen, indem Sie einen Teil der Audiodarstellung auswählen und im Menü **Bearbeiten** die Option **Phoneme** einfügen oder **Wort einfügen** auswählen. Diese Befehle sind auch verfügbar, wenn Sie mit der rechten Maustaste in die Auswahl klicken.

Um zu sehen, wie die linguistischen Informationen zum Synchronisieren von Zeichenanimationen mit dem Microsoft-Agent verwendet werden können, wählen Sie auf der Symbolleiste die Schaltfläche **Wiedergeben** aus, und der Editor gibt Ihre Sounddatei wieder, wobei basierend auf den generierten Bezeichnungsinformationen ein Beispielbild für den Mund animiert wird.

Sie können die Phoneme-Bezeichnungsanzeige so ändern, dass die IPA-Zuweisungen (Internationales phonetisches Alphabet) angezeigt werden, indem Sie im Menü **Bearbeiten** den Befehl **Phoneme Label Display** und dann den IPA-Befehl auswählen. Dadurch wird der Bytewert für die Phoneme angezeigt. Um zu den beschreibenden Namen zurückzukehren, wählen Sie erneut den Befehl **Phoneme Label Display (Phoneme-Bezeichnungsanzeige)** und dann **Name** aus.

### <a name="playing-a-sound-file"></a>Wiedergeben einer Sounddatei

Sie können Standard-Windows Sounddateien oder linguistisch erweiterte Sounddateien wiedergeben, indem Sie im Menü **Audio** oder auf der Symbolleiste des Editors den Befehl **Wiedergeben** auswählen. Mit den Befehlen **Anhalten** und **Beenden** können Sie die Wiedergabe der Sounddatei anhalten oder beenden. Während Sie die Datei wiedergeben, wird das Beispielbild animiert, um zu zeigen, wie die Informationen zur Synchronisierung von einem Microsoft-Agent-Zeichen verwendet werden können.

Sie können auch einen ausgewählten Teil einer Sounddatei wiedergeben, indem Sie eine Auswahl in der **Audiodarstellung** ziehen oder auf ein Wort oder eine Phoneme-Bezeichnung klicken und dann **Wiedergeben** auswählen. Sie können eine vorhandene Auswahl erweitern, indem Sie umschalten und klicken, oder umSCHALTTASTE drücken und an die neue Position in der **Audiodarstellung** ziehen.

### <a name="editing-linguistic-information"></a>Bearbeiten linguistischer Informationen

Sie können die linguistischen Informationen einer Datei auf verschiedene Weise bearbeiten. Beispielsweise können Sie die Begrenzung einer Wort- oder Phonemebezeichnung anpassen, indem Sie den Zeiger auf den Rand des Felds bewegen, das den Bereich der Bezeichnung definiert. Wenn sich der Zeiger auf den Begrenzungszeiger bewegt, ziehen Sie nach links oder rechts. Der Editor passt auch automatisch die benachbarte Wort- oder Phonemegrenze an.

![Screenshot: Änderungen an den linguistischen Informationen einer Datei](images/f4listadj.gif)

Durch das Anpassen der Begrenzung einer Phoneme-Bezeichnung ändert sich der Zeitpunkt einer Phoneme, wenn das Audio wiedergegeben wird. Bei Zeichen, die für die Verwendung mit dem Microsoft-Agent entwickelt wurden, kann das Ändern der Phoneme-Bezeichnungsgrenze den Zeitlichen Ablauf oder die Dauer eines Bilds ändern, das dieser Phoneme zugeordnet ist. Wenn Sie die Begrenzung einer Wortbezeichnung ändern, ändert sich der Zeitpunkt der Darstellung des Worts im Wortsprechblasen des Zeichens.

Sie können eine Phoneme-Zuweisung auch ersetzen, indem Sie die Phoneme-Bezeichnung auswählen und im Menü **Bearbeiten** die Option **Phoneme ersetzen** auswählen, oder klicken Sie mit der rechten Maustaste auf die Phoneme-Bezeichnung, und wählen Sie im Popupmenü **Phoneme ersetzen** aus. Der Editor zeigt das Dialogfeld **Phoneme ersetzen** an und hebt die aktuelle Phoneme-Zuweisung der Bezeichnung hervor. Sie können ein Ersatztelefon auswählen, indem Sie eines in der **IPA-Liste** oder einen anderen Eintrag in der **Liste Name** auswählen. Wenn für diesen Namen mehrere IPA-Übersetzungen verfügbar sind, wählen Sie ein Element in der **IPA-Liste** aus. Um eine IPA-Bezeichnung für eine Phoneme einzugeben, die möglicherweise nicht direkt in der Sprache enthalten ist, geben Sie den Hexadezimalwert oder mehrere Hexadezimalwerte ein, verkettet mit einem Pluszeichen (+). Nachdem Sie die Phoneme-Ersatzinformationen ausgewählt haben, wählen Sie **OK** aus, und der Editor ersetzt die ausgewählte Phoneme-Bezeichnung.

![Screenshot: Dialogfeld "Phoneme ersetzen" mit ausgewählter Bezeichnung "<SIL>"](images/f5listphone.gif)

Ebenso können Sie eine Wortbezeichnung ersetzen, indem Sie auf das Feld der Bezeichnung klicken und **Word ersetzen** auswählen, oder indem Sie mit der rechten Maustaste auf das Feld der Bezeichnung klicken und im Popupmenü **Word ersetzen** auswählen. Im Editor wird das Dialogfeld **Wort ersetzen** angezeigt. Geben Sie das Ersatzwort ein, und wählen Sie **OK** aus.

![Screenshot: Dialogfeld "Wort ersetzen" mit "Sound" im Textfeld "Word-Text"](images/f6listrep.gif)

Bei Zeichen, die für die Verwendung mit dem Microsoft-Agent entwickelt wurden, kann das Ersetzen einer Phoneme-Bezeichnung das beim Wiedergabe der Sounddatei angezeigte Zahnbild ändern. Durch das Ersetzen eines Worts wird der Text ersetzt, der im Wortsprechblasen des Zeichens angezeigt wird, wenn die [**Speak-Methode**](speak-method.md) aufgerufen wird.

Sie können auch eine neue Phonemebezeichnung oder ein neues Wort einfügen, indem Sie in der **Audiodarstellung** eine Auswahl treffen und im Menü **Bearbeiten** auf **Phoneme** einfügen oder **Wort einfügen** klicken oder mit der rechten Maustaste in die Auswahl klicken und die Befehle im Popupmenü auswählen. Diese Befehle rufen Dialogfelder auf, die den Dialogfeldern **Phoneme** ersetzen und **Wort ersetzen** ähneln, mit der Ausnahme, dass der Editor das neue Wort oder phoneme einfügt, anstatt die vorhandenen Informationen zu ersetzen.

Schließlich können Sie eine Phoneme oder ein Wort löschen, indem Sie die Bezeichnung auswählen und **Delete Phoneme (Phoneme löschen)** oder **Delete Word (Wort löschen)** auswählen. Dadurch werden die linguistischen Informationen aus der Datei entfernt.

 

 




