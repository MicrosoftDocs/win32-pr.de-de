---
description: Die \_ WMI-Klasse "Win32 wmisetting Singleton" enthält die Betriebsparameter für den WMI-Dienst. Diese Klasse kann nur über eine Instanz verfügen, die für jedes Windows-System immer vorhanden ist und nicht gelöscht werden kann. Es können keine zusätzlichen Instanzen erstellt werden.
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
ms.openlocfilehash: 8f94524d18074e3a35c7bcad09e9b9fba80e8470
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860683"
---
# <a name="win32_wmisetting-class"></a>Win32 \_ wmisetting-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ wmisetting** Singleton" enthält die Betriebsparameter für den WMI-Dienst. Diese Klasse kann nur über eine Instanz verfügen, die für jedes Windows-System immer vorhanden ist und nicht gelöscht werden kann. Es können keine zusätzlichen Instanzen erstellt werden.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

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

Die **Win32 \_ wmisetting** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ wmisetting** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**ASPScriptDefaultNamespace**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ Scripting \| Standard Namespace")
</dt> </dl>

Standardmäßiger Skript Namespace. Diese Eigenschaft enthält den Namespace, der von Aufrufen von der Skript-API für WMI verwendet wird, wenn keine vom Aufrufer angegeben wird.

Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **Scripting \| Standard Namespace**    

Beispiel: root \\ CIMV2

Ein Beispielskript, in dem diese Eigenschaft verwendet wird, finden Sie im Abschnitt "Hinweise".

</dd> <dt>

**ASPScriptEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ Scripting \| enable for ASP")
</dt> </dl>

**True** gibt an, dass WMI-Skripting auf Active Server Seiten (ASP) verwendet werden kann. Diese Eigenschaft gilt nur für Systeme, die nur nicht unterstützte Versionen von Windows ausführen. Für unterstützte Windows-Systeme ist die WMI-Skripterstellung in ASP immer zulässig.

</dd> <dt>

**Autorecovermufs**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutoRecover mufs")
</dt> </dl>

Liste der voll qualifizierten MOF-Dateinamen, die zum Initialisieren oder Wiederherstellen des WMI-Repository verwendet werden. Die Liste legt die Reihenfolge fest, in der MOF-Dateien kompiliert werden.

Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| AutoRecover-mufs**    

</dd> <dt>

**AutoStartWin9X**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X")
</dt> </dl>

Wird nicht unterstützt.

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

**Nicht starten** (0)


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

**Autostart** (1)


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

**Beim Neustart starten** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Sicherungs Intervall umfasst**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Backup Interval Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("Minutes")
</dt> </dl>

Wird nicht unterstützt. Sichern Sie das WMI-Repository stattdessen manuell.

</dd> <dt>

**BackupLastTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Functions \| GetTimeZoneInformation")
</dt> </dl>

Datum und Uhrzeit der letzten Sicherung.

</dd> <dt>

**BuildVersion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| Build")
</dt> </dl>

Versionsinformationen für den aktuell installierten WMI-Dienst.

Zeitspanne zwischen Sicherungen der WMI-Datenbank.

Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM \| Build**

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**DatabaseDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Repository Directory")
</dt> </dl>

Verzeichnispfad, der das WMI-Repository enthält.

</dd> <dt>

**Databasemaxsize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max DB Size"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")
</dt> </dl>

Maximale Größe des WMI-Repository.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**EnableAnonWin9xConnections**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| enableanonconnections")
</dt> </dl>

Wird nicht unterstützt.

</dd> <dt>

**EnableEvents**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| enableEvents")
</dt> </dl>

**True** gibt an, dass das WMI-Ereignis Subsystem aktiviert werden soll.

Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.

**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**

</dd> <dt>

**EnableStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation")
</dt> </dl>

**True** gibt an, dass WMI einen vorab zugeordneten Heap mit der Größe des **LastStartupHeapPreallocation** -Werts erstellt, wenn WMI initialisiert wird.

</dd> <dt>

**Highdie oldonclientobjects**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| High Threshold on Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("Objects per Second")
</dt> </dl>

