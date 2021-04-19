---
description: Die logfileeventconsumer-Klasse schreibt angepasste Zeichen folgen in eine Text Protokolldatei, wenn Ereignisse an Sie übermittelt werden.
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: Logfileeventconsumer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogFileEventConsumer
- LogFileEventConsumer.CreatorSID
- LogFileEventConsumer.MachineName
- LogFileEventConsumer.MaximumQueueSize
- LogFileEventConsumer.Filename
- LogFileEventConsumer.IsUnicode
- LogFileEventConsumer.MaximumFileSize
- LogFileEventConsumer.Name
- LogFileEventConsumer.Text
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 462989b740aaf6a6bd78968c951b7c676038cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348915"
---
# <a name="logfileeventconsumer-class"></a><span data-ttu-id="28aa6-103">Logfileeventconsumer-Klasse</span><span class="sxs-lookup"><span data-stu-id="28aa6-103">LogFileEventConsumer class</span></span>

<span data-ttu-id="28aa6-104">Die **logfileeventconsumer** -Klasse schreibt angepasste Zeichen folgen in eine Text Protokolldatei, wenn Ereignisse an Sie übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="28aa6-104">The **LogFileEventConsumer** class writes customized strings to a text log file when events are delivered to it.</span></span> <span data-ttu-id="28aa6-105">Die Zeichen folgen werden durch zeilige Zeilen voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="28aa6-105">The strings are separated by end-of-line sequences.</span></span> <span data-ttu-id="28aa6-106">Diese Klasse ist einer der standardereignisconsumer, die von WMI bereitstellt werden.</span><span class="sxs-lookup"><span data-stu-id="28aa6-106">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="28aa6-107">Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="28aa6-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="28aa6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="28aa6-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class LogFileEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  Filename;
  boolean IsUnicode;
  uint64  MaximumFileSize = 65535;
  string  Name;
  string  Text;
};
```

## <a name="members"></a><span data-ttu-id="28aa6-109">Member</span><span class="sxs-lookup"><span data-stu-id="28aa6-109">Members</span></span>

<span data-ttu-id="28aa6-110">Die **logfileeventconsumer** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="28aa6-110">The **LogFileEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="28aa6-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28aa6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="28aa6-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28aa6-112">Properties</span></span>

<span data-ttu-id="28aa6-113">Die **logfileeventconsumer** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="28aa6-113">The **LogFileEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="28aa6-114">**"Kreatorsid"**</span><span class="sxs-lookup"><span data-stu-id="28aa6-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28aa6-115">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="28aa6-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="28aa6-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="28aa6-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28aa6-117">Sicherheits-ID (SID), die den Benutzer, der einen Filter erstellt, eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="28aa6-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="28aa6-118">WMI speichert die SID des Benutzers, der eine Instanz von [**\_ \_ eventconsumer**](--eventconsumer.md) oder die Administrator-SID erstellt, je nach Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="28aa6-118">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="28aa6-119">Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="28aa6-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="28aa6-120">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="28aa6-120">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="28aa6-121">**Filename**</span><span class="sxs-lookup"><span data-stu-id="28aa6-121">**Filename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28aa6-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="28aa6-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28aa6-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="28aa6-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28aa6-124">Der Name einer Datei, die den Pfad enthält, an den die Protokolleinträge angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="28aa6-124">Name of a file that includes the path to which the log entries are appended.</span></span> <span data-ttu-id="28aa6-125">Wenn die Datei nicht vorhanden ist, versucht **logfileeventconsumer** , Sie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="28aa6-125">If the file does not exist, **LogFileEventConsumer** attempts to create it.</span></span> <span data-ttu-id="28aa6-126">Der Consumer schlägt fehl, wenn der Pfad nicht vorhanden ist oder wenn der Benutzer, der den Consumer erstellt, nicht über Schreibberechtigungen für die Datei oder den Pfad verfügt.</span><span class="sxs-lookup"><span data-stu-id="28aa6-126">The consumer fails when the path does not exist, or when the user who creates the consumer does not have write permissions for the file or path.</span></span>

</dd> <dt>

<span data-ttu-id="28aa6-127">**Isunicode**</span><span class="sxs-lookup"><span data-stu-id="28aa6-127">**IsUnicode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28aa6-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="28aa6-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="28aa6-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="28aa6-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28aa6-130">**True** gibt an, dass die Protokolldatei eine Unicode-Textdatei ist.</span><span class="sxs-lookup"><span data-stu-id="28aa6-130">If **TRUE**, the log file is a Unicode text file.</span></span> <span data-ttu-id="28aa6-131">Wenn der Wert **false** ist, ist die Protokolldatei eine Multibytezeichen-Code Textdatei.</span><span class="sxs-lookup"><span data-stu-id="28aa6-131">If **FALSE**, the log file is a multibyte code text file.</span></span> <span data-ttu-id="28aa6-132">Wenn die Datei vorhanden ist, wird diese Eigenschaft ignoriert, und die aktuelle Datei Einstellung wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="28aa6-132">If the file exists, this property is ignored and the current file setting is used.</span></span> <span data-ttu-id="28aa6-133">Wenn **isunicode** beispielsweise **false** ist, die vorhandene Datei jedoch eine Unicode-Datei ist, wird Unicode verwendet.</span><span class="sxs-lookup"><span data-stu-id="28aa6-133">For example, if **IsUnicode** is **FALSE**, but the existing file is a Unicode file, then Unicode is used.</span></span> <span data-ttu-id="28aa6-134">Wenn **isunicode** **true** ist, aber die Datei multibytecode ist, wird multibytecode verwendet.</span><span class="sxs-lookup"><span data-stu-id="28aa6-134">If **IsUnicode** is **TRUE**, but the file is multibyte code, then multibyte code is used.</span></span>

</dd> <dt>

<span data-ttu-id="28aa6-135">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="28aa6-135">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28aa6-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="28aa6-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28aa6-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="28aa6-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28aa6-138">Der Name des Computers, an den Windows-Verwaltungsinstrumentation (WMI) Ereignisse sendet.</span><span class="sxs-lookup"><span data-stu-id="28aa6-138">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="28aa6-139">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="28aa6-139">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="28aa6-140">**MaximumFileSize**</span><span class="sxs-lookup"><span data-stu-id="28aa6-140">**MaximumFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28aa6-141">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="28aa6-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="28aa6-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="28aa6-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28aa6-143">Maximale Größe einer Protokolldatei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="28aa6-143">Maximum size of a log file in bytes.</span></span> <span data-ttu-id="28aa6-144">Wenn die primäre Datei die maximale Größe überschreitet, wird der Inhalt in eine andere Datei verschoben, und die primäre Datei wird geleert.</span><span class="sxs-lookup"><span data-stu-id="28aa6-144">If the primary file exceeds its maximum size, the contents are moved to a different file and the primary file is emptied.</span></span> <span data-ttu-id="28aa6-145">Der Wert 0 (null) bedeutet, dass es keine Größenbeschränkung gibt.</span><span class="sxs-lookup"><span data-stu-id="28aa6-145">A value of 0 (zero) means there is no size limit.</span></span> <span data-ttu-id="28aa6-146">Der Standardwert ist 65.535 bytes.</span><span class="sxs-lookup"><span data-stu-id="28aa6-146">The default value is 65,535 bytes.</span></span> <span data-ttu-id="28aa6-147">Die Größe der Datei wird vor einem Schreibvorgang geprüft.</span><span class="sxs-lookup"><span data-stu-id="28aa6-147">The size of the file is checked before a write operation.</span></span> <span data-ttu-id="28aa6-148">Daher können Sie eine Datei haben, die etwas größer als die angegebene Größenbeschränkung ist.</span><span class="sxs-lookup"><span data-stu-id="28aa6-148">Therefore, you can have a file that is slightly larger than the specified size limit.</span></span> <span data-ttu-id="28aa6-149">Beim nächsten Schreibvorgang wird die Datei abgefangen und eine neue Datei gestartet.</span><span class="sxs-lookup"><span data-stu-id="28aa6-149">The next write operation catches it and starts a new file.</span></span>

<span data-ttu-id="28aa6-150">In der folgenden Liste ist die Benennungs Struktur für die Sicherungsdatei angegeben:</span><span class="sxs-lookup"><span data-stu-id="28aa6-150">The following list identifies the naming structure for the backup file:</span></span>

-   <span data-ttu-id="28aa6-151">Wenn der ursprüngliche Dateiname 8,3 ist, wird die Erweiterung durch eine Zeichenfolge im Format "001", "002" usw. ersetzt, wobei die kleinste Zahl größer als alle zuvor verwendeten und ausgewählten Zahlen ist.</span><span class="sxs-lookup"><span data-stu-id="28aa6-151">If the original filename is 8.3, the extension is replaced by a string in the format of "001", "002", and so on with the smallest number larger than all the previously used and chosen numbers.</span></span> <span data-ttu-id="28aa6-152">Wenn "999" verwendet wird, ist die ausgewählte Zahl die kleinste nicht verwendete Zahl.</span><span class="sxs-lookup"><span data-stu-id="28aa6-152">If "999" is used, then the number chosen is the smallest unused number.</span></span>
-   <span data-ttu-id="28aa6-153">Wenn der ursprüngliche Dateiname nicht 8,3 ist, wird eine Zeichenfolge im Format "001", "002" usw. an den Dateinamen angehängt.</span><span class="sxs-lookup"><span data-stu-id="28aa6-153">If the original filename is not 8.3, a string in the format of "001", "002", and so on is appended to the file name.</span></span>

<span data-ttu-id="28aa6-154">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="28aa6-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="28aa6-155">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="28aa6-155">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28aa6-156">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="28aa6-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28aa6-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="28aa6-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28aa6-158">Maximale Warteschlange für einen bestimmten Consumer in Bytes.</span><span class="sxs-lookup"><span data-stu-id="28aa6-158">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="28aa6-159">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="28aa6-159">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="28aa6-160">**Name**</span><span class="sxs-lookup"><span data-stu-id="28aa6-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28aa6-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="28aa6-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28aa6-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="28aa6-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28aa6-163">Qualifizierer: [ **Schlüssel**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="28aa6-163">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="28aa6-164">Eindeutiger Name für diesen Consumer.</span><span class="sxs-lookup"><span data-stu-id="28aa6-164">Unique name for this consumer.</span></span>

</dd> <dt>

<span data-ttu-id="28aa6-165">**Text**</span><span class="sxs-lookup"><span data-stu-id="28aa6-165">**Text**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28aa6-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="28aa6-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28aa6-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="28aa6-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28aa6-168">Standard Zeichen folgen [Vorlage](using-standard-string-templates.md) für den Text eines Protokoll Eintrags.</span><span class="sxs-lookup"><span data-stu-id="28aa6-168">Standard string [template](using-standard-string-templates.md) for the text of a log entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28aa6-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28aa6-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="28aa6-170">Die Protokolldatei wird von **logfileeventconsumer** nicht gesichert.</span><span class="sxs-lookup"><span data-stu-id="28aa6-170">The **LogFileEventConsumer** does not secure the log file.</span></span> <span data-ttu-id="28aa6-171">Wenn Sie **logfileeventconsumer** konfigurieren, ist es daher wichtig, ein Verzeichnis anzugeben, das auf der gewünschten Ebene gesichert ist.</span><span class="sxs-lookup"><span data-stu-id="28aa6-171">Therefore, when you configure the **LogFileEventConsumer**, it is important to specify a directory that is secured to the level that you require.</span></span>

 

<span data-ttu-id="28aa6-172">Die **logfileeventconsumer** -Klasse wird von der [**\_ \_ eventconsumer**](--eventconsumer.md) abstract-Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="28aa6-172">The **LogFileEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="28aa6-173">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28aa6-173">Examples</span></span>

<span data-ttu-id="28aa6-174">Ein Beispiel für die Verwendung von **logfileeventconsumer** , um einen Consumer zu erstellen, finden Sie unter [Schreiben in eine Protokolldatei auf Grundlage eines Ereignisses](writing-to-a-log-file-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="28aa6-174">For an example of using **LogFileEventConsumer** to create a consumer, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28aa6-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28aa6-175">Requirements</span></span>



| <span data-ttu-id="28aa6-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28aa6-176">Requirement</span></span> | <span data-ttu-id="28aa6-177">Wert</span><span class="sxs-lookup"><span data-stu-id="28aa6-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28aa6-178">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28aa6-178">Minimum supported client</span></span><br/> | <span data-ttu-id="28aa6-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28aa6-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28aa6-180">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28aa6-180">Minimum supported server</span></span><br/> | <span data-ttu-id="28aa6-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28aa6-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28aa6-182">Namespace</span><span class="sxs-lookup"><span data-stu-id="28aa6-182">Namespace</span></span><br/>                | <span data-ttu-id="28aa6-183">Stamm \\ Abonnement</span><span class="sxs-lookup"><span data-stu-id="28aa6-183">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="28aa6-184">MOF</span><span class="sxs-lookup"><span data-stu-id="28aa6-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28aa6-185"><dt>Wbemcons. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="28aa6-185"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="28aa6-186">DLL</span><span class="sxs-lookup"><span data-stu-id="28aa6-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28aa6-187"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28aa6-187"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28aa6-188">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28aa6-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28aa6-189">Standard Consumer-Klassen</span><span class="sxs-lookup"><span data-stu-id="28aa6-189">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="28aa6-190">Schreiben in eine Protokolldatei auf Grundlage eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="28aa6-190">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="28aa6-191">Erstellen eines logischen Consumers</span><span class="sxs-lookup"><span data-stu-id="28aa6-191">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="28aa6-192">Empfangen von Ereignissen zu allen Zeitpunkten</span><span class="sxs-lookup"><span data-stu-id="28aa6-192">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="28aa6-193">**\_\_Eventconsumer**</span><span class="sxs-lookup"><span data-stu-id="28aa6-193">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

