---
title: Win32_TSClientSetting-Klasse
description: Definiert Konfigurationseinstellungen für die Win32- \_ Terminal Klasse, die mit der Verbindungsrichtlinie verknüpft ist.
ms.assetid: 438baf22-adc2-410e-bf9b-4b17a05c5ce4
ms.tgt_platform: multiple
keywords:
- Win32_TSClientSetting-Klasse Remotedesktopdienste
- Win32_TSClientSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSClientSetting
- Win32_TSClientSetting.Caption
- Win32_TSClientSetting.Description
- Win32_TSClientSetting.InstallDate
- Win32_TSClientSetting.Name
- Win32_TSClientSetting.Status
- Win32_TSClientSetting.TerminalName
- Win32_TSClientSetting.ConnectionPolicy
- Win32_TSClientSetting.ConnectClientDrivesAtLogon
- Win32_TSClientSetting.ConnectPrinterAtLogon
- Win32_TSClientSetting.DefaultToClientPrinter
- Win32_TSClientSetting.PolicySourceDefaultToClientPrinter
- Win32_TSClientSetting.WindowsPrinterMapping
- Win32_TSClientSetting.PolicySourceWindowsPrinterMapping
- Win32_TSClientSetting.LPTPortMapping
- Win32_TSClientSetting.PolicySourceLPTPortMapping
- Win32_TSClientSetting.COMPortMapping
- Win32_TSClientSetting.PolicySourceCOMPortMapping
- Win32_TSClientSetting.DriveMapping
- Win32_TSClientSetting.PolicySourceDriveMapping
- Win32_TSClientSetting.AudioMapping
- Win32_TSClientSetting.PolicySourceAudioMapping
- Win32_TSClientSetting.ClipboardMapping
- Win32_TSClientSetting.PolicySourceClipboardMapping
- Win32_TSClientSetting.ColorDepthPolicy
- Win32_TSClientSetting.PolicySourceColorDepthPolicy
- Win32_TSClientSetting.ColorDepth
- Win32_TSClientSetting.PolicySourceColorDepth
- Win32_TSClientSetting.MaxMonitors
- Win32_TSClientSetting.MaxXResolution
- Win32_TSClientSetting.MaxYResolution
- Win32_TSClientSetting.PolicySourceMaxMonitors
- Win32_TSClientSetting.PolicySourceMaxResolution
- Win32_TSClientSetting.PNPRedirection
- Win32_TSClientSetting.PolicySourcePNPRedirection
- Win32_TSClientSetting.AudioCaptureRedir
- Win32_TSClientSetting.PolicySourceAudioCaptureRedir
- Win32_TSClientSetting.VideoPlaybackRedir
- Win32_TSClientSetting.PolicySourceVideoPlaybackRedir
- Win32_TSClientSetting.AllowDwm
- Win32_TSClientSetting.PolicySourceAllowDwm
- Win32_TSClientSetting.PolicyAdvancedRemoteAppGraphics
- Win32_TSClientSetting.AdvancedRemoteAppGraphics
- Win32_TSClientSetting.RemoteSessionProfile
- Win32_TSClientSetting.PolicySourceRemoteSessionProfile
- Win32_TSClientSetting.AVC444ModePreferred
- Win32_TSClientSetting.PolicySourceAvc444ModePreferred
- Win32_TSClientSetting.EncodeImageQuality
- Win32_TSClientSetting.PolicySourceEncodeImageQuality
- Win32_TSClientSetting.HardwareGraphicsAdapter
- Win32_TSClientSetting.PolicySourceHardwareGraphicsAdapter
- Win32_TSClientSetting.SelectTransport
- Win32_TSClientSetting.PolicySourceSelectTransport
- Win32_TSClientSetting.SelectNetworkDetect
- Win32_TSClientSetting.PolicySourceSelectNetworkDetect
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204f38570e1e023ca070ed1845e4574d9570b8ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105836"
---
# <a name="win32_tsclientsetting-class"></a><span data-ttu-id="3ca16-105">Win32- \_ tsclientsetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="3ca16-105">Win32\_TSClientSetting class</span></span>

<span data-ttu-id="3ca16-106">Die **Win32 \_ tsclientsetting** -WMI-Klasse definiert Konfigurationseinstellungen für die [**Win32- \_ Terminal**](win32-terminal.md) Klasse, die mit der Verbindungsrichtlinie verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3ca16-106">The **Win32\_TSClientSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to connection policy.</span></span>

