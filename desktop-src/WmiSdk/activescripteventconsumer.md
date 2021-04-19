---
description: Führt ein vordefiniertes Skript in einer beliebigen Skriptsprache aus, wenn ein Ereignis zugestellt wird.
ms.assetid: 2c0aa216-4255-49ff-9bbd-d6c62b5b9139
ms.tgt_platform: multiple
title: Activescripteventconsumer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActiveScriptEventConsumer
- ActiveScriptEventConsumer.CreatorSID
- ActiveScriptEventConsumer.KillTimeout
- ActiveScriptEventConsumer.MachineName
- ActiveScriptEventConsumer.MaximumQueueSize
- ActiveScriptEventConsumer.Name
- ActiveScriptEventConsumer.ScriptingEngine
- ActiveScriptEventConsumer.ScriptFileName
- ActiveScriptEventConsumer.ScriptText
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 11e2886fd5d0804946433e102e24617df768dcec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362880"
---
# <a name="activescripteventconsumer-class"></a><span data-ttu-id="6e53d-103">Activescripteventconsumer-Klasse</span><span class="sxs-lookup"><span data-stu-id="6e53d-103">ActiveScriptEventConsumer class</span></span>

<span data-ttu-id="6e53d-104">Die **activescripteventconsumer** -Klasse führt ein vordefiniertes Skript in einer beliebigen Skriptsprache aus, wenn ein Ereignis an Sie übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="6e53d-104">The **ActiveScriptEventConsumer** class runs a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span> <span data-ttu-id="6e53d-105">Diese Klasse ist einer der standardereignisconsumer, die von WMI bereitstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6e53d-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="6e53d-106">Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="6e53d-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



