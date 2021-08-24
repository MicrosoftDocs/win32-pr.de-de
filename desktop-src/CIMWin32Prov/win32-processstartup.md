---
description: Die abstrakte \_ WMI-Klasse Win32 ProcessStartup stellt die Startkonfiguration eines Windows-basierten Prozesses dar.
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
ms.openlocfilehash: 10b0732b89d5240b457152f4bd19f951f69b8ee693baec54daea3bd6bbba9439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759350"
---
# <a name="win32_processstartup-class"></a>Win32 \_ ProcessStartup-Klasse

Die abstrakte [WMI-Klasse](../wmisdk/retrieving-a-class.md) **Win32 \_ ProcessStartup** stellt die Startkonfiguration eines Windows-basierten Prozesses dar. Die -Klasse ist als Methodentypdefinition definiert. Dies bedeutet, dass sie nur zum Übergeben von Informationen an die [**Create-Methode**](create-method-in-class-win32-process.md) der [**Win32 \_ Process-Klasse**](win32-process.md) verwendet wird.

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

Die **Win32 \_ ProcessStartup-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ ProcessStartup-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Createflags**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Prozess \| und Threadfunktionen \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwCreationFlags")
</dt> </dl>

Zusätzliche Werte, die die Prioritätsklasse und die Erstellung des Prozesses steuern. Die folgenden Erstellungswerte können in beliebiger Kombination angegeben werden, mit Ausnahme der angegebenen.

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Debuggen \_ Prozess** (1)


</dt> <dd>

Wenn dieses Flag festgelegt ist, wird der aufrufende Prozess als Debugger behandelt, und der neue Prozess wird gedebuggt. Das System benachrichtigt den Debugger über alle Debugereignisse, die während des Debugvorgangs auftreten.

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Debuggen \_ Nur \_ dieser \_ Prozess** (2)


</dt> <dd>

Wenn dieses Flag nicht festgelegt ist und der aufrufende Prozess gedebuggt wird, wird der neue Prozess zu einem anderen Prozess, der gedebuggt wird. Wenn der aufrufende Prozess kein Debugvorgang ist, treten keine debugbezogenen Aktionen auf.

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Erstellen \_ Angehalten** (4)


</dt> <dd>

Der primäre Thread des neuen Prozesses wird in einem angehaltenen Zustand erstellt und erst ausgeführt, wenn die [**ResumeThread-Methode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) aufgerufen wird.

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Getrennt \_ Prozess** (8)


</dt> <dd>

Bei Konsolenprozessen hat der neue Prozess keinen Zugriff auf die Konsole des übergeordneten Prozesses. Dieses Flag kann nicht verwendet werden, wenn das Flag **\_ Neue \_ Konsole erstellen** festgelegt ist.

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Erstellen \_ Neue \_ Konsole** (16)


</dt> <dd>

Dieser neue Prozess verfügt über eine neue Konsole, anstatt die übergeordnete Konsole zu erben. Dieses Flag kann nicht mit dem **Flag Getrennter \_ Prozess** verwendet werden.

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Erstellen \_ Neue \_ \_ Prozessgruppe** (512)


</dt> <dd>

Dieser neue Prozess ist der Stammprozess einer neuen Prozessgruppe. Die Prozessgruppe enthält alle Prozesse, die Nachfolger dieses Stammprozesses sind. Der Prozessbezeichner der neuen Prozessgruppe entspricht dem Prozessbezeichner, der in der **ProcessID-Eigenschaft** der [**Win32 \_ Process-Klasse**](win32-process.md) zurückgegeben wird. Prozessgruppen werden von der [**GenerateConsoleCtrlEvent-Methode**](/windows/console/generateconsolectrlevent) verwendet, um das Senden eines STRG+C-Signals oder eines STRG+BREAK-Signals an eine Gruppe von Konsolenprozessen zu ermöglichen.

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Erstellen \_ \_Unicode-Umgebung** (1024)


</dt> <dd>

Die in der **EnvironmentVariables-Eigenschaft aufgeführten Umgebungseinstellungen** verwenden Unicode-Zeichen. Wenn dieses Flag nicht festgelegt ist, verwendet der Umgebungsblock ANSI-Zeichen.

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Erstellen \_ \_ \_ Standardfehlermodus** (67108864)


</dt> <dd>

