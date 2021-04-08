---
description: Fordert Berichts Ereignisse mit breiten-/Längen Grad an.
ms.assetid: c26a388b-e042-43da-a220-e3ecfcbd03a8
title: LocationDisp. latlongreportfactory. listenforreports-Methode (locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 7e822595339fa499aaf469336ca3580acb2815bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757338"
---
# <a name="locationdisplatlongreportfactorylistenforreports-method"></a><span data-ttu-id="45914-103">LocationDisp. latlongreportfactory. listenforreports-Methode</span><span class="sxs-lookup"><span data-stu-id="45914-103">LocationDisp.LatLongReportFactory.ListenForReports method</span></span>

<span data-ttu-id="45914-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="45914-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="45914-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="45914-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="45914-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="45914-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="45914-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="45914-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="45914-108">Fordert Berichts Ereignisse mit breiten-/Längen Grad an.</span><span class="sxs-lookup"><span data-stu-id="45914-108">Requests latitude/longitude report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="45914-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="45914-109">Syntax</span></span>


```JScript
LocationDisp.LatLongReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a><span data-ttu-id="45914-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="45914-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45914-111">*requestedreportinterval*</span><span class="sxs-lookup"><span data-stu-id="45914-111">*requestedReportInterval*</span></span> 
</dt> <dd> <span data-ttu-id="45914-112">Number (**doppeltes Wort**), das die angeforderte Zeit zwischen Breiten-/Längengrad-Berichts Ereignissen in Millisekunden darstellt.</span><span class="sxs-lookup"><span data-stu-id="45914-112">Number (**double word**) representing the requested time between latitude/longitude report events, in milliseconds.</span></span> <span data-ttu-id="45914-113">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="45914-113">See Remarks.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45914-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45914-114">Return value</span></span>

<span data-ttu-id="45914-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="45914-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45914-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45914-116">Remarks</span></span>

<span data-ttu-id="45914-117">Es ist nicht erforderlich, dass der standortanbieter Berichte in dem von Ihnen angeforderten Intervall bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="45914-117">The location provider is not required to provide reports at the interval that you request.</span></span> <span data-ttu-id="45914-118">Lesen Sie den Wert der [**reportinterval**](locationdisp-latlongreportfactory-reportinterval.md) -Eigenschaft, um die Einstellung für das tatsächliche Berichts Intervall zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="45914-118">Read the value of the [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) property to discover the true report interval setting.</span></span>

## <a name="examples"></a><span data-ttu-id="45914-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45914-119">Examples</span></span>

<span data-ttu-id="45914-120">Ein Beispiel für die Verwendung dieser Methode finden Sie unter [lauschen auf latlong-Bericht Ereignisse](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="45914-120">For an example of how to use this method, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="45914-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45914-121">Requirements</span></span>



| <span data-ttu-id="45914-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45914-122">Requirement</span></span> | <span data-ttu-id="45914-123">Wert</span><span class="sxs-lookup"><span data-stu-id="45914-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="45914-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45914-124">Minimum supported client</span></span><br/> | <span data-ttu-id="45914-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45914-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="45914-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45914-126">Minimum supported server</span></span><br/> | <span data-ttu-id="45914-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="45914-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="45914-128">Header</span><span class="sxs-lookup"><span data-stu-id="45914-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="45914-129"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="45914-129"><dt>Locationapi.h</dt></span></span> </dl> |



 

