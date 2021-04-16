---
title: Win32_TSEnvironmentSetting-Klasse
description: Definiert die Konfigurationseinstellungen für die Win32- \_ Terminal Klasse einschließlich der ersten Programm Richtlinie.
ms.assetid: 2d310a1e-a1bd-4ccb-965e-8389aaa2e4c1
ms.tgt_platform: multiple
keywords:
- Win32_TSEnvironmentSetting-Klasse Remotedesktopdienste
- Win32_TSEnvironmentSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting.Caption
- Win32_TSEnvironmentSetting.Description
- Win32_TSEnvironmentSetting.InstallDate
- Win32_TSEnvironmentSetting.Name
- Win32_TSEnvironmentSetting.Status
- Win32_TSEnvironmentSetting.TerminalName
- Win32_TSEnvironmentSetting.ClientWallPaper
- Win32_TSEnvironmentSetting.InitialProgramPath
- Win32_TSEnvironmentSetting.InitialProgramPolicy
- Win32_TSEnvironmentSetting.PolicySourceClientWallPaper
- Win32_TSEnvironmentSetting.PolicySourceInitialProgramPath
- Win32_TSEnvironmentSetting.PolicySourceStartIn
- Win32_TSEnvironmentSetting.Startin
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0689536385644ae3ef95d106e50ab198e5a57f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518815"
---
# <a name="win32_tsenvironmentsetting-class"></a><span data-ttu-id="18eed-105">Win32- \_ Klasse "tsenvironmentsetting"</span><span class="sxs-lookup"><span data-stu-id="18eed-105">Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="18eed-106">Die **Win32 \_ tsenvironmentsetting** -WMI-Klasse definiert die Konfigurationseinstellungen für die [**Win32- \_ Terminal**](win32-terminal.md) Klasse einschließlich der ersten Programm Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="18eed-106">The **Win32\_TSEnvironmentSetting** WMI class defines the configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including initial program policy.</span></span>

