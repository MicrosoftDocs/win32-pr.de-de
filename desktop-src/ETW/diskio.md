---
description: Diese Klasse ist die übergeordnete Klasse für Datenträger-e/a-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: Diskio-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97f9907e4da51675bb1a5f562931e471ee0e133e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958755"
---
# <a name="diskio-class"></a><span data-ttu-id="82b8e-104">Diskio-Klasse</span><span class="sxs-lookup"><span data-stu-id="82b8e-104">DiskIo class</span></span>

<span data-ttu-id="82b8e-105">Diese Klasse ist die übergeordnete Klasse für Datenträger-e/a-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="82b8e-105">This class is the parent class for disk I/O events.</span></span>

<span data-ttu-id="82b8e-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="82b8e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="82b8e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="82b8e-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="82b8e-108">Member</span><span class="sxs-lookup"><span data-stu-id="82b8e-108">Members</span></span>

<span data-ttu-id="82b8e-109">Die **diskio** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="82b8e-109">The **DiskIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="82b8e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82b8e-110">Remarks</span></span>

<span data-ttu-id="82b8e-111">Wenn Sie Datenträger-e/a-Ereignisse in einer NT-Kernel Protokollierungs Sitzung aktivieren möchten, geben Sie das Flag für die Ereignis Ablaufverfolgungsflag für Datenträger- [](/windows/win32/api/evntrace/nf-evntrace-starttracea) e/a im **enableflags** -Member einer Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="82b8e-111">To enable disk I/0 events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="82b8e-112">Sie können auch eines oder mehrere der folgenden Flags angeben:</span><span class="sxs-lookup"><span data-stu-id="82b8e-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="82b8e-113">**Ereignis \_ Ablauf \_ Verfolgung \_ Flag \_ Daten \_ Träger-e/a**</span><span class="sxs-lookup"><span data-stu-id="82b8e-113">**EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT**</span></span>
-   <span data-ttu-id="82b8e-114">**Ereignis Ablauf Verfolgungs Kennzeichen- \_ \_ \_ Treiber**</span><span class="sxs-lookup"><span data-stu-id="82b8e-114">**EVENT\_TRACE\_FLAG\_DRIVER**</span></span>

