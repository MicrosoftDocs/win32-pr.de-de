---
description: Die \_ WMI-Klasse "Win32 processstartup abstract" stellt die Startkonfiguration eines Windows-basierten Prozesses dar.
ms.assetid: 78508404-cab2-42fb-a0ed-0e6e7d21408c
ms.tgt_platform: multiple
title: Win32_ProcessStartup-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProcessStartup
- Win32_ProcessStartup.CreateFlags
- Win32_ProcessStartup.EnvironmentVariables
- Win32_ProcessStartup.ErrorMode
- Win32_ProcessStartup.FillAttribute
- Win32_ProcessStartup.PriorityClass
- Win32_ProcessStartup.ShowWindow
- Win32_ProcessStartup.Title
- Win32_ProcessStartup.WinstationDesktop
- Win32_ProcessStartup.X
- Win32_ProcessStartup.XCountChars
- Win32_ProcessStartup.XSize
- Win32_ProcessStartup.Y
- Win32_ProcessStartup.YCountChars
- Win32_ProcessStartup.YSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b0be949b106c1fa88b37e0c7764dbddb0546ded7
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106368282"
---
# <a name="win32_processstartup-class"></a>Win32- \_ Klasse "processstartup"

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ processstartup** abstract" stellt die Startkonfiguration eines Windows-basierten Prozesses dar. Die-Klasse ist als Methodentyp Definition definiert, was bedeutet, dass Sie nur zum Übergeben von Informationen an die [**Create**](create-method-in-class-win32-process.md) -Methode der [**Win32- \_ Prozess**](win32-process.md) Klasse verwendet wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{8502C4DB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProcessStartup : Win32_MethodParameterClass
{
  uint32 CreateFlags;
  string EnvironmentVariables[];
  uint16 ErrorMode = 1;
  uint32 FillAttribute;
  uint32 PriorityClass;
  uint16 ShowWindow;
  string Title;
  string WinstationDesktop;
  uint32 X;
  uint32 XCountChars;
  uint32 XSize;
  uint32 Y;
  uint32 YCountChars;
  uint32 YSize;
};
```

## <a name="members"></a>Member

Die **Win32 \_ processstartup** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ processstartup** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**"Kreateflags"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Functions \| [**forateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwkreationflags")
</dt> </dl>

Weitere Werte, die die Prioritäts Klasse und die Erstellung des Prozesses steuern. Die folgenden Erstellungs Werte können mit Ausnahme der Angabe in beliebiger Kombination angegeben werden.

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Debuggen \_ Prozess** (1)


</dt> <dd>

Wenn dieses Flag festgelegt ist, wird der aufrufende Prozess als Debugger behandelt, und der neue Prozess wird debuggt. Das System benachrichtigt den Debugger über alle Debugereignisse, die beim Debuggen des Prozesses auftreten.

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Debuggen \_ Nur \_ dieser \_ Prozess** (2)


</dt> <dd>

Wenn dieses Flag nicht festgelegt ist und der aufrufende Prozess gedebuggt wird, wird der neue Prozess zu einem anderen Prozess, der gedebuggt wird. Wenn der aufrufende Prozess nicht debuggt wird, treten keine debuggingbezogenen Aktionen auf.

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Erstellen \_ Sie Angehalten (4** )


</dt> <dd>

Der primäre Thread des neuen Prozesses wird in einem angehaltenen Zustand erstellt und wird erst ausgeführt, wenn die [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) -Methode aufgerufen wird.

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Getrennt \_ Prozess** (8)


</dt> <dd>

Bei Konsolen Prozessen hat der neue Prozess keinen Zugriff auf die Konsole des übergeordneten Prozesses. Dieses Flag kann nicht verwendet werden, wenn das Flag zum **Erstellen einer \_ neuen \_ Konsole** festgelegt ist.

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Erstellen \_ Sie Neue \_ Konsole** (16)


</dt> <dd>

Dieser neue Prozess verfügt über eine neue Konsole, anstatt die übergeordnete Konsole zu erben. Dieses Flag kann nicht mit dem getrennten **\_ prozessflag** verwendet werden.

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Erstellen \_ Sie Neue \_ Prozess \_ Gruppe** (512)


</dt> <dd>

Dieser neue Prozess ist der Stamm Prozess einer neuen Prozessgruppe. Die Prozessgruppe umfasst alle Prozesse, bei denen es sich um nachfolgende Elemente dieses Stamm Prozesses handelt. Der Prozess Bezeichner der neuen Prozessgruppe ist mit dem Prozess Bezeichner identisch, der in der **ProcessID-** Eigenschaft der [**Win32- \_ Prozess**](win32-process.md) Klasse zurückgegeben wird. Prozessgruppen werden von der [**generateconsolectrlevent**](/windows/console/generateconsolectrlevent) -Methode verwendet, um das Senden von einem STRG + C-Signal oder einem STRG + UNTBR-Signal an eine Gruppe von Konsolen Prozessen zu aktivieren.

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Erstellen \_ Sie Unicode- \_ Umgebung** (1024)


</dt> <dd>

Die in der Umgebungs **variables** -Eigenschaft aufgelisteten Umgebungseinstellungen verwenden Unicode-Zeichen. Wenn dieses Flag nicht festgelegt ist, verwendet der Umgebungsblock ANSI-Zeichen.

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Erstellen \_ Sie Standard \_ Fehler \_ Modus** (67108864)


</dt> <dd>

Neu erstellte Prozesse erhalten den Standardfehler Modus des aufrufenden Prozesses, anstatt den Fehler Modus des übergeordneten Prozesses zu erben. Dieses Flag eignet sich für multithreadshell-Anwendungen, die mit deaktivierten hart Fehlern ausgeführt werden.

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**Erstellen \_ Sie Breakaway \_ von \_ Auftrag** (16777216)


</dt> <dd>

Wird für den erstellten Prozess verwendet, der nicht durch das Auftrags Objekt eingeschränkt werden darf.

</dd> </dl>

</dd> <dt>

**EnvironmentVariables**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ Current \_ User \\ \\ Environment")
</dt> </dl>

Liste der Einstellungen für die Konfiguration eines Computers. Umgebungsvariablen geben Suchpfade für Dateien, Verzeichnisse für temporäre Dateien, anwendungsspezifische Optionen und andere ähnliche Informationen an. Das System verwaltet einen Block von Umgebungseinstellungen für jeden Benutzer und einen für den Computer. Der System Umgebungsblock stellt Umgebungsvariablen für alle Benutzer eines bestimmten Computers dar. Der Umgebungsblock eines Benutzers stellt die Umgebungsvariablen dar, die das System für einen bestimmten Benutzer verwaltet, und enthält den Satz von System Umgebungsvariablen. Standardmäßig erhält jeder Prozess eine Kopie des Umgebungs Blocks für seinen übergeordneten Prozess. In der Regel handelt es sich hierbei um den Umgebungsblock für den angemeldeten Benutzer. Von einem Prozess können unterschiedliche Umgebungs Blöcke für die untergeordneten Prozesse angegeben werden.

</dd> <dt>

**Attribut ErrorMode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Error Functions (* Error Functions \| )")
</dt> </dl>

Bei einigen nicht-x86-Prozessoren verursachen falsch ausgerichtete Speicher Verweise eine Ausrichtungsfehler Ausnahme. **\_ \_ \_ Mit Ausnahme von Flag ohne Ausrichtung** können Sie steuern, ob ein Betriebssystem solche Ausrichtungsfehler automatisch korrigiert oder ob Sie für eine Anwendung sichtbar sind. Bei einer Plattform für Millionen von Anweisungen pro Sekunde (MIPS) muss eine Anwendung [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) explizit mit dem Flag **No \_ Alignment (keine Ausrichtungs \_ Fehler \_** ) abrufen, damit das Betriebssystem Ausrichtungsfehler automatisch beheben kann.

Wie ein Betriebssystem verschiedene Typen von schwerwiegenden Fehlern verarbeitet. Sie können angeben, dass das Betriebssystem Fehler oder eine Anwendung Fehler empfangen und verarbeiten kann.

Die Standardeinstellung ist, dass das Betriebssystem Ausrichtungsfehler für eine Anwendung sichtbar macht. Da die x86-Plattform keine Ausrichtungsfehler für eine Anwendung sichtbar macht, bewirkt der Fehler " **keine \_ Ausrichtung" \_ \_ mit Ausnahme** von Flag nicht, dass das Betriebssystem einen Ausrichtungsfehler ausgelöst hat – auch wenn das Flag nicht festgelegt ist. Der Standardzustand für [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) besteht darin, alle Flags auf 0 (null) festzulegen.

<dt>



 (1)


</dt> <dd>

Standard

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Fehler \_ Kritische \_ Fehler** (2)


</dt> <dd>

Wenn dieses Flag festgelegt ist, zeigt das Betriebssystem das Meldungs Feld kritischer Fehlerhandler nicht an, wenn ein solcher Fehler auftritt. Stattdessen sendet das Betriebssystem den Fehler an den aufrufenden Prozess.

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**Nein \_ Ausrichtungs \_ Fehler \_ außer** (4)


</dt> <dd>

Wenn dieses Flag festgelegt ist, korrigiert das Betriebssystem automatisch speicherausrichtungsfehler und macht Sie für die Anwendung unsichtbar. Dies erfolgt für die aufrufenden und Nachfolger Prozesse. Dieses Flag gilt nur für das eingeschränkte Anweisungs Satz Computing (RISC) und hat keine Auswirkungen auf x86-Prozessoren.

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**Nein \_ \_ \_ Fehler \_ Feld** für den GP-Fehler (8)


</dt> <dd>

Wenn dieses Flag festgelegt ist, zeigt das Betriebssystem beim Auftreten eines GP-Fehlers das Fehler Meldungs Feld "allgemeiner Schutz (GP)" nicht an. Dieses Flag sollte nur durch Debuggen von Anwendungen festgelegt werden, die GP-Fehler behandeln.

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**Nein \_ \_ \_ Fehler \_ Feld "Datei öffnen** " (16)


</dt> <dd>

Wenn dieses Flag festgelegt ist, zeigt das Betriebssystem kein Meldungs Feld an, wenn eine Datei nicht gefunden werden kann. Stattdessen wird der Fehler an den aufrufenden Prozess zurückgegeben. Dieses Flag wird zurzeit ignoriert.

</dd> </dl>

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwfillattribute")
</dt> </dl>

Die Text-und Hintergrundfarben, wenn ein neues Konsolenfenster in einer Konsolenanwendung erstellt wird. Diese Werte werden in grafischen Benutzeroberflächen Anwendungen (GUI) ignoriert. Fügen Sie die Werte hinzu, um Vordergrund-und Hintergrundfarben anzugeben. Wenn Sie z. b. einen roten Typ (4) auf einem blauen Hintergrund (16) haben möchten, legen Sie für FillAttribute den Wert 20 fest.

<dt>

1
</dt> <dd>

Vordergrund \_ blau

</dd> <dt>

2
</dt> <dd>

Vordergrund \_ grün

</dd> <dt>

4
</dt> <dd>

Vordergrund \_ rot

</dd> <dt>

8
</dt> <dd>

Vordergrund \_ Intensität

</dd> <dt>

16
</dt> <dd>

Hintergrund \_ blau

</dd> <dt>

32
</dt> <dd>

Hintergrund \_ grün

</dd> <dt>

64
</dt> <dd>

\_Roter Hintergrund

</dd> <dt>

128
</dt> <dd>

Hintergrund \_ Intensität

</dd> </dl>

</dd> <dt>

**PriorityClass**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**JobObject \_ Basic \_ Limit \_ Information**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass")
</dt> </dl>

Prioritäts Klasse für den neuen Prozess. Verwenden Sie diese Eigenschaft, um die Zeit Plan Prioritäten der Threads im Prozess zu bestimmen. Wenn die Eigenschaft den Wert NULL hat, ist die Prioritäts Klasse standardmäßig auf normal –, es sei denn, die Prioritäts Klasse des erstellenden Prozesses ist in Leerlauf oder niedriger \_ In diesen Fällen empfängt der untergeordnete Prozess die Standard Prioritäts Klasse des aufrufenden Prozesses.

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)


</dt> <dd>

Gibt einen normalen Prozess ohne besondere Zeit Plan Anforderungen an.

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>Im **Leerlauf** (64)


</dt> <dd>

Gibt einen Prozess mit Threads an, die nur ausgeführt werden, wenn sich das System im Leerlauf befindet und durch die Threads eines Prozesses, der in einer höheren Prioritäts Klasse ausgeführt wird, vorzeitig entfernt werden. Ein Beispiel hierfür ist ein Bildschirmschoner. Die inaktive Prioritäts Klasse wird von untergeordneten Prozessen geerbt.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Hoch** (128)


</dt> <dd>

Gibt einen Prozess an, der zeitkritische Aufgaben ausführt, die sofort ausgeführt werden müssen, damit Sie ordnungsgemäß ausgeführt werden. Die Threads eines Klassen Prozesses mit hoher Priorität haben Vorrang vor den Threads der Klassen Prozesse mit normaler Priorität oder der Leerlauf Priorität. Ein Beispiel hierfür ist Windows Aufgabenliste, das beim Aufruf durch den Benutzer schnell reagieren muss, unabhängig von der Last des Betriebssystems. Verwenden Sie extrem Sorgfalt bei der Verwendung der Klasse mit hoher Priorität, weil eine CPU-gebundene Klasse mit hoher Priorität fast alle verfügbaren Zyklen verwenden kann. Nur die echtzeitpriorität wird auf diese Ebene festgelegt.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)


</dt> <dd>

Gibt einen Prozess an, der über die höchste mögliche Priorität verfügt. Die Threads eines echt Zeit Prioritäts Klassen Prozesses haben Vorrang vor den Threads aller anderen Prozesse – einschließlich Threads mit hoher Priorität und Betriebssystem Prozessen, die wichtige Aufgaben ausführen. Beispielsweise kann ein echt Zeit Prozess, der für mehr als ein sehr kurzes Intervall ausgeführt wird, dazu führen, dass Datenträger Caches nicht geleert werden oder dass die Maus nicht mehr reagiert.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Unten \_ Normal** (16384)


</dt> <dd>

Gibt einen Prozess an, der eine Priorität hat, die höher als der Leerlauf, aber niedriger als normal ist.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Oben \_ Normal** (32768)


</dt> <dd>

Gibt einen Prozess an, der eine Priorität hat, die höher als normal, aber kleiner als hoch ist.

</dd> </dl>

</dd> <dt>

**ShowWindow**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow")
</dt> </dl>

Gibt an, wie das Fenster dem Benutzer angezeigt wird. Dabei kann es sich um einen beliebigen Wert handeln, der im *nCmdShow* -Parameter für die [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) -Funktion angegeben werden kann.

</dd> <dt>

**Titel**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lptitle")
</dt> </dl>

Text, der in der Titelleiste angezeigt wird, wenn ein neues Konsolenfenster erstellt wird. wird für Konsolen Prozesse verwendet. Wenn der Wert **null** ist, wird der Name der ausführbaren Datei als Fenstertitel verwendet. Diese Eigenschaft muss für GUI-oder Konsolen Prozesse, die kein neues Konsolenfenster erstellen, den Wert **null** aufweisen.

</dd> <dt>

**WinstationDesktop**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpdesktop")
</dt> </dl>

Der Name des Desktops oder der Name der Desktop-und Fenster Station für den Prozess. Ein umgekehrter Schrägstrich in der Zeichenfolge gibt an, dass die Zeichenfolge sowohl Desktop-als auch Fenster Stationsnamen enthält Wenn **WinstationDesktop** **null** ist, erbt der neue Prozess den Desktop und die Fenster Station des übergeordneten Prozesses. Wenn **WinstationDesktop** eine leere Zeichenfolge ist, erbt der Prozess nicht den Desktop und die Fenster Station des übergeordneten Prozesses. Das System bestimmt, ob eine neue Desktop-und Fenster Station erstellt werden muss. Eine Fenster Station ist ein sicheres Objekt, das eine Zwischenablage, eine Reihe globaler Atome und eine Gruppe von Desktop Objekten enthält. Die interaktive Fenster Station, die der Anmelde Sitzung des interaktiven Benutzers zugewiesen ist, enthält auch das Tastatur-, Maus-und Anzeigegerät. Ein Desktop ist ein sicheres Objekt, das in einer Fenster Station enthalten ist. Ein Desktop verfügt über eine logische Anzeige Oberfläche und enthält Fenster, Menüs und Hooks. Eine Fenster Station kann über mehrere Desktops verfügen. Nur die Desktops der interaktiven Fenster Station können sichtbar sein und Benutzereingaben empfangen.

</dd> <dt>

**X**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| DWX")
</dt> </dl>

Der X-Offset der oberen linken Ecke eines Fensters, wenn ein neues Fenster erstellt wird – in Pixel. Die Offsets befinden sich in der oberen linken Ecke des Bildschirms. Bei GUI-Prozessen wird die angegebene Position verwendet, wenn der neue Prozess zum ersten Mal das überlappende [**Fenster aufruft,**](/windows/win32/api/winuser/nf-winuser-createwindowa) um ein überlappendes Fenster zu erstellen, wenn der *X* -Parameter von "up **Window** " den Wert **CW \_ usedefault** hat.

> \[! Hinweis X\]  
> und **Y** können nicht unabhängig angegeben werden.

 

</dd> <dt>

**Xcountrytchars**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| xcountrytchars")
</dt> </dl>

Breite des Bildschirm Puffers in Zeichen Spalten. Diese Eigenschaft wird für Prozesse verwendet, die ein Konsolenfenster erstellen, und wird in GUI-Prozessen ignoriert.

> [!Note]  
> **Xzähltchars** und **yzähltchars** können nicht unabhängig angegeben werden.

 

</dd> <dt>

**Xsize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwxsize")
</dt> </dl>

Pixel Breite eines Fensters, wenn ein neues Fenster erstellt wird. Für GUI-Prozesse wird dies nur verwendet, wenn der neue [**Prozess zum ersten**](/windows/win32/api/winuser/nf-winuser-createwindowa) Mal das überlappende Fenster aufruft, um ein überlappendes Fenster zu erstellen, wenn der nwidth-Parameter von "up **Window** " den Wert **CW \_ usedefault** hat.

> [!Note]  
> **XSize** und **YSize** können nicht unabhängig angegeben werden.

 

</dd> <dt>

**J**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwy")
</dt> </dl>

Der Pixel Offset der oberen linken Ecke eines Fensters, wenn ein neues Fenster erstellt wird. Die Offsets befinden sich in der oberen linken Ecke des Bildschirms. Bei GUI-Prozessen wird die angegebene Position verwendet, wenn der neue Prozess zum ersten Mal das überlappende [**Fenster aufruft,**](/windows/win32/api/winuser/nf-winuser-createwindowa) um ein überlappendes Fenster zu erstellen, wenn der *y* -Parameter von "up **Window** " den Wert **CW \_ usedefault** hat.

> \[! Hinweis X\]  
> und **Y** können nicht unabhängig angegeben werden.

 

</dd> <dt>

**Ycountrytchars**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| yzähltchars")
</dt> </dl>

Höhe des Bildschirm Puffers in Zeichen Zeilen. Diese Eigenschaft wird für Prozesse verwendet, die ein Konsolenfenster erstellen, wird jedoch in GUI-Prozessen ignoriert.

> [!Note]  
> **Xzähltchars** und **yzähltchars** können nicht unabhängig angegeben werden.

 

</dd> <dt>

**Ysize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwysize")
</dt> </dl>

Die Pixelhöhe eines Fensters, wenn ein neues Fenster erstellt wird. Für GUI-Prozesse wird dies nur beim ersten Aufrufen von " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) " durch den neuen Prozess zum Erstellen eines überlappenden Fensters verwendet, wenn der *nwidth* -Parameter von "up **Window** " den Wert " **CW \_ usedefault**" hat.

> [!Note]  
> **XSize** und **YSize** können nicht unabhängig angegeben werden.

 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von [**Win32 \_ methodparameterclass**](win32-methodparameterclass.md)abgeleitet.

Übersicht

Die [**Win32 \_ Process**](win32-process.md) [**Create**](create-method-in-class-win32-process.md) -Methode ermöglicht Ihnen das Konfigurieren von Startoptionen für jeden neuen Prozess, der auf einem Computer ausgeführt wird. Beispielsweise können Sie einen Prozess so konfigurieren, dass er in einem "ausgeblendeten" Fenster gestartet wird. Dadurch wird verhindert, dass ein Benutzer es sieht und möglicherweise unterbricht. Wenn der Prozess in einem Befehlsfenster ausgeführt wird, können Sie Größe, Titel und Vordergrund-und Hintergrundfarben des Fensters konfigurieren.

Startoptionen werden mithilfe der Win32-Klasse " **\_ processstartup** " konfiguriert. **Win32 \_ Processstartup** ist eine Klasse vom Typ "Methode". die Type-Methode der Methode ist nur vorhanden, um Informationen an eine Methode zu übergeben. In diesem Fall werden alle Eigenschaften einer Instanz von **Win32 \_ processstartup** an eine Instanz des [**Win32- \_ Prozesses**](win32-process.md)übermittelt.

**Verwenden von Win32 \_ processstartup**

1.  Erstellen Sie eine Instanz von **Win32 \_ processstartup**.
2.  Konfigurieren Sie die Eigenschaften der neuen Instanz.
3.  Fügen Sie die-Instanz als Teil der [**Win32 \_ Process**](win32-process.md) Create-Methode ein.

Wenn Sie z. b. eine **Win32- \_ processstartup** -Instanz mit dem Namen objconfig erstellt haben, würden Sie den Objektnamen in der Create-Methode wie folgt übergeben:

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a>Beispiele

Sie können die **Win32 \_ processstartup** -Klasse verwenden, um verschiedene Startoptionen für einen Prozess zu konfigurieren. Zu diesen Optionen zählen unter anderem das Erstellen eines Prozesses in einem ausgeblendeten Fenster und das Erstellen eines Prozesses mit höherer Priorität. Mit dem folgenden VBScript wird ein Prozess in einem verborgenen Fenster erstellt.


```VB
Const HIDDEN_WINDOW = 12
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
errReturn = objProcess.Create("Notepad.exe", null, objConfig, intProcessID)
```



Das folgende VBScript-Objekt erstellt einen Prozess mit höherer Priorität.


```VB
Const ABOVE_NORMAL = 32768
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.PriorityClass = ABOVE_NORMAL
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
objProcess.Create "Database.exe", Null, objConfig, intProcessID
```



Im folgenden VBScript-Codebeispiel wird ein Notepad-Prozess auf dem lokalen Computer erstellt. **Win32 \_ Processstartup** wird verwendet, um die Prozesseinstellungen zu konfigurieren.


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ methodparameterclass**](win32-methodparameterclass.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[**Win32- \_ Prozess**](win32-process.md)
</dt> <dt>

[**\_\_Providerhostquotaconfiguration**](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[WMI-Tasks: Prozesse](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
