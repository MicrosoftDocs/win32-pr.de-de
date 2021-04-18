---
description: Mithilfe von Kategorien können Sie Ereignisse organisieren, damit Sie von Ereignisanzeige gefiltert werden können. Jede Ereignis Quelle kann eigene nummerierte Kategorien und die Text Zeichenfolgen definieren, denen Sie zugeordnet sind.
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: Ereigniskategorien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd84a095754bd51499edf5a21ebea0ade042d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347827"
---
# <a name="event-categories"></a><span data-ttu-id="f51fc-104">Ereigniskategorien</span><span class="sxs-lookup"><span data-stu-id="f51fc-104">Event Categories</span></span>

<span data-ttu-id="f51fc-105">Mithilfe von Kategorien können Sie Ereignisse organisieren, damit Sie von Ereignisanzeige gefiltert werden können.</span><span class="sxs-lookup"><span data-stu-id="f51fc-105">Categories help you organize events so Event Viewer can filter them.</span></span> <span data-ttu-id="f51fc-106">Jede [Ereignis Quelle](event-sources.md) kann eigene nummerierte Kategorien und die Text Zeichenfolgen definieren, denen Sie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f51fc-106">Each [event source](event-sources.md) can define its own numbered categories and the text strings to which they are mapped.</span></span>

<span data-ttu-id="f51fc-107">Die Kategorien müssen nacheinander nummeriert werden, beginnend mit der Zahl 1.</span><span class="sxs-lookup"><span data-stu-id="f51fc-107">The categories must be numbered consecutively, beginning with the number 1.</span></span> <span data-ttu-id="f51fc-108">Die Kategorien selbst werden in einer Nachrichtendatei definiert.</span><span class="sxs-lookup"><span data-stu-id="f51fc-108">The categories themselves are defined in a message file.</span></span> <span data-ttu-id="f51fc-109">Verwenden Sie z. b. die folgende Syntax, um drei Ereignis Kategorien zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="f51fc-109">For example, use the following syntax to declare three event categories.</span></span> <span data-ttu-id="f51fc-110">In Ereignisanzeige werden die Ereignisse, in denen diese Kategorien verwendet werden, Kategorie 1, Kategorie 2 oder Kategorie 3 in der Spalte **Category** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f51fc-110">In Event Viewer, the events that use these categories will have Category 1, Category 2, or Category 3 displayed in the **Category** column.</span></span>

``` syntax
MessageId=0x1
SymbolicName=CATEGORY_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CATEGORY_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CATEGORY_3
Language=English
Category 3
.
```

<span data-ttu-id="f51fc-111">Kategorien können in einer separaten Nachrichtendatei oder in einer Datei gespeichert werden, die Nachrichten anderer Typen enthält.</span><span class="sxs-lookup"><span data-stu-id="f51fc-111">Categories can be stored in a separate message file, or in a file that contains messages of other types.</span></span> <span data-ttu-id="f51fc-112">Wenn Sie eine einzelne Nachrichtendatei erstellen, achten Sie darauf, dass es sich bei den Kategorien um die ersten Nachrichten in der Datei handelt.</span><span class="sxs-lookup"><span data-stu-id="f51fc-112">If you create a single message file, be sure that the categories are the first messages in the file.</span></span> <span data-ttu-id="f51fc-113">Weitere Informationen zum Erstellen und Verwenden von Nachrichten Dateien finden Sie unter [Nachrichten Dateien](message-files.md).</span><span class="sxs-lookup"><span data-stu-id="f51fc-113">For more information on creating and using message files, see [Message Files](message-files.md).</span></span>

<span data-ttu-id="f51fc-114">Die Gesamtanzahl der Kategorien wird im **CategoryCount** -Wert für die Ereignis Quelle gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f51fc-114">The total number of categories is stored in the **CategoryCount** value for the event source.</span></span>

 

 



