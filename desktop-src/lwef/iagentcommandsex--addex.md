---
title: Iagentcommandsex Addex
description: Iagentcommandsex Addex
ms.assetid: 54be4793-89ac-475b-8a6a-5b8c18bb4b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7487bb7c7af0295d82355c7a1f7fb50e30aa6e1f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725936"
---
# <a name="iagentcommandsexaddex"></a><span data-ttu-id="5d184-103">Iagentcommandsex:: Addex</span><span class="sxs-lookup"><span data-stu-id="5d184-103">IAgentCommandsEx::AddEx</span></span>

<span data-ttu-id="5d184-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="5d184-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT AddEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long * pdwID           // address for variable for ID
);
```

<span data-ttu-id="5d184-105">Fügt einer [**Befehls**](/windows/desktop/lwef/the-command-object) Auflistung einen [](/windows/desktop/lwef/the-commands-collection-object) Befehl hinzu.</span><span class="sxs-lookup"><span data-stu-id="5d184-105">Adds a [**Command**](/windows/desktop/lwef/the-command-object) to a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="5d184-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5d184-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5d184-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszcaption*</span><span class="sxs-lookup"><span data-stu-id="5d184-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="5d184-108">Ein BSTR, der den Wert des [**Beschriftungs**](caption-property.md) Texts angibt, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5d184-108">A BSTR that specifies the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="5d184-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszvoice*</span><span class="sxs-lookup"><span data-stu-id="5d184-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="5d184-110">Ein BSTR, der den Wert der [**sprach**](voice-property.md) Texteinstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="5d184-110">A BSTR that specifies the value of the [**Voice**](voice-property.md) text setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="5d184-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszvoicecaption*</span><span class="sxs-lookup"><span data-stu-id="5d184-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="5d184-112">Ein BSTR, der den Wert des [**voicecaption**](voicecaption-property.md) -Texts angibt, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5d184-112">A BSTR that specifies the value of the [**VoiceCaption**](voicecaption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="5d184-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*benabled*</span><span class="sxs-lookup"><span data-stu-id="5d184-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="5d184-114">Ein boolescher Ausdruck, der die [**aktivierte**](enabled-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in [**einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="5d184-114">A Boolean expression that specifies the [**Enabled**](enabled-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="5d184-115">Wenn der-Parameter **true** ist, ist der **Befehl** aktiviert und kann ausgewählt werden. **false** gibt an, dass der **Befehl** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5d184-115">If the parameter is **True**, the **Command** is enabled and can be selected; if **False**, the **Command** is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="5d184-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*</span><span class="sxs-lookup"><span data-stu-id="5d184-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="5d184-117">Ein boolescher Ausdruck, der die [**sichtbare**](visible-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) [**in einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="5d184-117">A Boolean expression that specifies the [**Visible**](visible-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="5d184-118">Wenn der-Parameter **true** ist, wird der **Befehl** im Popupmenü des Zeichens angezeigt (wenn die [**Caption**](caption-property.md) -Eigenschaft ebenfalls festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="5d184-118">If the parameter is **True**, the **Command** will be visible in the character's pop-up menu (if the [**Caption**](caption-property.md) property is also set).</span></span>

</dd> <dt>

<span data-ttu-id="5d184-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulhelpid*</span><span class="sxs-lookup"><span data-stu-id="5d184-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="5d184-120">Die Kontext Nummer des Hilfe Themas, das dem [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt zugeordnet ist. wird verwendet, um kontextbezogene Hilfe für den Befehl bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5d184-120">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> <dt>

<span data-ttu-id="5d184-121"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwid*</span><span class="sxs-lookup"><span data-stu-id="5d184-121"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span></span> 
</dt> <dd>

<span data-ttu-id="5d184-122">Adresse einer Variablen, die die ID für den hinzugefügten [**Befehl**](/windows/desktop/lwef/the-command-object)empfängt.</span><span class="sxs-lookup"><span data-stu-id="5d184-122">Address of a variable that receives the ID for the added [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="5d184-123">[**Iagentcommandsex:: Addex**](https://www.bing.com/search?q=**IAgentCommandsEx::AddEx**) erweitert [**iagentcommands:: Add**](iagentcommands--add.md) durch einschließen der [**HelpContextID**](helpcontextid-property.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5d184-123">[**IAgentCommandsEx::AddEx**](https://www.bing.com/search?q=**IAgentCommandsEx::AddEx**) extends [**IAgentCommands::Add**](iagentcommands--add.md) by including the [**HelpContextID**](helpcontextid-property.md) property.</span></span> <span data-ttu-id="5d184-124">Sie können die Eigenschaft auch mithilfe von [ **iagentcommandsex:: sethelpcontextid** festlegen.](iagentcommandsex--sethelpcontextid.md)</span><span class="sxs-lookup"><span data-stu-id="5d184-124">You can also set the property using [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="5d184-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5d184-125">See Also</span></span>

<span data-ttu-id="5d184-126">[**Iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommandsex:: sethelpcontextid**](iagentcommandsex--sethelpcontextid.md), [**iagentcommand:: setCaption**](iagentcommand--setcaption.md), [**iagentcommand:: SetEnabled**](iagentcommand--setenabled.md), [**iagentcommand:: setVisible**](iagentcommand--setvisible.md), [**iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommands:: Insert**](iagentcommands--insert.md), [**iagentcommandsex:: insertex**](iagentcommandsex--insertex.md), [**iagentcommands:: Remove**](iagentcommands--remove.md), [**iagentcommands:: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="5d184-126">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 