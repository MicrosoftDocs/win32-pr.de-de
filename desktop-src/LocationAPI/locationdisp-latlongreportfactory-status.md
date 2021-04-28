---
description: 'LocationDisp.LatLongReportFactory.Status-Eigenschaft: Der aktuelle Berichtsstatus.'
ms.assetid: bcdf76b5-88c4-481a-89ac-2b9558cecfc0
title: LocationDisp.LatLongReportFactory.Status-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 37e66c3f289f5376b31ffe516f45d79f2fef51e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088898"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a><span data-ttu-id="b9f8f-103">LocationDisp.LatLongReportFactory.Status-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b9f8f-103">LocationDisp.LatLongReportFactory.Status property</span></span>

<span data-ttu-id="b9f8f-104">\[Das Objektmodell der Standort-API ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b9f8f-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b9f8f-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b9f8f-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b9f8f-106">Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b9f8f-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="b9f8f-107">Verwenden Sie die [**Windows.Devices.Geolocation-API,**](/uwp/api/Windows.Devices.Geolocation) um von einer Desktopanwendung aus auf den Standort zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="b9f8f-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="b9f8f-108">Der aktuelle Berichtsstatus.</span><span class="sxs-lookup"><span data-stu-id="b9f8f-108">The current report status.</span></span>

<span data-ttu-id="b9f8f-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b9f8f-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9f8f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9f8f-110">Syntax</span></span>


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="b9f8f-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b9f8f-111">Property value</span></span>

<span data-ttu-id="b9f8f-112">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (unsigned long).</span><span class="sxs-lookup"><span data-stu-id="b9f8f-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="b9f8f-113">Status</span><span class="sxs-lookup"><span data-stu-id="b9f8f-113">Status</span></span>                                                                                               | <span data-ttu-id="b9f8f-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b9f8f-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="b9f8f-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f8f-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="b9f8f-116">Bericht wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9f8f-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="b9f8f-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f8f-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="b9f8f-118">Fehler.</span><span class="sxs-lookup"><span data-stu-id="b9f8f-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="b9f8f-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f8f-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="b9f8f-120">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="b9f8f-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="b9f8f-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f8f-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="b9f8f-122">Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="b9f8f-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="b9f8f-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f8f-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="b9f8f-124">Wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9f8f-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="b9f8f-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9f8f-125">Examples</span></span>

<span data-ttu-id="b9f8f-126">Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [Lauschen auf LatLong-Berichtsereignisse.](/uwp/api/Windows.Devices.Geolocation)</span><span class="sxs-lookup"><span data-stu-id="b9f8f-126">For an example of how to use this property, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9f8f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9f8f-127">Requirements</span></span>



| <span data-ttu-id="b9f8f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9f8f-128">Requirement</span></span> | <span data-ttu-id="b9f8f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b9f8f-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="b9f8f-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9f8f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b9f8f-131">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9f8f-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b9f8f-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9f8f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b9f8f-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b9f8f-133">None supported</span></span><br/>                  |



 

