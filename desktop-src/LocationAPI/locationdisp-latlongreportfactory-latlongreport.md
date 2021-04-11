---
description: Der aktuelle Breiten-/Längengrad Bericht.
ms.assetid: d2bb305f-911e-46f7-abde-56e9fba9182b
title: LocationDisp. latlongreportfactory. latlongreport-Eigenschaft (locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.LatLongReport
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: c44582c01685431e9b5dfa4820735728dd2a9cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216382"
---
# <a name="locationdisplatlongreportfactorylatlongreport-property"></a><span data-ttu-id="223f3-103">LocationDisp. latlongreportfactory. latlongreport (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="223f3-103">LocationDisp.LatLongReportFactory.LatLongReport property</span></span>

<span data-ttu-id="223f3-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="223f3-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="223f3-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="223f3-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="223f3-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="223f3-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="223f3-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="223f3-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="223f3-108">Der aktuelle Breiten-/Längengrad Bericht.</span><span class="sxs-lookup"><span data-stu-id="223f3-108">The current latitude/longitude report.</span></span>

<span data-ttu-id="223f3-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="223f3-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="223f3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="223f3-110">Syntax</span></span>


```JScript
objLatLongReport = LocationDisp.LatLongReportFactory.LatLongReport
```



## <a name="property-value"></a><span data-ttu-id="223f3-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="223f3-111">Property value</span></span>

<span data-ttu-id="223f3-112">Diese Eigenschaft ist eine schreibgeschützte [**LocationDisp. displatlongreport**](locationdisp-displatlongreport.md).</span><span class="sxs-lookup"><span data-stu-id="223f3-112">This property is a read-only [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).</span></span>

## <a name="examples"></a><span data-ttu-id="223f3-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="223f3-113">Examples</span></span>

<span data-ttu-id="223f3-114">Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [Beispiel für einen einfachen latlong-Bericht](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="223f3-114">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="223f3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="223f3-115">Requirements</span></span>



| <span data-ttu-id="223f3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="223f3-116">Requirement</span></span> | <span data-ttu-id="223f3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="223f3-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="223f3-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="223f3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="223f3-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="223f3-119">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="223f3-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="223f3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="223f3-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="223f3-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="223f3-122">Header</span><span class="sxs-lookup"><span data-stu-id="223f3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="223f3-123"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="223f3-123"><dt>Locationapi.h</dt></span></span> </dl> |



 

