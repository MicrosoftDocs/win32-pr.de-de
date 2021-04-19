---
description: In diesem Thema wird beschrieben, wie die Anwendung ein Win32 PE-Ressourcen Modul entweder unter Windows Vista und höher oder unter einem früheren Betriebssystem lädt. Zum Freigeben des Ressourcen Moduls sind Aufrufe enthalten.
ms.assetid: c9f126a7-315a-4856-80b3-aec02402a80e
title: Laden eines Win32 PE-Ressourcen Moduls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c4c1906a4fc09dc39b805e8ad5a875d96fae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373370"
---
# <a name="loading-a-win32-pe-resource-module"></a>Laden eines Win32 PE-Ressourcen Moduls

In diesem Thema wird beschrieben, wie die Anwendung ein Win32 PE-Ressourcen Modul entweder unter Windows Vista und höher oder unter einem früheren Betriebssystem lädt. Zum Freigeben des Ressourcen Moduls sind Aufrufe enthalten.

## <a name="load-the-resource-module-on-windows-vista-and-later"></a>Laden des Ressourcen Moduls unter Windows Vista und höher

Unter Windows Vista und höher lädt die Anwendung das Ressourcen Modul mithilfe eines [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -oder [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)-Aufrufes. Der empfohlene Vorgang besteht darin, diese Funktion mit beiden angegebenen Flags aufzurufen. Im folgenden finden Sie ein Beispiel für Anwendungscode, mit dem ein Modul auf der Grundlage der System Spracheinstellungen geladen wird.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a>Laden des Ressourcen Moduls auf Betriebssystemen vor Windows Vista

Bei Betriebssystemen vor Windows Vista lädt die Anwendung ein Ressourcen Modul basierend auf einer Spracheinstellung, die mit dem Ziel Betriebssystem kompatibel ist, sowie mit Windows Vista und höher. Für diese Art von Modul Ladevorgangs muss die Anwendung die MUI-Funktionen " [**loadmuilibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) " und " [**fremuilibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary)" abrufen.


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Suchen von Win32 PE-Ressourcen](locating-win32-pe-resources.md)
</dt> <dt>

[Beispiel für MUI: Application-Specific Einstellungen (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[Beispiel für MUI: Application-Specific Einstellungen (Pre-Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