Neu erstellte Prozesse erhalten den Standardfehlermodus des Systems des aufrufenden Prozesses, anstatt den Fehlermodus des übergeordneten Prozesses zu erben. Dieses Flag ist nützlich für Multithread-Shellanwendungen, die mit deaktivierten hard errors ausgeführt werden.

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**CREATE \_ BREAKAWAY \_ FROM \_ JOB** (16777216)


</dt> <dd>

Wird verwendet, damit der erstellte Prozess nicht durch das Auftragsobjekt beschränkt wird.

</dd> </dl>

</dd> <dt>

**EnvironmentVariables**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ CURRENT USER \_ \\ \\ Environment")
</dt> </dl>

Liste der Einstellungen für die Konfiguration eines Computers. Umgebungsvariablen geben Suchpfade für Dateien, Verzeichnisse für temporäre Dateien, anwendungsspezifische Optionen und andere ähnliche Informationen an. Das System verwaltet einen Block von Umgebungseinstellungen für jeden Benutzer und einen für den Computer. Der Systemumgebungsblock stellt Umgebungsvariablen für alle Benutzer eines bestimmten Computers dar. Der Umgebungsblock eines Benutzers stellt die Umgebungsvariablen dar, die das System für einen bestimmten Benutzer verwaltet, und enthält den Satz von Systemumgebungsvariablen. Standardmäßig erhält jeder Prozess eine Kopie des Umgebungsblocks für seinen übergeordneten Prozess. In der Regel ist dies der Umgebungsblock für den angemeldeten Benutzer. Ein Prozess kann verschiedene Umgebungsblöcke für seine untergeordneten Prozesse angeben.

</dd> <dt>

**Errormode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Fehlerfunktionen \| \| SetErrorMode")
</dt> </dl>

Bei einigen Nicht-x86-Prozessoren verursachen falsch ausgerichtete Speicherverweise eine Ausrichtungsfehlerausnahme. Mit dem Flag **No \_ Alignment Fault \_ \_ Except** können Sie steuern, ob ein Betriebssystem solche Ausrichtungsfehler automatisch behebt oder für eine Anwendung sichtbar macht. Auf einer MIPS-Plattform (Millionen von Anweisungen pro Sekunde) muss eine Anwendung [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) explizit mit dem Flag **No Alignment Fault \_ \_ \_ Except** aufrufen, damit das Betriebssystem Ausrichtungsfehler automatisch beheben kann.

Wie ein Betriebssystem mehrere Arten von schwerwiegenden Fehlern verarbeitet. Sie können angeben, dass die Betriebssystem-Prozessfehler oder eine Anwendung Fehler empfangen und verarbeiten kann.

Die Standardeinstellung ist, dass das Betriebssystem Ausrichtungsfehler für eine Anwendung sichtbar macht. Da die x86-Plattform ausrichtungsfehler für eine Anwendung nicht sichtbar macht, führt das Flag **No \_ Alignment Fault \_ \_ Except** nicht dazu, dass das Betriebssystem einen Ausrichtungsfehler verursacht – auch wenn das Flag nicht festgelegt ist. Der Standardzustand für [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) besteht darin, alle Flags auf 0 (null) festzulegen.

<dt>



 (1)


</dt> <dd>

Standard

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Fehler \_ Kritische \_ Fehler** (2)


</dt> <dd>

Wenn dieses Flag festgelegt ist, zeigt das Betriebssystem das Meldungsfeld für kritische Fehlerhandler nicht an, wenn ein solcher Fehler auftritt. Stattdessen sendet das Betriebssystem den Fehler an den aufrufenden Prozess.

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**Nein \_ \_Ausrichtungsfehler \_ außer** (4)


</dt> <dd>

Wenn dieses Flag festgelegt ist, behebt das Betriebssystem automatisch Speicherausrichtungsfehler und macht sie für die Anwendung unsichtbar. Dies geschieht für die Aufruf- und Nachfolgerprozesse. Dieses Flag gilt nur für risc (Reduced Instruction Set Computing) und hat keine Auswirkungen auf x86-Prozessoren.

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**Nein \_ Fehlerfeld \_ "Gp" \_ \_** (8)


</dt> <dd>