<span data-ttu-id="3ca16-107">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="3ca16-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="3ca16-108">Referenzinformationen zu-Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="3ca16-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca16-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ca16-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSCLIENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSClientSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ConnectionPolicy;
  uint32   ConnectClientDrivesAtLogon;
  uint32   ConnectPrinterAtLogon;
  uint32   DefaultToClientPrinter;
  uint32   PolicySourceDefaultToClientPrinter;
  uint32   WindowsPrinterMapping;
  uint32   PolicySourceWindowsPrinterMapping;
  uint32   LPTPortMapping;
  uint32   PolicySourceLPTPortMapping;
  uint32   COMPortMapping;
  uint32   PolicySourceCOMPortMapping;
  uint32   DriveMapping;
  uint32   PolicySourceDriveMapping;
  uint32   AudioMapping;
  uint32   PolicySourceAudioMapping;
  uint32   ClipboardMapping;
  uint32   PolicySourceClipboardMapping;
  uint32   ColorDepthPolicy;
  uint32   PolicySourceColorDepthPolicy;
  uint32   ColorDepth;
  uint32   PolicySourceColorDepth;
  uint32   MaxMonitors;
  uint32   MaxXResolution;
  uint32   MaxYResolution;
  uint32   PolicySourceMaxMonitors;
  uint32   PolicySourceMaxResolution;
  uint32   PNPRedirection;
  uint32   PolicySourcePNPRedirection;
  uint32   AudioCaptureRedir;
  uint32   PolicySourceAudioCaptureRedir;
  uint32   VideoPlaybackRedir;
  uint32   PolicySourceVideoPlaybackRedir;
  uint32   AllowDwm;
  uint32   PolicySourceAllowDwm;
  uint32   PolicyAdvancedRemoteAppGraphics;
  uint32   AdvancedRemoteAppGraphics;
  uint32   RemoteSessionProfile;
  uint32   PolicySourceRemoteSessionProfile;
  uint32   AVC444ModePreferred;
  uint32   PolicySourceAvc444ModePreferred;
  uint32   EncodeImageQuality;
  uint32   PolicySourceEncodeImageQuality;
  uint32   HardwareGraphicsAdapter;
  uint32   PolicySourceHardwareGraphicsAdapter;
  uint32   SelectTransport;
  uint32   PolicySourceSelectTransport;
  uint32   SelectNetworkDetect;
  uint32   PolicySourceSelectNetworkDetect;
};
```

## <a name="members"></a><span data-ttu-id="3ca16-110">Member</span><span class="sxs-lookup"><span data-stu-id="3ca16-110">Members</span></span>

<span data-ttu-id="3ca16-111">Die Win32-Klasse " **\_ tsclientsetting** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3ca16-111">The **Win32\_TSClientSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="3ca16-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="3ca16-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="3ca16-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3ca16-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3ca16-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="3ca16-114">Methods</span></span>

<span data-ttu-id="3ca16-115">Die **Win32 \_ tsclientsetting** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3ca16-115">The **Win32\_TSClientSetting** class has these methods.</span></span>



| <span data-ttu-id="3ca16-116">Methode</span><span class="sxs-lookup"><span data-stu-id="3ca16-116">Method</span></span>                                                                   | <span data-ttu-id="3ca16-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ca16-117">Description</span></span>                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ca16-118">**ConnectionSettings**</span><span class="sxs-lookup"><span data-stu-id="3ca16-118">**ConnectionSettings**</span></span>](win32-tsclientsetting-connectionsettings.md)   | <span data-ttu-id="3ca16-119">Legt die Eigenschaften **connectclientdrivesatlogon**, **connectprinteratlogon** und **defaultdeclientprinter** dieser Klasse fest.</span><span class="sxs-lookup"><span data-stu-id="3ca16-119">Sets the **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon**, and **DefaultToClientPrinter** properties of this class.</span></span><br/>                      |
| [<span data-ttu-id="3ca16-120">**"Abrunden lowdwm"**</span><span class="sxs-lookup"><span data-stu-id="3ca16-120">**SetAllowDwm**</span></span>](setallowdwm-win32-tsclientsetting.md)                 | <span data-ttu-id="3ca16-121">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ca16-121">Not supported.</span></span><br/> <span data-ttu-id="3ca16-122">**Windows 7 und Windows Server 2008 R2:** Legt die **allowdwm** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="3ca16-122">**Windows 7 and Windows Server 2008 R2:** Sets the **AllowDwm** property.</span></span><br/>                                               |
| [<span data-ttu-id="3ca16-123">**Setclientproperty**</span><span class="sxs-lookup"><span data-stu-id="3ca16-123">**SetClientProperty**</span></span>](win32-tsclientsetting-setclientproperty.md)     | <span data-ttu-id="3ca16-124">Legt die Eigenschaften **lptportmapping**, **COMPortMapping**, **audiomapping**, **ClipboardMapping**, **DriveMapping** oder **WindowsPrinterMapping** fest.</span><span class="sxs-lookup"><span data-stu-id="3ca16-124">Sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property.</span></span><br/> |
| [<span data-ttu-id="3ca16-125">**Setcolortiefe**</span><span class="sxs-lookup"><span data-stu-id="3ca16-125">**SetColorDepth**</span></span>](win32-tsclientsetting-setcolordepth.md)             | <span data-ttu-id="3ca16-126">Legt die **colortiefe** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="3ca16-126">Sets the **ColorDepth** property.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="3ca16-127">**Setcolordepthpolicy**</span><span class="sxs-lookup"><span data-stu-id="3ca16-127">**SetColorDepthPolicy**</span></span>](win32-tsclientsetting-setcolordepthpolicy.md) | <span data-ttu-id="3ca16-128">Legt die **ColorDepthPolicy** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="3ca16-128">Sets the **ColorDepthPolicy** property.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="3ca16-129">**Setmaxmonitors**</span><span class="sxs-lookup"><span data-stu-id="3ca16-129">**SetMaxMonitors**</span></span>](setmaxmonitors-win32-tsclientsetting.md)           | <span data-ttu-id="3ca16-130">Legt die **maxmonitors** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="3ca16-130">Sets the **MaxMonitors** property.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="3ca16-131">**Setmaxxresolution**</span><span class="sxs-lookup"><span data-stu-id="3ca16-131">**SetMaxXResolution**</span></span>](setmaxxresolution-win32-tsclientsetting.md)     | <span data-ttu-id="3ca16-132">Legt die **maxxresolution** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="3ca16-132">Sets the **MaxXResolution** property.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="3ca16-133">**Setmaxyresolution**</span><span class="sxs-lookup"><span data-stu-id="3ca16-133">**SetMaxYResolution**</span></span>](setmaxyresolution-win32-tsclientsetting.md)     | <span data-ttu-id="3ca16-134">Legt die **maxyresolution** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="3ca16-134">Sets the **MaxYResolution** property.</span></span><br/>                                                                                                             |



 

### <a name="properties"></a><span data-ttu-id="3ca16-135">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3ca16-135">Properties</span></span>

<span data-ttu-id="3ca16-136">Die **Win32 \_ tsclientsetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3ca16-136">The **Win32\_TSClientSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ca16-137">**Advancedremoteappgraphics**</span><span class="sxs-lookup"><span data-stu-id="3ca16-137">**AdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-138">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3ca16-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-140">Gibt an, ob erweiterte remotefx-Grafiken für RemoteApp aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3ca16-140">Specifies whether to enable advanced RemoteFX graphics for RemoteApp.</span></span>

<span data-ttu-id="3ca16-141">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2012 R2 und Windows 8.1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-141">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-142"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-142"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-143">Erweiterte Grafiken sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-143">Advanced graphics are disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-144"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-144"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-145">Erweiterte Grafiken sind aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-145">Advanced graphics are enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-146">**Allowdwm**</span><span class="sxs-lookup"><span data-stu-id="3ca16-146">**AllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-147">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-149">Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-149">This property is not available.</span></span>

<span data-ttu-id="3ca16-150">\* \* Windows 7 und Windows Server 2008 R2: \* \*</span><span class="sxs-lookup"><span data-stu-id="3ca16-150">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="3ca16-151">Gibt an, ob die Remote Desktop Komposition aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ca16-151">Specifies whether to enable or disable remote desktop composition.</span></span> <span data-ttu-id="3ca16-152">NULL deaktiviert die Remote Desktop Komposition, und ein Wert ungleich NULL wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-152">Zero will disable remote desktop composition and a nonzero value will enable it.</span></span>

<span data-ttu-id="3ca16-153">Verwenden Sie [**die Methode**](setallowdwm-win32-tsclientsetting.md) "-Methode", um diese Eigenschaft zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3ca16-153">Use the [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) method to modify this property.</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-154">**Audiocaptureredir**</span><span class="sxs-lookup"><span data-stu-id="3ca16-154">**AudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-155">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-157">Gibt an, ob die audioerfassungs Umleitung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="3ca16-157">Specifies whether to allow audio capture redirection.</span></span>

<span data-ttu-id="3ca16-158">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-158">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-159">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-159">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-160">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-160">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-161">**Audiomapping**</span><span class="sxs-lookup"><span data-stu-id="3ca16-161">**AudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-162">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-164">Gibt an, ob die Audiozuordnung deaktiviert oder aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3ca16-164">Specifies whether audio mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-165"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-165"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-166">Die Audiozuordnung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-166">Audio mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-167"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-167"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-168">Die Audiozuordnung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-168">Audio mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-169">**AVC444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="3ca16-169">**AVC444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-170">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-171">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3ca16-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-172">Gibt an, ob der AVC444-Modus bevorzugt wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-172">Specifies whether AVC444 mode is preferred.</span></span>

<span data-ttu-id="3ca16-173">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 10 oder Windows Server 2016 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-173">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-174">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-174">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-175">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-175">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-176">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3ca16-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ca16-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-179">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3ca16-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-180">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3ca16-180">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="3ca16-181">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ca16-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-182">**ClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="3ca16-182">**ClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-183">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-185">Gibt an, ob die Zwischenablage Zuordnung deaktiviert oder aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3ca16-185">Specifies whether clipboard mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-186"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-186"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-187">Die Zuordnung der Zwischenablage ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-187">Clipboard mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-188"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-188"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-189">Die Zuordnung der Zwischenablage ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-189">Clipboard mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-190">**ColorDepth**</span><span class="sxs-lookup"><span data-stu-id="3ca16-190">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-191">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-193">Gibt die Farbtiefe an.</span><span class="sxs-lookup"><span data-stu-id="3ca16-193">Specifies the color depth.</span></span> <span data-ttu-id="3ca16-194">Mögliche Werte finden Sie unter der [**setcolortiefe**](win32-tsclientsetting-setcolordepth.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3ca16-194">For possible values, see the [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) method.</span></span>

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span data-ttu-id="3ca16-195"><span id="8_bit"></span><span id="8_BIT"></span>**8-Bit** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-195"><span id="8_bit"></span><span id="8_BIT"></span>**8 bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span data-ttu-id="3ca16-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 Bit** (2)</span><span class="sxs-lookup"><span data-stu-id="3ca16-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 bit** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span data-ttu-id="3ca16-197"><span id="16_bit"></span><span id="16_BIT"></span>**16 Bit** (3)</span><span class="sxs-lookup"><span data-stu-id="3ca16-197"><span id="16_bit"></span><span id="16_BIT"></span>**16 bit** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span data-ttu-id="3ca16-198"><span id="24_bit"></span><span id="24_BIT"></span>**24-Bit** (4)</span><span class="sxs-lookup"><span data-stu-id="3ca16-198"><span id="24_bit"></span><span id="24_BIT"></span>**24 bit** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span data-ttu-id="3ca16-199"><span id="32_bit"></span><span id="32_BIT"></span>**32-Bit** (5)</span><span class="sxs-lookup"><span data-stu-id="3ca16-199"><span id="32_bit"></span><span id="32_BIT"></span>**32 bit** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-200">**ColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="3ca16-200">**ColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-201">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-203">Gibt an, ob die maximale Farbeinstellung des Benutzers überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ca16-203">Specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-204"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-204"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-205">Überschreiben Sie die Richtlinie des Benutzers nicht.</span><span class="sxs-lookup"><span data-stu-id="3ca16-205">Do not override the user's policy.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-206"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-206"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-207">Überschreiben Sie die Richtlinie des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3ca16-207">Override the user's policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-208">**COMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="3ca16-208">**COMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-209">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-211">Gibt an, ob die COM-Port Zuordnung deaktiviert oder aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3ca16-211">Specifies whether COM port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-212"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-212"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-213">Die COM-Port Zuordnung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-213">COM port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-214"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-214"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-215">Die COM-Port Zuordnung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-215">COM port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-216">**Connectclientdrivesatlogon**</span><span class="sxs-lookup"><span data-stu-id="3ca16-216">**ConnectClientDrivesAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-217">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-219">Gibt an, ob die Laufwerke des Clients während des Anmeldevorgangs automatisch verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="3ca16-219">Specifies whether the client's drives will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-220"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-220"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-221">Laufwerke werden nicht automatisch verbunden.</span><span class="sxs-lookup"><span data-stu-id="3ca16-221">Drives will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-222"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-222"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-223">Laufwerke werden automatisch verbunden.</span><span class="sxs-lookup"><span data-stu-id="3ca16-223">Drives will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-224">**ConnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="3ca16-224">**ConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-225">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3ca16-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-227">Die Richtlinie, die der Server zum Abrufen der Benutzer Verbindungseinstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ca16-227">The policy the server uses to retrieve the user connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="3ca16-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Pro Benutzer** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-229">Die Verbindungseinstellungen des Benutzers sind wirksam.</span><span class="sxs-lookup"><span data-stu-id="3ca16-229">The user's connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="3ca16-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-override** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-231">Die Verbindungseinstellungen des Benutzers werden vom Server überschrieben.</span><span class="sxs-lookup"><span data-stu-id="3ca16-231">The user's connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-232">**Connectprinteratlogon**</span><span class="sxs-lookup"><span data-stu-id="3ca16-232">**ConnectPrinterAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-233">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-235">Gibt an, ob alle zugeordneten lokalen Drucker des Clients während des Anmeldevorgangs automatisch verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="3ca16-235">Specifies whether all mapped local printers of the client will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-236"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-236"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-237">Lokale Drucker werden nicht automatisch verbunden.</span><span class="sxs-lookup"><span data-stu-id="3ca16-237">Local printers will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-238"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-238"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-239">Lokale Drucker werden automatisch verbunden.</span><span class="sxs-lookup"><span data-stu-id="3ca16-239">Local printers will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-240">**Defaultdeclientprinter**</span><span class="sxs-lookup"><span data-stu-id="3ca16-240">**DefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-241">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-243">Gibt an, ob Druckaufträge automatisch an den lokalen Drucker des Clients gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ca16-243">Specifies whether print jobs will be automatically sent to the client's local printer.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-244"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-244"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-245">Druckaufträge werden nicht automatisch an den lokalen Drucker des Clients gesendet.</span><span class="sxs-lookup"><span data-stu-id="3ca16-245">Print jobs are not to be automatically sent to the client's local printer.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-246"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-246"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-247">Druckaufträge werden automatisch an den lokalen Drucker des Clients gesendet.</span><span class="sxs-lookup"><span data-stu-id="3ca16-247">Print jobs are to be automatically sent to the client's local printer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-248">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ca16-248">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ca16-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-251">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3ca16-251">Description of the object.</span></span>

<span data-ttu-id="3ca16-252">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ca16-252">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-253">**DriveMapping**</span><span class="sxs-lookup"><span data-stu-id="3ca16-253">**DriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-254">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-256">Gibt an, ob die Laufwerk Zuordnung deaktiviert oder aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3ca16-256">Specifies whether drive mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-257"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-257"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-258">Die Laufwerk Zuordnung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-258">Drive mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-259"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-259"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-260">Die Laufwerk Zuordnung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-260">Drive mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-261">**Encodeimagequality**</span><span class="sxs-lookup"><span data-stu-id="3ca16-261">**EncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-262">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-263">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3ca16-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-264">Gibt die Bildqualität für die RDP-Darstellung an.</span><span class="sxs-lookup"><span data-stu-id="3ca16-264">Specifies the image quality for RDP experience.</span></span>

<span data-ttu-id="3ca16-265">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-265">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

<span data-ttu-id="3ca16-266">**verlustfreie** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-266">**lossless** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="3ca16-267">**hoch** (2)</span><span class="sxs-lookup"><span data-stu-id="3ca16-267">**high** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="3ca16-268">**Mittel** (3)</span><span class="sxs-lookup"><span data-stu-id="3ca16-268">**medium** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-269">**Hardwaregraphicsadapter**</span><span class="sxs-lookup"><span data-stu-id="3ca16-269">**HardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-270">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-271">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3ca16-271">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-272">Gibt an, ob der RD-Sitzungshost Server den Hardware Grafik-Renderer als Standard Adapter verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ca16-272">Specifies whether the RD Session Host server uses the hardware graphics renderer as the default adapter.</span></span>

<span data-ttu-id="3ca16-273">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-273">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-274">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-274">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-275">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-275">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-276">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3ca16-276">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-277">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3ca16-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-279">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="3ca16-279">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-280">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3ca16-280">The date the object was installed.</span></span> <span data-ttu-id="3ca16-281">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3ca16-281">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3ca16-282">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ca16-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-283">**Lptportmapping**</span><span class="sxs-lookup"><span data-stu-id="3ca16-283">**LPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-284">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-286">Gibt an, ob die LPT-Port Zuordnung deaktiviert oder aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3ca16-286">Specifies whether LPT port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-287"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-287"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-288">Die LPT-Port Zuordnung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-288">LPT port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-289"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-289"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-290">Die LPT-Port Zuordnung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-290">LPT port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-291">**Maxmonitors**</span><span class="sxs-lookup"><span data-stu-id="3ca16-291">**MaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-292">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-294">Die maximale Anzahl von Monitoren, die vom Server unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3ca16-294">The maximum number of monitors supported by the server.</span></span> <span data-ttu-id="3ca16-295">Verwenden Sie die [**setmaxmonitors**](setmaxmonitors-win32-tsclientsetting.md) -Methode, um diese Eigenschaft zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3ca16-295">Use the [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="3ca16-296">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-296">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-297">**Maxxresolution**</span><span class="sxs-lookup"><span data-stu-id="3ca16-297">**MaxXResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-298">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-298">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-300">Die maximale X-Auflösung, die vom Server unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-300">The maximum X resolution supported by the server.</span></span> <span data-ttu-id="3ca16-301">Verwenden Sie die [**setmaxxresolution**](setmaxxresolution-win32-tsclientsetting.md) -Methode, um diese Eigenschaft zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3ca16-301">Use the [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="3ca16-302">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-302">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-303">**Maxyresolution**</span><span class="sxs-lookup"><span data-stu-id="3ca16-303">**MaxYResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-304">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-304">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-306">Die maximale Y-Auflösung, die vom Server unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-306">The maximum Y resolution supported by the server.</span></span> <span data-ttu-id="3ca16-307">Verwenden Sie die [**setmaxyresolution**](setmaxyresolution-win32-tsclientsetting.md) -Methode, um diese Eigenschaft zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3ca16-307">Use the [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="3ca16-308">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-308">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-309">**Name**</span><span class="sxs-lookup"><span data-stu-id="3ca16-309">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-310">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ca16-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-312">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3ca16-312">The name of the object.</span></span>

<span data-ttu-id="3ca16-313">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ca16-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-314">**Pnpredirection**</span><span class="sxs-lookup"><span data-stu-id="3ca16-314">**PNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-315">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-317">Gibt an, ob Plug & Play Umleitung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="3ca16-317">Specifies whether to allow Plug and Play redirection.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-318"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-318"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-319">Ermöglicht Plug & Play Umleitung.</span><span class="sxs-lookup"><span data-stu-id="3ca16-319">Allow Plug and Play redirection.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-320"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-320"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-321">Plug & Play Umleitung nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="3ca16-321">Do not allow Plug and Play redirection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-322">**Policyadvancedremoteappgraphics**</span><span class="sxs-lookup"><span data-stu-id="3ca16-322">**PolicyAdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-323">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-325">Gibt an, ob die **advancedremoteappgraphics** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-325">Indicates whether the **AdvancedRemoteAppGraphics** property is configured by the server or group policy.</span></span>

<span data-ttu-id="3ca16-326">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2012 R2 und Windows 8.1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-326">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span data-ttu-id="3ca16-327">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-327">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-328">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-328">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-329">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-329">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-330">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-330">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-331">**Policysourceallowdwm**</span><span class="sxs-lookup"><span data-stu-id="3ca16-331">**PolicySourceAllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-332">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-334">Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-334">This property is not available.</span></span>

<span data-ttu-id="3ca16-335">\* \* Windows 7 und Windows Server 2008 R2: \* \*</span><span class="sxs-lookup"><span data-stu-id="3ca16-335">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="3ca16-336">Gibt an, ob die **allowdwm** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-336">Indicates whether the **AllowDwm** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="3ca16-337">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-337">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-338">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-338">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-339">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-339">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-340">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-340">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-341">**Policysourceaudiocaptureredir**</span><span class="sxs-lookup"><span data-stu-id="3ca16-341">**PolicySourceAudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-342">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-344">Gibt an, ob die **audiocaptureredir** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-344">Indicates whether the **AudioCaptureRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="3ca16-345">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-345">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="3ca16-346">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-346">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-347">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-347">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-348">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-348">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-349">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-349">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-350">**Policysourceaudiomapping**</span><span class="sxs-lookup"><span data-stu-id="3ca16-350">**PolicySourceAudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-351">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-353">Gibt an, ob die **audiomapping** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-353">Indicates whether the **AudioMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="3ca16-354">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-354">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-355">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-355">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-356">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-356">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-357">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-357">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-358">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="3ca16-358">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-359">Standard</span><span class="sxs-lookup"><span data-stu-id="3ca16-359">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-360">**PolicySourceAvc444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="3ca16-360">**PolicySourceAvc444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-361">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-363">Gibt an, wie die **AVC444ModePreferredis** -Eigenschaft konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-363">Indicates how the **AVC444ModePreferredis** property is configured.</span></span>

<span data-ttu-id="3ca16-364">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 10 oder Windows Server 2016 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-364">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span data-ttu-id="3ca16-365">0</span><span class="sxs-lookup"><span data-stu-id="3ca16-365">0</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-366">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-366">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-367">1</span><span class="sxs-lookup"><span data-stu-id="3ca16-367">1</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-368">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-368">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-369">**PolicySourceClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="3ca16-369">**PolicySourceClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-370">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-372">Gibt an, ob die **ClipboardMapping** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-372">Indicates whether the **ClipboardMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="3ca16-373">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-373">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-374">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-374">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-375">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-375">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-376">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-376">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-377">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="3ca16-377">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-378">Standard</span><span class="sxs-lookup"><span data-stu-id="3ca16-378">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-379">**Policysourcecolortiefe**</span><span class="sxs-lookup"><span data-stu-id="3ca16-379">**PolicySourceColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-380">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-382">Gibt an, ob die **colortiefe** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-382">Indicates whether the **ColorDepth** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="3ca16-383">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-383">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-384">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-384">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-385">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-385">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-386">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-386">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-387">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="3ca16-387">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-388">Standard</span><span class="sxs-lookup"><span data-stu-id="3ca16-388">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-389">**PolicySourceColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="3ca16-389">**PolicySourceColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-390">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-391">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-392">Gibt an, ob die **ColorDepthPolicy** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-392">Indicates whether the **ColorDepthPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="3ca16-393">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-393">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-394">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-394">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-395">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-395">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-396">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-396">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-397">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="3ca16-397">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-398">Standard</span><span class="sxs-lookup"><span data-stu-id="3ca16-398">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-399">**PolicySourceCOMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="3ca16-399">**PolicySourceCOMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-400">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-400">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-401">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-402">Gibt an, ob die **COMPortMapping** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-402">Indicates whether the **COMPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="3ca16-403">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-403">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-404">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-404">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-405">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-405">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-406">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-406">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-407">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="3ca16-407">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-408">Standard</span><span class="sxs-lookup"><span data-stu-id="3ca16-408">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-409">**Policysourcedefaultdeclientprinter**</span><span class="sxs-lookup"><span data-stu-id="3ca16-409">**PolicySourceDefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-410">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-411">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-412">Gibt an, ob die **defaultto clientprinter** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-412">Indicates whether the **DefaultToClientPrinter** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="3ca16-413">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-413">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-414">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-414">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-415">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-415">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-416">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-416">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-417">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="3ca16-417">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-418">Standard</span><span class="sxs-lookup"><span data-stu-id="3ca16-418">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-419">**PolicySourceDriveMapping**</span><span class="sxs-lookup"><span data-stu-id="3ca16-419">**PolicySourceDriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-420">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-422">Gibt an, ob die **DriveMapping** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-422">Indicates whether the **DriveMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="3ca16-423">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-424">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-425">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-426">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-426">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-427">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="3ca16-427">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-428">Standard</span><span class="sxs-lookup"><span data-stu-id="3ca16-428">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-429">**Policysourceencodeimagequality**</span><span class="sxs-lookup"><span data-stu-id="3ca16-429">**PolicySourceEncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-430">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-430">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-431">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-432">Gibt an, wie **encodeimagequalityi** konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-432">Indicates how the **EncodeImageQualityi** is configured.</span></span>

<span data-ttu-id="3ca16-433">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-433">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="3ca16-434">0</span><span class="sxs-lookup"><span data-stu-id="3ca16-434">0</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-435">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-435">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-436">1</span><span class="sxs-lookup"><span data-stu-id="3ca16-436">1</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-437">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-437">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-438">**Policysourcehardwaregraphicsadapter**</span><span class="sxs-lookup"><span data-stu-id="3ca16-438">**PolicySourceHardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-439">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-441">Gibt an, wie der **hardwaregraphicsadapter** konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="3ca16-441">Indicates how the **HardwareGraphicsAdapter** is configured.</span></span>

<span data-ttu-id="3ca16-442">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-442">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="3ca16-443">0</span><span class="sxs-lookup"><span data-stu-id="3ca16-443">0</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-444">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-444">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-445">1</span><span class="sxs-lookup"><span data-stu-id="3ca16-445">1</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-446">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-446">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-447">**Policysourcelptportmapping**</span><span class="sxs-lookup"><span data-stu-id="3ca16-447">**PolicySourceLPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-448">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-448">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-449">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-450">Gibt an, ob die **lptportmapping** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-450">Indicates whether the **LPTPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="3ca16-451">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-451">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-452">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-452">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-453">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-453">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-454">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-454">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-455">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="3ca16-455">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-456">Standard</span><span class="sxs-lookup"><span data-stu-id="3ca16-456">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-457">**Policysourcemaxmonitors**</span><span class="sxs-lookup"><span data-stu-id="3ca16-457">**PolicySourceMaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-458">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-458">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-459">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-460">Gibt an, ob die **maxmonitors** -Eigenschaft vom Server, von der Gruppenrichtlinie oder von der Standardeinstellung konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-460">Indicates whether the **MaxMonitors** property is configured by the server, group policy, or default.</span></span>

<dt>

<span data-ttu-id="3ca16-461">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-461">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-462">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-462">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-463">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-463">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-464">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-464">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-465">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="3ca16-465">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-466">Standard</span><span class="sxs-lookup"><span data-stu-id="3ca16-466">Default</span></span>

</dd> </dl>

<span data-ttu-id="3ca16-467">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-467">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-468">**Policysourcemaxresolution**</span><span class="sxs-lookup"><span data-stu-id="3ca16-468">**PolicySourceMaxResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-469">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-469">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-470">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-471">Gibt an, ob die Eigenschaften **maxxresolution** und **maxyresolution** vom Server, von der Gruppenrichtlinie oder von der Standardeinstellung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="3ca16-471">Indicates whether the **MaxXResolution** and **MaxYResolution** properties are configured by the server, group policy, or default.</span></span>

<span data-ttu-id="3ca16-472">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-472">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="3ca16-473">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-473">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-474">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-474">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-475">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-475">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-476">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-476">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-477">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="3ca16-477">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-478">Standard</span><span class="sxs-lookup"><span data-stu-id="3ca16-478">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-479">**Policysourcepnpredirection**</span><span class="sxs-lookup"><span data-stu-id="3ca16-479">**PolicySourcePNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-480">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-481">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-482">Gibt an, ob die **pnpredirection** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-482">Indicates whether the **PNPRedirection** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="3ca16-483">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-483">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-484">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-484">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-485">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-485">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-486">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-486">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-487">**Policysourceremotesessionprofile**</span><span class="sxs-lookup"><span data-stu-id="3ca16-487">**PolicySourceRemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-488">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-489">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-490">Gibt an, wie das **remotesessionprofile** -Verzeichnis konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="3ca16-490">Indicates how the **RemoteSessionProfile** is configured.</span></span>

<span data-ttu-id="3ca16-491">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-491">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is unavailable prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="3ca16-492">0</span><span class="sxs-lookup"><span data-stu-id="3ca16-492">0</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-493">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-493">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-494">1</span><span class="sxs-lookup"><span data-stu-id="3ca16-494">1</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-495">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-495">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-496">**Policysourceselectnetworkdetect**</span><span class="sxs-lookup"><span data-stu-id="3ca16-496">**PolicySourceSelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-497">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-497">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-498">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-499">Gibt an, wie die Eigenschaft " **selectnetworkdetect** " konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-499">Indicates how the property **SelectNetworkDetect** is configured.</span></span>

<span data-ttu-id="3ca16-500">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-500">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="3ca16-501">0</span><span class="sxs-lookup"><span data-stu-id="3ca16-501">0</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-502">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-502">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-503">1</span><span class="sxs-lookup"><span data-stu-id="3ca16-503">1</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-504">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-504">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-505">**Policysourceselecttransport**</span><span class="sxs-lookup"><span data-stu-id="3ca16-505">**PolicySourceSelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-506">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-507">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-508">Gibt an, wie die **selecttransport** -Eigenschaft konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-508">Indicates how the property **SelectTransport** is configured.</span></span>

<span data-ttu-id="3ca16-509">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-509">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="3ca16-510">0</span><span class="sxs-lookup"><span data-stu-id="3ca16-510">0</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-511">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-511">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-512">1</span><span class="sxs-lookup"><span data-stu-id="3ca16-512">1</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-513">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-513">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-514">**Policysourcevideoplaybackredir**</span><span class="sxs-lookup"><span data-stu-id="3ca16-514">**PolicySourceVideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-515">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-515">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-516">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-517">Gibt an, ob die **videoplaybackredir** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-517">Indicates whether the **VideoPlaybackRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="3ca16-518">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-518">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="3ca16-519">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-519">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-520">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-520">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-521">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-521">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-522">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-522">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-523">**PolicySourceWindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="3ca16-523">**PolicySourceWindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-524">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-525">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-526">Gibt an, ob die **WindowsPrinterMapping** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-526">Indicates whether the **WindowsPrinterMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="3ca16-527">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-527">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-528">Server</span><span class="sxs-lookup"><span data-stu-id="3ca16-528">Server</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-529">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-529">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-530">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3ca16-530">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-531">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="3ca16-531">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-532">Standard</span><span class="sxs-lookup"><span data-stu-id="3ca16-532">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-533">**Remotesessionprofile**</span><span class="sxs-lookup"><span data-stu-id="3ca16-533">**RemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-534">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-534">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-535">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3ca16-535">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-536">Gibt das Profil für den RDP-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="3ca16-536">Specifies the profile for the RDP experience.</span></span>

<span data-ttu-id="3ca16-537">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-537">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="scale"></span><span id="SCALE"></span>

<span data-ttu-id="3ca16-538">**skalieren** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-538">**scale** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

<span data-ttu-id="3ca16-539">Darstellung **(2** )</span><span class="sxs-lookup"><span data-stu-id="3ca16-539">**experience** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

<span data-ttu-id="3ca16-540">**Bandbreite** (3)</span><span class="sxs-lookup"><span data-stu-id="3ca16-540">**bandwidth** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-541">**Selectnetworkdetect**</span><span class="sxs-lookup"><span data-stu-id="3ca16-541">**SelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-542">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-543">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3ca16-543">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-544">Gibt an, ob die Netzwerk Ermittlung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-544">Specifies whether network detection is used.</span></span>

<span data-ttu-id="3ca16-545">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-545">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="3ca16-546">0</span><span class="sxs-lookup"><span data-stu-id="3ca16-546">0</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-547">wird zur Verbindungszeit und im stabilen Zustand verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ca16-547">used at connect time and in steady state.</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-548">1</span><span class="sxs-lookup"><span data-stu-id="3ca16-548">1</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-549">zum Zeitpunkt der Verbindungs Herstellung deaktiviert</span><span class="sxs-lookup"><span data-stu-id="3ca16-549">disabled at connect time</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-550">2</span><span class="sxs-lookup"><span data-stu-id="3ca16-550">2</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-551">im stabilen Zustand deaktiviert</span><span class="sxs-lookup"><span data-stu-id="3ca16-551">disabled in steady state</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-552">3</span><span class="sxs-lookup"><span data-stu-id="3ca16-552">3</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-553">deaktiviert zur Verbindungszeit und im stabilen Zustand.</span><span class="sxs-lookup"><span data-stu-id="3ca16-553">disabled at connect time and in steady state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-554">**Selecttransport**</span><span class="sxs-lookup"><span data-stu-id="3ca16-554">**SelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-555">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-555">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-556">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3ca16-556">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-557">Gibt an, welche Transportprotokolle für den RDP-Zugriff auf den Server verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3ca16-557">Specifies which transport protocols can be used for RDP access to server.</span></span>

<span data-ttu-id="3ca16-558">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-558">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="3ca16-559">0</span><span class="sxs-lookup"><span data-stu-id="3ca16-559">0</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-560">Verwenden Sie UDP und TCP.</span><span class="sxs-lookup"><span data-stu-id="3ca16-560">Use both UDP and TCP.</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-561">1</span><span class="sxs-lookup"><span data-stu-id="3ca16-561">1</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-562">Verwenden Sie nur TCP.</span><span class="sxs-lookup"><span data-stu-id="3ca16-562">Use only TCP.</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-563">2</span><span class="sxs-lookup"><span data-stu-id="3ca16-563">2</span></span>
</dt> <dd>

<span data-ttu-id="3ca16-564">Verwenden Sie entweder UDP oder TCP.</span><span class="sxs-lookup"><span data-stu-id="3ca16-564">Use either UDP or TCP.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-565">**Status**</span><span class="sxs-lookup"><span data-stu-id="3ca16-565">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-566">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ca16-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-567">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-568">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="3ca16-568">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-569">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3ca16-569">Current status of the object.</span></span> <span data-ttu-id="3ca16-570">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3ca16-570">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3ca16-571">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="3ca16-571">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3ca16-572">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="3ca16-572">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3ca16-573">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ca16-573">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3ca16-574">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="3ca16-574">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3ca16-575">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ca16-575">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="3ca16-576">("OK")</span><span class="sxs-lookup"><span data-stu-id="3ca16-576">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3ca16-577">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="3ca16-577">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3ca16-578">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="3ca16-578">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3ca16-579">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="3ca16-579">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3ca16-580">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="3ca16-580">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3ca16-581">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="3ca16-581">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3ca16-582">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="3ca16-582">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3ca16-583">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="3ca16-583">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-584">**Terminal Name**</span><span class="sxs-lookup"><span data-stu-id="3ca16-584">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-585">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ca16-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-586">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-587">Der Name des Terminals.</span><span class="sxs-lookup"><span data-stu-id="3ca16-587">The name of the terminal.</span></span>

<span data-ttu-id="3ca16-588">Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ca16-588">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ca16-589">**Videoplaybackredir**</span><span class="sxs-lookup"><span data-stu-id="3ca16-589">**VideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-590">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-591">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-592">Gibt an, ob die Umleitung von Videowiedergabe zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-592">Specifies whether to allow video playback redirection.</span></span>

<span data-ttu-id="3ca16-593">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ca16-593">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-594">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-594">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-595">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-595">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ca16-596">**WindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="3ca16-596">**WindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ca16-597">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca16-597">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ca16-598">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ca16-598">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ca16-599">Gibt an, ob die Drucker Zuordnung für das Fenster des Clients deaktiviert oder aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3ca16-599">Specifies whether printer mapping is disabled or enabled for the client's window.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="3ca16-600"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="3ca16-600"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-601">Die Drucker Zuordnung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-601">Printer mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="3ca16-602"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="3ca16-602"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ca16-603">Die Drucker Zuordnung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-603">Printer mapping is disabled.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ca16-604">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ca16-604">Remarks</span></span>

<span data-ttu-id="3ca16-605">Beachten Sie, dass eine Fenster Station, die der Konsolen Sitzung zugeordnet ist, nicht auf die Methoden und Eigenschaften dieser Klasse zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="3ca16-605">Be aware that a window station associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="3ca16-606">Wenn ein Versuch unternommen wird, indem "Console" als Wert der **Terminalname** -Eigenschaft angegeben wird, wird **WBEM \_ E \_ \_** von Methoden dieses Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3ca16-606">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="3ca16-607">Dieser Fehlercode wird auch zurückgegeben, wenn eine Fenster Station versucht, Methoden dieses Objekts aufzurufen, um die Sicherheitseigenschaften der Konten "LocalSystem", "LocalService" oder "Network Service" hinzuzufügen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3ca16-607">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="3ca16-608">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="3ca16-608">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="3ca16-609">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="3ca16-609">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="3ca16-610">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von sechs.</span><span class="sxs-lookup"><span data-stu-id="3ca16-610">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="3ca16-611">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3ca16-611">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="3ca16-612">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="3ca16-612">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3ca16-613">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="3ca16-613">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3ca16-614">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3ca16-614">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3ca16-615">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3ca16-615">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca16-616">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ca16-616">Requirements</span></span>



| <span data-ttu-id="3ca16-617">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ca16-617">Requirement</span></span> | <span data-ttu-id="3ca16-618">Wert</span><span class="sxs-lookup"><span data-stu-id="3ca16-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca16-619">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ca16-619">Minimum supported client</span></span><br/> | <span data-ttu-id="3ca16-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ca16-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ca16-621">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ca16-621">Minimum supported server</span></span><br/> | <span data-ttu-id="3ca16-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ca16-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ca16-623">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ca16-623">Namespace</span></span><br/>                | <span data-ttu-id="3ca16-624">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3ca16-624">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3ca16-625">MOF</span><span class="sxs-lookup"><span data-stu-id="3ca16-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ca16-626"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3ca16-626"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ca16-627">DLL</span><span class="sxs-lookup"><span data-stu-id="3ca16-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ca16-628"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ca16-628"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ca16-629">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ca16-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca16-630">**Win32- \_ Terminal**</span><span class="sxs-lookup"><span data-stu-id="3ca16-630">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="3ca16-631">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="3ca16-631">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="3ca16-632">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="3ca16-632">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

