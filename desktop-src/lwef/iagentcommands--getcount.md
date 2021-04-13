---
title: Iagentcommands GetCount
description: Iagentcommands GetCount
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ece3e007b644b370ee721cef2d273fa50d43ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390140"
---
# <a name="iagentcommandsgetcount"></a><span data-ttu-id="8bc83-103">Iagentcommands:: GetCount</span><span class="sxs-lookup"><span data-stu-id="8bc83-103">IAgentCommands::GetCount</span></span>

<span data-ttu-id="8bc83-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="8bc83-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of count of commands
);                    
```

<span data-ttu-id="8bc83-105">Ruft die Anzahl der [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte [**in einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="8bc83-105">Retrieves the number of [**Command**](/windows/desktop/lwef/the-command-object) objects in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="8bc83-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8bc83-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8bc83-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span><span class="sxs-lookup"><span data-stu-id="8bc83-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span></span>
</dt> <dd>

<span data-ttu-id="8bc83-108">Adresse einer Variablen, die die Anzahl der [**Befehle**](/windows/desktop/lwef/the-command-object) in einer [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung empfängt.</span><span class="sxs-lookup"><span data-stu-id="8bc83-108">Address of a variable that receives the number of [**Commands**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="8bc83-109">*pdwCount* umfasst nur die Anzahl der [**Befehle**](/windows/desktop/lwef/the-command-object) , die Sie in der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung definieren.</span><span class="sxs-lookup"><span data-stu-id="8bc83-109">*pdwCount* includes only the number of [**Commands**](/windows/desktop/lwef/the-command-object) you define in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="8bc83-110">Server-oder andere Client Einträge sind nicht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8bc83-110">Server or other client entries are not included.</span></span>

 

 