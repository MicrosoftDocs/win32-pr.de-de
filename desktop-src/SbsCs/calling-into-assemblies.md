---
description: Beim Aufrufen der entryPoints einer Assembly empfiehlt es sich, den gleichen Aktivierungs Kontext zu verwenden, der beim Suchen nach der Assembly aktiv war.
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: Aufrufen in Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4742b19ea47e03fac5f7d0318248ea167182e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959972"
---
# <a name="calling-into-assemblies"></a><span data-ttu-id="d4523-103">Aufrufen in Assemblys</span><span class="sxs-lookup"><span data-stu-id="d4523-103">Calling Into Assemblies</span></span>

<span data-ttu-id="d4523-104">Beim Aufrufen der entryPoints einer Assembly empfiehlt es sich, den gleichen Aktivierungs Kontext zu verwenden, der beim Suchen nach der Assembly aktiv war.</span><span class="sxs-lookup"><span data-stu-id="d4523-104">When calling into the entrypoints of an assembly, it is recommended that you use the same activation context that was active when searching for the assembly.</span></span> <span data-ttu-id="d4523-105">Stellen Sie mindestens sicher, dass die Komponente, die die Assembly lädt, nicht versehentlich den Aktivierungs Kontext erhält, den Ihre Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4523-105">At minimum, ensure that the component loading the assembly does not accidentally get the activation context your application is using.</span></span> <span data-ttu-id="d4523-106">Das Verlust von Aktivierungs Kontext über dll-Grenzen hinweg kann zu unerwarteten Abhängigkeiten führen.</span><span class="sxs-lookup"><span data-stu-id="d4523-106">Leaking activation context across DLL boundaries can lead to unexpected dependencies.</span></span> <span data-ttu-id="d4523-107">Dies ist kein Problem, wenn Ihre Anwendung die Isolations \_ Funktion \_ aktiviert kompiliert, da in diesem Fall standardmäßig kein Aktivierungs Kontext aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="d4523-107">This is not a problem if your application compiles ISOLATION\_AWARE\_ENABLED because in that case no activation context is active by default.</span></span> <span data-ttu-id="d4523-108">Wenn die Kompilierung nicht mit aktivierter Isolations Funktion \_ \_ aktiviert ist, sollten Sie den **null** -Aktivierungs Kontext oder den gleichen Aktivierungs Kontext aktivieren, der zum Laden der Assembly verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d4523-108">If you do not compile with ISOLATION\_AWARE\_ENABLED defined, you should activate the **NULL** activation context or the same activation context that was used to load the assembly.</span></span>

<span data-ttu-id="d4523-109">Im folgenden Beispiel wird sichergestellt, dass die gehostete dll in einem Kontext ausgeführt wird, den Sie erkennt:</span><span class="sxs-lookup"><span data-stu-id="d4523-109">The following example ensures that the hosted DLL runs in a context that it recognizes:</span></span>

``` syntax
ULONG_PTR ulpCookie;
ActivateActCtx(hTheActCtxForMyDll, &ulpCookie);
__try 
{
        MyDllIsolatedFunction();
    myDllIsolatedComInterface->Funct();
}
__finally 
{
    DeactivateActCtx(0, ulpCookie);
}
```

 

 



