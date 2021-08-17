---
description: Beim Aufrufen der Einstiegpunkte einer Assembly wird empfohlen, den gleichen Aktivierungskontext zu verwenden, der beim Suchen nach der Assembly aktiv war.
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: Aufrufen von Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6f785c9d68aa0dbf4bec24927d9f2a1443aed1fb7fe65ec9244616fce8feec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142423"
---
# <a name="calling-into-assemblies"></a>Aufrufen von Assemblys

Beim Aufrufen der Einstiegpunkte einer Assembly wird empfohlen, den gleichen Aktivierungskontext zu verwenden, der beim Suchen nach der Assembly aktiv war. Stellen Sie mindestens sicher, dass die Komponente, die die Assembly lädt, nicht versehentlich den Aktivierungskontext bekommt, den Ihre Anwendung verwendet. Ein Überlauf des Aktivierungskontexts über DLL-Grenzen hinweg kann zu unerwarteten Abhängigkeiten führen. Dies ist kein Problem, wenn Ihre Anwendung ISOLATION AWARE ENABLED kompiliert, da in diesem Fall standardmäßig kein \_ \_ Aktivierungskontext aktiv ist. Wenn Sie nicht mit der definitionen ISOLATION AWARE ENABLED kompilieren, sollten Sie den NULL-Aktivierungskontext oder denselben Aktivierungskontext aktivieren, der zum \_ Laden der Assembly verwendet \_ wurde. 

Im folgenden Beispiel wird sichergestellt, dass die gehostete DLL in einem von ihr erkannten Kontext ausgeführt wird:

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

 

 



