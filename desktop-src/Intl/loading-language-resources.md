---
description: Laden von Sprachressourcen
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: Laden von Sprachressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eebf027476658872fe392fe60699da1a586f9297f39a191898b1e132439962c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106930"
---
# <a name="loading-language-resources"></a>Laden von Sprachressourcen

Ihre Anwendung lädt alle Benutzeroberflächensprachressourcen außer bestimmten umgeleiteten Registrierungszeichenfolgen mithilfe von Aufrufen von Standardfunktionen zum Laden von Ressourcen, z. B. [**FormatMessage,**](/windows/win32/api/winbase/nf-winbase-formatmessage) [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)und [**LoadImage.**](/windows/win32/api/winuser/nf-winuser-loadimagea) Viele Funktionen zum Laden von Ressourcen wurden so geändert, dass Ressourcen automatisch aus sprachspezifischen Ressourcendateien geladen werden. Dabei werden Ressourcen so behandelt, als wären sie in der LN-Datei enthalten. Das folgende Beispiel veranschaulicht die Verwendung von **LoadString** zum Laden von Sprachzeichenfolgen für eine Anwendung, die den Systemspracheinstellungen folgt.


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

 

 
