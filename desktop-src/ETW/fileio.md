---
description: 'FileIo-Klasse: Diese Klasse ist die übergeordnete Klasse für Datei-E/A-Ereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: FileIo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 716528902a115e23eae5b49ef572b87a71d11e25
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106528"
---
# <a name="fileio-class"></a><span data-ttu-id="5ef10-104">FileIo-Klasse</span><span class="sxs-lookup"><span data-stu-id="5ef10-104">FileIo class</span></span>

<span data-ttu-id="5ef10-105">Diese Klasse ist die übergeordnete Klasse für Datei-E/A-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="5ef10-105">This class is the parent class for file I/O events.</span></span>

<span data-ttu-id="5ef10-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="5ef10-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ef10-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ef10-107">Syntax</span></span>

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="5ef10-108">Member</span><span class="sxs-lookup"><span data-stu-id="5ef10-108">Members</span></span>

<span data-ttu-id="5ef10-109">Die **FileIo-Klasse** definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="5ef10-109">The **FileIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ef10-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ef10-110">Remarks</span></span>

<span data-ttu-id="5ef10-111">Um die Datei-E/A-Ereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **FLAG EVENT TRACE FLAG DISK FILE \_ \_ \_ \_ \_ IO** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an.</span><span class="sxs-lookup"><span data-stu-id="5ef10-111">To enable the File IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="5ef10-112">Sie können auch eines oder mehrere der folgenden Flags angeben:</span><span class="sxs-lookup"><span data-stu-id="5ef10-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="5ef10-113">**\_ \_ EREIGNISVERFOLGUNGSFLAGDATEI \_ \_ E/A**</span><span class="sxs-lookup"><span data-stu-id="5ef10-113">**EVENT\_TRACE\_FLAG\_FILE\_IO**</span></span>
-   <span data-ttu-id="5ef10-114">**\_ \_ EREIGNIS-ABLAUFVERFOLGUNGSFLAGDATEI \_ IO \_ \_ INIT**</span><span class="sxs-lookup"><span data-stu-id="5ef10-114">**EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT**</span></span>

