---
title: Erstellen von linguistischen Informationen
description: Erstellen von linguistischen Informationen
ms.assetid: 903561f0-89dc-4297-8ea0-3fa150f2e6dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23fb99a5139e287e07e353791ce776b8a04dd8d2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104565488"
---
# <a name="generating-linguistic-information"></a>Erstellen von linguistischen Informationen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Nachdem Sie eine neue Audiodatei aufgezeichnet oder eine vorhandene Audiodatei geladen haben, können Sie phonetische und Wort Umbruch Informationen generieren, indem Sie Text eingeben, der Ihrer Audiodatei im Feld **Textdarstellung** entspricht. Wählen Sie dann im Menü **Bearbeiten** oder auf der Symbolleiste den Befehl **linguistische Informationen generieren** aus. Der Sound-Editor zeigt eine Fortschrittsmeldung an und beginnt mit der Verarbeitung der Audiodatei. Wenn das Erstellen von linguistischen Informationen abgeschlossen ist, wird eine Zuordnung von Word-und Phonem-Bezeichnungen für die Audiodatei in den Feldern im Feld **Audiodarstellung** angezeigt. Beachten Sie, dass der Befehl " **linguistische Informationen generieren** " deaktiviert bleibt, bis Sie eine Textdarstellung für die Audiodatei eingeben.

![Screenshot, der die Bereiche "Text Darstellung" und "Audiodarstellung" im Microsoft-Sound Bearbeitungs Tool für linguistische Informationen anzeigt.](images/f3listlabel.gif)

Wenn der Editor keinen akzeptablen Satz von Word-oder Phonem-Bezeichnungen erzeugt, wählen Sie den Befehl **linguistische Informationen generieren** erneut aus. Wenn der Editor keine linguistischen Informationen generiert, überprüfen Sie die Textdarstellung, um sicherzustellen, dass alle Wörter ordnungsgemäß geordnet und geschrieben sind und dass Sie keine unnötigen Leerzeichen um die Interpunktions Zeichen haben. Wählen Sie dann erneut den Befehl **linguistische Informationen generieren** aus. Sie können die Textdarstellung bearbeiten, indem Sie im Textfeld **Textdarstellung** den Text auswählen und die Befehle **Ausschneiden**, **Kopieren** und **Einfügen** im Menü **Bearbeiten** verwenden. Wenn Sie nicht sicher sind, welche Wörter in der Audiodatei enthalten sind, können Sie die Audiodatei wiedergeben, indem Sie im Menü **Bearbeiten** oder auf der Symbolleiste des Editors die Option wieder **Gabe** auswählen. Wenn der Editor weiterhin keine linguistischen Bezeichnungen erzeugt, versuchen Sie erneut, die Audiodatei aufzuzeichnen. Eine schlechte Qualitäts Aufzeichnung, insbesondere bei übermäßigem Hintergrundrauschen, verringert wahrscheinlich die Wahrscheinlichkeit, dass sinnvolle linguistische Informationen erzeugt werden.

Sie können Ihre eigenen linguistischen Informationen auch manuell erstellen, indem Sie einen Teil der Audiodarstellung auswählen und **Phoneme einfügen** oder **Word** aus dem Menü **Bearbeiten** auswählen. Diese Befehle sind auch verfügbar, wenn Sie mit der rechten Maustaste innerhalb der Auswahl klicken.

Um zu sehen, wie die linguistischen Informationen für die Animation der Tasten Synchronisierung mit dem Microsoft-Agent verwendet werden können, wählen Sie die **Wiedergabe** Schaltfläche auf der Symbolleiste aus, und der Editor gibt die Audiodatei wieder. dabei wird ein beispielmundbild basierend auf den generierten Bezeichnungs Informationen animiert.

Sie können die Anzeige der Phonem-Bezeichnung so ändern, dass die IPA-Zuweisungen (Internationale Phonetische Alphabet) angezeigt werden, indem Sie im Menü **Bearbeiten** auf den Befehl für die **Bezeichnung "Phonem Label Display** " klicken und dann den Befehl IPA Dadurch wird der Bytewert für das Phonem angezeigt. Wenn Sie zurück zu den beschreibenden Namen wechseln möchten, wählen Sie den Befehl **Phoneme Label Display** erneut aus, und wählen Sie dann **Name** aus.

### <a name="playing-a-sound-file"></a>Abspielen einer Sound Datei

Sie können standardmäßige Windows-Sounddateien oder linguistisch erweiterte Audiodateien wiedergeben, indem Sie den Befehl "wiedergeben" über das **Audiomenü** **oder die Symbol** Leiste des Editors auswählen. Mit **den Befehlen zum** **Anhalten und stoppen** können Sie die Audiodatei anhalten oder anhalten. Wenn Sie die Datei abspielen, wird das Beispiel-Mundbild animiert, um zu veranschaulichen, wie die Informationen zur Lip-Synchronisierung von einem Microsoft-agentzeichen verwendet werden können.

