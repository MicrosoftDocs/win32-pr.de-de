---
title: Spracheingabe Unterstützung
description: Spracheingabe Unterstützung
ms.assetid: 4702b941-fcc9-4d00-aba2-eca624b6d417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ecb6f2ddfbbe10f8b892ce922cd466eca96890
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340908"
---
# <a name="speech-input-support"></a>Spracheingabe Unterstützung

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Zusätzlich zur Unterstützung der Maus-und Tastatur Interaktion bietet der Microsoft-Agent eine direkte Unterstützung für Spracheingaben. Da die Unterstützung von Spracheingaben durch den Microsoft-Agent auf Microsoft SAPI (Sprache Application Programming Interface) basiert, können Sie den Microsoft-Agent mit sprach Erkennungs Befehlen und Steuerungsmodulen verwenden, die die SAPI-erforderliche Unterstützung enthalten. Weitere Informationen zu den Anforderungen an die Sprach-Engine finden Sie [unter Support Anforderungen für sprach](requirements-for-speech-recognition-engines.md)Modul.

Microsoft stellt ein sprach Erkennungs Modul für die Befehls-und Steuerelemente bereit, das Sie mit dem Microsoft-Agent verwenden können. Weitere Informationen finden Sie unter [Sprach-Engine-Auswahl](speech-engine-selection.md).

Der Benutzer kann Spracheingaben initiieren, indem er den Push-to-Talk-lausch Hotkey drückt und hält. Wenn die Sprach-Engine in diesem Empfangsmodus den Anfang der gesprochenen Eingabe empfängt, hält Sie den Audiokanal geöffnet, bis das Ende der Ausdrucks Zeile erkannt wird. Beim Empfang von Eingaben wird die Audioausgabe jedoch nicht blockiert. Dies ermöglicht es dem Benutzer, mehrere Sprachbefehle auszugeben, während der Schlüssel gedrückt gehalten wird, und das Zeichen kann Antworten, wenn der Benutzer nicht spricht.

Der Modus für die Überwachung wird nach einem Timeout durch den Benutzer aufgehoben. Der Benutzer kann das Timeout für diesen Modus mithilfe der erweiterten Zeichen Optionen anpassen. Dieser Timeout kann nicht aus dem Client Anwendungscode festgelegt werden.

Wenn ein Zeichen versucht, zu sprechen, während der Benutzer spricht, schlägt die akustische Ausgabe des Zeichens fehl, obwohl Text weiterhin in der Wort Sprechblase angezeigt werden kann. Wenn das Zeichen über den Audiokanal verfügt, während die Abhör Taste gedrückt wird, überträgt der Server die Steuerung automatisch an den Benutzer zurück, nachdem der Text in der [**Sprech**](speak-method.md) Methode verarbeitet wurde. Ein optionaler MIDI-Ton wird wiedergegeben, um den Benutzer zu über den Einstieg zu sprechen. Dadurch kann der Benutzer auch dann Eingaben bereitstellen, wenn die Anwendung, die das Zeichen steuert, keine logischen Pausen in der Ausgabe bereitstellt.

Sie können auch die Methode " [**lauschen**](listen-method.md) " verwenden, um Spracheingaben zu initiieren. Durch Aufrufen dieser Methode wird die Spracherkennung für einen vordefinierten Zeitraum eingeschaltet. Wenn während dieses Intervalls keine Eingabe erfolgt, schaltet der Microsoft-Agent die sprach Erkennungs-Engine automatisch aus und gibt den Audiokanal frei. Dadurch wird verhindert, dass Eingaben für das Audiogerät blockiert werden, und der Prozessor Aufwand, der von der Spracherkennung verwendet wird, wird minimiert. Sie können die **Abhör Methode auch** verwenden, um die Spracheingabe zu deaktivieren. Beachten Sie jedoch, dass der Effekt möglicherweise nicht unmittelbar ist, da die Spracherkennungs-Engine asynchron arbeitet. Daher ist es möglich, auch dann ein [**Befehls**](command-event.md) Ereignis zu empfangen, wenn der Code " **lauschen** " aufgerufen hat, um die Spracheingabe zu deaktivieren.

Zur Unterstützung von Spracheingaben definieren Sie eine *Grammatik*, eine Reihe von Wörtern, die die sprach Erkennungs-Engine überwachen und mit der **sprach** Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung vergleichen soll. Sie können optionale und alternative Wörter und wiederholte Sequenzen in die Grammatik einschließen. Beachten Sie, dass der-Agent den lauschenden Hotkey erst aktiviert, wenn einer seiner Clients eine Sprach-Engine erfolgreich geladen hat oder eine **Stimme** für eines seiner **Befehls** Objekte verfasst hat.

Ob der Benutzer den abzurufenden Hotkey drückt, oder die Client Anwendung ruft die [**Abhör Methode auf**](listen-method.md) , um die Spracheingabe zu initiieren. die Spracherkennungs-Engine versucht, die Eingabe einer Äußerung an die Grammatik für die Befehle abzugleichen, die definiert wurden, und übergibt die Informationen zurück an den Server. Der Server benachrichtigt die Client Anwendung dann mithilfe des [**Befehls**](command-event.md) Ereignisses ([**iagentnotifysink:: Command**](iagentnotifysink--command.md)); Zurückgeben des [**UserInput**](/windows/desktop/lwef/iagentuserinput) -Objekts, das die Befehls-ID der besten Übereinstimmung und der nächsten zwei alternativen Übereinstimmungen (sofern vorhanden), ein Vertrauens Ergebnis und den übereinstimmenden Text für jede Übereinstimmung enthält.

Der Server benachrichtigt auch Ihre Client Anwendung, wenn Sie mit den Spracheingaben für einen der angegebenen Befehle übereinstimmt. Obwohl die Befehls-ID **null** ist, erhalten Sie immer noch das Vertrauens Ergebnis und den Text, der übereinstimmt. Im Empfangsmodus spielt der Server automatisch die Animation, die dem Empfangs Zustand des Zeichens **zugewiesen ist.** Wenn dann eine Äußerung tatsächlich erkannt wird, gibt der Server die Animation für den **hörzustand** des Zeichens wieder. Der Server verbleibt das Zeichen in einem aufmerksamen Zustand, bis die Äußerung beendet ist. Dies ermöglicht das entsprechende soziale Feedback, um dem Benutzer die Eingabe zu geben.

Wenn der Benutzer die Spracheingabe in erweiterten Zeichen Optionen deaktiviert, wird der lausch Ende Hotkey ebenfalls deaktiviert. Ebenso führt der Versuch, die [**Abhör Methode aufzurufen, wenn die sprach**](listen-method.md) Eingabe deaktiviert ist, dazu, dass die Methode fehlschlägt.

 

 