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
# <a name="win32_tsclientsetting-class"></a>Win32- \_ tsclientsetting-Klasse

Die **Win32 \_ tsclientsetting** -WMI-Klasse definiert Konfigurationseinstellungen für die [**Win32- \_ Terminal**](win32-terminal.md) Klasse, die mit der Verbindungsrichtlinie verknüpft ist.

Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge. Referenzinformationen zu-Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.

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

Die Win32-Klasse " **\_ tsclientsetting** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ tsclientsetting** -Klasse verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionSettings**](win32-tsclientsetting-connectionsettings.md)   | Legt die Eigenschaften **connectclientdrivesatlogon**, **connectprinteratlogon** und **defaultdeclientprinter** dieser Klasse fest.<br/>                      |
| [**"Abrunden lowdwm"**](setallowdwm-win32-tsclientsetting.md)                 | Wird nicht unterstützt.<br/> **Windows 7 und Windows Server 2008 R2:** Legt die **allowdwm** -Eigenschaft fest.<br/>                                               |
| [**Setclientproperty**](win32-tsclientsetting-setclientproperty.md)     | Legt die Eigenschaften **lptportmapping**, **COMPortMapping**, **audiomapping**, **ClipboardMapping**, **DriveMapping** oder **WindowsPrinterMapping** fest.<br/> |
| [**Setcolortiefe**](win32-tsclientsetting-setcolordepth.md)             | Legt die **colortiefe** -Eigenschaft fest.<br/>                                                                                                                 |
| [**Setcolordepthpolicy**](win32-tsclientsetting-setcolordepthpolicy.md) | Legt die **ColorDepthPolicy** -Eigenschaft fest.<br/>                                                                                                           |
| [**Setmaxmonitors**](setmaxmonitors-win32-tsclientsetting.md)           | Legt die **maxmonitors** -Eigenschaft fest.<br/>                                                                                                                |
| [**Setmaxxresolution**](setmaxxresolution-win32-tsclientsetting.md)     | Legt die **maxxresolution** -Eigenschaft fest.<br/>                                                                                                             |
| [**Setmaxyresolution**](setmaxyresolution-win32-tsclientsetting.md)     | Legt die **maxyresolution** -Eigenschaft fest.<br/>                                                                                                             |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ tsclientsetting** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Advancedremoteappgraphics**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob erweiterte remotefx-Grafiken für RemoteApp aktiviert werden sollen.

**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2012 R2 und Windows 8.1 nicht verfügbar.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Erweiterte Grafiken sind deaktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Erweiterte Grafiken sind aktiviert.

</dd> </dl>

</dd> <dt>

**Allowdwm**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft ist nicht verfügbar.

* * Windows 7 und Windows Server 2008 R2: * *

Gibt an, ob die Remote Desktop Komposition aktiviert oder deaktiviert werden soll. NULL deaktiviert die Remote Desktop Komposition, und ein Wert ungleich NULL wird aktiviert.

Verwenden Sie [**die Methode**](setallowdwm-win32-tsclientsetting.md) "-Methode", um diese Eigenschaft zu ändern.

</dd> <dt>

**Audiocaptureredir**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die audioerfassungs Umleitung zulässig ist.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Audiomapping**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Audiozuordnung deaktiviert oder aktiviert ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Die Audiozuordnung ist aktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Die Audiozuordnung ist deaktiviert.

</dd> </dl>

</dd> <dt>

**AVC444ModePreferred**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der AVC444-Modus bevorzugt wird.

**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 10 oder Windows Server 2016 nicht verfügbar.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**ClipboardMapping**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zwischenablage Zuordnung deaktiviert oder aktiviert ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Die Zuordnung der Zwischenablage ist aktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Die Zuordnung der Zwischenablage ist deaktiviert.

</dd> </dl>

</dd> <dt>

