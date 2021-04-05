---
description: Verwaltet die Berichte zu öffentlichen Adressen.
ms.assetid: 46c2d001-409a-4a0a-9006-1c2c9d327c13
title: LocationDisp. civicaddressreportfactory-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 451bb21822d1b56e4c7a45f1587df04761b67690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758280"
---
# <a name="locationdispcivicaddressreportfactory-object"></a><span data-ttu-id="b775a-103">LocationDisp. civicaddressreportfactory-Objekt</span><span class="sxs-lookup"><span data-stu-id="b775a-103">LocationDisp.CivicAddressReportFactory object</span></span>

<span data-ttu-id="b775a-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b775a-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b775a-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b775a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b775a-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b775a-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="b775a-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="b775a-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="b775a-108">Verwaltet die Berichte zu öffentlichen Adressen.</span><span class="sxs-lookup"><span data-stu-id="b775a-108">Manages civic address reports.</span></span>

## <a name="members"></a><span data-ttu-id="b775a-109">Member</span><span class="sxs-lookup"><span data-stu-id="b775a-109">Members</span></span>

<span data-ttu-id="b775a-110">Das **LocationDisp. civicaddressreportfactory** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b775a-110">The **LocationDisp.CivicAddressReportFactory** object has these types of members:</span></span>