Maximale Rate, mit der vom Anbieter erstellte Objekte an Clients übermittelt werden können. Um die Geschwindigkeit von Unterschieden zwischen Anbietern und Clients zu unterstützen, hält WMI Objekte in Warteschlangen vor der Übermittlung an Consumer. Zur Steigerung der Effizienz müssen die Consumer die Objekte in einem Tempo erfassen, das mit dem Anbieter übereinstimmt. Wenn der Speicher, der von nicht erfassten Objekten belegt wird, **Lowder oldonobjects** erreicht, verlangsamt WMI das Hinzufügen neuer Objekte in die Warteschlange. Wenn nicht erfasste Ereignisse weiterhin gesammelt werden und die maximale Wartezeit für das Übermitteln von Ereignissen in **maxwaitonclientobjects** erreicht wird, während der verwendete Arbeitsspeicher den Wert in **highationsoldonclientobjects** hat, nimmt WMI keine weiteren Objekte von Anbietern an und gibt **WBEM \_ E aus dem Arbeits \_ \_ \_ Speicher** an die Clients zurück.

</dd> <dt>

**Highderoldonevents**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| High Threshold on Events"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Ereignisse pro Sekunde")
</dt> </dl>

Maximale Rate, mit der Ereignisse an Clients übermittelt werden. Um die Geschwindigkeit von Unterschieden zwischen Anbietern und Clients zu unterstützen, werden Ereignisse in der WMI-Warteschlange vor der Übermittlung an Consumer Zur Steigerung der Effizienz müssen die Consumer die Ereignisse in einem Tempo erfassen, das mit dem Anbieter übereinstimmt. Wenn der Speicher, der von nicht gesammelten Ereignissen belegt wird, **Lowder oldonobjects** erreicht, verlangsamt WMI das Hinzufügen neuer Ereignisse in die Warteschlange. Wenn nicht gesammelte Ereignisse weiterhin kumuliert werden und die maximale Wartezeit für das Übermitteln von Ereignissen in **maxwaitonevents** erreicht wird, während der verwendete Arbeitsspeicher den Wert in **highationsoldonevents** hat, akzeptiert WMI keine weiteren Ereignisse von Anbietern und gibt **WBEM E nicht mehr den Arbeits \_ \_ \_ \_ Speicher** an die Clients zurück.

> [!Note]  
> Die Drosselung wird nur für permanente Ereignisconsumer durchgeführt, sodass temporäre Consumer keine Drosselung erwarten sollten, wenn Ereignisse in der internen WMI-Ereignis Warteschlange gesichert werden.

 

Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold on Client Objects (B)**    

</dd> <dt>

**InstallationDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM- \| Installationsverzeichnis")
</dt> </dl>

Verzeichnispfad, in dem die WMI-Software installiert wurde. Der Standard Speicherort ist \\ system32 \\ WBEM.

Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM- \| Installationsverzeichnis**

</dd> <dt>

**LastStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Größe des vorab zugeordneten Heaps, der während der Initialisierung von WMI erstellt wurde.

Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**

</dd> <dt>

**Loggingdirectory**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging Directory")
</dt> </dl>

Verzeichnispfad, der den Speicherort der WMI-System Protokolldateien enthält.

Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM- \| Protokollierungs Verzeichnis**

</dd> <dt>

**LoggingLevel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging")
</dt> </dl>

Aktivieren der Ereignisprotokollierung und des ausführlichkeits Grads der verwendeten Protokollierung.

Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM- \| Protokollierung**

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Aus** (0)


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

**Fehler Protokollierung** (1)


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

Ausführliche **Fehler Protokollierung** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Lowder oldonclientobjects**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Low Threshold on Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("Objects per Second")
</dt> </dl>

Rate, mit der WMI die Erstellung neuer Objekte verlangsamt, die für-Clients erstellt wurden. Um die Geschwindigkeit von Unterschieden zwischen Anbietern und Clients zu unterstützen, hält WMI Objekte in Warteschlangen vor der Übermittlung an Consumer. Zur Steigerung der Effizienz müssen die Consumer die Objekte in einem Tempo erfassen, das mit dem Anbieter übereinstimmt. Wenn die Anforderungs Rate von Objekten **lowationsoldonclientobjects** erreicht, verlangsamt WMI schrittweise die Erstellung neuer Objekte entsprechend der Verwendungsrate des Clients. Diese Verlangsamung beginnt, wenn die Rate, mit der Objekte erstellt werden, den Wert dieser Eigenschaft überschreitet. Siehe **highdie oldonclientobjects**.

