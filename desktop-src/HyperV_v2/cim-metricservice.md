---
description: Verwaltet Metriken für verwaltete Elemente.
ms.assetid: df249d0c-960b-47d6-9590-f0fd08ddec18
title: CIM_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 41c4ab5e947fe22434e38006c5169711701915a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351716"
---
# <a name="cim_metricservice-class"></a><span data-ttu-id="cc7cb-103">CIM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="cc7cb-103">CIM\_MetricService class</span></span>

<span data-ttu-id="cc7cb-104">Verwaltet Metriken für verwaltete Elemente.</span><span class="sxs-lookup"><span data-stu-id="cc7cb-104">Manages metrics for managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc7cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc7cb-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="cc7cb-106">Member</span><span class="sxs-lookup"><span data-stu-id="cc7cb-106">Members</span></span>

<span data-ttu-id="cc7cb-107">Die **CIM \_ metricservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cc7cb-107">The **CIM\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="cc7cb-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="cc7cb-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cc7cb-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="cc7cb-109">Methods</span></span>

<span data-ttu-id="cc7cb-110">Die **CIM \_ metricservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="cc7cb-110">The **CIM\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="cc7cb-111">Methode</span><span class="sxs-lookup"><span data-stu-id="cc7cb-111">Method</span></span>                                                                   | <span data-ttu-id="cc7cb-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc7cb-112">Description</span></span>                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc7cb-113">**Controlmetrics**</span><span class="sxs-lookup"><span data-stu-id="cc7cb-113">**ControlMetrics**</span></span>](cim-metricservice-controlmetrics.md)               | <span data-ttu-id="cc7cb-114">Aktiviert und deaktiviert die Auflistung von Metriken.</span><span class="sxs-lookup"><span data-stu-id="cc7cb-114">Enables and disables the collection of metrics.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="cc7cb-115">**Controlmetricsbyclass**</span><span class="sxs-lookup"><span data-stu-id="cc7cb-115">**ControlMetricsByClass**</span></span>](cim-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="cc7cb-116">Aktiviert und deaktiviert die Auflistung von Metriken für eine Klasse.</span><span class="sxs-lookup"><span data-stu-id="cc7cb-116">Enables and disables the collection of metrics for a class.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="cc7cb-117">**Controlsampletimes**</span><span class="sxs-lookup"><span data-stu-id="cc7cb-117">**ControlSampleTimes**</span></span>](cim-metricservice-controlsampletimes.md)       | <span data-ttu-id="cc7cb-118">Gibt an, wann Metriken erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="cc7cb-118">Specifies when metrics are gathered.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="cc7cb-119">**Getmetricvalues**</span><span class="sxs-lookup"><span data-stu-id="cc7cb-119">**GetMetricValues**</span></span>](cim-metricservice-getmetricvalues.md)             | <span data-ttu-id="cc7cb-120">Ruft eine gefilterte Liste von Metrikwerten ab.</span><span class="sxs-lookup"><span data-stu-id="cc7cb-120">Retrieves a filtered list of metric values.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="cc7cb-121">**Showmetrics**</span><span class="sxs-lookup"><span data-stu-id="cc7cb-121">**ShowMetrics**</span></span>](cim-metricservice-showmetrics.md)                     | <span data-ttu-id="cc7cb-122">Gibt an, ob die metrikauflistung für die angegebenen verwalteten Elemente aktiviert ist, und gibt die Metriken an, die für jedes verwaltete Element für die Auflistung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="cc7cb-122">Indicates whether metric collection is enabled for the specified managed elements, and indicates the metrics that are available for collection for each managed element.</span></span><br/> |
| [<span data-ttu-id="cc7cb-123">**Showmetricsbyclass**</span><span class="sxs-lookup"><span data-stu-id="cc7cb-123">**ShowMetricsByClass**</span></span>](cim-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="cc7cb-124">Gibt an, welche Metriken für alle Instanzen einer CIM-Klasse für die Auflistung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="cc7cb-124">Indicates which metrics are available for collection for all instances of a CIM class.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="cc7cb-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc7cb-125">Requirements</span></span>



| <span data-ttu-id="cc7cb-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc7cb-126">Requirement</span></span> | <span data-ttu-id="cc7cb-127">Wert</span><span class="sxs-lookup"><span data-stu-id="cc7cb-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc7cb-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc7cb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cc7cb-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cc7cb-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="cc7cb-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc7cb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cc7cb-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc7cb-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="cc7cb-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc7cb-132">Namespace</span></span><br/>                | <span data-ttu-id="cc7cb-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cc7cb-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cc7cb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="cc7cb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc7cb-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cc7cb-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc7cb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cc7cb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc7cb-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cc7cb-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cc7cb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc7cb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc7cb-139">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="cc7cb-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




