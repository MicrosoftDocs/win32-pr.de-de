---
title: Deaktivieren von Strict
description: Wenn Sie die strikte Typüberprüfung deaktivieren möchten, definieren Sie den Symbolnamen "No \_ Strict". In Visual C/C++ können Sie diese Definition auch in der Befehlszeile oder in einem Makefile-Element angeben, indem Sie/DNO \_ Strict als Compileroption angeben.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bfdfef2aa7988576aa4c1e17f002639de98121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711976"
---
# <a name="disabling-strict"></a><span data-ttu-id="b3ba0-104">Deaktivieren von Strict</span><span class="sxs-lookup"><span data-stu-id="b3ba0-104">Disabling STRICT</span></span>

<span data-ttu-id="b3ba0-105">Wenn Sie die **strikte** Typüberprüfung deaktivieren möchten, definieren Sie den Symbolnamen " **No \_ Strict**".</span><span class="sxs-lookup"><span data-stu-id="b3ba0-105">To disable **STRICT** type checking, define the symbol name **NO\_STRICT**.</span></span> <span data-ttu-id="b3ba0-106">In Visual C/C++ können Sie diese Definition auch in der Befehlszeile oder in einem Makefile-Element angeben, indem Sie **/DNO \_ Strict** als Compileroption angeben.</span><span class="sxs-lookup"><span data-stu-id="b3ba0-106">In Visual C/C++, you can also specify this definition on the command line or in a makefile by specifying **/DNO\_STRICT** as a compiler option.</span></span>

<span data-ttu-id="b3ba0-107">Fügen Sie vor dem einschließen von Windows. h eine **\# define** -Anweisung ein, um **keine \_ strikte** Datei zu definieren:</span><span class="sxs-lookup"><span data-stu-id="b3ba0-107">To define **NO\_STRICT** on a file-by-file basis, insert a **\#define** statement before including Windows.h:</span></span>


```C++
#define NO_STRICT
#include <windows.h>
```



<span data-ttu-id="b3ba0-108">Um optimale Ergebnisse zu erzielen, sollten Sie auch die Warnstufe für Fehlermeldungen auf mindestens **/w3** festlegen.</span><span class="sxs-lookup"><span data-stu-id="b3ba0-108">For best results, you should also set the warning level for error messages to at least **/W3**.</span></span> <span data-ttu-id="b3ba0-109">Dies ist bei Anwendungen für Windows immer empfehlenswert, da eine Codierungs Praxis, die eine Warnung auslöst (z. b. das übergeben der falschen Anzahl von Parametern), in der Regel zur Laufzeit einen schwerwiegenden Fehler verursacht, wenn Sie nicht korrigiert wird.</span><span class="sxs-lookup"><span data-stu-id="b3ba0-109">This is always advisable with applications for Windows, because a coding practice that causes a warning (for example, passing the wrong number of parameters) usually causes a fatal error at run time if it is not corrected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3ba0-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3ba0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3ba0-111">Aktivieren von Strict</span><span class="sxs-lookup"><span data-stu-id="b3ba0-111">Enabling STRICT</span></span>](enabling-strict.md)
</dt> <dt>

[<span data-ttu-id="b3ba0-112">Strikte Konformität</span><span class="sxs-lookup"><span data-stu-id="b3ba0-112">STRICT Compliance</span></span>](strict-compliance.md)
</dt> </dl>

 

 




