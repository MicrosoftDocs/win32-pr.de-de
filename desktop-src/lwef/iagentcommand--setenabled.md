---
title: Iagentcommand-abgeleitete
description: Iagentcommand-abgeleitete
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8377307d66257f7a9b74ac82512edc6e4ec64034
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038864"
---
# <a name="iagentcommandsetenabled"></a><span data-ttu-id="dc461-103">Iagentcommand:: stenabled</span><span class="sxs-lookup"><span data-stu-id="dc461-103">IAgentCommand::SetEnabled</span></span>

<span data-ttu-id="dc461-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="dc461-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

<span data-ttu-id="dc461-105">Legt die [**aktivierte**](enabled-property.md) Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.</span><span class="sxs-lookup"><span data-stu-id="dc461-105">Sets the [**Enabled**](enabled-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="dc461-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="dc461-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="dc461-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*benabled*</span><span class="sxs-lookup"><span data-stu-id="dc461-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="dc461-108">Ein boolescher Wert, der den Wert der [**aktivierten**](enabled-property.md) Einstellung eines [**Befehls**](/windows/desktop/lwef/the-command-object)festlegt.</span><span class="sxs-lookup"><span data-stu-id="dc461-108">A Boolean value that sets the value of the [**Enabled**](enabled-property.md) setting of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="dc461-109">**True** aktiviert den **Befehl**. **False** deaktiviert es.</span><span class="sxs-lookup"><span data-stu-id="dc461-109">**True** enables the **Command**; **False** disables it.</span></span> <span data-ttu-id="dc461-110">Ein deaktivierter **Befehl** kann nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="dc461-110">A disabled **Command** cannot be selected.</span></span>

</dd> </dl>

<span data-ttu-id="dc461-111">Für einen [**Befehl**](/windows/desktop/lwef/the-command-object) muss die [**aktivierte**](enabled-property.md) Eigenschaft auf **true** festgelegt sein, damit Sie ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="dc461-111">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Enabled**](enabled-property.md) property set to **True** to be selectable.</span></span> <span data-ttu-id="dc461-112">Außerdem muss die [**Beschriftung**](caption-property.md) -Eigenschaft festgelegt sein, und die [**Visible**](visible-property.md) -Eigenschaft muss auf **true** festgelegt sein, damit Sie im Popup Menü des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dc461-112">It also must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear in the character's pop-up menu.</span></span> <span data-ttu-id="dc461-113">Damit der **Befehl** im **Fenster "Sprachbefehle**" angezeigt wird, müssen Sie die [**Voice**](voice-property.md)-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="dc461-113">To make the **Command** appear in the **Voice Commands Window**, you must set its [**Voice**](voice-property.md)property.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc461-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dc461-114">See Also</span></span>

<span data-ttu-id="dc461-115">[**Iagentcommand:: getcaption**](iagentcommand--getcaption.md), [**iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="dc461-115">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 