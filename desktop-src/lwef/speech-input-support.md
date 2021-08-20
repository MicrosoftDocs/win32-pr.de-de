---
title: Spracheingabeunterstützung
description: Spracheingabeunterstützung
ms.assetid: 4702b941-fcc9-4d00-aba2-eca624b6d417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd777f5dca0df91a4660249b0cdda380f2f20c37ba5c1c38a04264bb871ab3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746251"
---
# <a name="speech-input-support"></a>Spracheingabeunterstützung

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Zusätzlich zur Unterstützung der Maus- und Tastaturinteraktion bietet der Microsoft-Agent direkte Unterstützung für Spracheingaben. Da die Unterstützung von Spracheingaben durch den Microsoft-Agent auf Microsoft SAPI (Speech Application Programming Interface) basiert, können Sie den Microsoft-Agent mit Spracherkennungsbefehls- und Steuerungs-Engines verwenden, die die sapi-erforderliche Unterstützung enthalten. Weitere Informationen zu den Anforderungen der Sprach-Engine finden Sie unter Supportanforderungen für die [Speech-Engine.](requirements-for-speech-recognition-engines.md)

Microsoft bietet eine Spracherkennungs-Engine für Befehle und Steuerungen, die Sie mit dem Microsoft-Agent verwenden können. Weitere Informationen finden Sie unter Auswahl der [Sprach-Engine.](speech-engine-selection.md)

Der Benutzer kann die Spracheingabe initiieren, indem er den Hotkey Push-to-Talk Listening gedrückt hält. Wenn die Sprach-Engine in diesem Lauschmodus den Anfang der gesprochenen Eingabe empfängt, bleibt der Audiokanal geöffnet, bis das Ende der Äußerung erkannt wird. Wenn sie jedoch keine Eingabe empfängt, wird die Audioausgabe nicht blockiert. Dadurch kann der Benutzer mehrere Sprachbefehle ausführen, während er den Schlüssel gedrückt hält, und das Zeichen kann reagieren, wenn der Benutzer nicht spricht.

Beim Lauschen-Modus kommt es zu einem Zeitsendlauf, sobald der Benutzer den Überwachungsschlüssel freigibt. Der Benutzer kann das Time out für diesen Modus mithilfe der erweiterten Zeichenoptionen anpassen. Sie können dieses Time out nicht im Clientanwendungscode festlegen.

Wenn ein Zeichen versucht, zu sprechen, während der Benutzer spricht, schlägt die akustische Ausgabe des Zeichens fehl, obwohl Text möglicherweise weiterhin in der Sprechblase angezeigt wird. Wenn das Zeichen den Audiokanal aufweist, während die Taste Lauschen gedrückt wird, überträgt der Server die Steuerung automatisch an den Benutzer zurück, nachdem der Text in der [**Speak-Methode**](speak-method.md) verarbeitet wurde. Ein optionaler TONE-Ton wird wiedergegeben, um den Benutzer zum Sprechen zu bringen. Dadurch kann der Benutzer Eingaben bereitstellen, auch wenn die Anwendung, die das Zeichen antreibt, in der Ausgabe keine logischen Pausen bereitstellen konnte.

Sie können auch die [**Listen-Methode**](listen-method.md) verwenden, um Spracheingaben zu initiieren. Durch Aufrufen dieser Methode wird die Spracherkennung für einen vordefinierten Zeitraum aktiviert. Wenn während dieses Intervalls keine Eingabe erfolgt, schaltet der Microsoft-Agent automatisch die Spracherkennungs-Engine aus und gibt den Audiokanal frei. Dadurch wird vermieden, dass Eingaben oder Ausgaben des Audiogeräts blockiert werden, und der Prozessoraufwand, den die Spracherkennung verwendet, wenn sie eingeschaltet ist, wird minimiert. Sie können auch die **Listen-Methode** verwenden, um die Spracheingabe zu deaktivieren. Beachten Sie jedoch, dass die Auswirkung möglicherweise nicht sofort auftritt, da die Spracherkennungs-Engine asynchron funktioniert. Daher ist es möglich, ein [**Command-Ereignis**](command-event.md) auch nach dem Code **Lauschen** zu empfangen, um die Spracheingabe zu deaktivieren.

Um die Spracheingabe zu unterstützen, definieren Sie eine *Grammatik*, eine Reihe von Wörtern, die die Spracherkennungs-Engine lauschen und abgleichen soll, als **Spracheinstellung** für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in Ihrer [**Commands-Sammlung.**](/windows/desktop/lwef/the-commands-collection-object) Sie können optionale und alternative Wörter und wiederholte Sequenzen in Ihre Grammatik einschließen. Beachten Sie, dass der -Agent den Lauschen-Hotkey erst aktiviert, wenn einer seiner Clients erfolgreich eine Sprach-Engine geladen oder eine **Stimme** für eines seiner **Command-Objekte** erstellt hat.

Unabhängig davon, ob der Benutzer den Hotkey Listening drückt oder Ihre Clientanwendung die [**Listen-Methode**](listen-method.md) aufruft, um die Spracheingabe zu initiieren, versucht die Spracherkennungs-Engine, die Eingabe einer Äußerung mit der Grammatik für die definierten Befehle abzugleichen, und übergibt die Informationen an den Server. Der Server benachrichtigt dann die Clientanwendung mithilfe des [**Command-Ereignisses**](command-event.md) ([**IAgentNotifySink::Command**](iagentnotifysink--command.md)); Übergeben des [**UserInput-Objekts,**](/windows/desktop/lwef/iagentuserinput) das die Befehls-ID der besten Übereinstimmung und der nächsten beiden alternativen Übereinstimmungen (falls vorhanden), eine Zuverlässigkeitsbewertung und den übereinstimmenden Text für jede Übereinstimmung enthält.

Der Server benachrichtigt Ihre Clientanwendung auch, wenn sie die Spracheingabe mit einem der angegebenen Befehle abgibt. Während die Befehls-ID **NULL** ist, erhalten Sie weiterhin die Zuverlässigkeitsbewertung und den übereinstimmende Text. Im Überwachungsmodus gibt der Server automatisch die Animation wieder, die dem **Überwachungszustand** des Zeichens zugewiesen ist. Wenn dann eine Äußerung tatsächlich erkannt wird, gibt der  Server die Hörzustandsanimation des Zeichens wieder. Der Server bewahrt das Zeichen in einem zustandsbehaltenen Zustand auf, bis die Äußerung beendet wurde. Dies bietet das entsprechende Feedback zu sozialen Netzwerken, um den Benutzer zur Eingabe zu bringen.

Wenn der Benutzer die Spracheingabe in erweiterten Zeichenoptionen deaktiviert, wird auch der Hotkey Lauschen deaktiviert. Ebenso führt der Versuch, die [**Listen-Methode**](listen-method.md) aufzurufen, wenn die Spracheingabe deaktiviert ist, dazu, dass die Methode fehlschlägt.

 

 