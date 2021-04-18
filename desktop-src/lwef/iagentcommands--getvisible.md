---
title: Iagentcommands getVisible
description: Iagentcommands getVisible
ms.assetid: 229a02c8-f0a1-4ee5-9bae-961b63792038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853a47f6136779415a08adc3c891d9b5cc95dcca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338660"
---
# <a name="iagentcommandsgetvisible"></a><span data-ttu-id="0b099-103">Iagentcommands:: getVisible</span><span class="sxs-lookup"><span data-stu-id="0b099-103">IAgentCommands::GetVisible</span></span>

<span data-ttu-id="0b099-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0b099-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Commands collection
);
```

<span data-ttu-id="0b099-105">Ruft den Wert der [**Visible**](visible-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="0b099-105">Retrieves the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="0b099-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0b099-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0b099-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbvisible*</span><span class="sxs-lookup"><span data-stu-id="0b099-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="0b099-108">Die Adresse einer Variablen, die den Wert der [**Visible**](visible-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung empfängt.</span><span class="sxs-lookup"><span data-stu-id="0b099-108">The address of a variable that receives the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="0b099-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0b099-109">See Also</span></span>

<span data-ttu-id="0b099-110">[**Iagentcommands:: setVisible**](iagentcommands--setvisible.md), [ **iagentcommands:: setCaption**](iagentcommands--setcaption.md)</span><span class="sxs-lookup"><span data-stu-id="0b099-110">[**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetCaption**](iagentcommands--setcaption.md)</span></span>


 

 