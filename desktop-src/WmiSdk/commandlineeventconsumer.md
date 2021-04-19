---
description: Die commandlineeventconsumer-Klasse startet einen beliebigen Prozess im lokalen System, wenn ein Ereignis an Sie übermittelt wird.
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: Commandlineeventconsumer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommandLineEventConsumer
- CommandLineEventConsumer.CreatorSID
- CommandLineEventConsumer.MachineName
- CommandLineEventConsumer.MaximumQueueSize
- CommandLineEventConsumer.CommandLineTemplate
- CommandLineEventConsumer.CreateNewConsole
- CommandLineEventConsumer.CreateNewProcessGroup
- CommandLineEventConsumer.CreateSeparateWowVdm
- CommandLineEventConsumer.CreateSharedWowVdm
- CommandLineEventConsumer.DesktopName
- CommandLineEventConsumer.ExecutablePath
- CommandLineEventConsumer.FillAttributes
- CommandLineEventConsumer.ForceOffFeedback
- CommandLineEventConsumer.ForceOnFeedback
- CommandLineEventConsumer.KillTimeout
- CommandLineEventConsumer.Name
- CommandLineEventConsumer.Priority
- CommandLineEventConsumer.RunInteractively
- CommandLineEventConsumer.ShowWindowCommand
- CommandLineEventConsumer.UseDefaultErrorMode
- CommandLineEventConsumer.WindowTitle
- CommandLineEventConsumer.WorkingDirectory
- CommandLineEventConsumer.XCoordinate
- CommandLineEventConsumer.XNumCharacters
- CommandLineEventConsumer.XSize
- CommandLineEventConsumer.YCoordinate
- CommandLineEventConsumer.YNumCharacters
- CommandLineEventConsumer.YSize
- CommandLineEventConsumer.FillAttribute
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 1784ba116417f6ed94aed2249a797cf8de4b3527
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106372552"
---
# <a name="commandlineeventconsumer-class"></a>Commandlineeventconsumer-Klasse

Die **commandlineeventconsumer** -Klasse startet einen beliebigen Prozess im lokalen System, wenn ein Ereignis an Sie übermittelt wird. Diese Klasse ist einer der standardereignisconsumer, die von WMI bereitstellt werden. Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

