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
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a><span data-ttu-id="8e6e9-110">Verwenden der Code Beispiele für den Microsoft Windows Media DRM-Client</span><span class="sxs-lookup"><span data-stu-id="8e6e9-110">Using the Microsoft Windows Media DRM Client Code Examples</span></span>

<span data-ttu-id="8e6e9-111">Code Beispiele sind in dieser Dokumentation enthalten, um die Verwendung von-Komponenten zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="8e6e9-111">Code examples are included in this documentation to illustrate the use of components.</span></span> <span data-ttu-id="8e6e9-112">Die Beispiele sind so klar und präzise wie möglich.</span><span class="sxs-lookup"><span data-stu-id="8e6e9-112">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="8e6e9-113">Wenn Sie die Beispiele lesen, sollten Sie die folgenden Konventionen beachten.</span><span class="sxs-lookup"><span data-stu-id="8e6e9-113">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="8e6e9-114">Bei allen Beispielen wird davon ausgegangen, dass Sie Windows. h und wmdrmsdk. h einschließen.</span><span class="sxs-lookup"><span data-stu-id="8e6e9-114">All examples are assumed to include windows.h and wmdrmsdk.h.</span></span> <span data-ttu-id="8e6e9-115">Das Beispiel enthält eine Notiz, wenn für die Kompilierung andere Header benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="8e6e9-115">The example will include a note if it requires other headers in order to compile.</span></span>
-   <span data-ttu-id="8e6e9-116">Die Fehlerüberprüfung wurde auf das Abbrechen der Funktion beschränkt, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="8e6e9-116">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="8e6e9-117">In einer Anwendung sollten Sie nach bestimmten Fehlercodes suchen und eine Art Fehlerberichterstattung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8e6e9-117">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>
-   <span data-ttu-id="8e6e9-118">Schnittstellen und Arbeitsspeicher werden in den Codebeispielen mithilfe von Makros namens sicheres \_ Release und sicheres Löschen von Arrays freigegeben \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8e6e9-118">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="8e6e9-119">Diese Makros sind im folgenden Code definiert:</span><span class="sxs-lookup"><span data-stu-id="8e6e9-119">These macros are defined in the following code:</span></span>
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

    

## <a name="related-topics"></a><span data-ttu-id="8e6e9-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8e6e9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e6e9-121">**Einstieg**</span><span class="sxs-lookup"><span data-stu-id="8e6e9-121">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




