---
title: Iagentcommand getvoice
description: Iagentcommand getvoice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2365019f71447e9d9c5a560c6506ee1dae7423df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341710"
---
# <a name="iagentcommandgetvoice"></a><span data-ttu-id="e88e1-103">Iagentcommand:: getvoice</span><span class="sxs-lookup"><span data-stu-id="e88e1-103">IAgentCommand::GetVoice</span></span>

<span data-ttu-id="e88e1-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e88e1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

<span data-ttu-id="e88e1-105">Ruft den Wert der [**Voice**](voice-property.md) -Text-Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)ab.</span><span class="sxs-lookup"><span data-stu-id="e88e1-105">Retrieves the value of the [**Voice**](voice-property.md) text property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="e88e1-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e88e1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e88e1-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszvoice*</span><span class="sxs-lookup"><span data-stu-id="e88e1-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="e88e1-108">Die Adresse eines BSTR, der die [**Voice**](voice-property.md) -Text-Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)empfängt.</span><span class="sxs-lookup"><span data-stu-id="e88e1-108">The address of a BSTR that receives the [**Voice**](voice-property.md) text property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="e88e1-109">Ein [**Befehl**](/windows/desktop/lwef/the-command-object) , bei dem der [**Voice**](voice-property.md) -Eigenschaften Satz und seine [**aktivierte**](enabled-property.md) Eigenschaft auf **true** festgelegt sind, sind sprach zugänglich.</span><span class="sxs-lookup"><span data-stu-id="e88e1-109">A [**Command**](/windows/desktop/lwef/the-command-object) with its [**Voice**](voice-property.md) property set and its [**Enabled**](enabled-property.md) property set to **True** will be voice-accessible.</span></span> <span data-ttu-id="e88e1-110">Wenn die [**Beschriftungs**](caption-property.md) Eigenschaft ebenfalls festgelegt ist, wird Sie im Fenster "Sprachbefehle" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e88e1-110">If its [**Caption**](caption-property.md) property is also set it appears in the Voice Commands Window.</span></span> <span data-ttu-id="e88e1-111">Wenn die [**sichtbare**](visible-property.md) Eigenschaft auf **true** festgelegt ist, wird Sie im Popupmenü des Zeichens angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e88e1-111">If its [**Visible**](visible-property.md) property is set to **True**, it appears in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="e88e1-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e88e1-112">See Also</span></span>

<span data-ttu-id="e88e1-113">[**Iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="e88e1-113">[**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 