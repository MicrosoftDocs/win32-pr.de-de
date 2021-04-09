---
description: Der folgende Code entlädt ein Symbol Modul, auf das von der baseofdll-Modul Adresse mithilfe von SymUnloadModule64 verwiesen wird.
ms.assetid: f185ae64-1de9-4139-acd5-7c3a108e1eba
title: Entladen eines Symbol Moduls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b6fad0177fce36865e90dadf04bd563130789
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861139"
---
# <a name="unloading-a-symbol-module"></a><span data-ttu-id="38892-103">Entladen eines Symbol Moduls</span><span class="sxs-lookup"><span data-stu-id="38892-103">Unloading a Symbol Module</span></span>

<span data-ttu-id="38892-104">Der folgende Code entlädt ein Symbol Modul, auf das von der baseofdll-Modul Adresse mithilfe von [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="38892-104">The following code unloads a symbol module referred to by the BaseOfDll module address using [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule).</span></span>


```C++
if (SymUnloadModule64(hProcess, BaseOfDll))
{
    // SymUnloadModule64 returned success
}
else
{
    // SymUnloadModule64 failed
    DWORD error = GetLastError();
    printf("SymUnloadModule64 returned error : %d\n", error);
}
```



## <a name="related-topics"></a><span data-ttu-id="38892-105">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="38892-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38892-106">Laden eines Symbol Moduls</span><span class="sxs-lookup"><span data-stu-id="38892-106">Loading a Symbol Module</span></span>](loading-a-symbol-module.md)
</dt> </dl>

 

 



