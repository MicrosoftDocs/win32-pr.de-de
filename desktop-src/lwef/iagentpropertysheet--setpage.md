---
title: Iagentpropertysheet (setpage)
description: Iagentpropertysheet (setpage)
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711352"
---
# <a name="iagentpropertysheetsetpage"></a><span data-ttu-id="e2bb3-103">Iagentpropertysheet:: setpage</span><span class="sxs-lookup"><span data-stu-id="e2bb3-103">IAgentPropertySheet::SetPage</span></span>

<span data-ttu-id="e2bb3-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e2bb3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

<span data-ttu-id="e2bb3-105">Legt die aktuelle Seite des Eigenschaften Blatts von Microsoft-Agent fest.</span><span class="sxs-lookup"><span data-stu-id="e2bb3-105">Sets the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="e2bb3-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e2bb3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e2bb3-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszpage*</span><span class="sxs-lookup"><span data-stu-id="e2bb3-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span></span>
</dt> <dd>

<span data-ttu-id="e2bb3-108">Ein BSTR, das die aktuelle Seite der Eigenschaft festlegt.</span><span class="sxs-lookup"><span data-stu-id="e2bb3-108">A BSTR that sets the current page of the property.</span></span> <span data-ttu-id="e2bb3-109">Der Parameter kann eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="e2bb3-109">The parameter can be one of the following.</span></span>



|                 |                        |
|-----------------|------------------------|
| <span data-ttu-id="e2bb3-110">**Sprache**</span><span class="sxs-lookup"><span data-stu-id="e2bb3-110">**"Speech"**</span></span>    | <span data-ttu-id="e2bb3-111">Die Spracheingabe Seite.</span><span class="sxs-lookup"><span data-stu-id="e2bb3-111">The Speech Input page.</span></span> |
| <span data-ttu-id="e2bb3-112">**Ausgeben**</span><span class="sxs-lookup"><span data-stu-id="e2bb3-112">**"Output"**</span></span>    | <span data-ttu-id="e2bb3-113">Die Ausgabe Seite.</span><span class="sxs-lookup"><span data-stu-id="e2bb3-113">The Output page.</span></span>       |
| <span data-ttu-id="e2bb3-114">**Copyright**</span><span class="sxs-lookup"><span data-stu-id="e2bb3-114">**"Copyright"**</span></span> | <span data-ttu-id="e2bb3-115">Die Seite Copyright.</span><span class="sxs-lookup"><span data-stu-id="e2bb3-115">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="e2bb3-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e2bb3-116">See Also</span></span>

[<span data-ttu-id="e2bb3-117">**Iagentpropertysheet:: GetPage**</span><span class="sxs-lookup"><span data-stu-id="e2bb3-117">**IAgentPropertySheet::GetPage**</span></span>](iagentpropertysheet--getpage.md)


 

 




