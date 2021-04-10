---
title: Definieren von Namen für den Präprozessor
description: Sie können die bedingte Kompilierung in einem Skript angeben, abhängig davon, ob ein Name in der RC-Befehlszeile mit der/d-Option oder in der Datei oder einer Includedatei mit der \ define-Direktive definiert ist.
ms.assetid: bc72911e-2aca-46a4-b6c1-60cc8ed7d82f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64b339959ace5a70d83fa8ee8beb615f1bc5ce4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309427"
---
# <a name="defining-names-for-the-preprocessor"></a><span data-ttu-id="1d8be-103">Definieren von Namen für den Präprozessor</span><span class="sxs-lookup"><span data-stu-id="1d8be-103">Defining Names for the Preprocessor</span></span>

<span data-ttu-id="1d8be-104">Sie können die bedingte Kompilierung in einem Skript angeben, abhängig davon, ob ein Name in der RC-Befehlszeile mit der **/d** -Option oder in der Datei oder einer Includedatei mit der [**\# define**](-define.md) -Direktive definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1d8be-104">You can specify conditional compilation in a script, based on whether a name is defined on the RC command line with the **/d** option, or in the file or an include file with the [**\#define**](-define.md) directive.</span></span>

<span data-ttu-id="1d8be-105">Angenommen, die Anwendung verfügt über ein Popup Menü, das nur mit Debugversionen der Anwendung angezeigt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="1d8be-105">For example, suppose your application has a pop-up menu that should appear only with debugging versions of the application.</span></span> <span data-ttu-id="1d8be-106">Wenn Sie die Anwendung für die normale Verwendung kompilieren, ist das Menü nicht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1d8be-106">When you compile the application for normal use, the menu is not included.</span></span> <span data-ttu-id="1d8be-107">Das folgende Beispiel zeigt die-Anweisungen, die der Ressourcen Definitionsdatei hinzugefügt werden können, um ein debugmenü zu definieren:</span><span class="sxs-lookup"><span data-stu-id="1d8be-107">The following example shows the statements that can be added to the resource-definition file to define a Debug menu:</span></span>

``` syntax
#include <windows.h>

MainMenu MENU
{
    //. . .
#ifdef DEBUG
    POPUP "&Debug"
    {
        MENUITEM "&Memory usage", ID_MEMORY
        MENUITEM "&Walk data heap", ID_WALK_HEAP
    }
#endif
}
```

<span data-ttu-id="1d8be-108">Wenn Sie Ressourcen für eine Debugversion der Anwendung kompilieren, können Sie das Menü Debuggen mit dem folgenden Befehl einschließen:</span><span class="sxs-lookup"><span data-stu-id="1d8be-108">When compiling resources for a debugging version of the application, you could include the Debug menu by using the following command:</span></span>

<span data-ttu-id="1d8be-109">**RC-d Debuggen MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="1d8be-109">**rc -d DEBUG myapp.rc**</span></span>

<span data-ttu-id="1d8be-110">Verwenden Sie den folgenden Befehl, um Ressourcen für eine normale Version der Anwendung zu kompilieren? eine, die das Menü "Debuggen" nicht enthält?</span><span class="sxs-lookup"><span data-stu-id="1d8be-110">To compile resources for a normal version of the application?one that does not include the Debug menu?you could use the following command:</span></span>

<span data-ttu-id="1d8be-111">**RC MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="1d8be-111">**rc myapp.rc**</span></span>

 

 




