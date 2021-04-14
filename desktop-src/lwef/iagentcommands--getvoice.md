---
title: Iagentcommands getvoice
description: Iagentcommands getvoice
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1915512c89611267df3788e5dcaa84fb0874a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390317"
---
# <a name="iagentcommandsgetvoice"></a><span data-ttu-id="62b42-103">Iagentcommands:: getvoice</span><span class="sxs-lookup"><span data-stu-id="62b42-103">IAgentCommands::GetVoice</span></span>

<span data-ttu-id="62b42-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="62b42-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Commands collection
);
```

<span data-ttu-id="62b42-105">Ruft den Wert der [**Voice**](voice-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="62b42-105">Retrieves the value of the [**Voice**](voice-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="62b42-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="62b42-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="62b42-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszvoice*</span><span class="sxs-lookup"><span data-stu-id="62b42-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="62b42-108">Die Adresse eines BSTR-Werts, der den Wert der [**sprach**](voice-property.md) Texteinstellung für eine [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung empfängt.</span><span class="sxs-lookup"><span data-stu-id="62b42-108">The address of a BSTR that receives the value of the [**Voice**](voice-property.md) text setting for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="62b42-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="62b42-109">See Also</span></span>

<span data-ttu-id="62b42-110">[**Iagentcommands:: setvoice**](iagentcommands--setvoice.md), [**iagentcommands:: getcaption**](iagentcommands--getcaption.md), [**iagentcommands:: getVisible**](iagentcommands--getvisible.md)</span><span class="sxs-lookup"><span data-stu-id="62b42-110">[**IAgentCommands::SetVoice**](iagentcommands--setvoice.md), [**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md)</span></span>


 

 