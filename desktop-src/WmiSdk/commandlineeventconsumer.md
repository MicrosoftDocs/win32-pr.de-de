---
description: Die CommandLineEventConsumer-Klasse startet einen beliebigen Prozess im lokalen System, wenn ein Ereignis an das System übermittelt wird.
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: CommandLineEventConsumer-Klasse
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
ms.openlocfilehash: dce5100ba83a04ef2f6252421ec49068e84730141830e7b01f177c81bbac21b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319589"
---
# <a name="commandlineeventconsumer-class"></a>CommandLineEventConsumer-Klasse

Die **CommandLineEventConsumer-Klasse** startet einen beliebigen Prozess im lokalen System, wenn ein Ereignis an das System übermittelt wird. Diese Klasse ist einer der Standardereignis-Consumer, die WMI bereitstellt. Weitere Informationen finden Sie unter [Überwachen und Reagieren auf Ereignisse mit Standard-Consumern.](monitoring-and-responding-to-events-with-standard-consumers.md)

> [!Note]  
> Wenn Sie die **CommandLineEventConsumer-Klasse** verwenden, sichern Sie die ausführbare Datei, die Sie starten möchten. Wenn sich die ausführbare Datei nicht an einem sicheren Speicherort oder mit einer Starken Zugriffssteuerungsliste (Strong Access Control List, ACL) befindet, kann ein nicht autorisierter Benutzer Ihre ausführbare Datei durch eine schädliche ausführbare Datei ersetzen. Weitere Informationen zu ACLs finden Sie im Abschnitt Sicherheit des Microsoft Windows Software Development Kit (SDK) und unter [Erstellen eines Sicherheitsdeskriptors für ein neues Objekt.](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)

 

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

Die **CommandLineEventConsumer-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CommandLineEventConsumer-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CommandLineTemplate**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Standardzeichenfolgenvorlage, die den zu startden Prozess angibt. Diese Eigenschaft kann **NULL** sein, und die **ExecutablePath-Eigenschaft** wird als Befehlszeile verwendet.

</dd> <dt>

**CreateNewConsole**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird nicht verwendet. Wenn dieser Eigenschaft ein Wert zugewiesen wird, wird eine Ablaufverfolgungsmeldung generiert. Weitere Informationen finden Sie unter [Ablaufverfolgung der WMI-Aktivität](tracing-wmi-activity.md).

</dd> <dt>

**CreateNewProcessGroup**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der neue Prozess der Stammprozess einer neuen Prozessgruppe ist. Die Prozessgruppe enthält alle Prozesse, die Nachfolger dieses Stammprozesses sind. Der Prozessbezeichner der neuen Prozessgruppe entspricht diesem Prozessbezeichner. Prozessgruppen werden von der [**GenerateConsoleCtrlEvent-Methode**](/windows/console/generateconsolectrlevent) verwendet, um das Senden eines STRG+C- oder STRG+BREAK-Signals an eine Gruppe von Konsolenprozessen zu ermöglichen.

</dd> <dt>

**CreateSeparateWowVdm**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der neue Prozess auf einem privaten virtuellen DOS-Computer (Virtual DOS Machine, VDM) ausgeführt wird. Dies ist nur gültig, wenn eine Anwendung gestartet wird, die auf einem 16-Bit-Windows Betriebssystem ausgeführt wird. Wenn **false** festgelegt ist, werden alle Anwendungen, die auf einem 16-Bit-Windows Betriebssystem ausgeführt werden, als Threads in einem einzigen freigegebenen VDM ausgeführt. Weitere Informationen finden Sie im Abschnitt "Hinweise" dieses Themas.

</dd> <dt>

