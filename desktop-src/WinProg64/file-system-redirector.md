---
title: Dateisystem-Redirector
description: Das Verzeichnis windir \\ System32 ist für 64-Bit-Anwendungen unter 64-Bit-Windows reserviert.
ms.assetid: b4d36fe8-8bbb-469b-8ad1-650d559a4c75
keywords:
- Dateisystem-Redirector 64-Bit-Windows-Programmierung
- 64-Bit-Windows-Programmierhandbuch 64-Bit-Windows-Programmierung , Dateisystem-Redirector
- WOW64 64-Bit-Windows-Programmierung, Dateisystem-Redirector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568ddde85d18f90b951051251774c3509081dfdd
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443631"
---
# <a name="file-system-redirector"></a>Dateisystem-Redirector

Das Verzeichnis %windir% \\ System32 ist für 64-Bit-Anwendungen unter 64-Bit-Windows reserviert. Die meisten DLL-Dateinamen wurden nicht geändert, als 64-Bit-Versionen der DLLs erstellt wurden, sodass 32-Bit-Versionen der DLLs in einem anderen Verzeichnis gespeichert werden. WOW64 blendet diesen Unterschied mithilfe eines *Dateisystem-Redirectors* aus.

In den meisten Fällen wird der Zugriff an einen architekturspezifischen Pfad umgeleitet, wenn eine 32-Bit-Anwendung versucht, auf %windir% \\ \\ System32, %windir% lastgood \\ system32 oder %windir% \\regedit.exe zuzugreifen.

> [!Note]  
> Diese Pfade werden nur zur Referenz bereitgestellt. Aus Kompatibilitätsgründen sollten Anwendungen diese Pfade nicht direkt verwenden. Stattdessen sollten sie die unten beschriebenen APIs aufrufen.

 



| Original Path                | Umgeleiteter Pfad für 32-Bit-x86-Prozesse | Umgeleiteter Pfad für 32-Bit-ARM-Prozesse |
|------------------------------|------------------------------------------|------------------------------------------|
| %windir% \\ System32           | %windir% \\ SysWOW64                       | %windir% \\ SysArm32                       |
| %windir% \\ lastgood \\ system32 | %windir% \\ lastgood \\ SysWOW64             | %windir% \\ lastgood \\ SysArm32             |
| %windir% \\regedit.exe        | %windir% \\ SysWOW64 \\regedit.exe          | %windir% \\ SysArm32 \\regedit.exe         |



 

Wenn der Zugriff bewirkt, dass das System die UAC-Eingabeaufforderung anzeigt, erfolgt keine Umleitung. Stattdessen wird die 64-Bit-Version der angeforderten Datei gestartet. Um dieses Problem zu vermeiden, geben Sie entweder das Verzeichnis SysWOW64 an, um eine Umleitung zu vermeiden und den Zugriff auf die 32-Bit-Version der Datei sicherzustellen, oder führen Sie die 32-Bit-Anwendung mit Administratorrechten aus, damit die UAC-Eingabeaufforderung nicht angezeigt wird.

**Windows Server 2003 und Windows XP: ** UAC wird nicht unterstützt.

Bestimmte Unterverzeichnisse sind von der Umleitung ausgenommen. Der Zugriff auf diese Unterverzeichnisse wird nicht an %windir% \\ SysWOW64 umgeleitet: <dl> %windir% \\ system32 \\ catroot  
%windir% \\ system32 \\ catroot2  
%windir% \\ system32 \\ driverstore  
%windir% \\ system32 \\ drivers \\ etc  
%windir% \\ system32 \\ protokolldateis  
%windir% \\ system32 \\ spool  
</dl>

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP: **%windir% \\ system32 \\ driverstore wird umgeleitet.

Um den Namen des 32-Bit-Systemverzeichnisses abzurufen, sollten 64-Bit-Anwendungen die [**GetSystemWow64Directory2-Funktion**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) (Windows 10, Version 1511) oder die [**GetSystemWow64Directory-Funktion**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) verwenden.

Anwendungen sollten die [**SHGetKnownFolderPath-Funktion**](https://www.bing.com/search?q=**SHGetKnownFolderPath**) verwenden, um den Verzeichnisnamen %ProgramFiles% zu bestimmen.

**Windows Server 2003 und Windows XP:** Anwendungen sollten die [**SHGetSpecialFolderPath-Funktion**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) verwenden, um den Verzeichnisnamen %ProgramFiles% zu bestimmen.

Anwendungen können den WOW64-Dateisystem-Redirector mithilfe der Funktionen [**Wow64DisableWow64FsRedirection,**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection) [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)und [**Wow64RevertWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection) steuern. Das Deaktivieren der Dateisystemumleitung wirkt sich auf alle Dateivorgänge aus, die vom aufrufenden Thread ausgeführt werden. Daher sollte sie nur deaktiviert werden, wenn dies für einen einzelnen [**CreateFile-Aufruf**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) erforderlich ist, und sofort nach der Rückgabe der Funktion erneut aktiviert werden. Das Deaktivieren der Dateisystemumleitung für längere Zeiträume kann verhindern, dass 32-Bit-Anwendungen System-DLLs laden, was dazu führt, dass die Anwendungen fehlschlagen.

32-Bit-Anwendungen können auf das systemeigene Systemverzeichnis zugreifen, indem sie %windir% \\ Sysnative durch %windir% \\ System32 ersetzen. WOW64 erkennt Sysnative als speziellen Alias, der angibt, dass das Dateisystem den Zugriff nicht umleiten soll. Dieser Mechanismus ist flexibel und einfach zu verwenden. Daher wird empfohlen, die Dateisystemumleitung zu umgehen. Beachten Sie, dass 64-Bit-Anwendungen den Sysnative-Alias nicht verwenden können, da es sich um ein virtuelles Verzeichnis handelt, das kein echtes ist.

**Windows Server 2003 und Windows XP:** Der Sysnative-Alias wurde ab Windows Vista hinzugefügt.

 

 