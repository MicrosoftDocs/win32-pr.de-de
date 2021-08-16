---
description: Die \_ WMI-Klasse Win32 WMISetting singleton enthält die Betriebsparameter für den WMI-Dienst. Diese Klasse kann nur eine -Instanz haben, die immer für jedes Windows system vorhanden ist und nicht gelöscht werden kann. Zusätzliche Instanzen können nicht erstellt werden.
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Win32_WMISetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMISetting
- Win32_WMISetting.Caption
- Win32_WMISetting.Description
- Win32_WMISetting.SettingID
- Win32_WMISetting.ASPScriptDefaultNamespace
- Win32_WMISetting.ASPScriptEnabled
- Win32_WMISetting.AutorecoverMofs
- Win32_WMISetting.AutoStartWin9X
- Win32_WMISetting.BackupInterval
- Win32_WMISetting.BackupLastTime
- Win32_WMISetting.BuildVersion
- Win32_WMISetting.DatabaseDirectory
- Win32_WMISetting.DatabaseMaxSize
- Win32_WMISetting.EnableAnonWin9xConnections
- Win32_WMISetting.EnableEvents
- Win32_WMISetting.EnableStartupHeapPreallocation
- Win32_WMISetting.HighThresholdOnClientObjects
- Win32_WMISetting.HighThresholdOnEvents
- Win32_WMISetting.InstallationDirectory
- Win32_WMISetting.LastStartupHeapPreallocation
- Win32_WMISetting.LoggingDirectory
- Win32_WMISetting.LoggingLevel
- Win32_WMISetting.LowThresholdOnClientObjects
- Win32_WMISetting.LowThresholdOnEvents
- Win32_WMISetting.MaxLogFileSize
- Win32_WMISetting.MaxWaitOnClientObjects
- Win32_WMISetting.MaxWaitOnEvents
- Win32_WMISetting.MofSelfInstallDirectory
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 39c976a6a8b4c25fbc42561b7d0a8db52b9029f679ad72993f931efa596d2d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079574"
---
# <a name="win32_wmisetting-class"></a>Win32 \_ WMISetting-Klasse

