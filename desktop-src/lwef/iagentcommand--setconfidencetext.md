---
title: Iagentcommand setconficetext
description: Iagentcommand setconficetext
ms.assetid: e776a2ba-3592-4f26-a3e3-2c044eed7f0c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cff1ae34c03f8ff67da61bea1834c25d6844ab2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390155"
---
# <a name="iagentcommandsetconfidencetext"></a><span data-ttu-id="919bf-103">Iagentcommand:: setconficetext</span><span class="sxs-lookup"><span data-stu-id="919bf-103">IAgentCommand::SetConfidenceText</span></span>

<span data-ttu-id="919bf-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="919bf-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetConfidenceText(
   BSTR bszTipText  // ConfidenceText setting for Command 
);
```

<span data-ttu-id="919bf-105">Legt den Wert des lauschtexttexts für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.</span><span class="sxs-lookup"><span data-stu-id="919bf-105">Sets the value of the Listening Tip text for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="919bf-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="919bf-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="919bf-107"><span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bsztiptext*</span><span class="sxs-lookup"><span data-stu-id="919bf-107"><span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*</span></span>
</dt> <dd>

<span data-ttu-id="919bf-108">Ein BSTR, der den Text für die [**conficetext**](confidencetext-property.md) -Eigenschaft eines [**Befehls**](/windows/desktop/lwef/the-command-object)angibt.</span><span class="sxs-lookup"><span data-stu-id="919bf-108">A BSTR that specifies the text for the [**ConfidenceText**](confidencetext-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="919bf-109">Wenn der von der am besten zurückgegebene Wert zurückgegebene Vertrauens Wert den Wert, der [**für die Eigenschaft**](/windows/desktop/lwef/the-command-object) [**conficethreshold**](/windows/desktop/lwef/confidence-property) zurückgegeben wurde, nicht überschreitet, wird der in *bsztiptext* angegebene Text in der lausch Info angezeigt.</span><span class="sxs-lookup"><span data-stu-id="919bf-109">If the confidence value returned of the best match returned in the [**Command**](/windows/desktop/lwef/the-command-object) event does not exceed the value set for the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property, the text supplied in *bszTipText* is displayed in the Listening Tip.</span></span>

## <a name="see-also"></a><span data-ttu-id="919bf-110">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="919bf-110">See Also</span></span>

<span data-ttu-id="919bf-111">[**Iagentcommand:: setconficethreshold**](iagentcommand--setconfidencethreshold.md), [**iagentcommand:: getconficethreshold**](iagentcommand--getconfidencethreshold.md), [**iagentcommand:: getconficetext**](iagentcommand--getconfidencetext.md), [**iagentuserinput:: getitemconfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="919bf-111">[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::GetConfidenceText**](iagentcommand--getconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 