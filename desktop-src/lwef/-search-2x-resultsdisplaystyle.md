---
title: Resultendisplaystyle-Enumeration
description: Wird von iresultviewer resultstyle verwendet, um festzulegen, wie Ergebnisse angezeigt werden, oder legt diese fest.
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- Resultdisplaystyle-Enumeration Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- ResultsDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26d564e0a7bb8a10b44e2957f26aa20a07afa535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369216"
---
# <a name="resultsdisplaystyle-enumeration"></a><span data-ttu-id="4b47e-104">Resultendisplaystyle-Enumeration</span><span class="sxs-lookup"><span data-stu-id="4b47e-104">ResultsDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="4b47e-105">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="4b47e-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="4b47e-106">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="4b47e-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="4b47e-107">Wird von [**iresultviewer:: resultstyle**](-search-2x-iresultsviewer-resultsstyle.md) verwendet, um festzulegen oder zu bestimmen, wie Ergebnisse angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4b47e-107">Used by [**IResultsViewer::ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) to set or determine how results are displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b47e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b47e-108">Syntax</span></span>


```C++
typedef enum ResultsDisplayStyleEnum { 
  SmallIconResults  = 0,
  LargeIconResults  = 1
} ResultsDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="4b47e-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="4b47e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4b47e-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**Smallireresults**</span><span class="sxs-lookup"><span data-stu-id="4b47e-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="4b47e-111">Gibt an, dass die Ergebnisse als kleine Symbole angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4b47e-111">Indicates Results are displayed as small icons.</span></span>

</dd> <dt>

<span data-ttu-id="4b47e-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**Largeireresults**</span><span class="sxs-lookup"><span data-stu-id="4b47e-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="4b47e-113">Gibt an, dass die Ergebnisse als große Symbole angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4b47e-113">Indicates Results are displayed as large icons.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b47e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b47e-114">Requirements</span></span>



| <span data-ttu-id="4b47e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b47e-115">Requirement</span></span> | <span data-ttu-id="4b47e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4b47e-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b47e-117">IDL</span><span class="sxs-lookup"><span data-stu-id="4b47e-117">IDL</span></span><br/> | <dl> <span data-ttu-id="4b47e-118"><dt>Wdsview. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b47e-118"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





