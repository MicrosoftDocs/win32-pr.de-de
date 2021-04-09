---
description: Verwaltet Berichte mit breiten-und Längengrad.
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: LocationDisp. latlongreportfactory-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868892"
---
# <a name="locationdisplatlongreportfactory-object"></a><span data-ttu-id="e9e3a-103">LocationDisp. latlongreportfactory-Objekt</span><span class="sxs-lookup"><span data-stu-id="e9e3a-103">LocationDisp.LatLongReportFactory object</span></span>

<span data-ttu-id="e9e3a-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e9e3a-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e9e3a-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="e9e3a-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="e9e3a-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="e9e3a-108">Verwaltet Berichte mit breiten-und Längengrad.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-108">Manages latitude/longitude reports.</span></span>

## <a name="members"></a><span data-ttu-id="e9e3a-109">Member</span><span class="sxs-lookup"><span data-stu-id="e9e3a-109">Members</span></span>

<span data-ttu-id="e9e3a-110">Das **LocationDisp. latlongreportfactory** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e9e3a-110">The **LocationDisp.LatLongReportFactory** object has these types of members:</span></span>

-   [<span data-ttu-id="e9e3a-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="e9e3a-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e9e3a-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e9e3a-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e9e3a-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="e9e3a-113">Methods</span></span>

<span data-ttu-id="e9e3a-114">Das **LocationDisp. latlongreportfactory** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-114">The **LocationDisp.LatLongReportFactory** object has these methods.</span></span>



| <span data-ttu-id="e9e3a-115">Methode</span><span class="sxs-lookup"><span data-stu-id="e9e3a-115">Method</span></span>                                                                                       | <span data-ttu-id="e9e3a-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9e3a-116">Description</span></span>                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9e3a-117">**Listenforreports**</span><span class="sxs-lookup"><span data-stu-id="e9e3a-117">**ListenForReports**</span></span>](locationdisp-latlongreportfactory-listenforreports.md)               | <span data-ttu-id="e9e3a-118">Fordert Berichts Ereignisse mit breiten-/Längen Grad an.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-118">Requests latitude/longitude report events.</span></span><br/>                                         |
| [<span data-ttu-id="e9e3a-119">**Requestberechtigungs Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="e9e3a-119">**RequestPermissions**</span></span>](locationdisp-latlongreportfactory-requestpermissions.md)           | <span data-ttu-id="e9e3a-120">Öffnet ein System Dialogfeld zum Anfordern von Benutzerberechtigungen für Geräte, die für den Standort aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-120">Opens a system dialog box to request user permission for location-enabled devices.</span></span><br/> |
| <span data-ttu-id="e9e3a-121">[**Stoplisteningforreports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9e3a-121">[**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span></span> | <span data-ttu-id="e9e3a-122">Bricht Anforderungen für Berichts Ereignisse mit breiten-und Längengrad ab.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-122">Cancels requests for latitude/longitude report events.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="e9e3a-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e9e3a-123">Properties</span></span>

<span data-ttu-id="e9e3a-124">Das **LocationDisp. latlongreportfactory** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-124">The **LocationDisp.LatLongReportFactory** object has these properties.</span></span>



| <span data-ttu-id="e9e3a-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e9e3a-125">Property</span></span>                                                                                | <span data-ttu-id="e9e3a-126">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="e9e3a-126">Access type</span></span>           | <span data-ttu-id="e9e3a-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9e3a-127">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9e3a-128">**Desiredaccuracy**</span><span class="sxs-lookup"><span data-stu-id="e9e3a-128">**DesiredAccuracy**</span></span>](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | <span data-ttu-id="e9e3a-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e9e3a-129">Read/write</span></span><br/> | <span data-ttu-id="e9e3a-130">Der aktuelle Wert für die gewünschte Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-130">The current desired-accuracy value.</span></span><br/>                                                   |
| [<span data-ttu-id="e9e3a-131">**Latlongreport**</span><span class="sxs-lookup"><span data-stu-id="e9e3a-131">**LatLongReport**</span></span>](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | <span data-ttu-id="e9e3a-132">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9e3a-132">Read-only</span></span><br/>  | <span data-ttu-id="e9e3a-133">Der aktuelle [**LocationDisp. displatlongreport**](locationdisp-displatlongreport.md).</span><span class="sxs-lookup"><span data-stu-id="e9e3a-133">The current [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).</span></span><br/> |
| [<span data-ttu-id="e9e3a-134">**Report Interval**</span><span class="sxs-lookup"><span data-stu-id="e9e3a-134">**ReportInterval**</span></span>](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | <span data-ttu-id="e9e3a-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e9e3a-135">Read/write</span></span><br/> | <span data-ttu-id="e9e3a-136">Das aktuelle Berichts Ereignis Intervall (breiten-/Längen Grad) in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-136">The current latitude/longitude report event interval in milliseconds.</span></span><br/>                 |
| [<span data-ttu-id="e9e3a-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="e9e3a-137">**Status**</span></span>](locationdisp-latlongreportfactory-status.md)<br/>                   | <span data-ttu-id="e9e3a-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9e3a-138">Read-only</span></span><br/>  | <span data-ttu-id="e9e3a-139">Der aktuelle Status des Berichts.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-139">The current report status.</span></span><br/>                                                            |



 

## <a name="examples"></a><span data-ttu-id="e9e3a-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9e3a-140">Examples</span></span>

<span data-ttu-id="e9e3a-141">Der folgende Beispielcode zeigt, wie Sie dieses Objekt in HTML-Code erstellen.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-141">The following example code shows how to create this object in HTML code.</span></span>


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



<span data-ttu-id="e9e3a-142">Der folgende Beispielcode zeigt, wie dieses Objekt in JScript mithilfe von Windows Script Host erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-142">The following example code shows how to create this object in JScript using Windows Script Host.</span></span>


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



<span data-ttu-id="e9e3a-143">Der folgende Beispielcode zeigt, wie dieses Objekt in VBScript mithilfe von Windows Script Host erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e9e3a-143">The following example code shows how to create this object in VBScript using Windows Script Host.</span></span>


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a><span data-ttu-id="e9e3a-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9e3a-144">Requirements</span></span>



| <span data-ttu-id="e9e3a-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9e3a-145">Requirement</span></span> | <span data-ttu-id="e9e3a-146">Wert</span><span class="sxs-lookup"><span data-stu-id="e9e3a-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="e9e3a-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9e3a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="e9e3a-148">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9e3a-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e9e3a-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9e3a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="e9e3a-150">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e9e3a-150">None supported</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="e9e3a-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9e3a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9e3a-152">**LocationDisp. displatlongreport**</span><span class="sxs-lookup"><span data-stu-id="e9e3a-152">**LocationDisp.DispLatLongReport**</span></span>](locationdisp-displatlongreport.md)
</dt> </dl>

 

