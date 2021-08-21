---
title: Portieren von Defs, Binds und Sets
description: Portieren von Defs, Binds und Sets
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- IRIS GL-Portierung, Definitionen
- Portieren von IRIS GL,Definitionen
- Portieren von IRIS GL zu OpenGL, Definitionen
- OpenGL-Portierung von IRIS GL,Definitionen
- IRIS GL-Portierung, Bindungen
- Portieren von IRIS GL,Bindungen
- Portieren von IRIS GL zu OpenGL, Bindungen
- OpenGL-Portierung von IRIS GL,bindungen
- IRIS GL-Portierung, Sätze
- Portieren von IRIS GL,sets
- Portieren zu OpenGL von IRIS GL,sets
- OpenGL-Portierung von IRIS GL,sets
- definitions
- Bindet
- Mengen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a4c3776d3e5eb8000a4e81578bb5df95658a37e0793944a9cda6923fc7a2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132662"
---
# <a name="porting-defs-binds-and-sets"></a>Portieren von Defs, Binds und Sets

OpenGL enthält keine Tabellen mit gespeicherten Definitionen. Sie können Beleuchtungsmodelle, Material, Texturen, Linienstile oder Muster nicht wie in IRIS GL als separate Objekte definieren. Daher weist OpenGL keine direkten Entsprechungen zu den folgenden IRIS GL-Funktionen auf:

-   **Imdef** und **Imbind**
-   **tevdef** und **tevbind**
-   **textdef** und **textbind**
-   **definestyle** und **setstyle**
-   **defpattern** und **setpattern**

Sie können OpenGL-Anzeigelisten verwenden, um den IRIS GL-Def/Bind-Mechanismus zu imitieren. Hier sehen Sie beispielsweise eine Materialdefinition in IRIS GL:


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



Im folgenden OpenGL-Codebeispiel wird das gleiche Material in einer Anzeigeliste definiert, auf die durch die durch **MYMATERIAL** definierte Listennummer verwiesen wird.


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



 

 




