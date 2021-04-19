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
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a><span data-ttu-id="17af1-103">Verwenden von Anwendungs Wörterbüchern mit den Tablet PC Platform-APIs</span><span class="sxs-lookup"><span data-stu-id="17af1-103">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>

<span data-ttu-id="17af1-104">Wenn Sie ein Anwendungs Wörterbuch mit der Tablet PC-API verwenden möchten, müssen Sie zuerst eine Datei mit der Liste der Wörter für das Anwendungs Wörterbuch erstellen.</span><span class="sxs-lookup"><span data-stu-id="17af1-104">To use an application dictionary with the Tablet PC API, you must first create a file with the list of words for your application dictionary.</span></span>

<span data-ttu-id="17af1-105">Die einfachste Lösung hierfür ist die Verwendung einer Textdatei, die eine Liste der Wörter enthält.</span><span class="sxs-lookup"><span data-stu-id="17af1-105">The easiest solution for this is to use a text file that contains a list of the words.</span></span> <span data-ttu-id="17af1-106">Wenn die Anwendung geladen wird, liest Sie die Textdatei und erstellt ein [**WordList**](inkwordlist-class.md) -Objekt aus der Liste der Wörter in der Datei.</span><span class="sxs-lookup"><span data-stu-id="17af1-106">When your application loads, it reads the text file and creates a [**WordList**](inkwordlist-class.md) object from the list of words in the file.</span></span> <span data-ttu-id="17af1-107">Legen Sie für jeden mit dem Anwendungs Wörterbuch verknüpften [**Erkennungs Kontext**](inkrecognizercontext-class.md) die [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -Eigenschaft des **erkenzercontext** -Objekts auf die Word-Liste in der Textdatei fest.</span><span class="sxs-lookup"><span data-stu-id="17af1-107">For each [**RecognizerContext**](inkrecognizercontext-class.md) associated with the application dictionary, set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object to the word list in the text file.</span></span>

<span data-ttu-id="17af1-108">Im folgenden Beispiel wird veranschaulicht, wie ein [**WordList**](inkwordlist-class.md) -Objekt aus einer [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) -Auflistung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="17af1-108">The following example illustrates how to create a [**WordList**](inkwordlist-class.md) object from a [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) collection.</span></span> <span data-ttu-id="17af1-109">In diesem Beispiel wird davon ausgegangen, dass Sie die Liste der Wörter bereits von der Festplatte geladen und eine StringCollection-Sammlung mit diesen Wörtern erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="17af1-109">This example assumes that you have already loaded the list of words from disk and created a StringCollection collection from these words.</span></span>


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
> <span data-ttu-id="17af1-110">Die [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) -Eigenschaft des [**erkenzercontext**](inkrecognizercontext-class.md) -Objekts muss leer sein, bevor Sie die [**WordList**](inkwordlist-class.md) -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="17af1-110">The [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object must be empty before you set the [**WordList**](inkwordlist-class.md) property.</span></span> <span data-ttu-id="17af1-111">Wenn die [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Eigenschaft nicht leer ist, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="17af1-111">If the [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) property is not empty, an exception is thrown.</span></span> <span data-ttu-id="17af1-112">Außerdem sollten Wörter niemals zu einer Word-Liste hinzugefügt werden, nachdem Sie einem **erkenzercontext** -Objekt zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="17af1-112">In addition, words should never be added to a word list after it has been assigned to a **RecognizerContext** object.</span></span> <span data-ttu-id="17af1-113">Wörter, die der Word-Liste hinzugefügt werden, nachdem Sie dem **erkenzercontext** -Objekt zugewiesen wurde, werden in der Erkennung nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="17af1-113">Words that are added to the word list after it is assigned to the **RecognizerContext** object are not updated in the recognizer.</span></span> <span data-ttu-id="17af1-114">Zum Aktualisieren der Word-Liste müssen Sie das **WordList** -Objekt der [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -Eigenschaft des **erkenzercontext** -Objekts neu zuweisen.</span><span class="sxs-lookup"><span data-stu-id="17af1-114">To update the word list you must reassign the **WordList** object to the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object.</span></span>

 

<span data-ttu-id="17af1-115">Kombinieren Sie für maximale Erkennungsgenauigkeit die Faktoide mit Ihrem Anwendungs Wörterbuch in einer vorteilhaften Beziehung.</span><span class="sxs-lookup"><span data-stu-id="17af1-115">For maximum recognition accuracy, combine factoids with your application dictionary in an advantageous relationship.</span></span> <span data-ttu-id="17af1-116">Weitere Informationen über die Beziehung zwischen Faktoiden und Anwendungs Wörterbüchern finden Sie Untergrund Legendes zu [Wortlisten, Erkennungs Kontext und Faktoiden](understanding-wordlists--the-recognizercontext--and-factoids.md).</span><span class="sxs-lookup"><span data-stu-id="17af1-116">For more information about the relationship between factoids and application dictionaries, see [Understanding Word Lists, Recognizer Context, and Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).</span></span>

<span data-ttu-id="17af1-117">Ein Beispiel für die Verwendung von Anwendungs Wörterbüchern mit dem [InkEdit](inkedit-control-reference.md) -Steuerelement finden [Sie unter Verwenden eines Anwendungs Wörterbuchs mit InkEdit](using-an-application-dictionary-with-inkedit.md).</span><span class="sxs-lookup"><span data-stu-id="17af1-117">For an example of using application dictionaries with the [InkEdit](inkedit-control-reference.md) control, see [Using an Application Dictionary with InkEdit](using-an-application-dictionary-with-inkedit.md).</span></span>

 

 
