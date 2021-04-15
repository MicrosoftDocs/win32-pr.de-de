---
title: Aufrufen von Funktionen
description: Aufrufen von Funktionen
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Windows Media Player Skins, Aufrufen von Funktionen in JScript
- Skins, Aufrufen von Funktionen in JScript
- Aufrufen von Funktionen in JScript
- JScript-Dateien für Skins, Aufrufen von Funktionen
- Windows Media Player Skins, scriptfile-Attribut in JScript
- Skins, scriptfile-Attribut in JScript
- Attribute, scriptfile in JScript
- scriptfile-Attribut in JScript
- JScript-Dateien für Skins, scriptfile-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516077"
---
# <a name="calling-functions"></a><span data-ttu-id="d1bc6-112">Aufrufen von Funktionen</span><span class="sxs-lookup"><span data-stu-id="d1bc6-112">Calling Functions</span></span>

<span data-ttu-id="d1bc6-113">Wenn Sie mehr als ein paar Codezeilen aufzurufen müssen, können Sie eine Skriptdatei mit dem **scriptfile** -Attribut des **View** -Elements laden und die Funktionen im Skript aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d1bc6-113">If you need to call more than a few lines of code, you can load a script file using the **scriptFile** attribute of the **VIEW** element, and call the functions in the script.</span></span> <span data-ttu-id="d1bc6-114">Sie können mehr als eine Datei pro Ansicht laden:</span><span class="sxs-lookup"><span data-stu-id="d1bc6-114">You can load more than one file per view:</span></span>


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



<span data-ttu-id="d1bc6-115">Nachdem die Skriptdateien geladen wurden, können Sie die darin enthaltenen Funktionen innerhalb Ihres Ansichts Abschnitts abrufen.</span><span class="sxs-lookup"><span data-stu-id="d1bc6-115">After the script files are loaded, you can call functions in them from inside your View section.</span></span> <span data-ttu-id="d1bc6-116">Wenn Sie z. b. eine Funktion mit dem Namen *MyFunction* aufrufen möchten, wenn auf etwas geklickt wird, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="d1bc6-116">For example, to call a function called *myfunction* when something is clicked, type the following:</span></span>


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> <span data-ttu-id="d1bc6-117">Wenn Sie mehr als eine Ansicht haben, sind nur die Funktionen in den in die aktuelle Ansicht geladenen Dateien für den XML-und JScript-Code verfügbar, der mit der aktuellen Ansicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1bc6-117">If you have more than one view, only the functions in files loaded into the current view are available to the XML and JScript code running with the current view.</span></span> <span data-ttu-id="d1bc6-118">Dateien, die in andere Sichten geladen wurden, befinden sich nicht im Gültigkeitsbereich der aktuellen Ansicht.</span><span class="sxs-lookup"><span data-stu-id="d1bc6-118">Files loaded in other views are not in scope with the current view.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d1bc6-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d1bc6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1bc6-120">**Verwenden von JScript**</span><span class="sxs-lookup"><span data-stu-id="d1bc6-120">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




