---
description: Gibt einen Ablauf Verfolgungs Anbieter (ETW oder WPP) für MF-Ablauf Verfolgung an.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ca319b686101766dacd79821ac6d9caf859cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753897"
---
# <a name="provider-element"></a><span data-ttu-id="17907-103">provider-Element</span><span class="sxs-lookup"><span data-stu-id="17907-103">provider element</span></span>

<span data-ttu-id="17907-104">Gibt einen Ablauf Verfolgungs Anbieter (ETW oder WPP) für [MF](mftrace.md)-Ablauf Verfolgung an.</span><span class="sxs-lookup"><span data-stu-id="17907-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="17907-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="17907-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="17907-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="17907-106">Attributes</span></span>



| <span data-ttu-id="17907-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="17907-107">Attribute</span></span>            | <span data-ttu-id="17907-108">type</span><span class="sxs-lookup"><span data-stu-id="17907-108">Type</span></span>             | <span data-ttu-id="17907-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="17907-109">Required</span></span>       | <span data-ttu-id="17907-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17907-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="17907-111">**ID**</span><span class="sxs-lookup"><span data-stu-id="17907-111">**ID**</span></span><br/>    | <span data-ttu-id="17907-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="17907-112">CDATA</span></span><br/> | <span data-ttu-id="17907-113">Ja</span><span class="sxs-lookup"><span data-stu-id="17907-113">Yes</span></span><br/> | <span data-ttu-id="17907-114">Der Name oder die GUID des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="17907-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="17907-115">**level**</span><span class="sxs-lookup"><span data-stu-id="17907-115">**level**</span></span><br/> | <span data-ttu-id="17907-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="17907-116">CDATA</span></span><br/> | <span data-ttu-id="17907-117">Ja</span><span class="sxs-lookup"><span data-stu-id="17907-117">Yes</span></span><br/> | <span data-ttu-id="17907-118">Die Ablaufverfolgungsebene.</span><span class="sxs-lookup"><span data-stu-id="17907-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="17907-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17907-119">Child elements</span></span>



| <span data-ttu-id="17907-120">Element</span><span class="sxs-lookup"><span data-stu-id="17907-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="17907-121">**Schlüsselwort**</span><span class="sxs-lookup"><span data-stu-id="17907-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="17907-122">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="17907-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="17907-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17907-123">Parent elements</span></span>



| <span data-ttu-id="17907-124">Element</span><span class="sxs-lookup"><span data-stu-id="17907-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="17907-125">**providers**</span><span class="sxs-lookup"><span data-stu-id="17907-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="17907-126">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="17907-126">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="17907-127">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="17907-127">Can be empty</span></span> | <span data-ttu-id="17907-128">Nein</span><span class="sxs-lookup"><span data-stu-id="17907-128">No</span></span>  |



## <a name="see-also"></a><span data-ttu-id="17907-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="17907-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17907-130">MF-Ablauf Verfolgungs Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="17907-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




