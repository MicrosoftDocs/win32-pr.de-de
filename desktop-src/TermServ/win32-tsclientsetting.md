---
title: Win32_TSClientSetting-Klasse
description: Definiert Konfigurationseinstellungen für die Win32 \_ Terminal-Klasse im Zusammenhang mit der Verbindungsrichtlinie.
ms.assetid: 438baf22-adc2-410e-bf9b-4b17a05c5ce4
ms.tgt_platform: multiple
keywords:
- Win32_TSClientSetting-Klassen-Remotedesktopdienste
- Win32_TSClientSetting-Klasse Remotedesktopdienste beschrieben
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
ms.openlocfilehash: dff3e4eb9d99288914fb6d4e9a6e2d22aa38689cdc6b60f227e7e5ba2e0c5323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349364"
---
# <a name="win32_tsclientsetting-class"></a>Win32 \_ TSClientSetting-Klasse

Die WMI-Klasse **Win32 \_ TSClientSetting** definiert Konfigurationseinstellungen für die [**Win32 \_ Terminal-Klasse**](win32-terminal.md) im Zusammenhang mit der Verbindungsrichtlinie.

Die folgende Syntax wird aus MOF-Code vereinfacht und enthält alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge. Referenzinformationen zu Methoden finden Sie in der Tabelle der Methoden weiter unten in diesem Thema.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **Win32 \_ TSClientSetting-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSClientSetting-Klasse** verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionSettings**](win32-tsclientsetting-connectionsettings.md)   | Legt die Eigenschaften **ConnectClientDrivesAtLogon,** **ConnectPrinterAtLogon** und **DefaultToClientPrinter** dieser Klasse fest.<br/>                      |
| [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md)                 | Wird nicht unterstützt.<br/> **Windows 7 und Windows Server 2008 R2:** Legt die **AllowDwm-Eigenschaft** fest.<br/>                                               |
| [**SetClientProperty**](win32-tsclientsetting-setclientproperty.md)     | Legt die Eigenschaften **LPTPortMapping,** **COMPortMapping,** **AudioMapping,** **ClipboardMapping,** **DriveMapping** oder **WindowsPrinterMapping** fest.<br/> |
| [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md)             | Legt die **ColorDepth-Eigenschaft** fest.<br/>                                                                                                                 |
| [**SetColorDepthPolicy**](win32-tsclientsetting-setcolordepthpolicy.md) | Legt die **ColorDepthPolicy-Eigenschaft** fest.<br/>                                                                                                           |
| [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md)           | Legt die **MaxMonitors-Eigenschaft** fest.<br/>                                                                                                                |
| [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md)     | Legt die **MaxXResolution-Eigenschaft** fest.<br/>                                                                                                             |
| [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md)     | Legt die **MaxYResolution-Eigenschaft** fest.<br/>                                                                                                             |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSClientSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AdvancedRemoteAppGraphics**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob erweiterte RemoteFX Grafiken für RemoteApp aktiviert werden sollen.

**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2012 R2 und Windows 8.1 nicht verfügbar.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Erweiterte Grafiken sind deaktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Erweiterte Grafiken sind aktiviert.

</dd> </dl>

</dd> <dt>

**AllowDwm**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft ist nicht verfügbar.

**Windows 7 und Windows Server 2008 R2: **

Gibt an, ob die Remotedesktopkomposition aktiviert oder deaktiviert werden soll. Null deaktiviert die Remotedesktopkomposition, und ein Wert ungleich 0 (null) aktiviert ihn.

Verwenden Sie die [**SetAllowDwm-Methode,**](setallowdwm-win32-tsclientsetting.md) um diese Eigenschaft zu ändern.

</dd> <dt>

**AudioCaptureRedir**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Umleitung von Audioaufnahmen zugelassen werden soll.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.

<dt>

<span id="FALSE"></span><span id="false"></span>

**FALSE** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**TRUE** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**AudioMapping**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Audiozuordnung deaktiviert oder aktiviert ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Die Audiozuordnung ist aktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Die Audiozuordnung ist deaktiviert.

</dd> </dl>

</dd> <dt>

