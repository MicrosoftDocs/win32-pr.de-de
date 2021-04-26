---
description: Definiert die Hostingmetadaten für das zu implementierende Gerät. Dieses Element wird nur für Geräteimplementierungen (Hosts) verwendet.
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: hostMetadata-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9cf6fa139a2723ed90dfe281fc7b054016386fa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994797"
---
# <a name="hostmetadata-element"></a><span data-ttu-id="8b1f1-104">hostMetadata-Element</span><span class="sxs-lookup"><span data-stu-id="8b1f1-104">hostMetadata element</span></span>

<span data-ttu-id="8b1f1-105">Definiert die Hostingmetadaten für das zu implementierende Gerät.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-105">Defines the hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="8b1f1-106">Dieses Element wird nur für Geräteimplementierungen (Hosts) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="8b1f1-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="8b1f1-107">Usage</span></span>

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a><span data-ttu-id="8b1f1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8b1f1-108">Attributes</span></span>

<span data-ttu-id="8b1f1-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8b1f1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b1f1-110">Child elements</span></span>



| <span data-ttu-id="8b1f1-111">Element</span><span class="sxs-lookup"><span data-stu-id="8b1f1-111">Element</span></span>                             | <span data-ttu-id="8b1f1-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b1f1-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b1f1-113">**Host**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="8b1f1-114">Definiert die Elemente ServiceID und [**Types**](types.md) für den Diensthost.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-114">Defines the ServiceID and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="8b1f1-115">Wenn sie nicht explizit angegeben wird, stellt WSDAPI als Reaktion auf Metadatenanforderungen keine Standarddaten bereit.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                                          |
| [<span data-ttu-id="8b1f1-116">**Gehostet**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="8b1f1-117">Definiert die [**Elemente ServiceID**](serviceid.md) und [**Types**](types.md) für die von diesem Diensthost bereitgestellten Dienste.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-117">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="8b1f1-118">Jeder von diesem Diensthost bereitgestellte Dienst sollte über eigene [**Gehostete**](hosted.md) Elementinformationen verfügen, um sicherzustellen, dass der Dienst ordnungsgemäß als Antwort auf Metadatenanforderungen veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="8b1f1-119">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="8b1f1-119">Child element sequence</span></span>

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a><span data-ttu-id="8b1f1-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b1f1-120">Parent elements</span></span>



| <span data-ttu-id="8b1f1-121">Element</span><span class="sxs-lookup"><span data-stu-id="8b1f1-121">Element</span></span>                                                         | <span data-ttu-id="8b1f1-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b1f1-122">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="8b1f1-123">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-123">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="8b1f1-124">Beschreibt die Host- und gehosteten Metadaten für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-124">Describes the host and hosted metadata for the device.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8b1f1-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b1f1-125">Remarks</span></span>

<span data-ttu-id="8b1f1-126">Die Hostingmetadaten werden in diesem Element in einer Form angezeigt, die der im Geräteprofil angegebenen ähnelt.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-126">The hosting metadata appears in this element in a form similar to the one specified in the device profile.</span></span> <span data-ttu-id="8b1f1-127">**hostMetadata** unterscheidet sich geringfügig vom im Geräteprofil beschriebenen Format, da die einzige referenz-Eigenschaft, die sie unterstützt, die Dienst-ID ist.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-127">**hostMetadata** is slightly different from the format described in the device profile in that the only reference property it supports is the service ID.</span></span>

<span data-ttu-id="8b1f1-128">Das [**relationshipMetadataDefinition-Element**](relationshipmetadatadefinition.md) wird anschließend verwendet, um eine C-Konstante zu generieren, die diese Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-128">The [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) element is used subsequently to generate a C constant containing this information.</span></span>

## <a name="element-information"></a><span data-ttu-id="8b1f1-129">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8b1f1-129">Element information</span></span>



| <span data-ttu-id="8b1f1-130">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="8b1f1-130">Label</span></span> | <span data-ttu-id="8b1f1-131">Wert</span><span class="sxs-lookup"><span data-stu-id="8b1f1-131">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8b1f1-132">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="8b1f1-132">Minimum supported system</span></span><br/> | <span data-ttu-id="8b1f1-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b1f1-133">Windows Vista</span></span> |
| <span data-ttu-id="8b1f1-134">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="8b1f1-134">Can be empty</span></span>                        | <span data-ttu-id="8b1f1-135">Nein</span><span class="sxs-lookup"><span data-stu-id="8b1f1-135">No</span></span>            |



 

 




