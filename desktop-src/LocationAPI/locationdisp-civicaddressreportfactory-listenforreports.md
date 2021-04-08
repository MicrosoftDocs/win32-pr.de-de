---
description: Fordert Ereignisse für den Bericht "Civic Address" an
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: LocationDisp. civicaddressreportfactory. listenforreports-Methode (locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 02315f8b2f7fced76c3d0d1330df246af6bad4b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960839"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a><span data-ttu-id="e0dc9-103">LocationDisp. civicaddressreportfactory. listenforreports-Methode</span><span class="sxs-lookup"><span data-stu-id="e0dc9-103">LocationDisp.CivicAddressReportFactory.ListenForReports method</span></span>

<span data-ttu-id="e0dc9-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e0dc9-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e0dc9-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e0dc9-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e0dc9-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e0dc9-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="e0dc9-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="e0dc9-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="e0dc9-108">Fordert Ereignisse für den Bericht "Civic Address" an</span><span class="sxs-lookup"><span data-stu-id="e0dc9-108">Requests civic address report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0dc9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0dc9-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a><span data-ttu-id="e0dc9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0dc9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0dc9-111">*requestedreportinterval*</span><span class="sxs-lookup"><span data-stu-id="e0dc9-111">*requestedReportInterval*</span></span> 
</dt> <dd> <span data-ttu-id="e0dc9-112">Number (**doppeltes Wort**), das die angeforderte Zeit zwischen den Ereignissen des öffentlichen Adress Berichts (in Millisekunden) darstellt.</span><span class="sxs-lookup"><span data-stu-id="e0dc9-112">Number (**double word**) representing the requested time between civic address report events, in milliseconds.</span></span> <span data-ttu-id="e0dc9-113">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e0dc9-113">See Remarks.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0dc9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0dc9-114">Return value</span></span>

<span data-ttu-id="e0dc9-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e0dc9-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0dc9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0dc9-116">Remarks</span></span>

<span data-ttu-id="e0dc9-117">Der Speicherort Anbieter ist nicht erforderlich, um die gewünschte Genauigkeit anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e0dc9-117">The location provider is not required to provide the accuracy that you request.</span></span> <span data-ttu-id="e0dc9-118">Lesen Sie den Wert der [**reportinterval**](locationdisp-civicaddressreportfactory-reportinterval.md) -Eigenschaft, um die Einstellung für das tatsächliche Berichts Intervall zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e0dc9-118">Read the value of the [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) property to discover the true report interval setting.</span></span>

## <a name="examples"></a><span data-ttu-id="e0dc9-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0dc9-119">Examples</span></span>

<span data-ttu-id="e0dc9-120">Ein Beispiel für die Verwendung dieser Methode finden Sie unter Überwachen von [Ereignissen zu öffentlichen Adress Berichten](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="e0dc9-120">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0dc9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0dc9-121">Requirements</span></span>



| <span data-ttu-id="e0dc9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0dc9-122">Requirement</span></span> | <span data-ttu-id="e0dc9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e0dc9-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0dc9-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0dc9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e0dc9-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0dc9-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e0dc9-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0dc9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e0dc9-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e0dc9-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e0dc9-128">Header</span><span class="sxs-lookup"><span data-stu-id="e0dc9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0dc9-129"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0dc9-129"><dt>Locationapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0dc9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0dc9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0dc9-131">**Newcivicaddressreport-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="e0dc9-131">**NewCivicAddressReport Event**</span></span>](newcivicaddressreport.md)
</dt> </dl>

 

