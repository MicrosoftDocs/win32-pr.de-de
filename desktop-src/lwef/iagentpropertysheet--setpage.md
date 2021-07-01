---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b84f9b9d5f74170644488cc2049376ecf409997
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120745"
---
# <a name="iagentpropertysheetsetpage"></a><span data-ttu-id="00637-103">IAgentPropertySheet::SetPage</span><span class="sxs-lookup"><span data-stu-id="00637-103">IAgentPropertySheet::SetPage</span></span>

<span data-ttu-id="00637-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="00637-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

<span data-ttu-id="00637-105">Legt die aktuelle Seite des Eigenschaftenblatts des Microsoft-Agents fest.</span><span class="sxs-lookup"><span data-stu-id="00637-105">Sets the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="00637-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="00637-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="00637-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span><span class="sxs-lookup"><span data-stu-id="00637-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span></span>
</dt> <dd>

<span data-ttu-id="00637-108">Ein BSTR, der die aktuelle Seite der Eigenschaft festlegt.</span><span class="sxs-lookup"><span data-stu-id="00637-108">A BSTR that sets the current page of the property.</span></span> <span data-ttu-id="00637-109">Der -Parameter kann einer der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="00637-109">The parameter can be one of the following.</span></span>



|                 | <span data-ttu-id="00637-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00637-110">Description</span></span>            |
|-----------------|------------------------|
| <span data-ttu-id="00637-111">**"Speech"**</span><span class="sxs-lookup"><span data-stu-id="00637-111">**"Speech"**</span></span>    | <span data-ttu-id="00637-112">Die Seite Spracheingabe.</span><span class="sxs-lookup"><span data-stu-id="00637-112">The Speech Input page.</span></span> |
| <span data-ttu-id="00637-113">**"Ausgabe"**</span><span class="sxs-lookup"><span data-stu-id="00637-113">**"Output"**</span></span>    | <span data-ttu-id="00637-114">Die Seite Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="00637-114">The Output page.</span></span>       |
| <span data-ttu-id="00637-115">**"Copyright"**</span><span class="sxs-lookup"><span data-stu-id="00637-115">**"Copyright"**</span></span> | <span data-ttu-id="00637-116">Die Copyrightseite.</span><span class="sxs-lookup"><span data-stu-id="00637-116">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="00637-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="00637-117">See Also</span></span>

[<span data-ttu-id="00637-118">**IAgentPropertySheet::GetPage**</span><span class="sxs-lookup"><span data-stu-id="00637-118">**IAgentPropertySheet::GetPage**</span></span>](iagentpropertysheet--getpage.md)


 

 




