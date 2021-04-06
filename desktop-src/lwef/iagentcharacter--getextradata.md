---
title: Iagentcharacter GetExtraData
description: Iagentcharacter GetExtraData
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100822"
---
# <a name="iagentcharactergetextradata"></a><span data-ttu-id="3fc0a-103">Iagentcharacter:: GetExtraData</span><span class="sxs-lookup"><span data-stu-id="3fc0a-103">IAgentCharacter::GetExtraData</span></span>

<span data-ttu-id="3fc0a-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3fc0a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

<span data-ttu-id="3fc0a-105">Ruft zusätzliche Daten ab, die als Teil des Zeichens gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-105">Retrieves additional data stored as part of the character.</span></span>

-   <span data-ttu-id="3fc0a-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3fc0a-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszextradata*</span><span class="sxs-lookup"><span data-stu-id="3fc0a-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*</span></span>
</dt> <dd>

<span data-ttu-id="3fc0a-108">Die Adresse eines BSTR-Werts, der den Wert der zusätzlichen Daten für das Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-108">The address of a BSTR that receives the value of the additional data for the character.</span></span> <span data-ttu-id="3fc0a-109">Die zusätzlichen Daten eines Zeichens werden bei der Kompilierung mit dem Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-109">A character's additional data is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="3fc0a-110">Ein Zeichen Entwickler kann diese Zeichenfolge bereitstellen, indem er den bearbeitet. ACD-Datei für ein Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-110">A character developer can supply this string by editing the .ACD file for a character.</span></span> <span data-ttu-id="3fc0a-111">Die Einstellung ist optional und kann nicht für alle Zeichen angegeben werden, und die Daten können zur Laufzeit nicht definiert oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-111">The setting is optional and may not be supplied for all characters, nor can the data be defined or changed at run time.</span></span> <span data-ttu-id="3fc0a-112">Außerdem wird die Bedeutung der bereitgestellten Daten vom Zeichen Entwickler definiert.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-112">In addition, the meaning of the data supplied is defined by the character developer.</span></span>

</dd> </dl>

 

 




