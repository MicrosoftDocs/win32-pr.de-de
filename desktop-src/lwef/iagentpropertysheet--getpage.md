---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c08e564b5170d62cf5757536b9e11baec4883c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119865"
---
# <a name="iagentpropertysheetgetpage"></a><span data-ttu-id="1d565-103">IAgentPropertySheet::GetPage</span><span class="sxs-lookup"><span data-stu-id="1d565-103">IAgentPropertySheet::GetPage</span></span>

<span data-ttu-id="1d565-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="1d565-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

<span data-ttu-id="1d565-105">Ruft die aktuelle Seite des Eigenschaftenblatts des Microsoft-Agents ab.</span><span class="sxs-lookup"><span data-stu-id="1d565-105">Retrieves the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="1d565-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1d565-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1d565-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span><span class="sxs-lookup"><span data-stu-id="1d565-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span></span>
</dt> <dd>

<span data-ttu-id="1d565-108">Adresse einer Variablen, die die aktuelle Seite des Eigenschaftenblatts empfängt (zuletzt angezeigte Seite, wenn das Fenster nicht geöffnet ist).</span><span class="sxs-lookup"><span data-stu-id="1d565-108">Address of a variable that receives the current page of the property sheet (last viewed page if the window is not open).</span></span> <span data-ttu-id="1d565-109">Der -Parameter kann eine der folgenden Sein:</span><span class="sxs-lookup"><span data-stu-id="1d565-109">The parameter can be one of the following:</span></span>



|                 | <span data-ttu-id="1d565-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d565-110">Description</span></span>            |
|-----------------|------------------------|
| <span data-ttu-id="1d565-111">**"Speech"**</span><span class="sxs-lookup"><span data-stu-id="1d565-111">**"Speech"**</span></span>    | <span data-ttu-id="1d565-112">Die Seite Spracheingabe.</span><span class="sxs-lookup"><span data-stu-id="1d565-112">The Speech Input page.</span></span> |
| <span data-ttu-id="1d565-113">**"Ausgabe"**</span><span class="sxs-lookup"><span data-stu-id="1d565-113">**"Output"**</span></span>    | <span data-ttu-id="1d565-114">Die Seite Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="1d565-114">The Output page.</span></span>       |
| <span data-ttu-id="1d565-115">**"Copyright"**</span><span class="sxs-lookup"><span data-stu-id="1d565-115">**"Copyright"**</span></span> | <span data-ttu-id="1d565-116">Die Copyrightseite.</span><span class="sxs-lookup"><span data-stu-id="1d565-116">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="1d565-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1d565-117">See Also</span></span>

[<span data-ttu-id="1d565-118">**IAgentPropertySheet::SetPage**</span><span class="sxs-lookup"><span data-stu-id="1d565-118">**IAgentPropertySheet::SetPage**</span></span>](iagentpropertysheet--setpage.md)


 

 




