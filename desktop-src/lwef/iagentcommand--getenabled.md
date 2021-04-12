---
title: Iagentcommand GetEnabled
description: Iagentcommand GetEnabled
ms.assetid: b4ec25d2-b2e0-4b1b-8dc5-10fbb44149b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238844a70ea7fde3ef0c07cad1a6f3abab5613d1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472932"
---
# <a name="iagentcommandgetenabled"></a><span data-ttu-id="5acbe-103">Iagentcommand:: GetEnabled</span><span class="sxs-lookup"><span data-stu-id="5acbe-103">IAgentCommand::GetEnabled</span></span>

<span data-ttu-id="5acbe-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="5acbe-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of Enabled setting for Command
);
```

<span data-ttu-id="5acbe-105">Ruft den Wert der [**aktivierten**](enabled-property.md) Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)ab.</span><span class="sxs-lookup"><span data-stu-id="5acbe-105">Retrieves the value of the [**Enabled**](enabled-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="5acbe-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5acbe-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5acbe-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbenabled*</span><span class="sxs-lookup"><span data-stu-id="5acbe-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="5acbe-108">Die Adresse einer Variablen, die **true** erhält, wenn der [**Befehl**](/windows/desktop/lwef/the-command-object) aktiviert ist, oder **false** , wenn Sie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5acbe-108">The address of a variable that receives **True** if the [**Command**](/windows/desktop/lwef/the-command-object) is enabled, or **False** if it is disabled.</span></span> <span data-ttu-id="5acbe-109">Ein deaktivierter **Befehl** kann nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="5acbe-109">A disabled **Command** cannot be selected.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="5acbe-110">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5acbe-110">See Also</span></span>

<span data-ttu-id="5acbe-111">[**Iagentcommand:: setCaption**](iagentcommand--setcaption.md), [**iagentcommand:: setVisible**](iagentcommand--setvisible.md), [**iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="5acbe-111">[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 