> [!Note]  
> Wenn Sie die **commandlineeventconsumer** -Klasse verwenden, sichern Sie die ausführbare Datei, die Sie starten möchten. Wenn sich die ausführbare Datei nicht an einem sicheren Speicherort befindet oder durch eine sichere Zugriffs Steuerungs Liste (ACL) geschützt ist, kann ein nicht autorisierter Benutzer die ausführbare Datei durch eine böswillige ausführbare Datei ersetzen. Weitere Informationen zu ACLs finden Sie im Abschnitt "Sicherheit" des Microsoft Windows Software Development Kit (SDK) und unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class CommandLineEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  CommandLineTemplate;
  boolean CreateNewConsole = False;
  boolean CreateNewProcessGroup = True;
  boolean CreateSeparateWowVdm = False;
  boolean CreateSharedWowVdm = False;
  string  DesktopName;
  string  ExecutablePath;
  uint32  FillAttributes;
  boolean ForceOffFeedback = False;
  boolean ForceOnFeedback = False;
  uint32  KillTimeout = 0;
  string  Name;
  sint32  Priority = 0x20;
  boolean RunInteractively = False;
  uint32  ShowWindowCommand;
  boolean UseDefaultErrorMode = False;
  string  WindowTitle;
  string  WorkingDirectory;
  uint32  XCoordinate;
  uint32  XNumCharacters;
  uint32  XSize;
  uint32  YCoordinate;
  uint32  YNumCharacters;
  uint32  YSize;
  uint32  FillAttribute;
};
```

## <a name="members"></a>Member

Die **commandlineeventconsumer** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **commandlineeventconsumer** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Commandlinetemplate**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Standard Zeichen folgen Vorlage, die den zu startenden Prozess angibt. Diese Eigenschaft kann **null** sein, und die **ExecutablePath** -Eigenschaft wird als Befehlszeile verwendet.

</dd> <dt>

**"Kreatenewconsole"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Wenn dieser Eigenschaft ein Wert zugewiesen wird, wird eine Ablauf Verfolgungs Meldung generiert. Weitere Informationen finden Sie unter Ablauf [Verfolgung von WMI-Aktivitäten](tracing-wmi-activity.md).

</dd> <dt>

**"Kreatenewprocessgroup"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der neue Prozess der Stamm Prozess einer neuen Prozessgruppe ist. Die Prozessgruppe umfasst alle Prozesse, bei denen es sich um nachfolgende Elemente dieses Stamm Prozesses handelt. Der Prozess Bezeichner der neuen Prozessgruppe ist mit diesem Prozess Bezeichner identisch. Prozessgruppen werden von der [**generateconsolectrlevent**](/windows/console/generateconsolectrlevent) -Methode verwendet, um das Senden eines STRG + C-oder STRG + Break-Signals an eine Gruppe von Konsolen Prozessen zu aktivieren.

</dd> <dt>

**"Kreateseparser"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der neue Prozess in einem privaten virtuellen DOS-Computer (VDM) ausgeführt wird. Dies ist nur gültig, wenn eine Anwendung gestartet wird, die auf einem 16-Bit-Windows-Betriebssystem ausgeführt wird. Wenn **false** festgelegt ist, werden alle Anwendungen, die auf einem 16-Bit-Windows-Betriebssystem ausgeführt werden, als Threads in einem einzelnen, freigegebenen VDM ausgeführt. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.

</dd> <dt>

**"Kreatesharedwowvdm"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass die Methode " [**kreateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " den neuen Prozess auf dem freigegebenen virtuellen DOS-Computer (VDM) ausführt. Diese Eigenschaft kann den Schalter defaultseparatevdm im Windows-Abschnitt von Win.ini überschreiben, wenn der Wert auf **true** festgelegt ist. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.

</dd> <dt>

**"Kreatorsid"**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Sicherheits-ID (SID), die den Benutzer, der einen Filter erstellt, eindeutig identifiziert. WMI speichert die SID des Benutzers, der eine Instanz von [**\_ \_ eventconsumer**](--eventconsumer.md) oder die Administrator-SID erstellt, je nach Betriebssystem. Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**Desktopname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Wenn dieser Eigenschaft ein Wert zugewiesen wird, wird eine Ablauf Verfolgungs Meldung generiert. Weitere Informationen finden Sie unter Ablauf [Verfolgung von WMI-Aktivitäten](tracing-wmi-activity.md).

</dd> <dt>

**ExecutablePath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Auszuführenden Modul. Die Zeichenfolge kann den vollständigen Pfad und den Dateinamen des auszuführenden Moduls angeben, oder es kann ein partieller Name angegeben werden. Wenn ein partieller Name angegeben ist, wird das aktuelle Laufwerk und das aktuelle Verzeichnis angenommen.

Die **ExecutablePath** -Eigenschaft kann **null** sein. In diesem Fall muss der Modulname das erste durch Leerzeichen getrennte Token im **commandlinetemplate** -Eigenschafts Wert sein. Wenn Sie einen langen Dateinamen verwenden, der ein Leerzeichen enthält, verwenden Sie Zeichen folgen in Anführungszeichen, um anzugeben, wo der Dateiname endet und die Argumente beginnen, den Dateinamen zu verdeutlichen

> [!Note]  
> Da die **commandlinetemplate** -Eigenschaft eine Vorlage sein kann, in der das auszuführende Modul von einer Variablen bereitgestellt wird, ermöglicht eine **ExecutablePath** -Eigenschaft von **null** , dass das im-Parameter angegebene Modul ausgeführt wird. Legen Sie die **ExecutablePath** -Eigenschaft in der **commandlineeventconsumer** -Registrierung immer auf die erforderliche ausführbare Datei fest, wodurch das Überschreiben von Ereignis Parametern vermieden wird. Wenn Sie eine Vorlage und eine Variable verwenden müssen, um das auszuführende Modul anzugeben, achten Sie darauf, wem das vollständige Schreib Privileg im-Namespace erteilt wird.

 

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Anfangstext-und Hintergrundfarben an, wenn ein neues Konsolenfenster in einer Konsolenanwendung erstellt wird.

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Anfängliche Text-und Hintergrundfarben, wenn ein neues Konsolenfenster in einer Konsolenanwendung erstellt wird. Diese Eigenschaft wird in einer GUI-Anwendung ignoriert. Der Wert kann eine beliebige Kombination der folgenden Werte sein.

<dt>

1 (0x1)
</dt> <dd>

Blauer Vordergrund

</dd> <dt>

2 (0x2)
</dt> <dd>

grüner Vordergrund

</dd> <dt>

4 (0x4)
</dt> <dd>

Roter Vordergrund

</dd> <dt>

8 (0x8)
</dt> <dd>

Vordergrund Intensität

</dd> <dt>

16 (0x10)
</dt> <dd>

Blauer Hintergrund

</dd> <dt>

32 (0x20)
</dt> <dd>

Grüner Hintergrund

</dd> <dt>

64 (0x40)
</dt> <dd>

Roter Hintergrund

</dd> <dt>

128 (0x80)
</dt> <dd>

Hintergrund Intensität

</dd> </dl>

Beispielsweise wird in den folgenden Kombinationen roter Text auf einem weißen Hintergrund erzeugt:


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  oder  


```mof
0x74
```



</dd> <dt>

**Forceofffeedback**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der Feedback Cursor beim Start des Prozesses erzwungen wird. Der normale Cursor wird angezeigt.

</dd> <dt>

**Forceonfeedback**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass sich der Cursor zwei Sekunden nach dem Aufruf von " [**kreateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " im Feedback Modus befindet. Wenn während dieser zwei Sekunden der Prozess den ersten GUI-Befehl aufruft, gibt das System fünf weitere Sekunden an den Prozess. In diesen fünf Sekunden gibt das System, wenn der Prozess ein Fenster anzeigt, weitere fünf Sekunden an den Prozess, um das Zeichnen des Fensters abzuschließen.

</dd> <dt>

**Killtimeout**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl (in Sekunden), die der WMI-Dienst wartet, bevor er einen Prozess 0 (null) beendet, gibt an, dass ein Prozess nicht abgebrochen werden soll. Durch das Abbrechen eines Prozesses wird verhindert, dass ein Prozess unbegrenzt ausgeführt wird.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, an den Windows-Verwaltungsinstrumentation (WMI) Ereignisse sendet.

Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Warteschlange für einen bestimmten Consumer in Bytes.

Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](key-qualifier.md)
</dt> </dl>

Der eindeutige Name eines Consumers.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Planen der Prioritätsstufe der Prozessthreads. In der folgenden Liste sind die verfügbaren Prioritätsstufen aufgeführt.

<dt>

32 (0x20)
</dt> <dd>

Gibt einen normalen Prozess ohne Planungsanforderungen an.

</dd> <dt>

64 (0x40)
</dt> <dd>

Gibt einen Prozess an, dessen Threads nur ausgeführt werden, wenn sich das System im Leerlauf befindet. Sie werden von den Threads eines Prozesses, der in einer höheren Prioritäts Klasse ausgeführt wird, vorzeitig entfernt. Ein Beispiel hierfür ist ein Bildschirmschoner. Die inaktive Prioritäts Klasse wird von untergeordneten Prozessen geerbt.

</dd> <dt>

128 (0x80)
</dt> <dd>

Gibt einen Prozess an, der zeitkritische Aufgaben mit hoher Priorität ausführt. In den Threads eines Klassen Prozesses mit hoher Priorität werden die Threads von Klassen Prozessen mit normaler Priorität oder der Leerlauf Priorität vorzeitig entfernt. Ein Beispiel hierfür ist die Aufgabenliste, die schnell reagieren muss, wenn der Benutzer unabhängig von der System Auslastung aufgerufen wird. Verwenden Sie extrem Sorgfalt bei der Verwendung der Klasse mit hoher Priorität, da eine CPU-gebundene Anwendung mit einer Klasse mit hoher Priorität fast alle verfügbaren Zyklen verwenden kann.

</dd> <dt>

256 (0x100)
</dt> <dd>

Gibt einen Prozess an, der über die höchste mögliche Priorität verfügt. Die Threads eines Echtzeit-Prioritäts Klassen Prozesses haben Vorrang vor den Threads aller anderen Prozesse, einschließlich der Betriebssystem Prozesse, von denen wichtige Aufgaben ausgeführt werden. Beispielsweise kann ein echt Zeit Prozess, der für mehr als ein kurzes Intervall ausgeführt wird, dazu führen, dass Datenträger Caches nicht geleert werden oder die Maus nicht reagiert.

</dd> </dl>

</dd> <dt>

**Runinteraktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der Prozess in der interaktiven WinStation gestartet wird. Wenn der Wert **false** ist, wird der Prozess in der standardmäßigen Dienst-WinStation gestartet. Diese Eigenschaft überschreibt die **Desktopname** -Eigenschaft. Diese Eigenschaft wird nur lokal und nur dann verwendet, wenn es sich bei dem interaktiven Benutzer um denselben Benutzer handelt, der den Consumer eingerichtet hat.

Ab Windows Vista wird der Prozess, der die **commandlineeventconsumer** -Instanz ausgeführt wird, unter dem Konto " **LocalSystem** " gestartet und befindet sich in Sitzung 0. Dienste, die in Sitzung 0 ausgeführt werden, können nicht mit Benutzersitzungen interagieren.

</dd> <dt>

**Showwindowcommand**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Fenster Anzeige Zustand. Dabei kann es sich um einen beliebigen Wert handeln, der im *nCmdShow* -Parameter für die [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) -Funktion angegeben werden kann.

</dd> <dt>

**Usedefaulterrormode**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der Standardfehler Modus verwendet wird.

</dd> <dt>

**WindowTitle**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Titel, der in der Titelleiste des Prozesses angezeigt wird. Diese Eigenschaft wird für GUI-Anwendungen ignoriert.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Arbeitsverzeichnis für diesen Prozess.

</dd> <dt>

**Xkoordinate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

X-Offset in Pixel vom linken Rand des Bildschirms bis zum linken Rand des Fensters, wenn ein neues Fenster erstellt wird.

</dd> <dt>

**Xnumcharacter**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bildschirm Puffer Breite (in Zeichen Spalten), wenn ein neues Konsolenfenster erstellt wird. Diese Eigenschaft wird in einem GUI-Prozess ignoriert.

</dd> <dt>

**Xsize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Breite eines neuen Fensters in Pixel, wenn ein neues Fenster erstellt wird.

</dd> <dt>

**Ykoordinate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Y-Offset (in Pixel) vom oberen Rand des Bildschirms bis zum oberen Rand des Fensters, wenn ein neues Fenster erstellt wird.

</dd> <dt>

**Ynumcharacters**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Höhe des Bildschirm Puffers in Zeichen Zeilen, wenn ein neues Konsolenfenster erstellt wird. Diese Eigenschaft wird in einem GUI-Prozess ignoriert.

</dd> <dt>

**Ysize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Höhe des neuen Fensters in Pixel, wenn ein neues Fenster erstellt wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **commandlineeventconsumer** -Klasse wird von der [**\_ \_ eventconsumer**](--eventconsumer.md) abstract-Klasse abgeleitet.

Die Eigenschaft " **kreateseparametewowvdm** " gibt an, ob der neue Prozess in einem privaten virtuellen DOS-Computer (VDM) ausgeführt wird. Der Vorteil der separaten Ausführung besteht darin, dass ein Absturz nur den einzelnen VDM beendet. Programme, die auf unterschiedlichen VDMs ausgeführt werden, funktionieren weiterhin normal, und die 16-Bit-Windows-basierten Anwendungen, die in separaten VDMs ausgeführt werden, haben separate Eingabe Warteschlangen Dies bedeutet, dass die Anwendungen in separaten VDMs weiterhin Eingaben empfangen, wenn eine Anwendung nicht mehr reagiert. Der Nachteil der separaten Ausführung besteht darin, dass es erheblich mehr Arbeitsspeicher benötigt. Legen Sie diese Eigenschaft nur dann auf **true** fest, wenn der Benutzer anfordert, dass 16-Bit-Windows-basierte Anwendungen in Ihrem eigenen VDM ausgeführt werden.

> [!Note]  
> **Commandlineeventconsumer** verwendet intern die Methode " [**kreateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " und übergibt die Eigenschaften **ExecutablePath** und **commandlinetemplate** als *lpApplicationName* -und *lpCommandLine* -Parameter. Im folgenden Managed Object Format (MOF)-Codebeispiel wird **commandlineeventconsumer** nicht ordnungsgemäß verwendet.

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



Die Methode " [**kreateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " übergibt *lpCommandLine* als `argv[0]` , `argv[1]` usw. Da `argv[0]` für 16-Bit-Anwendungen, die für den Namen der ausführbaren Datei reserviert sind, der vorherige MOF-Code dazu führt, dass der Prozess erstellt wird, als ob der folgende Befehl an der Eingabeaufforderung eingegeben wird: **c: \\ Windows \\ system32 \\cscript.exe param1 Param2**.

Der vorherige Befehl ist nicht erfolgreich, da sich Cscript.exe nicht untersucht `argv[0]` und somit nicht erkennt, dass er keinen eigenen Namen, sondern etwas anderes ("c: \\ \\ Scripts \\ \\MyScript.js") enthält. Im folgenden Beispiel wird die empfohlene Verwendung von **commandlineeventconsumer** identifiziert.


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



Die vorherige Verwendung von **commandlineeventconsumer** führt dazu, dass der Prozess erstellt wird, als ob der folgende Befehl an der Eingabeaufforderung eingegeben wurde: **c: \\ Windows \\ system32 \\cscript.exe c: \\ Scripts \\MyScript.js param1 Param2**

Da "c: \\ \\ Scripts \\ \\MyScript.js" jetzt ist `argv[1]` , wird es von Cscript.exe erkannt, und der Befehl wird erfolgreich ausgeführt.

Weitere Informationen finden Sie unter der Funktion "up- [**Process**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) ".

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung von **commandlineeventconsumer** , um einen Consumer zu erstellen, finden Sie unter [Ausführen eines Programms in der Befehlszeile auf der Grundlage eines Ereignisses](running-a-program-from-the-command-line-based-on-an-event.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Stamm \\ Abonnement<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Standard Consumer-Klassen](standard-consumer-classes.md)
</dt> <dt>

[Überwachen von und reagieren auf Ereignisse mit Standard Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Erstellen eines logischen Consumers](creating-a-logical-consumer.md)
</dt> <dt>

[Empfangen von Ereignissen zu allen Zeitpunkten](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_Eventconsumer**](--eventconsumer.md)
</dt> </dl>

 

