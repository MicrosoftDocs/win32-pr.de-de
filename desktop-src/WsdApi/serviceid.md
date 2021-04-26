---
description: Ein URI, der den Dienstbezeichner darstellt.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: ServiceID-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c8b02fa8ecfa936aa658a1f18242e4f14eb0dd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995107"
---
# <a name="serviceid-element"></a><span data-ttu-id="b443c-103">ServiceID-Element</span><span class="sxs-lookup"><span data-stu-id="b443c-103">ServiceID element</span></span>

<span data-ttu-id="b443c-104">Ein URI, der den Dienstbezeichner darstellt.</span><span class="sxs-lookup"><span data-stu-id="b443c-104">A URI that represents the service identifier.</span></span>

## <a name="usage"></a><span data-ttu-id="b443c-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="b443c-105">Usage</span></span>

``` syntax
<ServiceID/>
```

## <a name="attributes"></a><span data-ttu-id="b443c-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="b443c-106">Attributes</span></span>

<span data-ttu-id="b443c-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="b443c-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b443c-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b443c-108">Child elements</span></span>

<span data-ttu-id="b443c-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="b443c-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b443c-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b443c-110">Parent elements</span></span>



| <span data-ttu-id="b443c-111">Element</span><span class="sxs-lookup"><span data-stu-id="b443c-111">Element</span></span>                             | <span data-ttu-id="b443c-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b443c-112">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b443c-113">**Host**</span><span class="sxs-lookup"><span data-stu-id="b443c-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="b443c-114">Definiert die **Elemente ServiceID** und [**Types**](types.md) für den Diensthost.</span><span class="sxs-lookup"><span data-stu-id="b443c-114">Defines the **ServiceID** and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="b443c-115">Wenn sie nicht explizit angegeben wird, stellt WSDAPI als Reaktion auf Metadatenanforderungen keine Standarddaten bereit.</span><span class="sxs-lookup"><span data-stu-id="b443c-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                     |
| [<span data-ttu-id="b443c-116">**Gehostet**</span><span class="sxs-lookup"><span data-stu-id="b443c-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="b443c-117">Definiert die **Elemente ServiceID** und [**Types**](types.md) für die von diesem Diensthost bereitgestellten Dienste.</span><span class="sxs-lookup"><span data-stu-id="b443c-117">Defines the **ServiceID** and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="b443c-118">Jeder von diesem Diensthost bereitgestellte Dienst sollte über eigene Informationen zu [**gehosteten**](hosted.md) Elementen verfügen, um sicherzustellen, dass der Dienst ordnungsgemäß als Antwort auf Metadatenanforderungen veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="b443c-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="b443c-119">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b443c-119">Element information</span></span>



| <span data-ttu-id="b443c-120">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="b443c-120">Label</span></span> | <span data-ttu-id="b443c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b443c-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b443c-122">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="b443c-122">Minimum supported system</span></span><br/> | <span data-ttu-id="b443c-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b443c-123">Windows Vista</span></span> |
| <span data-ttu-id="b443c-124">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="b443c-124">Can be empty</span></span>                        | <span data-ttu-id="b443c-125">Ja</span><span class="sxs-lookup"><span data-stu-id="b443c-125">Yes</span></span>           |



 

 




