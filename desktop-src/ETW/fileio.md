---
description: Diese Klasse ist die übergeordnete Klasse für Datei-e/a-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: Klasse "fleio"
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
ms.openlocfilehash: 2f7c032cb7af325efa1d2ea76702068fc7b3be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978849"
---
# <a name="fileio-class"></a><span data-ttu-id="ec4c2-104">Klasse "fleio"</span><span class="sxs-lookup"><span data-stu-id="ec4c2-104">FileIo class</span></span>

<span data-ttu-id="ec4c2-105">Diese Klasse ist die übergeordnete Klasse für Datei-e/a-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-105">This class is the parent class for file I/O events.</span></span>

<span data-ttu-id="ec4c2-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec4c2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec4c2-107">Syntax</span></span>

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="ec4c2-108">Member</span><span class="sxs-lookup"><span data-stu-id="ec4c2-108">Members</span></span>

<span data-ttu-id="ec4c2-109">Die Klasse " **fleio** " definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-109">The **FileIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec4c2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec4c2-110">Remarks</span></span>

<span data-ttu-id="ec4c2-111">Wenn Sie die Datei-e/a-Ereignisse in einer NT-Kernel Protokollierungs Sitzung aktivieren möchten, geben Sie beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion das Flag für die **\_ \_ \_ ablaufverfolgungsdatenträgerdatei \_ \_** -e/a im **enableflags** -Member der [**\_ \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)</span><span class="sxs-lookup"><span data-stu-id="ec4c2-111">To enable the File IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="ec4c2-112">Sie können auch eines oder mehrere der folgenden Flags angeben:</span><span class="sxs-lookup"><span data-stu-id="ec4c2-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="ec4c2-113">**Datei-e/a \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ec4c2-113">**EVENT\_TRACE\_FLAG\_FILE\_IO**</span></span>
-   <span data-ttu-id="ec4c2-114">**Ereignis Ablauf Verfolgungs Kennzeichen- \_ \_ \_ Datei \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ec4c2-114">**EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT**</span></span>

