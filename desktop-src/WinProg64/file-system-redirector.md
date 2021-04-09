---
title: Datei System-Redirector
description: Das Verzeichnis windir \\ system32 ist für 64-Bit-Anwendungen auf 64-Bit-Windows reserviert.
ms.assetid: b4d36fe8-8bbb-469b-8ad1-650d559a4c75
keywords:
- Dateisystem-Redirector 64-Bit-Windows-Programmierung
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Dateisystemredirector
- WOW64 64-Bit-Windows-Programmierung, Dateisystemredirector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561d03c8da51bd37a2d97746296bc74e24e43154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039320"
---
# <a name="file-system-redirector"></a>Datei System-Redirector

Das Verzeichnis% windir% \\ system32 ist für 64-Bit-Anwendungen auf 64-Bit-Windows reserviert. Die meisten DLL-Dateinamen wurden beim Erstellen von 64-Bit-Versionen der DLLs nicht geändert, sodass die 32-Bit-Versionen der DLLs in einem anderen Verzeichnis gespeichert werden. WOW64 blendet diesen Unterschied mithilfe eines *Dateisystem-Redirectors* aus.

In den meisten Fällen wird immer dann, wenn eine 32-Bit-Anwendung versucht, auf% WINDIR% \\ system32,% windir% \\ lastgood \\ system32 oder% windir% \\regedit.exe zuzugreifen, der Zugriff an einen architekturspezifischen Pfad umgeleitet.

> [!Note]  
> Diese Pfade werden nur zur Referenz bereitgestellt. Aus Kompatibilitätsgründen sollten Anwendungen diese Pfade nicht direkt verwenden. Stattdessen sollten Sie die unten beschriebenen APIs aufzurufen.

 



|                              |                                          |                                          |
|------------------------------|------------------------------------------|------------------------------------------|
| Original Path                | Umgeleiteter Pfad für 32-Bit-x86-Prozesse | Umgeleiteter Pfad für 32-Bit-ARM-Prozesse |
| % windir% \\ system32           | % windir% \\ syswow64                       | % windir% \\ SysArm32                       |
| % windir% \\ lastgood \\ system32 | % windir% \\ lastgood \\ syswow64             | % windir% \\ lastgood \\ SysArm32             |
| % windir% \\regedit.exe        | % windir% \\ syswow64 \\regedit.exe          | % windir% \\ SysArm32 \\regedit.exe         |



 

Wenn der Zugriff bewirkt, dass das System die UAC-Eingabeaufforderung anzeigt, erfolgt keine Umleitung. Stattdessen wird die 64-Bit-Version der angeforderten Datei gestartet. Um dieses Problem zu vermeiden, geben Sie entweder das Verzeichnis syswow64 an, um eine Umleitung zu vermeiden, und stellen Sie sicher, dass der Zugriff auf die 32-Bit-Version der Datei erfolgt, oder führen Sie die 32-Bit-Anwendung mit Administratorrechten aus.

**Windows Server 2003 und Windows XP:  ** UAC wird nicht unterstützt.

Bestimmte Unterverzeichnisse sind von der Umleitung ausgenommen. Der Zugriff auf diese Unterverzeichnisse wird nicht an% windir% \\ syswow64 umgeleitet: <dl> % windir% \\ system32- \\ Basis  
% windir% \\ system32 \\ Catroot2  
% windir% \\ system32 \\ DriverStore  
% windir% \\ system32 \\ Drivers \\ usw.  
% windir% \\ system32 \\ Logfiles  
% windir% \\ system32 \\ Spool  
</dl>

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:  **% windir% \\ system32 \\ DriverStore wird umgeleitet.

Zum Abrufen des Namens des 32-Bit-System Verzeichnisses sollten für 64-Bit-Anwendungen die [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) -Funktion (Windows 10, Version 1511) oder die [**GetSystemWow64Directory**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) -Funktion verwendet werden.

Anwendungen sollten die [**shgetknownfolderpath**](https://www.bing.com/search?q=**SHGetKnownFolderPath**) -Funktion verwenden, um den% Program Files%-Verzeichnisnamen zu ermitteln.

**Windows Server 2003 und Windows XP:** Anwendungen sollten die [**SHGetSpecialFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) -Funktion verwenden, um den% Program Files%-Verzeichnisnamen zu ermitteln.

Anwendungen können den Redirector von WOW64 File System mithilfe der Funktionen [**Wow64DisableWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection), [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)und [**Wow64RevertWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection) steuern. Die Deaktivierung der Dateisystem Umleitung wirkt sich auf alle Datei Vorgänge aus, die vom aufrufenden Thread ausgeführt werden. Daher sollte Sie nur bei Bedarf für einen einzelnen [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) -Aufruf deaktiviert und unmittelbar nach der Rückgabe der Funktion erneut aktiviert werden. Die Deaktivierung der Dateisystem Umleitung für längere Zeiträume kann verhindern, dass 32-Bit-Anwendungen System-DLLs laden, sodass die Anwendungen nicht mehr funktionieren.

32-Bit-Anwendungen können auf das systemeigene System Verzeichnis zugreifen, indem Sie% windir% \\ sysnative für% windir% \\ system32 ersetzen. WOW64 erkennt sysnative als speziellen Alias, mit dem angegeben wird, dass das Dateisystem den Zugriff nicht umleiten soll. Dieser Mechanismus ist flexibel und einfach zu verwenden. Daher wird empfohlen, die Umleitung des Dateisystems zu umgehen. Beachten Sie, dass 64-Bit-Anwendungen den sysnative-Alias nicht verwenden können, da es sich um ein virtuelles Verzeichnis handelt, das nicht richtig ist.

**Windows Server 2003 und Windows XP:** Der sysnative Alias wurde ab Windows Vista hinzugefügt.

 

 