Wenn dieses Flag festgelegt ist, zeigt das Betriebssystem das Fehlermeldungsfeld allgemeiner Schutz (GP) nicht an, wenn ein GP-Fehler auftritt. Dieses Flag sollte nur durch das Debuggen von Anwendungen festgelegt werden, die GP-Fehler behandeln.

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**Nein \_ \_ \_ \_ Dateifehlerfeld öffnen** (16)


</dt> <dd>

Wenn dieses Flag festgelegt ist, zeigt das Betriebssystem kein Meldungsfeld an, wenn keine Datei gefunden wird. Stattdessen wird der Fehler an den aufrufenden Prozess zurückgegeben. Dieses Flag wird derzeit ignoriert.

</dd> </dl>

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Prozess- \| und Threadstrukturen \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwFillAttribute")
</dt> </dl>

Die Text- und Hintergrundfarben, wenn ein neues Konsolenfenster in einer Konsolenanwendung erstellt wird. Diese Werte werden in Gui-Anwendungen (Graphical User Interface, grafische Benutzeroberfläche) ignoriert. Fügen Sie die Werte zusammen hinzu, um sowohl Vordergrund- als auch Hintergrundfarben anzugeben. Um beispielsweise den roten Typ (4) auf einem blauen Hintergrund (16) zu verwenden, legen Sie FillAttribute auf 20 fest.

<dt>

1
</dt> <dd>

\_Vordergrundblau

</dd> <dt>

2
</dt> <dd>

\_Vordergrundgrün

</dd> <dt>

4
</dt> <dd>

\_Vordergrundrot

</dd> <dt>

8
</dt> <dd>

\_Vordergrund-Intensität

</dd> <dt>

16
</dt> <dd>

\_Hintergrundblau

</dd> <dt>

32
</dt> <dd>

\_Hintergrundgrün

</dd> <dt>

64
</dt> <dd>

Hintergrund \_ rot

</dd> <dt>

128
</dt> <dd>

\_Hintergrundstärke

</dd> </dl>

</dd> <dt>

**Priorityclass**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**JOBOBJECT BASIC LIMIT \_ \_ \_ INFORMATION**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass")
</dt> </dl>

Prioritätsklasse des neuen Prozesses. Verwenden Sie diese Eigenschaft, um die Zeitplanprioritäten der Threads im Prozess zu bestimmen. Wenn die Eigenschaft NULL bleibt, wird die Prioritätsklasse standardmäßig auf Normal festgelegt, es sei denn, die Prioritätsklasse des Erstellungsprozesses ist Leerlauf oder Unter \_ normal. In diesen Fällen empfängt der untergeordnete Prozess die Standardprioritätsklasse des aufrufenden Prozesses.

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)


</dt> <dd>

Gibt einen normalen Prozess ohne spezielle Zeitplananforderungen an.

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Leerlauf** (64)


</dt> <dd>

Gibt einen Prozess mit Threads an, die nur ausgeführt werden, wenn sich das System im Leerlauf befindet und von den Threads eines Prozesses, der in einer Klasse mit höherer Priorität ausgeführt wird, nicht mehr verwendet wird. Ein Beispiel ist ein Bildschirmschoner. Die Prioritätsklasse im Leerlauf wird von untergeordneten Prozessen geerbt.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Hoch** (128)


</dt> <dd>

Gibt einen Prozess an, der zeitkritische Aufgaben ausführt, die sofort ausgeführt werden müssen, um ordnungsgemäß ausgeführt zu werden. Die Threads eines Klassenprozesses mit hoher Priorität leeren die Threads von Klassenprozessen mit normaler Priorität oder Leerlaufpriorität. Ein Beispiel ist Windows Aufgabenliste, das unabhängig von der Auslastung des Betriebssystems schnell reagieren muss, wenn er vom Benutzer aufgerufen wird. Verwenden Sie die Klasse mit hoher Priorität mit äußerster Sorgfalt, da eine CPU-gebundene Anwendung mit hoher Priorität nahezu alle verfügbaren Zyklen verwenden kann. Nur eine Echtzeitpriorität verdrängt Threads, die auf diese Ebene festgelegt sind.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)


</dt> <dd>

Gibt einen Prozess mit der höchsten möglichen Priorität an. Die Threads eines Echtzeit-Prioritätsklassenprozesses verdrängen die Threads aller anderen Prozesse– einschließlich Threads mit hoher Priorität und Betriebssystemprozesse, die wichtige Aufgaben ausführen. Beispielsweise kann ein Echtzeitprozess, der länger als ein sehr kurzes Intervall ausgeführt wird, dazu führen, dass Datenträgercaches nicht geleert werden oder dass eine Maus nicht reagiert.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Weiter unten \_ Normal** (16384)


