---
title: Erstellen eines Renderingkontexts als nicht aktuell
description: Um einen Renderingkontext von einem Thread zu trennen, machen Sie ihn nicht aktuell. Rufen Sie hierzu die wglMakeCurrent-Funktion auf, wobei die Parameter auf NULL festgelegt sind. Im Folgenden wird ein Beispiel für diese einfache Aufgabe veranschaulicht.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL für Windows,Renderingkontexte
- Renderingkontexte OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914bbed6e2d595d23cfcf8dc38820efc18153f4433a2a48446090ec16818b671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937363"
---
# <a name="making-a-rendering-context-not-current"></a>Erstellen eines Renderingkontexts als nicht aktuell

Um einen Renderingkontext von einem Thread zu trennen, machen Sie ihn nicht aktuell. Rufen Sie hierzu die [**wglMakeCurrent-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) auf, wobei die Parameter auf **NULL** festgelegt sind. Im Folgenden wird ein Beispiel für diese einfache Aufgabe veranschaulicht.

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




