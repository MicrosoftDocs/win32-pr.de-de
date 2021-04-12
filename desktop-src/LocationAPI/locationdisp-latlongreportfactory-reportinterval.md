---
description: Das aktuelle Berichts Ereignis Intervall (breiten-/Längen Grad) in Millisekunden.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: LocationDisp. latlongreportfactory. reportinterval (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: b456f69a70655b22b1eca30e02d9d5369d19f38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216572"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a><span data-ttu-id="6641f-103">LocationDisp. latlongreportfactory. reportinterval (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6641f-103">LocationDisp.LatLongReportFactory.ReportInterval property</span></span>

<span data-ttu-id="6641f-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6641f-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6641f-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6641f-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6641f-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="6641f-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="6641f-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="6641f-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="6641f-108">Das aktuelle Berichts Ereignis Intervall (breiten-/Längen Grad) in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="6641f-108">The current latitude/longitude report event interval in milliseconds.</span></span>

<span data-ttu-id="6641f-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6641f-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6641f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6641f-110">Syntax</span></span>


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a><span data-ttu-id="6641f-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6641f-111">Property value</span></span>

<span data-ttu-id="6641f-112">Diese Eigenschaft ist ein Lese- **/Schreib-ULONG**.</span><span class="sxs-lookup"><span data-stu-id="6641f-112">This property is a read/write **ULONG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6641f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6641f-113">Remarks</span></span>

<span data-ttu-id="6641f-114">Dieser Wert ist eine Anforderung an den Speicherort Anbieter.</span><span class="sxs-lookup"><span data-stu-id="6641f-114">This value is a request to the location provider.</span></span> <span data-ttu-id="6641f-115">Es ist nicht erforderlich, dass der standortanbieter Berichte in dem von Ihnen angeforderten Intervall bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6641f-115">The location provider is not required to provide reports at the interval that you request.</span></span> <span data-ttu-id="6641f-116">Lesen Sie den Wert dieser Eigenschaft, um die Einstellung für das tatsächliche Berichts Intervall zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="6641f-116">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="6641f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6641f-117">Requirements</span></span>



| <span data-ttu-id="6641f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6641f-118">Requirement</span></span> | <span data-ttu-id="6641f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6641f-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="6641f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6641f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6641f-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6641f-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6641f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6641f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6641f-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6641f-123">None supported</span></span><br/>                  |



 

