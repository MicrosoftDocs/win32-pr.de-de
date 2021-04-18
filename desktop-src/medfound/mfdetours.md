---
description: Gibt den Microsoft Media Foundation umleitet-Anbieter an, der Media Foundation API-Aufrufe verfolgt.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: MF-Umleitungen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09d39d6f8a7c7ff1d88471e71c6fc58aa49bd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343736"
---
# <a name="mfdetours-element"></a><span data-ttu-id="b9049-103">MF-Umleitungen-Element</span><span class="sxs-lookup"><span data-stu-id="b9049-103">mfdetours element</span></span>

<span data-ttu-id="b9049-104">Gibt den Microsoft Media Foundation umleitet-Anbieter an, der Media Foundation API-Aufrufe verfolgt.</span><span class="sxs-lookup"><span data-stu-id="b9049-104">Specifies the Microsoft Media Foundation Detours provider, which traces Media Foundation API calls.</span></span>

## <a name="usage"></a><span data-ttu-id="b9049-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="b9049-105">Usage</span></span>

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a><span data-ttu-id="b9049-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="b9049-106">Attributes</span></span>



| <span data-ttu-id="b9049-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="b9049-107">Attribute</span></span>            | <span data-ttu-id="b9049-108">type</span><span class="sxs-lookup"><span data-stu-id="b9049-108">Type</span></span>             | <span data-ttu-id="b9049-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b9049-109">Required</span></span>       | <span data-ttu-id="b9049-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9049-110">Description</span></span>                             |
|----------------------|------------------|----------------|-----------------------------------------|
| <span data-ttu-id="b9049-111">**level**</span><span class="sxs-lookup"><span data-stu-id="b9049-111">**level**</span></span><br/> | <span data-ttu-id="b9049-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="b9049-112">CDATA</span></span><br/> | <span data-ttu-id="b9049-113">Ja</span><span class="sxs-lookup"><span data-stu-id="b9049-113">Yes</span></span><br/> | <span data-ttu-id="b9049-114">Die Ablaufverfolgungsebene.</span><span class="sxs-lookup"><span data-stu-id="b9049-114">The trace level.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="b9049-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b9049-115">Child elements</span></span>



| <span data-ttu-id="b9049-116">Element</span><span class="sxs-lookup"><span data-stu-id="b9049-116">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="b9049-117">**Schlüsselwort**</span><span class="sxs-lookup"><span data-stu-id="b9049-117">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="b9049-118">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="b9049-118">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="b9049-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b9049-119">Parent elements</span></span>



| <span data-ttu-id="b9049-120">Element</span><span class="sxs-lookup"><span data-stu-id="b9049-120">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="b9049-121">**providers**</span><span class="sxs-lookup"><span data-stu-id="b9049-121">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="b9049-122">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b9049-122">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="b9049-123">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="b9049-123">Can be empty</span></span> | <span data-ttu-id="b9049-124">Nein</span><span class="sxs-lookup"><span data-stu-id="b9049-124">No</span></span>  |



## <a name="see-also"></a><span data-ttu-id="b9049-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b9049-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9049-126">MF-Ablauf Verfolgungs Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="b9049-126">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




