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
# <a name="message-files"></a><span data-ttu-id="914d1-103">Nachrichten Dateien</span><span class="sxs-lookup"><span data-stu-id="914d1-103">Message Files</span></span>

<span data-ttu-id="914d1-104">Jede [Ereignis Quelle](event-sources.md) muss Nachrichten Dateien registrieren, die Beschreibungs Zeichenfolgen für jeden [Ereignis Bezeichner](event-identifiers.md), jede [Ereignis Kategorie](event-categories.md)und jeden [Parameter](event-identifiers.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="914d1-104">Each [event source](event-sources.md) should register message files that contain description strings for each [event identifier](event-identifiers.md), [event category](event-categories.md), and [parameter](event-identifiers.md).</span></span> <span data-ttu-id="914d1-105">Registrieren Sie diese Dateien in den Registrierungs Werten **EventMessageFile**, **categorymessagefile** und **ParameterMessageFile** für die Ereignis Quelle.</span><span class="sxs-lookup"><span data-stu-id="914d1-105">Register these files in the **EventMessageFile**, **CategoryMessageFile**, and **ParameterMessageFile** registry values for the event source.</span></span>

<span data-ttu-id="914d1-106">Sie können eine Nachrichtendatei erstellen, die Beschreibungen für die Ereignis Bezeichner, Kategorien und Parameter enthält, oder Sie können drei separate Nachrichten Dateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="914d1-106">You can create one message file that contains descriptions for the event identifiers, categories, and parameters, or create three separate message files.</span></span> <span data-ttu-id="914d1-107">Die Nachrichten-IDs für alle Nachrichten sollten eindeutig sein, unabhängig davon, ob Sie die Nachrichten in einer Datei oder in drei Dateien angeben.</span><span class="sxs-lookup"><span data-stu-id="914d1-107">The message identifiers for all of your messages should be unique whether you specify the messages in one file or three files.</span></span> <span data-ttu-id="914d1-108">Mehrere Anwendungen können dieselbe Nachrichtendatei gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="914d1-108">Several applications can share the same message file.</span></span> <span data-ttu-id="914d1-109">Weitere Informationen zu Nachrichten Dateien finden Sie unter [**Message Compiler**](/windows/desktop/WES/message-compiler--mc-exe-).</span><span class="sxs-lookup"><span data-stu-id="914d1-109">For more information on message files, see [**Message Compiler**](/windows/desktop/WES/message-compiler--mc-exe-).</span></span> <span data-ttu-id="914d1-110">Ausführliche Informationen zur Syntax einer Nachrichtendatei finden Sie unter [Nachrichten Text Dateien](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="914d1-110">For details on the syntax of a message file, see [Message Text Files](message-text-files.md).</span></span>

## <a name="example-message-file"></a><span data-ttu-id="914d1-111">Beispiel Nachrichtendatei</span><span class="sxs-lookup"><span data-stu-id="914d1-111">Example Message File</span></span>

<span data-ttu-id="914d1-112">Im folgenden finden Sie eine Beispiel Nachrichtendatei.</span><span class="sxs-lookup"><span data-stu-id="914d1-112">The following is an example message file.</span></span>

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

<span data-ttu-id="914d1-113">Die Anwendung [für die Ereignis](event-identifiers.md) Anzeige kann das folgende Verfahren verwenden, um Zugriff auf die Meldungs Zeichenfolgen in der Nachrichten-DLL zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="914d1-113">The event-viewing application can use the following procedure to gain access to the [message strings](event-identifiers.md) in the message DLL.</span></span>

<span data-ttu-id="914d1-114">**Abrufen von Beschreibungs Zeichenfolgen**</span><span class="sxs-lookup"><span data-stu-id="914d1-114">**To obtain description strings**</span></span>

1.  <span data-ttu-id="914d1-115">Ruft die [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) -Funktion auf, um die Ereignis Quelle zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="914d1-115">Call the [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) function to open the event source.</span></span>
2.  <span data-ttu-id="914d1-116">Rufen Sie die [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) -Funktion auf, um den Inhalt des **EventMessageFile** -Werts für die Ereignis Quelle zu erhalten. Dies ist der Name der Nachrichten-dll.</span><span class="sxs-lookup"><span data-stu-id="914d1-116">Call the [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function to obtain the contents of the **EventMessageFile** value for the event source, which is the name of the message DLL.</span></span>
3.  <span data-ttu-id="914d1-117">Aufrufen der [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) -Funktion zum Laden der von Schritt 2 festgelegten Nachrichten-dll.</span><span class="sxs-lookup"><span data-stu-id="914d1-117">Call the [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) function to load the message DLL determined by step 2.</span></span>
4.  <span data-ttu-id="914d1-118">Rufen Sie die [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) -Funktion mit der Nachrichten-ID auf, um die Beschreibung aus der dll zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="914d1-118">Call the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function with the message identifier to obtain the description from the DLL.</span></span> <span data-ttu-id="914d1-119">(Beachten Sie, dass die Nachrichten-IDs in definiert sind. H-Datei, die vom Nachrichten Compiler generiert wurde.) Die **FormatMessage** -Funktion ersetzt die Einfügezeichenfolgen mit den Argument Werten, die Sie übergeben, ersetzt jedoch nicht die Parameter Einfügezeichenfolgen. vor der Anzeige der Zeichenfolge müssen Sie die Parameter Einfügezeichenfolgen selbst ersetzen.</span><span class="sxs-lookup"><span data-stu-id="914d1-119">(Note that the messages identifiers are defined in the .H file generated by the message compiler.) The **FormatMessage** function will replace the insertion strings using the argument values that you pass but it will not replace the parameter insertion strings; you must replace the parameter insertion strings yourself before displaying the string.</span></span>

 

 
