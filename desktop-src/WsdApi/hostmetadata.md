---
description: Definiert die hostingmetadaten für das zu implementierende Gerät. Dieses Element wird nur für Geräte Implementierungen (Hosts) verwendet.
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: hostmetadata-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: becd6bc3eab6b1aa1d95414c6348288e0d29dbd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359536"
---
# <a name="hostmetadata-element"></a><span data-ttu-id="4f334-104">hostmetadata-Element</span><span class="sxs-lookup"><span data-stu-id="4f334-104">hostMetadata element</span></span>

<span data-ttu-id="4f334-105">Definiert die hostingmetadaten für das zu implementierende Gerät.</span><span class="sxs-lookup"><span data-stu-id="4f334-105">Defines the hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="4f334-106">Dieses Element wird nur für Geräte Implementierungen (Hosts) verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f334-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="4f334-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="4f334-107">Usage</span></span>

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a><span data-ttu-id="4f334-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4f334-108">Attributes</span></span>

<span data-ttu-id="4f334-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="4f334-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4f334-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f334-110">Child elements</span></span>



| <span data-ttu-id="4f334-111">Element</span><span class="sxs-lookup"><span data-stu-id="4f334-111">Element</span></span>                             | <span data-ttu-id="4f334-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f334-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f334-113">**Host**</span><span class="sxs-lookup"><span data-stu-id="4f334-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="4f334-114">Definiert die serviceid-und [**types**](types.md) -Elemente für den Dienst Host.</span><span class="sxs-lookup"><span data-stu-id="4f334-114">Defines the ServiceID and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="4f334-115">Wenn Sie nicht explizit bereitgestellt werden, stellt WSDAPI keine Standarddaten als Antwort auf Metadatenanforderungen bereit.</span><span class="sxs-lookup"><span data-stu-id="4f334-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                                          |
| [<span data-ttu-id="4f334-116">**gehostet**</span><span class="sxs-lookup"><span data-stu-id="4f334-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="4f334-117">Definiert die [**serviceid**](serviceid.md) -und [**types**](types.md) -Elemente für die Dienste, die von diesem Dienst Host bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4f334-117">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="4f334-118">Jeder von diesem Dienst Host bereitgestellte Dienst sollte über eigene [**gehostete**](hosted.md) Element Informationen verfügen, um sicherzustellen, dass der Dienst in Antworten auf Metadatenanforderungen ordnungsgemäß veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="4f334-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="4f334-119">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="4f334-119">Child element sequence</span></span>

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a><span data-ttu-id="4f334-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f334-120">Parent elements</span></span>



| <span data-ttu-id="4f334-121">Element</span><span class="sxs-lookup"><span data-stu-id="4f334-121">Element</span></span>                                                         | <span data-ttu-id="4f334-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f334-122">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="4f334-123">**relationshipmetadata**</span><span class="sxs-lookup"><span data-stu-id="4f334-123">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="4f334-124">Beschreibt den Host und die gehosteten Metadaten für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="4f334-124">Describes the host and hosted metadata for the device.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4f334-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f334-125">Remarks</span></span>

<span data-ttu-id="4f334-126">Die hostingmetadaten werden in diesem Element in einem Formular angezeigt, das dem im Geräte Profil angegebenen Formular ähnelt.</span><span class="sxs-lookup"><span data-stu-id="4f334-126">The hosting metadata appears in this element in a form similar to the one specified in the device profile.</span></span> <span data-ttu-id="4f334-127">**hostmetadata** unterscheiden sich geringfügig von dem im Geräte Profil beschriebenen Format, dass die einzige unterstützte Verweis Eigenschaft die Dienst-ID ist.</span><span class="sxs-lookup"><span data-stu-id="4f334-127">**hostMetadata** is slightly different from the format described in the device profile in that the only reference property it supports is the service ID.</span></span>

<span data-ttu-id="4f334-128">Anschließend wird das [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) -Element verwendet, um eine C-Konstante zu generieren, die diese Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="4f334-128">The [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) element is used subsequently to generate a C constant containing this information.</span></span>

## <a name="element-information"></a><span data-ttu-id="4f334-129">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4f334-129">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="4f334-130">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="4f334-130">Minimum supported system</span></span><br/> | <span data-ttu-id="4f334-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f334-131">Windows Vista</span></span> |
| <span data-ttu-id="4f334-132">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="4f334-132">Can be empty</span></span>                        | <span data-ttu-id="4f334-133">Nein</span><span class="sxs-lookup"><span data-stu-id="4f334-133">No</span></span>            |



 

 




