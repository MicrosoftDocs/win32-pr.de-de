---
description: In den Tabellen in diesem Dokument sind Wrapper Funktionen von Shlwapi.dll aufgelistet, die eingeschränkte Unicode-Funktionen für Windows 95, Windows 98 und Windows Millennium Edition (Windows Me) bereitstellen.
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
ms.openlocfilehash: 52e3a5b60a331a74ced1888d5a196348497c5ff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757717"
---
# <a name="shlwapi-wrapper-functions"></a>SHLWAPI-Wrapper-Funktionen

\[Diese Funktionen sind über Windows XP Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie werden möglicherweise in nachfolgenden Versionen von Windows geändert oder sind nicht verfügbar.\]

In den Tabellen in diesem Dokument sind Wrapper Funktionen von Shlwapi.dll aufgelistet, die eingeschränkte Unicode-Funktionen für Windows 95, Windows 98 und Windows Millennium Edition (Windows Me) bereitstellen.

Windows 95, Windows 98 und Windows Millennium Edition (Windows Me) werden hier als "Native ANSI-Plattformen" bezeichnet. Auf nativen ANSI-Plattformen konvertieren diese Wrapper Funktionen die Unicode-Eingabe Zeichenfolgen-Parameter in ANSI und geben ANSI-Versionen von Funktionen in der weitergeleiteten Spalte **an** . Beispielsweise ruft **appendmenuwrapw** **appendmenua** auf, d. h. die ANSI-Version von [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). Die anderen Funktionen folgen dem gleichen Muster. Alle von der ANSI-Funktion zurückgegebenen Zeichen folgen werden in Unicode konvertiert und an die aufrufenden Anwendung zurückgegeben. Abgesehen von den in der Spalte " **Hinweise** " notierten Ausnahmen hat die Wrapper Funktion dieselbe Syntax und bietet die gleiche Funktionalität wie die Funktion in der **Weiterleitung an** -Spalte. Ausführliche Informationen zur Verwendung finden Sie auf dieser Referenzseite.

**Sicherheitswarnung:** Mehrere Unicode-Zeichen folgen können in dieselbe ANSI-Zeichenfolge konvertiert werden. Unerwartete Konflikte nach der Konvertierung können zu unerwartetem Verhalten führen. Wenn z. b. mithilfe von "-" "" "" "mit" "" "" mit "" "" mit dem ersten-Befehl ein Handle für dasselbe Ereignis wie der erste-Befehl **erstellt wird,** gibt der zweite-Befehl ein Handle für dasselbe Ereignis zurück, auch wenn sich die ursprünglichen Unicode-Zeichen folgen unterscheiden.

Microsoft Windows NT, Windows 2000, Windows XP, Windows Server 2003 und spätere Betriebssysteme werden als "Native Unicode-Plattformen" bezeichnet. Zum größten Teil leiten diese Wrapper Funktionen auf nativen Unicode-Plattformen einfach Eingabe Zeichenfolgen-Parameter an die Unicode-Version der-Funktion in **der weitergeleiteten-Spalte weiter** . Beispielsweise leitet **appendmenuwrapw** an **appendmenuw** weiter. Dies ist die Unicode-Version von [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). Die anderen Funktionen folgen dem gleichen Muster. Alle Zeichen folgen, die von der Unicode-Funktion zurückgegeben werden, werden an die aufrufenden Anwendung zurückgegeben. Abgesehen von den in der Spalte " **Hinweise** " notierten Ausnahmen hat die Wrapper Funktion dieselbe Syntax und bietet die gleiche Funktionalität wie die Funktion in der **Weiterleitung an** -Spalte. Ausführliche Informationen zur Verwendung finden Sie auf dieser Referenzseite.

**Sicherheitswarnung:** Die Sicherheitsprobleme, die für die Funktionen in der **weiter** geleiteten Spalte angegeben werden, gelten auch für die entsprechenden Wrapper Funktionen. Weitere Informationen finden Sie in der Referenz Dokumentation für die-Funktion in der **Weiterleitung an** -Spalte.

Die Wrapper Funktionen in dieser Tabelle sind alle in Shlwapi.dll enthalten. Um Sie aufzurufen, müssen Sie die in der Tabelle aufgeführte Ordinalzahl verwenden.

> [!Note]  
> Diese Wrapper Funktionen sind unter Windows XP verfügbar, bieten aber keine Wrapper Funktionen in Windows XP Service Pack 2 (SP2) und höher. Außerdem bieten Sie keine Wrapper Funktionen in Windows Server 2003. Verwenden Sie stattdessen die Funktionen, die in der **Weiterleitung zu** -Spalte aufgeführt sind.

 



