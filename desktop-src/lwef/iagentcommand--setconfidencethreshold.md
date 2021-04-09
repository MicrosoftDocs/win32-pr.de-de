---
title: Iagentcommand setconficethreshold
description: Iagentcommand setconficethreshold
ms.assetid: f62d646a-895d-468c-9397-0495680109a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a6ba352f9385c57d0f3d1f01070f4b46e147d3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101615"
---
# <a name="iagentcommandsetconfidencethreshold"></a><span data-ttu-id="4cc87-103">Iagentcommand:: setconficethreshold</span><span class="sxs-lookup"><span data-stu-id="4cc87-103">IAgentCommand::SetConfidenceThreshold</span></span>

<span data-ttu-id="4cc87-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="4cc87-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

<span data-ttu-id="4cc87-105">Legt den Wert der Eigenschaft " [**Vertrauen**](confidence-property.md) " für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.</span><span class="sxs-lookup"><span data-stu-id="4cc87-105">Sets the value of the [**Confidence**](confidence-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="4cc87-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4cc87-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4cc87-107"><span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lconfidence*</span><span class="sxs-lookup"><span data-stu-id="4cc87-107"><span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*</span></span>
</dt> <dd>

<span data-ttu-id="4cc87-108">Der Wert für die Eigenschaft " [**Confidence**](confidence-property.md) " eines [**Befehls**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="4cc87-108">The value for the [**Confidence**](confidence-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="4cc87-109">Wenn der von der am besten zurückgegebene Wert zurückgegebene Vertrauens Wert den Wert, der [**für die Eigenschaft**](/windows/desktop/lwef/the-command-object) [**conficethreshold**](/windows/desktop/lwef/confidence-property) zurückgegeben wurde, nicht überschreitet, wird der in [**setconficetext**](iagentcommand--setconfidencetext.md) angegebene Text in der lausch Info angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4cc87-109">If the confidence value returned of the best match returned in the [**Command**](/windows/desktop/lwef/the-command-object) event does not exceed the value set for the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property, the text supplied in [**SetConfidenceText**](iagentcommand--setconfidencetext.md) is displayed in the Listening Tip.</span></span>

## <a name="see-also"></a><span data-ttu-id="4cc87-110">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4cc87-110">See Also</span></span>

<span data-ttu-id="4cc87-111">[**Iagentcommand:: getconficethreshold**](iagentcommand--getconfidencethreshold.md), [**iagentcommand:: setvertrauenstext**](iagentcommand--setconfidencetext.md), [**iagentuserinput:: getitemconfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="4cc87-111">[**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 