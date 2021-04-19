---
description: Die commandlineeventconsumer-Klasse startet einen beliebigen Prozess im lokalen System, wenn ein Ereignis an Sie übermittelt wird.
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: Commandlineeventconsumer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommandLineEventConsumer
- CommandLineEventConsumer.CreatorSID
- CommandLineEventConsumer.MachineName
- CommandLineEventConsumer.MaximumQueueSize
- CommandLineEventConsumer.CommandLineTemplate
- CommandLineEventConsumer.CreateNewConsole
- CommandLineEventConsumer.CreateNewProcessGroup
- CommandLineEventConsumer.CreateSeparateWowVdm
- CommandLineEventConsumer.CreateSharedWowVdm
- CommandLineEventConsumer.DesktopName
- CommandLineEventConsumer.ExecutablePath
- CommandLineEventConsumer.FillAttributes
- CommandLineEventConsumer.ForceOffFeedback
- CommandLineEventConsumer.ForceOnFeedback
- CommandLineEventConsumer.KillTimeout
- CommandLineEventConsumer.Name
- CommandLineEventConsumer.Priority
- CommandLineEventConsumer.RunInteractively
- CommandLineEventConsumer.ShowWindowCommand
- CommandLineEventConsumer.UseDefaultErrorMode
- CommandLineEventConsumer.WindowTitle
- CommandLineEventConsumer.WorkingDirectory
- CommandLineEventConsumer.XCoordinate
- CommandLineEventConsumer.XNumCharacters
- CommandLineEventConsumer.XSize
- CommandLineEventConsumer.YCoordinate
- CommandLineEventConsumer.YNumCharacters
- CommandLineEventConsumer.YSize
- CommandLineEventConsumer.FillAttribute
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 1784ba116417f6ed94aed2249a797cf8de4b3527
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106372552"
---
# <a name="commandlineeventconsumer-class"></a><span data-ttu-id="32f4f-103">Commandlineeventconsumer-Klasse</span><span class="sxs-lookup"><span data-stu-id="32f4f-103">CommandLineEventConsumer class</span></span>

<span data-ttu-id="32f4f-104">Die **commandlineeventconsumer** -Klasse startet einen beliebigen Prozess im lokalen System, wenn ein Ereignis an Sie übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-104">The **CommandLineEventConsumer** class starts an arbitrary process in the local system when an event is delivered to it.</span></span> <span data-ttu-id="32f4f-105">Diese Klasse ist einer der standardereignisconsumer, die von WMI bereitstellt werden.</span><span class="sxs-lookup"><span data-stu-id="32f4f-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="32f4f-106">Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="32f4f-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

> [!Note]  
> <span data-ttu-id="32f4f-107">Wenn Sie die **commandlineeventconsumer** -Klasse verwenden, sichern Sie die ausführbare Datei, die Sie starten möchten.</span><span class="sxs-lookup"><span data-stu-id="32f4f-107">When using the **CommandLineEventConsumer** class, secure the executable that you want to start.</span></span> <span data-ttu-id="32f4f-108">Wenn sich die ausführbare Datei nicht an einem sicheren Speicherort befindet oder durch eine sichere Zugriffs Steuerungs Liste (ACL) geschützt ist, kann ein nicht autorisierter Benutzer die ausführbare Datei durch eine böswillige ausführbare Datei ersetzen.</span><span class="sxs-lookup"><span data-stu-id="32f4f-108">If the executable is not in a secure location, or secured with a strong access control list (ACL), an unauthorized user can replace your executable with a malicious executable.</span></span> <span data-ttu-id="32f4f-109">Weitere Informationen zu ACLs finden Sie im Abschnitt "Sicherheit" des Microsoft Windows Software Development Kit (SDK) und unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="32f4f-109">For more information about ACLs, visit the Security section of the Microsoft Windows Software Development Kit (SDK), and see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="32f4f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="32f4f-110">Syntax</span></span>

``` syntax
[AMENDMENT]
class CommandLineEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  CommandLineTemplate;
  boolean CreateNewConsole = False;
  boolean CreateNewProcessGroup = True;
  boolean CreateSeparateWowVdm = False;
  boolean CreateSharedWowVdm = False;
  string  DesktopName;
  string  ExecutablePath;
  uint32  FillAttributes;
  boolean ForceOffFeedback = False;
  boolean ForceOnFeedback = False;
  uint32  KillTimeout = 0;
  string  Name;
  sint32  Priority = 0x20;
  boolean RunInteractively = False;
  uint32  ShowWindowCommand;
  boolean UseDefaultErrorMode = False;
  string  WindowTitle;
  string  WorkingDirectory;
  uint32  XCoordinate;
  uint32  XNumCharacters;
  uint32  XSize;
  uint32  YCoordinate;
  uint32  YNumCharacters;
  uint32  YSize;
  uint32  FillAttribute;
};
```

