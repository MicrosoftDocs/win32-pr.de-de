---
title: Navigate-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Das Navigate-Element gibt eine URL an, die von Aufrufen von "extern. navigatetaskpaneurl" verwendet wird.
ms.assetid: 3898e381-baf8-481a-90ee-d64e55b319a0
keywords:
- Navigation in Element Fenstern Media Player
topic_type:
- apiref
api_name:
- Navigate Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab3a76fba522332f1414b02d3e317f2793e88292
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367024"
---
# <a name="navigate-element"></a><span data-ttu-id="e8013-106">Navigate-Element</span><span class="sxs-lookup"><span data-stu-id="e8013-106">Navigate Element</span></span>

> [!Note]  
> <span data-ttu-id="e8013-107">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="e8013-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e8013-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e8013-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e8013-109">Das **Navigate** -Element gibt eine URL an, die von Aufrufen von " **extern. navigatetaskpaneurl**" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8013-109">The **Navigate** element specifies a URL used by calls to **External.NavigateTaskPaneURL**.</span></span>

``` syntax
<Navigate
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="e8013-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="e8013-110">Attributes</span></span>



| <span data-ttu-id="e8013-111">Begriff</span><span class="sxs-lookup"><span data-stu-id="e8013-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="e8013-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8013-112">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8013-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**Baseurl** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="e8013-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span><br/> | <span data-ttu-id="e8013-114">Voll qualifizierte URL für die Webseite, zu der navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8013-114">Fully qualified URL for the webpage to which to navigate.</span></span> <span data-ttu-id="e8013-115">**Navigatetaskpaneurl** kann eine Abfrage Zeichenfolge an diese URL anfügen.</span><span class="sxs-lookup"><span data-stu-id="e8013-115">**NavigateTaskPaneURL** can append a query string to this URL.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="e8013-116">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="e8013-116">Parent/Child Elements</span></span>



| <span data-ttu-id="e8013-117">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="e8013-117">Hierarchy</span></span>       | <span data-ttu-id="e8013-118">Element</span><span class="sxs-lookup"><span data-stu-id="e8013-118">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="e8013-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8013-119">Parent elements</span></span> | <span data-ttu-id="e8013-120">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="e8013-120">**ServiceInfo**</span></span> |
| <span data-ttu-id="e8013-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8013-121">Child elements</span></span>  | <span data-ttu-id="e8013-122">Keine</span><span class="sxs-lookup"><span data-stu-id="e8013-122">None</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="e8013-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8013-123">Requirements</span></span>



| <span data-ttu-id="e8013-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8013-124">Requirement</span></span> | <span data-ttu-id="e8013-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e8013-125">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="e8013-126">Version</span><span class="sxs-lookup"><span data-stu-id="e8013-126">Version</span></span><br/> | <span data-ttu-id="e8013-127">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e8013-127">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8013-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8013-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8013-129">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="e8013-129">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="e8013-130">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="e8013-130">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="e8013-131">**Extern. navigatetaskpaneurl**</span><span class="sxs-lookup"><span data-stu-id="e8013-131">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="e8013-132">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="e8013-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





