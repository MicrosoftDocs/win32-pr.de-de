---
description: In diesem Thema wird beschrieben, wie die Anwendung ein Win32 PE-Ressourcenmodul auf Windows Vista und höher oder unter einem früheren Betriebssystem lädt. Aufrufe sind für die Freigabe des Ressourcenmoduls enthalten.
ms.assetid: c9f126a7-315a-4856-80b3-aec02402a80e
title: Laden eines Win32 PE-Ressourcenmoduls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: affcd1cf582d81aafd70f208531e03723ea44b314f92848f35dfd391f950b0ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145842"
---
# <a name="loading-a-win32-pe-resource-module"></a>Laden eines Win32 PE-Ressourcenmoduls

In diesem Thema wird beschrieben, wie die Anwendung ein Win32 PE-Ressourcenmodul auf Windows Vista und höher oder unter einem früheren Betriebssystem lädt. Aufrufe sind für die Freigabe des Ressourcenmoduls enthalten.

## <a name="load-the-resource-module-on-windows-vista-and-later"></a>Laden des Ressourcenmoduls auf Windows Vista und höher

Auf Windows Vista und höher lädt die Anwendung das Ressourcenmodul mithilfe eines Aufrufs von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa) Der empfohlene Vorgang besteht darin, diese Funktion mit beiden angegebenen Flags aufzurufen. Es folgt ein Beispiel für Anwendungscode, der ein Modul basierend auf Systemspracheinstellungen lädt.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a>Laden des Ressourcenmoduls unter Betriebssystemen vor Windows Vista

Bei Betriebssystemen vor Windows Vista lädt die Anwendung ein Ressourcenmodul basierend auf einer Spracheinstellung, die mit dem Zielbetriebssystem kompatibel ist, sowie Windows Vista und höher. Für diese Art des Ladens von Modulen muss die Anwendung die FUNKTIONEN [**LOADMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) und [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary)aufrufen.


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

[WÄHREND: Application-Specific Einstellungen-Beispiel (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[WÄHREND: Application-Specific Einstellungen-Beispiel (Pre-Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
