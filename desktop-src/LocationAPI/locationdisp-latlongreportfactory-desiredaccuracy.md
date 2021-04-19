---
description: Der aktuelle Wert für die gewünschte Genauigkeit.
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: LocationDisp. latlongreportfactory. desiredaccuracy (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: e17e415d9503660d873ae4df67d2469c646dd80e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363782"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a><span data-ttu-id="09b54-103">LocationDisp. latlongreportfactory. desiredaccuracy (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="09b54-103">LocationDisp.LatLongReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="09b54-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="09b54-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="09b54-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="09b54-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="09b54-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="09b54-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="09b54-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="09b54-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="09b54-108">Der aktuelle Wert für die gewünschte Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="09b54-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="09b54-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="09b54-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="09b54-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="09b54-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="09b54-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="09b54-111">Property value</span></span>

<span data-ttu-id="09b54-112">Diese Eigenschaft ist ein Lese- **/Schreib-ULONG**.</span><span class="sxs-lookup"><span data-stu-id="09b54-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="09b54-113">Wert</span><span class="sxs-lookup"><span data-stu-id="09b54-113">Value</span></span>                                                                        | <span data-ttu-id="09b54-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="09b54-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09b54-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="09b54-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="09b54-116">Standard.</span><span class="sxs-lookup"><span data-stu-id="09b54-116">Default.</span></span> <span data-ttu-id="09b54-117">Der Sensor sollte die Genauigkeit verwenden, bei der der Energieverbrauch und andere Kostenüberlegungen optimiert werden können.</span><span class="sxs-lookup"><span data-stu-id="09b54-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="09b54-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="09b54-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="09b54-119">Der Sensor sollte den genauesten Bericht übermitteln.</span><span class="sxs-lookup"><span data-stu-id="09b54-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="09b54-120">Dies beinhaltet die Verwendung von kostenpflichtigen Diensten oder Diensten mit höherem Akkuverbrauch oder höherer Verbindungsbandbreite.</span><span class="sxs-lookup"><span data-stu-id="09b54-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09b54-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09b54-121">Remarks</span></span>

<span data-ttu-id="09b54-122">Dieser Wert ist eine Anforderung an den Speicherort Anbieter.</span><span class="sxs-lookup"><span data-stu-id="09b54-122">This value is a request to the location provider.</span></span> <span data-ttu-id="09b54-123">Es ist nicht erforderlich, dass der standortanbieter Berichte in dem von Ihnen angeforderten Intervall bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="09b54-123">The location provider is not required to provide reports at the interval you requested.</span></span> <span data-ttu-id="09b54-124">Lesen Sie den Wert dieser Eigenschaft, um die Einstellung für das tatsächliche Berichts Intervall zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="09b54-124">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="09b54-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09b54-125">Requirements</span></span>



| <span data-ttu-id="09b54-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09b54-126">Requirement</span></span> | <span data-ttu-id="09b54-127">Wert</span><span class="sxs-lookup"><span data-stu-id="09b54-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="09b54-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09b54-128">Minimum supported client</span></span><br/> | <span data-ttu-id="09b54-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09b54-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="09b54-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09b54-130">Minimum supported server</span></span><br/> | <span data-ttu-id="09b54-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="09b54-131">None supported</span></span><br/>                  |



 

