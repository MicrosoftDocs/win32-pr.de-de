---
description: Die folgenden Funktionen werden beim dynamischen Verknüpfen verwendet.
ms.assetid: 29e50bd5-1712-407f-bcb3-50a0a22ab8b5
title: Dynamic-Link Bibliotheksfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521c9200b3fa6585ec2804d76ac385845dcd6fb56ef4e7b70a7a3d9bd59150c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070580"
---
# <a name="dynamic-link-library-functions"></a>Dynamic-Link Bibliotheksfunktionen

Die folgenden Funktionen werden beim dynamischen Verknüpfen verwendet.



| Funktion                                                       | Beschreibung                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)                     | Fügt dem Prozess-DLL-Suchpfad ein Verzeichnis hinzu.                                                                                                               |
| [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) | Deaktiviert Thread attach- und thread detach-Benachrichtigungen für die angegebene DLL.                                                                                  |
| [**DllMain**](dllmain.md)                                     | Ein optionaler Einstiegspunkt in eine DLL.                                                                                                                            |
| [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)                             | Dekrementiert die Verweisanzahl der geladenen DLL. Wenn die Verweisanzahl 0 (null) erreicht, wird das Modul aus dem Adressraum des aufrufenden Prozesses entfernt. |
| [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)   | Dekrementiert die Verweisanzahl einer geladenen DLL um eins und ruft dann [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) auf, um den aufrufenden Thread zu beenden.                       |
| [**GetDllDirectory**](/windows/desktop/api/WinBase/nf-winbase-getdlldirectorya)                     | Ruft den anwendungsspezifischen Teil des Suchpfads ab, der zum Suchen von DLLs für die Anwendung verwendet wird.                                                         |
| [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)                 | Ruft den vollqualifizierten Pfad für die Datei ab, die das angegebene Modul enthält.                                                                               |
| [**GetModuleFileNameEx**](/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa)            | Ruft den vollqualifizierten Pfad für die Datei ab, die das angegebene Modul enthält.                                                                               |
| [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)                     | Ruft ein Modulhand handle für das angegebene Modul ab.                                                                                                            |
| [**GetModuleHandleEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandleexa)                 | Ruft ein Modulhand handle für das angegebene Modul ab.                                                                                                            |
| [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)                       | Ruft die Adresse einer exportierten Funktion oder Variablen aus der angegebenen DLL ab.                                                                              |
| [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                             | Karten das angegebene ausführbare Modul in den Adressraum des aufrufenden Prozesses ein.                                                                            |
| [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)                         | Karten das angegebene ausführbare Modul in den Adressraum des aufrufenden Prozesses ein.                                                                            |
| [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)             | Karten das angegebene gepackte Modul und seine Abhängigkeiten in den Adressraum des aufrufenden Prozesses ein. Nur Windows Store Apps können diese Funktion aufrufen.         |
| [**RemoveDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-removedlldirectory)               | Entfernt ein Verzeichnis, das dem Prozess-DLL-Suchpfad mit [**addDllDirectory hinzugefügt wurde.**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)                                         |
| [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)   | Gibt einen Standardsatz von Verzeichnissen an, die durchsucht werden, wenn der aufrufende Prozess eine DLL lädt.                                                                         |
| [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)                     | Ändert den Suchpfad, der zum Suchen von DLLs für die Anwendung verwendet wird.                                                                                              |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

Diese Funktionen werden nur zur Kompatibilität mit 16-Bit-Versionen von Windows.

[**Loadmodule**](/windows/desktop/api/Winbase/nf-winbase-loadmodule)

 

 
