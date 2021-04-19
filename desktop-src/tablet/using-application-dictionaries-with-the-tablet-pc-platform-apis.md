---
description: Wenn Sie ein Anwendungs Wörterbuch mit der Tablet PC-API verwenden möchten, müssen Sie zuerst eine Datei mit der Liste der Wörter für das Anwendungs Wörterbuch erstellen.
ms.assetid: 6abadad1-262b-4536-8846-1c06226dc18a
title: Verwenden von Anwendungs Wörterbüchern mit den Tablet PC Platform-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fc0e444ad2213d945c0210d07c72f9540ae16be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353057"
---
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a>Verwenden von Anwendungs Wörterbüchern mit den Tablet PC Platform-APIs

Wenn Sie ein Anwendungs Wörterbuch mit der Tablet PC-API verwenden möchten, müssen Sie zuerst eine Datei mit der Liste der Wörter für das Anwendungs Wörterbuch erstellen.

Die einfachste Lösung hierfür ist die Verwendung einer Textdatei, die eine Liste der Wörter enthält. Wenn die Anwendung geladen wird, liest Sie die Textdatei und erstellt ein [**WordList**](inkwordlist-class.md) -Objekt aus der Liste der Wörter in der Datei. Legen Sie für jeden mit dem Anwendungs Wörterbuch verknüpften [**Erkennungs Kontext**](inkrecognizercontext-class.md) die [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -Eigenschaft des **erkenzercontext** -Objekts auf die Word-Liste in der Textdatei fest.

Im folgenden Beispiel wird veranschaulicht, wie ein [**WordList**](inkwordlist-class.md) -Objekt aus einer [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) -Auflistung erstellt wird. In diesem Beispiel wird davon ausgegangen, dass Sie die Liste der Wörter bereits von der Festplatte geladen und eine StringCollection-Sammlung mit diesen Wörtern erstellt haben.


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
> Die [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) -Eigenschaft des [**erkenzercontext**](inkrecognizercontext-class.md) -Objekts muss leer sein, bevor Sie die [**WordList**](inkwordlist-class.md) -Eigenschaft festlegen. Wenn die [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Eigenschaft nicht leer ist, wird eine Ausnahme ausgelöst. Außerdem sollten Wörter niemals zu einer Word-Liste hinzugefügt werden, nachdem Sie einem **erkenzercontext** -Objekt zugewiesen wurde. Wörter, die der Word-Liste hinzugefügt werden, nachdem Sie dem **erkenzercontext** -Objekt zugewiesen wurde, werden in der Erkennung nicht aktualisiert. Zum Aktualisieren der Word-Liste müssen Sie das **WordList** -Objekt der [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -Eigenschaft des **erkenzercontext** -Objekts neu zuweisen.

 

Kombinieren Sie für maximale Erkennungsgenauigkeit die Faktoide mit Ihrem Anwendungs Wörterbuch in einer vorteilhaften Beziehung. Weitere Informationen über die Beziehung zwischen Faktoiden und Anwendungs Wörterbüchern finden Sie Untergrund Legendes zu [Wortlisten, Erkennungs Kontext und Faktoiden](understanding-wordlists--the-recognizercontext--and-factoids.md).

Ein Beispiel für die Verwendung von Anwendungs Wörterbüchern mit dem [InkEdit](inkedit-control-reference.md) -Steuerelement finden [Sie unter Verwenden eines Anwendungs Wörterbuchs mit InkEdit](using-an-application-dictionary-with-inkedit.md).

 

 