Sie können auch einen ausgewählten Teil einer Audiodatei wiedergeben, indem Sie eine Auswahl in der **Audiodarstellung** ziehen oder auf eine Wort-oder Phonem-Bezeichnung und dann auf **abspielen** klicken. Sie können eine vorhandene Auswahl erweitern, indem Sie UMSCHALTTASTE drücken und auf Verschieben klicken, oder indem Sie die UMSCHALTTASTE drücken und an die neue Position in der **Audiodarstellung** ziehen.

### <a name="editing-linguistic-information"></a>Bearbeiten von linguistischen Informationen

Sie können die linguistischen Informationen einer Datei auf verschiedene Weise bearbeiten. Beispielsweise können Sie die Begrenzung einer Wort-oder Phonem-Bezeichnung anpassen, indem Sie den Zeiger an den Rand des Felds bewegen, das den Bereich der Bezeichnung definiert. Wenn sich der Zeiger auf den Begrenzungs Verschiebungs Zeiger ändert, ziehen Sie nach links oder rechts. Der Editor passt auch automatisch die angrenzende Wort-oder Phonem-Grenze an.

![Screenshot, der Änderungen an den linguistischen Informationen einer Datei anzeigt.](images/f4listadj.gif)

Durch das Anpassen der Grenze einer Phonem-Bezeichnung wird die zeitliche Steuerung eines Phonem geändert, wenn die Audiowiedergabe durchlaufen wird. Für Zeichen, die für die Verwendung mit dem Microsoft-Agent entwickelt wurden, kann das Ändern der Phonem-Beschriftungs Grenze die zeitliche or-Dauer eines mundbilds ändern Durch Ändern der Grenze einer Wort Bezeichnung wird die zeitliche Darstellung des Worts in der Wort Sprechblase des Zeichens geändert.

Sie können eine Phonem-Zuweisung auch ersetzen, indem Sie die Bezeichnung Phonem auswählen und **Phonem** aus dem Menü **Bearbeiten** auswählen, oder klicken Sie mit der rechten Maustaste auf die Bezeichnung Phonem, und wählen Sie im Popupmenü die Option **Phonem ersetzen** aus. Der Editor zeigt das Dialogfeld **Phonem ersetzen** an und hebt die aktuelle Phonem-Zuweisung der Bezeichnung hervor. Sie können ein Ersatz Phonem auswählen, indem Sie eines in der **IPA** -Liste auswählen oder einen anderen Eintrag in der Liste **Name** auswählen. Wenn mehr als eine IPA-Übersetzung für diesen Namen verfügbar ist, wählen Sie ein Element in der **IPA** -Liste aus. Um eine IPA-Bezeichnung für ein Phonem einzugeben, das möglicherweise nicht direkt in der Sprache enthalten ist, geben Sie den Hexadezimalwert oder mehrere hexadezimale Werte ein, die mit einem Pluszeichen (+) verkettet sind. Nachdem Sie die Informationen zum Ersetzungs Phonem ausgewählt haben, wählen Sie **OK** aus, und der Editor ersetzt die ausgewählte Phonem-Bezeichnung.

![Screenshot mit dem Dialogfeld "Replace Phoneme", wobei "<SIL>" als beschreibende Bezeichnung ausgewählt ist.](images/f5listphone.gif)

Auf ähnliche Weise können Sie eine Wort Bezeichnung ersetzen, indem Sie auf das Feld "Bezeichnung" klicken und " **Wort ersetzen**" auswählen, oder indem Sie mit der rechten Maustaste auf das Feld "Bezeichnung" klicken und im Popupmenü **Wort ersetzen** auswählen. Der Editor zeigt das Dialogfeld **Wort ersetzen** an. Geben Sie das Ersatzwort ein, und wählen Sie **OK**.

![Screenshot, der das Dialogfeld "Wort ersetzen" mit "Sound" anzeigt, das in das Textfeld "Word Text" eingegeben wurde.](images/f6listrep.gif)

Für Zeichen, die für die Verwendung mit dem Microsoft-Agent entwickelt wurden, kann das Ersetzen einer Phonem-Bezeichnung das beim Wiedergabe der Audiodatei angezeigte Mundbild ändern Durch das Ersetzen eines Worts wird der Text ersetzt, der in der Wort [**Sprechblase**](speak-method.md) des Zeichens angezeigt wird, wenn die Sprech Methode aufgerufen wird.

Sie können auch eine neue Phonem-Bezeichnung oder Word einfügen, indem Sie eine Auswahl in der **Audiodarstellung** treffen und **Phonem einfügen** oder **Word** aus dem Menü **Bearbeiten** auswählen, oder indem Sie mit der rechten Maustaste auf die Auswahl klicken und die Befehle aus dem Popupmenü auswählen. Mit diesen Befehlen werden Dialogfelder ähnlich wie in den Dialogfeldern " **Phonem ersetzen** " und " **Wort ersetzen** " angezeigt, mit dem Unterschied, dass der Editor das neue Wort oder Phonem einfügt, anstatt die vorhandenen Informationen zu ersetzen.

Schließlich können Sie ein Phonem oder Word löschen, indem Sie die zugehörige Bezeichnung auswählen und **Phonem löschen** oder **Word löschen** auswählen. Dadurch werden die linguistischen Informationen aus der Datei entfernt.

 

 




