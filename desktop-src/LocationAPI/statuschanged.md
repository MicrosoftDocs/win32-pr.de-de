---
description: Tritt auf, wenn sich der Betriebsstatus eines Berichts ändert.
ms.assetid: f0c4e678-1666-4f99-89de-85879eacd0ac
title: Statuschangi-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StatusChanged
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1bda6645002f586eda0e2dad99a134450329d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218853"
---
# <a name="statuschanged-event"></a><span data-ttu-id="27384-103">Statuschangi-Ereignis</span><span class="sxs-lookup"><span data-stu-id="27384-103">StatusChanged event</span></span>

<span data-ttu-id="27384-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="27384-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="27384-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="27384-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="27384-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="27384-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="27384-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="27384-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="27384-108">Tritt auf, wenn sich der Betriebsstatus eines Berichts ändert.</span><span class="sxs-lookup"><span data-stu-id="27384-108">Occurs when the operational status of a report changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="27384-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="27384-109">Syntax</span></span>


```JScript
.StatusChanged(
  status
)
```



## <a name="parameters"></a><span data-ttu-id="27384-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="27384-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27384-111">*status*</span><span class="sxs-lookup"><span data-stu-id="27384-111">*status*</span></span> 
</dt> <dd>

<span data-ttu-id="27384-112">Der neue Status.</span><span class="sxs-lookup"><span data-stu-id="27384-112">The new status.</span></span>



| <span data-ttu-id="27384-113">Status</span><span class="sxs-lookup"><span data-stu-id="27384-113">Status</span></span>                                                                                               | <span data-ttu-id="27384-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="27384-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="27384-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="27384-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="27384-116">Der Bericht wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27384-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="27384-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="27384-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="27384-118">Fehler.</span><span class="sxs-lookup"><span data-stu-id="27384-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="27384-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="27384-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="27384-120">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="27384-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="27384-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="27384-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="27384-122">Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="27384-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="27384-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="27384-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="27384-124">Wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27384-124">Running.</span></span><br/>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27384-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27384-125">Return value</span></span>

<span data-ttu-id="27384-126">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="27384-126">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="27384-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27384-127">Remarks</span></span>

<span data-ttu-id="27384-128">Sie sollten separate berichtsänderungsberichtlerhandler für Berichte zu öffentlichen Adressen und breiten-/Längen Grad implementieren.</span><span class="sxs-lookup"><span data-stu-id="27384-128">You should implement separate status change report handlers for civic address reports and latitude/longitude reports.</span></span>

## <a name="examples"></a><span data-ttu-id="27384-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27384-129">Examples</span></span>

<span data-ttu-id="27384-130">Ein Beispiel für die Verwendung dieses Ereignisses finden Sie unter [lauschen auf latlong-Bericht Ereignisse](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="27384-130">For an example of how to use this event, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="27384-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27384-131">Requirements</span></span>



| <span data-ttu-id="27384-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27384-132">Requirement</span></span> | <span data-ttu-id="27384-133">Wert</span><span class="sxs-lookup"><span data-stu-id="27384-133">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="27384-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27384-134">Minimum supported client</span></span><br/> | <span data-ttu-id="27384-135">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27384-135">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="27384-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27384-136">Minimum supported server</span></span><br/> | <span data-ttu-id="27384-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="27384-137">None supported</span></span><br/>                  |



 