**ColorDepth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Farbtiefe an. Mögliche Werte finden Sie unter der [**setcolortiefe**](win32-tsclientsetting-setcolordepth.md) -Methode.

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span id="8_bit"></span><span id="8_BIT"></span>**8-Bit** (1)


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span id="15_bit"></span><span id="15_BIT"></span>**15 Bit** (2)


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span id="16_bit"></span><span id="16_BIT"></span>**16 Bit** (3)


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span id="24_bit"></span><span id="24_BIT"></span>**24-Bit** (4)


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span id="32_bit"></span><span id="32_BIT"></span>**32-Bit** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ColorDepthPolicy**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die maximale Farbeinstellung des Benutzers überschrieben werden soll.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Überschreiben Sie die Richtlinie des Benutzers nicht.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Überschreiben Sie die Richtlinie des Benutzers.

</dd> </dl>

</dd> <dt>

**COMPortMapping**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die COM-Port Zuordnung deaktiviert oder aktiviert ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Die COM-Port Zuordnung ist aktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Die COM-Port Zuordnung ist deaktiviert.

</dd> </dl>

</dd> <dt>

**Connectclientdrivesatlogon**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Laufwerke des Clients während des Anmeldevorgangs automatisch verbunden werden.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Laufwerke werden nicht automatisch verbunden.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Laufwerke werden automatisch verbunden.

</dd> </dl>

</dd> <dt>

**ConnectionPolicy**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Richtlinie, die der Server zum Abrufen der Benutzer Verbindungseinstellungen verwendet.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Pro Benutzer** (0)


</dt> <dd>

Die Verbindungseinstellungen des Benutzers sind wirksam.

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-override** (1)


</dt> <dd>

Die Verbindungseinstellungen des Benutzers werden vom Server überschrieben.

</dd> </dl>

</dd> <dt>

**Connectprinteratlogon**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob alle zugeordneten lokalen Drucker des Clients während des Anmeldevorgangs automatisch verbunden werden.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Lokale Drucker werden nicht automatisch verbunden.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Lokale Drucker werden automatisch verbunden.

</dd> </dl>

</dd> <dt>

**Defaultdeclientprinter**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Druckaufträge automatisch an den lokalen Drucker des Clients gesendet werden.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Druckaufträge werden nicht automatisch an den lokalen Drucker des Clients gesendet.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Druckaufträge werden automatisch an den lokalen Drucker des Clients gesendet.

</dd> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**DriveMapping**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Laufwerk Zuordnung deaktiviert oder aktiviert ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Die Laufwerk Zuordnung ist aktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Die Laufwerk Zuordnung ist deaktiviert.

</dd> </dl>

</dd> <dt>

**Encodeimagequality**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die Bildqualität für die RDP-Darstellung an.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

**verlustfreie** (1)


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

**hoch** (2)


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

**Mittel** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Hardwaregraphicsadapter**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der RD-Sitzungshost Server den Hardware Grafik-Renderer als Standard Adapter verwendet.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Das Datum, an dem das Objekt installiert wurde. Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Lptportmapping**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die LPT-Port Zuordnung deaktiviert oder aktiviert ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Die LPT-Port Zuordnung ist aktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Die LPT-Port Zuordnung ist deaktiviert.

</dd> </dl>

</dd> <dt>

**Maxmonitors**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von Monitoren, die vom Server unterstützt werden. Verwenden Sie die [**setmaxmonitors**](setmaxmonitors-win32-tsclientsetting.md) -Methode, um diese Eigenschaft zu ändern.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.

</dd> <dt>

**Maxxresolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale X-Auflösung, die vom Server unterstützt wird. Verwenden Sie die [**setmaxxresolution**](setmaxxresolution-win32-tsclientsetting.md) -Methode, um diese Eigenschaft zu ändern.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.

</dd> <dt>

**Maxyresolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Y-Auflösung, die vom Server unterstützt wird. Verwenden Sie die [**setmaxyresolution**](setmaxyresolution-win32-tsclientsetting.md) -Methode, um diese Eigenschaft zu ändern.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Pnpredirection**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Plug & Play Umleitung zulässig ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Ermöglicht Plug & Play Umleitung.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Plug & Play Umleitung nicht zulassen.

</dd> </dl>

</dd> <dt>

**Policyadvancedremoteappgraphics**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **advancedremoteappgraphics** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2012 R2 und Windows 8.1 nicht verfügbar.

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

**Policysourceallowdwm**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft ist nicht verfügbar.