**AVC444ModePreferred**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der AVC444-Modus bevorzugt wird.

**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 10 oder Windows Server 2016 nicht verfügbar.

<dt>

<span id="FALSE"></span><span id="false"></span>

**FALSE** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**TRUE** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Beschreibung (einzeilige Zeichenfolge) des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**ClipboardMapping**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zwischenablagezuordnung deaktiviert oder aktiviert ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Die Zwischenablagezuordnung ist aktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Die Zwischenablagezuordnung ist deaktiviert.

</dd> </dl>

</dd> <dt>

**ColorDepth**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Farbtiefe an. Mögliche Werte finden Sie in der [**SetColorDepth-Methode.**](win32-tsclientsetting-setcolordepth.md)

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span id="8_bit"></span><span id="8_BIT"></span>**8 Bit** (1)


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span id="15_bit"></span><span id="15_BIT"></span>**15 Bit** (2)


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span id="16_bit"></span><span id="16_BIT"></span>**16 Bit** (3)


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span id="24_bit"></span><span id="24_BIT"></span>**24 Bit** (4)


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span id="32_bit"></span><span id="32_BIT"></span>**32 Bit** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ColorDepthPolicy**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die maximale Farbeinstellung des Benutzers überschrieben werden soll.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Setzen Sie die Richtlinie des Benutzers nicht außer Kraft.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Überschreiben Sie die Richtlinie des Benutzers.

</dd> </dl>

</dd> <dt>

**COMPortMapping**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die COM-Portzuordnung deaktiviert oder aktiviert ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Die COM-Portzuordnung ist aktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Die COM-Portzuordnung ist deaktiviert.

</dd> </dl>

</dd> <dt>

**ConnectClientDrivesAtLogon**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Laufwerke des Clients während des Anmeldevorgangs automatisch verbunden werden.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Laufwerke werden nicht automatisch verbunden.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Laufwerke werden automatisch verbunden.

</dd> </dl>

</dd> <dt>

**ConnectionPolicy**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Richtlinie, die der Server zum Abrufen der Benutzerverbindungseinstellungen verwendet.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Pro Benutzer** (0)


</dt> <dd>

Die Verbindungseinstellungen des Benutzers sind wirksam.

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Serverüberschreibung** (1)


</dt> <dd>

Die Verbindungseinstellungen des Benutzers werden vom Server überschrieben.

</dd> </dl>

</dd> <dt>

**ConnectPrinterAtLogon**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob alle zugeordneten lokalen Drucker des Clients während des Anmeldevorgangs automatisch verbunden werden.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Lokale Drucker werden nicht automatisch verbunden.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Lokale Drucker werden automatisch verbunden.

</dd> </dl>

</dd> <dt>

**DefaultToClientPrinter**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Druckaufträge automatisch an den lokalen Drucker des Clients gesendet werden.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Druckaufträge sollen nicht automatisch an den lokalen Drucker des Clients gesendet werden.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Druckaufträge werden automatisch an den lokalen Drucker des Clients gesendet.

</dd> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**DriveMapping**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Laufwerkzuordnung deaktiviert oder aktiviert ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Die Laufwerkzuordnung ist aktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Die Laufwerkzuordnung ist deaktiviert.

</dd> </dl>

</dd> <dt>

**EncodeImageQuality**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die Imagequalität für die RDP-Benutzeroberfläche an.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

**verlustfrei** (1)


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

**hoch** (2)


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

**mittel** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HardwareGraphicsAdapter**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der RD-Sitzungshost Server den Hardwaregrafikrenderer als Standardadapter verwendet.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.

<dt>

<span id="FALSE"></span><span id="false"></span>

**FALSE** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**TRUE** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Das Datum, an dem das Objekt installiert wurde. Das Fehlen eines Werts gibt nicht an, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**LPTPortMapping**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die LPT-Portzuordnung deaktiviert oder aktiviert ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Die LPT-Portzuordnung ist aktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Die LPT-Portzuordnung ist deaktiviert.

</dd> </dl>

</dd> <dt>