<span data-ttu-id="6e53d-107">Sie können die Leistung aller Instanzen von **activescripteventconsumer** in einem System konfigurieren, indem Sie die Werte der Eigenschaft [**Timeout**](scriptingstandardconsumersetting.md) oder **maximumscripts** in der einzelnen Instanz von **scriptingstandardconsumersetting** festlegen.</span><span class="sxs-lookup"><span data-stu-id="6e53d-107">You can configure the performance of all instances of **ActiveScriptEventConsumer** on a system by setting the values of either the [**Timeout**](scriptingstandardconsumersetting.md) or **MaximumScripts** property in the single instance of **ScriptingStandardConsumerSetting**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e53d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e53d-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class ActiveScriptEventConsumer : __EventConsumer
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  uint32 KillTimeout = 0;
  string MachineName;
  uint32 MaximumQueueSize;
  string Name;
  string ScriptingEngine;
  string ScriptFileName;
  string ScriptText;
};
```

## <a name="members"></a><span data-ttu-id="6e53d-109">Member</span><span class="sxs-lookup"><span data-stu-id="6e53d-109">Members</span></span>

<span data-ttu-id="6e53d-110">Die **activescripteventconsumer** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6e53d-110">The **ActiveScriptEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="6e53d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e53d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e53d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e53d-112">Properties</span></span>

<span data-ttu-id="6e53d-113">Die **activescripteventconsumer** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6e53d-113">The **ActiveScriptEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e53d-114">**"Kreatorsid"**</span><span class="sxs-lookup"><span data-stu-id="6e53d-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e53d-115">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="6e53d-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6e53d-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e53d-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e53d-117">Ein Array, das die Sicherheits-ID (SID) darstellt, die den Ersteller des aktiven Skript-Ereignisconsumers eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6e53d-117">Array that represents the security identifier (SID), which uniquely identifies the creator of the Active Script Event consumer.</span></span> <span data-ttu-id="6e53d-118">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e53d-118">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e53d-119">**Killtimeout**</span><span class="sxs-lookup"><span data-stu-id="6e53d-119">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e53d-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e53d-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e53d-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e53d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e53d-122">Anzahl in Sekunden, für die das Skript ausgeführt werden darf.</span><span class="sxs-lookup"><span data-stu-id="6e53d-122">Number, in seconds, that the script is allowed to run.</span></span> <span data-ttu-id="6e53d-123">Wenn der Standardwert 0 (null) ist, wird das Skript nicht beendet.</span><span class="sxs-lookup"><span data-stu-id="6e53d-123">If 0 (zero), which is the default, the script is not terminated.</span></span>

</dd> <dt>

<span data-ttu-id="6e53d-124">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="6e53d-124">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e53d-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e53d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e53d-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e53d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e53d-127">Der Name des Computers, an den WMI Ereignisse sendet.</span><span class="sxs-lookup"><span data-stu-id="6e53d-127">Name of the computer to which WMI sends events.</span></span> <span data-ttu-id="6e53d-128">Gemäß der Konvention von Microsoft-Standard Verbrauchern kann der Skript Consumer nicht remote ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6e53d-128">By convention of Microsoft standard consumers, the script consumer cannot be run remotely.</span></span> <span data-ttu-id="6e53d-129">Consumer von Drittanbietern können diese Eigenschaft ebenfalls verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e53d-129">Third-party consumers can also use this property.</span></span> <span data-ttu-id="6e53d-130">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e53d-130">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e53d-131">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="6e53d-131">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e53d-132">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e53d-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e53d-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e53d-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e53d-134">Maximale Warteschlange in Bytes für den aktiven Skript-Ereignisconsumer.</span><span class="sxs-lookup"><span data-stu-id="6e53d-134">Maximum queue, in bytes, for the Active Script Event consumer.</span></span> <span data-ttu-id="6e53d-135">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e53d-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e53d-136">**Name**</span><span class="sxs-lookup"><span data-stu-id="6e53d-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e53d-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e53d-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e53d-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6e53d-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6e53d-139">Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6e53d-139">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6e53d-140">Eindeutiger Bezeichner für den Ereignisconsumer.</span><span class="sxs-lookup"><span data-stu-id="6e53d-140">Unique identifier for the event consumer.</span></span> <span data-ttu-id="6e53d-141">Wenn Sie den Consumer umbenennen, ist das Ergebnis zwei gleichwertige Consumer mit unterschiedlichen Namen.</span><span class="sxs-lookup"><span data-stu-id="6e53d-141">If you rename the consumer, the result is two equal consumers that have different names.</span></span>

</dd> <dt>

<span data-ttu-id="6e53d-142">**Scriptfilename**</span><span class="sxs-lookup"><span data-stu-id="6e53d-142">**ScriptFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e53d-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e53d-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e53d-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e53d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e53d-145">Der Name der Datei, aus der der Skript Text gelesen wird. Sie dient als Alternative zum Angeben des Skript Texts in der **ScriptText** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6e53d-145">Name of the file from which the script text is read, intended as an alternative to specifying the text of the script in the **ScriptText** property.</span></span> <span data-ttu-id="6e53d-146">Diese Eigenschaft muss **null** sein, wenn die **ScriptText** -Eigenschaft nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="6e53d-146">This property must be **NULL** if the **ScriptText** property is not **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="6e53d-147">Wenn Sie **scriptfilename** angeben, ist es wichtig, die ausführbare Datei zu sichern, die Sie starten.</span><span class="sxs-lookup"><span data-stu-id="6e53d-147">When you specify the **ScriptFileName**, it is important to secure the executable that you are launching.</span></span> <span data-ttu-id="6e53d-148">Wenn sich die ausführbare Datei nicht an einem sicheren Speicherort befindet oder durch eine sichere Zugriffs Steuerungs Liste (ACL) geschützt ist, kann jeder Benutzer die ausführbare Datei durch eine andere ersetzen.</span><span class="sxs-lookup"><span data-stu-id="6e53d-148">If the executable is not in a secure location or secured with a strong access control list (ACL), anyone can replace the executable with a different one.</span></span> <span data-ttu-id="6e53d-149">Weitere Informationen zu ACLs finden Sie unter [Erstellen eines Sicherheits Deskriptors (SD) für ein neues Objekt in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="6e53d-149">For more information about ACLs, see [Creating a Security Descriptor (SD) for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="6e53d-150">**Scriptingengine**</span><span class="sxs-lookup"><span data-stu-id="6e53d-150">**ScriptingEngine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e53d-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e53d-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e53d-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e53d-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e53d-153">Der Name der zu verwendenden Skript-Engine, z. b. "VBScript".</span><span class="sxs-lookup"><span data-stu-id="6e53d-153">Name of the scripting engine to use, for example, "VBScript".</span></span> <span data-ttu-id="6e53d-154">Diese Eigenschaft darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="6e53d-154">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6e53d-155">**ScriptText**</span><span class="sxs-lookup"><span data-stu-id="6e53d-155">**ScriptText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e53d-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e53d-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e53d-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e53d-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e53d-158">Text des Skripts, das in einer Sprache ausgedrückt wird, die der Skript-Engine bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6e53d-158">Text of the script that is expressed in a language known to the scripting engine.</span></span> <span data-ttu-id="6e53d-159">Diese Eigenschaft muss **null** sein, wenn die **scriptfilename** -Eigenschaft nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="6e53d-159">This property must be **NULL** if the **ScriptFileName** property is not **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e53d-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e53d-160">Remarks</span></span>

<span data-ttu-id="6e53d-161">Diese Klasse wird von der [**\_ \_ eventconsumer**](--eventconsumer.md) abstract-Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6e53d-161">This class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span> <span data-ttu-id="6e53d-162">Sie befindet sich im \\ Namespace des Stamm Abonnements.</span><span class="sxs-lookup"><span data-stu-id="6e53d-162">It is located in the root\\subscription namespace.</span></span>

<span data-ttu-id="6e53d-163">Wenn der Text eines Skripts in der ereignisconsumerinstanz angegeben ist, hat das Skript Zugriff auf die Ereignis Instanz in der Skript Umgebungsvariablen **targetevent**.</span><span class="sxs-lookup"><span data-stu-id="6e53d-163">When the text of a script is specified in the event consumer instance, the script has access to the event instance in the script environment variable **TargetEvent**.</span></span>

<span data-ttu-id="6e53d-164">Die Skripts werden im Sicherheitskontext "LocalSystem" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e53d-164">The scripts run in the LocalSystem security context.</span></span> <span data-ttu-id="6e53d-165">Als Sicherheitsmaßnahme kann der skriptingconsumer nur von einem lokalen Systemadministrator oder einem Domänen Administrator konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="6e53d-165">As a security measure, only a local system administrator or a domain administrator can configure the scripting consumer.</span></span> <span data-ttu-id="6e53d-166">Zugriffsrechte werden bis zur Laufzeit nicht geprüft.</span><span class="sxs-lookup"><span data-stu-id="6e53d-166">Access rights are not checked until run time.</span></span> <span data-ttu-id="6e53d-167">Nachdem der Consumer konfiguriert wurde, kann jeder Benutzer das Ereignis, das das Skript verursacht, auslöst.</span><span class="sxs-lookup"><span data-stu-id="6e53d-167">After the consumer is configured, any user can trigger the event that causes the script to .</span></span>

<span data-ttu-id="6e53d-168">Fehler beim Laden der Skript-Engine oder beim Analysieren und Validieren des Skripts werden als Fehler betrachtet.</span><span class="sxs-lookup"><span data-stu-id="6e53d-168">Failure to load the scripting engine or parse and validate the script is considered a failure.</span></span> <span data-ttu-id="6e53d-169">Fehlerrückgabe Codes aus dem Skript und das Beenden des Skripts mit einem Timeout werden ebenfalls als Fehler betrachtet.</span><span class="sxs-lookup"><span data-stu-id="6e53d-169">Error return codes from the script and terminating the script by using a time-out are also considered failures.</span></span>

<span data-ttu-id="6e53d-170">Entweder ' **ScriptText** ' oder ' **scriptfilename** ' darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="6e53d-170">Either **ScriptText** or **ScriptFileName** must be not **NULL**.</span></span> <span data-ttu-id="6e53d-171">Wenn beide Eigenschaften **null** oder nicht **null** sind, wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="6e53d-171">If both properties are **NULL** or not **NULL**, an error is generated.</span></span>

<span data-ttu-id="6e53d-172">Wenn WMI als Dienst ausgeführt wird, generieren Skripts, die von **activescripteventconsumer** ausgeführt werden, keine Bildschirmausgabe.</span><span class="sxs-lookup"><span data-stu-id="6e53d-172">When WMI is run as a service, scripts run by **ActiveScriptEventConsumer** do not generate screen output.</span></span> <span data-ttu-id="6e53d-173">Skripts, die **MsgBox** verwenden, werden nicht auf dem Bildschirm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6e53d-173">Scripts that use **MsgBox** do run, but they do not display information on the screen.</span></span> <span data-ttu-id="6e53d-174">Das Ausführen des WMI-Dienstanbieter als ausführbare Datei wird nicht unterstützt, aber WMI ermöglicht es Skripts, die die **MsgBox** -Funktion verwenden, Ausgaben anzuzeigen oder Benutzereingaben zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="6e53d-174">Running the WMI service as an executable file is not supported, but WMI allows scripts that use the **MsgBox** function to display output or accept user input.</span></span> <span data-ttu-id="6e53d-175">Keine der vom [WScript](/previous-versions//at5ydy31(v=vs.85)) -Objekt bereitgestellten Methoden kann verwendet werden, da **activescripteventconsumer** Windows Script Host (WSH) nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e53d-175">None of the methods provided by the [WScript](/previous-versions//at5ydy31(v=vs.85)) object can be used because **ActiveScriptEventConsumer** does not use Windows Script Host (WSH).</span></span>

## <a name="examples"></a><span data-ttu-id="6e53d-176">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e53d-176">Examples</span></span>

<span data-ttu-id="6e53d-177">Das PowerShell-Beispiel [Erstellen permanenter WMI-Ereignis Registrierung zum Überwachen von Dateien](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) in der TechNet Gallery verwendet **activescripteventconsumer** als Teil eines komplexen Skripts, um eine permanente WMI-Ereignis Registrierung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="6e53d-177">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **ActiveScriptEventConsumer** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e53d-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e53d-178">Requirements</span></span>



| <span data-ttu-id="6e53d-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e53d-179">Requirement</span></span> | <span data-ttu-id="6e53d-180">Wert</span><span class="sxs-lookup"><span data-stu-id="6e53d-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e53d-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e53d-181">Minimum supported client</span></span><br/> | <span data-ttu-id="6e53d-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e53d-182">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6e53d-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e53d-183">Minimum supported server</span></span><br/> | <span data-ttu-id="6e53d-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e53d-184">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6e53d-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e53d-185">Namespace</span></span><br/>                | <span data-ttu-id="6e53d-186">Stamm \\ Abonnement</span><span class="sxs-lookup"><span data-stu-id="6e53d-186">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="6e53d-187">MOF</span><span class="sxs-lookup"><span data-stu-id="6e53d-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e53d-188"><dt>Scrcons. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6e53d-188"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e53d-189">DLL</span><span class="sxs-lookup"><span data-stu-id="6e53d-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e53d-190"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e53d-190"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e53d-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e53d-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e53d-192">Standard Consumer-Klassen</span><span class="sxs-lookup"><span data-stu-id="6e53d-192">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="6e53d-193">Ausführen eines Skripts auf der Grundlage eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="6e53d-193">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="6e53d-194">Empfangen von Ereignissen zu allen Zeitpunkten</span><span class="sxs-lookup"><span data-stu-id="6e53d-194">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="6e53d-195">Erstellen eines logischen Consumers</span><span class="sxs-lookup"><span data-stu-id="6e53d-195">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="6e53d-196">**\_\_Eventconsumer**</span><span class="sxs-lookup"><span data-stu-id="6e53d-196">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="6e53d-197">**Scriptingstandardconsumersetting**</span><span class="sxs-lookup"><span data-stu-id="6e53d-197">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md)
</dt> </dl>

 

