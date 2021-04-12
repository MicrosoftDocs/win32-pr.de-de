---
description: Alle Anwendungs Wörterbücher werden mithilfe des WordList-Objekts implementiert.
ms.assetid: 805788ec-1672-462a-b188-c680f56c2641
title: Grundlegendes zu Wortlisten, Erkennungs Kontext und Faktoiden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27f15d64f353b8702695b0067f13857427fc34e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216584"
---
# <a name="understanding-word-lists-recognizer-context-and-factoids"></a>Grundlegendes zu Wortlisten, Erkennungs Kontext und Faktoiden

Alle Anwendungs Wörterbücher werden mithilfe des [**WordList**](inkwordlist-class.md) -Objekts implementiert. Das [**erkenzercontext**](inkrecognizercontext-class.md) -Objekt verwaltet die Erkennung teilweise durch die [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -Eigenschaft dieses Objekts. Das **erkenzercontext** -Objekt übergibt die Wortliste an die Erkennung. Sie können ein Anwendungs Wörterbuch in jedem **Erkennungs Kontext** in der Anwendung aktivieren, indem Sie die **WordList** -Eigenschaft des **Erkennungs Kontext** -Objekts festlegen. Um die Wort Liste für die gesamte Anwendung verfügbar zu machen, müssen Sie die **WordList** -Eigenschaft jedes **Erkennungs Kontext** -Objekts in der Anwendung festlegen.

Auf der Erkennungs Ebene werden alle Wörterbücher außer dem System Wörterbuch als Wortlisten implementiert. Allerdings kann die Erkennung jeweils nur eine aktive Wort Liste haben. Dies bedeutet, dass Sie nicht sowohl ein Anwendungs Wörterbuch als auch das Benutzerwörterbuch gleichzeitig aktiv haben können. Auf der anderen Seite ist das System Wörterbuch immer verfügbar, es sei denn, es ist ein Faktoid festgelegt, das das System Wörterbuch deaktiviert.

Das Benutzerwörterbuch ist die Liste der Wörter, die der Benutzer seinem Tablet PC hinzugefügt hat. Wenn die [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -Eigenschaft des [**erkenzercontext**](inkrecognizercontext-class.md) nicht festgelegt ist, übergibt der **Erkennungs Kontext** das Benutzerwörterbuch als Wort Liste an die Erkennung. Wenn jedoch die **WordList** -Eigenschaft des **erkenzercontext** -Objekts festgelegt ist, wird die Wortliste anstelle des Benutzer Wörterbuchs an die Erkennung übermittelt.

> [!Note]  
> Die [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) -Eigenschaft des [**erkenzercontext**](inkrecognizercontext-class.md) -Objekts muss leer sein, bevor Sie die [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -Eigenschaft festlegen. Wenn die **Strokes** -Eigenschaft nicht leer ist, wird eine Ausnahme ausgelöst. Wörter sollten niemals zu einer Word-Liste hinzugefügt werden, nachdem Sie einem **erkenzercontext** -Objekt zugewiesen wurde.

 

Das Festlegen einer Faktoid für das [**erkennzercontext**](inkrecognizercontext-class.md) -Objekt wirkt sich auch darauf aus, wie Anwendungs Wörterbücher von der Erkennung verwendet werden. Die Faktoide, die sich auf das Verhalten von Wörterbüchern auswirken, sind:

-   **"WordList**
-   **System Dictionary**
-   **None**

Der wichtigste Faktoid für Anwendungs Wörterbücher ist die **WordList** -Faktoid. Das **WordList** -Faktoid Bias die Erkennungsfunktion, um nur die Wörter zurückzugeben, die in der Wort Liste gefunden werden. Diese Faktoid deaktiviert alle anderen Wörterbücher außer der Wort Liste. Wenn die **WordList** -Faktoid festgelegt ist und keine Word-Liste im Erkennungs Kontext angegeben ist, wird das Benutzerwörterbuch als Word-Liste verwendet.

Wenn Sie z. b. eine Anwendung für Flugzeugteile mit einem Feld entwerfen, das einen von zehn Namen spezieller Teile annimmt, können Sie eine Wort Liste erstellen, die nur diese Teilnamen enthält. Durch das Festlegen des Faktoid **WordList** für das Feld wird die Erkennung der in das Feld eingegebenen Wörter erheblich verbessert. Die Erkennung muss nicht zwischen Wörtern im System Wörterbuch und Wörtern in der Word-Liste wählen.

Das System **Dictionary** -Faktoid aktiviert nur das System Wörterbuch. Mit dem Faktoid **None** werden alle Wörterbücher deaktiviert. Diese beiden Faktoide werden verwendet, um die Erkennungsgenauigkeit in bestimmten Instanzen zu erhöhen. Da Sie jedoch Anwendungs Wörterbücher deaktivieren, werden Sie selten in Verbindung mit Anwendungs Wörterbüchern verwendet.

Weitere Informationen zur Auswirkung von Faktoids auf die Erkennung finden [Sie unter Verwenden von Kontext zur Verbesserung der Genauigkeit](using-context-to-improve-accuracy.md).

Weitere Informationen zu " **System Dictionary** " und " **None** " finden Sie [unter Unterstützte Faktoide aus Version 1](supported-factoids-from-version-1.md).

 

 



