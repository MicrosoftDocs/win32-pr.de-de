---
title: Portieren von bearbeiteten anzeigen Listen
description: Obwohl Sie keine OpenGL-Anzeigelisten bearbeiten können, können Sie ähnliche Ergebnisse erzielen, indem Sie die Anzeigelisten Schachteln und dann neue Versionen der Unterlisten zerstören und erstellen.
ms.assetid: b7f7ffed-c3de-43d4-bff2-f244faa3a27a
keywords:
- IRIS GL portieren, Anzeigen von Listen
- Portieren von IRIS GL, Anzeigen von Listen
- Portieren auf OpenGL von IRIS GL, Anzeigen von Listen
- OpenGL-Portierung von IRIS GL, Anzeigen von Listen
- Anzeigen von Listen, Portieren von IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5555c850d4695ba3732b61c0a41b7aedd8af0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341465"
---
# <a name="porting-edited-display-lists"></a>Portieren von bearbeiteten anzeigen Listen

Obwohl Sie keine OpenGL-Anzeigelisten bearbeiten können, können Sie ähnliche Ergebnisse erzielen, indem Sie die Anzeigelisten Schachteln und dann neue Versionen der Unterlisten zerstören und erstellen. Beispiel:

``` syntax
glNewList (1, GL_COMPILE); 
    glIndexi(MY_RED); 
glEndlist(); 
 
glNewList(2, GL_COMPILE); 
    glScalef(1.2, 1.2, 1.0); 
glEndList(); 
 
glNewList(3, GL_COMPILE); 
    glCallList(1); 
    glCallList(2); 
glEndList(); 
 
glDeleteLists(1, 2); 
glNewList(1, GL_COMPILE); 
    glIndexi(MY_CYAN); 
glEndList(); 
glNewList(2, GL_COPILE); 
    glScalef(0.5, 0.5, 1.0); 
glEndList;
```

 

 




