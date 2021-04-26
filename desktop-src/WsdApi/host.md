---
description: Definiert die Elemente ServiceID und Types für den Diensthost.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: host-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f051f6665715ecaa519a060e18a3cbf4912210
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993797"
---
# <a name="host-element"></a><span data-ttu-id="d7cc4-103">host-Element</span><span class="sxs-lookup"><span data-stu-id="d7cc4-103">host element</span></span>

<span data-ttu-id="d7cc4-104">Definiert die [**Elemente ServiceID**](serviceid.md) und [**Types**](types.md) für den Diensthost.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-104">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="d7cc4-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d7cc4-105">Usage</span></span>

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a><span data-ttu-id="d7cc4-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="d7cc4-106">Attributes</span></span>

<span data-ttu-id="d7cc4-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d7cc4-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d7cc4-108">Child elements</span></span>



| <span data-ttu-id="d7cc4-109">Element</span><span class="sxs-lookup"><span data-stu-id="d7cc4-109">Element</span></span>                                   | <span data-ttu-id="d7cc4-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7cc4-110">Description</span></span>                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="d7cc4-111">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="d7cc4-111">**ServiceID**</span></span>](serviceid.md)<br/> | <span data-ttu-id="d7cc4-112">Definiert den Dienstbezeichner für den Diensthost.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-112">Defines the service identifier for the service host.</span></span><br/> <br/> |
| [<span data-ttu-id="d7cc4-113">**Typen**</span><span class="sxs-lookup"><span data-stu-id="d7cc4-113">**Types**</span></span>](types.md)<br/>         | <span data-ttu-id="d7cc4-114">Definiert eine Liste der qualifizierten XSD-Namen.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-114">Defines a list of XSD qualified names.</span></span><br/> <br/>               |



### <a name="child-element-sequence"></a><span data-ttu-id="d7cc4-115">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="d7cc4-115">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a><span data-ttu-id="d7cc4-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d7cc4-116">Parent elements</span></span>



| <span data-ttu-id="d7cc4-117">Element</span><span class="sxs-lookup"><span data-stu-id="d7cc4-117">Element</span></span>                                         | <span data-ttu-id="d7cc4-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7cc4-118">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="d7cc4-119">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="d7cc4-119">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="d7cc4-120">Die Hostingmetadaten für das zu implementierende Gerät.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-120">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="d7cc4-121">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d7cc4-121">Element information</span></span>



| <span data-ttu-id="d7cc4-122">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="d7cc4-122">Label</span></span> | <span data-ttu-id="d7cc4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d7cc4-123">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="d7cc4-124">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="d7cc4-124">Minimum supported system</span></span><br/> | <span data-ttu-id="d7cc4-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7cc4-125">Windows Vista</span></span> |
| <span data-ttu-id="d7cc4-126">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="d7cc4-126">Can be empty</span></span>                        | <span data-ttu-id="d7cc4-127">Nein</span><span class="sxs-lookup"><span data-stu-id="d7cc4-127">No</span></span>            |



 

 




