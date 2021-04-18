---
title: Win32_TSPublishedApplication-Klasse
description: Definiert die Anwendungen, die für die Remote Verwendung über Windows Server 2008 R2 RemoteApp verfügbar gemacht werden.
ms.assetid: 5b9cb36b-3d8d-4105-acea-c79440d977fe
ms.tgt_platform: multiple
keywords:
- Win32_TSPublishedApplication-Klasse Remotedesktopdienste
- Win32_TSPublishedApplication Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplication
- Win32_TSPublishedApplication.Caption
- Win32_TSPublishedApplication.Description
- Win32_TSPublishedApplication.InstallDate
- Win32_TSPublishedApplication.Name
- Win32_TSPublishedApplication.Status
- Win32_TSPublishedApplication.Alias
- Win32_TSPublishedApplication.SecurityDescriptor
- Win32_TSPublishedApplication.Path
- Win32_TSPublishedApplication.PathExists
- Win32_TSPublishedApplication.VPath
- Win32_TSPublishedApplication.IconPath
- Win32_TSPublishedApplication.IconIndex
- Win32_TSPublishedApplication.IconContents
- Win32_TSPublishedApplication.CommandLineSetting
- Win32_TSPublishedApplication.RequiredCommandLine
- Win32_TSPublishedApplication.ShowInPortal
- Win32_TSPublishedApplication.RDPFileContents
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3825087d05b622818c74f011f30b325ed8ff7f60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337924"
---
# <a name="win32_tspublishedapplication-class"></a><span data-ttu-id="7fd2e-105">Win32 \_ tspublishedappliationklasse</span><span class="sxs-lookup"><span data-stu-id="7fd2e-105">Win32\_TSPublishedApplication class</span></span>

