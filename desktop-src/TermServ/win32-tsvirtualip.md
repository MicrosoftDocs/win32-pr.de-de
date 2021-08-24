---
title: Win32_TSVirtualIP-Klasse
description: Definiert IP-Virtualisierungseinstellungen (Internetprotokoll) für einen Remotedesktop-Sitzungshost-Server (RD-Sitzungshost Server).
ms.assetid: c37d572c-f6db-438b-8290-006a623c6593
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualIP-Remotedesktopdienste
- Win32_TSVirtualIP klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP
- Win32_TSVirtualIP.Caption
- Win32_TSVirtualIP.Description
- Win32_TSVirtualIP.InstallDate
- Win32_TSVirtualIP.Name
- Win32_TSVirtualIP.Status
- Win32_TSVirtualIP.VirtualIPActive
- Win32_TSVirtualIP.PolicySourceVirtualIPActive
- Win32_TSVirtualIP.VirtualIPMode
- Win32_TSVirtualIP.PolicySourceVirtualIPMode
- Win32_TSVirtualIP.ProgramList
- Win32_TSVirtualIP.PolicySourceProgramList
- Win32_TSVirtualIP.NetworkAdapterDescription
- Win32_TSVirtualIP.NetworkAdapterMacAddress
- Win32_TSVirtualIP.PolicySourceNetworkAdapter
- Win32_TSVirtualIP.NetworkAdapterDescriptionList
- Win32_TSVirtualIP.NetworkAdapterMacList
- Win32_TSVirtualIP.VirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28830e44fd54e9246cb0affc5fdde1427673d92e843adfd3e1e19cd221af370e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769050"
---
# <a name="win32_tsvirtualip-class"></a>Win32 \_ TSVirtualIP-Klasse

Definiert IP-Virtualisierungseinstellungen (Internetprotokoll) für einen Remotedesktop-Sitzungshost-Server (RD-Sitzungshost Server).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_TSVIRTUALIP_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIP : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   VirtualIPActive;
  uint32   PolicySourceVirtualIPActive;
  uint32   VirtualIPMode;
  uint32   PolicySourceVirtualIPMode;
  string   ProgramList[];
  uint32   PolicySourceProgramList;
  string   NetworkAdapterDescription;
  string   NetworkAdapterMacAddress;
  uint32   PolicySourceNetworkAdapter;
  string   NetworkAdapterDescriptionList[];
  string   NetworkAdapterMacList[];
  uint32   VirtualizeLoopbackAddressesEnabled;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSVirtualIP-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSVirtualIP-Klasse** verfügt über diese Methoden.



| Methode                                                                                                   | Beschreibung                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddProgram**](addprogram-win32-tsvirtualip.md)                                                       | Fügt der Liste der Programme, die IP-Virtualisierung verwenden, ein Programm hinzu.<br/>                                                                                                |
| [**RemoveProgram**](removeprogram-win32-tsvirtualip.md)                                                 | Entfernt ein Programm aus der Liste der Programme, die IP-Virtualisierung verwenden.<br/>                                                                                           |
| [**SelectNetworkAdapter**](selectnetworkadapter-win32-tsvirtualip.md)                                   | Legt die MAC-Adresse des Netzwerkadapters fest, der für die IP-Virtualisierung verwendet werden soll.<br/>                                                                                         |
| [**SetProgramList**](setprogramlist-win32-tsvirtualip.md)                                               | Überschreibt die Liste der Programme, die IP-Virtualisierung verwenden.<br/>                                                                                                       |
| [**SetVirtualIPActive**](setvirtualipactive-win32-tsvirtualip.md)                                       | Legt den **VirtualIPActive-Eigenschaftswert** fest.<br/>                                                                                                                      |
| [**SetVirtualIPMode**](setvirtualipmode-win32-tsvirtualip.md)                                           | Legt den **VirtualIPMode-Eigenschaftswert** fest.<br/>                                                                                                                        |
| [**SetVirtualizeLoopbackAddressesEnabled**](setvirtualizeloopbackaddressesenabled-win32-tsvirtualip.md) | Legt den **VirtualizeLoopbackAddressesEnabled-Eigenschaftswert** fest.<br/> **Windows Server 2008 R2:** Diese Methode ist vor der Windows Server 2012.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSVirtualIP-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Beschreibung (einzeilenbasierte Zeichenfolge) des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Das Datum, an dem das Objekt installiert wurde. Ein fehlender Wert gibt nicht an, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

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

**NetworkAdapterDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Beschreibung für den Netzwerkadapter.

</dd> <dt>

**NetworkAdapterDescriptionList**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Liste der Beschreibungen der verfügbaren physischen Netzwerkadapter.

</dd> <dt>

**NetworkAdapterMacAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die MAC-Adresse des Netzwerkadapters.

</dd> <dt>

**NetworkAdapterMacList**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Liste der MAC-Adressen der verfügbaren physischen Netzwerkadapter.

</dd> <dt>

**PolicySourceNetworkAdapter**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Netzwerkadapter vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**PolicySourceProgramList**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die ProgramList-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**PolicySourceVirtualIPActive**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die VirtualIPActive-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**PolicySourceVirtualIPMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die VirtualIPMode-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**ProgramList**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Programme an, die für die Verwendung der IP-Virtualisierung konfiguriert sind. Dies kann ein Programmname oder der vollständige Pfad sein.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene betriebsbereite und nicht betriebsbereite Status definiert werden. Folgende Betriebsstatus sind möglich: "OK", "Heruntergestuft" und "Fehler vor dem Ausfall" (ein Element, z. B. ein SMART-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber es wird in naher Zukunft ein Fehler vorhergesagt). Nicht operative Status sind: "Error", "Starting", "Stopping" und "Service". Letzteres, "Dienst", kann während der Spiegelung eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen administrativen Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element befindet sich weder in "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

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

**VirtualIPActive**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Gibt an, ob die IP-Virtualisierung auf dem Server aktiv ist. Dies kann einer der folgenden Werte sein.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Die IP-Virtualisierung ist nicht aktiv.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Die IP-Virtualisierung ist aktiv.

</dd> </dl>

</dd> <dt>

**VirtualIPMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, welcher IP-Virtualisierungsmodus auf dem Server verwendet wird. Dies kann einer der folgenden Werte sein.

<dt>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Pro Sitzung** (0)


</dt> <dd>

Der IP-Virtualisierungsmodus ist sitzungsweise.

</dd> <dt>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Pro Programm** (1)


</dt> <dd>

Der IP-Virtualisierungsmodus gilt pro Benutzer.

</dd> </dl>

</dd> <dt>

**VirtualizeLoopbackAddressesEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob loopback address virtualization aktiviert ist.

**Windows Server 2008 R2:** Diese Eigenschaft ist vor der Windows Server 2012.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Nicht aktiviert

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Aktiviert

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



 

