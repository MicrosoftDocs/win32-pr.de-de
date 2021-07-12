---
description: Die Tabellen in diesem Dokument listen Wrapperfunktionen von Shlwapi.dll auf, die eingeschränkte Unicode-Funktionen auf Windows 95, Windows 98 und Windows Editionsversion (Windows Me) bereitstellen.
title: SHLWAPI-Wrapper-Funktionen
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3c428c89-b650-48c1-9f91-b94f9f8e10e2
api_name:
- SHLWAPI Wrapper Functions
- AppendMenuWrapW
- CallWindowProcWrapW
- CharLowerWrapW
- CharUpperBufWrapW
- CharUpperWrapW
- CompareStringWrapW
- CopyFileWrapW
- CreateEventWrapW
- CreateFileWrapW
- CreateWindowExWrapW
- DefWindowProcWrapW
- DeleteFileWrapW
- DialogBoxParamWrapW
- DispatchMessageWrapW
- DragQueryFileWrapW
- DrawTextExWrapW
- DrawTextWrapW
- ExtTextOutWrapW
- FormatMessageWrapW
- GetClassInfoWrapW
- GetDateFormatW
- GetDateFormatWrapW
- GetDlgItemTextWrapW
- GetFileAttributesWrapW
- GetLocaleInfoWrapW
- GetMenuItemInfoWrapW
- GetModuleFileNameWrapW
- GetModuleHandleWrapW
- GetObjectWrapW
- GetOpenFileNameWrapW
- GetSaveFileNameWrapW
- GetSystemDirectoryWrapW
- GetTimeFormatWrapW
- GetWindowLongWrapW
- GetWindowsDirectoryWrapW
- GetWindowTextLengthWrapW
- GetWindowTextWrapW
- InsertMenuItemWrapW
- IsCharAlphaNumericWrapW
- IsCharAlphaWrapW
- IsCharUpperWrapW
- LoadLibraryWrapW
- LoadStringWrapW
- MessageBoxWrapW
- MLGetUILanguage
- MoveFileWrapW
- OutputDebugStringWrapW
- PeekMessageWrapW
- PostMessageWrapW
- RegCreateKeyExWrapW
- RegisterClassWrapW
- RegOpenKeyExWrapW
- RegQueryValueExW
- RegQueryValueExWrapW
- RegQueryValueWrapW
- RegSetValueExWrapW
- SendMessageWrapW
- SetDlgItemTextWrapW
- SetWindowLongWrapW
- SetWindowTextWrapW
- SHCancelTimerQueueTimer
- SHDeleteTimerQueue
- ShellExecuteExWrapW
- ShellMessageBoxWrapW
- SHGetFileInfoWrapW
- SHGetPathFromIDListWrapW
- SHInterlockedCompareExchange
- SHQueueUserWorkItem
- SHSetTimerQueueTimer
- TranslateAcceleratorWrapW
- UnregisterClassWrapW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7c166e005c9bcc9efe68fee926c9fa9c2a4f4e7e
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581768"
---
# <a name="shlwapi-wrapper-functions"></a>SHLWAPI-Wrapper-Funktionen

\[Diese Funktionen sind über Windows XP Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie können in nachfolgenden Versionen von geändert oder nicht verfügbar Windows.\]

Die Tabellen in diesem Dokument listen Wrapperfunktionen von Shlwapi.dll auf, die eingeschränkte Unicode-Funktionen auf Windows 95, Windows 98 und Windows Editionsversion (Windows Me) bereitstellen.

Windows 95, Windows 98 und Windows Edition (Windows Me) werden hier als "native ANSI-Plattformen" bezeichnet. Auf nativen ANSI-Plattformen konvertieren diese Wrapperfunktionen die Unicode-Eingabezeichenfolgenparameter in ANSI und rufen ANSI-Versionen von Funktionen in der **Spalte Forwards To** auf. **AppendMenuWrapW** ruft beispielsweise **AppendMenuA** auf. Dies ist die ANSI-Version von [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). Die anderen Funktionen folgen dem gleichen Muster. Alle von der ANSI-Funktion zurückgegebenen Zeichenfolgen werden in Unicode konvertiert und an die aufrufende Anwendung zurückgegeben. Abgesehen von den ausnahmen, die in der **Spalte "Hinweise"** angegeben sind, verfügt die Wrapperfunktion über die gleiche Syntax und bietet die gleiche Funktionalität wie die Funktion in der **Spalte "Forwards To".** Ausführliche Informationen zur Verwendung finden Sie auf dieser Referenzseite.

**Sicherheitswarnung:** Mehrere Unicode-Zeichenfolgen können in dieselbe ANSI-Zeichenfolge konvertiert werden. Unerwartete Kollisionen nach der Konvertierung können zu unerwartetem Verhalten führen. Wenn beispielsweise **CreateEventWrapW** verwendet wird, um zwei ereignisse mit unterschiedlichen Namen zu erstellen, deren Namen nach der Konvertierung von Unicode in ANSI übereinstimmen, gibt der zweite Aufruf ein Handle für dasselbe Ereignis wie beim ersten Aufruf zurück, obwohl sich die ursprünglichen Unicode-Zeichenfolgen unterscheiden.

Microsoft Windows NT, Windows 2000, Windows XP, Windows Server 2003 und höher werden hier als "native Unicode-Plattformen" bezeichnet. In den meisten Teilen werden diese Wrapperfunktionen auf nativen Unicode-Plattformen einfach Eingabezeichenfolgenparameter an die Unicode-Version der Funktion in der **Spalte Forwards To (Weitergeleitet an)** weitergeleitet. Beispielsweise wird **AppendMenuWrapW** an **AppendMenuW** weitergeleitet. Dies ist die Unicode-Version von [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). Die anderen Funktionen folgen dem gleichen Muster. Alle Zeichenfolgen, die von der Unicode-Funktion zurückgegeben werden, werden an die aufrufende Anwendung zurückgegeben. Abgesehen von den ausnahmen, die in der **Spalte "Hinweise"** angegeben sind, verfügt die Wrapperfunktion über die gleiche Syntax und bietet die gleiche Funktionalität wie die Funktion in der **Spalte "Forwards To".** Ausführliche Informationen zur Verwendung finden Sie auf dieser Referenzseite.

