---
description: Gibt einen Ablaufverfolgungsanbieter (ETW oder WPP) für MFTrace an.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d96b3015dddbcff74c09f77a1b6245d052fe034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118445"
---
# <a name="provider-element"></a><span data-ttu-id="97c6f-103">provider-Element</span><span class="sxs-lookup"><span data-stu-id="97c6f-103">provider element</span></span>

<span data-ttu-id="97c6f-104">Gibt einen Ablaufverfolgungsanbieter (ETW oder WPP) für [MFTrace](mftrace.md)an.</span><span class="sxs-lookup"><span data-stu-id="97c6f-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="97c6f-105">Verwendung</span><span class="sxs-lookup"><span data-stu-id="97c6f-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="97c6f-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="97c6f-106">Attributes</span></span>



| <span data-ttu-id="97c6f-107">attribute</span><span class="sxs-lookup"><span data-stu-id="97c6f-107">Attribute</span></span>            | <span data-ttu-id="97c6f-108">Typ</span><span class="sxs-lookup"><span data-stu-id="97c6f-108">Type</span></span>             | <span data-ttu-id="97c6f-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="97c6f-109">Required</span></span>       | <span data-ttu-id="97c6f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97c6f-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="97c6f-111">**ID**</span><span class="sxs-lookup"><span data-stu-id="97c6f-111">**ID**</span></span><br/>    | <span data-ttu-id="97c6f-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="97c6f-112">CDATA</span></span><br/> | <span data-ttu-id="97c6f-113">Ja</span><span class="sxs-lookup"><span data-stu-id="97c6f-113">Yes</span></span><br/> | <span data-ttu-id="97c6f-114">Der Name oder die GUID des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="97c6f-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="97c6f-115">**level**</span><span class="sxs-lookup"><span data-stu-id="97c6f-115">**level**</span></span><br/> | <span data-ttu-id="97c6f-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="97c6f-116">CDATA</span></span><br/> | <span data-ttu-id="97c6f-117">Ja</span><span class="sxs-lookup"><span data-stu-id="97c6f-117">Yes</span></span><br/> | <span data-ttu-id="97c6f-118">Die Ablaufverfolgungsebene.</span><span class="sxs-lookup"><span data-stu-id="97c6f-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="97c6f-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97c6f-119">Child elements</span></span>



| <span data-ttu-id="97c6f-120">Element</span><span class="sxs-lookup"><span data-stu-id="97c6f-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="97c6f-121">**Schlüsselwort**</span><span class="sxs-lookup"><span data-stu-id="97c6f-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="97c6f-122">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="97c6f-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="97c6f-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97c6f-123">Parent elements</span></span>



| <span data-ttu-id="97c6f-124">Element</span><span class="sxs-lookup"><span data-stu-id="97c6f-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="97c6f-125">**Anbieter**</span><span class="sxs-lookup"><span data-stu-id="97c6f-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="97c6f-126">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="97c6f-126">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="97c6f-127">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="97c6f-127">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="97c6f-128">Nein</span><span class="sxs-lookup"><span data-stu-id="97c6f-128">No</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="97c6f-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="97c6f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c6f-130">MFTrace-Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="97c6f-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




