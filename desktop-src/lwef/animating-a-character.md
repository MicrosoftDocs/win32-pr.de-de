---
title: Animieren eines Zeichens
description: Animieren eines Zeichens
ms.assetid: ed42de30-acac-41e8-bacb-4caaff254724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed47b30a9bcfcdb5e305b87ced5f02526ae0056
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038867"
---
# <a name="animating-a-character"></a>Animieren eines Zeichens

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Sobald ein Zeichen geladen ist, können Sie mehrere der Methoden des Microsoft-Agents verwenden, um das Zeichen zu animieren. Der erste, den Sie verwenden, ist in der Regel die [**Show**](show-method.md) -Methode. **Show** macht den Frame des Zeichens sichtbar und gibt die Animation wieder, die dem **anzeigen** Zustand des Zeichens zugewiesen ist.

Sobald der Rahmen des Zeichens sichtbar ist, können Sie die [**Play**](play-method.md) -Methode verwenden, um den Namen einer Animation anzugeben, um diese Animation wiederzugeben. Animations Namen sind spezifisch für eine Zeichen Definition. Wenn eine Animation abgespielt wird, ändert sich die Form des Fensters so, dass Sie dem Bild im Frame entspricht. Dies führt zu einem verschiebbaren Grafik Bild oder *Sprite*, das auf dem Desktop und allen Fenstern oder der *z-Reihenfolge* angezeigt wird.

Wenn die Datei des Zeichens lokal gespeichert wird, können Sie einfach die [**Play**](play-method.md) -Methode aufzurufen. In anderen Fällen, z. b. Wenn Sie eine geladen haben. ACF-Zeichen von einem HTTP-Server. Sie müssen die [**Get**](get-method.md) (oder [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare))-Methode verwenden, um zuerst die Animationsdaten abzurufen. Dies bewirkt, dass der-Agent die Animations Datei vom Server anfordert und Sie im Puffer des Browsers auf dem lokalen Computer speichert.

Die [**Sprech**](speak-method.md) Methode ermöglicht es Ihnen, das Zeichen zu programmieren und die Ausgabe automatisch zu synchronisieren. Weitere Informationen finden Sie im Abschnitt Ausgabe dieses Dokuments.

Sie können die Methode " [**muveto**](moveto-method.md) " verwenden, um das Zeichen an einem neuen Speicherort zu positionieren. Wenn Sie die " **muveto** "-Methode anrufen, wird die entsprechende Animation von Microsoft-Agent automatisch auf der Grundlage des aktuellen Speicher Orts der Zeichen wiedergegeben, und der Rahmen des Zeichens wird verschoben. Wenn Sie " [**gestureat**](gestureat-method.md)" aufrufen, gibt der Microsoft-Agent entsprechend der Position des Zeichens und der Position, die im-Befehl angegeben ist, die passende gesturinganimation wieder.

Um das Zeichen auszublenden, müssen Sie die [Hide](hide-method.md) -Methode aufzurufen. Dadurch wird automatisch das Zeichen wiedergegeben, das dem **Ausblenden des Zeichens** zugeordnet ist, und anschließend wird der Rahmen des Zeichens ausgeblendet. Sie können jedoch auch ein Zeichen ausblenden oder anzeigen, indem Sie die [**Visible**](visible-property.md) -Eigenschaft des Zeichens festlegen.

Der Microsoft-Agent verarbeitet alle Animations Aufrufe oder *Anforderungen* asynchron. Dadurch kann der Code Ihrer Anwendung weiterhin andere Ereignisse verarbeiten, während die Anforderung verarbeitet wird. Beispielsweise platzieren Aufrufe der [**Play**](play-method.md) -Methode die Animation in einer Warteschlange für das Zeichen, damit die Animationen sequenziell wiedergegeben werden können. Dies bedeutet jedoch, dass Sie nicht davon ausgehen können, dass ein aufrufanderer Funktionen nach einer Animation im Code ausgeführt wird. In der Regel wird z. b. eine-Anweisung, die nach einem " **Play** "-oder " [**muveto**](moveto-method.md) "-Befehl ausgeführt wird, vor

Sie können Ihren Code mit Animationen in der Warteschlange eines Zeichens synchronisieren, indem Sie einen Objekt Verweis auf die Animations Anforderung erstellen und beim Starten oder Abschließen der Animation die [Anforderungs](the-request-object.md) Ereignisse überwachen, die der Server verwendet, um Clients über das Zeichen zu benachrichtigen. Wenn Sie z. b. möchten, dass ein Meldungs Feld angezeigt wird, wenn das Zeichen eine Animation beendet, können Sie den Meldungs Feld aufrufen in Ihre [**requestcomplete**](requestcomplete-event.md) -Ereignis Behandlungs Unterroutine einfügen und auf die jeweilige Anforderungs-ID überprüfen.

Wenn ein Zeichen ausgeblendet wird, gibt der Server keine Animationen wieder. Es wird jedoch immer noch die Animations Anforderung in die Warteschlange eingereiht und verarbeitet (die Animation wird wiedergegeben) und der Anforderungs Status an den Client zurückgegeben. Im ausgeblendeten Zustand kann das Zeichen nicht als Eingabe aktiv werden. Wenn der Benutzer jedoch den Namen des Zeichens spricht (wenn die Spracheingabe aktiviert ist), zeigt der Server automatisch das Zeichen an.

Wenn die Client Anwendung mehrere Zeichen gleichzeitig lädt, können Sie mit den Animations Diensten von Microsoft Agent Zeichen unabhängig animieren oder die Methoden zum [**warten**](wait-method.md), unter [**brechen**](interrupt-method.md)oder [**Beenden**](stop-method.md) verwenden, um Ihre Animation untereinander zu synchronisieren.

Der Microsoft-Agent spielt auch andere Animationen automatisch für Sie. Wenn der Zustand des Zeichens z. b. mehrere Sekunden lang nicht geändert wurde, beginnt der-Agent mit der Wiedergabe von Animationen, die den **idck** -Animationen des Zeichens zugewiesen sind. Entsprechend gibt der-Agent bei aktivierter Spracheingabe die **Abhör** Animationen des Zeichens an und **hört** dann Animationen ab, wenn eine Äußerung erkannt wird. Diese vom Server verwalteten Animationen werden als *Zustände* bezeichnet und beim Erstellen eines Zeichens definiert. Weitere Informationen finden Sie unter [Entwerfen von Zeichen für den Microsoft-Agent](agent-states.md).

 

 