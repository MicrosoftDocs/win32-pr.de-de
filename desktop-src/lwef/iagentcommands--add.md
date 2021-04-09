---
title: Iagentcommands hinzufügen
description: Iagentcommands hinzufügen
ms.assetid: f6be7773-77fa-4c59-8feb-c2ebf54fd2e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee56854c302a096143e58fe6c21ef75fedfbf59
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101482"
---
# <a name="iagentcommandsadd"></a><span data-ttu-id="e0d22-103">Iagentcommands:: Add</span><span class="sxs-lookup"><span data-stu-id="e0d22-103">IAgentCommands::Add</span></span>

<span data-ttu-id="e0d22-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e0d22-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Add(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long * pdwID      // address for variable for ID
);
```

<span data-ttu-id="e0d22-105">Fügt einer [**Befehls**](/windows/desktop/lwef/the-command-object) Auflistung einen [](/windows/desktop/lwef/the-commands-collection-object) Befehl hinzu.</span><span class="sxs-lookup"><span data-stu-id="e0d22-105">Adds a [**Command**](/windows/desktop/lwef/the-command-object) to a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="e0d22-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e0d22-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e0d22-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszcaption*</span><span class="sxs-lookup"><span data-stu-id="e0d22-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="e0d22-108">Ein BSTR, der den Wert des [**Beschriftungs**](caption-property.md) Texts angibt, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e0d22-108">A BSTR that specifies the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="e0d22-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszvoice*</span><span class="sxs-lookup"><span data-stu-id="e0d22-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="e0d22-110">Ein BSTR, der den Wert der [**sprach**](voice-property.md) Texteinstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="e0d22-110">A BSTR that specifies the value of the [**Voice**](voice-property.md) text setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="e0d22-111"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*benabled*</span><span class="sxs-lookup"><span data-stu-id="e0d22-111"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="e0d22-112">Ein boolescher Ausdruck, der die [**aktivierte**](enabled-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in [**einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="e0d22-112">A Boolean expression that specifies the [**Enabled**](enabled-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="e0d22-113">Wenn der-Parameter **true** ist, ist der **Befehl** aktiviert und kann ausgewählt werden. **false** gibt an, dass der **Befehl** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e0d22-113">If the parameter is **True**, the **Command** is enabled and can be selected; if **False**, the **Command** is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="e0d22-114"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*</span><span class="sxs-lookup"><span data-stu-id="e0d22-114"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="e0d22-115">Ein boolescher Ausdruck, der die [**sichtbare**](visible-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) [**in einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="e0d22-115">A Boolean expression that specifies the [**Visible**](visible-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="e0d22-116">Wenn der-Parameter **true** ist, wird der **Befehl** im Popupmenü des Zeichens angezeigt (wenn die [**Caption**](caption-property.md) -Eigenschaft ebenfalls festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="e0d22-116">If the parameter is **True**, the **Command** will be visible in the character's pop-up menu (if the [**Caption**](caption-property.md) property is also set).</span></span>

</dd> <dt>

<span data-ttu-id="e0d22-117"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwid*</span><span class="sxs-lookup"><span data-stu-id="e0d22-117"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span></span> 
</dt> <dd>

<span data-ttu-id="e0d22-118">Adresse einer Variablen, die die ID für den hinzugefügten [**Befehl**](/windows/desktop/lwef/the-command-object)empfängt.</span><span class="sxs-lookup"><span data-stu-id="e0d22-118">Address of a variable that receives the ID for the added [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="e0d22-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e0d22-119">See Also</span></span>

<span data-ttu-id="e0d22-120">[**Iagentcommand:: setCaption**](iagentcommand--setcaption.md), [**iagentcommand:: SetEnabled**](iagentcommand--setenabled.md), [**iagentcommand:: setVisible**](iagentcommand--setvisible.md), [**iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommands:: Insert**](iagentcommands--insert.md), [**iagentcommands:: Remove**](iagentcommands--remove.md), [**iagentcommands:: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="e0d22-120">[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 