<span data-ttu-id="ec4c2-115">Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für Datei-e/a-Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und als *pguid* -Parameter " [**fleioguid**](nt-kernel-logger-constants.md) " angeben</span><span class="sxs-lookup"><span data-stu-id="ec4c2-115">Event trace consumers can implement special processing for file I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**FileIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="ec4c2-116">Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Ereignis beim Verarbeiten von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-116">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="ec4c2-117">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="ec4c2-117">Event type</span></span>             | <span data-ttu-id="ec4c2-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec4c2-118">Description</span></span>                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec4c2-119">Der Ereignistyp Wert ist 0.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-119">Event type value is 0</span></span>  | <span data-ttu-id="ec4c2-120">Dateiname-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-120">File name event.</span></span> <span data-ttu-id="ec4c2-121">Die Klasse " [**fleio \_ Name**](fileio-name.md) MOF" definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-121">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                               |
| <span data-ttu-id="ec4c2-122">Der Ereignistyp Wert ist 32</span><span class="sxs-lookup"><span data-stu-id="ec4c2-122">Event type value is 32</span></span> | <span data-ttu-id="ec4c2-123">Ereignis zum Erstellen der Datei.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-123">File create event.</span></span> <span data-ttu-id="ec4c2-124">Die Klasse " [**fleio \_ Name**](fileio-name.md) MOF" definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-124">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="ec4c2-125">Der Ereignistyp Wert ist 35</span><span class="sxs-lookup"><span data-stu-id="ec4c2-125">Event type value is 35</span></span> | <span data-ttu-id="ec4c2-126">Ereignis zum Löschen von Dateien.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-126">File delete event.</span></span> <span data-ttu-id="ec4c2-127">Die Klasse " [**fleio \_ Name**](fileio-name.md) MOF" definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-127">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="ec4c2-128">Der Ereignistyp Wert ist 36</span><span class="sxs-lookup"><span data-stu-id="ec4c2-128">Event type value is 36</span></span> | <span data-ttu-id="ec4c2-129">Dateirundown-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-129">File rundown event.</span></span> <span data-ttu-id="ec4c2-130">Listet alle geöffneten Dateien auf dem Computer am Ende der Ablauf Verfolgungs Sitzung auf.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-130">Enumerates all open files on the computer at the end of the trace session.</span></span> <span data-ttu-id="ec4c2-131">Die Klasse " [**fleio \_ Name**](fileio-name.md) MOF" definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-131">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="ec4c2-132">Der Ereignistyp Wert ist 64</span><span class="sxs-lookup"><span data-stu-id="ec4c2-132">Event type value is 64</span></span> | <span data-ttu-id="ec4c2-133">Ereignis zum Erstellen der Datei.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-133">File create event.</span></span> <span data-ttu-id="ec4c2-134">Die "MOF"-Klasse " [**fleio \_ Create**](fileio-create.md) " definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-134">The [**FileIo\_Create**](fileio-create.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="ec4c2-135">Der Ereignistyp Wert ist 72</span><span class="sxs-lookup"><span data-stu-id="ec4c2-135">Event type value is 72</span></span> | <span data-ttu-id="ec4c2-136">Verzeichnisenumerationsereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-136">Directory enumeration event.</span></span> <span data-ttu-id="ec4c2-137">Die Klasse " [**fleio \_ direnum**](fileio-direnum.md) MOF" definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-137">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                             |
| <span data-ttu-id="ec4c2-138">Der Ereignistyp Wert ist 77</span><span class="sxs-lookup"><span data-stu-id="ec4c2-138">Event type value is 77</span></span> | <span data-ttu-id="ec4c2-139">Verzeichnis Benachrichtigungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-139">Directory notification event.</span></span> <span data-ttu-id="ec4c2-140">Die Klasse " [**fleio \_ direnum**](fileio-direnum.md) MOF" definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-140">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="ec4c2-141">Der Ereignistyp Wert ist 69</span><span class="sxs-lookup"><span data-stu-id="ec4c2-141">Event type value is 69</span></span> | <span data-ttu-id="ec4c2-142">Legen Sie das Informations Ereignis fest.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-142">Set information event.</span></span> <span data-ttu-id="ec4c2-143">Die " [**fleio \_ Info**](fileio-info.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-143">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="ec4c2-144">Der Ereignistyp Wert ist 70</span><span class="sxs-lookup"><span data-stu-id="ec4c2-144">Event type value is 70</span></span> | <span data-ttu-id="ec4c2-145">Datei Ereignis löschen.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-145">Delete file event.</span></span> <span data-ttu-id="ec4c2-146">Die " [**fleio \_ Info**](fileio-info.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-146">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="ec4c2-147">Der Ereignistyp Wert ist 71</span><span class="sxs-lookup"><span data-stu-id="ec4c2-147">Event type value is 71</span></span> | <span data-ttu-id="ec4c2-148">Datei Ereignis umbenennen.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-148">Rename file event.</span></span> <span data-ttu-id="ec4c2-149">Die " [**fleio \_ Info**](fileio-info.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-149">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="ec4c2-150">Der Ereignistyp Wert ist 74</span><span class="sxs-lookup"><span data-stu-id="ec4c2-150">Event type value is 74</span></span> | <span data-ttu-id="ec4c2-151">Ereignis für Abfrage Dateiinformationen.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-151">Query file information event.</span></span> <span data-ttu-id="ec4c2-152">Die " [**fleio \_ Info**](fileio-info.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-152">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="ec4c2-153">Der Ereignistyp Wert ist 75</span><span class="sxs-lookup"><span data-stu-id="ec4c2-153">Event type value is 75</span></span> | <span data-ttu-id="ec4c2-154">Dateisystem-Steuerungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-154">File system control event.</span></span> <span data-ttu-id="ec4c2-155">Die " [**fleio \_ Info**](fileio-info.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-155">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="ec4c2-156">Der Ereignistyp Wert ist 76</span><span class="sxs-lookup"><span data-stu-id="ec4c2-156">Event type value is 76</span></span> | <span data-ttu-id="ec4c2-157">Ende des Vorgangs Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-157">End of operation event.</span></span> <span data-ttu-id="ec4c2-158">Die Klasse " [**fleio \_ opend**](fileio-opend.md) MOF" definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-158">The [**FileIo\_OpEnd**](fileio-opend.md) MOF class defines the event data for this event.</span></span>                                                                      |
| <span data-ttu-id="ec4c2-159">Der Ereignistyp Wert ist 67</span><span class="sxs-lookup"><span data-stu-id="ec4c2-159">Event type value is 67</span></span> | <span data-ttu-id="ec4c2-160">Datei Lese Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-160">File read event.</span></span> <span data-ttu-id="ec4c2-161">Die MOF-Klasse " [**fleio Read \_ Write**](fileio-readwrite.md) " definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-161">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="ec4c2-162">Der Ereignistyp Wert ist 68</span><span class="sxs-lookup"><span data-stu-id="ec4c2-162">Event type value is 68</span></span> | <span data-ttu-id="ec4c2-163">Datei Schreib Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-163">File write event.</span></span> <span data-ttu-id="ec4c2-164">Die MOF-Klasse " [**fleio Read \_ Write**](fileio-readwrite.md) " definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-164">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                    |
| <span data-ttu-id="ec4c2-165">Der Ereignistyp Wert ist 65</span><span class="sxs-lookup"><span data-stu-id="ec4c2-165">Event type value is 65</span></span> | <span data-ttu-id="ec4c2-166">Bereinigen Sie das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-166">Clean up event.</span></span> <span data-ttu-id="ec4c2-167">Das-Ereignis wird generiert, wenn das letzte Handle der Datei freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-167">The event is generated when the last handle to the file is released.</span></span> <span data-ttu-id="ec4c2-168">Die MOF-Klasse " [**fleio \_ simpleop**](fileio-simpleop.md) " definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-168">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="ec4c2-169">Der Ereignistyp Wert ist 66</span><span class="sxs-lookup"><span data-stu-id="ec4c2-169">Event type value is 66</span></span> | <span data-ttu-id="ec4c2-170">Schließen Sie das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-170">Close event.</span></span> <span data-ttu-id="ec4c2-171">Das-Ereignis wird generiert, wenn das File-Objekt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-171">The event is generated when the file object is freed.</span></span> <span data-ttu-id="ec4c2-172">Die MOF-Klasse " [**fleio \_ simpleop**](fileio-simpleop.md) " definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-172">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>                     |
| <span data-ttu-id="ec4c2-173">Der Ereignistyp Wert ist 73</span><span class="sxs-lookup"><span data-stu-id="ec4c2-173">Event type value is 73</span></span> | <span data-ttu-id="ec4c2-174">Flush-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-174">Flush event.</span></span> <span data-ttu-id="ec4c2-175">Dieses Ereignis wird generiert, wenn die Datei Puffer vollständig auf den Datenträger geleert werden.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-175">This event is generated when the file buffers are fully flushed to disk.</span></span> <span data-ttu-id="ec4c2-176">Die MOF-Klasse " [**fleio \_ simpleop**](fileio-simpleop.md) " definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-176">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="ec4c2-177">Datei-e/a-Ereignisse werden zu Beginn des Vorgangs protokolliert.</span><span class="sxs-lookup"><span data-stu-id="ec4c2-177">File IO events are logged at the beginning of the operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec4c2-178">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ec4c2-178">Requirements</span></span>



| <span data-ttu-id="ec4c2-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec4c2-179">Requirement</span></span> | <span data-ttu-id="ec4c2-180">Wert</span><span class="sxs-lookup"><span data-stu-id="ec4c2-180">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ec4c2-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec4c2-181">Minimum supported client</span></span><br/> | <span data-ttu-id="ec4c2-182">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec4c2-182">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ec4c2-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec4c2-183">Minimum supported server</span></span><br/> | <span data-ttu-id="ec4c2-184">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec4c2-184">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ec4c2-185">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec4c2-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec4c2-186">**MSNT \_ systemtrace**</span><span class="sxs-lookup"><span data-stu-id="ec4c2-186">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="ec4c2-187">**"Fleio \_ v0"**</span><span class="sxs-lookup"><span data-stu-id="ec4c2-187">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> <dt>

[<span data-ttu-id="ec4c2-188">**Fleio \_ v1**</span><span class="sxs-lookup"><span data-stu-id="ec4c2-188">**FileIo\_V1**</span></span>](fileio-v1.md)
</dt> </dl>

 

 
