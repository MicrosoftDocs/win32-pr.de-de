---
title: Iagentcommand-GetId
description: Iagentcommand-GetId
ms.assetid: 4d8d8be7-7003-4ef3-abba-b5232267c993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1f5887123df19496c0610c53fe59a3f64961cd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390157"
---
# <a name="iagentcommandgetid"></a><span data-ttu-id="95a1f-103">Iagentcommand:: GetId</span><span class="sxs-lookup"><span data-stu-id="95a1f-103">IAgentCommand::GetID</span></span>

<span data-ttu-id="95a1f-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="95a1f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetID(
   long * pdwID  // address of ID for Command
);
```

<span data-ttu-id="95a1f-105">Ruft die ID für einen [**Befehl**](/windows/desktop/lwef/the-command-object)ab.</span><span class="sxs-lookup"><span data-stu-id="95a1f-105">Retrieves the ID for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="95a1f-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="95a1f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="95a1f-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwid*</span><span class="sxs-lookup"><span data-stu-id="95a1f-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span></span>
</dt> <dd>

<span data-ttu-id="95a1f-108">Die Adresse einer Variablen, die die ID eines [**Befehls**](/windows/desktop/lwef/the-command-object)empfängt.</span><span class="sxs-lookup"><span data-stu-id="95a1f-108">The address of a variable that receives the ID of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="95a1f-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="95a1f-109">See Also</span></span>

<span data-ttu-id="95a1f-110">[**Iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md), [**iagentcommands:: Remove**](iagentcommands--remove.md)</span><span class="sxs-lookup"><span data-stu-id="95a1f-110">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md)</span></span>


 

 