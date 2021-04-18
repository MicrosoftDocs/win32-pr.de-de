---
title: Iagentcommand setVisible
description: Iagentcommand setVisible
ms.assetid: 58a383f4-6c98-4037-b469-ae68f06c852d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b583f79a93a5b13914486fb3e1a9cb513a682e63
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340265"
---
# <a name="iagentcommandsetvisible"></a><span data-ttu-id="49ea9-103">Iagentcommand:: setVisible</span><span class="sxs-lookup"><span data-stu-id="49ea9-103">IAgentCommand::SetVisible</span></span>

<span data-ttu-id="49ea9-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="49ea9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // Visible setting for Command
);
```

<span data-ttu-id="49ea9-105">Legt den Wert der [**Visible**](visible-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.</span><span class="sxs-lookup"><span data-stu-id="49ea9-105">Sets the value of the [**Visible**](visible-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="49ea9-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="49ea9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="49ea9-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*</span><span class="sxs-lookup"><span data-stu-id="49ea9-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="49ea9-108">Ein boolescher Wert, der die [**sichtbare**](visible-property.md) Eigenschaft eines [**Befehls**](/windows/desktop/lwef/the-command-object)bestimmt.</span><span class="sxs-lookup"><span data-stu-id="49ea9-108">A Boolean value that determines the [**Visible**](visible-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="49ea9-109">**True** zeigt den **Befehl** an. **False** blendet es aus.</span><span class="sxs-lookup"><span data-stu-id="49ea9-109">**True** shows the **Command**; **False** hides it.</span></span>

</dd> </dl>

<span data-ttu-id="49ea9-110">Für einen [**Befehl**](/windows/desktop/lwef/the-command-object) muss die [**Visible**](visible-property.md) -Eigenschaft auf **true** festgelegt sein, und die [**Beschriftung**](caption-property.md) -Eigenschaft muss im Popup Menü des Zeichens angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="49ea9-110">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Visible**](visible-property.md) property set to **True** and its [**Caption**](caption-property.md) property set to appear in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="49ea9-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="49ea9-111">See Also</span></span>

<span data-ttu-id="49ea9-112">[**Iagentcommand:: getVisible**](iagentcommand--getvisible.md), [**iagentcommand:: setCaption**](iagentcommand--setcaption.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="49ea9-112">[**IAgentCommand::GetVisible**](iagentcommand--getvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 