Diese Eigenschaft gibt den Registrierungs Wert wieder.

**Schlüssel \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold on Client Objects (B)**    

</dd> <dt>

**Lowdie oldonevents**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Low Threshold on Events"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Ereignisse pro Sekunde")
</dt> </dl>

Rate, mit der WMI die Übermittlung neuer Ereignisse verlangsamt. Um die Geschwindigkeit von Unterschieden zwischen Anbietern und Clients zu unterstützen, werden Ereignisse in der WMI-Warteschlange vor der Übermittlung an Consumer Zur Steigerung der Effizienz müssen die Consumer die Objekte in einem Tempo erfassen, das mit dem Anbieter übereinstimmt. Wenn die Warteschlange nicht mehr von der Kontrolle ist, wird die WMI-Drosselung – verlangsamt – die Bereitstellung von Ereignissen nach und nach mit der Client Rate. Diese Verlangsamung beginnt, wenn die Rate, mit der Ereignisse generiert werden, den Wert dieser Eigenschaft überschreitet. Siehe **highdie oldonevents**.

> [!Note]  
> Die Drosselung wird nur für permanente Ereignisconsumer durchgeführt, sodass temporäre Consumer keine Drosselung erwarten sollten, wenn Ereignisse in der internen WMI-Ereignis Warteschlange gesichert werden.

 

Diese Eigenschaft gibt den Registrierungs Wert wieder.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold on Client Objects {B}**    

</dd> <dt>

**MaxLogFileSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| log file max size"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Maximale Größe der Protokolldateien, die vom WMI-Dienst erstellt werden.

Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM- \| Protokolldatei maximale Größe**

</dd> <dt>

**Maxwaitonclientobjects**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max Wait on Events"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millisekunden")
</dt> </dl>

Die Zeitspanne, die ein neu erstelltes Objekt auf die Verwendung durch den Client wartet, bevor es verworfen wird, und es wird ein Fehlerwert zurückgegeben. Diese Eigenschaft interagiert mit den Eigenschaften **lowmittloldonclientobjects** und **highmittloldonclientobjects** , um die – langsamer zu drosseln – die Übermittlung von Objekten an Consumer, wenn der Consumer die Objekte zu langsam empfängt.

</dd> <dt>

**Maxwaitonevents**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max Wait on Events"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millisekunden")
</dt> </dl>

Die Zeitspanne, für die ein Ereignis an einen Client in die Warteschlange eingereiht wird, bevor es verworfen wird. Diese Eigenschaft interacts0 mit **lowmittloldonevents** und **highmittloldonevents** zur Drosselung – verlangsamt die Übermittlung von Objekten an Consumer, wenn der Consumer die Objekte zu langsam empfängt.

Diese Eigenschaft gibt den Registrierungs Wert wieder.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Max. Wartezeit auf Ereignisse (MS)**    

</dd> <dt>

**"Mamaselfinstalldirectory"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| MOF Self-Install Directory")
</dt> </dl>

Verzeichnispfad für Anwendungen, die MOF-Dateien im WMI-Repository installieren. WMI kompiliert automatisch alle MOF-Dateien, die in diesem Verzeichnis abgelegt werden, und verschiebt die MOF-Datei, je nach Erfolg, in ein Unterverzeichnis mit der Bezeichnung "gut" oder "schlecht". Wenn der \# [pragma Auto Wiederherstellen](../wmisdk/pragma-autorecover.md) -Befehl enthalten ist, wird der voll qualifizierte Dateiname der **autorecovermufs** -Liste hinzugefügt, die verwendet wird, wenn WMI das Repository initialisiert oder wiederherstellt. In der Liste wird die Reihenfolge bestimmt, in der die Zusammenstellung von-und-

Diese Eigenschaft gibt den Wert im Registrierungsschlüssel wieder.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| MOF Self = Installationsverzeichnis**

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ wmisetting** -Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet. Auf einem Computer kann nur eine Instanz dieser Klasse vorhanden sein.

