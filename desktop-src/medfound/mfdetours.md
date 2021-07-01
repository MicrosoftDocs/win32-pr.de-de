---
description: Gibt den Microsoft Media Foundation Detours-Anbieter an, der Media Foundation API-Aufrufe verfolgt.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: mfdetours-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cd03711c74c21a9a6ff33d2cc2560e4b6d6e0a3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119335"
---
# <a name="mfdetours-element"></a><span data-ttu-id="64617-103">mfdetours-Element</span><span class="sxs-lookup"><span data-stu-id="64617-103">mfdetours element</span></span>

<span data-ttu-id="64617-104">Gibt den Microsoft Media Foundation Detours-Anbieter an, der Media Foundation API-Aufrufe verfolgt.</span><span class="sxs-lookup"><span data-stu-id="64617-104">Specifies the Microsoft Media Foundation Detours provider, which traces Media Foundation API calls.</span></span>

## <a name="usage"></a><span data-ttu-id="64617-105">Verwendung</span><span class="sxs-lookup"><span data-stu-id="64617-105">Usage</span></span>

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a><span data-ttu-id="64617-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="64617-106">Attributes</span></span>



| <span data-ttu-id="64617-107">attribute</span><span class="sxs-lookup"><span data-stu-id="64617-107">Attribute</span></span>            | <span data-ttu-id="64617-108">Typ</span><span class="sxs-lookup"><span data-stu-id="64617-108">Type</span></span>             | <span data-ttu-id="64617-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="64617-109">Required</span></span>       | <span data-ttu-id="64617-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64617-110">Description</span></span>                             |
|----------------------|------------------|----------------|-----------------------------------------|
| <span data-ttu-id="64617-111">**level**</span><span class="sxs-lookup"><span data-stu-id="64617-111">**level**</span></span><br/> | <span data-ttu-id="64617-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="64617-112">CDATA</span></span><br/> | <span data-ttu-id="64617-113">Ja</span><span class="sxs-lookup"><span data-stu-id="64617-113">Yes</span></span><br/> | <span data-ttu-id="64617-114">Die Ablaufverfolgungsebene.</span><span class="sxs-lookup"><span data-stu-id="64617-114">The trace level.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="64617-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="64617-115">Child elements</span></span>



| <span data-ttu-id="64617-116">Element</span><span class="sxs-lookup"><span data-stu-id="64617-116">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="64617-117">**Schlüsselwort**</span><span class="sxs-lookup"><span data-stu-id="64617-117">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="64617-118">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="64617-118">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="64617-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="64617-119">Parent elements</span></span>

| <span data-ttu-id="64617-120">Element</span><span class="sxs-lookup"><span data-stu-id="64617-120">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="64617-121">**Anbieter**</span><span class="sxs-lookup"><span data-stu-id="64617-121">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="64617-122">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="64617-122">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="64617-123">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="64617-123">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="64617-124">Nein</span><span class="sxs-lookup"><span data-stu-id="64617-124">No</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="64617-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="64617-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64617-126">MFTrace-Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="64617-126">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




