---
description: Der folgende Code entlädt ein Symbolmodul, auf das von der BaseOfDll-Moduladresse verwiesen wird, mithilfe von SymUnloadModule64.
ms.assetid: f185ae64-1de9-4139-acd5-7c3a108e1eba
title: Entladen eines Symbolmoduls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0da437fe0ce188e3559280d2bc347f3b976aba52adbf8e4a0306e4e469747435
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929280"
---
# <a name="unloading-a-symbol-module"></a>Entladen eines Symbolmoduls

Der folgende Code entlädt mithilfe von [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)ein Symbolmodul, auf das von der Moduladresse BaseOfDll verwiesen wird.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Laden eines Symbolmoduls](loading-a-symbol-module.md)
</dt> </dl>

 

 



