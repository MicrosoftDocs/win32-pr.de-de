---
title: Portieren von defs, Bindungen und Sätzen
description: Portieren von defs, Bindungen und Sätzen
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- IRIS GL portieren, Definitionen
- Portieren von IRIS GL, Definitionen
- Portieren auf OpenGL von IRIS GL, Definitionen
- OpenGL-Portierung von IRIS GL, Definitionen
- IRIS GL portieren, Bindungen
- Portieren von IRIS GL, Bindungen
- Portieren auf OpenGL von IRIS GL, Bindungen
- OpenGL-Portierung von IRIS GL, Bindungen
- IRIS GL Porting, Sets
- Portieren von IRIS GL, Sets
- Portieren auf OpenGL von IRIS GL, Sets
- OpenGL-Portierung von IRIS GL, Sets
- definitions
- miteinander
- Mengen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f9a88253390ee99f5b5870fd7a09e272f1c549
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342244"
---
# <a name="porting-defs-binds-and-sets"></a>Portieren von defs, Bindungen und Sätzen

OpenGL hat keine Tabellen mit gespeicherten Definitionen. Sie können keine Beleuchtungs Modelle, Materialien, Texturen, Linienstile oder Muster als separate Objekte definieren, wie Sie es in IRIS GL haben. Daher hat OpenGL keine direkten Entsprechungen für die folgenden IRIS GL-Funktionen:

-   **Imdef** und **imbind**
-   **tevdef** und **tevbind**
-   **textdef** und **textbind**
-   **definestyle** und **SetStyle**
-   **defpattern** und **SetPattern**

Mithilfe der OpenGL-Anzeigelisten können Sie den Iris GL DEF/BIND-Mechanismus imitieren. Hier ist beispielsweise eine Material Definition in IRIS GL:


```C++
float mat() = { 
    AMBIENT, .1, .1, .1, 
    DIFFUSE, 0, .369, .165, 
    SPECULAR, .5, .5, .5, 
    SHININESS, 10, 
    LMNULL 
}; 
lmdef(DEFMATERIAL, 1, 0, mat); 
lmbind(MATERIAL, 1);
```



Im folgenden OpenGL-Codebeispiel wird das gleiche Material in einer Anzeigeliste definiert, auf die durch die von **myMaterial** definierte Listen Zahl verwiesen wird.


```C++
#define MYMATERIAL 10 
 
GLfloat        mat_amb[] = {.1, .1, .1, 1.0}; 
GLfloat        mat_dif[] = {0, .369, .165, 1.0}; 
GLfloat        mat_spec[] = {.5, .5, .5, 1.0}; 
 
glNewList(MYMATERIAL, GL_COMPILE); 
    glMaterialfv(GL_FRONT, GL_AMBIENT, mat_amb); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_dif); 
    glMaterialfv(GL_FRONT, GL_SHININESS, 10); 
glEndList(); 
 
glCallList( MYMATERIAL );
```



 

 