<span data-ttu-id="18eed-107">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="18eed-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="18eed-108">Referenzinformationen zu-Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="18eed-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="18eed-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="18eed-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSENVIRONMENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSEnvironmentSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientWallPaper;
  string   InitialProgramPath;
  uint32   InitialProgramPolicy;
  uint32   PolicySourceClientWallPaper;
  uint32   PolicySourceInitialProgramPath;
  uint32   PolicySourceStartIn;
  string   Startin;
};
```

## <a name="members"></a><span data-ttu-id="18eed-110">Member</span><span class="sxs-lookup"><span data-stu-id="18eed-110">Members</span></span>

<span data-ttu-id="18eed-111">Die Win32-Klasse " **\_ tsenvironmentsetting** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="18eed-111">The **Win32\_TSEnvironmentSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="18eed-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="18eed-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="18eed-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18eed-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="18eed-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="18eed-114">Methods</span></span>

<span data-ttu-id="18eed-115">Die Win32-Klasse " **\_ tsenvironmentsetting** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="18eed-115">The **Win32\_TSEnvironmentSetting** class has these methods.</span></span>



| <span data-ttu-id="18eed-116">Methode</span><span class="sxs-lookup"><span data-stu-id="18eed-116">Method</span></span>                                                                      | <span data-ttu-id="18eed-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18eed-117">Description</span></span>                                                            |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="18eed-118">**InitialProgram**</span><span class="sxs-lookup"><span data-stu-id="18eed-118">**InitialProgram**</span></span>](win32-tsenvironmentsetting-initialprogram.md)         | <span data-ttu-id="18eed-119">Legt die Eigenschaften des Start Programms fest, die in dieser Klasse enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="18eed-119">Sets the startup program properties included in this class.</span></span><br/> |
| [<span data-ttu-id="18eed-120">**Setclientwallpaper**</span><span class="sxs-lookup"><span data-stu-id="18eed-120">**SetClientWallPaper**</span></span>](win32-tsenvironmentsetting-setclientwallpaper.md) | <span data-ttu-id="18eed-121">Legt die **ClientWallPaper** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="18eed-121">Sets the **ClientWallPaper** property.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="18eed-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18eed-122">Properties</span></span>

<span data-ttu-id="18eed-123">Die Win32-Klasse " **\_ tsenvironmentsetting** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="18eed-123">The **Win32\_TSEnvironmentSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18eed-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="18eed-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18eed-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18eed-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18eed-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18eed-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18eed-127">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="18eed-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="18eed-128">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="18eed-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="18eed-129">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18eed-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18eed-130">**ClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="18eed-130">**ClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18eed-131">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18eed-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18eed-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18eed-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18eed-133">Gibt an, ob das Hintergrundbild auf dem Client angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="18eed-133">Specifies whether the wallpaper image is displayed on the client.</span></span> <span data-ttu-id="18eed-134">Wenn Sie das Hintergrundbild nicht anzeigen, können Sie Systemressourcen sparen, indem Sie die zum Neuzeichnen des Bildschirms benötigte Zeit verringern.</span><span class="sxs-lookup"><span data-stu-id="18eed-134">Not displaying the wallpaper image can save system resources by decreasing the time required to repaint the screen.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="18eed-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="18eed-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="18eed-136">Das Hintergrundbild wird auf dem Client nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="18eed-136">The wallpaper image is not displayed on the client.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="18eed-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="18eed-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18eed-138">Das Hintergrundbild wird auf dem Client angezeigt.</span><span class="sxs-lookup"><span data-stu-id="18eed-138">The wallpaper image is displayed on the client.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18eed-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18eed-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18eed-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18eed-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18eed-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18eed-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18eed-142">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="18eed-142">Description of the object.</span></span>

<span data-ttu-id="18eed-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18eed-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18eed-144">**Initialprogrampath**</span><span class="sxs-lookup"><span data-stu-id="18eed-144">**InitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18eed-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18eed-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18eed-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18eed-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18eed-147">Der Name und der Pfad des Programms, das der Benutzer unmittelbar nach der Anmeldung beim RD-Sitzungshost Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18eed-147">The name and the path of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="18eed-148">**Initialprogrampolicy**</span><span class="sxs-lookup"><span data-stu-id="18eed-148">**InitialProgramPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18eed-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18eed-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18eed-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="18eed-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18eed-151">Die Richtlinie, die der Server verwendet, um den Pfad und den Dateinamen des Start Programms sowie den Namen des Ordners zu bestimmen, in dem er sich befindet.</span><span class="sxs-lookup"><span data-stu-id="18eed-151">The policy the server uses to determine the startup program path and file name, and the name of the folder it is located in.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="18eed-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Pro Benutzer** (0)</span><span class="sxs-lookup"><span data-stu-id="18eed-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="18eed-153">Die Start Programmeinstellungen des Benutzers sind wirksam.</span><span class="sxs-lookup"><span data-stu-id="18eed-153">The user's startup program settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="18eed-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-override** (1)</span><span class="sxs-lookup"><span data-stu-id="18eed-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18eed-155">Die Start Programmeinstellungen des Benutzers werden vom Server überschrieben.</span><span class="sxs-lookup"><span data-stu-id="18eed-155">The user's startup program settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>

<span data-ttu-id="18eed-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Einzel Anwendungsmodus** (2)</span><span class="sxs-lookup"><span data-stu-id="18eed-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Single-App Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="18eed-157">In dieser Sitzung wird nur eine einzige Anwendung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18eed-157">Only a single application will be run in this session.</span></span> <span data-ttu-id="18eed-158">Die Informationen zum Start Programm werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="18eed-158">The startup program information is ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18eed-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18eed-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18eed-160">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="18eed-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18eed-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18eed-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18eed-162">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="18eed-162">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="18eed-163">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="18eed-163">The date the object was installed.</span></span> <span data-ttu-id="18eed-164">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="18eed-164">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="18eed-165">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18eed-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18eed-166">**Name**</span><span class="sxs-lookup"><span data-stu-id="18eed-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18eed-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18eed-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18eed-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18eed-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18eed-169">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="18eed-169">The name of the object.</span></span>

<span data-ttu-id="18eed-170">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18eed-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18eed-171">**Policysourceclientwallpaper**</span><span class="sxs-lookup"><span data-stu-id="18eed-171">**PolicySourceClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18eed-172">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18eed-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18eed-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18eed-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18eed-174">Gibt an, ob die **ClientWallPaper** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="18eed-174">Indicates whether the **ClientWallPaper** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="18eed-175">0</span><span class="sxs-lookup"><span data-stu-id="18eed-175">0</span></span>
</dt> <dd>

<span data-ttu-id="18eed-176">Server</span><span class="sxs-lookup"><span data-stu-id="18eed-176">Server</span></span>

</dd> <dt>

<span data-ttu-id="18eed-177">1</span><span class="sxs-lookup"><span data-stu-id="18eed-177">1</span></span>
</dt> <dd>

<span data-ttu-id="18eed-178">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="18eed-178">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="18eed-179">2</span><span class="sxs-lookup"><span data-stu-id="18eed-179">2</span></span>
</dt> <dd>

<span data-ttu-id="18eed-180">Standard</span><span class="sxs-lookup"><span data-stu-id="18eed-180">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18eed-181">**Policysourceinitialprogrampath**</span><span class="sxs-lookup"><span data-stu-id="18eed-181">**PolicySourceInitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18eed-182">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18eed-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18eed-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18eed-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18eed-184">Gibt an, ob die **initialprogrampath** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="18eed-184">Indicates whether the **InitialProgramPath** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="18eed-185">0</span><span class="sxs-lookup"><span data-stu-id="18eed-185">0</span></span>
</dt> <dd>

<span data-ttu-id="18eed-186">Server</span><span class="sxs-lookup"><span data-stu-id="18eed-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="18eed-187">1</span><span class="sxs-lookup"><span data-stu-id="18eed-187">1</span></span>
</dt> <dd>

<span data-ttu-id="18eed-188">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="18eed-188">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="18eed-189">2</span><span class="sxs-lookup"><span data-stu-id="18eed-189">2</span></span>
</dt> <dd>

<span data-ttu-id="18eed-190">Standard</span><span class="sxs-lookup"><span data-stu-id="18eed-190">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18eed-191">**PolicySourceStartIn**</span><span class="sxs-lookup"><span data-stu-id="18eed-191">**PolicySourceStartIn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18eed-192">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18eed-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18eed-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18eed-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18eed-194">Gibt an, ob die **Startin** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="18eed-194">Indicates whether the **StartIn** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="18eed-195">0</span><span class="sxs-lookup"><span data-stu-id="18eed-195">0</span></span>
</dt> <dd>

<span data-ttu-id="18eed-196">Server</span><span class="sxs-lookup"><span data-stu-id="18eed-196">Server</span></span>

</dd> <dt>

<span data-ttu-id="18eed-197">1</span><span class="sxs-lookup"><span data-stu-id="18eed-197">1</span></span>
</dt> <dd>

<span data-ttu-id="18eed-198">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="18eed-198">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="18eed-199">2</span><span class="sxs-lookup"><span data-stu-id="18eed-199">2</span></span>
</dt> <dd>

<span data-ttu-id="18eed-200">Standard</span><span class="sxs-lookup"><span data-stu-id="18eed-200">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18eed-201">**Startin**</span><span class="sxs-lookup"><span data-stu-id="18eed-201">**Startin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18eed-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18eed-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18eed-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18eed-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18eed-204">Der Pfad des Arbeitsverzeichnisses des Programms, das der Benutzer unmittelbar nach der Anmeldung beim RD-Sitzungshost Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18eed-204">The path of the working directory of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="18eed-205">**Status**</span><span class="sxs-lookup"><span data-stu-id="18eed-205">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18eed-206">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18eed-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18eed-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18eed-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18eed-208">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="18eed-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="18eed-209">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="18eed-209">Current status of the object.</span></span> <span data-ttu-id="18eed-210">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="18eed-210">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="18eed-211">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="18eed-211">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="18eed-212">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="18eed-212">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="18eed-213">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="18eed-213">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="18eed-214">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="18eed-214">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="18eed-215">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18eed-215">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="18eed-216">("OK")</span><span class="sxs-lookup"><span data-stu-id="18eed-216">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18eed-217">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="18eed-217">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18eed-218">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="18eed-218">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18eed-219">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="18eed-219">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18eed-220">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="18eed-220">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18eed-221">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="18eed-221">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18eed-222">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="18eed-222">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18eed-223">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="18eed-223">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18eed-224">**Terminal Name**</span><span class="sxs-lookup"><span data-stu-id="18eed-224">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18eed-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18eed-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18eed-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18eed-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18eed-227">Der Name des Terminals.</span><span class="sxs-lookup"><span data-stu-id="18eed-227">The name of the terminal.</span></span>

<span data-ttu-id="18eed-228">Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18eed-228">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18eed-229">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18eed-229">Remarks</span></span>

<span data-ttu-id="18eed-230">Beachten Sie, dass die der Konsolen Sitzung zugeordneten Winstations nicht auf die Methoden und Eigenschaften dieser Klasse zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="18eed-230">Be aware that Winstations that are associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="18eed-231">Wenn ein Versuch unternommen wird, indem "Console" als Wert der **Terminalname** -Eigenschaft angegeben wird, geben die Methoden dieses Objekts **WBEM \_ E \_ nicht \_ unterstützt** zurück.</span><span class="sxs-lookup"><span data-stu-id="18eed-231">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="18eed-232">Dieser Fehlercode wird auch zurückgegeben, wenn eine Fenster Station versucht, Methoden dieses Objekts aufzurufen, um die Sicherheitseigenschaften der Konten "LocalSystem", "LocalService" oder "Network Service" hinzuzufügen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="18eed-232">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="18eed-233">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="18eed-233">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="18eed-234">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="18eed-234">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="18eed-235">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="18eed-235">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="18eed-236">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="18eed-236">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="18eed-237">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="18eed-237">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="18eed-238">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="18eed-238">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="18eed-239">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="18eed-239">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="18eed-240">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="18eed-240">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="18eed-241">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18eed-241">Requirements</span></span>



| <span data-ttu-id="18eed-242">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18eed-242">Requirement</span></span> | <span data-ttu-id="18eed-243">Wert</span><span class="sxs-lookup"><span data-stu-id="18eed-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18eed-244">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18eed-244">Minimum supported client</span></span><br/> | <span data-ttu-id="18eed-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18eed-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18eed-246">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18eed-246">Minimum supported server</span></span><br/> | <span data-ttu-id="18eed-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18eed-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18eed-248">Namespace</span><span class="sxs-lookup"><span data-stu-id="18eed-248">Namespace</span></span><br/>                | <span data-ttu-id="18eed-249">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="18eed-249">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="18eed-250">MOF</span><span class="sxs-lookup"><span data-stu-id="18eed-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18eed-251"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="18eed-251"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="18eed-252">DLL</span><span class="sxs-lookup"><span data-stu-id="18eed-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18eed-253"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18eed-253"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18eed-254">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18eed-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18eed-255">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="18eed-255">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

