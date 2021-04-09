---
description: Die folgenden Funktionen werden bei der dynamischen Verknüpfung verwendet.
ms.assetid: 29e50bd5-1712-407f-bcb3-50a0a22ab8b5
title: Funktionen der Dynamic-Link-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47ce37b6f91570ce9f3314fc329b5e85cde310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868259"
---
# <a name="dynamic-link-library-functions"></a>Funktionen der Dynamic-Link-Bibliothek

Die folgenden Funktionen werden bei der dynamischen Verknüpfung verwendet.



| Funktion                                                       | BESCHREIBUNG                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Adddlldirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)                     | Fügt dem Prozess-dll-Suchpfad ein Verzeichnis hinzu.                                                                                                               |
| [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) | Deaktiviert Thread Anfüge-und Thread Trennungs Benachrichtigungen für die angegebene DLL.                                                                                  |
| [**DllMain**](dllmain.md)                                     | Ein optionaler Einstiegspunkt in eine DLL.                                                                                                                            |
| [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)                             | Dekremente den Verweis Zähler der geladenen DLL. Wenn der Verweis Zähler Null erreicht, wird das Modul nicht mehr dem Adressraum des aufrufenden Prozesses zugeordnet. |
| [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)   | Dekremente den Verweis Zähler einer geladenen DLL um 1 und ruft dann [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) auf, um den aufrufenden Thread zu beenden.                       |
| [**Getdlldirectory**](/windows/desktop/api/WinBase/nf-winbase-getdlldirectorya)                     | Ruft den anwendungsspezifischen Teil des Suchpfads ab, der zum Suchen von DLLs für die Anwendung verwendet wird.                                                         |
| [**Fehler bei GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)                 | Ruft den voll qualifizierten Pfad für die Datei ab, die das angegebene Modul enthält.                                                                               |
| [**Getmoduledateinameex**](/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa)            | Ruft den voll qualifizierten Pfad für die Datei ab, die das angegebene Modul enthält.                                                                               |
| [**Fehler bei GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)                     | Ruft ein Modul Handle für das angegebene Modul ab.                                                                                                            |
| [**Getmodulelenker Ex**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandleexa)                 | Ruft ein Modul Handle für das angegebene Modul ab.                                                                                                            |
| [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)                       | Ruft die Adresse einer exportierten Funktion oder Variablen aus der angegebenen DLL ab.                                                                              |
| [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                             | Ordnet das angegebene ausführbare Modul dem Adressraum des aufrufenden Prozesses zu.                                                                            |
| [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)                         | Ordnet das angegebene ausführbare Modul dem Adressraum des aufrufenden Prozesses zu.                                                                            |
| [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)             | Ordnet das angegebene Paket Modul und seine Abhängigkeiten dem Adressraum des aufrufenden Prozesses zu. Diese Funktion kann nur von Windows Store-Apps aufgerufen werden.         |
| [**Removedlldirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-removedlldirectory)               | Entfernt ein Verzeichnis, das zum Prozess-dll-Suchpfad hinzugefügt wurde, mithilfe von [**adddlldirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory).                                         |
| [**Setdefaultdlldirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)   | Gibt einen Standardsatz von Verzeichnissen an, die durchsucht werden sollen, wenn der aufrufenden Prozess eine DLL lädt.                                                                         |
| [**Setdlldirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)                     | Ändert den Suchpfad, der zum Suchen von DLLs für die Anwendung verwendet wird.                                                                                              |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

Diese Funktionen werden nur aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt.

[**LoadModule**](/windows/desktop/api/Winbase/nf-winbase-loadmodule)

 

 
