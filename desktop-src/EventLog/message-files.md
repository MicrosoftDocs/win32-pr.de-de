---
description: Jede Ereignis Quelle muss Nachrichten Dateien registrieren, die Beschreibungs Zeichenfolgen für jeden Ereignis Bezeichner, jede Ereignis Kategorie und jeden Parameter enthalten.
ms.assetid: 0c251a45-1414-4855-a6f5-86ebdfab2693
title: Nachrichten Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb20d5919c75f06bfd7b6db9b47216566ab6ac8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528745"
---
# <a name="message-files"></a>Nachrichten Dateien

Jede [Ereignis Quelle](event-sources.md) muss Nachrichten Dateien registrieren, die Beschreibungs Zeichenfolgen für jeden [Ereignis Bezeichner](event-identifiers.md), jede [Ereignis Kategorie](event-categories.md)und jeden [Parameter](event-identifiers.md)enthalten. Registrieren Sie diese Dateien in den Registrierungs Werten **EventMessageFile**, **categorymessagefile** und **ParameterMessageFile** für die Ereignis Quelle.

Sie können eine Nachrichtendatei erstellen, die Beschreibungen für die Ereignis Bezeichner, Kategorien und Parameter enthält, oder Sie können drei separate Nachrichten Dateien erstellen. Die Nachrichten-IDs für alle Nachrichten sollten eindeutig sein, unabhängig davon, ob Sie die Nachrichten in einer Datei oder in drei Dateien angeben. Mehrere Anwendungen können dieselbe Nachrichtendatei gemeinsam verwenden. Weitere Informationen zu Nachrichten Dateien finden Sie unter [**Message Compiler**](/windows/desktop/WES/message-compiler--mc-exe-). Ausführliche Informationen zur Syntax einer Nachrichtendatei finden Sie unter [Nachrichten Text Dateien](message-text-files.md).

## <a name="example-message-file"></a>Beispiel Nachrichtendatei

Im folgenden finden Sie eine Beispiel Nachrichtendatei.

``` syntax
; /* --------------------------------------------------------
; HEADER SECTION
;*/
SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
               Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
               Warning=0x2:STATUS_SEVERITY_WARNING
               Error=0x3:STATUS_SEVERITY_ERROR
              )
;
;
FacilityNames=(System=0x0:FACILITY_SYSTEM
               Runtime=0x2:FACILITY_RUNTIME
               Stubs=0x3:FACILITY_STUBS
               Io=0x4:FACILITY_IO_ERROR_CODE
              )
;
;/* ------------------------------------------------------------------
; MESSAGE DEFINITION SECTION
;*/

MessageIdTypedef=WORD

MessageId=0x1
SymbolicName=CAT_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CAT_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CAT_3
Language=English
Category 3
.

MessageIdTypedef=DWORD

MessageId=0x100
Severity=Error
Facility=Runtime
SymbolicName=MSG_COMMAND_ERR
Language=English
The command is incorrect. 
.

MessageId=0x101
Severity=Success
Facility=System
SymbolicName=MSG_STRIKE_ANY_KEY
Language=English
Press any key to continue . . . %0
.

MessageId=0x102
Severity=Error
Facility=System
SymbolicName=MSG_FILE_BAD_CONTENTS
Language=English
File %1 contains %2, which is in error
.

MessageId=0x103
Severity=Warning
Facility=System
SymbolicName=MSG_RETRYS
Language=English
There have been %1 retrys with %2 success! Disconnect from
the server and retry later.
.

MessageId=0x104
Severity=Informational
Facility=System
SymbolicName=MSG_INSERT_DISK
Language=English
Insert %%1000 in %%1001 and hit any key when ready... 
.

;/* Insert string parameters */
;

MessageId=1000
Severity=Success
Facility=System
SymbolicName=DISK
Language=English
disk%0
.

MessageId=1001
Severity=Success
Facility=System
SymbolicName=DRIVE
Language=English
drive%0
.
```

Die Anwendung [für die Ereignis](event-identifiers.md) Anzeige kann das folgende Verfahren verwenden, um Zugriff auf die Meldungs Zeichenfolgen in der Nachrichten-DLL zu erhalten.

**Abrufen von Beschreibungs Zeichenfolgen**

1.  Ruft die [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) -Funktion auf, um die Ereignis Quelle zu öffnen.
2.  Rufen Sie die [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) -Funktion auf, um den Inhalt des **EventMessageFile** -Werts für die Ereignis Quelle zu erhalten. Dies ist der Name der Nachrichten-dll.
3.  Aufrufen der [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) -Funktion zum Laden der von Schritt 2 festgelegten Nachrichten-dll.
4.  Rufen Sie die [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) -Funktion mit der Nachrichten-ID auf, um die Beschreibung aus der dll zu erhalten. (Beachten Sie, dass die Nachrichten-IDs in definiert sind. H-Datei, die vom Nachrichten Compiler generiert wurde.) Die **FormatMessage** -Funktion ersetzt die Einfügezeichenfolgen mit den Argument Werten, die Sie übergeben, ersetzt jedoch nicht die Parameter Einfügezeichenfolgen. vor der Anzeige der Zeichenfolge müssen Sie die Parameter Einfügezeichenfolgen selbst ersetzen.

 

 
