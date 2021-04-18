---
title: Iagentcommands getcaption
description: Iagentcommands getcaption
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f886413ae6bfbfe104306d7280d8c66b08bf311a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340897"
---
# <a name="iagentcommandsgetcaption"></a><span data-ttu-id="1a71b-103">Iagentcommands:: getcaption</span><span class="sxs-lookup"><span data-stu-id="1a71b-103">IAgentCommands::GetCaption</span></span>

<span data-ttu-id="1a71b-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="1a71b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

<span data-ttu-id="1a71b-105">Ruft die [**Beschriftung**](caption-property.md) für eine [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="1a71b-105">Retrieves the [**Caption**](caption-property.md) for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="1a71b-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1a71b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1a71b-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszcaption*</span><span class="sxs-lookup"><span data-stu-id="1a71b-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="1a71b-108">Die Adresse eines BSTR-Werts, der den Wert der über [**Schrift**](caption-property.md) Texteinstellung empfängt, der für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1a71b-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text setting displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="1a71b-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1a71b-109">See Also</span></span>

<span data-ttu-id="1a71b-110">[**Iagentcommands:: setCaption**](iagentcommands--setcaption.md), [**iagentcommands:: getVisible**](iagentcommands--getvisible.md), [**iagentcommands:: getvoice**](iagentcommands--getvoice.md)</span><span class="sxs-lookup"><span data-stu-id="1a71b-110">[**IAgentCommands::SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommands::GetVoice**](iagentcommands--getvoice.md)</span></span>


 

 