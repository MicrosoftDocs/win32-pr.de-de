---
description: Ein URI, der den Dienst Bezeichner darstellt.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Serviceid-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e97250b0b33d276dced4b5d454aec9298387c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351094"
---
# <a name="serviceid-element"></a><span data-ttu-id="a766b-103">Serviceid-Element</span><span class="sxs-lookup"><span data-stu-id="a766b-103">ServiceID element</span></span>

<span data-ttu-id="a766b-104">Ein URI, der den Dienst Bezeichner darstellt.</span><span class="sxs-lookup"><span data-stu-id="a766b-104">A URI that represents the service identifier.</span></span>

## <a name="usage"></a><span data-ttu-id="a766b-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="a766b-105">Usage</span></span>

``` syntax
<ServiceID/>
```

## <a name="attributes"></a><span data-ttu-id="a766b-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="a766b-106">Attributes</span></span>

<span data-ttu-id="a766b-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="a766b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a766b-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a766b-108">Child elements</span></span>

<span data-ttu-id="a766b-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="a766b-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a766b-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a766b-110">Parent elements</span></span>



| <span data-ttu-id="a766b-111">Element</span><span class="sxs-lookup"><span data-stu-id="a766b-111">Element</span></span>                             | <span data-ttu-id="a766b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a766b-112">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a766b-113">**Host**</span><span class="sxs-lookup"><span data-stu-id="a766b-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="a766b-114">Definiert die **serviceid** -und [**types**](types.md) -Elemente für den Dienst Host.</span><span class="sxs-lookup"><span data-stu-id="a766b-114">Defines the **ServiceID** and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="a766b-115">Wenn Sie nicht explizit bereitgestellt werden, stellt WSDAPI keine Standarddaten als Antwort auf Metadatenanforderungen bereit.</span><span class="sxs-lookup"><span data-stu-id="a766b-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                     |
| [<span data-ttu-id="a766b-116">**gehostet**</span><span class="sxs-lookup"><span data-stu-id="a766b-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="a766b-117">Definiert die **serviceid** -und [**types**](types.md) -Elemente für die Dienste, die von diesem Dienst Host bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a766b-117">Defines the **ServiceID** and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="a766b-118">Jeder von diesem Dienst Host bereitgestellte Dienst sollte über eigene [**gehostete**](hosted.md) Element Informationen verfügen, um sicherzustellen, dass der Dienst in Antworten auf Metadatenanforderungen ordnungsgemäß veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="a766b-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="a766b-119">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a766b-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="a766b-120">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="a766b-120">Minimum supported system</span></span><br/> | <span data-ttu-id="a766b-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a766b-121">Windows Vista</span></span> |
| <span data-ttu-id="a766b-122">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="a766b-122">Can be empty</span></span>                        | <span data-ttu-id="a766b-123">Ja</span><span class="sxs-lookup"><span data-stu-id="a766b-123">Yes</span></span>           |



 

 




