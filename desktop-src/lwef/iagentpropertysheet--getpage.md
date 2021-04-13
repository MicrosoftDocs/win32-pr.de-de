---
title: Iagentpropertysheet GetPage
description: Iagentpropertysheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb1fe6cdf6f667011eb048625349f6905913a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388380"
---
# <a name="iagentpropertysheetgetpage"></a><span data-ttu-id="658ab-103">Iagentpropertysheet:: GetPage</span><span class="sxs-lookup"><span data-stu-id="658ab-103">IAgentPropertySheet::GetPage</span></span>

<span data-ttu-id="658ab-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="658ab-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

<span data-ttu-id="658ab-105">Ruft die aktuelle Seite des Microsoft-Agent-Eigenschaften Blatts ab.</span><span class="sxs-lookup"><span data-stu-id="658ab-105">Retrieves the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="658ab-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="658ab-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="658ab-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszpage*</span><span class="sxs-lookup"><span data-stu-id="658ab-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span></span>
</dt> <dd>

<span data-ttu-id="658ab-108">Adresse einer Variablen, die die aktuelle Seite des Eigenschaften Blatts empfängt (zuletzt angezeigte Seite, wenn das Fenster nicht geöffnet ist).</span><span class="sxs-lookup"><span data-stu-id="658ab-108">Address of a variable that receives the current page of the property sheet (last viewed page if the window is not open).</span></span> <span data-ttu-id="658ab-109">Der Parameter kann eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="658ab-109">The parameter can be one of the following:</span></span>



|                 |                        |
|-----------------|------------------------|
| <span data-ttu-id="658ab-110">**Sprache**</span><span class="sxs-lookup"><span data-stu-id="658ab-110">**"Speech"**</span></span>    | <span data-ttu-id="658ab-111">Die Spracheingabe Seite.</span><span class="sxs-lookup"><span data-stu-id="658ab-111">The Speech Input page.</span></span> |
| <span data-ttu-id="658ab-112">**Ausgeben**</span><span class="sxs-lookup"><span data-stu-id="658ab-112">**"Output"**</span></span>    | <span data-ttu-id="658ab-113">Die Ausgabe Seite.</span><span class="sxs-lookup"><span data-stu-id="658ab-113">The Output page.</span></span>       |
| <span data-ttu-id="658ab-114">**Copyright**</span><span class="sxs-lookup"><span data-stu-id="658ab-114">**"Copyright"**</span></span> | <span data-ttu-id="658ab-115">Die Seite Copyright.</span><span class="sxs-lookup"><span data-stu-id="658ab-115">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="658ab-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="658ab-116">See Also</span></span>

[<span data-ttu-id="658ab-117">**Iagentpropertysheet:: setpage**</span><span class="sxs-lookup"><span data-stu-id="658ab-117">**IAgentPropertySheet::SetPage**</span></span>](iagentpropertysheet--setpage.md)


 

 




