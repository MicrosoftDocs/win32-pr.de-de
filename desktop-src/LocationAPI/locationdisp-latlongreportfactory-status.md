---
description: Der aktuelle Status des Berichts.
ms.assetid: bcdf76b5-88c4-481a-89ac-2b9558cecfc0
title: LocationDisp. latlongreportfactory. Status (Eigenschaft)
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
ms.openlocfilehash: c32f1e58c5c519bdbdf797f81f11a449bfb3dc1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346029"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a><span data-ttu-id="853ca-103">LocationDisp. latlongreportfactory. Status (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="853ca-103">LocationDisp.LatLongReportFactory.Status property</span></span>

<span data-ttu-id="853ca-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="853ca-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="853ca-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="853ca-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="853ca-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="853ca-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="853ca-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="853ca-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="853ca-108">Der aktuelle Status des Berichts.</span><span class="sxs-lookup"><span data-stu-id="853ca-108">The current report status.</span></span>

<span data-ttu-id="853ca-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="853ca-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="853ca-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="853ca-110">Syntax</span></span>


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="853ca-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="853ca-111">Property value</span></span>

<span data-ttu-id="853ca-112">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (unsigned long).</span><span class="sxs-lookup"><span data-stu-id="853ca-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="853ca-113">Status</span><span class="sxs-lookup"><span data-stu-id="853ca-113">Status</span></span>                                                                                               | <span data-ttu-id="853ca-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="853ca-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="853ca-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="853ca-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="853ca-116">Der Bericht wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="853ca-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="853ca-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="853ca-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="853ca-118">Fehler.</span><span class="sxs-lookup"><span data-stu-id="853ca-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="853ca-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="853ca-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="853ca-120">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="853ca-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="853ca-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="853ca-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="853ca-122">Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="853ca-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="853ca-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="853ca-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="853ca-124">Wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="853ca-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="853ca-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="853ca-125">Examples</span></span>

<span data-ttu-id="853ca-126">Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [lauschen auf latlong-Bericht Ereignisse](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="853ca-126">For an example of how to use this property, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="853ca-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="853ca-127">Requirements</span></span>



| <span data-ttu-id="853ca-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="853ca-128">Requirement</span></span> | <span data-ttu-id="853ca-129">Wert</span><span class="sxs-lookup"><span data-stu-id="853ca-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="853ca-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="853ca-130">Minimum supported client</span></span><br/> | <span data-ttu-id="853ca-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="853ca-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="853ca-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="853ca-132">Minimum supported server</span></span><br/> | <span data-ttu-id="853ca-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="853ca-133">None supported</span></span><br/>                  |



 

