---
title: Iagentcharacter GetName
description: Iagentcharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33679577cfb5179a799ee61207f7ecd9b2be8a21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311603"
---
# <a name="iagentcharactergetname"></a><span data-ttu-id="eed1a-103">Iagentcharacter:: GetName</span><span class="sxs-lookup"><span data-stu-id="eed1a-103">IAgentCharacter::GetName</span></span>

<span data-ttu-id="eed1a-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="eed1a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

<span data-ttu-id="eed1a-105">Ruft den Namen des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="eed1a-105">Retrieves the name of the character.</span></span>

-   <span data-ttu-id="eed1a-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="eed1a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="eed1a-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszname*</span><span class="sxs-lookup"><span data-stu-id="eed1a-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span></span>
</dt> <dd>

<span data-ttu-id="eed1a-108">Die Adresse eines BSTR-Werts, der den Wert des Namens für das Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="eed1a-108">The address of a BSTR that receives the value of the name for the character.</span></span>

</dd> </dl>

<span data-ttu-id="eed1a-109">Der Standardname eines Zeichens wird bei der Kompilierung mit dem Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="eed1a-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="eed1a-110">Der Name eines Zeichens kann je nach Sprach-ID des Zeichens variieren.</span><span class="sxs-lookup"><span data-stu-id="eed1a-110">A character's name may vary based on the character's language ID.</span></span> <span data-ttu-id="eed1a-111">Zeichen können mit unterschiedlichen Namen für verschiedene Sprachen kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="eed1a-111">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="eed1a-112">Sie können auch den Namen des Zeichens mithilfe von " **iagentcharacter: SetName**;" festlegen. Dadurch wird jedoch der Name für alle aktuellen Clients des Zeichens geändert.</span><span class="sxs-lookup"><span data-stu-id="eed1a-112">You can also set the character's name using **IAgentCharacter:SetName**; however, this changes the name for all current clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="eed1a-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eed1a-113">See Also</span></span>

[<span data-ttu-id="eed1a-114">**Iagentcharacter:: SetName**</span><span class="sxs-lookup"><span data-stu-id="eed1a-114">**IAgentCharacter::SetName**</span></span>](iagentcharacter--setname.md)


 

 