-   [<span data-ttu-id="b775a-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="b775a-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b775a-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b775a-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b775a-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="b775a-113">Methods</span></span>

<span data-ttu-id="b775a-114">Das **LocationDisp. civicaddressreportfactory** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b775a-114">The **LocationDisp.CivicAddressReportFactory** object has these methods.</span></span>



| <span data-ttu-id="b775a-115">Methode</span><span class="sxs-lookup"><span data-stu-id="b775a-115">Method</span></span>                                                                                            | <span data-ttu-id="b775a-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b775a-116">Description</span></span>                                                                                   |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b775a-117">**Listenforreports**</span><span class="sxs-lookup"><span data-stu-id="b775a-117">**ListenForReports**</span></span>](locationdisp-civicaddressreportfactory-listenforreports.md)               | <span data-ttu-id="b775a-118">Fordert Ereignisse für den Bericht "Civic Address" an</span><span class="sxs-lookup"><span data-stu-id="b775a-118">Requests civic address report events.</span></span><br/>                                              |
| [<span data-ttu-id="b775a-119">**Requestberechtigungs Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="b775a-119">**RequestPermissions**</span></span>](locationdisp-civicaddressreportfactory-requestpermissions.md)           | <span data-ttu-id="b775a-120">Öffnet ein System Dialogfeld zum Anfordern von Benutzerberechtigungen für Geräte, die für den Standort aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="b775a-120">Opens a system dialog box to request user permission for location-enabled devices.</span></span><br/> |
| [<span data-ttu-id="b775a-121">**Stoplisteningforreports**</span><span class="sxs-lookup"><span data-stu-id="b775a-121">**StopListeningForReports**</span></span>](locationdisp-civicaddressreportfactory-stoplisteningforreports.md) | <span data-ttu-id="b775a-122">Bricht die Ereignis Anforderungen für den Bericht "Civic Address" ab</span><span class="sxs-lookup"><span data-stu-id="b775a-122">Cancels civic address report event requests.</span></span><br/>                                       |



 

### <a name="properties"></a><span data-ttu-id="b775a-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b775a-123">Properties</span></span>

<span data-ttu-id="b775a-124">Das **LocationDisp. civicaddressreportfactory** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b775a-124">The **LocationDisp.CivicAddressReportFactory** object has these properties.</span></span>



| <span data-ttu-id="b775a-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b775a-125">Property</span></span>                                                                                        | <span data-ttu-id="b775a-126">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="b775a-126">Access type</span></span>           | <span data-ttu-id="b775a-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b775a-127">Description</span></span>                                                                                                |
|:------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b775a-128">**Civicaddressreport**</span><span class="sxs-lookup"><span data-stu-id="b775a-128">**CivicAddressReport**</span></span>](locationdisp-dispcivicaddressreport-civicaddressreport.md)<br/> | <span data-ttu-id="b775a-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b775a-129">Read-only</span></span><br/>  | <span data-ttu-id="b775a-130">Der aktuelle [**LocationDisp. dispcivicaddressreport**](locationdisp-dispcivicaddressreport.md).</span><span class="sxs-lookup"><span data-stu-id="b775a-130">The current [**LocationDisp.DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md).</span></span><br/> |
| [<span data-ttu-id="b775a-131">**Desiredaccuracy**</span><span class="sxs-lookup"><span data-stu-id="b775a-131">**DesiredAccuracy**</span></span>](locationdisp-civicaddressreportfactory-desiredaccuracy.md)<br/>    | <span data-ttu-id="b775a-132">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b775a-132">Read/write</span></span><br/> | <span data-ttu-id="b775a-133">Die aktuelle Einstellung für die gewünschte Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="b775a-133">The current desired-accuracy setting.</span></span><br/>                                                           |
| [<span data-ttu-id="b775a-134">**Report Interval**</span><span class="sxs-lookup"><span data-stu-id="b775a-134">**ReportInterval**</span></span>](locationdisp-civicaddressreportfactory-reportinterval.md)<br/>      | <span data-ttu-id="b775a-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b775a-135">Read/write</span></span><br/> | <span data-ttu-id="b775a-136">Das aktuelle Ereignis Intervall für das Berichts Ereignis in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="b775a-136">The current civic address report event interval in milliseconds.</span></span><br/>                                |
| [<span data-ttu-id="b775a-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="b775a-137">**Status**</span></span>](locationdisp-civicaddressreportfactory-status.md)<br/>                      | <span data-ttu-id="b775a-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b775a-138">Read-only</span></span><br/>  | <span data-ttu-id="b775a-139">Der aktuelle Status des Berichts.</span><span class="sxs-lookup"><span data-stu-id="b775a-139">The current report status.</span></span><br/>                                                                      |



 

## <a name="examples"></a><span data-ttu-id="b775a-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b775a-140">Examples</span></span>

<span data-ttu-id="b775a-141">Der folgende Beispielcode zeigt, wie Sie dieses Objekt in HTML-Code erstellen.</span><span class="sxs-lookup"><span data-stu-id="b775a-141">The following example code shows how to create this object in HTML code.</span></span>


```Text
<object id="civicfactory" 
    classid="clsid:2A11F42C-3E81-4ad4-9CBE-45579D89671A"
    type="application/x-oleobject">
</object>
```



<span data-ttu-id="b775a-142">Der folgende Beispielcode zeigt, wie dieses Objekt in JScript mithilfe von Windows Script Host erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b775a-142">The following example code shows how to create this object in JScript using Windows Script Host.</span></span>


```JScript
var civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory");
```



<span data-ttu-id="b775a-143">Der folgende Beispielcode zeigt, wie dieses Objekt in VBScript mithilfe von Windows Script Host erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b775a-143">The following example code shows how to create this object in VBScript using Windows Script Host.</span></span>


```VB
Dim civicfactory
Set civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory")
```



## <a name="requirements"></a><span data-ttu-id="b775a-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b775a-144">Requirements</span></span>



| <span data-ttu-id="b775a-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b775a-145">Requirement</span></span> | <span data-ttu-id="b775a-146">Wert</span><span class="sxs-lookup"><span data-stu-id="b775a-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="b775a-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b775a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="b775a-148">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b775a-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b775a-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b775a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="b775a-150">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b775a-150">None supported</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="b775a-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b775a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b775a-152">**LocationDisp. civicaddressreport**</span><span class="sxs-lookup"><span data-stu-id="b775a-152">**LocationDisp.CivicAddressReport**</span></span>](locationdisp-dispcivicaddressreport.md)
</dt> </dl>

 

