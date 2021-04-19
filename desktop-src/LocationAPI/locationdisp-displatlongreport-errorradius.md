---
description: Eine Entfernung vom gemeldeten Speicherort in Meter. In Kombination mit dem gemeldeten Speicherort als Ursprung beschreibt dieser RADIUS den Kreis, in dem sich der tatsächliche Speicherort wahrscheinlich befindet.
ms.assetid: a9565bd5-d1e0-45f8-abeb-3191b16480fa
title: LocationDisp. displatlongreport. errorradius-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.ErrorRadius
api_type:
- COM
api_location: ''
ms.openlocfilehash: f99ff9b03451738158a98541bfae0e67a8827717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362286"
---
# <a name="locationdispdisplatlongreporterrorradius-property"></a><span data-ttu-id="02cd4-104">LocationDisp. displatlongreport. errorradius-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="02cd4-104">LocationDisp.DispLatLongReport.ErrorRadius property</span></span>

<span data-ttu-id="02cd4-105">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="02cd4-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="02cd4-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="02cd4-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="02cd4-107">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="02cd4-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="02cd4-108">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="02cd4-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="02cd4-109">Eine Entfernung vom gemeldeten Speicherort in Meter.</span><span class="sxs-lookup"><span data-stu-id="02cd4-109">A distance from the reported location, in meters.</span></span> <span data-ttu-id="02cd4-110">In Kombination mit dem gemeldeten Speicherort als Ursprung beschreibt dieser RADIUS den Kreis, in dem sich der tatsächliche Speicherort wahrscheinlich befindet.</span><span class="sxs-lookup"><span data-stu-id="02cd4-110">Combined with the reported location as the origin, this radius describes the circle in which the actual location is probably located.</span></span>

<span data-ttu-id="02cd4-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="02cd4-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="02cd4-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="02cd4-112">Syntax</span></span>


```JScript
ErrorRadius = LocationDisp.DispLatLongReport.ErrorRadius
```



## <a name="property-value"></a><span data-ttu-id="02cd4-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="02cd4-113">Property value</span></span>

<span data-ttu-id="02cd4-114">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (Gleit Komma Wert mit doppelter Genauigkeit).</span><span class="sxs-lookup"><span data-stu-id="02cd4-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="02cd4-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02cd4-115">Examples</span></span>

<span data-ttu-id="02cd4-116">Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [Beispiel für einen einfachen latlong-Bericht](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="02cd4-116">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="02cd4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02cd4-117">Requirements</span></span>



| <span data-ttu-id="02cd4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02cd4-118">Requirement</span></span> | <span data-ttu-id="02cd4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="02cd4-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="02cd4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02cd4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="02cd4-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02cd4-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="02cd4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02cd4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="02cd4-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="02cd4-123">None supported</span></span><br/>                  |



 

