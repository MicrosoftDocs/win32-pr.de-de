---
title: Iagentcommand getVisible
description: Iagentcommand getVisible
ms.assetid: cac07737-6a0b-4587-ae16-2137ce0d412c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1058c3855214dada0f1567f9fef81a3efc7e20a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390295"
---
# <a name="iagentcommandgetvisible"></a><span data-ttu-id="2882e-103">Iagentcommand:: getVisible</span><span class="sxs-lookup"><span data-stu-id="2882e-103">IAgentCommand::GetVisible</span></span>

<span data-ttu-id="2882e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="2882e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Command
);
```

<span data-ttu-id="2882e-105">Ruft den Wert der [**Visible**](visible-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)ab.</span><span class="sxs-lookup"><span data-stu-id="2882e-105">Retrieves the value of the [**Visible**](visible-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="2882e-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2882e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2882e-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbvisible*</span><span class="sxs-lookup"><span data-stu-id="2882e-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="2882e-108">Die Adresse einer Variablen, die die [**sichtbare**](visible-property.md) Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)empfängt.</span><span class="sxs-lookup"><span data-stu-id="2882e-108">The address of a variable that receives the [**Visible**](visible-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="2882e-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2882e-109">See Also</span></span>

<span data-ttu-id="2882e-110">[**Iagentcommand:: setVisible**](iagentcommand--setvisible.md), [**iagentcommand:: setCaption**](iagentcommand--setcaption.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="2882e-110">[**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 