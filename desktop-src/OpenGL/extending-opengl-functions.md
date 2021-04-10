---
title: Erweitern von OpenGL-Funktionen
description: Die OpenGL-Bibliothek unterstützt mehrere Implementierungen ihrer Funktionen.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL unter Windows, Erweiterungsfunktionen
- Erweiterungsfunktionen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcbb59aa15a9690ac05728548f0d8073a334a2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947978"
---
# <a name="extending-opengl-functions"></a><span data-ttu-id="c728d-105">Erweitern von OpenGL-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c728d-105">Extending OpenGL Functions</span></span>

<span data-ttu-id="c728d-106">Die OpenGL-Bibliothek unterstützt mehrere Implementierungen ihrer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="c728d-106">The OpenGL library supports multiple implementations of its functions.</span></span> <span data-ttu-id="c728d-107">In einem renderingkontext unterstützte Erweiterungsfunktionen werden nicht notwendigerweise in einem anderen renderingkontext unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c728d-107">Extension functions supported in one rendering context aren't necessarily supported in a different rendering context.</span></span> <span data-ttu-id="c728d-108">Verwenden Sie für einen gegebenen renderingkontext in einer Anwendung, die Erweiterungsfunktionen verwendet, nur die von der [**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) -Funktion zurückgegebenen Funktions Adressen.</span><span class="sxs-lookup"><span data-stu-id="c728d-108">For a given rendering context in an application using extension functions, use only the function addresses returned by the [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) function.</span></span>

 

 




