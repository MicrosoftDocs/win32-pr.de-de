---
description: Der aktuelle Wert für die gewünschte Genauigkeit.
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: LocationDisp. civicaddressreportfactory. desiredaccuracy (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: eb05aeb6a69bfe978682d418cf1e71aed2184bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373358"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a><span data-ttu-id="6818c-103">LocationDisp. civicaddressreportfactory. desiredaccuracy (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6818c-103">LocationDisp.CivicAddressReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="6818c-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6818c-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6818c-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6818c-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6818c-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="6818c-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="6818c-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="6818c-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="6818c-108">Der aktuelle Wert für die gewünschte Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="6818c-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="6818c-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6818c-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6818c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6818c-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="6818c-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6818c-111">Property value</span></span>

<span data-ttu-id="6818c-112">Diese Eigenschaft ist ein Lese- **/Schreib-ULONG**.</span><span class="sxs-lookup"><span data-stu-id="6818c-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="6818c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="6818c-113">Value</span></span>                                                                        | <span data-ttu-id="6818c-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6818c-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6818c-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6818c-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="6818c-116">Standard.</span><span class="sxs-lookup"><span data-stu-id="6818c-116">Default.</span></span> <span data-ttu-id="6818c-117">Der Sensor sollte die Genauigkeit verwenden, bei der der Energieverbrauch und andere Kostenüberlegungen optimiert werden können.</span><span class="sxs-lookup"><span data-stu-id="6818c-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="6818c-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6818c-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6818c-119">Der Sensor sollte den genauesten Bericht übermitteln.</span><span class="sxs-lookup"><span data-stu-id="6818c-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="6818c-120">Dies beinhaltet die Verwendung von kostenpflichtigen Diensten oder Diensten mit höherem Akkuverbrauch oder höherer Verbindungsbandbreite.</span><span class="sxs-lookup"><span data-stu-id="6818c-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6818c-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6818c-121">Remarks</span></span>

<span data-ttu-id="6818c-122">Dieser Wert ist eine Anforderung an den Speicherort Anbieter.</span><span class="sxs-lookup"><span data-stu-id="6818c-122">This value is a request to the location provider.</span></span> <span data-ttu-id="6818c-123">Der Speicherort Anbieter ist nicht erforderlich, um die gewünschte Genauigkeit anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6818c-123">The location provider is not required to provide the accuracy that you request.</span></span> <span data-ttu-id="6818c-124">Lesen Sie den Wert dieser Eigenschaft, um die Einstellung für die tatsächliche Genauigkeit zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="6818c-124">Read the value of this property to discover the true accuracy setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="6818c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6818c-125">Requirements</span></span>



| <span data-ttu-id="6818c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6818c-126">Requirement</span></span> | <span data-ttu-id="6818c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="6818c-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="6818c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6818c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6818c-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6818c-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6818c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6818c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6818c-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6818c-131">None supported</span></span><br/>                  |



 