## <a name="members"></a><span data-ttu-id="32f4f-111">Member</span><span class="sxs-lookup"><span data-stu-id="32f4f-111">Members</span></span>

<span data-ttu-id="32f4f-112">Die **commandlineeventconsumer** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="32f4f-112">The **CommandLineEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="32f4f-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="32f4f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32f4f-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="32f4f-114">Properties</span></span>

<span data-ttu-id="32f4f-115">Die **commandlineeventconsumer** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="32f4f-115">The **CommandLineEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32f4f-116">**Commandlinetemplate**</span><span class="sxs-lookup"><span data-stu-id="32f4f-116">**CommandLineTemplate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="32f4f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-119">Standard Zeichen folgen Vorlage, die den zu startenden Prozess angibt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-119">Standard string template that specifies the process to be started.</span></span> <span data-ttu-id="32f4f-120">Diese Eigenschaft kann **null** sein, und die **ExecutablePath** -Eigenschaft wird als Befehlszeile verwendet.</span><span class="sxs-lookup"><span data-stu-id="32f4f-120">This property can be **NULL**, and the **ExecutablePath** property is used as the command line.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-121">**"Kreatenewconsole"**</span><span class="sxs-lookup"><span data-stu-id="32f4f-121">**CreateNewConsole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-122">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="32f4f-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="32f4f-124">Not used.</span></span> <span data-ttu-id="32f4f-125">Wenn dieser Eigenschaft ein Wert zugewiesen wird, wird eine Ablauf Verfolgungs Meldung generiert.</span><span class="sxs-lookup"><span data-stu-id="32f4f-125">If a value is assigned to this property, a tracing message is generated.</span></span> <span data-ttu-id="32f4f-126">Weitere Informationen finden Sie unter Ablauf [Verfolgung von WMI-Aktivitäten](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="32f4f-126">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-127">**"Kreatenewprocessgroup"**</span><span class="sxs-lookup"><span data-stu-id="32f4f-127">**CreateNewProcessGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="32f4f-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-130">**True** gibt an, dass der neue Prozess der Stamm Prozess einer neuen Prozessgruppe ist.</span><span class="sxs-lookup"><span data-stu-id="32f4f-130">If **True**, the new process is the root process of a new process group.</span></span> <span data-ttu-id="32f4f-131">Die Prozessgruppe umfasst alle Prozesse, bei denen es sich um nachfolgende Elemente dieses Stamm Prozesses handelt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-131">The process group includes all processes that are descendants of this root process.</span></span> <span data-ttu-id="32f4f-132">Der Prozess Bezeichner der neuen Prozessgruppe ist mit diesem Prozess Bezeichner identisch.</span><span class="sxs-lookup"><span data-stu-id="32f4f-132">The process identifier of the new process group is the same as this process identifier.</span></span> <span data-ttu-id="32f4f-133">Prozessgruppen werden von der [**generateconsolectrlevent**](/windows/console/generateconsolectrlevent) -Methode verwendet, um das Senden eines STRG + C-oder STRG + Break-Signals an eine Gruppe von Konsolen Prozessen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="32f4f-133">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable sending a CTRL+C or CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-134">**"Kreateseparser"**</span><span class="sxs-lookup"><span data-stu-id="32f4f-134">**CreateSeparateWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-135">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="32f4f-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-137">**True** gibt an, dass der neue Prozess in einem privaten virtuellen DOS-Computer (VDM) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-137">If **True**, the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="32f4f-138">Dies ist nur gültig, wenn eine Anwendung gestartet wird, die auf einem 16-Bit-Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-138">This is only valid when starting an application running on a 16-bit Windows operating system.</span></span> <span data-ttu-id="32f4f-139">Wenn **false** festgelegt ist, werden alle Anwendungen, die auf einem 16-Bit-Windows-Betriebssystem ausgeführt werden, als Threads in einem einzelnen, freigegebenen VDM ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-139">If set to **False**, all applications running on a 16-bit Windows operating system run as threads in a single, shared VDM.</span></span> <span data-ttu-id="32f4f-140">Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="32f4f-140">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-141">**"Kreatesharedwowvdm"**</span><span class="sxs-lookup"><span data-stu-id="32f4f-141">**CreateSharedWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-142">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="32f4f-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-144">**True** gibt an, dass die Methode " [**kreateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " den neuen Prozess auf dem freigegebenen virtuellen DOS-Computer (VDM) ausführt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-144">If **True**, the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method runs the new process in the shared Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="32f4f-145">Diese Eigenschaft kann den Schalter defaultseparatevdm im Windows-Abschnitt von Win.ini überschreiben, wenn der Wert auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="32f4f-145">This property can override the DefaultSeparateVDM switch in the Windows section of Win.ini if set to **True**.</span></span> <span data-ttu-id="32f4f-146">Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="32f4f-146">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-147">**"Kreatorsid"**</span><span class="sxs-lookup"><span data-stu-id="32f4f-147">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-148">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="32f4f-148">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-150">Sicherheits-ID (SID), die den Benutzer, der einen Filter erstellt, eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="32f4f-150">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="32f4f-151">WMI speichert die SID des Benutzers, der eine Instanz von [**\_ \_ eventconsumer**](--eventconsumer.md) oder die Administrator-SID erstellt, je nach Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="32f4f-151">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="32f4f-152">Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="32f4f-152">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="32f4f-153">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-153">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-154">**Desktopname**</span><span class="sxs-lookup"><span data-stu-id="32f4f-154">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="32f4f-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-157">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="32f4f-157">Not used.</span></span> <span data-ttu-id="32f4f-158">Wenn dieser Eigenschaft ein Wert zugewiesen wird, wird eine Ablauf Verfolgungs Meldung generiert.</span><span class="sxs-lookup"><span data-stu-id="32f4f-158">If a value is assigned to this property a tracing message is generated.</span></span> <span data-ttu-id="32f4f-159">Weitere Informationen finden Sie unter Ablauf [Verfolgung von WMI-Aktivitäten](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="32f4f-159">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-160">**ExecutablePath**</span><span class="sxs-lookup"><span data-stu-id="32f4f-160">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="32f4f-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-163">Auszuführenden Modul.</span><span class="sxs-lookup"><span data-stu-id="32f4f-163">Module to execute.</span></span> <span data-ttu-id="32f4f-164">Die Zeichenfolge kann den vollständigen Pfad und den Dateinamen des auszuführenden Moduls angeben, oder es kann ein partieller Name angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="32f4f-164">The string can specify the full path and file name of the module to execute, or it can specify a partial name.</span></span> <span data-ttu-id="32f4f-165">Wenn ein partieller Name angegeben ist, wird das aktuelle Laufwerk und das aktuelle Verzeichnis angenommen.</span><span class="sxs-lookup"><span data-stu-id="32f4f-165">If a partial name is specified, the current drive and current directory are assumed.</span></span>

<span data-ttu-id="32f4f-166">Die **ExecutablePath** -Eigenschaft kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="32f4f-166">The **ExecutablePath** property can be **NULL**.</span></span> <span data-ttu-id="32f4f-167">In diesem Fall muss der Modulname das erste durch Leerzeichen getrennte Token im **commandlinetemplate** -Eigenschafts Wert sein.</span><span class="sxs-lookup"><span data-stu-id="32f4f-167">In that case, the module name must be the first white space-delimited token in the **CommandLineTemplate** property value.</span></span> <span data-ttu-id="32f4f-168">Wenn Sie einen langen Dateinamen verwenden, der ein Leerzeichen enthält, verwenden Sie Zeichen folgen in Anführungszeichen, um anzugeben, wo der Dateiname endet und die Argumente beginnen, den Dateinamen zu verdeutlichen</span><span class="sxs-lookup"><span data-stu-id="32f4f-168">If using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin to clarify the file name.</span></span>

> [!Note]  
> <span data-ttu-id="32f4f-169">Da die **commandlinetemplate** -Eigenschaft eine Vorlage sein kann, in der das auszuführende Modul von einer Variablen bereitgestellt wird, ermöglicht eine **ExecutablePath** -Eigenschaft von **null** , dass das im-Parameter angegebene Modul ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-169">Because the **CommandLineTemplate** property can be a template where the module to execute is supplied by a variable, a **NULL** **ExecutablePath** property permits the module that is specified in the parameter to execute, and then it is out of your control.</span></span> <span data-ttu-id="32f4f-170">Legen Sie die **ExecutablePath** -Eigenschaft in der **commandlineeventconsumer** -Registrierung immer auf die erforderliche ausführbare Datei fest, wodurch das Überschreiben von Ereignis Parametern vermieden wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-170">Always set the **ExecutablePath** property in the **CommandLineEventConsumer** registration to include the required executable, which avoids overwriting by events parameters.</span></span> <span data-ttu-id="32f4f-171">Wenn Sie eine Vorlage und eine Variable verwenden müssen, um das auszuführende Modul anzugeben, achten Sie darauf, wem das vollständige Schreib Privileg im-Namespace erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-171">If you must use a template and variable to specify the module to execute, be careful about who is granted full write privilege in the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="32f4f-172">**FillAttribute**</span><span class="sxs-lookup"><span data-stu-id="32f4f-172">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-173">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f4f-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-175">Gibt die Anfangstext-und Hintergrundfarben an, wenn ein neues Konsolenfenster in einer Konsolenanwendung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-175">Specifies the initial text and background colors if a new console window is created in a console application</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-176">**FillAttribute**</span><span class="sxs-lookup"><span data-stu-id="32f4f-176">**FillAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-177">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f4f-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="32f4f-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-179">Anfängliche Text-und Hintergrundfarben, wenn ein neues Konsolenfenster in einer Konsolenanwendung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-179">Initial text and background colors, if a new console window is created in a console application.</span></span> <span data-ttu-id="32f4f-180">Diese Eigenschaft wird in einer GUI-Anwendung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="32f4f-180">This property is ignored in a GUI application.</span></span> <span data-ttu-id="32f4f-181">Der Wert kann eine beliebige Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="32f4f-181">The value can be any combination of the following values.</span></span>

<dt>

<span data-ttu-id="32f4f-182">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="32f4f-182">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="32f4f-183">Blauer Vordergrund</span><span class="sxs-lookup"><span data-stu-id="32f4f-183">blue foreground</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-184">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="32f4f-184">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="32f4f-185">grüner Vordergrund</span><span class="sxs-lookup"><span data-stu-id="32f4f-185">green foreground</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-186">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="32f4f-186">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="32f4f-187">Roter Vordergrund</span><span class="sxs-lookup"><span data-stu-id="32f4f-187">red foreground</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-188">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="32f4f-188">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="32f4f-189">Vordergrund Intensität</span><span class="sxs-lookup"><span data-stu-id="32f4f-189">foreground intensity</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-190">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="32f4f-190">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="32f4f-191">Blauer Hintergrund</span><span class="sxs-lookup"><span data-stu-id="32f4f-191">blue background</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-192">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="32f4f-192">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="32f4f-193">Grüner Hintergrund</span><span class="sxs-lookup"><span data-stu-id="32f4f-193">green background</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-194">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="32f4f-194">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="32f4f-195">Roter Hintergrund</span><span class="sxs-lookup"><span data-stu-id="32f4f-195">red background</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-196">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="32f4f-196">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="32f4f-197">Hintergrund Intensität</span><span class="sxs-lookup"><span data-stu-id="32f4f-197">background intensity</span></span>

</dd> </dl>

<span data-ttu-id="32f4f-198">Beispielsweise wird in den folgenden Kombinationen roter Text auf einem weißen Hintergrund erzeugt:</span><span class="sxs-lookup"><span data-stu-id="32f4f-198">For example, the following combinations produce red text on a white background:</span></span>


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  <span data-ttu-id="32f4f-199">oder</span><span class="sxs-lookup"><span data-stu-id="32f4f-199">or</span></span>  


```mof
0x74
```



</dd> <dt>

<span data-ttu-id="32f4f-200">**Forceofffeedback**</span><span class="sxs-lookup"><span data-stu-id="32f4f-200">**ForceOffFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-201">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="32f4f-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-203">**True** gibt an, dass der Feedback Cursor beim Start des Prozesses erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-203">If **True**, the feedback cursor is forced off while the process is starting.</span></span> <span data-ttu-id="32f4f-204">Der normale Cursor wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-204">The normal cursor is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-205">**Forceonfeedback**</span><span class="sxs-lookup"><span data-stu-id="32f4f-205">**ForceOnFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-206">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="32f4f-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-208">**True** gibt an, dass sich der Cursor zwei Sekunden nach dem Aufruf von " [**kreateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " im Feedback Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="32f4f-208">If **True**, the cursor is in feedback mode for two seconds after [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) is called.</span></span> <span data-ttu-id="32f4f-209">Wenn während dieser zwei Sekunden der Prozess den ersten GUI-Befehl aufruft, gibt das System fünf weitere Sekunden an den Prozess.</span><span class="sxs-lookup"><span data-stu-id="32f4f-209">During those two seconds, if the process makes the first GUI call, the system gives five more seconds to the process.</span></span> <span data-ttu-id="32f4f-210">In diesen fünf Sekunden gibt das System, wenn der Prozess ein Fenster anzeigt, weitere fünf Sekunden an den Prozess, um das Zeichnen des Fensters abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="32f4f-210">During those five seconds, if the process shows a window, the system gives another five seconds to the process to finish drawing the window.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-211">**Killtimeout**</span><span class="sxs-lookup"><span data-stu-id="32f4f-211">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-212">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f4f-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-214">Die Anzahl (in Sekunden), die der WMI-Dienst wartet, bevor er einen Prozess 0 (null) beendet, gibt an, dass ein Prozess nicht abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="32f4f-214">Number, in seconds, that the WMI service waits before killing a process 0 (zero) indicates a process is not to be killed.</span></span> <span data-ttu-id="32f4f-215">Durch das Abbrechen eines Prozesses wird verhindert, dass ein Prozess unbegrenzt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-215">Killing a process prevents a process from running indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-216">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="32f4f-216">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="32f4f-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-219">Der Name des Computers, an den Windows-Verwaltungsinstrumentation (WMI) Ereignisse sendet.</span><span class="sxs-lookup"><span data-stu-id="32f4f-219">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="32f4f-220">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-220">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-221">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="32f4f-221">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-222">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f4f-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-224">Maximale Warteschlange für einen bestimmten Consumer in Bytes.</span><span class="sxs-lookup"><span data-stu-id="32f4f-224">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="32f4f-225">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-225">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-226">**Name**</span><span class="sxs-lookup"><span data-stu-id="32f4f-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="32f4f-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-229">Qualifizierer: [ **Schlüssel**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="32f4f-229">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-230">Der eindeutige Name eines Consumers.</span><span class="sxs-lookup"><span data-stu-id="32f4f-230">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-231">**Priority**</span><span class="sxs-lookup"><span data-stu-id="32f4f-231">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-232">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32f4f-232">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-234">Planen der Prioritätsstufe der Prozessthreads.</span><span class="sxs-lookup"><span data-stu-id="32f4f-234">Scheduling priority level of the process threads.</span></span> <span data-ttu-id="32f4f-235">In der folgenden Liste sind die verfügbaren Prioritätsstufen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-235">The following list lists the priority levels available.</span></span>

<dt>

<span data-ttu-id="32f4f-236">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="32f4f-236">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="32f4f-237">Gibt einen normalen Prozess ohne Planungsanforderungen an.</span><span class="sxs-lookup"><span data-stu-id="32f4f-237">Indicates a normal process without scheduling needs.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-238">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="32f4f-238">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="32f4f-239">Gibt einen Prozess an, dessen Threads nur ausgeführt werden, wenn sich das System im Leerlauf befindet. Sie werden von den Threads eines Prozesses, der in einer höheren Prioritäts Klasse ausgeführt wird, vorzeitig entfernt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-239">Indicates a process whose threads run only when the system is idle, and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="32f4f-240">Ein Beispiel hierfür ist ein Bildschirmschoner.</span><span class="sxs-lookup"><span data-stu-id="32f4f-240">An example is a screen saver.</span></span> <span data-ttu-id="32f4f-241">Die inaktive Prioritäts Klasse wird von untergeordneten Prozessen geerbt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-241">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-242">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="32f4f-242">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="32f4f-243">Gibt einen Prozess an, der zeitkritische Aufgaben mit hoher Priorität ausführt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-243">Indicates a process that performs high-priority, time critical tasks.</span></span> <span data-ttu-id="32f4f-244">In den Threads eines Klassen Prozesses mit hoher Priorität werden die Threads von Klassen Prozessen mit normaler Priorität oder der Leerlauf Priorität vorzeitig entfernt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-244">The threads of a high-priority class process preempts the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="32f4f-245">Ein Beispiel hierfür ist die Aufgabenliste, die schnell reagieren muss, wenn der Benutzer unabhängig von der System Auslastung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-245">An example is the Task List, which must respond quickly when called by the user regardless of the load on the system.</span></span> <span data-ttu-id="32f4f-246">Verwenden Sie extrem Sorgfalt bei der Verwendung der Klasse mit hoher Priorität, da eine CPU-gebundene Anwendung mit einer Klasse mit hoher Priorität fast alle verfügbaren Zyklen verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="32f4f-246">Use extreme care when using the high-priority class, because a CPU-bound application with a high-priority class can use nearly all available cycles.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-247">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="32f4f-247">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="32f4f-248">Gibt einen Prozess an, der über die höchste mögliche Priorität verfügt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-248">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="32f4f-249">Die Threads eines Echtzeit-Prioritäts Klassen Prozesses haben Vorrang vor den Threads aller anderen Prozesse, einschließlich der Betriebssystem Prozesse, von denen wichtige Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="32f4f-249">The threads of a real-time priority class process preempt the threads of all other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="32f4f-250">Beispielsweise kann ein echt Zeit Prozess, der für mehr als ein kurzes Intervall ausgeführt wird, dazu führen, dass Datenträger Caches nicht geleert werden oder die Maus nicht reagiert.</span><span class="sxs-lookup"><span data-stu-id="32f4f-250">For example, a real-time process that executes for more than a brief interval can cause disk caches not to flush, or cause the mouse to be unresponsive.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="32f4f-251">**Runinteraktiv**</span><span class="sxs-lookup"><span data-stu-id="32f4f-251">**RunInteractively**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-252">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="32f4f-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-254">**True** gibt an, dass der Prozess in der interaktiven WinStation gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-254">If **True**, the process is launched in the interactive WinStation.</span></span> <span data-ttu-id="32f4f-255">Wenn der Wert **false** ist, wird der Prozess in der standardmäßigen Dienst-WinStation gestartet.</span><span class="sxs-lookup"><span data-stu-id="32f4f-255">If **False**, the process is launched in the default service WinStation.</span></span> <span data-ttu-id="32f4f-256">Diese Eigenschaft überschreibt die **Desktopname** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="32f4f-256">This property overrides the **DesktopName** property.</span></span> <span data-ttu-id="32f4f-257">Diese Eigenschaft wird nur lokal und nur dann verwendet, wenn es sich bei dem interaktiven Benutzer um denselben Benutzer handelt, der den Consumer eingerichtet hat.</span><span class="sxs-lookup"><span data-stu-id="32f4f-257">This property is only used locally, and only if the interactive user is the same user who set up the consumer.</span></span>

<span data-ttu-id="32f4f-258">Ab Windows Vista wird der Prozess, der die **commandlineeventconsumer** -Instanz ausgeführt wird, unter dem Konto " **LocalSystem** " gestartet und befindet sich in Sitzung 0.</span><span class="sxs-lookup"><span data-stu-id="32f4f-258">Starting with Windows Vista, the process running the **CommandLineEventConsumer** instance is started under the **LocalSystem** account and is in session 0.</span></span> <span data-ttu-id="32f4f-259">Dienste, die in Sitzung 0 ausgeführt werden, können nicht mit Benutzersitzungen interagieren.</span><span class="sxs-lookup"><span data-stu-id="32f4f-259">Services which run in session 0 cannot interact with user sessions.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-260">**Showwindowcommand**</span><span class="sxs-lookup"><span data-stu-id="32f4f-260">**ShowWindowCommand**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-261">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f4f-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-263">Fenster Anzeige Zustand.</span><span class="sxs-lookup"><span data-stu-id="32f4f-263">Window show state.</span></span> <span data-ttu-id="32f4f-264">Dabei kann es sich um einen beliebigen Wert handeln, der im *nCmdShow* -Parameter für die [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) -Funktion angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="32f4f-264">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-265">**Usedefaulterrormode**</span><span class="sxs-lookup"><span data-stu-id="32f4f-265">**UseDefaultErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-266">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="32f4f-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-268">**True** gibt an, dass der Standardfehler Modus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-268">If **True**, the default error mode is used.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-269">**WindowTitle**</span><span class="sxs-lookup"><span data-stu-id="32f4f-269">**WindowTitle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-270">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="32f4f-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-271">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-272">Der Titel, der in der Titelleiste des Prozesses angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-272">Title that appears on the title bar of the process.</span></span> <span data-ttu-id="32f4f-273">Diese Eigenschaft wird für GUI-Anwendungen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="32f4f-273">This property is ignored for GUI applications.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-274">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="32f4f-274">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-275">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="32f4f-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-277">Arbeitsverzeichnis für diesen Prozess.</span><span class="sxs-lookup"><span data-stu-id="32f4f-277">Working directory for this process.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-278">**Xkoordinate**</span><span class="sxs-lookup"><span data-stu-id="32f4f-278">**XCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-279">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f4f-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-281">X-Offset in Pixel vom linken Rand des Bildschirms bis zum linken Rand des Fensters, wenn ein neues Fenster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-281">X-offset, in pixels, from the left edge of the screen to the left edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-282">**Xnumcharacter**</span><span class="sxs-lookup"><span data-stu-id="32f4f-282">**XNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-283">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f4f-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-285">Bildschirm Puffer Breite (in Zeichen Spalten), wenn ein neues Konsolenfenster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-285">Screen buffer width, in character columns, if a new console window is created.</span></span> <span data-ttu-id="32f4f-286">Diese Eigenschaft wird in einem GUI-Prozess ignoriert.</span><span class="sxs-lookup"><span data-stu-id="32f4f-286">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-287">**Xsize**</span><span class="sxs-lookup"><span data-stu-id="32f4f-287">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-288">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f4f-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-290">Breite eines neuen Fensters in Pixel, wenn ein neues Fenster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-290">Width, in pixels, of a new window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-291">**Ykoordinate**</span><span class="sxs-lookup"><span data-stu-id="32f4f-291">**YCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-292">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f4f-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-294">Y-Offset (in Pixel) vom oberen Rand des Bildschirms bis zum oberen Rand des Fensters, wenn ein neues Fenster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-294">Y-offset, in pixels, from the top edge of the screen to the top edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-295">**Ynumcharacters**</span><span class="sxs-lookup"><span data-stu-id="32f4f-295">**YNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-296">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f4f-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-298">Die Höhe des Bildschirm Puffers in Zeichen Zeilen, wenn ein neues Konsolenfenster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-298">Screen buffer height, in character rows, if a new console window is created.</span></span> <span data-ttu-id="32f4f-299">Diese Eigenschaft wird in einem GUI-Prozess ignoriert.</span><span class="sxs-lookup"><span data-stu-id="32f4f-299">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="32f4f-300">**Ysize**</span><span class="sxs-lookup"><span data-stu-id="32f4f-300">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f4f-301">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32f4f-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f4f-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32f4f-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32f4f-303">Die Höhe des neuen Fensters in Pixel, wenn ein neues Fenster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-303">Height, in pixels, of the new window, if a new window is created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32f4f-304">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32f4f-304">Remarks</span></span>

<span data-ttu-id="32f4f-305">Die **commandlineeventconsumer** -Klasse wird von der [**\_ \_ eventconsumer**](--eventconsumer.md) abstract-Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="32f4f-305">The **CommandLineEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="32f4f-306">Die Eigenschaft " **kreateseparametewowvdm** " gibt an, ob der neue Prozess in einem privaten virtuellen DOS-Computer (VDM) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32f4f-306">The **CreateSeparateWowVdm** property indicates whether or not the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="32f4f-307">Der Vorteil der separaten Ausführung besteht darin, dass ein Absturz nur den einzelnen VDM beendet.</span><span class="sxs-lookup"><span data-stu-id="32f4f-307">The advantage of running separately is that a crash only terminates the single VDM.</span></span> <span data-ttu-id="32f4f-308">Programme, die auf unterschiedlichen VDMs ausgeführt werden, funktionieren weiterhin normal, und die 16-Bit-Windows-basierten Anwendungen, die in separaten VDMs ausgeführt werden, haben separate Eingabe Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="32f4f-308">Programs running in distinct VDMs continue to function normally, and the 16-bit Windows-based applications running in separate VDMs have separate input queues.</span></span> <span data-ttu-id="32f4f-309">Dies bedeutet, dass die Anwendungen in separaten VDMs weiterhin Eingaben empfangen, wenn eine Anwendung nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="32f4f-309">This means that if one application stops responding momentarily, the applications in separate VDMs continue to receive input.</span></span> <span data-ttu-id="32f4f-310">Der Nachteil der separaten Ausführung besteht darin, dass es erheblich mehr Arbeitsspeicher benötigt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-310">The disadvantage of running separately is that it takes significantly more memory to do so.</span></span> <span data-ttu-id="32f4f-311">Legen Sie diese Eigenschaft nur dann auf **true** fest, wenn der Benutzer anfordert, dass 16-Bit-Windows-basierte Anwendungen in Ihrem eigenen VDM ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="32f4f-311">You should set this property to **True** only if the user requests that 16-bit Windows-based applications run in their own VDM.</span></span>

> [!Note]  
> <span data-ttu-id="32f4f-312">**Commandlineeventconsumer** verwendet intern die Methode " [**kreateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " und übergibt die Eigenschaften **ExecutablePath** und **commandlinetemplate** als *lpApplicationName* -und *lpCommandLine* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="32f4f-312">The **CommandLineEventConsumer** uses the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method internally, and passes the **ExecutablePath** and **CommandLineTemplate** properties as the *lpApplicationName* and *lpCommandLine* parameters.</span></span> <span data-ttu-id="32f4f-313">Im folgenden Managed Object Format (MOF)-Codebeispiel wird **commandlineeventconsumer** nicht ordnungsgemäß verwendet.</span><span class="sxs-lookup"><span data-stu-id="32f4f-313">The following Managed Object Format (MOF) code example does not use **CommandLineEventConsumer** correctly.</span></span>

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="32f4f-314">Die Methode " [**kreateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " übergibt *lpCommandLine* als `argv[0]` , `argv[1]` usw.</span><span class="sxs-lookup"><span data-stu-id="32f4f-314">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method passes *lpCommandLine* as `argv[0]`, `argv[1]`, and so on.</span></span> <span data-ttu-id="32f4f-315">Da `argv[0]` für 16-Bit-Anwendungen, die für den Namen der ausführbaren Datei reserviert sind, der vorherige MOF-Code dazu führt, dass der Prozess erstellt wird, als ob der folgende Befehl an der Eingabeaufforderung eingegeben wird: **c: \\ Windows \\ system32 \\cscript.exe param1 Param2**.</span><span class="sxs-lookup"><span data-stu-id="32f4f-315">Because `argv[0]` for 16-bit applications used to be reserved for the executable file name, the previous MOF code results in the process being created as though the following command is entered at the command prompt: **c:\\windows\\system32\\cscript.exe param1 param2**.</span></span>

<span data-ttu-id="32f4f-316">Der vorherige Befehl ist nicht erfolgreich, da sich Cscript.exe nicht untersucht `argv[0]` und somit nicht erkennt, dass er keinen eigenen Namen, sondern etwas anderes ("c: \\ \\ Scripts \\ \\MyScript.js") enthält.</span><span class="sxs-lookup"><span data-stu-id="32f4f-316">The previous command does not succeed because Cscript.exe does not look at `argv[0]`, and so it does not recognize that it does not contain its own name, but something else ("c:\\\\scripts\\\\MyScript.js").</span></span> <span data-ttu-id="32f4f-317">Im folgenden Beispiel wird die empfohlene Verwendung von **commandlineeventconsumer** identifiziert.</span><span class="sxs-lookup"><span data-stu-id="32f4f-317">The following example identifies the recommended use of **CommandLineEventConsumer**.</span></span>


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="32f4f-318">Die vorherige Verwendung von **commandlineeventconsumer** führt dazu, dass der Prozess erstellt wird, als ob der folgende Befehl an der Eingabeaufforderung eingegeben wurde: **c: \\ Windows \\ system32 \\cscript.exe c: \\ Scripts \\MyScript.js param1 Param2**</span><span class="sxs-lookup"><span data-stu-id="32f4f-318">The previous use of **CommandLineEventConsumer** results in the process created as though the following command was entered at the command prompt: **c:\\windows\\system32\\cscript.exe c:\\scripts\\MyScript.js param1 param2**</span></span>

<span data-ttu-id="32f4f-319">Da "c: \\ \\ Scripts \\ \\MyScript.js" jetzt ist `argv[1]` , wird es von Cscript.exe erkannt, und der Befehl wird erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32f4f-319">Because "c:\\\\scripts\\\\MyScript.js" is now `argv[1]`, it is seen by Cscript.exe and the command succeeds.</span></span>

<span data-ttu-id="32f4f-320">Weitere Informationen finden Sie unter der Funktion "up- [**Process**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) ".</span><span class="sxs-lookup"><span data-stu-id="32f4f-320">For more information, see the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="32f4f-321">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32f4f-321">Examples</span></span>

<span data-ttu-id="32f4f-322">Ein Beispiel für die Verwendung von **commandlineeventconsumer** , um einen Consumer zu erstellen, finden Sie unter [Ausführen eines Programms in der Befehlszeile auf der Grundlage eines Ereignisses](running-a-program-from-the-command-line-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="32f4f-322">For an example of using **CommandLineEventConsumer** to create a consumer, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32f4f-323">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32f4f-323">Requirements</span></span>



| <span data-ttu-id="32f4f-324">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32f4f-324">Requirement</span></span> | <span data-ttu-id="32f4f-325">Wert</span><span class="sxs-lookup"><span data-stu-id="32f4f-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32f4f-326">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32f4f-326">Minimum supported client</span></span><br/> | <span data-ttu-id="32f4f-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32f4f-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32f4f-328">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32f4f-328">Minimum supported server</span></span><br/> | <span data-ttu-id="32f4f-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32f4f-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32f4f-330">Namespace</span><span class="sxs-lookup"><span data-stu-id="32f4f-330">Namespace</span></span><br/>                | <span data-ttu-id="32f4f-331">Stamm \\ Abonnement</span><span class="sxs-lookup"><span data-stu-id="32f4f-331">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="32f4f-332">MOF</span><span class="sxs-lookup"><span data-stu-id="32f4f-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32f4f-333"><dt>Wbemcons. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="32f4f-333"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="32f4f-334">DLL</span><span class="sxs-lookup"><span data-stu-id="32f4f-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32f4f-335"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32f4f-335"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32f4f-336">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32f4f-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f4f-337">Standard Consumer-Klassen</span><span class="sxs-lookup"><span data-stu-id="32f4f-337">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="32f4f-338">Überwachen von und reagieren auf Ereignisse mit Standard Consumern</span><span class="sxs-lookup"><span data-stu-id="32f4f-338">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="32f4f-339">Erstellen eines logischen Consumers</span><span class="sxs-lookup"><span data-stu-id="32f4f-339">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="32f4f-340">Empfangen von Ereignissen zu allen Zeitpunkten</span><span class="sxs-lookup"><span data-stu-id="32f4f-340">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="32f4f-341">**\_\_Eventconsumer**</span><span class="sxs-lookup"><span data-stu-id="32f4f-341">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

