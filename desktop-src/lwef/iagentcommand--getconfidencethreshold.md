---
title: Iagentcommand getconficethreshold
description: Iagentcommand getconficethreshold
ms.assetid: dfbaba7c-ed45-464e-82ab-39e33c023e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6557ad4e6831734106ee2c2e8021f923ef8806
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725945"
---
# <a name="iagentcommandgetconfidencethreshold"></a><span data-ttu-id="594bd-103">Iagentcommand:: getconficethreshold</span><span class="sxs-lookup"><span data-stu-id="594bd-103">IAgentCommand::GetConfidenceThreshold</span></span>

<span data-ttu-id="594bd-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="594bd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetConfidenceThreshold(
long * plConfidenceThreshold  // address of ConfidenceThreshold 
);                            // setting for Command
```

<span data-ttu-id="594bd-105">Ruft den Wert der [**conficethreshold**](/windows/desktop/lwef/confidence-property) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)ab.</span><span class="sxs-lookup"><span data-stu-id="594bd-105">Retrieves the value of the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="594bd-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="594bd-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="594bd-107"><span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*plconficethreshold*</span><span class="sxs-lookup"><span data-stu-id="594bd-107"><span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*plConfidenceThreshold*</span></span>
</dt> <dd>

<span data-ttu-id="594bd-108">Die Adresse einer Variablen, die den Wert der [**conficethreshold**](/windows/desktop/lwef/confidence-property) -Eigenschaft für einen Befehl empfängt.</span><span class="sxs-lookup"><span data-stu-id="594bd-108">The address of a variable that receives the value of the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property for a Command.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="594bd-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="594bd-109">See Also</span></span>

<span data-ttu-id="594bd-110">[**Iagentcommand:: setconficethreshold**](iagentcommand--setconfidencethreshold.md), [**iagentcommand:: setvertrauenstext**](iagentcommand--setconfidencetext.md), [**iagentuserinput:: getitemconfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="594bd-110">[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 