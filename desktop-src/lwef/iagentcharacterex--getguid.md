---
title: Iagentcharakteriex GetGuid
description: Iagentcharakteriex GetGuid
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e0e14d0931774bf6ab5e1c8599bbebaadd0ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947919"
---
# <a name="iagentcharacterexgetguid"></a><span data-ttu-id="f680d-103">Iagentcharakteriex:: GetGuid</span><span class="sxs-lookup"><span data-stu-id="f680d-103">IAgentCharacterEx::GetGUID</span></span>

<span data-ttu-id="f680d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="f680d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

<span data-ttu-id="f680d-105">Ruft die eindeutige ID für das Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="f680d-105">Retrieves the unique ID for the character.</span></span>

-   <span data-ttu-id="f680d-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f680d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f680d-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszguid*</span><span class="sxs-lookup"><span data-stu-id="f680d-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="f680d-108">Adresse eines BSTR, der die ID für das Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="f680d-108">Address of a BSTR that receives the ID for the character.</span></span>

</dd> </dl>

<span data-ttu-id="f680d-109">Die-Eigenschaft gibt eine Zeichen folgen Darstellung der GUID (formatiert mit geschweiften Klammern und Bindestrichen) zurück, die der Server zum eindeutigen Identifizieren des Zeichens verwendet.</span><span class="sxs-lookup"><span data-stu-id="f680d-109">The property returns a string representation of the GUID (formatted with braces and dashes) that the server uses to uniquely identify the character.</span></span> <span data-ttu-id="f680d-110">Eine Zeichen Kennung wird festgelegt, wenn Sie mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="f680d-110">A character identifier is set when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="f680d-111">Die Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f680d-111">The property is read-only.</span></span>

 

 