**MaxMonitors**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von Monitoren, die vom Server unterstützt werden. Verwenden Sie die [**SetMaxMonitors-Methode,**](setmaxmonitors-win32-tsclientsetting.md) um diese Eigenschaft zu ändern.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.

</dd> <dt>

**MaxXResolution**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale X-Auflösung, die vom Server unterstützt wird. Verwenden Sie [**die SetMaxXResolution-Methode,**](setmaxxresolution-win32-tsclientsetting.md) um diese Eigenschaft zu ändern.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht vor Windows Server 2008 R2 und Windows 7 verfügbar.

</dd> <dt>

**MaxYResolution**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Y-Auflösung, die vom Server unterstützt wird. Verwenden Sie [**die SetMaxYResolution-Methode,**](setmaxyresolution-win32-tsclientsetting.md) um diese Eigenschaft zu ändern.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht vor Windows Server 2008 R2 und Windows 7 verfügbar.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**PNPRedirection**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Umleitung Plug & Play werden soll.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Zulassen Plug & Play Umleitung.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Lassen Sie keine Plug & Play zu.

</dd> </dl>

</dd> <dt>

**PolicyAdvancedRemoteAppGraphics**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die AdvancedRemoteAppGraphics-Eigenschaft** durch die Server- oder Gruppenrichtlinie konfiguriert wird.

**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht verfügbar, bevor Windows Server 2012 R2 und Windows 8.1.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceAllowDwm**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft ist nicht verfügbar.

**Windows 7 und Windows Server 2008 R2: **

Gibt an, ob **die AllowDwm-Eigenschaft** von der Server- oder Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceAudioCaptureRedir**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die AudioCaptureRedir-Eigenschaft** durch die Server- oder Gruppenrichtlinie konfiguriert wird.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht vor Windows Server 2008 R2 und Windows 7 verfügbar.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceAudioMapping**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, **ob die AudioMapping-Eigenschaft** vom Server, der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**PolicySourceAvc444ModePreferred**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, **wie die AVC444ModePreferredis-Eigenschaft** konfiguriert ist.

**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor dem Windows 10 oder Windows Server 2016.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceClipboardMapping**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt **an, ob die ClipboardMapping-Eigenschaft** vom Server, der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**PolicySourceColorDepth**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, **ob die ColorDepth-Eigenschaft** vom Server, der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**PolicySourceColorDepthPolicy**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, **ob die ColorDepthPolicy-Eigenschaft** vom Server, der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**PolicySourceCOMPortMapping**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, **ob die COMPortMapping-Eigenschaft** vom Server, der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**PolicySourceDefaultToClientPrinter**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, **ob die DefaultToClientPrinter-Eigenschaft** vom Server, der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**PolicySourceDriveMapping**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, **ob die DriveMapping-Eigenschaft** vom Server, der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**PolicySourceEncodeImageQuality**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie **EncodeImageQualityi** konfiguriert ist.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor dem Windows 8 oder Windows Server 2012.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceHardwareGraphicsAdapter**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie **HardwareGraphicsAdapter** konfiguriert ist.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor dem Windows 8 oder Windows Server 2012.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceLPTPortMapping**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, **ob die LPTPortMapping-Eigenschaft** vom Server, der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**PolicySourceMaxMonitors**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, **ob die MaxMonitors-Eigenschaft** vom Server, der Gruppenrichtlinie oder dem Standardwert konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht vor Windows Server 2008 R2 und Windows 7 verfügbar.

</dd> <dt>

**PolicySourceMaxResolution**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, **ob die Eigenschaften MaxXResolution** und **MaxYResolution** vom Server, der Gruppenrichtlinie oder dem Standardwert konfiguriert werden.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht vor Windows Server 2008 R2 und Windows 7 verfügbar.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**PolicySourcePNPRedirection**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die PNPRedirection-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceRemoteSessionProfile**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie **RemoteSessionProfile** konfiguriert ist.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor dem Windows 8 oder Windows Server 2012.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceSelectNetworkDetect**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie die **Eigenschaft SelectNetworkDetect** konfiguriert ist.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor dem Windows 8 oder Windows Server 2012.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceSelectTransport**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie die Eigenschaft **SelectTransport** konfiguriert ist.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceVideoPlaybackRedir**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **VideoPlaybackRedir-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceWindowsPrinterMapping**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **WindowsPrinterMapping-Eigenschaft** vom Server, der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**RemoteSessionProfile**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt das Profil für die RDP-Benutzeroberfläche an.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.

