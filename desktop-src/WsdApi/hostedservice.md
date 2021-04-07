---
description: Definiert einen Dienst, der in einer Host Generatorfunktion gehostet werden soll.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: tustedservice-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfcf2f4c67cadf90279221fd5bdfd518e285e844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863991"
---
# <a name="hostedservice-element"></a><span data-ttu-id="29585-103">tustedservice-Element</span><span class="sxs-lookup"><span data-stu-id="29585-103">hostedService element</span></span>

<span data-ttu-id="29585-104">Definiert einen Dienst, der in einer Host Generatorfunktion gehostet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29585-104">Defines a service to be hosted in a host builder function.</span></span>

## <a name="usage"></a><span data-ttu-id="29585-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="29585-105">Usage</span></span>

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a><span data-ttu-id="29585-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="29585-106">Attributes</span></span>

<span data-ttu-id="29585-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="29585-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="29585-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="29585-108">Child elements</span></span>



| <span data-ttu-id="29585-109">Element</span><span class="sxs-lookup"><span data-stu-id="29585-109">Element</span></span>                                     | <span data-ttu-id="29585-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29585-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29585-111">**codeName**</span><span class="sxs-lookup"><span data-stu-id="29585-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="29585-112">Gibt den Namen an, der für den Porttyp im generierten Code verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29585-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="29585-113">Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.</span><span class="sxs-lookup"><span data-stu-id="29585-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="29585-114">**PortType**</span><span class="sxs-lookup"><span data-stu-id="29585-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="29585-115">Der Porttyp, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="29585-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                                       |
| [<span data-ttu-id="29585-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="29585-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="29585-117">Der Klassenname, der aus der Generatorfunktion generiert wird.</span><span class="sxs-lookup"><span data-stu-id="29585-117">Class name to generate from builder function.</span></span><br/> <br/>                                                                                                      |
| [<span data-ttu-id="29585-118">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="29585-118">**ServiceID**</span></span>](serviceid.md)<br/>   | <span data-ttu-id="29585-119">Ein URI, der den Dienst Bezeichner darstellt.</span><span class="sxs-lookup"><span data-stu-id="29585-119">A URI that represents the service identifier.</span></span><br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="29585-120">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="29585-120">Child element sequence</span></span>

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a><span data-ttu-id="29585-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="29585-121">Parent elements</span></span>



| <span data-ttu-id="29585-122">Element</span><span class="sxs-lookup"><span data-stu-id="29585-122">Element</span></span>                         | <span data-ttu-id="29585-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29585-123">Description</span></span>                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="29585-124">**Datei**</span><span class="sxs-lookup"><span data-stu-id="29585-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="29585-125">Die Ausgabedatei Spezifikation für den Code-Generator.</span><span class="sxs-lookup"><span data-stu-id="29585-125">The output file specification for the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="29585-126">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="29585-126">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="29585-127">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="29585-127">Minimum supported system</span></span><br/> | <span data-ttu-id="29585-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29585-128">Windows Vista</span></span> |
| <span data-ttu-id="29585-129">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="29585-129">Can be empty</span></span>                        | <span data-ttu-id="29585-130">Nein</span><span class="sxs-lookup"><span data-stu-id="29585-130">No</span></span>            |



 

 