<span data-ttu-id="7fd2e-106">Definiert die Anwendungen, die für die Remote Verwendung über Windows Server 2008 R2 RemoteApp verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-106">Defines the applications that are made available for remote use through Windows Server 2008 R2 RemoteApp.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd2e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fd2e-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  boolean  PathExists;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   RDPFileContents;
};
```

## <a name="members"></a><span data-ttu-id="7fd2e-108">Member</span><span class="sxs-lookup"><span data-stu-id="7fd2e-108">Members</span></span>

<span data-ttu-id="7fd2e-109">Die **Win32 \_ tspublishedappliationklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7fd2e-109">The **Win32\_TSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="7fd2e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7fd2e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7fd2e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7fd2e-111">Properties</span></span>

<span data-ttu-id="7fd2e-112">Die **Win32 \_ tspublishedappliationklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-112">The **Win32\_TSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7fd2e-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7fd2e-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-116">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-117">Der Alias der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-117">The alias of the application.</span></span> <span data-ttu-id="7fd2e-118">Der Alias ist ein eindeutiger Bezeichner für das Programm, das standardmäßig auf den Dateinamen des Programms (ohne Erweiterung) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-118">The alias is a unique identifier for the program that defaults to the program's file name (without the extension).</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd2e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-122">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7fd2e-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-123">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="7fd2e-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-125">**Commandlinesesetting**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-125">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-126">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7fd2e-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-128">Die Befehlszeilenargumente-Einstellung für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-128">The command-line arguments setting for the application.</span></span> <span data-ttu-id="7fd2e-129">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-129">The following values are possible.</span></span>

<dt>

<span data-ttu-id="7fd2e-130">0</span><span class="sxs-lookup"><span data-stu-id="7fd2e-130">0</span></span>
</dt> <dd>

<span data-ttu-id="7fd2e-131">Befehlszeilenargumente dürfen nicht zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-131">Do not allow command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-132">1</span><span class="sxs-lookup"><span data-stu-id="7fd2e-132">1</span></span>
</dt> <dd>

<span data-ttu-id="7fd2e-133">Hiermit werden Befehlszeilenargumente zugelassen.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-133">Allow any command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-134">2</span><span class="sxs-lookup"><span data-stu-id="7fd2e-134">2</span></span>
</dt> <dd>

<span data-ttu-id="7fd2e-135">Verwenden Sie immer die erforderlichen Befehlszeilenargumente (in "Requirements **dcommandline**" angegeben).</span><span class="sxs-lookup"><span data-stu-id="7fd2e-135">Always use the required command-line arguments (specified in **RequiredCommandLine**).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7fd2e-136">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd2e-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-139">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-139">Description of the object.</span></span>

<span data-ttu-id="7fd2e-140">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-141">**Iconcontent**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-141">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-142">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="7fd2e-142">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd2e-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-144">Der Byte Inhalt des Symbols, das der Anwendung entspricht.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-144">The byte contents of the icon that corresponds to the application.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-145">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-145">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-146">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-147">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7fd2e-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-148">Der Index oder die ID des Symbols.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-148">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-149">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-149">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7fd2e-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-152">Der Pfad des Anwendungs Symbols.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-152">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-154">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd2e-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-156">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="7fd2e-156">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-157">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-157">The date the object was installed.</span></span> <span data-ttu-id="7fd2e-158">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-158">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7fd2e-159">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-160">**Name**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd2e-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-163">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-163">The name of the object.</span></span>

<span data-ttu-id="7fd2e-164">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-165">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-165">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-167">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7fd2e-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-168">Pfad der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-168">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-169">**Pathist vorhanden**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-169">**PathExists**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-170">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7fd2e-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd2e-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-172">Gibt an, ob der Anwendungspfad gültig ist.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-172">Indicates whether the application path is valid.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-173">**Rdpfilecontents**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-173">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7fd2e-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-176">Der Inhalt der RDP-Datei, die der Anwendung entspricht.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-176">The contents of the RDP file that correspond to the application.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-177">**"Requirements dcommandline"**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-177">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-179">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7fd2e-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-180">Die Befehlszeilenargumente, die für die Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-180">The command-line arguments that are required for the application.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-181">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-181">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-183">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7fd2e-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-184">Ein Sicherheits Deskriptor, der den Zugriff auf die Anwendung im SDDL-Format steuert.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-184">A security descriptor that controls access to the application, in SDDL format.</span></span> <span data-ttu-id="7fd2e-185">Eine leere Zeichenfolge impliziert den gesamten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-185">An empty string implies allow all access.</span></span> <span data-ttu-id="7fd2e-186">Diese Sicherheits Beschreibung unterstützt keine deny-ACEs oder ACEs, die auf Benutzer oder Gruppen von nicht-Domänen verweisen.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-186">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-187">**Showinportal**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-187">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-188">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7fd2e-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-189">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7fd2e-189">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-190">Gibt an, ob die Anwendung in RD-Webzugriff angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-190">Indicates whether the application should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2e-191">**Status**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-191">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fd2e-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-194">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="7fd2e-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-195">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-195">Current status of the object.</span></span> <span data-ttu-id="7fd2e-196">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-196">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7fd2e-197">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="7fd2e-197">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7fd2e-198">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="7fd2e-198">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7fd2e-199">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-199">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7fd2e-200">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-200">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7fd2e-201">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="7fd2e-202">("OK")</span><span class="sxs-lookup"><span data-stu-id="7fd2e-202">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7fd2e-203">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="7fd2e-203">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7fd2e-204">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="7fd2e-204">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7fd2e-205">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="7fd2e-205">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7fd2e-206">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="7fd2e-206">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7fd2e-207">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="7fd2e-207">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7fd2e-208">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="7fd2e-208">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7fd2e-209">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="7fd2e-209">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7fd2e-210">**Vpath**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-210">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd2e-211">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd2e-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fd2e-212">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7fd2e-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7fd2e-213">Der virtuelle Pfad der Anwendung, d. h. der Pfad mit Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-213">The virtual path of the application, meaning the path with environment variables included.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7fd2e-214">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fd2e-214">Remarks</span></span>

<span data-ttu-id="7fd2e-215">Sie müssen Mitglied der Gruppe "Administratoren" sein, um Eigenschaften mithilfe dieser Klasse festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-215">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="7fd2e-216">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-216">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="7fd2e-217">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene für den **\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene**, die mithilfe der com-Funktion [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="7fd2e-218">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="7fd2e-219">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="7fd2e-220">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7fd2e-221">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7fd2e-222">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7fd2e-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7fd2e-223">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7fd2e-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fd2e-224">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fd2e-224">Requirements</span></span>



| <span data-ttu-id="7fd2e-225">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fd2e-225">Requirement</span></span> | <span data-ttu-id="7fd2e-226">Wert</span><span class="sxs-lookup"><span data-stu-id="7fd2e-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd2e-227">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fd2e-227">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd2e-228">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7fd2e-228">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7fd2e-229">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fd2e-229">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd2e-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fd2e-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7fd2e-231">Namespace</span><span class="sxs-lookup"><span data-stu-id="7fd2e-231">Namespace</span></span><br/>                | <span data-ttu-id="7fd2e-232">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7fd2e-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7fd2e-233">MOF</span><span class="sxs-lookup"><span data-stu-id="7fd2e-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fd2e-234"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7fd2e-234"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="7fd2e-235">DLL</span><span class="sxs-lookup"><span data-stu-id="7fd2e-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fd2e-236"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fd2e-236"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

