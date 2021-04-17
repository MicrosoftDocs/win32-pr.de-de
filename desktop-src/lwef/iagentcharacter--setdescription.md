---
title: Iagentcharacter setDescription
description: Iagentcharacter setDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9815e5c0e01537c7db2b400326f86da37af003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388806"
---
# <a name="iagentcharactersetdescription"></a><span data-ttu-id="fe847-103">Iagentcharacter:: setDescription</span><span class="sxs-lookup"><span data-stu-id="fe847-103">IAgentCharacter::SetDescription</span></span>

<span data-ttu-id="fe847-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="fe847-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

<span data-ttu-id="fe847-105">Legt die Beschreibung des Zeichens fest.</span><span class="sxs-lookup"><span data-stu-id="fe847-105">Sets the description of the character.</span></span>

-   <span data-ttu-id="fe847-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="fe847-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="fe847-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszdescription*</span><span class="sxs-lookup"><span data-stu-id="fe847-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="fe847-108">Ein BSTR, der die Beschreibung für das Zeichen festlegt.</span><span class="sxs-lookup"><span data-stu-id="fe847-108">A BSTR that sets the description for the character.</span></span> <span data-ttu-id="fe847-109">Die Standardbeschreibung eines Zeichens wird bei der Kompilierung mit dem Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="fe847-109">A character's default description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="fe847-110">Die Beschreibungs Einstellung ist optional und kann nicht für alle Zeichen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fe847-110">The description setting is optional and may not be supplied for all characters.</span></span> <span data-ttu-id="fe847-111">Sie können die Beschreibung des Zeichens mithilfe von **iagentcharacter:: setDescription**; ändern. Dieser Wert ist jedoch nicht persistent (wird permanent gespeichert).</span><span class="sxs-lookup"><span data-stu-id="fe847-111">You can change the character's description using **IAgentCharacter::setDescription**; however, this value is not persistent (stored permanently).</span></span> <span data-ttu-id="fe847-112">Die Zeichen Beschreibung wird immer wieder auf die Standardeinstellung festgelegt, wenn das Zeichen zuerst von einem Client geladen wird.</span><span class="sxs-lookup"><span data-stu-id="fe847-112">The character's description reverts to its default setting whenever the character is first loaded by a client.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="fe847-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fe847-113">See Also</span></span>

[<span data-ttu-id="fe847-114">**Iagentcharacter:: GetDescription**</span><span class="sxs-lookup"><span data-stu-id="fe847-114">**IAgentCharacter::GetDescription**</span></span>](iagentcharacter--getdescription.md)


 

 