<dt>

<span id="scale"></span><span id="SCALE"></span>

**Skalierung** (1)


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

**Experience** (2)


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

**Bandbreite** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Wählen SieNetworkDetect aus.**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Netzwerkerkennung verwendet wird.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.

<dt>

0
</dt> <dd>

wird zur Verbindungszeit und im stabilen Zustand verwendet.

</dd> <dt>

1
</dt> <dd>

Zum Zeitpunkt der Verbindung deaktiviert

</dd> <dt>

2
</dt> <dd>

deaktiviert im stabilen Zustand

</dd> <dt>

3
</dt> <dd>

deaktiviert zur Verbindungszeit und im stabilen Zustand.

</dd> </dl>

</dd> <dt>

**Auswählen von "Transport"**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, welche Transportprotokolle für den RDP-Zugriff auf den Server verwendet werden können.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.

<dt>

0
</dt> <dd>

Verwenden Sie UDP und TCP.

</dd> <dt>

1
</dt> <dd>

Verwenden Sie nur TCP.

</dd> <dt>

2
</dt> <dd>

Verwenden Sie entweder UDP oder TCP.

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs- und Nichtoperationsstatus definiert werden. Betriebsstatus: "OK", "Heruntergestuft" und "Pred Fail" (ein Element, z. B. ein SMART-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, sagt aber einen Fehler in naher Zukunft vorher). Nichtoperationale Status: "Error", "Starting", "Stopping" und "Service". Letzteres, "Dienst", kann während des Spiegelungsresilverings eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Verwaltungsaufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Fehler")


</dt> <dd></dd> <dt>



 ("Heruntergestuft")


</dt> <dd></dd> <dt>



 ("Unbekannt")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Wird gestartet")


</dt> <dd></dd> <dt>



 ("Wird beendet")


</dt> <dd></dd> <dt>



 ("Dienst")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Terminals.

Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.

</dd> <dt>

**VideoPlaybackRedir**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Umleitung der Videowiedergabe zugelassen werden soll.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.

<dt>

<span id="FALSE"></span><span id="false"></span>

**FALSE** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**TRUE** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**WindowsPrinterMapping**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Druckerzuordnung für das Clientfenster deaktiviert oder aktiviert ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Die Druckerzuordnung ist aktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Die Druckerzuordnung ist deaktiviert.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass eine Fensterstation, die der Konsolensitzung zugeordnet ist, nicht auf die Methoden und Eigenschaften dieser Klasse zugreifen kann. Wenn versucht wird, dies zu tun, indem "Console" als Wert der **TerminalName-Eigenschaft** angegeben wird, geben Methoden dieses Objekts **WBEM \_ E NOT SUPPORTED \_ \_ zurück.** Dieser Fehlercode wird auch zurückgegeben, wenn eine Fensterstation versucht, Methoden dieses Objekts aufzurufen, um die Sicherheitseigenschaften der Konten LocalSystem, LocalService oder NetworkService hinzuzufügen oder zu ändern.

Um eine Verbindung mit dem \\ \\ CIMV2 \\ TerminalServices-Stammnamespace herzustellen, muss die Authentifizierungsebene Paketdatenschutz enthalten. Bei C/C++-Aufrufen ist dies eine Authentifizierungsebene von **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Bei Visual Basic- und Skriptaufrufen ist dies eine Authentifizierungsebene von **WbemAuthenticationLevelPktPrivacy** oder "pktPrivacy" mit dem Wert sechs.

Das folgende Beispiel Visual Basic Scripting Edition (VBScript) zeigt, wie Sie eine Verbindung mit einem Remotecomputer mit Paketschutz herstellen.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_Win32-Terminal**](win32-terminal.md)
</dt> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dt>

[**\_CIM-Einstellung**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