Das wissen, wie WMI auf einem Computer konfiguriert ist, kann sehr nützlich sein, wenn Sie Skripts debuggen oder Probleme mit dem WMI-Dienst selbst beheben. Beispielsweise werden viele WMI-Skripts unter der Annahme geschrieben, dass root \\ CIMV2 der Standard Namespace auf dem Zielcomputer ist. Daher kann es vorkommen, dass Skript Schreiber, die auf eine Klasse in "root \\ CIMv2" zugreifen müssen, den Namespace oft nicht in den GetObject-Moniker einschließen, wie im folgenden Codebeispiel gezeigt:

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

Wenn root \\ CIMV2 nicht der Standard Namespace auf dem Zielcomputer ist, kann dieses Skript nicht ausgeführt werden. Um dies zu verhindern, muss der Namespace Stamm \\ CIMV2 im Moniker enthalten sein, wie im folgenden Codebeispiel gezeigt:

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

Wenn sich der Standard Namespace auf dem Zielcomputer von dem Namespace unterscheidet, der von einem Skript angenommen wird, schlägt das Skript fehl. Darüber hinaus wird dem Benutzer die etwas irreführende Fehlermeldung "Ungültige Klasse" angezeigt. Der Fehler ist in Wahrheit nicht, weil die Klasse ungültig ist, aber weil die Klasse im Standard Namespace nicht gefunden werden kann. Dies ist ein schwieriges Problem bei der Problembehandlung, da Sie wahrscheinlich mögliche Probleme mit der-Klasse untersuchen und keine Probleme mit dem Namespace, der (oder in diesem Fall nicht) angegeben wurde.

Sie können die **Win32 \_ wmisetting** -Klasse verwenden, um zu bestimmen, wie WMI auf einem Computer konfiguriert wurde. Konfigurationsdetails wie z. b. der Standard Namespace oder die WMI-Buildnummer können bei der Problembehandlung von Skript Problemen nützlich sein. Diese Einstellungen bieten außerdem wichtige administrative Informationen, wie z. b. wie oder ob WMI-Fehler auf einem Computer protokolliert werden und welche WMI-Anbieter automatisch erneut geladen werden, wenn Sie das WMI-Repository neu erstellen müssen.

## <a name="examples"></a>Beispiele

Das Codebeispiel [Ändern von WMI-Einstellungen](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript in der TechNet Gallery verwendet die **Win32 \_ wmisetting** -Klasse, um das WMI-Sicherungs Intervall und den Protokolliergrad zu konfigurieren.

Der [Liste der Standard Namespace](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) VBScript-Code in der TechNet Gallery verwendet die **Win32 \_ wmisetting** -Klasse zum Abrufen und Anzeigen der aktuellen WMI-Einstellung "Standard Namespace für die Skripterstellung".

Das Codebeispiel für das [Ändern des standardmäßigen WMI-Namespace](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) VBScript in der TechNet Gallery verwendet die **ASPScriptDefaultNamespace** -Eigenschaft, um die WMI-Einstellung "Standard Namespace für die Skripterstellung" auf "root \\ CIMV2" festzulegen.

Das Codebeispiel [List All the WMI Settings](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBScript verwendet eine Reihe von Eigenschaften für **Win32 \_ wmisetting** , um eine Liste der auf einem Computer konfigurierten WMI-Einstellungen zurückzugeben.

Im JavaScript-Codebeispiel für das [Auflisten von WMI](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) -Einstellungs Informationen wird eine Reihe von Eigenschaften für **Win32- \_ wmisetting** verwendet, um eine Liste der auf einem Computer konfigurierten WMI-Einstellungen zurückzugeben.

Im python-Codebeispiel für das [Auflisten von WMI-Einstellungsinformationen](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) wird eine Reihe von Eigenschaften für **Win32 \_ wmisetting** verwendet, um eine Liste der auf einem Computer konfigurierten WMI-Einstellungen anzuzeigen.

Das Codebeispiel für die [Auflistung von WMI-Einstellungs Informationen](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) Objekt REXX verwendet eine Reihe von Eigenschaften für **Win32 \_ wmisetting** , um eine Liste der auf einem Computer konfigurierten WMI-Einstellungen zurückzugeben.

Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Sie die WMI-Version abrufen, die auf dem lokalen Computer ausgeführt wird. "Win32 \_ wmisetting = @" gibt die einzelne Instanz der Klasse an. Weitere Informationen finden Sie unter WMI-Versionen.


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> <dt>

[WMI-Dienst Verwaltungs Klassen](./wmi-service-management-classes.md)
</dt> </dl>

 

 
