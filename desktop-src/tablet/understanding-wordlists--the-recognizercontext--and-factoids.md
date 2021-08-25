---
description: Alle Anwendungswörterbücher werden mithilfe des WordList-Objekts implementiert.
ms.assetid: 805788ec-1672-462a-b188-c680f56c2641
title: Grundlegendes zu Wortlisten, Kontext der Wiedererkennung und Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60fbfc7a3a3099a1146307637d20e777cca416789a61f5dd034f9d86911f1a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842810"
---
# <a name="understanding-word-lists-recognizer-context-and-factoids"></a>Grundlegendes zu Wortlisten, Kontext der Wiedererkennung und Factoids

Alle Anwendungswörterbücher werden mithilfe des [**WordList-Objekts**](inkwordlist-class.md) implementiert. Das [**RecognizerContext-Objekt**](inkrecognizercontext-class.md) verwaltet die Erkennung, teilweise über die [**WordList-Eigenschaft dieses**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) Objekts. Das **RecognizerContext-Objekt** übergibt die Wortliste an die Erkennende. Sie können ein Anwendungswörterbuch in einem **beliebigen RecognizerContext** in Ihrer Anwendung aktivieren, indem Sie die **WordList-Eigenschaft** des **RecognizerContext-Objekts** festlegen. Um die Wortliste für die gesamte Anwendung verfügbar zu machen, müssen Sie die **WordList-Eigenschaft** jedes **RecognizerContext-Objekts** in der Anwendung festlegen.

Auf der Recognizer-Ebene werden alle Wörterbücher mit Ausnahme des Systemwörterbuchs als Wortlisten implementiert. Die -Erkannte kann jedoch nur eine aktive Wortliste gleichzeitig haben. Dies bedeutet, dass sie nicht gleichzeitig sowohl ein Anwendungswörterbuch als auch das Benutzerwörterbuch aktiv haben können. Andererseits ist das Systemwörterbuch immer verfügbar, es sei denn, es wird ein Factoid festgelegt, das das Systemwörterbuch deaktiviert.

Das Benutzerwörterbuch ist die Liste der Wörter, die der Benutzer seinem Tablet-PC hinzugefügt hat. Wenn die [**WordList-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) von [**RecognizerContext**](inkrecognizercontext-class.md) nicht festgelegt ist, übergibt **recognizerContext** das Benutzerwörterbuch als Wortliste an die Recognizer-Klasse. Wenn jedoch die **WordList-Eigenschaft** des **RecognizerContext-Objekts** festgelegt ist, wird die Wortliste an die Erkennende statt an das Benutzerwörterbuch übergeben.

> [!Note]  
> Die [**Strokes-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) des [**RecognizerContext-Objekts**](inkrecognizercontext-class.md) muss leer sein, bevor Sie die [**WordList-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) festlegen. Wenn die **Strokes-Eigenschaft** nicht leer ist, wird eine Ausnahme ausgelöst. Wörter sollten niemals einer Wortliste hinzugefügt werden, nachdem sie einem **RecognizerContext-Objekt zugewiesen** wurde.

 

Das Festlegen eines Factoids für das [**RecognizerContext-Objekt**](inkrecognizercontext-class.md) wirkt sich auch darauf aus, wie Anwendungswörterbücher von der Recognizer verwendet werden. Die Factoids, die sich auf das Verhalten von Wörterbüchern auswirken, sind:

-   **Wordlist**
-   **SystemDictionary**
-   **Keine**

Das bei weitem nützlichste Faktenoid für Anwendungswörterbücher ist das **WordList-Factoid.** Das **WordList-Factoid** verzerrt die Erkannten in Richtung der Rückgabe von nur Wörtern, die in der Wortliste gefunden wurden. Dieses Factoid deaktiviert alle anderen Wörterbücher mit Ausnahme der Wortliste. Wenn das **WordList-Factoid** festgelegt ist und keine Wortliste im Kontext der Erkannten angegeben wird, wird das Benutzerwörterbuch als Wortliste verwendet.

Wenn Sie beispielsweise eine Anwendung für Flugzeugteile mit einem Feld entwerfen, das einen von zehn Namen spezialisierter Teile akzeptiert, können Sie eine Wortliste erstellen, die nur diese Teilenamen enthält. Das Festlegen **des WordList-Factoids** für das Feld verbessert die Erkennung der in dieses Feld eingegebenen Wörter erheblich. Die Erkannten müssen nicht zwischen Wörtern im Systemwörterbuch und Wörtern in der Wortliste wählen.

Das **SystemDictionary-Factoid** aktiviert nur das Systemwörterbuch. Das **Faktenoid** None deaktiviert alle Wörterbücher. Diese beiden Factoide werden verwendet, um die Erkennungsgenauigkeit in bestimmten Instanzen zu erhöhen. Da sie Jedoch Anwendungswörterbücher deaktivieren, werden sie selten in Verbindung mit Anwendungswörterbüchern verwendet.

Weitere Informationen dazu, wie factoids die Erkennung beeinflussen, finden Sie unter [Using Context to Improve Accuracy](using-context-to-improve-accuracy.md).

Weitere Informationen zu den **Fakten "SystemDictionary"** und **"None"** finden Sie unter [Unterstützte Factoids aus Version 1.](supported-factoids-from-version-1.md)

 

 



