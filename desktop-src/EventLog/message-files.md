---
description: Jede Ereignisquelle sollte Nachrichtendateien registrieren, die Beschreibungszeichenfolgen für jeden Ereignisbezeichner, jede Ereigniskategorie und jeden Parameter enthalten.
ms.assetid: 0c251a45-1414-4855-a6f5-86ebdfab2693
title: Nachrichtendateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44de0c91a098ab1b916a73d99a02d0d31a8b5b7690936322166e65baef4bd13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951409"
---
# <a name="message-files"></a>Nachrichtendateien

Jede [Ereignisquelle](event-sources.md) sollte Nachrichtendateien registrieren, die Beschreibungszeichenfolgen für jeden [Ereignisbezeichner,](event-identifiers.md)die [Ereigniskategorie](event-categories.md)und den [Parameter](event-identifiers.md)enthalten. Registrieren Sie diese Dateien in den Registrierungswerten **EventMessageFile,** **CategoryMessageFile** und **ParameterMessageFile** für die Ereignisquelle.

Sie können eine Nachrichtendatei erstellen, die Beschreibungen für die Ereignisbezeichner, Kategorien und Parameter enthält, oder drei separate Nachrichtendateien erstellen. Die Nachrichtenbezeichner für alle Nachrichten sollten eindeutig sein, unabhängig davon, ob Sie die Nachrichten in einer oder drei Dateien angeben. Mehrere Anwendungen können dieselbe Nachrichtendatei gemeinsam nutzen. Weitere Informationen zu Nachrichtendateien finden Sie unter [**Nachrichtencompiler.**](/windows/desktop/WES/message-compiler--mc-exe-) Ausführliche Informationen zur Syntax einer Nachrichtendatei finden Sie unter [Nachrichtentextdateien.](message-text-files.md)

## <a name="example-message-file"></a>Beispielmeldungsdatei

Im Folgenden wird eine Beispielmeldungsdatei angezeigt.

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

Die Anwendung für die Ereignisanzeige kann das folgende Verfahren verwenden, um Zugriff auf die [Nachrichtenzeichenfolgen](event-identifiers.md) in der Nachrichten-DLL zu erhalten.

**So rufen Sie Beschreibungszeichenfolgen ab**

1.  Rufen Sie die [**RegOpenKey-Funktion**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) auf, um die Ereignisquelle zu öffnen.
2.  Rufen Sie die [**RegQueryValueEx-Funktion**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) auf, um den Inhalt des **EventMessageFile-Werts** für die Ereignisquelle abzurufen. Dies ist der Name der Nachrichten-DLL.
3.  Rufen Sie die [**LoadLibraryEx-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) auf, um die in Schritt 2 festgelegte Nachrichten-DLL zu laden.
4.  Rufen Sie die [**FormatMessage-Funktion**](/windows/desktop/api/winbase/nf-winbase-formatmessage) mit dem Nachrichtenbezeichner auf, um die Beschreibung aus der DLL abzurufen. (Beachten Sie, dass die Nachrichtenbezeichner in definiert sind. Vom Nachrichtencompiler generierte H-Datei.) Die **FormatMessage-Funktion** ersetzt die Einfügezeichenfolgen mithilfe der übergebenen Argumentwerte, aber nicht die Parametereinfügungszeichenfolgen. Sie müssen die Parametereinfügungszeichenfolgen selbst ersetzen, bevor Sie die Zeichenfolge anzeigen.

 

 