Die **WMI-Klasse \_ Win32 WMISetting** singleton enthält die Betriebsparameter für den WMI-Dienst. [](../wmisdk/retrieving-a-class.md) Diese Klasse kann nur eine -Instanz haben, die immer für jedes Windows system vorhanden ist und nicht gelöscht werden kann. Zusätzliche Instanzen können nicht erstellt werden.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Singleton, Dynamic, Provider("WBEMCORE"), UUID("{A83EF166-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMISetting : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  string   ASPScriptDefaultNamespace = "\\\\root\\cimv2";
  boolean  ASPScriptEnabled;
  string   AutorecoverMofs[];
  uint32   AutoStartWin9X;
  uint32   BackupInterval;
  datetime BackupLastTime;
  string   BuildVersion;
  string   DatabaseDirectory;
  uint32   DatabaseMaxSize;
  boolean  EnableAnonWin9xConnections;
  boolean  EnableEvents;
  boolean  EnableStartupHeapPreallocation;
  uint32   HighThresholdOnClientObjects;
  uint32   HighThresholdOnEvents;
  string   InstallationDirectory;
  uint32   LastStartupHeapPreallocation;
  string   LoggingDirectory;
  uint32   LoggingLevel;
  uint32   LowThresholdOnClientObjects;
  uint32   LowThresholdOnEvents;
  uint32   MaxLogFileSize;
  uint32   MaxWaitOnClientObjects;
  uint32   MaxWaitOnEvents;
  string   MofSelfInstallDirectory;
};
```

## <a name="members"></a>Member

Die **Win32 \_ WMISetting-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ WMISetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ASPScriptDefaultNamespace**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ scripting Default \| Namespace")
</dt> </dl>

Standardskriptnamespace. Diese Eigenschaft enthält den Namespace, der von Aufrufen der Skripterstellungs-API für WMI verwendet wird, wenn keiner vom Aufrufer angegeben wird.

Diese Eigenschaft spiegelt den Wert im Registrierungsschlüssel wider.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **scripting Default \| Namespace**    

Beispiel: root \\ cimv2

Ein Beispielskript, das diese Eigenschaft verwendet, finden Sie im Abschnitt Hinweise.

</dd> <dt>

**ASPScriptEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ scripting Enable for \| ASP")
</dt> </dl>

True **gibt an,** dass WMI-Skripts auf Active Server Pages (ASP) verwendet werden können. Diese Eigenschaft ist nur auf Systemen gültig, auf denen nicht unterstützte Versionen von Windows werden. Bei unterstützten Windows ist WMI-Skripterstellung in ASP immer zulässig.

</dd> <dt>

**AutorecoverMofs**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Autorecover MOFs")
</dt> </dl>

Liste der vollqualifizierten MOF-Dateinamen, die zum Initialisieren oder Wiederherstellen des WMI-Repositorys verwendet werden. Die Liste bestimmt die Reihenfolge, in der MOF-Dateien kompiliert werden.

Diese Eigenschaft spiegelt den Wert im Registrierungsschlüssel wider.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Autoecover MOFs**    

</dd> <dt>

**AutoStartWin9X**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X")
</dt> </dl>

Wird nicht unterstützt.

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

**Nicht starten** (0)


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

**Automatischer Start** (1)


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

**Starten beim Neustart** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**BackupInterval**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Backup Interval Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")
</dt> </dl>

Wird nicht unterstützt. Sichern Sie stattdessen das WMI-Repository manuell.

</dd> <dt>

**BackupLastTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Functions \| GetTimeZoneInformation")
</dt> </dl>

Datum und Uhrzeit der letzten Sicherung.

</dd> <dt>

**BuildVersion**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \| Build")
</dt> </dl>

Versionsinformationen für den derzeit installierten WMI-Dienst.

Die Zeitspanne, die zwischen sicherungen der WMI-Datenbank verstreicht.

Diese Eigenschaft spiegelt den Wert im Registrierungsschlüssel wider.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| Build**

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

**DatabaseDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Repository Directory")
</dt> </dl>

Verzeichnispfad, der das WMI-Repository enthält.

</dd> <dt>

**DatabaseMaxSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Max DB Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Maximale Größe des WMI-Repositorys.

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

**EnableAnonWin9xConnections**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections")
</dt> </dl>

Wird nicht unterstützt.

</dd> <dt>

**Enableevents**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| EnableEvents")
</dt> </dl>

True **gibt an,** dass das WMI-Ereignissubsystem aktiviert sein sollte.

Diese Eigenschaft spiegelt den Wert im Registrierungsschlüssel wider.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**

</dd> <dt>

**EnableStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation")
</dt> </dl>

**True** gibt an, dass WMI einen vorab zugeordneten Heap mit der Größe des **LastStartupHeapPreallocation-Werts** erstellt, wenn WMI initialisiert wird.

</dd> <dt>

**HighThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| High Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")
</dt> </dl>

Maximale Rate, mit der vom Anbieter erstellte Objekte an Clients übermittelt werden können. Um Geschwindigkeitsunterschiede zwischen Anbietern und Clients zu berücksichtigen, enthält WMI Objekte in Warteschlangen, bevor sie an Consumer geliefert werden. Um die Effizienz zu erhöhen, müssen Consumer die Objekte in einer Geschwindigkeit erfassen, die dem Anbieter entspricht. Wenn der von nicht sortierten Objekten gehaltene Arbeitsspeicher **LowThresholdOnObjects** erreicht, verlangsamt WMI das Hinzufügen neuer Objekte in die Warteschlange. Wenn sich nicht gesammelte Ereignisse weiter ansammeln und die maximale Wartezeit für die Bereitstellung von Ereignissen in **MaxWaitOnClientObjects** erreicht wird, während der verwendete Arbeitsspeicher den Wert in **HighThresholdOnClientObjects** erreicht, akzeptiert WMI keine weiteren Objekte von Anbietern und gibt **WBEM \_ E OUT OF \_ \_ \_ MEMORY** an die Clients zurück.

</dd> <dt>

**HighThresholdOnEvents**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| High Threshold On Events"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Ereignisse pro Sekunde")
</dt> </dl>

Maximale Rate, mit der Ereignisse an Clients übermittelt werden sollen. Um Geschwindigkeitsunterschiede zwischen Anbietern und Clients zu berücksichtigen, stellt WMI Ereignisse in die Warteschlange, bevor sie an Consumer geliefert werden. Um die Effizienz zu erhöhen, müssen Consumer die Ereignisse in einer Geschwindigkeit sammeln, die dem Anbieter entspricht. Wenn der von nicht sortierten Ereignissen gespeicherte Arbeitsspeicher **LowThresholdOnObjects** erreicht, verlangsamt WMI das Hinzufügen neuer Ereignisse in die Warteschlange. Wenn sich nicht gesammelte Ereignisse weiter ansammeln und die maximale Wartezeit für die Bereitstellung von Ereignissen in **MaxWaitOnEvents** erreicht ist, während der verwendete Arbeitsspeicher den Wert in **HighThresholdOnEvents** aufnimmt, akzeptiert WMI keine weiteren Ereignisse von Anbietern und gibt **WBEM \_ E OUT OF \_ \_ \_ MEMORY** an die Clients zurück.

> [!Note]  
> Die Drosselung erfolgt nur für Permanente Ereignis-Consumer. Temporäre Consumer sollten daher keine Drosselung erwarten, wenn Ereignisse in der internen WMI-Ereigniswarteschlange gesichert werden.

 

Diese Eigenschaft spiegelt den Wert im Registrierungsschlüssel wider.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold on Client Objects (B)**    

</dd> <dt>

**InstallationDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM-Installationsverzeichnis") \|
</dt> </dl>

Verzeichnispfad, in dem die WMI-Software installiert wurde. Der Standardspeicherort ist \\ System32 \\ Wbem.

Diese Eigenschaft spiegelt den Wert im Registrierungsschlüssel wider.

**HKEY \_ Microsoft \_** \\  \\  \\ **WBEM-Installationsverzeichnis \|** für lokale Computersoftware

</dd> <dt>

**LastStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Größe des vorab zugeordneten Heaps, der von WMI während der Initialisierung erstellt wurde.

Diese Eigenschaft spiegelt den Wert im Registrierungsschlüssel wider.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**

</dd> <dt>

**LoggingDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Logging Directory")
</dt> </dl>

Verzeichnispfad, der den Speicherort der WMI-Systemprotokolldateien enthält.

Diese Eigenschaft spiegelt den Wert im Registrierungsschlüssel wider.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM Logging \| Directory**

</dd> <dt>

**LoggingLevel**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Logging")
</dt> </dl>

Aktivieren der Ereignisprotokollierung und des Ausführlichkeitsgrads der verwendeten Protokollierung.

Diese Eigenschaft spiegelt den Wert im Registrierungsschlüssel wider.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| Logging**

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Aus** (0)


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

**Fehlerprotokollierung** (1)


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

**Ausführliche Fehlerprotokollierung** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**LowThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Low Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")
</dt> </dl>

Rate, mit der WMI beginnt, die Erstellung neuer Objekte zu verlangsamen, die für Clients erstellt wurden. Um Geschwindigkeitsunterschiede zwischen Anbietern und Clients zu berücksichtigen, enthält WMI Objekte in Warteschlangen, bevor sie an Consumer geliefert werden. Um die Effizienz zu erhöhen, müssen Consumer die Objekte in einer Geschwindigkeit erfassen, die dem Anbieter entspricht. Wenn die Rate der Anforderungen für -Objekte **LowThresholdOnClientObjects** erreicht, verlangsamt WMI die Erstellung neuer Objekte schrittweise, um der Nutzungsrate des Clients zu entsprechen. Diese Verlangsamung beginnt, wenn die Rate, mit der Objekte erstellt werden, den Wert dieser Eigenschaft überschreitet. Weitere Informationen finden Sie unter **HighThresholdOnClientObjects.**

Diese Eigenschaft spiegelt den Registrierungswert wider.

**KEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold on Client Objects (B)**    

</dd> <dt>

**LowThresholdOnEvents**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Low Threshold On Events"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Ereignisse pro Sekunde")
</dt> </dl>

Rate, mit der WMI die Übermittlung neuer Ereignisse verlangsamt. Um Geschwindigkeitsunterschiede zwischen Anbietern und Clients zu berücksichtigen, stellt WMI Ereignisse in die Warteschlange, bevor sie an Consumer geliefert werden. Um die Effizienz zu erhöhen, müssen Consumer die Objekte in einer Geschwindigkeit erfassen, die dem Anbieter entspricht. Wenn die Warteschlange nicht mehr die Kontrolle hat, drosselt WMI die Übermittlung von Ereignissen und drosselt sie , um sie an die Clientrate anzupassen. Diese Verlangsamung beginnt, wenn die Rate, mit der Ereignisse generiert werden, den Wert dieser Eigenschaft überschreitet. Weitere Informationen finden Sie unter **HighThresholdOnEvents.**

> [!Note]  
> Die Drosselung erfolgt nur für permanente Ereignisverbraucher. Temporäre Consumer sollten daher keine Drosselung erwarten, wenn Ereignisse in der internen WMI-Ereigniswarteschlange gesichert werden.

 

Diese Eigenschaft spiegelt den Registrierungswert wider.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold on Client Objects {B}**    

</dd> <dt>

**MaxLogFileSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Log File Max Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Maximale Größe der protokolldateien, die vom WMI-Dienst erstellt werden.

Diese Eigenschaft spiegelt den Wert im Registrierungsschlüssel wider.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM Log File Max \| Size**

</dd> <dt>

**MaxWaitOnClientObjects**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

Die Zeitspanne, in der ein neu erstelltes Objekt auf die Verwendung durch den Client wartet, bevor es verworfen und ein Fehlerwert zurückgegeben wird. Diese Eigenschaft interagiert mit den Eigenschaften **LowThresholdOnClientObjects** und **HighThresholdOnClientObjects,** um die Übermittlung von Objekten an Consumer zu drosseln ( verlangsamen), wenn der Consumer die Objekte zu langsam empfängt.

</dd> <dt>

**MaxWaitOnEvents**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

Die Zeit, für die ein an einen Client gesendetes Ereignis in die Warteschlange gestellt wird, bevor es verworfen wird. Diese Eigenschaft interagiert0 mit **LowThresholdOnEvents** und **HighThresholdOnEvents,** um die Übermittlung von Objekten an Consumer zu drosseln , wenn der Consumer die Objekte zu langsam empfängt.

Diese Eigenschaft spiegelt den Registrierungswert wider.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Max Wait On Events (ms)**    

</dd> <dt>

**MofSelfInstallDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \| MOF Self-Install Directory")
</dt> </dl>

Verzeichnispfad für Anwendungen, die MOF-Dateien im WMI-Repository installieren. WMI kompiliert automatisch alle MOF-Dateien, die in diesem Verzeichnis platziert sind, und verschiebt die MOF je nach Erfolg in ein Unterverzeichnis mit der Bezeichnung "Gut" oder "Schlecht". Wenn \# [der Pragma-Befehl autorecover](../wmisdk/pragma-autorecover.md) enthalten ist, wird der vollqualifizierte Dateiname der Liste **AutorecoverMofs** hinzugefügt, die verwendet wird, wenn WMI das Repository initialisiert oder wiederherstellt. Die Liste bestimmt die Reihenfolge, in der MOFs kompiliert werden.

Diese Eigenschaft spiegelt den Wert im Registrierungsschlüssel wider.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| MOF Self=Install Directory**

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

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ WMISetting-Klasse** wird von der [**\_ CIM-Einstellung abgeleitet.**](cim-setting.md) Auf einem Computer kann nur eine Instanz dieser Klasse vorhanden sein.

Das Wissen, wie WMI auf einem Computer konfiguriert ist, kann sehr nützlich sein, wenn Sie Skripts debuggen oder Probleme mit dem WMI-Dienst selbst beheben. Beispielsweise werden viele WMI-Skripts unter der Annahme geschrieben, dass root cimv2 der Standardnamespace \\ auf dem Zielcomputer ist. Daher können Skriptautoren, die auf eine Klasse in "Root CIMv2" zugreifen müssen, den Namespace häufig nicht in den GetObject-Moniker enthalten, wie im folgenden \\ Codebeispiel gezeigt:

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

Wenn root \\ cimv2 nicht der Standardnamespace auf dem Zielcomputer ist, kann dieses Skript nicht ausgeführt werden. Um dies zu verhindern, muss der Namespacestamm \\ cimv2 im Moniker enthalten sein, wie im folgenden Codebeispiel gezeigt:

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

Wenn sich der Standardnamespace auf dem Zielcomputer von dem Namespace abt, der von einem Skript angenommen wird, kann das Skript nicht ausgeführt werden. Dem Benutzer wird dann die etwas irreführende Fehlermeldung "Ungültige Klasse" angezeigt. Tatsächlich liegt der Fehler nicht daran, dass die Klasse ungültig ist, sondern weil die Klasse nicht im Standardnamespace gefunden werden kann. Die Problembehandlung ist schwierig, da Sie wahrscheinlich mögliche Probleme mit der Klasse untersuchen werden, anstatt Probleme mit dem Namespace, der angegeben wurde (oder in diesem Fall nicht angegeben wurde).

Sie können die **Win32 \_ WMISetting-Klasse** verwenden, um zu bestimmen, wie WMI auf einem Computer konfiguriert wurde. Konfigurationsdetails wie der Standardnamespace oder die WMI-Buildnummer können bei der Behandlung von Skriptproblemen hilfreich sein. Diese Einstellungen enthalten auch wichtige administrative Informationen, z. B. wie oder sogar ob WMI-Fehler auf einem Computer protokolliert werden und welche WMI-Anbieter automatisch neu geladen werden, wenn Sie das WMI-Repository neu erstellen müssen.

## <a name="examples"></a>Beispiele

Im [Codebeispiel Modify WMI Einstellungen](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript im TechNet Gallery wird die **Win32 \_ WMISetting-Klasse** verwendet, um das WMI-Sicherungsintervall und den Protokollierstand zu konfigurieren.

Im [Codebeispiel](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) List the Default Namespace VBScript (VbScript-Standardnamespace auflisten) im TechNet-Katalog wird die **Win32 \_ WMISetting-Klasse** verwendet, um die aktuelle WMI-Einstellung "Standardnamespace für Skripterstellung" abzurufen und anzuzeigen.

Im VbScript-Codebeispiel Ändern des [Standard-WMI-Namespaces](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) im TechNet-Katalog wird die **Eigenschaft ASPScriptDefaultNamespace** verwendet, um die WMI-Einstellung "Standardnamespace für Skripterstellung" auf "root \\ cimv2" zu setzen.

Das Codebeispiel List [All the WMI Einstellungen](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBSCript verwendet eine Reihe von Eigenschaften für **Win32 \_ WMISetting,** um eine Liste der WMI-Einstellungen zurück, die auf einem Computer konfiguriert sind.

Im [JavaScript-Codebeispiel](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) List WMI Setting Information (WMI-Einstellungsinformationen auflisten) wird eine Reihe von Eigenschaften für **Win32 \_ WMISetting** verwendet, um eine Liste der WMI-Einstellungen zurück, die auf einem Computer konfiguriert sind.

Im [Python-Codebeispiel List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) (WMI-Einstellungsinformationen auflisten) wird eine Reihe von Eigenschaften für **Win32 \_ WMISetting** verwendet, um eine Liste der auf einem Computer konfigurierten WMI-Einstellungen zurück zu geben.

Im REXX-Codebeispiel List [WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) Object (WMI-Einstellungsinformationsobjekt auflisten) wird eine Reihe von Eigenschaften für **Win32 \_ WMISetting** verwendet, um eine Liste der WMI-Einstellungen zurück, die auf einem Computer konfiguriert sind.

Das folgende VBScript-Codebeispiel zeigt, wie Sie die version of WMI abrufen, die auf dem lokalen Computer ausgeführt wird. "Win32 \_ WMISetting=@" gibt die einzelne Instanz der -Klasse an. Weitere Informationen finden Sie unter WMI-Versionen.


```VB
set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!/Root/CIMv2")

set objWMISetting = objWMIService.Get("Win32_WMISetting=@")

WScript.Echo  objWMISetting.BuildVersion
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Einstellung**](cim-setting.md)
</dt> <dt>

[WMI-Dienstverwaltungsklassen](./wmi-service-management-classes.md)
</dt> </dl>

 

 
