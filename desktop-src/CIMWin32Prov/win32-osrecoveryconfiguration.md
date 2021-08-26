---
description: Win32 \_ OSRecoveryConfiguration&\# 8194; Die WMI-Klasse stellt die Arten von Informationen dar, die aus dem Arbeitsspeicher gesammelt werden, wenn das Betriebssystem ausfällt. Dies schließt Startfehler und Systemabstürze ein.
ms.assetid: 0c8a2aeb-2fd9-44b7-8f91-d19afb8d2de6
ms.tgt_platform: multiple
title: Win32_OSRecoveryConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OSRecoveryConfiguration
- Win32_OSRecoveryConfiguration.Caption
- Win32_OSRecoveryConfiguration.Description
- Win32_OSRecoveryConfiguration.SettingID
- Win32_OSRecoveryConfiguration.AutoReboot
- Win32_OSRecoveryConfiguration.DebugFilePath
- Win32_OSRecoveryConfiguration.DebugInfoType
- Win32_OSRecoveryConfiguration.ExpandedDebugFilePath
- Win32_OSRecoveryConfiguration.ExpandedMiniDumpDirectory
- Win32_OSRecoveryConfiguration.KernelDumpOnly
- Win32_OSRecoveryConfiguration.MiniDumpDirectory
- Win32_OSRecoveryConfiguration.Name
- Win32_OSRecoveryConfiguration.OverwriteExistingDebugFile
- Win32_OSRecoveryConfiguration.SendAdminAlert
- Win32_OSRecoveryConfiguration.WriteDebugInfo
- Win32_OSRecoveryConfiguration.WriteToSystemLog
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a780e0997ef3a56bc644adda2842b905aaf9744d28a2075fbc4726134c16aa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972290"
---
# <a name="win32_osrecoveryconfiguration-class"></a>Win32 \_ OSRecoveryConfiguration-Klasse

Die **WMI-Klasse Win32 \_ OSRecoveryConfiguration** stellt die Typen von Informationen dar, die aus dem Arbeitsspeicher gesammelt werden, wenn das Betriebssystem ausfällt. [](../wmisdk/retrieving-a-class.md) Dies schließt Startfehler und Systemabstürze ein.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4E8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OSRecoveryConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AutoReboot;
  string  DebugFilePath;
  uint32  DebugInfoType;
  string  ExpandedDebugFilePath;
  string  ExpandedMiniDumpDirectory;
  boolean KernelDumpOnly;
  string  MiniDumpDirectory;
  string  Name;
  boolean OverwriteExistingDebugFile;
  boolean SendAdminAlert;
  boolean WriteDebugInfo;
  boolean WriteToSystemLog;
};
```

## <a name="members"></a>Member

Die **Win32 \_ OSRecoveryConfiguration-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ OSRecoveryConfiguration-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AutoReboot**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| AutoReboot")
</dt> </dl>

Das System wird während eines Wiederherstellungsvorgang automatisch neu gestartet.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen Objekts.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**DebugFilePath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| DumpFile")
</dt> </dl>

Vollständiger Pfad zur Debugdatei. Nach einem Computerausfall wird eine Debugdatei mit dem Arbeitsspeicherstatus des Computers erstellt.

Beispiel: "C: \\ Windows \\ Memory.dmp"

</dd> <dt>

**DebugInfoType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Typ der Debuginformationen, die in die Protokolldatei geschrieben werden.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (0)


</dt> <dd></dd> <dt>

<span id="Complete_memory_dump"></span><span id="complete_memory_dump"></span><span id="COMPLETE_MEMORY_DUMP"></span>

**Vollständiges Speicherabbild** (1)


</dt> <dd></dd> <dt>

<span id="Kernel_memory_dump"></span><span id="kernel_memory_dump"></span><span id="KERNEL_MEMORY_DUMP"></span>

**Kernel-Speicherabbild** (2)


</dt> <dd></dd> <dt>

<span id="Small_memory_dump"></span><span id="small_memory_dump"></span><span id="SMALL_MEMORY_DUMP"></span>

**Kleines Speicherabbild** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen -Objekts.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**ExpandedDebugFilePath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Erweiterte Version der **DebugFilePath-Eigenschaft.**

Beispiel: "C: \\ Windows \\ Memory.dmp"

</dd> <dt>

**ExpandedMiniDumpDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Erweiterte Version der **MiniDumpDirectory-Eigenschaft.**

Beispiel: "C: \\ Windows \\ MiniDump"

</dd> <dt>

**KernelDumpOnly**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| KernelDumpOnly")
</dt> </dl>

Nur Kerneldebuginformationen werden in die Debugprotokolldatei geschrieben. True **gibt** an, dass bei einem Systemfehler nur der Status des Kernels in eine Datei geschrieben wird. False **gibt** an, dass das System versucht, den Zustand des Arbeitsspeichers sowie alle Geräte zu protokollieren, die bei einem Fehler Informationen zum System bereitstellen können.

</dd> <dt>

**MiniDumpDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| MiniDumpDir")
</dt> </dl>

Verzeichnis, in dem kleine Speicherabbilddateien aufgezeichnet und gesammelt werden.

Beispiel: "%systemRoot% \\ MiniDump"

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](../wmisdk/key-qualifier.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Identifizieren des Namens für diese Instanz der **Win32 \_ OSRecoveryConfiguration-Klasse.**

</dd> <dt>

**OverwriteExistingDebugFile**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| Overwrite")
</dt> </dl>

Eine neue Debugdatei überschreibt eine vorhandene.

</dd> <dt>

**SendAdminAlert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| SendAlert")
</dt> </dl>

Bei einem Betriebssystemfehler wird eine Warnmeldung an den Systemadministrator gesendet.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Bezeichner, unter dem das aktuelle Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**WriteDebugInfo**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| CrashDumpEnabled")
</dt> </dl>

Debuginformationen müssen in eine Protokolldatei geschrieben werden.

</dd> <dt>

**WriteToSystemLog**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| LogEvent")
</dt> </dl>

Ereignisse werden in ein Systemprotokoll geschrieben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ OSRecoveryConfiguration-Klasse** wird von [**der \_ CIM-Einstellung**](cim-setting.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Einstellung**](cim-setting.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
