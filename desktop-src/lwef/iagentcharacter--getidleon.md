---
title: Iagentcharacter getidleon
description: Iagentcharacter getidleon
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdaf3ea460a76549112741ac77f83e10ec37cd9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714592"
---
# <a name="iagentcharactergetidleon"></a><span data-ttu-id="a18d2-103">Iagentcharacter:: getidleon</span><span class="sxs-lookup"><span data-stu-id="a18d2-103">IAgentCharacter::GetIdleOn</span></span>

<span data-ttu-id="a18d2-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="a18d2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

<span data-ttu-id="a18d2-105">Gibt den automatischen Leerlauf Verarbeitungs Status für ein Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="a18d2-105">Indicates the automatic idle processing state for a character.</span></span>

-   <span data-ttu-id="a18d2-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a18d2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a18d2-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbon*</span><span class="sxs-lookup"><span data-stu-id="a18d2-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="a18d2-108">Die Adresse einer Variablen, die " **true** " empfängt, wenn der Microsoft-Agent-Server für ein Zeichen automatisch **idlinger** -Zustands Animationen abspielt, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="a18d2-108">Address of a variable that receives **True** if the Microsoft Agent server automatically plays **Idling** state animations for a character and **False** if not.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="a18d2-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a18d2-109">See Also</span></span>

[<span data-ttu-id="a18d2-110">**Iagentcharacter::/tidleon**</span><span class="sxs-lookup"><span data-stu-id="a18d2-110">**IAgentCharacter::SetIdleOn**</span></span>](iagentcharacter--setidleon.md)


 

 




