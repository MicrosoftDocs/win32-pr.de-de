---
title: Vordefinierte Makros
description: RC unterstützt die vordefinierten ANSI C-Makros ( \_ \_ Date \_ \_ , \_ \_ file \_ \_ , \_ \_ line \_ \_ , \_ \_ stdc \_ \_ , \_ \_ time \_ \_ , \_ \_ timestamp \_ \_ ) nicht. Daher können Sie diese Makros nicht in Header Dateien einschließen, die Sie in Ihr Ressourcen Skript einschließen.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 351674bc86ab56753bb49dba9e65edd97a7b1a04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100683"
---
# <a name="predefined-macros"></a><span data-ttu-id="f8de6-104">Vordefinierte Makros</span><span class="sxs-lookup"><span data-stu-id="f8de6-104">Predefined Macros</span></span>

<span data-ttu-id="f8de6-105">RC unterstützt die vordefinierten ANSI C-Makros (**\_ \_ Date \_ \_**, **\_ \_ file \_ \_**, **\_ \_ line \_ \_**, **\_ \_ \_ stdc \_**, **\_ \_ time \_ , \_** **\_ \_ timestamp \_ ) \_** nicht.</span><span class="sxs-lookup"><span data-stu-id="f8de6-105">RC does not support the ANSI C predefined macros (**\_\_DATE\_\_**, **\_\_FILE\_\_**, **\_\_LINE\_\_**, **\_\_STDC\_\_**, **\_\_TIME\_\_**, **\_\_TIMESTAMP\_\_**).</span></span> <span data-ttu-id="f8de6-106">Daher können Sie diese Makros nicht in Header Dateien einschließen, die Sie in Ihr Ressourcen Skript einschließen.</span><span class="sxs-lookup"><span data-stu-id="f8de6-106">Therefore, you cannot include these macros in header files that you will include in your resource script.</span></span>

<span data-ttu-id="f8de6-107">RC definiert RC- \_ aufgerufen, sodass Sie Teile der Header Dateien bedingt kompilieren können, je nachdem, ob der Compiler der C-Compiler oder der RC-Compiler ist.</span><span class="sxs-lookup"><span data-stu-id="f8de6-107">RC does define RC\_INVOKED, which enables you conditionally compile portions of your header files, depending on whether the compiler is your C compiler or the RC compiler.</span></span> <span data-ttu-id="f8de6-108">Dies ist wichtig, da der RC-Compiler nur eine Teilmenge der Anweisungen unterstützt, die von einem C-Compiler unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f8de6-108">This is important because the RC compiler supports only a subset of the statements a C compiler would support.</span></span>

<span data-ttu-id="f8de6-109">Um den Code bedingt mit dem RC-Compiler zu kompilieren, müssen Sie den Code umschließen, den RC nicht mit den Aufrufen \# \_ und **\# EndIf** von ifndef RC kompilieren kann</span><span class="sxs-lookup"><span data-stu-id="f8de6-109">To conditionally compile your code with the RC compiler, surround code that RC cannot compile with \#ifndef RC\_INVOKED and **\#endif**.</span></span>

<span data-ttu-id="f8de6-110">Das folgende Beispiel stammt aus den SDK-Beispielen.</span><span class="sxs-lookup"><span data-stu-id="f8de6-110">The following example is taken from the SDK samples.</span></span> <span data-ttu-id="f8de6-111">Es wird veranschaulicht, wie eine Header Datei erstellt wird, die bedingt kompiliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f8de6-111">It demonstrates how to create a header file that can be compiled conditionally.</span></span>

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




