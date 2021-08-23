---
title: Dateisystem-Redirector
description: Das Verzeichnis windir \\ System32 ist für 64-Bit-Anwendungen auf 64-Bit-Windows.
ms.assetid: b4d36fe8-8bbb-469b-8ad1-650d559a4c75
keywords:
- Dateisystemumleitung 64-Bit-Windows Programmierung
- 64-Bit-Windows 64-Bit-Programmierhandbuch Windows Programmierung , Dateisystemumleitung
- WOW64 64-Bit Windows Programming , Dateisystem-Redirector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318a04d85309ca6c97c87ae2d6a580a85f1a4ee224e162a008034e731a1ff557
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569970"
---
# <a name="file-system-redirector"></a>Dateisystem-Redirector

Das Verzeichnis %windir% \\ System32 ist für 64-Bit-Anwendungen auf 64-Bit-Windows. Die meisten DLL-Dateinamen wurden nicht geändert, als 64-Bit-Versionen der DLLs erstellt wurden, sodass 32-Bit-Versionen der DLLs in einem anderen Verzeichnis gespeichert werden. WOW64 blendet diesen Unterschied mithilfe eines *Dateisystem-Redirectors aus.*

In den meisten Fällen wird der Zugriff an einen architekturspezifischen Pfad umgeleitet, wenn eine \\ 32-Bit-Anwendung versucht, auf %windir% System32, %windir% \\ lastgood \\ system32 oder %windir%regedit.exe zu \\ zugreifen.

> [!Note]  
> Diese Pfade werden nur als Referenz bereitgestellt. Aus Kompatibilitäts- und Kompatibilitätsanforderungen sollten Anwendungen diese Pfade nicht direkt verwenden. Stattdessen sollten sie die unten beschriebenen APIs aufrufen.

 



| Original Path                | Umgeleiteter Pfad für 32-Bit-x86-Prozesse | Umgeleiteter Pfad für 32-Bit-ARM-Prozesse |
|------------------------------|------------------------------------------|------------------------------------------|
| %windir% \\ System32           | %windir% \\ SysWOW64                       | %windir% \\ SysArm32                       |
| %windir% \\ lastgood \\ system32 | %windir% \\ lastgood \\ SysWOW64             | %windir% \\ lastgood \\ SysArm32             |
| %windir% \\regedit.exe        | %windir% \\ SysWOW64 \\regedit.exe          | %windir% \\ SysArm32 \\regedit.exe         |



 

Wenn der Zugriff bewirkt, dass das System die UAC-Eingabeaufforderung angezeigt, erfolgt keine Umleitung. Stattdessen wird die 64-Bit-Version der angeforderten Datei gestartet. Um dieses Problem zu vermeiden, geben Sie entweder das SysWOW64-Verzeichnis an, um eine Umleitung zu vermeiden und den Zugriff auf die 32-Bit-Version der Datei sicherzustellen, oder führen Sie die 32-Bit-Anwendung mit Administratorrechten aus, damit die UAC-Eingabeaufforderung nicht angezeigt wird.

**Windows Server 2003 und Windows XP: ** UAC wird nicht unterstützt.

Bestimmte Unterverzeichnisse sind von der Umleitung ausgenommen. Der Zugriff auf diese Unterverzeichnisse wird nicht an %windir% \\ SysWOW64 umgeleitet: <dl> %windir% \\ system32 \\ catroot  
%windir% \\ system32 \\ catroot2  
%windir% \\ system32 \\ driverstore  
%windir% \\ system32 \\ drivers \\ usw.  
%windir% \\ system32 \\ logfiles  
%windir% \\ system32 \\ spool  
</dl>

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP: **%windir% \\ system32 \\ driverstore is redirected.

Um den Namen des 32-Bit-Systemverzeichnisses abzurufen, sollten 64-Bit-Anwendungen die [**GetSystemWow64Directory2-Funktion**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) (Windows 10, Version 1511) oder die [**GetSystemWow64Directory-Funktion**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) verwenden.

Anwendungen sollten die [**SHGetKnownFolderPath-Funktion verwenden,**](https://www.bing.com/search?q=**SHGetKnownFolderPath**) um den Verzeichnisnamen %ProgramFiles% zu bestimmen.

**Windows Server 2003 und Windows XP:** Anwendungen sollten die [**SHGetSpecialFolderPath-Funktion verwenden,**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) um den Verzeichnisnamen %ProgramFiles% zu bestimmen.

Anwendungen können den WOW64-Dateisystemredirector mithilfe der [**Funktionen Wow64DisableWow64FsRedirection,**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection) [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)und [**Wow64RevertWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection) steuern. Das Deaktivieren der Dateisystemumleitung wirkt sich auf alle Dateivorgänge aus, die vom aufrufenden Thread ausgeführt werden. Daher sollte sie nur deaktiviert werden, wenn dies für einen einzelnen [**CreateFile-Aufruf**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) erforderlich ist, und unmittelbar nach der Rückgabe der Funktion erneut aktiviert werden. Das Deaktivieren der Dateisystemumleitung für längere Zeiträume kann verhindern, dass 32-Bit-Anwendungen System-DLLs laden, was dazu führt, dass die Anwendungen fehlschlagen.

32-Bit-Anwendungen können auf das systemeigene Systemverzeichnis zugreifen, indem sie %windir% \\ Sysnative durch %windir% \\ System32 ändern. WOW64 erkennt Sysnative als speziellen Alias, mit dem angegeben wird, dass das Dateisystem den Zugriff nicht umleiten soll. Dieser Mechanismus ist flexibel und einfach zu verwenden. Daher ist er der empfohlene Mechanismus, um die Dateisystemumleitung zu umgehen. Beachten Sie, dass 64-Bit-Anwendungen den Sysnative-Alias nicht verwenden können, da es sich um ein virtuelles Verzeichnis handelt, das kein echtes Verzeichnis ist.

**Windows Server 2003 und Windows XP:** Der sysnative Alias wurde ab Windows Vista hinzugefügt.

 

 