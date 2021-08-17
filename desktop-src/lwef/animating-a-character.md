---
title: Animieren eines Zeichens
description: Animieren eines Zeichens
ms.assetid: ed42de30-acac-41e8-bacb-4caaff254724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 937b970f1cdc9de9c973d298bbe963bfa70e4de3733869292e54d5d32742c722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976780"
---
# <a name="animating-a-character"></a>Animieren eines Zeichens

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Nachdem ein Zeichen geladen wurde, können Sie mehrere Microsoft Agent-Methoden zum Animieren des Zeichens verwenden. Die erste, die Sie verwenden, ist in der Regel die [**Show-Methode.**](show-method.md) **Show** macht den Rahmen des Zeichens sichtbar und gibt die Animation wieder, die dem Status Wird angezeigt **des Zeichens zugewiesen** ist.

Sobald der Rahmen des Zeichens sichtbar ist, können Sie die [**Play-Methode**](play-method.md) verwenden und den Namen einer Animation angeben, um diese Animation wieder zu spielen. Animationsnamen sind spezifisch für eine Zeichendefinition. Während eine Animation abspielt, ändert sich die Form ihres Fensters so, dass sie mit dem Bild im Frame übereinstimmen. Dies führt zu einem verschiebbaren Grafikbild *(Sprite),* das über dem Desktop und allen Fenstern angezeigt wird, oder *z-Reihenfolge.*

Wenn die Datei des Zeichens lokal gespeichert wird, können Sie einfach die [**Play-Methode**](play-method.md) aufrufen. In anderen Fällen, z. B. wenn Sie eine geladen haben. ACF-Zeichen von einem HTTP-Server verwenden, müssen Sie die [**Get-Methode**](get-method.md) (oder [**Prepare)-Methode**](/windows/desktop/lwef/iagentcharacter--prepare)verwenden, um zuerst die Animationsdaten abzurufen. Dadurch fordert der -Agent die Animationsdatei vom Server an und speichert sie im Puffer des Browsers auf dem lokalen Computer.

Mit [**der Speak-Methode**](speak-method.md) können Sie das Zu sprechende Zeichen programmieren und die Ausgabe automatisch synchronisieren. Weitere Informationen finden Sie im Abschnitt Ausgabe dieses Dokuments.

Sie können die [**MoveTo-Methode**](moveto-method.md) verwenden, um das Zeichen an einer neuen Position zu positionieren. Wenn Sie die **MoveTo-Methode** aufrufen, gibt Microsoft Agent automatisch die entsprechende Animation basierend auf der aktuellen Position des Zeichens wieder und verschiebt dann den Rahmen des Zeichens. Wenn Sie [**GestureAt**](gestureat-method.md)aufrufen, gibt Microsoft Agent die entsprechende Gesturierungsanimation auf der Grundlage der Position des Zeichens und des im Aufruf angegebenen Speicherorts wieder.

Um das Zeichen auszublenden, rufen Sie die [Hide-Methode](hide-method.md) auf. Dadurch wird automatisch das Zeichen abspielt, das dem **Hiding-Zustand** des Zeichens zugeordnet ist, und blendet dann den Rahmen des Zeichens aus. Sie können jedoch auch ein Zeichen ausblenden oder anzeigen, indem Sie die Visible-Eigenschaft des [**Zeichens**](visible-property.md) festlegen.

Microsoft Agent verarbeitet alle Animationsaufrufe oder *Anforderungen* asynchron. Dadurch kann der Code Ihrer Anwendung während der Verarbeitung der Anforderung weitere Ereignisse verarbeiten. Beispielsweise platzieren Aufrufe der [**Play-Methode**](play-method.md) die Animation in einer Warteschlange für das Zeichen, damit die Animationen sequenziell abgespielt werden können. Dies bedeutet jedoch nicht, dass Sie nicht davon ausgehen können, dass ein Aufruf anderer Funktionen notwendigerweise nach einer Animation ausgeführt wird, die im Code folgt. Beispielsweise wird in der Regel eine -Anweisung nach einem Aufruf von **Play** oder [**MoveTo**](moveto-method.md) ausgeführt, bevor die Animation abgeschlossen ist.

Sie können Ihren Code mit Animationen in der Warteschlange eines Zeichens synchronisieren, indem Sie einen Objektverweis auf die Animationsanforderung erstellen und nach dem Start oder Abschluss der Animation die Anforderungsereignisse überwachen, die der Server verwendet, um Clients über das Zeichen zu benachrichtigen. [](the-request-object.md) Wenn beispielsweise ein Meldungsfeld angezeigt werden soll, wenn das Zeichen eine Animation abgeschlossen hat, können Sie den Meldungsfeldaufruf in Die [**RequestComplete-Ereignisbehandlungsunterroutine**](requestcomplete-event.md) setzen und nach der jeweiligen Anforderungs-ID überprüfen.

Wenn ein Zeichen ausgeblendet ist, gibt der Server keine Animationen wieder. Allerdings wird die Animationsanforderung weiterhin in die Warteschlange gestellt und verarbeitet (die Animation wird abspielt) und ein Anforderungsstatus an den Client zurückübergibt. Im ausgeblendeten Zustand kann das Zeichen nicht eingabeaktiv werden. Wenn der Benutzer jedoch den Namen des Zeichens spricht (wenn die Spracheingabe aktiviert ist), zeigt der Server das Zeichen automatisch an.

Wenn Ihre Clientanwendung mehrere Zeichen gleichzeitig lädt, können Sie mit den Animationsdiensten von Microsoft Agent Zeichen unabhängig animieren oder die [**Methoden Wait,**](wait-method.md) [**Interrupt**](interrupt-method.md)oder [**Stop**](stop-method.md) verwenden, um ihre Animationen miteinander zu synchronisieren.

Microsoft Agent gibt auch andere Animationen automatisch für Sie wieder. Wenn sich der Zustand des Zeichens beispielsweise mehrere Sekunden lang nicht geändert hat, beginnt der -Agent mit der Wiedergabe von Animationen, die den **Idlinganimationen des Zeichens zugewiesen** sind. Wenn die Spracheingabe aktiviert ist, gibt der  -Agent die  Lauschen-Animationen des Zeichens und dann Höranimationen wieder, wenn eine Äußerung erkannt wird. Diese vom Server verwalteten Animationen werden als *Zustände* bezeichnet und beim Erstellen eines Zeichens definiert. Weitere Informationen finden Sie unter [Entwerfen von Zeichen für Microsoft Agent.](agent-states.md)

 

 