<span data-ttu-id="82b8e-115">Consumer der Ereignis Ablauf Verfolgung können eine spezielle Verarbeitung für Datenträger-e/a-Ereignisse implementieren, indem Sie die Funktion [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**diskioguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="82b8e-115">Event trace consumers can implement special processing for disk I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**DiskIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="82b8e-116">Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Datenträger-e/a-Ereignis beim Verarbeiten von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="82b8e-116">Use the following event types to identify the actual disk I/O event when consuming events.</span></span>



| <span data-ttu-id="82b8e-117">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="82b8e-117">Event type</span></span>                                                                      | <span data-ttu-id="82b8e-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82b8e-118">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b8e-119">**Ereignis \_ E \_ \_ \_**/a-Ablaufverfolgungstyp</span><span class="sxs-lookup"><span data-stu-id="82b8e-119">**EVENT\_TRACE\_TYPE\_IO\_READ**(Event type value is 10)</span></span><br/>             | <span data-ttu-id="82b8e-120">Lese Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-120">Read event.</span></span> <span data-ttu-id="82b8e-121">Die [**diskio \_ TypeGroup1**](diskio-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-121">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                              |
| <span data-ttu-id="82b8e-122">**Ereignis \_ E/a-Schreibvorgänge des \_ \_ ablaufverfolgungstyps \_**</span><span class="sxs-lookup"><span data-stu-id="82b8e-122">**EVENT\_TRACE\_TYPE\_IO\_WRITE**(Event type value is 11)</span></span><br/>            | <span data-ttu-id="82b8e-123">Schreib Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-123">Write event.</span></span> <span data-ttu-id="82b8e-124">Die [**diskio \_ TypeGroup1**](diskio-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-124">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                             |
| <span data-ttu-id="82b8e-125">**Ereignis \_ Ablaufverfolgungstyp-e/a \_ \_ \_ Lesen \_ Init**(Ereignistyp ist 12)</span><span class="sxs-lookup"><span data-stu-id="82b8e-125">**EVENT\_TRACE\_TYPE\_IO\_READ\_INIT**(Event type value is 12)</span></span><br/>       | <span data-ttu-id="82b8e-126">Lese Ereignis initialisieren.</span><span class="sxs-lookup"><span data-stu-id="82b8e-126">Initialize read event.</span></span> <span data-ttu-id="82b8e-127">Die [**diskio \_ TypeGroup2**](diskio-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-127">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="82b8e-128">**Ereignis \_ E/a- \_ \_ \_ \_ Ablaufverfolgungstyp**</span><span class="sxs-lookup"><span data-stu-id="82b8e-128">**EVENT\_TRACE\_TYPE\_IO\_WRITE\_INIT**(Event type value is 13)</span></span><br/>      | <span data-ttu-id="82b8e-129">Initialisieren Sie das Schreib Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-129">Initialize write event.</span></span> <span data-ttu-id="82b8e-130">Die [**diskio \_ TypeGroup2**](diskio-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-130">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="82b8e-131">**Ereignis \_ E \_ \_ \_**/a-Leerung des Ablauf Verfolgungs Typs (Ereignistyp ist 14</span><span class="sxs-lookup"><span data-stu-id="82b8e-131">**EVENT\_TRACE\_TYPE\_IO\_FLUSH**(Event type value is 14)</span></span><br/>            | <span data-ttu-id="82b8e-132">Initialisieren Sie das Schreib Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-132">Initialize write event.</span></span> <span data-ttu-id="82b8e-133">Die [**diskio \_ TypeGroup3**](diskio-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-133">The [**DiskIo\_TypeGroup3**](diskio-typegroup3.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="82b8e-134">**Ereignis \_ Ablauf Verfolgungs Typen-e/a-Leerungs- \_ \_ \_ \_ Init**</span><span class="sxs-lookup"><span data-stu-id="82b8e-134">**EVENT\_TRACE\_TYPE\_IO\_FLUSH\_INIT**(Event type value is 15)</span></span><br/>      | <span data-ttu-id="82b8e-135">Lösch Ereignis initialisieren.</span><span class="sxs-lookup"><span data-stu-id="82b8e-135">Initialize flush event.</span></span> <span data-ttu-id="82b8e-136">Die [**diskio \_ TypeGroup2**](diskio-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-136">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="82b8e-137">**Ereignis \_ \_ \_ \_ Umgeleiteter \_** e/a-Ablaufverfolgungstyp</span><span class="sxs-lookup"><span data-stu-id="82b8e-137">**EVENT\_TRACE\_TYPE\_IO\_REDIRECTED\_INIT**(Event type value is 16)</span></span><br/> | <span data-ttu-id="82b8e-138">Initialisieren Sie das umgeleitete Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-138">Initialize redirected event.</span></span> <span data-ttu-id="82b8e-139">Umgeleitete e/a-Ereignisse werden verwendet, um die Datenträger-e/a-Vorgänge in einem Windows-Abbild Format (WIM) dem Dateinamen</span><span class="sxs-lookup"><span data-stu-id="82b8e-139">Redirected IO events are used to map disk IOs to a Windows Imaging Format (WIM) to the filename within the WIM.</span></span>                  |
| <span data-ttu-id="82b8e-140">Der Ereignistyp Wert ist 52</span><span class="sxs-lookup"><span data-stu-id="82b8e-140">Event type value is 52</span></span><br/>                                               | <span data-ttu-id="82b8e-141">Anforderungs Ereignis für Treiber Abschluss.</span><span class="sxs-lookup"><span data-stu-id="82b8e-141">Driver complete request event.</span></span> <span data-ttu-id="82b8e-142">Die " [**drivercompleterequest**](drivercompleterequest.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-142">The [**DriverCompleteRequest**](drivercompleterequest.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="82b8e-143">Der Ereignistyp Wert ist 53</span><span class="sxs-lookup"><span data-stu-id="82b8e-143">Event type value is 53</span></span><br/>                                               | <span data-ttu-id="82b8e-144">Das Anforderungs Rückgabe Ereignis des Treibers wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="82b8e-144">Driver complete request return event.</span></span> <span data-ttu-id="82b8e-145">Die " [**drivercompleterequestreturn**](drivercompleterequestreturn.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-145">The [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="82b8e-146">Der Ereignistyp Wert ist 37</span><span class="sxs-lookup"><span data-stu-id="82b8e-146">Event type value is 37</span></span><br/>                                               | <span data-ttu-id="82b8e-147">Routine Ereignis für Treiber Abschluss.</span><span class="sxs-lookup"><span data-stu-id="82b8e-147">Driver completion routine event.</span></span> <span data-ttu-id="82b8e-148">Die MOF-Klasse [**drivercompletionroutine**](drivercompletionroutine.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-148">The [**DriverCompletionRoutine**](drivercompletionroutine.md) MOF class defines the event data for this event.</span></span>              |
| <span data-ttu-id="82b8e-149">Der Ereignistyp Wert ist 34</span><span class="sxs-lookup"><span data-stu-id="82b8e-149">Event type value is 34</span></span><br/>                                               | <span data-ttu-id="82b8e-150">Ereignis des Haupt Funktions aufrufdes Treibers.</span><span class="sxs-lookup"><span data-stu-id="82b8e-150">Driver major function call event.</span></span> <span data-ttu-id="82b8e-151">Die " [**drivermajorfunctioncallmof**](drivermajorfunctioncall.md) "-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-151">The [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) MOF class defines the event data for this event.</span></span>             |
| <span data-ttu-id="82b8e-152">Der Ereignistyp Wert ist 35</span><span class="sxs-lookup"><span data-stu-id="82b8e-152">Event type value is 35</span></span><br/>                                               | <span data-ttu-id="82b8e-153">Ereignis für den Haupt Funktions Rückruf des Treibers.</span><span class="sxs-lookup"><span data-stu-id="82b8e-153">Driver major function call return event.</span></span> <span data-ttu-id="82b8e-154">Die " [**drivermajorfunctionreturn**](drivermajorfunctionreturn.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82b8e-154">The [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="82b8e-155">Der Datenträger-e/a-Anbieter kann nicht ermitteln, welche Datei während eines Datenträger-e/a-Ereignisses gelesen oder geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="82b8e-155">The disk I/0 provider cannot identify which file is read or written during a disk I/O event.</span></span> <span data-ttu-id="82b8e-156">Aktivieren Sie den Datei-e/a-Ereignis Anbieter, um den Namen der Datei abzurufen, die dem Datenträger-e/a-Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="82b8e-156">To retrieve the name of the file associated with the disk I/O event, enable the file I/0 event provider.</span></span>

<span data-ttu-id="82b8e-157">Datenträger-e/a-Ereignisse werden zum Zeitpunkt des e/a-Abschlusses aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="82b8e-157">Disk I/O events are recorded at the I/O completion time.</span></span> <span data-ttu-id="82b8e-158">Um zu ermitteln, wann der e/a-Vorgang begonnen hat, verwenden Sie die Initialisierungs Ereignisse, z. b. den Ereignis Ablauf \_ Verfolgungs \_ Typ \_ IO \_ Read \_ init.</span><span class="sxs-lookup"><span data-stu-id="82b8e-158">To determine when the I/O operation began, use the initialization events, for example, EVENT\_TRACE\_TYPE\_IO\_READ\_INIT.</span></span>

## <a name="requirements"></a><span data-ttu-id="82b8e-159">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="82b8e-159">Requirements</span></span>



| <span data-ttu-id="82b8e-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82b8e-160">Requirement</span></span> | <span data-ttu-id="82b8e-161">Wert</span><span class="sxs-lookup"><span data-stu-id="82b8e-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="82b8e-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82b8e-162">Minimum supported client</span></span><br/> | <span data-ttu-id="82b8e-163">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82b8e-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="82b8e-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82b8e-164">Minimum supported server</span></span><br/> | <span data-ttu-id="82b8e-165">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82b8e-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82b8e-166">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="82b8e-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b8e-167">**Diskio \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="82b8e-167">**DiskIo\_TypeGroup1**</span></span>](diskio-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="82b8e-168">**Diskio \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="82b8e-168">**DiskIo\_TypeGroup2**</span></span>](diskio-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="82b8e-169">**Diskio \_ TypeGroup3**</span><span class="sxs-lookup"><span data-stu-id="82b8e-169">**DiskIo\_TypeGroup3**</span></span>](diskio-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="82b8e-170">**Drivercompleterequest**</span><span class="sxs-lookup"><span data-stu-id="82b8e-170">**DriverCompleteRequest**</span></span>](drivercompleterequest.md)
</dt> <dt>

[<span data-ttu-id="82b8e-171">**Drivercompleterequestreturn**</span><span class="sxs-lookup"><span data-stu-id="82b8e-171">**DriverCompleteRequestReturn**</span></span>](drivercompleterequestreturn.md)
</dt> <dt>

[<span data-ttu-id="82b8e-172">**Drivercompletionroutine**</span><span class="sxs-lookup"><span data-stu-id="82b8e-172">**DriverCompletionRoutine**</span></span>](drivercompletionroutine.md)
</dt> <dt>

[<span data-ttu-id="82b8e-173">**Drivermajorfunctioncallcenter**</span><span class="sxs-lookup"><span data-stu-id="82b8e-173">**DriverMajorFunctionCall**</span></span>](drivermajorfunctioncall.md)
</dt> <dt>

[<span data-ttu-id="82b8e-174">**Drivermajorfunctionreturn**</span><span class="sxs-lookup"><span data-stu-id="82b8e-174">**DriverMajorFunctionReturn**</span></span>](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
