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
# <a name="calling-into-assemblies"></a>Aufrufen in Assemblys

Beim Aufrufen der entryPoints einer Assembly empfiehlt es sich, den gleichen Aktivierungs Kontext zu verwenden, der beim Suchen nach der Assembly aktiv war. Stellen Sie mindestens sicher, dass die Komponente, die die Assembly lädt, nicht versehentlich den Aktivierungs Kontext erhält, den Ihre Anwendung verwendet. Das Verlust von Aktivierungs Kontext über dll-Grenzen hinweg kann zu unerwarteten Abhängigkeiten führen. Dies ist kein Problem, wenn Ihre Anwendung die Isolations \_ Funktion \_ aktiviert kompiliert, da in diesem Fall standardmäßig kein Aktivierungs Kontext aktiv ist. Wenn die Kompilierung nicht mit aktivierter Isolations Funktion \_ \_ aktiviert ist, sollten Sie den **null** -Aktivierungs Kontext oder den gleichen Aktivierungs Kontext aktivieren, der zum Laden der Assembly verwendet wurde.

Im folgenden Beispiel wird sichergestellt, dass die gehostete dll in einem Kontext ausgeführt wird, den Sie erkennt:

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

 

 



