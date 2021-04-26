---
description: Definiert einen Dienst, der in einer Host-Generatorfunktion gehostet werden soll.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: hostedService-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96c9f6e010989f4844d93299bb34f1ab8893236
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994787"
---
# <a name="hostedservice-element"></a><span data-ttu-id="56728-103">hostedService-Element</span><span class="sxs-lookup"><span data-stu-id="56728-103">hostedService element</span></span>

<span data-ttu-id="56728-104">Definiert einen Dienst, der in einer Host-Generatorfunktion gehostet werden soll.</span><span class="sxs-lookup"><span data-stu-id="56728-104">Defines a service to be hosted in a host builder function.</span></span>

## <a name="usage"></a><span data-ttu-id="56728-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="56728-105">Usage</span></span>

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a><span data-ttu-id="56728-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="56728-106">Attributes</span></span>

<span data-ttu-id="56728-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="56728-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="56728-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="56728-108">Child elements</span></span>



| <span data-ttu-id="56728-109">Element</span><span class="sxs-lookup"><span data-stu-id="56728-109">Element</span></span>                                     | <span data-ttu-id="56728-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56728-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56728-111">**Codename**</span><span class="sxs-lookup"><span data-stu-id="56728-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="56728-112">Gibt den Namen an, der für den Porttyp im generierten Code verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="56728-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="56728-113">Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.</span><span class="sxs-lookup"><span data-stu-id="56728-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="56728-114">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="56728-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="56728-115">Porttyp, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="56728-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                                       |
| [<span data-ttu-id="56728-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="56728-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="56728-117">Klassenname, der aus der Generatorfunktion generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="56728-117">Class name to generate from builder function.</span></span><br/> <br/>                                                                                                      |
| [<span data-ttu-id="56728-118">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="56728-118">**ServiceID**</span></span>](serviceid.md)<br/>   | <span data-ttu-id="56728-119">Ein URI, der den Dienstbezeichner darstellt.</span><span class="sxs-lookup"><span data-stu-id="56728-119">A URI that represents the service identifier.</span></span><br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="56728-120">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="56728-120">Child element sequence</span></span>

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a><span data-ttu-id="56728-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="56728-121">Parent elements</span></span>



| <span data-ttu-id="56728-122">Element</span><span class="sxs-lookup"><span data-stu-id="56728-122">Element</span></span>                         | <span data-ttu-id="56728-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56728-123">Description</span></span>                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="56728-124">**Datei**</span><span class="sxs-lookup"><span data-stu-id="56728-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="56728-125">Die Ausgabedateispezifikation für den Codegenerator.</span><span class="sxs-lookup"><span data-stu-id="56728-125">The output file specification for the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="56728-126">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="56728-126">Element information</span></span>



| <span data-ttu-id="56728-127">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="56728-127">Label</span></span> | <span data-ttu-id="56728-128">Wert</span><span class="sxs-lookup"><span data-stu-id="56728-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="56728-129">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="56728-129">Minimum supported system</span></span><br/> | <span data-ttu-id="56728-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56728-130">Windows Vista</span></span> |
| <span data-ttu-id="56728-131">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="56728-131">Can be empty</span></span>                        | <span data-ttu-id="56728-132">Nein</span><span class="sxs-lookup"><span data-stu-id="56728-132">No</span></span>            |



 

 




