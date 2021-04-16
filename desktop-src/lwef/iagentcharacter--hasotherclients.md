---
title: Iagentcharacter hasotherclients
description: Iagentcharacter hasotherclients
ms.assetid: ee74fa9b-2842-43ac-8493-bc69b480581e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32380e31e63278f4181cfd854ecaada1775a4fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516118"
---
# <a name="iagentcharacterhasotherclients"></a><span data-ttu-id="0292d-103">Iagentcharacter:: hasotherclients</span><span class="sxs-lookup"><span data-stu-id="0292d-103">IAgentCharacter::HasOtherClients</span></span>

<span data-ttu-id="0292d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0292d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT HasOtherClients(
   long * plNumOtherClients  // address of variable for number of clients 
);                           // for character 
```

<span data-ttu-id="0292d-105">Ruft ab, ob ein Zeichen über andere Clients verfügt.</span><span class="sxs-lookup"><span data-stu-id="0292d-105">Retrieves whether a character has other clients.</span></span>

-   <span data-ttu-id="0292d-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0292d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0292d-107"><span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plnumotherclients*</span><span class="sxs-lookup"><span data-stu-id="0292d-107"><span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plNumOtherClients*</span></span>
</dt> <dd>

<span data-ttu-id="0292d-108">Adresse einer Variablen, die die Anzahl anderer verbundener Clients für das Zeichen empfängt (Gesamtzahl der Clients abzüglich des Clients).</span><span class="sxs-lookup"><span data-stu-id="0292d-108">Address of a variable that receives the number of other connected clients for the character (total number of clients minus your client).</span></span>

</dd> </dl>

 

 




