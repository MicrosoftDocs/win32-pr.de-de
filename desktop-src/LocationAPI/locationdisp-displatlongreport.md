---
description: Stellt einen breiten-/Längen Grad dar.
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: LocationDisp. displatlongreport-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b9629f22aee33670463b2a0832c12d520a9b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352363"
---
# <a name="locationdispdisplatlongreport-object"></a><span data-ttu-id="539bf-103">LocationDisp. displatlongreport-Objekt</span><span class="sxs-lookup"><span data-stu-id="539bf-103">LocationDisp.DispLatLongReport object</span></span>

<span data-ttu-id="539bf-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="539bf-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="539bf-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="539bf-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="539bf-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="539bf-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="539bf-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="539bf-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="539bf-108">Stellt einen breiten-/Längen Grad dar.</span><span class="sxs-lookup"><span data-stu-id="539bf-108">Represents a latitude/longitude report.</span></span>

## <a name="members"></a><span data-ttu-id="539bf-109">Member</span><span class="sxs-lookup"><span data-stu-id="539bf-109">Members</span></span>

<span data-ttu-id="539bf-110">Das **LocationDisp. displatlongreport** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="539bf-110">The **LocationDisp.DispLatLongReport** object has these types of members:</span></span>

-   [<span data-ttu-id="539bf-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="539bf-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="539bf-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="539bf-112">Properties</span></span>

<span data-ttu-id="539bf-113">Das **LocationDisp. displatlongreport** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="539bf-113">The **LocationDisp.DispLatLongReport** object has these properties.</span></span>



| <span data-ttu-id="539bf-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="539bf-114">Property</span></span>                                                                         | <span data-ttu-id="539bf-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="539bf-115">Access type</span></span>          | <span data-ttu-id="539bf-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="539bf-116">Description</span></span>                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="539bf-117">**Höhe**</span><span class="sxs-lookup"><span data-stu-id="539bf-117">**Altitude**</span></span>](locationdisp-displatlongreport-altitude.md)<br/>           | <span data-ttu-id="539bf-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="539bf-118">Read-only</span></span><br/> | <span data-ttu-id="539bf-119">Aktuelle Höhe in Meter.</span><span class="sxs-lookup"><span data-stu-id="539bf-119">Current altitude, in meters.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="539bf-120">**"Altitudebug Error"**</span><span class="sxs-lookup"><span data-stu-id="539bf-120">**AltitudeError**</span></span>](locationdisp-displatlongreport-altitudeerror.md)<br/> | <span data-ttu-id="539bf-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="539bf-121">Read-only</span></span><br/> | <span data-ttu-id="539bf-122">Höhen Fehler in Meter.</span><span class="sxs-lookup"><span data-stu-id="539bf-122">Altitude error, in meters.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="539bf-123">**Errorradius**</span><span class="sxs-lookup"><span data-stu-id="539bf-123">**ErrorRadius**</span></span>](locationdisp-displatlongreport-errorradius.md)<br/>     | <span data-ttu-id="539bf-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="539bf-124">Read-only</span></span><br/> | <span data-ttu-id="539bf-125">Eine Entfernung vom gemeldeten Speicherort in Meter.</span><span class="sxs-lookup"><span data-stu-id="539bf-125">A distance from the reported location, in meters.</span></span> <span data-ttu-id="539bf-126">In Kombination mit dem gemeldeten Speicherort als Ursprung beschreibt dieser RADIUS den Kreis, in dem sich der tatsächliche Speicherort befindet.</span><span class="sxs-lookup"><span data-stu-id="539bf-126">Combined with the reported location as the origin, this radius describes the circle in which the actual location is proably located.</span></span><br/> |
| [<span data-ttu-id="539bf-127">**Breiten**</span><span class="sxs-lookup"><span data-stu-id="539bf-127">**Latitude**</span></span>](locationdisp-displatlongreport-latitude.md)<br/>           | <span data-ttu-id="539bf-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="539bf-128">Read-only</span></span><br/> | <span data-ttu-id="539bf-129">Aktueller Breitengrad in Grad.</span><span class="sxs-lookup"><span data-stu-id="539bf-129">Current latitude, in degrees.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="539bf-130">**Längengrad**</span><span class="sxs-lookup"><span data-stu-id="539bf-130">**Longitude**</span></span>](locationdisp-displatlongreport-longitude.md)<br/>         | <span data-ttu-id="539bf-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="539bf-131">Read-only</span></span><br/> | <span data-ttu-id="539bf-132">Aktueller Längengrad in Grad.</span><span class="sxs-lookup"><span data-stu-id="539bf-132">Current longitude, in degrees.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="539bf-133">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="539bf-133">**Timestamp**</span></span>](locationdisp-displatlongreport-timestamp.md)<br/>         | <span data-ttu-id="539bf-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="539bf-134">Read-only</span></span><br/> | <span data-ttu-id="539bf-135">Das Datum und die Uhrzeit, zu der der Bericht generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="539bf-135">The date and time when the report was generated.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="539bf-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="539bf-136">Remarks</span></span>

<span data-ttu-id="539bf-137">Sie können dieses Objekt über die [**latlongreport**](locationdisp-latlongreportfactory-latlongreport.md) -Eigenschaft des [**latlongreportfactory**](locationdisp-latlongreportfactory.md) -Objekts abrufen.</span><span class="sxs-lookup"><span data-stu-id="539bf-137">You can retrieve this object through the [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) property of the [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) object.</span></span> <span data-ttu-id="539bf-138">Sie können dieses Objekt über das [**newlatlongreport**](newlatlongreport.md) -Ereignis empfangen.</span><span class="sxs-lookup"><span data-stu-id="539bf-138">You can receive this object through the [**NewLatLongReport**](newlatlongreport.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="539bf-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="539bf-139">Requirements</span></span>



| <span data-ttu-id="539bf-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="539bf-140">Requirement</span></span> | <span data-ttu-id="539bf-141">Wert</span><span class="sxs-lookup"><span data-stu-id="539bf-141">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="539bf-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="539bf-142">Minimum supported client</span></span><br/> | <span data-ttu-id="539bf-143">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="539bf-143">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="539bf-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="539bf-144">Minimum supported server</span></span><br/> | <span data-ttu-id="539bf-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="539bf-145">None supported</span></span><br/>                  |



 

