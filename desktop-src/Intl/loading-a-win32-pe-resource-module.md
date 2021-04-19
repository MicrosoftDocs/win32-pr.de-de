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
# <a name="loading-a-win32-pe-resource-module"></a><span data-ttu-id="332ed-104">Laden eines Win32 PE-Ressourcen Moduls</span><span class="sxs-lookup"><span data-stu-id="332ed-104">Loading a Win32 PE Resource Module</span></span>

<span data-ttu-id="332ed-105">In diesem Thema wird beschrieben, wie die Anwendung ein Win32 PE-Ressourcen Modul entweder unter Windows Vista und höher oder unter einem früheren Betriebssystem lädt.</span><span class="sxs-lookup"><span data-stu-id="332ed-105">This topic describes how the application loads a Win32 PE resource module on either Windows Vista and later or on an earlier operating system.</span></span> <span data-ttu-id="332ed-106">Zum Freigeben des Ressourcen Moduls sind Aufrufe enthalten.</span><span class="sxs-lookup"><span data-stu-id="332ed-106">Calls are included for releasing the resource module.</span></span>

## <a name="load-the-resource-module-on-windows-vista-and-later"></a><span data-ttu-id="332ed-107">Laden des Ressourcen Moduls unter Windows Vista und höher</span><span class="sxs-lookup"><span data-stu-id="332ed-107">Load the Resource Module on Windows Vista and Later</span></span>

<span data-ttu-id="332ed-108">Unter Windows Vista und höher lädt die Anwendung das Ressourcen Modul mithilfe eines [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -oder [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)-Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="332ed-108">On Windows Vista and later, the application loads the resource module using a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span> <span data-ttu-id="332ed-109">Der empfohlene Vorgang besteht darin, diese Funktion mit beiden angegebenen Flags aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="332ed-109">The recommended operation is to call this function with both flags specified.</span></span> <span data-ttu-id="332ed-110">Im folgenden finden Sie ein Beispiel für Anwendungscode, mit dem ein Modul auf der Grundlage der System Spracheinstellungen geladen wird.</span><span class="sxs-lookup"><span data-stu-id="332ed-110">The following is an example of application code that loads a module based on system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="332ed-111">Laden des Ressourcen Moduls auf Betriebssystemen vor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="332ed-111">Load the Resource Module on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="332ed-112">Bei Betriebssystemen vor Windows Vista lädt die Anwendung ein Ressourcen Modul basierend auf einer Spracheinstellung, die mit dem Ziel Betriebssystem kompatibel ist, sowie mit Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="332ed-112">On pre-Windows Vista operating systems, the application loads a resource module based on a language setting that is compatible with the target operating system, as well as Windows Vista and later.</span></span> <span data-ttu-id="332ed-113">Für diese Art von Modul Ladevorgangs muss die Anwendung die MUI-Funktionen " [**loadmuilibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) " und " [**fremuilibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary)" abrufen.</span><span class="sxs-lookup"><span data-stu-id="332ed-113">For this type of module loading, the application must call the MUI functions [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).</span></span>


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="332ed-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="332ed-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="332ed-115">Suchen von Win32 PE-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="332ed-115">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> <dt>

[<span data-ttu-id="332ed-116">Beispiel für MUI: Application-Specific Einstellungen (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="332ed-116">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[<span data-ttu-id="332ed-117">Beispiel für MUI: Application-Specific Einstellungen (Pre-Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="332ed-117">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
