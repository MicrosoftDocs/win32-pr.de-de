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
# <a name="loading-language-resources"></a>Laden von Sprachressourcen

Die Anwendung lädt alle Sprachressourcen für die Benutzeroberfläche, außer bestimmte umgeleitete Registrierungs Zeichenfolgen, mit Aufrufen von Funktionen zum Laden von Standard Ressourcen, z. b. [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)und [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea). Viele Funktionen zum Laden von Ressourcen wurden so geändert, dass Ressourcen aus sprachspezifischen Ressourcen Dateien automatisch geladen werden, wobei Ressourcen so behandelt werden, als wären Sie in der LN-Datei enthalten. Das folgende Beispiel veranschaulicht die Verwendung von **LoadString** zum Laden von sprach Zeichenfolgen für eine Anwendung, die den System Spracheinstellungen folgt.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Suchen von Win32 PE-Ressourcen](locating-win32-pe-resources.md)
</dt> </dl>

 

 