</dt> <dd>

Gibt einen Prozess mit einer Priorität an, die höher ist als Leerlauf, aber niedriger als Normal.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Oben \_ Normal** (32768)


</dt> <dd>

Gibt einen Prozess mit einer Priorität an, die höher als Normal, aber niedriger als Hoch ist.

</dd> </dl>

</dd> <dt>

**ShowWindow**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow")
</dt> </dl>

Anzeige des Fensters für den Benutzer. Dies kann einer der Werte sein, die im *nCmdShow-Parameter* für die [ShowWindow-Funktion angegeben werden](/windows/desktop/api/winuser/nf-winuser-showwindow) können.

</dd> <dt>

**Titel**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpTitle")
</dt> </dl>

Text, der in der Titelleiste angezeigt wird, wenn ein neues Konsolenfenster erstellt wird. wird für Konsolenprozesse verwendet. Bei **NULL** wird der Name der ausführbaren Datei als Fenstertitel verwendet. Diese Eigenschaft muss NULL für **GUI-** oder Konsolenprozesse sein, die kein neues Konsolenfenster erstellen.

</dd> <dt>

**WinstationDesktop**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpDesktop")
</dt> </dl>

Der Name des Desktops oder der Name der Desktop- und Fensterstation für den Prozess. Ein schräger Schrägstrich in der Zeichenfolge gibt an, dass die Zeichenfolge sowohl Desktop- als auch Fensterstationsnamen enthält. Wenn **WinstationDesktop** **NULL ist,** erbt der neue Prozess die Desktop- und Fensterstation des übergeordneten Prozesses. Wenn **WinstationDesktop** eine leere Zeichenfolge ist, erbt der Prozess nicht die Desktop- und Fensterstation des übergeordneten Prozesses. Das System bestimmt, ob eine neue Desktop- und Fensterstation erstellt werden muss. Eine Fensterstation ist ein sicheres Objekt, das eine Zwischenablage, einen Satz globaler Atome und eine Gruppe von Desktopobjekten enthält. Die interaktive Fensterstation, die der Anmeldesitzung des interaktiven Benutzers zugewiesen ist, enthält auch die Tastatur, die Maus und das Anzeigegerät. Ein Desktop ist ein sicheres Objekt, das in einer Fensterstation enthalten ist. Ein Desktop verfügt über eine logische Anzeigeoberfläche und enthält Fenster, Menüs und Hooks. Eine Fensterstation kann mehrere Desktops haben. Nur die Desktops der interaktiven Fensterstation können sichtbar sein und Benutzereingaben empfangen.

</dd> <dt>

**X**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwX")
</dt> </dl>

Der X-Offset der oberen linken Ecke eines Fensters, wenn ein neues Fenster erstellt wird – in Pixel. Die Offsets befinden sich in der oberen linken Ecke des Bildschirms. Bei GUI-Prozessen wird die angegebene Position verwendet, wenn der neue Prozess [**createWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) zum ersten Mal aufruft, um ein überlappende Fenster zu erstellen, wenn der *X-Parameter* von **CreateWindow** **CW \_ USEDEFAULT ist.**

> \[! Hinweis X\]  
> und **Y** können nicht unabhängig angegeben werden.

 

</dd> <dt>

**XCountChars**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| XCountChars")
</dt> </dl>

Bildschirmpufferbreite in Zeichenspalten. Diese Eigenschaft wird für Prozesse verwendet, die ein Konsolenfenster erstellen, und wird in GUI-Prozessen ignoriert.

> [!Note]  
> **XCountChars** und **YCountChars können** nicht unabhängig angegeben werden.

 

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwXSize")
</dt> </dl>

Pixelbreite eines Fensters, wenn ein neues Fenster erstellt wird. Bei GUI-Prozessen wird dies nur verwendet, wenn der neue Prozess [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) zum ersten Mal aufruft, um ein überlappende Fenster zu erstellen, wenn der nWidth-Parameter von **CreateWindow** **CW \_ USEDEFAULT ist.**

> [!Note]  
> **XSize** und **YSize** können nicht unabhängig angegeben werden.

 

</dd> <dt>