<span data-ttu-id="5ef10-115">Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für Datei-E/A-Ereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**FileIoGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben.</span><span class="sxs-lookup"><span data-stu-id="5ef10-115">Event trace consumers can implement special processing for file I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**FileIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="5ef10-116">Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Ereignis bei der Nutzung von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5ef10-116">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="5ef10-117">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="5ef10-117">Event type</span></span>             | <span data-ttu-id="5ef10-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ef10-118">Description</span></span>                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef10-119">Ereignistypwert ist 0</span><span class="sxs-lookup"><span data-stu-id="5ef10-119">Event type value is 0</span></span>  | <span data-ttu-id="5ef10-120">Dateinamenereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-120">File name event.</span></span> <span data-ttu-id="5ef10-121">Die [**MOF-Klasse FileIo \_ Name**](fileio-name.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-121">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                               |
| <span data-ttu-id="5ef10-122">Der Ereignistypwert ist 32.</span><span class="sxs-lookup"><span data-stu-id="5ef10-122">Event type value is 32</span></span> | <span data-ttu-id="5ef10-123">Datei-Erstellungsereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-123">File create event.</span></span> <span data-ttu-id="5ef10-124">Die [**MOF-Klasse FileIo \_ Name**](fileio-name.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-124">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="5ef10-125">Der Ereignistypwert ist 35</span><span class="sxs-lookup"><span data-stu-id="5ef10-125">Event type value is 35</span></span> | <span data-ttu-id="5ef10-126">Dateilöschereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-126">File delete event.</span></span> <span data-ttu-id="5ef10-127">Die [**MOF-Klasse FileIo \_ Name**](fileio-name.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-127">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="5ef10-128">Der Ereignistypwert ist 36.</span><span class="sxs-lookup"><span data-stu-id="5ef10-128">Event type value is 36</span></span> | <span data-ttu-id="5ef10-129">Datei-Rundownereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-129">File rundown event.</span></span> <span data-ttu-id="5ef10-130">Listet alle geöffneten Dateien auf dem Computer am Ende der Ablaufverfolgungssitzung auf.</span><span class="sxs-lookup"><span data-stu-id="5ef10-130">Enumerates all open files on the computer at the end of the trace session.</span></span> <span data-ttu-id="5ef10-131">Die [**MOF-Klasse FileIo \_ Name**](fileio-name.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-131">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="5ef10-132">Der Ereignistypwert ist 64.</span><span class="sxs-lookup"><span data-stu-id="5ef10-132">Event type value is 64</span></span> | <span data-ttu-id="5ef10-133">Dateierstellungsereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-133">File create event.</span></span> <span data-ttu-id="5ef10-134">Die [**FILEIO \_ CREATE**](fileio-create.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-134">The [**FileIo\_Create**](fileio-create.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="5ef10-135">Der Ereignistypwert ist 72.</span><span class="sxs-lookup"><span data-stu-id="5ef10-135">Event type value is 72</span></span> | <span data-ttu-id="5ef10-136">Verzeichnisenumerationsereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-136">Directory enumeration event.</span></span> <span data-ttu-id="5ef10-137">Die [**FileIo \_ DirEnum**](fileio-direnum.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-137">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                             |
| <span data-ttu-id="5ef10-138">Der Ereignistypwert ist 77.</span><span class="sxs-lookup"><span data-stu-id="5ef10-138">Event type value is 77</span></span> | <span data-ttu-id="5ef10-139">Verzeichnisbenachrichtigungsereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-139">Directory notification event.</span></span> <span data-ttu-id="5ef10-140">Die [**FileIo \_ DirEnum**](fileio-direnum.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-140">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="5ef10-141">Der Ereignistypwert ist 69.</span><span class="sxs-lookup"><span data-stu-id="5ef10-141">Event type value is 69</span></span> | <span data-ttu-id="5ef10-142">Ereignis zum Festlegen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="5ef10-142">Set information event.</span></span> <span data-ttu-id="5ef10-143">Die [**MOF-Klasse FileIo \_ Info**](fileio-info.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-143">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="5ef10-144">Der Ereignistypwert ist 70.</span><span class="sxs-lookup"><span data-stu-id="5ef10-144">Event type value is 70</span></span> | <span data-ttu-id="5ef10-145">Dateiereignis löschen.</span><span class="sxs-lookup"><span data-stu-id="5ef10-145">Delete file event.</span></span> <span data-ttu-id="5ef10-146">Die [**MOF-Klasse FileIo \_ Info**](fileio-info.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-146">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="5ef10-147">Der Ereignistypwert ist 71.</span><span class="sxs-lookup"><span data-stu-id="5ef10-147">Event type value is 71</span></span> | <span data-ttu-id="5ef10-148">Dateiereignis umbenennen.</span><span class="sxs-lookup"><span data-stu-id="5ef10-148">Rename file event.</span></span> <span data-ttu-id="5ef10-149">Die [**MOF-Klasse FileIo \_ Info**](fileio-info.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-149">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="5ef10-150">Der Ereignistypwert ist 74</span><span class="sxs-lookup"><span data-stu-id="5ef10-150">Event type value is 74</span></span> | <span data-ttu-id="5ef10-151">Abfragedateiinformationsereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-151">Query file information event.</span></span> <span data-ttu-id="5ef10-152">Die [**MOF-Klasse FileIo \_ Info**](fileio-info.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-152">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="5ef10-153">Der Ereignistypwert ist 75.</span><span class="sxs-lookup"><span data-stu-id="5ef10-153">Event type value is 75</span></span> | <span data-ttu-id="5ef10-154">Dateisystem-Steuerungsereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-154">File system control event.</span></span> <span data-ttu-id="5ef10-155">Die [**MOF-Klasse FileIo \_ Info**](fileio-info.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-155">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="5ef10-156">Der Ereignistypwert ist 76</span><span class="sxs-lookup"><span data-stu-id="5ef10-156">Event type value is 76</span></span> | <span data-ttu-id="5ef10-157">Ereignis zum Ende des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5ef10-157">End of operation event.</span></span> <span data-ttu-id="5ef10-158">Die [**MOF-Klasse FileIo \_ OpEnd**](fileio-opend.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-158">The [**FileIo\_OpEnd**](fileio-opend.md) MOF class defines the event data for this event.</span></span>                                                                      |
| <span data-ttu-id="5ef10-159">Der Ereignistypwert ist 67.</span><span class="sxs-lookup"><span data-stu-id="5ef10-159">Event type value is 67</span></span> | <span data-ttu-id="5ef10-160">Dateileseereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-160">File read event.</span></span> <span data-ttu-id="5ef10-161">Die [**\_ MOF-Klasse FileIo ReadWrite**](fileio-readwrite.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-161">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="5ef10-162">Der Ereignistypwert ist 68</span><span class="sxs-lookup"><span data-stu-id="5ef10-162">Event type value is 68</span></span> | <span data-ttu-id="5ef10-163">Datei-Schreibereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-163">File write event.</span></span> <span data-ttu-id="5ef10-164">Die [**\_ MOF-Klasse FileIo ReadWrite**](fileio-readwrite.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-164">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                    |
| <span data-ttu-id="5ef10-165">Der Ereignistypwert ist 65</span><span class="sxs-lookup"><span data-stu-id="5ef10-165">Event type value is 65</span></span> | <span data-ttu-id="5ef10-166">Clean up-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-166">Clean up event.</span></span> <span data-ttu-id="5ef10-167">Das Ereignis wird generiert, wenn das letzte Handle für die Datei freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5ef10-167">The event is generated when the last handle to the file is released.</span></span> <span data-ttu-id="5ef10-168">Die [**FileIo \_ SimpleOp**](fileio-simpleop.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-168">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="5ef10-169">Der Ereignistypwert ist 66.</span><span class="sxs-lookup"><span data-stu-id="5ef10-169">Event type value is 66</span></span> | <span data-ttu-id="5ef10-170">Close-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-170">Close event.</span></span> <span data-ttu-id="5ef10-171">Das Ereignis wird generiert, wenn das Dateiobjekt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5ef10-171">The event is generated when the file object is freed.</span></span> <span data-ttu-id="5ef10-172">Die [**FileIo \_ SimpleOp**](fileio-simpleop.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-172">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>                     |
| <span data-ttu-id="5ef10-173">Der Ereignistypwert ist 73.</span><span class="sxs-lookup"><span data-stu-id="5ef10-173">Event type value is 73</span></span> | <span data-ttu-id="5ef10-174">Flush-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-174">Flush event.</span></span> <span data-ttu-id="5ef10-175">Dieses Ereignis wird generiert, wenn die Dateipuffer vollständig auf den Datenträger geleert werden.</span><span class="sxs-lookup"><span data-stu-id="5ef10-175">This event is generated when the file buffers are fully flushed to disk.</span></span> <span data-ttu-id="5ef10-176">Die [**FileIo \_ SimpleOp**](fileio-simpleop.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5ef10-176">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="5ef10-177">Datei-E/A-Ereignisse werden zu Beginn des Vorgangs protokolliert.</span><span class="sxs-lookup"><span data-stu-id="5ef10-177">File IO events are logged at the beginning of the operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ef10-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ef10-178">Requirements</span></span>



| <span data-ttu-id="5ef10-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ef10-179">Requirement</span></span> | <span data-ttu-id="5ef10-180">Wert</span><span class="sxs-lookup"><span data-stu-id="5ef10-180">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5ef10-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ef10-181">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef10-182">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ef10-182">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5ef10-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ef10-183">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef10-184">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ef10-184">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ef10-185">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5ef10-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef10-186">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="5ef10-186">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="5ef10-187">**FileIo \_ V0**</span><span class="sxs-lookup"><span data-stu-id="5ef10-187">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> <dt>

[<span data-ttu-id="5ef10-188">**FileIo \_ V1**</span><span class="sxs-lookup"><span data-stu-id="5ef10-188">**FileIo\_V1**</span></span>](fileio-v1.md)
</dt> </dl>

 

 