* * Windows 7 und Windows Server 2008 R2: * *

Gibt an, ob die **allowdwm** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourceaudiocaptureredir**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **audiocaptureredir** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourceaudiomapping**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **audiomapping** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

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

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie die **AVC444ModePreferredis** -Eigenschaft konfiguriert wird.

**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 10 oder Windows Server 2016 nicht verfügbar.

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

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **ClipboardMapping** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

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

**Policysourcecolortiefe**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **colortiefe** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

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

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **ColorDepthPolicy** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

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

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **COMPortMapping** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

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

**Policysourcedefaultdeclientprinter**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **defaultto clientprinter** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

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

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **DriveMapping** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

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

**Policysourceencodeimagequality**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie **encodeimagequalityi** konfiguriert wird.

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

**Policysourcehardwaregraphicsadapter**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie der **hardwaregraphicsadapter** konfiguriert ist.

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

**Policysourcelptportmapping**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **lptportmapping** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

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

**Policysourcemaxmonitors**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **maxmonitors** -Eigenschaft vom Server, von der Gruppenrichtlinie oder von der Standardeinstellung konfiguriert wird.

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

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.

</dd> <dt>

**Policysourcemaxresolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Eigenschaften **maxxresolution** und **maxyresolution** vom Server, von der Gruppenrichtlinie oder von der Standardeinstellung konfiguriert werden.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.

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

**Policysourcepnpredirection**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **pnpredirection** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourceremotesessionprofile**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie das **remotesessionprofile** -Verzeichnis konfiguriert ist.

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

**Policysourceselectnetworkdetect**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie die Eigenschaft " **selectnetworkdetect** " konfiguriert wird.

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

**Policysourceselecttransport**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie die **selecttransport** -Eigenschaft konfiguriert wird.

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

**Policysourcevideoplaybackredir**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **videoplaybackredir** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **WindowsPrinterMapping** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

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

**Remotesessionprofile**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt das Profil für den RDP-Vorgang an.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.

<dt>

<span id="scale"></span><span id="SCALE"></span>

**skalieren** (1)


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

Darstellung **(2** )


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

**Bandbreite** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Selectnetworkdetect**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Netzwerk Ermittlung verwendet wird.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist vor Windows 8 oder Windows Server 2012 nicht verfügbar.

<dt>

0
</dt> <dd>

wird zur Verbindungszeit und im stabilen Zustand verwendet.

</dd> <dt>

1
</dt> <dd>

zum Zeitpunkt der Verbindungs Herstellung deaktiviert

</dd> <dt>

2
</dt> <dd>

im stabilen Zustand deaktiviert

</dd> <dt>

3
</dt> <dd>

deaktiviert zur Verbindungszeit und im stabilen Zustand.

</dd> </dl>

</dd> <dt>

**Selecttransport**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
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

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen). Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service". Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

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

**Terminal Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Terminals.

Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.

</dd> <dt>

**Videoplaybackredir**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Umleitung von Videowiedergabe zugelassen wird.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows Server 2008 R2 und Windows 7 nicht verfügbar.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**WindowsPrinterMapping**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Drucker Zuordnung für das Fenster des Clients deaktiviert oder aktiviert ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Die Drucker Zuordnung ist aktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Die Drucker Zuordnung ist deaktiviert.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass eine Fenster Station, die der Konsolen Sitzung zugeordnet ist, nicht auf die Methoden und Eigenschaften dieser Klasse zugreifen kann. Wenn ein Versuch unternommen wird, indem "Console" als Wert der **Terminalname** -Eigenschaft angegeben wird, wird **WBEM \_ E \_ \_** von Methoden dieses Objekts zurückgegeben. Dieser Fehlercode wird auch zurückgegeben, wenn eine Fenster Station versucht, Methoden dieses Objekts aufzurufen, um die Sicherheitseigenschaften der Konten "LocalSystem", "LocalService" oder "Network Service" hinzuzufügen oder zu ändern.

Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten. Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**. Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von sechs.

Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ Terminal**](win32-terminal.md)
</dt> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dt>

[**CIM- \_ Einstellung**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

