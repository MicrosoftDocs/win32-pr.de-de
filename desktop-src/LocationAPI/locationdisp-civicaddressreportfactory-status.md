---
description: 'LocationDisp.CivicAddressReportFactory.Status-Eigenschaft: Der aktuelle Berichtsstatus.'
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: LocationDisp.CivicAddressReportFactory.Status (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: acb5bcfa589139e2c69e75124253f9d9a7b53a87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118498"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a><span data-ttu-id="f4207-103">LocationDisp.CivicAddressReportFactory.Status (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f4207-103">LocationDisp.CivicAddressReportFactory.Status property</span></span>

<span data-ttu-id="f4207-104">\[Das Location-API-Objektmodell steht für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f4207-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f4207-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f4207-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f4207-106">Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f4207-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="f4207-107">Verwenden Sie die [**Windows.Devices.Geolocation-API,**](/uwp/api/Windows.Devices.Geolocation) um über eine Desktopanwendung auf den Standort zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="f4207-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="f4207-108">Der aktuelle Berichtsstatus.</span><span class="sxs-lookup"><span data-stu-id="f4207-108">The current report status.</span></span>

<span data-ttu-id="f4207-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f4207-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4207-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4207-110">Syntax</span></span>


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="f4207-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f4207-111">Property value</span></span>

<span data-ttu-id="f4207-112">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (unsigned long).</span><span class="sxs-lookup"><span data-stu-id="f4207-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="f4207-113">Status</span><span class="sxs-lookup"><span data-stu-id="f4207-113">Status</span></span>                                                                                               | <span data-ttu-id="f4207-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f4207-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="f4207-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="f4207-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="f4207-116">Bericht wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f4207-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="f4207-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f4207-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f4207-118">Fehler.</span><span class="sxs-lookup"><span data-stu-id="f4207-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="f4207-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f4207-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f4207-120">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="f4207-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="f4207-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="f4207-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f4207-122">Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="f4207-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="f4207-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="f4207-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f4207-124">Wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4207-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="f4207-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4207-125">Examples</span></span>

<span data-ttu-id="f4207-126">Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="f4207-126">For an example of how to use this property, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4207-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4207-127">Requirements</span></span>



| <span data-ttu-id="f4207-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4207-128">Requirement</span></span> | <span data-ttu-id="f4207-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f4207-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="f4207-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4207-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f4207-131">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4207-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f4207-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4207-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f4207-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f4207-133">None supported</span></span><br/>                  |



 