**CreateSharedWowVdm**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass die [**CreateProcess-Methode**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) den neuen Prozess auf dem freigegebenen virtuellen DOS-Computer (VDM) ausführt. Diese Eigenschaft kann den DefaultSeparateVDM-Switch im Windows Abschnitt von Win.ini überschreiben, wenn auf True festgelegt **ist.** Weitere Informationen finden Sie im Abschnitt "Hinweise" dieses Themas.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Sicherheits-ID (SID), die den Benutzer eindeutig identifiziert, der einen Filter erstellt. WMI speichert die SID des Benutzers, der je nach Betriebssystem eine Instanz von [**\_ \_ EventConsumer**](--eventconsumer.md) erstellt, oder die Administrator-SID. Weitere Informationen finden Sie unter [Binden eines Ereignisfilters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und Überwachen und Reagieren auf Ereignisse mit [Standard-Consumern.](monitoring-and-responding-to-events-with-standard-consumers.md)

Diese Eigenschaft wird von [**\_ \_ EventConsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**DesktopName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird nicht verwendet. Wenn dieser Eigenschaft ein Wert zugewiesen wird, wird eine Ablaufverfolgungsmeldung generiert. Weitere Informationen finden Sie unter [Ablaufverfolgung der WMI-Aktivität](tracing-wmi-activity.md).

</dd> <dt>

**ExecutablePath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Auszuführendes Modul. Die Zeichenfolge kann den vollständigen Pfad und Dateinamen des auszuführende Moduls oder einen partiellen Namen angeben. Wenn ein Teilname angegeben wird, werden das aktuelle Laufwerk und das aktuelle Verzeichnis angenommen.

Die **ExecutablePath-Eigenschaft** kann **NULL** sein. In diesem Fall muss der Modulname das erste durch Leerzeichen getrennte Token im **CommandLineTemplate-Eigenschaftswert** sein. Wenn Sie einen langen Dateinamen verwenden, der ein Leerzeichen enthält, verwenden Sie Zeichenfolgen in Anführungszeichen, um anzugeben, wo der Dateiname endet, und die Argumente beginnen, den Dateinamen zu verdeutlichen.

> [!Note]  
> Da die **CommandLineTemplate-Eigenschaft** eine Vorlage sein kann, in der das auszuführende Modul von einer Variablen bereitgestellt wird, lässt eine **NULL** **ExecutablePath-Eigenschaft** die Ausführung des im -Parameter angegebenen Moduls zu und befindet sich dann außerhalb Ihrer Kontrolle. Legen Sie die **ExecutablePath-Eigenschaft** in der **CommandLineEventConsumer-Registrierung** immer so fest, dass sie die erforderliche ausführbare Datei enthält, wodurch das Überschreiben durch Ereignisparameter vermieden wird. Wenn Sie eine Vorlage und eine Variable verwenden müssen, um das auszuführende Modul anzugeben, achten Sie darauf, wem vollständige Schreibberechtigungen im Namespace gewährt werden.

 

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Anfangstext und die Hintergrundfarben an, wenn in einer Konsolenanwendung ein neues Konsolenfenster erstellt wird.

</dd> <dt>

**FillAttributes**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Anfangstext und Hintergrundfarben, wenn ein neues Konsolenfenster in einer Konsolenanwendung erstellt wird. Diese Eigenschaft wird in einer GUI-Anwendung ignoriert. Der Wert kann eine beliebige Kombination der folgenden Werte sein.

<dt>

1 (0x1)
</dt> <dd>

Blauer Vordergrund

</dd> <dt>

2 (0x2)
</dt> <dd>

Grüner Vordergrund

</dd> <dt>

4 (0x4)
</dt> <dd>

Roter Vordergrund

</dd> <dt>

8 (0x8)
</dt> <dd>

Vordergrundintensivität

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

Hintergrundintensivität

</dd> </dl>

Die folgenden Kombinationen erzeugen beispielsweise roten Text auf einem weißen Hintergrund:


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  oder  


```mof
0x74
```



</dd> <dt>

**ForceOffFeedback**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass der Feedbackcursor beim Starten des Prozesses deaktiviert wird. Der normale Cursor wird angezeigt.

</dd> <dt>

**ForceOnFeedback**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass sich der Cursor zwei Sekunden nach dem [**CreateProcess-Namen im Feedbackmodus**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) befindet. Wenn der Prozess während dieser zwei Sekunden den ersten GUI-Aufruf vorgibt, gibt das System fünf weitere Sekunden für den Prozess zurück. Wenn während dieser fünf Sekunden ein Fenster angezeigt wird, gibt das System dem Prozess weitere fünf Sekunden Zeit, um das Zeichnen des Fensters fertig zu stellen.

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zahl in Sekunden, die der WMI-Dienst wartet, bevor ein Prozess 0 (null) abgesetzt wird, gibt an, dass ein Prozess nicht abgesetzt werden soll. Durch das Ausführen eines Prozesses wird verhindert, dass ein Prozess unbegrenzt ausgeführt wird.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name des Computers, an den die Windows Management Instrumentation (WMI) Ereignisse sendet.

Diese Eigenschaft wird von [**\_ \_ EventConsumer geerbt.**](--eventconsumer.md)

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Warteschlange für einen bestimmten Consumer in Bytes.

Diese Eigenschaft wird von [**\_ \_ EventConsumer geerbt.**](--eventconsumer.md)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](key-qualifier.md)
</dt> </dl>

Eindeutiger Name eines Consumers.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Planen der Prioritätsebene der Prozessthreads. In der folgenden Liste sind die verfügbaren Prioritätsstufen aufgeführt.

<dt>

32 (0x20)
</dt> <dd>

Gibt einen normalen Prozess ohne Planungsanforderungen an.

</dd> <dt>

64 (0x40)
</dt> <dd>

Gibt einen Prozess an, dessen Threads nur ausgeführt werden, wenn sich das System im Leerlauf befindet, und von den Threads eines Prozesses, der in einer Klasse mit höherer Priorität ausgeführt wird, vorverlegt werden. Ein Beispiel ist ein Bildschirmschoner. Die Prioritätsklasse im Leerlauf wird von untergeordneten Prozessen geerbt.

</dd> <dt>

128 (0x80)
</dt> <dd>

Gibt einen Prozess an, der zeitkritische Tasks mit hoher Priorität ausführt. Die Threads eines Klassenprozesses mit hoher Priorität verdrängen die Threads von Klassenprozessen mit normaler Priorität oder Leerlaufpriorität. Ein Beispiel ist die Aufgabenliste, die unabhängig von der Auslastung des Systems schnell reagieren muss, wenn sie vom Benutzer aufgerufen wird. Verwenden Sie die Klasse mit hoher Priorität mit äußerster Sorgfalt, da eine CPU-gebundene Anwendung mit einer Klasse mit hoher Priorität nahezu alle verfügbaren Zyklen verwenden kann.

</dd> <dt>

256 (0x100)
</dt> <dd>

Gibt einen Prozess mit der höchsten möglichen Priorität an. Die Threads eines Echtzeitprioritätsklassenprozesses verdrängen die Threads aller anderen Prozesse, einschließlich Betriebssystemprozesse, die wichtige Aufgaben ausführen. Beispielsweise kann ein Echtzeitprozess, der länger als ein kurzes Intervall ausgeführt wird, dazu führen, dass Datenträgercaches nicht geleert werden oder dass die Maus nicht reagiert.

</dd> </dl>

</dd> <dt>

**RunInteractively**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass der Prozess in der interaktiven WinStation gestartet wird. False **gibt an,** dass der Prozess im WinStation-Standarddienst gestartet wird. Diese Eigenschaft überschreibt die **DesktopName-Eigenschaft.** Diese Eigenschaft wird nur lokal verwendet und nur, wenn der interaktive Benutzer derselbe Benutzer ist, der den Consumer eingerichtet hat.

Ab Windows Vista wird der Prozess zum Ausführen der **CommandLineEventConsumer-Instanz** unter dem **LocalSystem-Konto** gestartet und befindet sich in Sitzung 0. Dienste, die in Sitzung 0 ausgeführt werden, können nicht mit Benutzersitzungen interagieren.

</dd> <dt>

**ShowWindowCommand**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Status des Fensters wird angezeigt. Dies kann einer der Werte sein, die im *nCmdShow-Parameter* für die [ShowWindow-Funktion angegeben werden](/windows/desktop/api/winuser/nf-winuser-showwindow) können.

</dd> <dt>

**UseDefaultErrorMode**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass der Standardfehlermodus verwendet wird.

</dd> <dt>

**Windowtitle**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Titel, der auf der Titelleiste des Prozesses angezeigt wird. Diese Eigenschaft wird für GUI-Anwendungen ignoriert.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Arbeitsverzeichnis für diesen Prozess.

</dd> <dt>

**XCoordinate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

X-Offset in Pixel vom linken Rand des Bildschirms bis zum linken Rand des Fensters, wenn ein neues Fenster erstellt wird.

</dd> <dt>

**XNumCharacters**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bildschirmpufferbreite in Zeichenspalten, wenn ein neues Konsolenfenster erstellt wird. Diese Eigenschaft wird in einem GUI-Prozess ignoriert.

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Breite eines neuen Fensters in Pixel, wenn ein neues Fenster erstellt wird.

</dd> <dt>

**YCoordinate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Y-Offset in Pixel vom oberen Rand des Bildschirms bis zum oberen Rand des Fensters, wenn ein neues Fenster erstellt wird.

</dd> <dt>

**YNumCharacters**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bildschirmpufferhöhe in Zeichenzeilen, wenn ein neues Konsolenfenster erstellt wird. Diese Eigenschaft wird in einem GUI-Prozess ignoriert.

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Höhe des neuen Fensters in Pixel, wenn ein neues Fenster erstellt wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CommandLineEventConsumer-Klasse** wird von der [**\_ \_ abstrakten EventConsumer-Klasse**](--eventconsumer.md) abgeleitet.

Die **CreateSeparateWowVdm-Eigenschaft** gibt an, ob der neue Prozess auf einem privaten virtuellen DOS-Computer (Virtual DOS Machine, VDM) ausgeführt wird oder nicht. Der Vorteil der getrennten Ausführung besteht darin, dass ein Absturz nur das einzelne VDM beendet. Programme, die in unterschiedlichen VDMs ausgeführt werden, funktionieren weiterhin normal, und die 16-Bit-Windows-basierten Anwendungen, die in separaten VDMs ausgeführt werden, verfügen über separate Eingabewarteschlangen. Dies bedeutet, dass die Anwendungen in separaten VDMs weiterhin Eingaben erhalten, wenn eine Anwendung vorübergehend nicht mehr reagiert. Der Nachteil der getrennten Ausführung besteht darin, dass dafür deutlich mehr Arbeitsspeicher benötigt wird. Sie sollten diese Eigenschaft nur auf **True** festlegen, wenn der Benutzer anfordert, dass 16-Bit-Windows-basierten Anwendungen in ihrem eigenen VDM ausgeführt werden.

> [!Note]  
> **CommandLineEventConsumer** verwendet intern die [**CreateProcess-Methode**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) und übergibt die Eigenschaften **ExecutablePath** und **CommandLineTemplate** als die Parameter *lpApplicationName* und *lpCommandLine.* Im folgenden MOF-Codebeispiel (Managed Object Format) wird **CommandLineEventConsumer** nicht ordnungsgemäß verwendet.

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



Die [**CreateProcess-Methode**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) übergibt *lpCommandLine* als `argv[0]` , `argv[1]` usw. Da `argv[0]` für 16-Bit-Anwendungen bisher für den Namen der ausführbaren Datei reserviert war, führt der vorherige MOF-Code dazu, dass der Prozess so erstellt wird, als würde der folgende Befehl an der Eingabeaufforderung eingegeben **werden: c: \\ windows \\ system32 \\cscript.exe param1 param2**.

Der vorherige Befehl ist nicht erfolgreich, da Cscript.exe nicht untersucht `argv[0]` und daher nicht erkennt, dass er keinen eigenen Namen enthält, sondern etwas anderes ("c: \\ \\ Skripts \\ \\MyScript.js"). Im folgenden Beispiel wird die empfohlene Verwendung von **CommandLineEventConsumer** identifiziert.


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



Die vorherige Verwendung von **CommandLineEventConsumer** führt dazu, dass der Prozess so erstellt wurde, als ob der folgende Befehl an der Eingabeaufforderung eingegeben **wurde: c: \\ windows \\ system32 \\cscript.exe c: scriptsMyScript.js \\ \\ param1 param2**

Da "c: \\ \\ scripts \\ \\MyScript.js" jetzt `argv[1]` ist, wird es von Cscript.exe erkannt, und der Befehl ist erfolgreich.

Weitere Informationen finden Sie in der [**CreateProcess-Funktion.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung von **CommandLineEventConsumer** zum Erstellen eines Consumers finden Sie unter [Ausführen eines Programms über die Befehlszeile basierend auf einem Ereignis.](running-a-program-from-the-command-line-based-on-an-event.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stammabonnement<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Standard-Consumerklassen](standard-consumer-classes.md)
</dt> <dt>

[Überwachen und Reagieren auf Ereignisse mit Standard-Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Erstellen eines logischen Consumers](creating-a-logical-consumer.md)
</dt> <dt>

[Empfangen von Ereignissen zu jedem Zeitpunkt](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

