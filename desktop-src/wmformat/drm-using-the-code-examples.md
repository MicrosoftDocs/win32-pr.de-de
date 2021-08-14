---
title: Verwenden der Microsoft Windows Media DRM-Clientcodebeispiele
description: Verwenden der Microsoft Windows Media DRM-Clientcodebeispiele
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows Medienformat-SDK, Codebeispiele
- Windows Medienformat-SDK, Beispielcode
- Windows Medienformat-SDK, DRM-Codebeispiele
- Digital Rights Management (DRM), Codebeispiele
- DRM (Digital Rights Management), Codebeispiele
- Digital Rights Management (DRM), Beispielcode
- DRM (Digital Rights Management), Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e14ef7e1d003dec8270bb4cfb63d5b4ead7f11751eb94dd09cd771ebd34b3ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704213"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a>Verwenden der Microsoft Windows Media DRM-Clientcodebeispiele

Codebeispiele sind in dieser Dokumentation enthalten, um die Verwendung von Komponenten zu veranschaulichen. Die Beispiele werden so klar und präzise wie möglich geschrieben. Beim Lesen der Beispiele sollten Sie die folgenden Konventionen beachten.

-   Es wird davon ausgegangen, dass alle Beispiele windows.h und wmdrmsdk.h enthalten. Das Beispiel enthält eine Notiz, wenn für die Kompilierung andere Header erforderlich sind.
-   Die Fehlerüberprüfung wurde auf das Ausbrechen der Funktion beschränkt, wenn ein Fehler auftritt. In einer Anwendung sollten Sie nach bestimmten Fehlercodes überprüfen und eine Art Fehlerberichterstattung bereitstellen.
-   Schnittstellen und Arbeitsspeicher werden in den Codebeispielen mit Makros namens SAFE \_ RELEASE und SAFE ARRAY DELETE \_ \_ freigegeben. Diese Makros werden im folgenden Code definiert:
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

[**Erste Schritte**](drm-getting-started.md)
</dt> </dl>

 

 