| Funktion                  | Ordinal | Weiterleiten an                                             | DLL      | Bemerkungen                                                                                                                             |
|---------------------------|---------|---------------------------------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| Appendmenuwrapw           | 36      | [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)                     | User32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(Menü)](#menu)                                                           |
| Callwindowprocwrapw       | 37      | [**Callwindowproc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)             | User32   | [Ich](#shlwapi-wrapper-functions)                                                                                                   |
| Charlowerwrapw            | 38      | [**Charlower**](/windows/win32/api/winuser/nf-winuser-charlowera)                       | Kernel32 | [Fresser](#shlwapi-wrapper-functions)                                                                                                   |
| Charupperbubwrapw         | 44      | [**Charupperbuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)               | Kernel32 | [Fresser](#shlwapi-wrapper-functions)                                                                                                   |
| Charupperwrapw            | 43      | [**Charupper**](/windows/win32/api/winuser/nf-winuser-charuppera)                       | Kernel32 | [Fresser](#shlwapi-wrapper-functions)                                                                                                   |
| Comparestringwrapw        | 45      | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                 | Kernel32 | [CompareString](#comparestring)                                                                                                   |
| Copyfilewrapw             | 112     | [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile)                             | Kernel32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| "Kreateeventwrapw"          | 51      | [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)                     | Kernel32 | [ein](#shlwapi-wrapper-functions)                                                                                                   |
| "Kreatefilewrapw"           | 52      | [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)                         | Kernel32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| "Kreatewindowexwrapw"       | 55      | [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)             | User32   | [ein](#shlwapi-wrapper-functions)                                                                                                   |
| Defwindowprocwrapw        | 56      | [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)               | User32   | [Ich](#shlwapi-wrapper-functions)                                                                                                   |
| Deletefilewrapw           | 57      | [**DeleteFile**](/windows/win32/api/fileapi/nf-fileapi-deletefilea)                         | Kernel32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| Dialogboxparamwrapw       | 59      | [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama)             | User32   | [(f)](#dragqueryfile), [(i)](#shlwapi-wrapper-functions), [(DialogBoxParam)](#dialogboxparam)                                       |
| Dispatchmessagewrapw      | 60      | [**DispatchMessage gesendet**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)           | User32   | [Ich](#shlwapi-wrapper-functions)                                                                                                   |
| Dragqueryfilewrapw        | 318     | [**Dragqueryfile**](/windows/win32/api/Shellapi/nf-shellapi-dragqueryfilea)                  | Shell32  | [(b)](#dialogboxparam), [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(dragqueryfile)](#dragqueryfile)               |
| Drawtextexwrapw           | 301     | [**Drawtextex**](/windows/win32/api/winuser/nf-winuser-drawtextexa)                        | User32   | [(a)](#shlwapi-wrapper-functions), [(d)](#shlwapi-wrapper-functions)                                                                |
| Drawtextwrapw             | 61      | [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)                            | User32   | [ein](#shlwapi-wrapper-functions)                                                                                                   |
| Exttextoutwrapw           | 299     | [**Exttextout**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)                        | GDI32    | [(d)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(exttextout)](#exttextout)                                               |
| Formatmessagewrapw        | 68      | [**Format Message**](/windows/win32/api/winbase/nf-winbase-formatmessage)                 | Kernel32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(FormatMessage)](#formatmessage)                                       |
| Getclassinfowrapw         | 69      | [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa)                 | User32   | [GetClassInfo](#getclassinfo)                                                                                                     |
| Getdateformatwrapw        | 311     | [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)                 | Kernel32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| Getdlgitemtextwrapw       | 74      | [**Getdlgitemtext**](/windows/win32/api/winuser/nf-winuser-getdlgitemtexta)             | User32   | [selbst](#compareexchange)                                                                                                             |
| Getfileattributeswrapw    | 75      | [**GetFileAttributes**](/windows/win32/api/fileapi/nf-fileapi-getfileattributesa)           | Kernel32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| Getlocaleingefowrapw        | 77      | [**Getlocaleingefo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)                 | Kernel32 | [selbst](#compareexchange)                                                                                                             |
| Getmenuiteminfowrapw      | 302     | [**Getmenuiteminfo**](/windows/win32/api/winuser/nf-winuser-getmenuiteminfoa)           | User32   | [(f)](#dragqueryfile), [(g)](#compareexchange), [(menuiteminfo)](#menuiteminfo)                                                     |
| Getmoduledateinamewrapw    | 80      | [**Fehler bei GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)         | Kernel32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| Getmodulelenker wrapw      | 83      | [**Fehler bei GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)             | Kernel32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| Getobjectwrapw            | 84      | [**GetObject**](/windows/win32/api/wingdi/nf-wingdi-getobject)                          | GDI32    | [selbst](#compareexchange)                                                                                                             |
| Getopendatamewrapw      | 403     | [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea)           | Comdlg32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OpenFileName)](#openfilename)                 |
| Getsavedateinamewrapw      | 389     | [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)           | Comdlg32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OpenFileName)](#openfilename)                 |
| Getsystemdirectoriywrapw   | 81      | [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)       | Kernel32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| Gettimeformatwrapw        | 310     | [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)                 | Kernel32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| Getwindowlongwrapw        | 94      | [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)               | User32   | [(Windowlong)](#windowlong)                                                                                                         |
| Getwindowsdirectoriywrapw  | 97      | [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)     | Kernel32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| Getwindowtextverlängert wrapw  | 96      | [**Getwindowtextlength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)   | User32   | [IStGH](#j)                                                                                                                           |
| Getwindowtextwrapw        | 95      | [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)               | User32   | [(f)](#dragqueryfile), [(g)](#compareexchange)                                                                                      |
| Insertmenuitemwrapw       | 98      | [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema)             | User32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(Menü)](#menu), [(menuiteminfo)](#menuiteminfo)                          |
| Ischaralphawrapw          | 25      | [**Ischaralpha**](/windows/win32/api/winuser/nf-winuser-ischaralphaa)                   | User32   | [Fresser](#shlwapi-wrapper-functions)                                                                                                   |
| Ischaralpha anumschlag wrapw   | 28      | [**Ischaralpha numerisch**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)     | Kernel32 | [Fresser](#shlwapi-wrapper-functions)                                                                                                   |
| Ischarupperwrapw          | 26      | [**Ischarupper**](/windows/win32/api/winuser/nf-winuser-ischaruppera)                   | User32   | [Fresser](#shlwapi-wrapper-functions)                                                                                                   |
| Loadlibrarywrapw          | 105     | [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                     | Kernel32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| Loadstringwrapw           | 107     | [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)                     | Kernel32 | [Fresser](#shlwapi-wrapper-functions)                                                                                                   |
| Messageboxwrapw           | 340     | [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox)                     | User32   | [ein](#shlwapi-wrapper-functions)                                                                                                   |
| "Muvefilewrapw"             | 113     | [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)                             | Kernel32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| Outputdebug-stringwrapw    | 115     | [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)         | Kernel32 | [ein](#shlwapi-wrapper-functions)                                                                                                   |
| Peekmessagewrapw          | 116     | [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)                   | User32   | [(Peer Message und PostMessage)](#peekmessage-and-postmessage)                                                                       |
| Postmessagewrapw          | 117     | [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)                   | User32   | [(Peer Message und PostMessage)](#peekmessage-and-postmessage)                                                                       |
| Regkreatekeyexwrapw       | 120     | [**Regkreatekeyex**](/windows/win32/api/winreg/nf-winreg-regcreatekeyexa)               | Advapi32 | [ein](#shlwapi-wrapper-functions)                                                                                                   |
| Registerclasswrapw        | 131     | [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)               | User32   | [(a)](#shlwapi-wrapper-functions), [(registerClass)](#registerclass)                                                                |
| Regopenkeyexwrapw         | 125     | [**Fehler bei RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)                   | Advapi32 | [ein](#shlwapi-wrapper-functions)                                                                                                   |
| Regqueryvalueexwrapw      | 128     | [**Fehler bei RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa)             | Advapi32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(valueex)](#regqueryvalueexw), [(regqueryvalueexw)](#regqueryvalueexw) |
| Regqueryvaluewrapw        | 127     | [**RegQueryValue**](/windows/win32/api/winreg/nf-winreg-regqueryvaluea)                 | Advapi32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| Regsetvalueexwrapw        | 130     | [**Fehler bei RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvalueexa)                 | Advapi32 | [(a)](#shlwapi-wrapper-functions), [(valueex)](#regqueryvalueexw)                                                                   |
| Sendmessagewrapw          | 136     | [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)                   | User32   | [SendMessage](#sendmessage)                                                                                                       |
| Setdlgitemtextwrapw       | 138     | [**SetDlgItemText**](/windows/win32/api/winuser/nf-winuser-setdlgitemtexta)             | User32   | [ein](#shlwapi-wrapper-functions)                                                                                                   |
| Setwindowlongwrapw        | 141     | [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)               | User32   | [(Windowlong)](#windowlong)                                                                                                         |
| Setwindowtextwrapw        | 143     | [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)               | User32   | [ein](#shlwapi-wrapper-functions)                                                                                                   |
| Shellexecuteexwrapw       | 35      | [**ShellExecuteEx**](/windows/win32/api/Shellapi/nf-shellapi-shellexecuteexa)                | Shell32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(ShellExecuteEx)](#shellexecuteex)                                      |
| Shellmessageboxwrapw      | 388     | [**Shellmessagebox**](/windows/win32/api/Shellapi/nf-shellapi-shellmessageboxa)              | Shlwapi  | [(a)](#shlwapi-wrapper-functions), [(FormatMessage)](#formatmessage)                                                                |
| Shgetfileingefowrapw        | 313     | [**Shgetfileingefo**](/windows/win32/api/Shellapi/nf-shellapi-shgetfileinfoa)                  | Shell32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange)                                                  |
| Shgetpathfroconlistwrapw  | 334     | [**Shgetpathfromittlerlist**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista)      | User32   | [selbst](#compareexchange)                                                                                                             |
| Translateacceleratorwrapw | 146     | [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) | User32   | [Ich](#shlwapi-wrapper-functions)                                                                                                   |
| Unregisterclasswrapw      | 147     | [**Unregisterclass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)           | User32   | [ein](#shlwapi-wrapper-functions)                                                                                                   |



 

Die Wrapper Funktionen in der folgenden Tabelle führen keine Zeichensatz Konvertierung aus. Stattdessen bieten Sie eingeschränkte Unterstützung für Betriebssystemfunktionen, die auf früheren Plattformen nicht verfügbar sind.



| Funktion                     | Ordinal | Weiterleiten an                                                                     | DLL      | Bemerkungen                                                                        |
|------------------------------|---------|---------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------|
| Mlgetuilanguage              | 376     | [**GetUserDefaultUILanguage**](/windows/win32/api/winnls/nf-winnls-getuserdefaultuilanguage)                   | Kernel32 | [Micha](#shlwapi-wrapper-functions)                                              |
| Shcanceltimerqueuetimer      | 265     | [**' Deletetimerqueuetimer '**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer)                         | Kernel32 | [Micha](#shlwapi-wrapper-functions)                                              |
| Shdeletetimerqueue           | 262     | [**' Deletetimerqueue '**](/windows/win32/api/winbase/nf-winbase-deletetimerqueue)                                   | Kernel32 | [Micha](#shlwapi-wrapper-functions)                                              |
| Shinterlockedcompareexchange | 342     | [**Interlockedcompareexchangepointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) | Kernel32 | [CompareExchange](#compareexchange)                                          |
| Shqueueuserworkitem          | 260     | [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                                 | Kernel32 | [(QueueUserWorkItem)](#queueuserworkitem), [(h)](#shlwapi-wrapper-functions)   |
| SH-ttimerqueuetimer         | 263     | [**' CreateTimerQueueTimer '**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)                         | Kernel32 | [(](#settimerqueuetimer)"*"), [(H)](#shlwapi-wrapper-functions) |



 

## <a name="remarks"></a>Bemerkungen

### <a name="a"></a>ein

Wenn eine Zeichen folgen Konvertierung erforderlich ist, werden alle Zeichen folgen über die \_ ACP ACP-Codepage konvertiert.

Diese Funktionen verwenden am besten geeignete Zeichen und führen keine Standardüberprüfung durch, wenn Sie von Unicode in ANSI-Zeichen Konvertierungen durchführen. Wenn die Zeichenfolge nicht von Unicode in ANSI konvertiert werden kann, übergibt die Wrapper Funktion außerdem eine **null** -Zeichenfolge an die zugrunde liegende ANSI-Funktion. Dies kann z. b. vorkommen, wenn nicht genügend Arbeitsspeicher vorhanden ist. Das übergeben einer **null** -Zeichenfolge kann dazu führen, dass einige Funktionen mit einem ungültigen Parameter Fehler fehlschlagen. andere Funktionen akzeptieren jedoch die **null** -Zeichenfolge und behandeln Sie als beabsichtigten Parameter. Ein Fehler tritt z. b. auf, wenn die Funktion "up- **windowexwrapw** " versucht, den *lpWindowName* -Parameter in ANSI zu konvertieren, und " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " ein Fenster mit einer leeren Beschriftung erstellt. Der Wrapper benachrichtigt Sie nicht, wenn diese Probleme aufgetreten sind.

Die Microsoft-Schicht für Unicode (MSLU) prüft bei der Konvertierung von Unicode in ANSI auf Fehler und gibt entsprechende Fehler Werte zurück. Die [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) -Wrapper Funktion in MSLU gibt beispielsweise 0 zurück, wenn das Element nicht erfolgreich angefügt wurde.

### <a name="b"></a>b

Diese Funktionen verwenden einen verzögerten geladenen Link zur entsprechenden Funktion. Dies bedeutet, dass die dll, die die Funktion in der Spalte "Weiterleiten" enthält, nicht vom Shlwapi.dll geladen wird, bis eine Funktion in dieser DLL aufgerufen wird. Der Microsoft Visual C++ Linker unterstützt diese Funktion in der Regel über die/DELAYLOAD-Option.

### <a name="c"></a>scher

Diese Funktion manipuliert Dateinamen. Wie in [(a)](#shlwapi-wrapper-functions)angemerkt, konvertieren die-Funktionen alle Zeichen folgen über die CP \_ ACP-Codepage. Sie prüfen nicht, ob die Datei-e/a-Funktionen auf den ANSI-Modus festgelegt wurden. Wenn sich die Datei-e/a-Funktionen im OEM-Modus befinden, werden die Zeichen folgen in und aus dem falschen Zeichensatz konvertiert. Eine Anwendung kann die Datei-e/a-Funktionen explizit auf den OEM-Modus festlegen, indem Sie die [**setfileapistooem**](/windows/win32/api/fileapi/nf-fileapi-setfileapistooem) -Funktion aufruft.

* * Sicherheitswarnung: * * Verwenden Sie diese Wrapper Funktionen für Dateinamen, um die Sicherheit Ihrer Anwendung zu beeinträchtigen. Da keine Standardüberprüfung durchgeführt wird und die Zeichen mit den besten Zeichen verwendet werden, können Dateinamen Zeichen auf unerwartete Weise konvertiert werden. Dies kann zu Spoofingangriffen des Dateisystems führen. Außerdem kann es während der Konvertierung von Unicode in ANSI zu einem unbeaufsichtigten Datenverlust kommen.

Die MSLU verfügt nicht über diese Einschränkungen.

### <a name="d"></a>d

Wenn die Zeichenfolge, die gezeichnet wird, einen Zeichensatz erfordert, der in der im Gerätekontext ausgewählten Schriftart nicht verfügbar ist, verwenden diese Wrapper Funktionen die [Schriftart Verknüpfungs](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767872(v=vs.85)) Funktion der [MLang](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767865(v=vs.85)) -Bibliothek, um die einzelnen Zeichen in einer entsprechenden Schriftart zu erzeugen. Im Gegensatz zu den meisten anderen Wrapper Funktionen sind diese neben den nativen ANSI-Plattformen auch unter Microsoft Windows NT 4,0 funktionsfähig.

### <a name="e"></a>Fresser

Vollständige Unicode-Implementierungen dieser Funktionen sind auf nativen ANSI-Plattformen verfügbar. Diese Funktionen nennen die zugehörige ANSI-Funktion nicht.

### <a name="f"></a>c

Wenn die Benutzer-Standardbenutzer Oberflächen Sprache einen anderen Zeichensatz als die Standardbenutzer Oberflächen Sprache des Systems verwendet, versucht das System, Dialog Vorlagen und Unterklassen-Steuerelemente umzuschreiben und Menü Elemente in "Besitzer zeichnen" zu konvertieren, damit Zeichen folgen in der Benutzeroberfläche der Benutzeroberflächen Sprache weiterhin ordnungsgemäß angezeigt werden. Die einzigen Steuerelemente, die von den Dialogfeld Vorlagen-Umschreib Regeln unterstützt werden, sind die Steuerelemente static, Button, ListBox und ComboBox Diese Steuerelemente werden untergeordnet, sodass die **sendmessagewrapw** -Funktion die ursprüngliche Unicode-Zeichenfolge abrufen kann, ohne dass Sie durch den ANSI-Zeichensatz übersetzt wird. Im Gegensatz zu den meisten anderen Wrapper Funktionen sind diese sowohl auf Microsoft Windows NT 4,0 als auch auf systemeigenen ANSI-Plattformen funktionsfähig. In den Hinweisen in der Dokumentation der [**mlloadlibrary**](./callbacks.md) -Funktion finden Sie weitere Informationen dazu, wie die Benutzeroberfläche der Benutzeroberfläche und die Benutzeroberflächen Sprache des Systems festgelegt wird.

### <a name="g"></a>selbst

Wenn eine Zeichen folgen Konvertierung erforderlich ist, werden alle Zeichen folgen über die \_ ACP ACP-Codepage konvertiert.

Wenn die zurückgegebene Zeichenfolge nicht in den Puffer passt, der bereitgestellt wurde, schneidet die Wrapper Funktion die Zeichenfolge ab, wenn Sie für die Ausgabe von ANSI in Unicode umschließt. Die Funktionen, die die Anzahl der Zeichen zurückgeben, die in den Puffer kopiert werden, oder die Anzahl der Zeichen, die zur Vermeidung von Abschneiden erforderlich sind, geben nicht die Anzahl der Unicode-Zeichen zurück Sie geben die Anzahl der ANSI-Zeichen zurück, die in den Puffer kopiert oder von der zugrunde liegenden ANSI-Funktion benötigt werden. Die MSLU verfügt nicht über diese Einschränkungen.

### <a name="h"></a>Micha

Auf Systemen vor Windows XP implementieren diese Funktionen einen vereinfachten Thread Pool und eine Zeit Geber Warteschlange. Unter Windows XP und höher verwenden diese Funktionen den System Thread Pool und die Zeit Geber Warteschlange des Systems. Für die Funktionen der Timer-Warteschlange muss der *hqueue* -Parameter auf **null** festgelegt werden, um anzugeben, dass der Vorgang für die Standardzeit Geber Warteschlange ausgeführt werden soll.

### <a name="i"></a>Ich

Auf Unicode-Plattformen übersetzen diese Funktionen die Nachricht von Unicode in ANSI, wenn das Zielfenster ANSI ist. Diese Funktionen führen keine Nachrichten Übersetzung auf systemeigenen ANSI-Plattformen aus. Daher müssen aufrufenden Anwendungen, die diese Funktion aufrufen, sicherstellen, dass die Nachricht im Unicode-Format auf Unicode-Plattformen und ANSI-Format auf ANSI-Plattformen vorliegt Beispielsweise muss der *wParam* -Parameter im folgenden Funktions Aufrufpunkt ein Unicode-Codepunkt sein, wenn das Programm auf einer Unicode-Plattform ausgeführt wird und ein ANSI-Zeichen sein muss, wenn das Programm auf einer ANSI-Plattform ausgeführt wird.

``` syntax
CallWindowProcWrapW(prevWndProc, hwnd, WM_CHAR, wParam, lParam);
```

MSLU verfolgt den Zeichensatz der Zielfenster Prozedur und konvertiert die Nachricht bei Bedarf.

### <a name="j"></a>IStGH

Auf ANSI-Plattformen geben diese Funktionen die Länge der zugrunde liegenden ANSI-Zeichenfolge zurück, nicht die Länge der übersetzten Unicode-Zeichenfolge. Die MSLU verfügt nicht über diese Einschränkungen.

### <a name="compareexchange"></a>CompareExchange

Die Syntax für " **shinterlockedcompareexchange** " unterscheidet sich etwas von " [**interlockedcompareexchangepointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer)", aber Sie funktioniert identisch.

``` syntax
void* SHInterlockedCompareExchange(void **ppDest, void *pExch, void *pComp);
```

### <a name="comparestring"></a>CompareString

Beachten Sie, dass beide Zeichen folgen auf nativen ANSI-Plattformen in ANSI konvertiert und als ANSI-Zeichen folgen verglichen werden. Wenn die Unicode-Zeichen folgen Zeichen enthalten, die in ANSI nicht dargestellt werden können, sind die Ergebnisse möglicherweise unerwartet. Wenn z. b. die Standard-ANSI-Codepage keine CJK-Zeichen unterstützt, werden die Zeichen folgen L " \\ x66F0" und L " \\ x6708" als gleich auf nativen ANSI-Plattformen verglichen, da beide der ANSI-Zeichenfolge "?" zugeordnet sind.

### <a name="datetime"></a>DateTime

Auf Shlwapi.dll Version 5,0, die mit Windows 2000 ausgeliefert wurde, muss die Codepage des Gebiets Schema Bezeichners, den Sie als ersten Parameter von **getdateformatwrapw** und **gettimeformatwrapw** übergeben, mit der aktuellen ANSI-Codepage identisch sein. Andernfalls kann die zurückgegebene Zeichenfolge falsch konvertiert werden. Diese Einschränkung gilt nicht für Shlwapi.dll Versionen 5,5 oder höher. Dies bedeutet, dass Windows XP und spätere Systeme diese Einschränkung nicht unterliegen. Die MSLU weist diese Einschränkung nicht auf.

### <a name="dialogboxparam"></a>(DialogBoxParam)

Der *lptemplatename* -Parameter für die **dialogboxparamwrapw** -Funktion darf keine Zeichenfolge sein. Dabei muss es sich um eine Ordinalzahl handeln, die vom [**makeintresource**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) -Makro erstellt wurde. Die durch den *lpdialogfunc* -Parameter angegebene Dialog Prozedur empfängt ANSI-Nachrichten auf systemeigenen ANSI-Plattformen und Unicode-Nachrichten auf nativen Unicode-Plattformen Die Dialogfeld Prozedur muss darauf vorbereitet sein, beide Fälle zu verarbeiten. Die MSLU verfügt nicht über diese Einschränkungen.

### <a name="exttextout"></a>(Exttextout)

Native ANSI-Plattformen implementieren sowohl die Funktion [**exttextoutw**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) als auch Native Unicode-Plattformen. **Exttextoutwrapw** dient zum Durchführen von Schriftart Verknüpfungen, wie in einer separaten Anmerkung beschrieben.

### <a name="dragqueryfile"></a>(Dragqueryfile)

Mit der **dragqueryfilewrapw** -Funktion können Sie die Länge einer Datei im Drop-Handle nicht Abfragen, indem Sie **null** als *lpszfile* -Parameter übergeben. Die MSLU verfügt nicht über diese Einschränkungen.

### <a name="formatmessage"></a>Format Message

Auf nativen ANSI-Plattformen werden die Formate in der Zeichenfolge nicht von Unicode in ANSI konvertiert. Das folgende Codebeispiel ist z. b. fehlerhaft.


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



In diesem Codebeispiel wird "! s!" verwendet. akzeptiert. Auf nativen ANSI-Plattformen wird diese Zeichenfolge an die ANSI-Version der [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion weitergegeben. Folglich wird anstelle einer Unicode-Zeichenfolge eine ANSI-Zeichenfolge erwartet. Entsprechend impliziert das Format "%2" ein Zeichen folgen Argument. Wenn Sie an die ANSI **FormatMessage** -Funktion weitergegeben wird, wird Sie als ANSI-Zeichenfolge und nicht als Unicode-Zeichenfolge interpretiert. Die richtige Format Zeichenfolge ist L "%1! WS! %2! WS! ". Dadurch werden Zeichen folgen auf ANSI-und Unicode-Plattformen ordnungsgemäß gedruckt.

Die Funktion unterstützt "%0" nicht. spezielle Format Zeichenfolge.

Die MSLU verfügt nicht über diese Einschränkungen.

### <a name="getclassinfo"></a>GetClassInfo

Auf nativen ANSI-Plattformen werden die Member **lpszmenuname** und **lpszClassName** der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur nicht in Unicode übersetzt und sind immer auf **null** festgelegt. Außerdem wird die im **lpfnwndproc** -Member der **WNDCLASS** -Struktur zurückgegebene Fenster Prozedur nicht in Unicode übersetzt und verweist auf eine ANSI-Fenster Prozedur. Die MSLU verfügt nicht über diese Einschränkungen.

### <a name="menu"></a>Stehen

Auf Shlwapi.dll Version 5,0, die mit Windows 2000 ausgeliefert wird, werden Menü Element Zeichenfolgen, die Tabstopp Zeichen ( \\ t) enthalten, möglicherweise nicht ordnungsgemäß angezeigt. Diese Einschränkung gilt nicht für Shlwapi.dll Versionen 5,5 oder höher. Dies bedeutet, dass Windows XP und spätere Systeme diese Einschränkung nicht unterliegen. Die MSLU weist diese Einschränkung nicht auf.

### <a name="menuiteminfo"></a>Menuiteminfo zuordnet

Diese Funktion unterstützt nur die Microsoft Windows NT 4,0-Version der [**menuiteminfow**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur. In dieser Struktur fehlt ein **hbmpitem** -Member. Außerdem unterstützt die Funktion das miim- \_ bitmapflag nicht. Die MSLU verfügt nicht über diese Einschränkungen.

### <a name="openfilename"></a>OpenFileName

Der **CBSIZE** -Member der [**opendatamew**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur muss auf sizeof (OpenFileName NT4W) festgelegt werden \_ .

Der **lpstraucustomfilter** -Member der [**opendatamew**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur muss auf **null** festgelegt werden.

Die Werte der **nmaxfile** -und **nmaxfiletitle** -Elemente der [**openfileamew**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur dürfen den maximalen Pfad nicht überschreiten \_ .

Wenn der **lpfnhook** -Member der [**OpenFile**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) Name-Struktur nicht **null** ist, muss er auf eine ANSI-Hook-Prozedur auf systemeigenen ANSI-Plattformen und eine Unicode-Hook-Prozedur auf nativen Unicode-Plattformen verweisen.

Die MSLU verfügt nicht über diese Einschränkungen.

### <a name="peekmessage-and-postmessage"></a>(Peer Message und PostMessage)

Auf nativen ANSI-Plattformen wird keine Übersetzung der übertragenen oder abgerufenen Nachricht durchgeführt. Die übertragene/abgerufene Nachricht ist ANSI auf systemeigenen ANSI-Plattformen und Unicode auf nativen Unicode-Plattformen Die aufrufende Anwendung muss darauf vorbereitet sein, beide Fälle zu verarbeiten. Wenn die abgerufene Nachricht z. b. WM \_ char lautet, ist *wParam* ein ANSI-Zeichencode auf nativen ANSI-Plattformen, aber es handelt sich um einen Unicode-Codepunkt auf nativen Unicode-Plattformen. Die MSLU verfügt nicht über diese Einschränkungen.

### <a name="queueuserworkitem"></a>QueueUserWorkItem

Die **shqueueuserworkitem** -Funktion unterscheidet sich geringfügig von der entsprechenden [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) -Funktion. Die Syntax für **shqueueuserworkitem** wird hier dargestellt.

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

-   Die Parameter " *pfncallback* " und " *pContext* " haben dieselbe Bedeutung wie die *Funktions* -und *Kontext* Parameter von [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem).
-   Der *dwtag* -Parameter wird nicht verwendet und muss auf 0 (null) festgelegt werden.
-   Der *pdwld* -Parameter wird nicht verwendet und muss auf **null** festgelegt werden.
-   Der *pszmodule* -Parameter verweist auf eine optionale, mit NULL endende ANSI-Zeichenfolge, die den Namen einer Bibliothek angibt, die vor dem Abschluss der Arbeitsaufgabe geladen und entladen werden soll. Dieser Parameter kann **NULL** sein.
-   Der *dwFlags* -Parameter unterstützt nur eine Teilmenge der Werte, die von [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)unterstützt werden. Die folgenden Flags werden erkannt.

    

    | Name              | Wert      | Bedeutung                          |
    |-------------------|------------|----------------------------------|
    | TPS \_ executeio    | 0x00000001 | Identisch mit dem WT \_ executeiniothread.   |
    | TPS- \_ Zeit (longexectime) | 0x00000008 | Identisch mit der "WT \_ executgestreckt"-Funktion. |

    

     

    > [!Note]  
    > Das TPS- \_ Flag "longexectime" hat nicht denselben numerischen Wert wie das "WT \_ executlänfunction"-Flag. Wenn Sie **shqueueuserworkitem** verwenden, muss der dwFlags-Parameter eine Kombination von TPS- \_ \* Werten, nicht von WT- \_ \* Werten sein.

     

**Shqueueuserworkitem** gibt einen Wert ungleich 0 (null) zurück, wenn das Arbeits Element erfolgreich in die Warteschlange eingereiht wurde, andernfalls 0. Wenn die Funktion fehlschlägt, können Sie " [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) " verwenden, um zusätzliche Informationen zu erhalten.

### <a name="registerclass"></a>RegisterClass

Auf nativen ANSI-Plattformen wird keine Übersetzung für den **lpfnwndproc** -Member der [**wndclassw**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur ausgeführt. Das Fenster empfängt ANSI-Fenster Meldungen auf nativen ANSI-Plattformen und Unicode-Fenster Meldungen auf systemeigenen Unicode-Plattformen. Die Fenster Prozedur muss darauf vorbereitet sein, beide Fälle zu verarbeiten. Die MSLU verfügt nicht über diese Einschränkungen.

### <a name="regqueryvalueexw"></a>(Regqueryvalueexw)

**Regqueryvalueexwrapw** wurde auch unter dem Namen " **regqueryvalueexw**" aufgerufen. Wie bei allen unbenannten Funktionen, die streng durch Ordinal exportiert werden, können Sie den Namen, den die Funktion kennt, in Ihrem Code auswählen.

### <a name="sendmessage"></a>SendMessage

Auf nativen Unicode-Plattformen leitet die **sendmessagewrapw** -Funktion an die [**sendmessagew**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion weiter. Auf nativen ANSI-Plattformen bietet **sendmessagewrapw** eingeschränkte Unterstützung für das Übersetzen von Unicode-Nachrichten in ANSI. Die Liste der unterstützten Meldungen finden Sie in der folgenden Tabelle. Die Funktion übersetzt keine anderen Nachrichten.

Die MSLU verfügt nicht über diese Einschränkungen.



|                      |                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| CB \_ AddString        | (b) (f) (c)                                                                                               |
| CB- \_ FindString       | (b) (f) (c)                                                                                               |
| CB- \_ FindStringExact  | (a) (f) (c)                                                                                               |
| CB \_ getlbtext        | (b) (f) (c) (o) der Puffer, der im *LPARAM* -Parameter übergeben wird, muss Platz für mindestens 256 Zeichen aufweisen.   |
| CB \_ getlbtextlen     | ein                                                                                                       |
| CB \_ InsertString     | (b) (f) (c)                                                                                               |
| CB- \_ SelectString     | (b) (f) (c)                                                                                               |
| EM \_ charfrompos      |                                                                                                           |
| EM \_ getline          | (e) der Rückgabewert ist die Anzahl der kopierten ANSI-Zeichen.                                             |
| EM- \_ GetSEL           |                                                                                                           |
| EM \_ replacesel       | (b) (f)                                                                                                   |
| EM \_ setpasswordchar  | ein                                                                                                       |
| EM- \_ tsel           |                                                                                                           |
| EM \_ setwordbreakproc | Diese Nachricht hat keine Auswirkung. Die Prozedur für die Wort Umbruch ist nicht festgelegt.                                          |
| LB- \_ AddString        | (b) (f) (d)                                                                                               |
| LB- \_ FindString       | (b) (f) (d)                                                                                               |
| LB- \_ FindStringExact  | (b) (f) (lbs)                                                                                             |
| LB- \_ gettext          | (b) (f) (lbs) (o) der Puffer, der im *LPARAM* -Parameter übergeben wird, muss Platz für mindestens 256 Zeichen aufweisen. |
| LB- \_ gettextlen       | ein                                                                                                       |
| LB- \_ InsertString     | (b) (f) (d)                                                                                               |
| LB- \_ SelectString     | (b) (f) (d)                                                                                               |
| WM \_ gettext          | (b) (f)                                                                                                   |
| WM \_ getTextLength    | ein                                                                                                       |
| WM- \_ SetText          | (b) (f)                                                                                                   |
| WM- \_ settingchange    | (a) die Nachricht wird mit einem Timeout von drei Sekunden gesendet.                                                  |



 


-   (a) die ANSI-Zeichenfolge, die gemessen oder abgerufen wird, muss die folgende Bedingung erfüllen: die Länge der entsprechenden Unicode-Version der Zeichenfolge darf die Länge der ANSI-Version der Zeichenfolge nicht überschreiten. Wenn diese Bedingung nicht erfüllt wird, ist die zurückgegebene Länge kurz. Wenn nicht genügend Arbeitsspeicher zur Bestimmung der Länge der Unicode-Zeichenfolge vorhanden ist, gibt die Funktion 0 (null), nicht lb \_ Err oder CB Err zurück, \_ wie es möglicherweise erwartet wird.
-   (b) Wenn eine Zeichen folgen Konvertierung erforderlich ist, werden alle Zeichen folgen über die \_ ACP ACP-Codepage konvertiert.

    Diese Funktion verwendet Zeichen mit der höchsten Passform und führt keine Standardüberprüfung durch, wenn Sie von Unicode in ANSI umschließt. Wenn die Zeichenfolge nicht von Unicode in ANSI konvertiert werden kann, übergibt die Funktion außerdem eine NULL-Zeichenfolge an die zugrunde liegende ANSI-Funktion. Dies kann z. b. vorkommen, wenn nicht genügend Arbeitsspeicher vorhanden ist. Das übergeben einer NULL-Zeichenfolge kann dazu führen, dass einige Funktionen mit einem ungültigen Parameter Fehler fehlschlagen. andere Funktionen akzeptieren jedoch die NULL-Zeichenfolge und behandeln Sie als beabsichtigten Parameter. Wenn z. b. ein Fehler auftritt, wenn der WM- \_ SetText-Wrapper versucht, den Fenstertitel in ANSI zu konvertieren, weist das Fenster eine leere Beschriftung auf. Wenn diese Probleme auftreten, werden Sie von der Funktion nicht benachrichtigt. Die MSLU verfügt nicht über diese Einschränkungen.

-   (c) das angegebene Fenster Handle muss das Handle für ein [ComboBox](../controls/combo-boxes.md) -oder [ComboBoxEx](../controls/comboboxex-controls.md) -Steuerelement sein. Wenn das Handle zu einem ComboBox-Steuerelement gehört, das vom Besitzer gezeichnet wird und nicht mit dem Format Stil der [Listen](../controls/list-box-styles.md) Felder erstellt wurde, schlägt die Übersetzung dieser Nachricht fehl und kann sogar abstürzen.
-   (d) das angegebene Fenster Handle muss das Handle für ein ListBox-Steuerelement sein. Wenn das ListBox-Steuerfeld Besitzer gezeichnet ist und nicht [mit der Format](../controls/list-box-styles.md) Vorlagen Formatvorlage erstellt wurde, schlägt die Übersetzung dieser Nachricht fehl und kann sogar abstürzen.
-   (e) Wenn eine Zeichen folgen Konvertierung erforderlich ist, werden alle Zeichen folgen über die \_ ACP ACP-Codepage konvertiert.

    Bei der Umstellung von ANSI in Unicode für die Ausgabe kürzen die Wrapper Funktionen die zurückgegebene Zeichenfolge, wenn Sie nicht in den bereitgestellten Puffer passt. Der Rückgabewert für Funktionen, die die Anzahl der Zeichen zurückgeben, die in den Puffer kopiert werden, oder die Anzahl der Zeichen, die zur Vermeidung von abkürzen erforderlich sind, bezieht sich auf die Anzahl von ANSI-Zeichen, die in den Puffer kopiert werden oder die von der zugrunde liegenden ANSI-Funktion benötigt wird. Die MSLU weist diese Einschränkung nicht auf. Weitere Informationen finden Sie unter [Microsoft-Schicht für Unicode auf Windows 95/98/Me-Systemen](/previous-versions/ms812865(v=msdn.10)).

### <a name="settimerqueuetimer"></a>("*")

Die **shcttimerqueuetimer** -Funktion unterscheidet sich geringfügig [](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) von der entsprechenden Funktion "Funktion" in "". Die Syntax ist wie folgt:

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

-   Der *hqueue* -Parameter muss auf **null** festgelegt werden und die standardmäßige Zeit Geber Warteschlange angeben.
-   Die Parameter " *pfncallback*", " *pContext*", " *dwduetime*" und " *dwperiod* " haben dieselbe Bedeutung wie die Parameter " *Callback*", " *Parameter*", " *dueTime*" und " *Period* " von " [**kreatetimerqueuetimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)".
-   Der *lpszlibrary* -Parameter wird nicht verwendet und muss auf **null** festgelegt werden.
-   Der *Flags* -Parameter unterstützt nur eine Teilmenge der Werte, die von " [**kreatetimerqueuetimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)" unterstützt werden.

    

    | Name              | Wert      | Bedeutung                         |
    |-------------------|------------|---------------------------------|
    | TPS \_ executeio    | 0x00000001 | Identisch mit WT \_ executeiniothread   |
    | TPS- \_ Zeit (longexectime) | 0x00000008 | Identisch mit der "WT \_ executgestreckt"-Funktion |

    

     

    > [!Note]  
    > Das TPS- \_ Flag "longexectime" hat nicht denselben numerischen Wert wie das "WT \_ executlänfunction"-Flag. Bei Verwendung von **SH-ttimerqueuetimer** muss der *dwFlags* -Parameter eine Kombination aus TPS- \_ \* Werten, nicht von WT- \_ \* Werten sein.

     

**Shaderttimerqueuetimer** gibt das Handle des erstellten Timers bei Erfolg und andernfalls **null** zurück.

### <a name="shellexecuteex"></a>(ShellExecuteEx)

Der **lpfile** -Member der [**shellexecuteinfo**](/windows/win32/api/Shellapi/ns-shellapi-shellexecuteinfoa) -Struktur, die in den only-Parameter dieser Funktion übergeben wird, darf die maximal zulässige Länge von URL-Zeichen nicht überschreiten \_ \_ \_ . Wenn das \_ Flag " \_ className anzeigen" weggelassen wird, muss der **lpclass** -Member mit **null** initialisiert werden.

### <a name="valueex"></a>(Valueex)

Nur die folgenden Registrierungs Datentypen werden unterstützt: reg \_ SZ, reg \_ Expand \_ SZ, reg \_ binary und reg \_ DWORD. Im Gegensatz zu diesen Wrapper Funktionen unterstützt MSLU auch reg \_ Multi \_ Expand \_ SZ.

### <a name="windowlong"></a>(Windowlong)

Auf nativen ANSI-Plattformen führt die Funktion keine Übersetzung in einem der Fenster-Longs aus. Wenn Sie z. b. gwlp \_ WndProc übergeben, gibt die-Funktion die ANSI-Fenster Prozedur zurück, nicht einen Thunk. Die MSLU verfügt nicht über diese Einschränkungen.

 

 
