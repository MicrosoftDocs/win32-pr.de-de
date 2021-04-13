---
title: Erstellen eines renderingkontexts ist nicht aktuell
description: Um einen renderingkontext von einem Thread zu trennen, machen Sie ihn nicht aktuell. Dazu rufen Sie die wglmakecurrent-Funktion mit den Parametern auf, die auf NULL festgelegt sind. Im folgenden finden Sie ein Beispiel für diese einfache Aufgabe.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL unter Windows, renderingkontexte
- Rendern von Kontexten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12b3e0184a606faef7792b990d674054c5ddf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309796"
---
# <a name="making-a-rendering-context-not-current"></a>Erstellen eines renderingkontexts ist nicht aktuell

Um einen renderingkontext von einem Thread zu trennen, machen Sie ihn nicht aktuell. Dazu rufen Sie die [**wglmakecurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) -Funktion mit den Parametern auf, die auf **null** festgelegt sind. Im folgenden finden Sie ein Beispiel für diese einfache Aufgabe.

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




