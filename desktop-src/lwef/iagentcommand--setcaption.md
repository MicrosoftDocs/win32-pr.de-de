---
title: Iagentcommand setCaption
description: Iagentcommand setCaption
ms.assetid: f4fdd37a-28b4-4e00-885c-58addedec659
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88453f54ffa59b413f30d27c58aa6cd2dcc6e12e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038911"
---
# <a name="iagentcommandsetcaption"></a><span data-ttu-id="c7488-103">Iagentcommand:: setCaption</span><span class="sxs-lookup"><span data-stu-id="c7488-103">IAgentCommand::SetCaption</span></span>

<span data-ttu-id="c7488-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="c7488-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Command
);
```

<span data-ttu-id="c7488-105">Legt den [**Beschriftungs**](caption-property.md) Text fest, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c7488-105">Sets the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="c7488-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c7488-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c7488-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszcaption*</span><span class="sxs-lookup"><span data-stu-id="c7488-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="c7488-108">Ein BSTR, der den Text für die [**Caption**](caption-property.md) -Eigenschaft eines [**Befehls**](/windows/desktop/lwef/the-command-object)angibt.</span><span class="sxs-lookup"><span data-stu-id="c7488-108">A BSTR that specifies the text for the [**Caption**](caption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="c7488-109">Wenn Sie die [**Caption**](caption-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object) festlegen, wird definiert, wie diese im Popupmenü des Zeichens angezeigt wird, wenn die [**sichtbare**](visible-property.md) Eigenschaft auf **true** festgelegt ist und die Anwendung nicht der Eingabe aktive Client ist.</span><span class="sxs-lookup"><span data-stu-id="c7488-109">Setting the [**Caption**](caption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object) defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to **True** and your application is not the input-active client.</span></span> <span data-ttu-id="c7488-110">Um einen Zugriffsschlüssel (unline-mnetmonic) für Ihre **Beschriftung** anzugeben, fügen Sie vor diesem Zeichen ein kaufmännisches und-Zeichen (&) ein.</span><span class="sxs-lookup"><span data-stu-id="c7488-110">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span> <span data-ttu-id="c7488-111">Um ihn auswählbar zu machen, muss seine [**aktivierte**](enabled-property.md) Eigenschaft auf **true** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c7488-111">To make it selectable, its [**Enabled**](enabled-property.md) property must be set to **True**.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7488-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c7488-112">See Also</span></span>

<span data-ttu-id="c7488-113">[**Iagentcommand:: getcaption**](iagentcommand--getcaption.md), [**iagentcommand:: SetEnabled**](iagentcommand--setenabled.md), [**iagentcommand:: setVisible**](iagentcommand--setvisible.md), [**iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="c7488-113">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 