---
title: Iagentcharacter GetDescription
description: Iagentcharacter GetDescription
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423cd1f5c799cc1f0177f6d3d7922d5d14de1dbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388814"
---
# <a name="iagentcharactergetdescription"></a><span data-ttu-id="67c7c-103">Iagentcharacter:: GetDescription</span><span class="sxs-lookup"><span data-stu-id="67c7c-103">IAgentCharacter::GetDescription</span></span>

<span data-ttu-id="67c7c-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="67c7c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

<span data-ttu-id="67c7c-105">Ruft die Beschreibung des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="67c7c-105">Retrieves the description of the character.</span></span>

-   <span data-ttu-id="67c7c-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="67c7c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="67c7c-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszdescription*</span><span class="sxs-lookup"><span data-stu-id="67c7c-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="67c7c-108">Die Adresse eines BSTR-Werts, der den Wert der Beschreibung für das Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="67c7c-108">The address of a BSTR that receives the value of the description for the character.</span></span> <span data-ttu-id="67c7c-109">Die Beschreibung eines Zeichens wird bei der Kompilierung mit dem Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="67c7c-109">A character's description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="67c7c-110">Die Beschreibungs Einstellung ist optional und kann nicht für alle Zeichen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="67c7c-110">The description setting is optional and may not be supplied for all characters.</span></span>

</dd> </dl>

 

 




