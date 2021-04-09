---
description: Aktuelle Höhe in Meter. Die Höhe ist relativ zum Verweis Ellipsoid.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: LocationDisp. displatlongreport. Altitude (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Altitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2004c8df6c61fb890bf8f71fb3c2b5446d71d79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865479"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a><span data-ttu-id="e384b-104">LocationDisp. displatlongreport. Altitude (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e384b-104">LocationDisp.DispLatLongReport.Altitude property</span></span>

<span data-ttu-id="e384b-105">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e384b-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e384b-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e384b-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e384b-107">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e384b-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="e384b-108">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="e384b-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="e384b-109">Aktuelle Höhe in Meter.</span><span class="sxs-lookup"><span data-stu-id="e384b-109">Current altitude, in meters.</span></span> <span data-ttu-id="e384b-110">Die Höhe ist relativ zum Verweis Ellipsoid.</span><span class="sxs-lookup"><span data-stu-id="e384b-110">Altitude is relative to the reference ellipsoid.</span></span>

<span data-ttu-id="e384b-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e384b-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e384b-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="e384b-112">Syntax</span></span>


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a><span data-ttu-id="e384b-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e384b-113">Property value</span></span>

<span data-ttu-id="e384b-114">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (Gleit Komma Wert mit doppelter Genauigkeit).</span><span class="sxs-lookup"><span data-stu-id="e384b-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="e384b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e384b-115">Remarks</span></span>

<span data-ttu-id="e384b-116">Location-Sensoren sind nicht erforderlich, um diese Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e384b-116">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="e384b-117">Sie sollten Ausnahmen behandeln, wenn Sie versuchen, auf diese Eigenschaft zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e384b-117">You should handle exceptions when attempting to access this property.</span></span>

<span data-ttu-id="e384b-118">Die **Höhen** Methode ruft die Höhe in Bezug auf den Verweis Ellipsoid ab, der durch die neueste Revision des World Geodetic System (WGS 84) definiert wird, anstatt die Höhe relativ zur Meeres Ebene.</span><span class="sxs-lookup"><span data-stu-id="e384b-118">The **Altitude** method retrieves the altitude relative to the reference ellipsoid that is defined by the latest revision of the World Geodetic System (WGS 84), rather than the altitude relative to sea level.</span></span>

## <a name="examples"></a><span data-ttu-id="e384b-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e384b-119">Examples</span></span>

<span data-ttu-id="e384b-120">Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [Beispiel für einen einfachen latlong-Bericht](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="e384b-120">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="e384b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e384b-121">Requirements</span></span>



| <span data-ttu-id="e384b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e384b-122">Requirement</span></span> | <span data-ttu-id="e384b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e384b-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="e384b-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e384b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e384b-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e384b-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e384b-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e384b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e384b-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e384b-127">None supported</span></span><br/>                  |



 

