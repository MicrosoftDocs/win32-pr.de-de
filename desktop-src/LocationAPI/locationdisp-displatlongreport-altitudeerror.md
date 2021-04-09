---
description: Höhen Fehler in Meter.
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: LocationDisp. displatlongreport. altitudeerror (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.AltitudeError
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92fd71b133912a57e6ed4ef034dda6fe92ef9b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866372"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a><span data-ttu-id="fd9a1-103">LocationDisp. displatlongreport. altitudeerror (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fd9a1-103">LocationDisp.DispLatLongReport.AltitudeError property</span></span>

<span data-ttu-id="fd9a1-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="fd9a1-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fd9a1-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="fd9a1-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="fd9a1-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="fd9a1-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="fd9a1-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="fd9a1-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="fd9a1-108">Höhen Fehler in Meter.</span><span class="sxs-lookup"><span data-stu-id="fd9a1-108">Altitude error, in meters.</span></span>

<span data-ttu-id="fd9a1-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fd9a1-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9a1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd9a1-110">Syntax</span></span>


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a><span data-ttu-id="fd9a1-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fd9a1-111">Property value</span></span>

<span data-ttu-id="fd9a1-112">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (Gleit Komma Wert mit doppelter Genauigkeit).</span><span class="sxs-lookup"><span data-stu-id="fd9a1-112">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd9a1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd9a1-113">Remarks</span></span>

<span data-ttu-id="fd9a1-114">Location-Sensoren sind nicht erforderlich, um diese Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fd9a1-114">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="fd9a1-115">Sie sollten Ausnahmen behandeln, wenn Sie versuchen, auf diese Eigenschaft zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="fd9a1-115">You should handle exceptions when attempting to access this property.</span></span>

## <a name="examples"></a><span data-ttu-id="fd9a1-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd9a1-116">Examples</span></span>

<span data-ttu-id="fd9a1-117">Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [Beispiel für einen einfachen latlong-Bericht](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="fd9a1-117">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd9a1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd9a1-118">Requirements</span></span>



| <span data-ttu-id="fd9a1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd9a1-119">Requirement</span></span> | <span data-ttu-id="fd9a1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="fd9a1-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="fd9a1-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd9a1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fd9a1-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd9a1-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fd9a1-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd9a1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fd9a1-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd9a1-124">None supported</span></span><br/>                  |



 

