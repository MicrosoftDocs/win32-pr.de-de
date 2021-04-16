---
description: Laden von Sprachressourcen
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: Laden von Sprachressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6917f03e773a470288fb4c9577812e0b38868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350308"
---
# <a name="loading-language-resources"></a><span data-ttu-id="697a4-103">Laden von Sprachressourcen</span><span class="sxs-lookup"><span data-stu-id="697a4-103">Loading Language Resources</span></span>

<span data-ttu-id="697a4-104">Die Anwendung lädt alle Sprachressourcen für die Benutzeroberfläche, außer bestimmte umgeleitete Registrierungs Zeichenfolgen, mit Aufrufen von Funktionen zum Laden von Standard Ressourcen, z. b. [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)und [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea).</span><span class="sxs-lookup"><span data-stu-id="697a4-104">Your application loads all user interface language resources, other than certain redirected registry strings, using calls to standard resource loading functions, for example, [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), and [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea).</span></span> <span data-ttu-id="697a4-105">Viele Funktionen zum Laden von Ressourcen wurden so geändert, dass Ressourcen aus sprachspezifischen Ressourcen Dateien automatisch geladen werden, wobei Ressourcen so behandelt werden, als wären Sie in der LN-Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="697a4-105">Many resource loading functions have been modified to load resources from language-specific resource files automatically, treating resources as if they are contained in the LN file.</span></span> <span data-ttu-id="697a4-106">Das folgende Beispiel veranschaulicht die Verwendung von **LoadString** zum Laden von sprach Zeichenfolgen für eine Anwendung, die den System Spracheinstellungen folgt.</span><span class="sxs-lookup"><span data-stu-id="697a4-106">The following example illustrates the use of **LoadString** to load language strings for an application that follows system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="697a4-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="697a4-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="697a4-108">Suchen von Win32 PE-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="697a4-108">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> </dl>

 

 
