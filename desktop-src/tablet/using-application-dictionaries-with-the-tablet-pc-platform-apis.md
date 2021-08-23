---
description: Um ein Anwendungswörterbuch mit der Tablet PC-API zu verwenden, müssen Sie zunächst eine Datei mit der Liste der Wörter für Ihr Anwendungswörterbuch erstellen.
ms.assetid: 6abadad1-262b-4536-8846-1c06226dc18a
title: Verwenden von Anwendungswörterbüchern mit den Plattform-APIs für Tablet-PCs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c30fec5539a9b1f4efb0ca89a53568becff2368942d069149106a4032676d50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091305"
---
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a>Verwenden von Anwendungswörterbüchern mit den Plattform-APIs für Tablet-PCs

Um ein Anwendungswörterbuch mit der Tablet PC-API zu verwenden, müssen Sie zunächst eine Datei mit der Liste der Wörter für Ihr Anwendungswörterbuch erstellen.

Die einfachste Lösung dafür ist die Verwendung einer Textdatei, die eine Liste der Wörter enthält. Wenn Ihre Anwendung geladen wird, liest sie die Textdatei und erstellt ein [**WordList-Objekt**](inkwordlist-class.md) aus der Liste der Wörter in der Datei. Legen Sie [**für jeden RecognizerContext,**](inkrecognizercontext-class.md) der dem Anwendungswörterbuch zugeordnet ist, die [**WordList-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) des **RecognizerContext-Objekts** auf die Wortliste in der Textdatei fest.

Im folgenden Beispiel wird veranschaulicht, wie ein [**WordList-Objekt**](inkwordlist-class.md) aus einer [StringCollection-Auflistung erstellt](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) wird. In diesem Beispiel wird davon ausgegangen, dass Sie bereits die Liste der Wörter vom Datenträger geladen und eine StringCollection-Sammlung aus diesen Wörtern erstellt haben.


```C++
using System.Collections.Specialized;
using Microsoft.Ink;
//...
RecognizerContext theRecognizerContext;
StringCollection theUserDictionary;
//... 
// Initialize theRecognizerContext and theUserDictionary objects here.
//...
WordList theUserWordList = new WordList();
foreach (string s in theUserDictionary)
{
    theUserWordList.Add(s);
}
theRecognizerContext.WordList = theUserWordList;
```



> [!Note]  
> Die [**Strokes-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) des [**RecognizerContext-Objekts**](inkrecognizercontext-class.md) muss leer sein, bevor Sie die [**WordList-Eigenschaft**](inkwordlist-class.md) festlegen. Wenn die [**Strokes-Eigenschaft**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) nicht leer ist, wird eine Ausnahme ausgelöst. Darüber hinaus sollten Wörter niemals einer Wortliste hinzugefügt werden, nachdem sie einem **RecognizerContext-Objekt zugewiesen** wurde. Wörter, die der Wortliste hinzugefügt werden, nachdem sie dem **RecognizerContext-Objekt** zugewiesen wurden, werden in der Recognizer-Klasse nicht aktualisiert. Um die Wortliste zu aktualisieren, müssen Sie das **WordList-Objekt** der [**WordList-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) des **RecognizerContext-Objekts neu** zuweisen.

 

Um eine maximale Erkennungsgenauigkeit zu erhalten, kombinieren Sie Factoids mit Ihrem Anwendungswörterbuch in einer vorteilhaften Beziehung. Weitere Informationen zur Beziehung zwischen Factoiden und Anwendungswörterbüchern finden Sie unter [Understanding Word Lists, Recognizer Context, and Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).

Ein Beispiel für die Verwendung von Anwendungswörterbüchern mit dem [InkEdit-Steuerelement](inkedit-control-reference.md) finden Sie unter Verwenden eines [Anwendungswörterbuchs mit InkEdit](using-an-application-dictionary-with-inkedit.md).

 

 