**Sicherheitswarnung:** Die Sicherheitsprobleme, die für die Funktionen in der **Spalte Forwards To** (Weiter an) angegeben sind, gelten auch für die entsprechenden Wrapperfunktionen. Weitere Informationen finden Sie in der Referenzdokumentation für die Funktion in der **Spalte "Forwards To".**

Die Wrapperfunktionen in dieser Tabelle sind alle in Shlwapi.dll. Um sie aufrufen zu können, müssen Sie die in der Tabelle aufgeführte Ordnungszahl verwenden.

> [!Note]  
> Diese Wrapperfunktionen sind unter Windows XP verfügbar, bieten jedoch keine Wrapperfunktionen in Windows XP Service Pack 2 (SP2) und höher. Außerdem bieten sie keine Wrapperfunktionen in Windows Server 2003. Sie sollten stattdessen die funktionen verwenden, die in **der Spalte Forwards To aufgeführt** sind.

 



| Funktion                  | Ordinal | Weitergeleitet an                                             | DLL      | Bemerkungen                                                                                                                             |
|---------------------------|---------|---------------------------------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| AppendMenuWrapW           | 36      | [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)                     | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(Menü)](#menu)                                                           |
| CallWindowProcWrapW       | 37      | [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)             | USER32   | [(i)](#shlwapi-wrapper-functions)                                                                                                   |
| CharLowerWrapW            | 38      | [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)                       | Kernel32.dll | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperBufWrapW         | 44      | [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)               | Kernel32.dll | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperWrapW            | 43      | [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)                       | Kernel32.dll | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| CompareStringWrapW        | 45      | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                 | Kernel32.dll | [(CompareString)](#comparestring)                                                                                                   |
| CopyFileWrapW             | 112     | [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile)                             | Kernel32.dll | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| CreateEventWrapW          | 51      | [**Createevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)                     | Kernel32.dll | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| CreateFileWrapW           | 52      | [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)                         | Kernel32.dll | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| CreateWindowExWrapW       | 55      | [**Createwindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa)             | USER32   | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| DefWindowProcWrapW        | 56      | [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)               | USER32   | [(i)](#shlwapi-wrapper-functions)                                                                                                   |
| DeleteFileWrapW           | 57      | [**DeleteFile**](/windows/win32/api/fileapi/nf-fileapi-deletefilea)                         | Kernel32.dll | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| DialogBoxParamWrapW       | 59      | [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama)             | USER32   | [(f)](#dragqueryfile), [(i)](#shlwapi-wrapper-functions), [(DialogBoxParam)](#dialogboxparam)                                       |
| DispatchMessageWrapW      | 60      | [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)           | USER32   | [(i)](#shlwapi-wrapper-functions)                                                                                                   |
| DragQueryFileWrapW        | 318     | [**DragQueryFile**](/windows/win32/api/Shellapi/nf-shellapi-dragqueryfilea)                  | SHELL32  | [(b)](#dialogboxparam), [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DragQueryFile)](#dragqueryfile)               |
| DrawTextExWrapW           | 301     | [**DrawTextEx**](/windows/win32/api/winuser/nf-winuser-drawtextexa)                        | USER32   | [(a)](#shlwapi-wrapper-functions), [(d)](#shlwapi-wrapper-functions)                                                                |
| DrawTextWrapW             | 61      | [**Drawtext**](/windows/win32/api/winuser/nf-winuser-drawtext)                            | USER32   | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| ExtTextOutWrapW           | 299     | [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)                        | GDI32    | [(d)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(ExtTextOut)](#exttextout)                                               |
| FormatMessageWrapW        | 68      | [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)                 | Kernel32.dll | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(FormatMessage)](#formatmessage)                                       |
| GetClassInfoWrapW         | 69      | [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa)                 | USER32   | [(GetClassInfo)](#getclassinfo)                                                                                                     |
| GetDateFormatWrapW        | 311     | [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)                 | Kernel32.dll | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| GetDlgItemTextWrapW       | 74      | [**GetDlgItemText**](/windows/win32/api/winuser/nf-winuser-getdlgitemtexta)             | USER32   | [(g)](#compareexchange)                                                                                                             |
| GetFileAttributesWrapW    | 75      | [**GetFileAttributes**](/windows/win32/api/fileapi/nf-fileapi-getfileattributesa)           | Kernel32.dll | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| GetLocaleInfoWrapW        | 77      | [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)                 | Kernel32.dll | [(g)](#compareexchange)                                                                                                             |
| GetMenuItemInfoWrapW      | 302     | [**GetMenuItemInfo**](/windows/win32/api/winuser/nf-winuser-getmenuiteminfoa)           | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange), [(MenuItemInfo)](#menuiteminfo)                                                     |
| GetModuleFileNameWrapW    | 80      | [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)         | Kernel32.dll | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetModuleHandleWrapW      | 83      | [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)             | Kernel32.dll | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetObjectWrapW            | 84      | [**Getobject**](/windows/win32/api/wingdi/nf-wingdi-getobject)                          | GDI32    | [(g)](#compareexchange)                                                                                                             |
| GetOpenFileNameWrapW      | 403     | [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OpenFileName)](#openfilename)                 |
| GetSaveFileNameWrapW      | 389     | [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OpenFileName)](#openfilename)                 |
| GetSystemDirectoryWrapW   | 81      | [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)       | Kernel32.dll | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetTimeFormatWrapW        | 310     | [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)                 | Kernel32.dll | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| GetWindowLongWrapW        | 94      | [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)               | USER32   | [(WindowLong)](#windowlong)                                                                                                         |
| GetWindowsDirectoryWrapW  | 97      | [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)     | Kernel32.dll | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetWindowTextLengthWrapW  | 96      | [**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)   | USER32   | [(j)](#j)                                                                                                                           |
| GetWindowTextWrapW        | 95      | [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)               | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange)                                                                                      |
| InsertMenuItemWrapW       | 98      | [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema)             | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(Menu)](#menu), [(MenuItemInfo)](#menuiteminfo)                          |
| IsCharAlphaWrapW          | 25      | [**IsCharAlpha**](/windows/win32/api/winuser/nf-winuser-ischaralphaa)                   | USER32   | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharAlphaNumericWrapW   | 28      | [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)     | Kernel32.dll | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharUpperWrapW          | 26      | [**IsCharUpper**](/windows/win32/api/winuser/nf-winuser-ischaruppera)                   | USER32   | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| LoadLibraryWrapW          | 105     | [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                     | Kernel32.dll | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| LoadStringWrapW           | 107     | [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)                     | Kernel32.dll | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| MessageBoxWrapW           | 340     | [**Messagebox**](/windows/win32/api/winuser/nf-winuser-messagebox)                     | USER32   | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| MoveFileWrapW             | 113     | [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)                             | Kernel32.dll | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| OutputDebugStringWrapW    | 115     | [**Outputdebugstring**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)         | Kernel32.dll | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| PeekMessageWrapW          | 116     | [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)                   | USER32   | [(PeekMessage und PostMessage)](#peekmessage-and-postmessage)                                                                       |
| PostMessageWrapW          | 117     | [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)                   | USER32   | [(PeekMessage und PostMessage)](#peekmessage-and-postmessage)                                                                       |
| RegCreateKeyExWrapW       | 120     | [**RegCreateKeyEx**](/windows/win32/api/winreg/nf-winreg-regcreatekeyexa)               | ADVAPI32 | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| RegisterClassWrapW        | 131     | [**Registerclass**](/windows/win32/api/winuser/nf-winuser-registerclassa)               | USER32   | [(a)](#shlwapi-wrapper-functions), [(RegisterClass)](#registerclass)                                                                |
| RegOpenKeyExWrapW         | 125     | [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)                   | ADVAPI32 | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| RegQueryValueExWrapW      | 128     | [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa)             | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(ValueEx)](#regqueryvalueexw), [(RegQueryValueExW)](#regqueryvalueexw) |
| RegQueryValueWrapW        | 127     | [**RegQueryValue**](/windows/win32/api/winreg/nf-winreg-regqueryvaluea)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| RegSetValueExWrapW        | 130     | [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvalueexa)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(ValueEx)](#regqueryvalueexw)                                                                   |
| SendMessageWrapW          | 136     | [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)                   | USER32   | [(SendMessage)](#sendmessage)                                                                                                       |
| SetDlgItemTextWrapW       | 138     | [**SetDlgItemText**](/windows/win32/api/winuser/nf-winuser-setdlgitemtexta)             | USER32   | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| SetWindowLongWrapW        | 141     | [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)               | USER32   | [(WindowLong)](#windowlong)                                                                                                         |
| SetWindowTextWrapW        | 143     | [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)               | USER32   | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| ShellExecuteExWrapW       | 35      | [**ShellExecuteEx**](/windows/win32/api/Shellapi/nf-shellapi-shellexecuteexa)                | SHELL32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(ShellExecuteEx)](#shellexecuteex)                                      |
| ShellMessageBoxWrapW      | 388     | [**ShellMessageBox**](/windows/win32/api/Shellapi/nf-shellapi-shellmessageboxa)              | SHLWAPI  | [(a)](#shlwapi-wrapper-functions), [(FormatMessage)](#formatmessage)                                                                |
| SHGetFileInfoWrapW        | 313     | [**SHGetFileInfo**](/windows/win32/api/Shellapi/nf-shellapi-shgetfileinfoa)                  | SHELL32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange)                                                  |
| SHGetPathFromIDListWrapW  | 334     | [**SHGetPathFromIDList**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista)      | USER32   | [(g)](#compareexchange)                                                                                                             |
| TranslateAcceleratorWrapW | 146     | [**Translateaccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) | USER32   | [(i)](#shlwapi-wrapper-functions)                                                                                                   |
| UnregisterClassWrapW      | 147     | [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)           | USER32   | [(a)](#shlwapi-wrapper-functions)                                                                                                   |



 

Die Wrapperfunktionen in der folgenden Tabelle führen keine Zeichensatzkonvertierung durch. Stattdessen bieten sie eingeschränkte Unterstützung für Betriebssystemfeatures, die auf früheren Plattformen nicht verfügbar sind.



| Funktion                     | Ordinal | Weiterleitung an                                                                     | DLL      | Bemerkungen                                                                        |
|------------------------------|---------|---------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------|
| MLGetUILanguage              | 376     | [**GetUserDefaultUILanguage**](/windows/win32/api/winnls/nf-winnls-getuserdefaultuilanguage)                   | Kernel32.dll | [(h)](#shlwapi-wrapper-functions)                                              |
| SHCancelTimerQueueTimer      | 265     | [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer)                         | Kernel32.dll | [(h)](#shlwapi-wrapper-functions)                                              |
| SHDeleteTimerQueue           | 262     | [**DeleteTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueue)                                   | Kernel32.dll | [(h)](#shlwapi-wrapper-functions)                                              |
| SHInterlockedCompareExchange | 342     | [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) | Kernel32.dll | [(CompareExchange)](#compareexchange)                                          |
| SHQueueUserWorkItem          | 260     | [**Queueuserworkitem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                                 | Kernel32.dll | [(QueueUserWorkItem)](#queueuserworkitem), [(h)](#shlwapi-wrapper-functions)   |
| SHSetTimerQueueTimer         | 263     | [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)                         | Kernel32.dll | [(SetTimerQueueTimer)](#settimerqueuetimer), [(h)](#shlwapi-wrapper-functions) |



 

## <a name="remarks"></a>Bemerkungen

### <a name="a"></a>(a)

Wenn eine Zeichenfolgenkonvertierung erforderlich ist, werden alle Zeichenfolgen über die CP \_ ACP-Codepage konvertiert.

Diese Funktionen verwenden am besten geeignete Zeichen und führen keine Standardüberprüfung durch, wenn sie von Unicode in ANSI konvertiert werden. Wenn die Zeichenfolge nicht aus Unicode in ANSI konvertiert werden kann, übergibt die Wrapperfunktion außerdem eine **NULL-Zeichenfolge** an die zugrunde liegende ANSI-Funktion. Dies kann beispielsweise auftreten, wenn nicht genügend Arbeitsspeicher vorhanden ist. Das Übergeben einer **NULL-Zeichenfolge** kann dazu führen, dass einige Funktionen mit einem Fehler aufgrund eines ungültigen Parameters fehlschlagen, aber andere Funktionen akzeptieren die **NULL-Zeichenfolge** und behandeln sie als beabsichtigten Parameter. Beispielsweise tritt ein Fehler auf, wenn die **CreateWindowExWrapW-Funktion** versucht, den *lpWindowName-Parameter* in ANSI zu konvertieren, und [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ein Fenster mit einer leeren Beschriftung erstellt. Der Wrapper benachrichtigt Sie nicht, wenn diese Probleme aufgetreten sind.

Die Microsoft Layer for Unicode (MSLU) überprüft während der Konvertierung von Unicode in ANSI auf Fehler und gibt entsprechende Fehlerwerte zurück. Beispielsweise gibt die [**AppendMenu-Wrapperfunktion**](/windows/win32/api/winuser/nf-winuser-appendmenua) in der MSLU 0 zurück, wenn das Element nicht erfolgreich angefügt wurde.

### <a name="b"></a>(b)

Diese Funktionen verwenden einen verzögert geladenen Link zur entsprechenden Funktion. Dies bedeutet, dass die DLL, die die Funktion in der Spalte "Forwards To" enthält, erst vom Shlwapi.dll geladen wird, wenn eine Funktion in dieser DLL aufgerufen wird. Der linker Microsoft Visual C++ unterstützt diese Funktionalität allgemeiner über die Option /DELAYLOAD.

### <a name="c"></a>(c)

Diese Funktion bearbeitet Dateinamen. Wie in [(a)](#shlwapi-wrapper-functions)erwähnt, konvertieren die Funktionen alle Zeichenfolgen über die CP \_ ACP-Codepage. Sie überprüfen nicht, ob die Datei-E/A-Funktionen auf den ANSI-Modus festgelegt wurden. Wenn sich die Datei-E/A-Funktionen im OEM-Modus befinden, werden die Zeichenfolgen in und aus dem falschen Zeichensatz konvertiert. Eine Anwendung kann die Datei-E/A-Funktionen explizit auf den OEM-Modus festlegen, indem sie die [**SetFileApisToOEM-Funktion**](/windows/win32/api/fileapi/nf-fileapi-setfileapistooem) aufruft.

**Sicherheitswarnung: ** Die Verwendung dieser Wrapperfunktionen für Dateinamen kann die Sicherheit Ihrer Anwendung beeinträchtigen. Da keine Standardüberprüfung durchgeführt wird und am besten geeignete Zeichen verwendet werden, können Dateinamenzeichen auf unerwartete Weise konvertiert werden. Dies kann zu Dateisystem-Spoofingangriffen führen. Darüber hinaus kann während der Konvertierung von Unicode in ANSI ein automatischer Datenverlust auftreten.

Für die MSLU gelten diese Einschränkungen nicht.

### <a name="d"></a>(d)

Wenn für die gezeichnete Zeichenfolge ein Zeichensatz erforderlich ist, der nicht in der Schriftart verfügbar ist, die im Gerätekontext ausgewählt ist, verwenden diese Wrapperfunktionen das [Feature "Schriftartverknüpfung"](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767872(v=vs.85)) der [MLang-Bibliothek,](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767865(v=vs.85)) um jedes Zeichen in einer geeigneten Schriftart zu rendern. Im Gegensatz zu den meisten anderen Wrapperfunktionen funktionieren diese zusätzlich zu nativen ANSI-Plattformen auf Microsoft Windows NT 4.0.

### <a name="e"></a>(e)

Vollständige Unicode-Implementierungen dieser Funktionen sind auf nativen ANSI-Plattformen verfügbar. Diese Funktionen rufen nicht die zugehörige ANSI-Funktion auf.

### <a name="f"></a>(f)

Wenn die Benutzerstandard-UI-Sprache einen anderen Zeichensatz als die Standardsprache der Benutzeroberfläche verwendet, versucht das System, Dialogvorlagen und Unterklassensteuerelemente neu zu schreiben und Menüelemente in owner-draw zu konvertieren, sodass Zeichenfolgen in der Benutzerstandard-UI-Sprache weiterhin ordnungsgemäß angezeigt werden. Die einzigen Steuerelemente, die von den Regeln für das erneute Schreiben von Dialogfeldvorlagen unterstützt werden, sind statische Steuerelemente, Schaltflächen-, Listenfeld- und Combobox-Steuerelemente. Diese Steuerelemente sind so untergliedert, dass die **SendMessageWrapW-Funktion** die ursprüngliche Unicode-Zeichenfolge abrufen kann, ohne durch den ANSI-Zeichensatz übersetzt zu werden. Im Gegensatz zu den meisten anderen Wrapperfunktionen funktionieren diese sowohl auf Microsoft Windows NT 4.0 als auch auf nativen ANSI-Plattformen. In den Hinweisen in der Dokumentation der [**MLLoadLibrary-Funktion**](./callbacks.md) wird näher erläutert, wie die Benutzerstandard-UI-Sprache und die Systemstandard-UI-Sprache bestimmt werden.

### <a name="g"></a>(g)

Wenn eine Zeichenfolgenkonvertierung erforderlich ist, werden alle Zeichenfolgen über die CP \_ ACP-Codepage konvertiert.

Wenn beim Konvertieren von ANSI in Unicode für die Ausgabe die zurückgegebene Zeichenfolge nicht in den bereitgestellten Puffer passt, werden die Zeichenfolgen von den Wrapperfunktionen abgeschnitten. Funktionen, die die Anzahl der in den Puffer kopierten Zeichen oder die Anzahl der Zeichen zurückgeben, die erforderlich sind, um abgeschnittene Zeichen zu vermeiden, geben nicht die Anzahl der Unicode-Zeichen zurück, die in den Puffer kopiert werden, der vom Aufrufer der Wrapperfunktion bereitgestellt oder vom Aufrufer benötigt wird. Sie geben die Anzahl der ANSI-Zeichen zurück, die in den Puffer kopiert oder von der zugrunde liegenden ANSI-Funktion benötigt werden. Für die MSLU gelten diese Einschränkungen nicht.

### <a name="h"></a>(h)

Auf Systemen vor Windows XP implementieren diese Funktionen einen vereinfachten Threadpool und eine vereinfachte Timerwarteschlange. Auf Windows XP und höher verwenden diese Funktionen den Systemthreadpool und die Systemzeitgeberwarteschlange. Für die Zeitgeber-Warteschlangenfunktionen muss der *hQueue-Parameter* auf **NULL** festgelegt werden, um anzugeben, dass der Vorgang für die Standardzeitgeberwarteschlange ausgeführt werden soll.

### <a name="i"></a>(i)

Auf Unicode-Plattformen übersetzen diese Funktionen die Nachricht aus Unicode in ANSI, wenn das Zielfenster ANSI ist. Diese Funktionen führen keine Nachrichtenübersetzung auf nativen ANSI-Plattformen durch. Daher muss durch aufrufende Anwendungen, die diese Funktion aufrufen, sichergestellt werden, dass die Nachricht auf Unicode-Plattformen im Unicode-Format und auf ANSI-Plattformen im ANSI-Format vorliegt. Im folgenden Funktionsaufruf muss das *wParam* beispielsweise ein Unicode-Codepunkt sein, wenn das Programm auf einer Unicode-Plattform ausgeführt wird, und ein ANSI-Zeichen sein, wenn das Programm auf einer ANSI-Plattform ausgeführt wird.

``` syntax
CallWindowProcWrapW(prevWndProc, hwnd, WM_CHAR, wParam, lParam);
```

Die MSLU verfolgt den Zeichensatz der Zielfensterprozedur nach und konvertiert die Nachricht nach Bedarf.

### <a name="j"></a>(j)

Auf ANSI-Plattformen geben diese Funktionen die Länge der zugrunde liegenden ANSI-Zeichenfolge zurück, nicht die Länge der übersetzten Unicode-Zeichenfolge. Für die MSLU gelten diese Einschränkungen nicht.

### <a name="compareexchange"></a>(CompareExchange)

Die Syntax für **SHInterlockedCompareExchange** unterscheidet sich etwas von der von [**InterlockedCompareExchangePointer,**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer)funktioniert aber identisch.

``` syntax
void* SHInterlockedCompareExchange(void **ppDest, void *pExch, void *pComp);
```

### <a name="comparestring"></a>(CompareString)

Beachten Sie, dass auf nativen ANSI-Plattformen beide Zeichenfolgen in ANSI konvertiert und als ANSI-Zeichenfolgen verglichen werden. Wenn die Unicode-Zeichenfolgen Zeichen enthalten, die nicht in ANSI dargestellt werden können, können die Ergebnisse unerwartet sein. Wenn die STANDARD-ANSI-Codepage beispielsweise keine CJK-Zeichen unterstützt, würden die Zeichenfolgen L" \\ x66F0" und L" \\ x6708" auf nativen ANSI-Plattformen als gleich verglichen, da sie beide der ANSI-Zeichenfolge "?" zugeordnet sind.

### <a name="datetime"></a>(DateTime)

In Shlwapi.dll Version 5.0, die mit Windows 2000 ausgeliefert wurde, muss die Codepage des Gebietsschemabezeichners, den Sie als ersten Parameter von **GetDateFormatWrapW** und **GetTimeFormatWrapW** übergeben, mit der aktuellen ANSI-Codepage übereinstimmen. Andernfalls kann die zurückgegebene Zeichenfolge falsch konvertiert werden. Diese Einschränkung gilt nicht für Shlwapi.dll Version 5.5 oder höher. Dies bedeutet, dass Windows XP- und höher-Systeme dieser Einschränkung nicht unterliegen. Für die MSLU gilt diese Einschränkung nicht.

### <a name="dialogboxparam"></a>(DialogBoxParam)

Der *lpTemplateName-Parameter* für die **DialogBoxParamWrapW-Funktion** darf keine Zeichenfolge sein. Es muss sich um eine Ordnungszahl handelt, die vom [**MAKEINTRESOURCE-Makro**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) erstellt wird. Die vom *lpDialogFunc-Parameter* angegebene Dialogprozedur empfängt ANSI-Nachrichten auf nativen ANSI-Plattformen und Unicode-Nachrichten auf nativen Unicode-Plattformen. Die Dialogprozedur muss für beide Fälle vorbereitet sein. Für die MSLU gelten diese Einschränkungen nicht.

### <a name="exttextout"></a>(ExtTextOut)

Native ANSI-Plattformen implementieren die [**ExtTextOutW-Funktion**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) sowie native Unicode-Plattformen. Der Zweck von **ExtTextOutWrapW** besteht darin, Schriftartverknüpfungen durchzuführen, wie in einer separaten Anmerkung beschrieben.

### <a name="dragqueryfile"></a>(DragQueryFile)

Mit der **DragQueryFileWrapW-Funktion** können Sie die Länge einer Datei im Drop-Handle nicht abfragen, indem **Sie NULL** als *lpszFile-Parameter* übergeben. Für die MSLU gelten diese Einschränkungen nicht.

### <a name="formatmessage"></a>(FormatMessage)

Auf nativen ANSI-Plattformen werden die Formate in der Zeichenfolge nicht aus Unicode in ANSI konvertiert. Das folgende Codebeispiel ist beispielsweise fehlerhaft.


```
WCHAR szBuffer[MAX_PATH];
DWORD_PTR Arguments[2] = { L"String1", L"String2" };

FormatMessageWrapW(FORMAT_MESSAGE_FROM_STRING, 
               L"%1!s! %2", 
               0, 0, 
               szBuffer, 
               MAX_PATH, 
               (va_list*)Arguments);
```



In diesem Codebeispiel wird "!s!" verwendet. akzeptiert. Auf nativen ANSI-Plattformen wird diese Zeichenfolge an die ANSI-Version der [**FormatMessage-Funktion**](/windows/win32/api/winbase/nf-winbase-formatmessage) übergeben. Daher wird anstelle einer Unicode-Zeichenfolge eine ANSI-Zeichenfolge erwartet. Ebenso impliziert das Format "%2" ein Zeichenfolgenargument. Wenn sie an die ANSI **FormatMessage-Funktion** übergeben wird, wird sie als ANSI-Zeichenfolge und nicht als Unicode-Zeichenfolge interpretiert. Die richtige Formatzeichenfolge ist L"%1!ws! %2!ws!". Dadurch werden Zeichenfolgen sowohl auf ANSI- als auch auf Unicode-Plattformen ordnungsgemäß gedruckt.

Die Funktion unterstützt "%0" nicht. Spezielle Formatzeichenfolge.

Für die MSLU gelten diese Einschränkungen nicht.

### <a name="getclassinfo"></a>(GetClassInfo)

Auf nativen ANSI-Plattformen werden die Member **lpszMenuName** und **lpszClassName** der [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) nicht in Unicode übersetzt und immer auf **NULL** festgelegt. Darüber hinaus wird die im **lpfnWndProc-Member** der **WNDCLASS-Struktur** zurückgegebene Fensterprozedur nicht in Unicode übersetzt und verweist auf eine ANSI-Fensterprozedur. Für die MSLU gelten diese Einschränkungen nicht.

### <a name="menu"></a>(Menü)

In Shlwapi.dll Version 5.0, die mit Windows 2000 ausgeliefert wurde, werden Menüelementzeichenfolgen, die Tabstoppzeichen (t) enthalten, \\ möglicherweise nicht ordnungsgemäß angezeigt. Diese Einschränkung gilt nicht für Shlwapi.dll Version 5.5 oder höher. Dies bedeutet, dass Windows XP- und höher-Systeme dieser Einschränkung nicht unterliegen. Für die MSLU gilt diese Einschränkung nicht.

### <a name="menuiteminfo"></a>(MenuItemInfo)

Diese Funktion unterstützt nur die Microsoft Windows NT 4.0-Version der [**MENUITEMINFOW-Struktur.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) Dieser Struktur fehlt ein **hbmpItem-Member.** Darüber hinaus unterstützt die Funktion das MIIM \_ BITMAP-Flag nicht. Für die MSLU gelten diese Einschränkungen nicht.

### <a name="openfilename"></a>(OpenFileName)

Der **cbSize-Member** der [**OPENFILENAMEW-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) muss auf sizeof(OPENFILENAME \_ NT4W) festgelegt werden.

Der **lpstrCustomFilter-Member** der [**OPENFILENAMEW-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) muss auf **NULL** festgelegt werden.

Die Werte der **Member nMaxFile** und **nMaxFileTitle** der [**OPENFILENAMEW-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) dürfen MAX PATH nicht \_ überschreiten.

Wenn der **lpfnHook-Member** der [**OPENFILENAMEW-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) nicht **NULL** ist, muss er auf eine ANSI-Hookprozedur auf nativen ANSI-Plattformen und eine Unicode-Hookprozedur auf nativen Unicode-Plattformen verweisen.

Für die MSLU gelten diese Einschränkungen nicht.

### <a name="peekmessage-and-postmessage"></a>(PeekMessage und PostMessage)

Auf nativen ANSI-Plattformen wird keine Übersetzung für die übertragene oder abgerufene Nachricht ausgeführt. Die übertragene/abgerufene Nachricht ist ANSI auf nativen ANSI-Plattformen und Unicode auf nativen Unicode-Plattformen. Die aufrufende Anwendung muss darauf vorbereitet sein, beide Fälle zu verarbeiten. Wenn die abgerufene Nachricht z. B. WM \_ CHAR ist, ist die *wParam* ein ANSI-Zeichencode auf nativen ANSI-Plattformen, aber es handelt sich um einen Unicode-Codepunkt auf nativen Unicode-Plattformen. Für die MSLU gelten diese Einschränkungen nicht.

### <a name="queueuserworkitem"></a>(QueueUserWorkItem)

Die **SHQueueUserWorkItem-Funktion** unterscheidet sich geringfügig von der entsprechenden [**QueueUserWorkItem-Funktion.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) Die Syntax für **SHQueueUserWorkItem** wird hier gezeigt.

``` syntax
BOOL SHQueueUserWorkItem(LPTHREAD_START_ROUTINE pfnCallback,
                     LPVOID pContext,
                     LONG lPriority,
                     DWORD_PTR dwTag,
                     DWORD_PTR * pdwId,
                     LPCSTR pszModule,
                     DWORD dwFlags);
```

Die Parameter sollten wie folgt festgelegt werden:

-   Die Parameter *pfnCallback* und *pContext* haben die gleiche Bedeutung wie die *Parameter Function* *bzw. Context* von [**QueueUserWorkItem.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)
-   Der *dwTag-Parameter* wird nicht verwendet und muss auf 0 festgelegt werden.
-   Der *pdwld-Parameter* wird nicht verwendet und muss auf **NULL** festgelegt werden.
-   Der *pszModule-Parameter* verweist auf eine optionale NULL-terminierte ANSI-Zeichenfolge, die den Namen einer Bibliothek angibt, die geladen werden soll, bevor das Arbeitselement beginnt und nach Abschluss des Arbeitselements entladen wird. Dieser Parameter kann **NULL** sein.
-   Der *dwFlags-Parameter* unterstützt nur eine Teilmenge der Werte, die von [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)unterstützt werden. Die folgenden Flags werden erkannt.

    

    | Name              | Wert      | Bedeutung                          |
    |-------------------|------------|----------------------------------|
    | TPS \_ EXECUTEIO    | 0x00000001 | Identisch mit WT \_ EXECUTEINIOTHREAD.   |
    | TPS \_ LONGEXECTIME | 0x00000008 | Identisch mit WT \_ EXECUTELONGFUNCTION. |

    

     

    > [!Note]  
    > Das FLAG TPS \_ LONGEXECTIME weist nicht den gleichen numerischen Wert wie das WT \_ EXECUTELONGFUNCTION-Flag auf. Bei Verwendung von **SHQueueUserWorkItem** muss der dwFlags-Parameter eine Kombination aus TPS-Werten \_ \* und nicht WT-Werten \_ \* sein.

     

**SHQueueUserWorkItem** gibt einen Wert ungleich 0 (null) zurück, wenn das Arbeitselement erfolgreich in die Warteschlange eingereiht wurde, andernfalls 0. Wenn die Funktion fehlschlägt, können Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) verwenden, um zusätzliche Informationen abzurufen.

### <a name="registerclass"></a>(RegisterClass)

Auf nativen ANSI-Plattformen wird keine Übersetzung für den **lpfnWndProc-Member** der [**WNDCLASSW-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) ausgeführt. Das Fenster empfängt ANSI-Fenstermeldungen auf nativen ANSI-Plattformen und Unicode-Fenstermeldungen auf nativen Unicode-Plattformen. Die Fensterprozedur muss für beide Fälle vorbereitet sein. Für die MSLU gelten diese Einschränkungen nicht.

### <a name="regqueryvalueexw"></a>(RegQueryValueExW)

**RegQueryValueExWrapW** wurde auch unter dem Namen **RegQueryValueExW** aufgerufen. Wie jede unbenannte Funktion, die ausschließlich nach Ordnungszahl exportiert wird, können Sie den Namen auswählen, unter dem die Funktion im Code bekannt ist.

### <a name="sendmessage"></a>(SendMessage)

Auf nativen Unicode-Plattformen leitet die **SendMessageWrapW-Funktion** an die [**SendMessageW-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessage) weiter. Auf nativen ANSI-Plattformen bietet **SendMessageWrapW** eingeschränkte Unterstützung für die Übersetzung von Unicode-Nachrichten in ANSI. Die Liste der unterstützten Nachrichten ist in der folgenden Tabelle angegeben. Die Funktion übersetzt keine anderen Nachrichten.

Für die MSLU gelten diese Einschränkungen nicht.



| `Message`              | BESCHREIBUNG                                                                                               |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| CB \_ ADDSTRING        | (b) (f) (c)                                                                                               |
| CB \_ FINDSTRING       | (b) (f) (c)                                                                                               |
| CB \_ FINDSTRINGEXACT  | (a) (f) (c)                                                                                               |
| CB \_ GETLBTEXT        | (b) (f) (c) (o) Der im *lParam-Parameter* übergebene Puffer muss über Platz für mindestens 256 Zeichen verfügen.   |
| CB \_ GETLBTEXTLEN     | (a)                                                                                                       |
| CB \_ INSERTSTRING     | (b) (f) (c)                                                                                               |
| CB \_ SELECTSTRING     | (b) (f) (c)                                                                                               |
| EM \_ CHARFROMPOS      |                                                                                                           |
| EM \_ GETLINE          | (e) Der Rückgabewert ist die Anzahl der kopierten ANSI-Zeichen.                                             |
| EM \_ GETSEL           |                                                                                                           |
| EM \_ REPLACESEL       | (b) (f)                                                                                                   |
| EM \_ SETPASSWORDCHAR  | (a)                                                                                                       |
| EM \_ SETSEL           |                                                                                                           |
| EM \_ SETWORDBREAKPROC | Diese Meldung hat keine Auswirkungen. Die Wörterbruchprozedur ist nicht festgelegt.                                          |
| LB \_ ADDSTRING        | (b) (f) (d)                                                                                               |
| LB \_ FINDSTRING       | (b) (f) (d)                                                                                               |
| LB \_ FINDSTRINGEXACT  | (b) (f) (lbs)                                                                                             |
| LB \_ GETTEXT          | (b) (f) (lbs) (o) Der im *lParam-Parameter* übergebene Puffer muss über Platz für mindestens 256 Zeichen verfügen. |
| LB \_ GETTEXTLEN       | (a)                                                                                                       |
| LB \_ INSERTSTRING     | (b) (f) (d)                                                                                               |
| LB \_ SELECTSTRING     | (b) (f) (d)                                                                                               |
| WM \_ GETTEXT          | (b) (f)                                                                                                   |
| WM \_ GETTEXTLENGTH    | (a)                                                                                                       |
| WM \_ SETTEXT          | (b) (f)                                                                                                   |
| WM \_ SETTINGCHANGE    | (a) Die Nachricht wird mit einem Timeout von drei Sekunden gesendet.                                                  |



 


-   (a) Die gemessene oder abgerufene ANSI-Zeichenfolge muss die folgende Bedingung erfüllen: Die Länge der entsprechenden Unicode-Version der Zeichenfolge darf die Länge der ANSI-Version der Zeichenfolge nicht überschreiten. Wenn diese Bedingung nicht erfüllt ist, ist die zurückgegebene Länge kurz. Wenn nicht genügend Arbeitsspeicher vorhanden ist, um die Länge der Unicode-Zeichenfolge zu bestimmen, gibt die Funktion 0 (null) zurück, nicht WIE erwartet LB \_ ERR oder CB \_ ERR.
-   (b) Wenn eine Zeichenfolgenkonvertierung erforderlich ist, werden alle Zeichenfolgen über die CP \_ ACP-Codepage konvertiert.

    Diese Funktion verwendet am besten passende Zeichen und führt keine Standardüberprüfung durch, wenn sie von Unicode in ANSI konvertiert wird. Darüber hinaus übergibt die Funktion eine NULL-Zeichenfolge an die zugrunde liegende ANSI-Funktion, wenn die Zeichenfolge nicht von Unicode in ANSI konvertiert werden kann. Dies kann beispielsweise auftreten, wenn nicht genügend Arbeitsspeicher verfügbar ist. Das Übergeben einer NULL-Zeichenfolge kann dazu führen, dass bei einigen Funktionen ein Fehler mit ungültigen Parametern auftritt. Andere Funktionen akzeptieren jedoch die NULL-Zeichenfolge und behandeln sie als den beabsichtigten Parameter. Wenn beispielsweise ein Fehler auftritt, wenn der WM SETTEXT-Wrapper versucht, den Fenstertitel in ANSI zu konvertieren, hat das Fenster eine \_ leere Beschriftung. Die Funktion benachrichtigt Sie nicht, wenn diese Probleme auftreten. Die MSLU verfügt nicht über diese Einschränkungen.

-   (c) Das angegebene Fensterhand handle muss das Handle für ein [ComboBox-](../controls/combo-boxes.md) oder [ComboBoxEx-Steuerelement](../controls/comboboxex-controls.md) sein. Wenn das Handle zu einem Kombinationsfeld-Steuerelement gehört, das owner-draw ist und nicht mit dem [Stil List Box Styles](../controls/list-box-styles.md) erstellt wurde, kann die Übersetzung dieser Meldung fehlschlagen und sogar abstürzen.
-   (d) Das angegebene Fensterhand handle muss das Handle für ein Listbox-Steuerelement sein. Wenn das Listenfeld owner-draw ist und nicht mit dem [Stil List Box Styles (Listenfeldstile)](../controls/list-box-styles.md) erstellt wurde, kann die Übersetzung dieser Nachricht fehlschlagen und sogar abstürzen.
-   (e) Wenn eine Zeichenfolgenkonvertierung erforderlich ist, werden alle Zeichenfolgen über die CP \_ ACP-Codepage konvertiert.

    Beim Konvertieren von ANSI in Unicode für die Ausgabe schneiden die Wrapperfunktionen die zurückgegebene Zeichenfolge ab, wenn sie nicht in den bereitgestellten Puffer passt. Der Rückgabewert für Funktionen, die die Anzahl der in den Puffer kopierten Zeichen zurückgeben, oder die Anzahl der Zeichen, die zur Vermeidung von Kürzungen erforderlich sind, bezieht sich auf die Anzahl der ANSI-Zeichen, die in den Puffer kopiert oder von der zugrunde liegenden ANSI-Funktion benötigt werden, und nicht auf die Anzahl der Unicode-Zeichen, die in den Puffer kopiert werden, der von der aufrufenden Anwendung bereitgestellt wird oder von der aufrufenden Anwendung benötigt wird, die die Wrapperfunktion aufgerufen hat. Die MSLU verfügt nicht über diese Einschränkung. Weitere Informationen finden Sie unter [Microsoft Layer for Unicode on Windows 95/98/Me Systems](/previous-versions/ms812865(v=msdn.10)).

### <a name="settimerqueuetimer"></a>(SetTimerQueueTimer)

Die **SHSetTimerQueueTimer-Funktion** ist etwas anders als die entsprechende [**CreateTimerQueueTimer-Funktion.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) Die Syntax ist wie folgt:

``` syntax
HANDLE SHSetTimerQueueTimer(HANDLE hQueue,
                        WAITORTIMERCALLBACK pfnCallback,
                        LPVOID pContext,
                        DWORD dwDueTime,
                        DWORD dwPeriod,
                        LPCSTR lpszLibrary,
                        DWORD dwFlags);
```

Die Parameter sollten wie folgt festgelegt werden:

-   Der *hQueue-Parameter* muss auf NULL festgelegt **werden,** und die Standard-Timerwarteschlange wird angegeben.
-   Die *Parameter pfnCallback,* *pContext,* *dwDueTime* und *dwPeriod* haben die gleiche Bedeutung wie die *Callback-,* *Parameter-,* *DueTime-* bzw. *Period-Parameter* von [**CreateTimerQueueTimer.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)
-   Der *lpszLibrary-Parameter* wird nicht verwendet und muss auf **NULL festgelegt werden.**
-   Der *Flags-Parameter* unterstützt nur eine Teilmenge der Werte, die von [**CreateTimerQueueTimer unterstützt werden.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)

    

    | Name              | Wert      | Bedeutung                         |
    |-------------------|------------|---------------------------------|
    | TPS \_ EXECUTEIO    | 0x00000001 | Identisch mit WT \_ EXECUTEINIOTHREAD   |
    | TPS \_ LONGEXECTIME | 0x00000008 | Identisch mit WT \_ EXECUTELONGFUNCTION |

    

     

    > [!Note]  
    > Das TPS \_ LONGEXECTIME-Flag hat nicht denselben numerischen Wert wie das WT \_ EXECUTELONGFUNCTION-Flag. Bei Verwendung **von SHSetTimerQueueTimer** muss der *dwFlags-Parameter* eine Kombination aus TPS-Werten \_ \* und nicht aus WT-Werten \_ \* sein.

     

**SHSetTimerQueueTimer** gibt das Handle des erstellten Timers bei Erfolg und **andernfalls NULL** zurück.

### <a name="shellexecuteex"></a>(ShellExecuteEx)

Der **lpFile-Member** der [**SHELLEXECUTEINFO-Struktur,**](/windows/win32/api/Shellapi/ns-shellapi-shellexecuteinfoa) der im einzigen Parameter dieser Funktion übergeben wird, darf internet \_ max URL \_ \_ LENGTH-Zeichen nicht überschreiten. Wenn das FLAG SEE \_ MASK \_ CLASSNAME weggelassen wird, muss der **lpClass-Member** mit NULL initialisiert **werden.**

### <a name="valueex"></a>(ValueEx)

Es werden nur die folgenden Registrierungsdatentypen unterstützt: REG \_ SZ, REG \_ EXPAND \_ SZ, REG \_ BINARY und REG \_ DWORD. Im Gegensatz zu diesen Wrapperfunktionen unterstützt MSLU auch REG \_ MULTI \_ EXPAND \_ SZ.

### <a name="windowlong"></a>(WindowLong)

Auf nativen ANSI-Plattformen führt die Funktion keine Übersetzung für eine der Fenster-Longs durch. Wenn Sie beispielsweise GWLP WNDPROC übergeben, gibt die Funktion die \_ PROZEDUR DES ANSI-Fensters und keinen Thunk zurück. Die MSLU verfügt nicht über diese Einschränkungen.

 

 
