---
title: Verwenden der Code Beispiele für den Microsoft Windows Media DRM-Client
description: Verwenden der Code Beispiele für den Microsoft Windows Media DRM-Client
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows Media-Format-SDK, Codebeispiele
- Windows Media-Format-SDK, Beispielcode
- Windows Media-Format-SDK, DRM-Codebeispiele
- Digital Rights Management (DRM), Codebeispiele
- DRM (Digital Rights Management), Codebeispiele
- Digital Rights Management (DRM), Beispielcode
- DRM (Digital Rights Management), Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 054d1ed804873c8aca104203ee1f235ecb3856f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391355"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a>Verwenden der Code Beispiele für den Microsoft Windows Media DRM-Client

Code Beispiele sind in dieser Dokumentation enthalten, um die Verwendung von-Komponenten zu veranschaulichen. Die Beispiele sind so klar und präzise wie möglich. Wenn Sie die Beispiele lesen, sollten Sie die folgenden Konventionen beachten.

-   Bei allen Beispielen wird davon ausgegangen, dass Sie Windows. h und wmdrmsdk. h einschließen. Das Beispiel enthält eine Notiz, wenn für die Kompilierung andere Header benötigt werden.
-   Die Fehlerüberprüfung wurde auf das Abbrechen der Funktion beschränkt, wenn ein Fehler auftritt. In einer Anwendung sollten Sie nach bestimmten Fehlercodes suchen und eine Art Fehlerberichterstattung bereitstellen.
-   Schnittstellen und Arbeitsspeicher werden in den Codebeispielen mithilfe von Makros namens sicheres \_ Release und sicheres Löschen von Arrays freigegeben \_ \_ . Diese Makros sind im folgenden Code definiert:
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einstieg**](drm-getting-started.md)
</dt> </dl>

 

 