**J**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwY")
</dt> </dl>

Pixeloffset der oberen linken Ecke eines Fensters, wenn ein neues Fenster erstellt wird. Die Offsets befinden sich in der oberen linken Ecke des Bildschirms. Bei GUI-Prozessen wird die angegebene Position verwendet, wenn der neue Prozess [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) zum ersten Mal aufruft, um ein überlappende Fenster zu erstellen, wenn der *y-Parameter* von **CreateWindow** **CW \_ USEDEFAULT ist.**

> \[! Hinweis X\]  
> und **Y** können nicht unabhängig angegeben werden.

 

</dd> <dt>

**YCountChars**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Prozess \| und Threadstrukturen \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| YCountChars")
</dt> </dl>

Bildschirmpufferhöhe in Zeichenzeilen. Diese Eigenschaft wird für Prozesse verwendet, die ein Konsolenfenster erstellen, aber in GUI-Prozessen ignoriert werden.

> [!Note]  
> **XCountChars** und **YCountChars** können nicht unabhängig angegeben werden.

 

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Prozess- \| und Threadstrukturen \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwYSize")
</dt> </dl>

Pixelhöhe eines Fensters, wenn ein neues Fenster erstellt wird. Bei GUI-Prozessen wird dies nur verwendet, wenn der neue Prozess [**createWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) zum ersten Mal aufruft, um ein überlappendes Fenster zu erstellen, wenn der *nWidth-Parameter* von **CreateWindow** **CW \_ USEDEFAULT** ist.

> [!Note]  
> **XSize** und **YSize** können nicht unabhängig angegeben werden.

 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Klasse wird von [**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md)abgeleitet.

Übersicht

Mit der [**Win32 \_ Process**](win32-process.md) [**Create-Methode**](create-method-in-class-win32-process.md) können Sie Startoptionen für jeden neuen Prozess konfigurieren, der auf einem Computer ausgeführt wird. Beispielsweise können Sie einen Prozess so konfigurieren, dass er in einem "ausgeblendeten" Fenster gestartet wird, wodurch verhindert wird, dass ein Benutzer ihn sieht und möglicherweise unterbricht. Wenn der Prozess in einem Befehlsfenster ausgeführt wird, können Sie die Größe, den Titel sowie die Vordergrund- und Hintergrundfarben des Fensters konfigurieren.

Startoptionen werden mit der **Win32 \_ ProcessStartup-Klasse** konfiguriert. **Win32 \_ ProcessStartup** ist eine Method Type-Klasse. Die Method Type-Klasse ist ausschließlich vorhanden, um Informationen an eine Methode zu übergeben. In diesem Fall werden alle Eigenschaften einer Instanz von **Win32 \_ ProcessStartup** an eine Instanz von [**Win32 \_ Process**](win32-process.md)übergeben.

**Verwenden von Win32 \_ ProcessStartup**

1.  Erstellen Sie eine Instanz von **Win32 \_ ProcessStartup**.
2.  Konfigurieren Sie die Eigenschaften der neuen Instanz.
3.  Schließen Sie die -Instanz als Teil der [**Win32 \_ Process Create-Methode**](win32-process.md) ein.

Wenn Sie beispielsweise eine **Win32 \_ ProcessStartup-Instanz** mit dem Namen objConfig erstellt haben, übergeben Sie den Objektnamen in der Create-Methode wie folgt:

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a>Beispiele

Sie können die **Win32 \_ ProcessStartup-Klasse** verwenden, um verschiedene Startoptionen für einen Prozess zu konfigurieren. Zu diesen Optionen zählen u. a. das Erstellen eines Prozesses in einem ausgeblendeten Fenster und das Erstellen eines Prozesses mit höherer Priorität. Der folgende VBScript-Code erstellt einen Prozess in einem ausgeblendeten Fenster.


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



Mit dem folgenden VBScript-Code wird ein Prozess mit höherer Priorität erstellt.


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



Im folgenden VBScript-Codebeispiel wird ein Editor Prozess auf dem lokalen Computer erstellt. **Win32 \_ ProcessStartup** wird verwendet, um die Prozesseinstellungen zu konfigurieren.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[**\_Win32-Prozess**](win32-process.md)
</dt> <dt>

[**\_\_ProviderHostQuotaConfiguration**](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[WMI-Aufgaben: Prozesse](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
