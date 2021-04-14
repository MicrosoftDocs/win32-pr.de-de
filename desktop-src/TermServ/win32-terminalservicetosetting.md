---
title: Win32_TerminalServiceToSetting-Klasse
description: Stellt die Zuordnung zwischen einer Instanz der Win32 \_ Terminalservice-Klasse und der Einstellung einer bestimmten Win32 \_ terminalservicesetts-Eigenschaft dar.
ms.assetid: 4c206812-7549-4410-b6ba-1163f20d2bee
ms.tgt_platform: multiple
keywords:
- Win32_TerminalServiceToSetting-Klasse Remotedesktopdienste
- Win32_TerminalServiceToSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TerminalServiceToSetting
- Win32_TerminalServiceToSetting.Caption
- Win32_TerminalServiceToSetting.Description
- Win32_TerminalServiceToSetting.InstallDate
- Win32_TerminalServiceToSetting.Name
- Win32_TerminalServiceToSetting.Status
- Win32_TerminalServiceToSetting.Element
- Win32_TerminalServiceToSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d37a255b0a894ab257166f17c765f009d33b075
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391852"
---
# <a name="win32_terminalservicetosetting-class"></a>Win32 \_ terminalservicedesetting-Klasse

Die **Win32 \_ terminalservicedesetting** -WMI-Klasse stellt die Zuordnung zwischen einer Instanz der [**Win32 \_ Terminalservice**](win32-terminalservice.md) -Klasse und der Einstellung einer bestimmten [**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md) -Eigenschaft dar. Zu den Konfigurationseinstellungen gehören Remotedesktop-Sitzungshost (RD-Sitzungshost) Server Modus, Lizenzierung, aktiver Desktop, Berechtigungs Funktion, Löschen von temporären Ordnern und temporären Ordnern pro Sitzung.

Die folgende Syntax wird durch den MOF-Code vereinfacht und umfasst alle definierten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("Win32_WIN32_TERMINALSERVICETOSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceToSetting : CIM_ElementSetting
{
  string                           Caption;
  string                           Description;
  datetime                         InstallDate;
  string                           Name;
  string                           Status;
  Win32_TerminalService        REF Element;
  Win32_TerminalServiceSetting REF Setting;
};
```

## <a name="members"></a>Member

Die **Win32 \_ terminalservicetosetting** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ terminalservicedesetting** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

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

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ Terminalservice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Stellt die Instanz von [**Win32 \_ Terminalservice**](win32-terminalservice.md) dar, die mit der **Setting** -Eigenschaft konfiguriert werden kann.

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

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ terminalservicesetts**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Stellt die Remotedesktopdienste Konfigurationseinstellungen dar, die auf den zugeordneten RD-Sitzungshost Server angewendet werden können.

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

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

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

[**CIM- \_ Element Setting**](cim-elementsetting.md)
</dt> <dt>

[**Win32 \_ Terminalservice**](win32-terminalservice.md)
</dt> <dt>

[**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md)
</dt> <dt>

[**CIM- \_ Element Setting**](/windows/desktop/CIMWin32Prov/cim-elementsetting)
</dt> </dl>

 

