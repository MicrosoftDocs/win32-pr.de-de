---
title: Portieren von Beleuchtungs- und Materialfunktionen
description: OpenGL-Funktionen für Beleuchtung und Materialien unterscheiden sich erheblich von den IRIS GL-Funktionen. Im Gegensatz zu IRIS GL verfügt OpenGL über separate Funktionen zum Festlegen von Licht, Lichtmodellen und Materialien.
ms.assetid: de57d041-1ea1-46d0-b584-009608625ea5
keywords:
- IRIS GL-Portierung, Beleuchtung
- Portieren von IRIS GL, Beleuchtung
- Portieren von IRIS GL zu OpenGL, Beleuchtung
- OpenGL-Portierung von IRIS GL,Beleuchtung
- IRIS GL-Portierung, Materialien
- Portieren von IRIS GL,Materialien
- Portieren von IRIS GL,Materialien zu OpenGL
- OpenGL-Portierung aus IRIS GL,Materialien
- Belichtung
- Materialien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45041dde0902f983648c6d258f4c4a8220085d0d8bbeddc6fbdbc970033a50ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118933030"
---
# <a name="porting-lighting-and-materials-functions"></a>Portieren von Beleuchtungs- und Materialfunktionen

OpenGL-Funktionen für Beleuchtung und Materialien unterscheiden sich erheblich von den IRIS GL-Funktionen. Im Gegensatz zu IRIS GL verfügt OpenGL über separate Funktionen zum Festlegen von Licht, Lichtmodellen und Materialien.

Beachten Sie beim Portieren von Beleuchtungs- und Materialfunktionen folgende Punkte:

-   OpenGL verfügt über keine Tabelle mit gespeicherten Definitionen. Sie können Anzeigelisten verwenden, um den IRIS GL-Def/Bind-Mechanismus zu imitieren. Weitere Informationen zu Defs und Binds finden Sie unter [Portieren von Defs, Binds und Sets.](porting-defs--binds--and-sets.md)
-   Bei OpenGL ist die Dämpfung jeder Lichtquelle und nicht dem gesamten Beleuchtungsmodell zugeordnet.
-   Diffuse und specular-Komponenten werden in OpenGL-Lichtquellen getrennt.
-   OpenGL-Lichtquellen verfügen über eine Alphakomponente. Legen Sie beim Portieren Ihres IRIS GL-Codes diese Alphakomponente auf 1,0 fest, was 100 % undurchsichtig angibt. Die Alphawerte werden dann nur durch die Alphakomponente Ihrer Materialien bestimmt, sodass die Objekte in Ihrer Szene genauso aussehen wie in IRIS GL.

In der folgenden Tabelle sind die Beleuchtungs- und Materialfunktionen von IRIS GL sowie die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion                 | OpenGL-Funktion                               | Bedeutung                                                       |
|----------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| **Imdef(DEFLIGHT**, ... **)**    | [glLight](gllight-functions.md)              | Definieren Sie eine Lichtquelle.                                        |
| **Imdef(DEFLMODEL**, ... **)**   | [glLightModel](gllightmodel-functions.md)    | Definieren Sie ein Beleuchtungsmodell.                                      |
| **Imbinden**                       | [**glEnable**](glenable.md) ( GL \_ LIGHT *i*) | Aktivieren Sie light *i*.                                             |
| **Imbinden**                       | **glEnable**( GL \_ LIGHTING )                  | Aktivieren Sie die Beleuchtung.                                              |
| **Imdef(DEFMATERIAL**, ... **)** | [**glMaterial**](glmaterial-functions.md)    | Definieren Sie ein Material.                                            |
| **Imcolor**                      | [**glColorMaterial**](glcolormaterial.md)    | Ändern Sie den Effekt von Farbbefehlen, während die Beleuchtung aktiv ist. |
|                                  | [**glGetMaterial**](glgetmaterial.md)        | Materialparameter erhalten.                                      |



 

In der folgenden Tabelle sind verschiedene IRIS GL-Materialparameter und die entsprechenden OpenGL-Parameter aufgeführt.



| Imdef-Index  | glMaterial-Parameter                              | Standard              | Bedeutung                                                                                       |
|--------------|---------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------|
| ALPHA        | GL \_ DIFFUSE                                       |                      | Der vierte Wert im GL \_ DIFFUSE-Parameter gibt den Alphawert an.                      |
| Ambient      | GL \_ AMBIENT                                       | (0.2, 0.2, 0.2, 1.0) | Umgebungsfarbe.                                                                                |
| Diffuse      | GL \_ DIFFUSE                                       | (0.8, 0.8, 0.8, 1.0) | Diffuse Farbe.                                                                                |
| Specular     | GL \_ SPECULAR                                      | (0.0, 0.0, 0.0, 1.0) | Farbliche Farbgebung.                                                                               |
| SCHLÄFRIGKEIT    | \_GL-GL-GL-AMBIENT \_ \_ UND \_ DIFFUSE<br/> | 0,0                  | Specular-Exponent. Entspricht dem **zweimalen Aufrufen von glMaterial** mit denselben Werten.<br/> |
| COLORINDEXES | \_ \_ GL-FARBINDIZES                                |                      | Farbindizes für Umgebungs-, diffuse und speculare Beleuchtung.                                    |



 

Wenn der erste Parameter von **Imdef** DEFMODEL ist, ist die entsprechende OpenGL-Übersetzung die [**Funktion glLightModel**](gllightmodel-functions.md). Die Ausnahme ist, wenn der Parameter nach DEFMODEL ATTENUATION ist: Dann ist die entsprechende OpenGL-Funktion [**glLight.**](gllight-functions.md)

In der folgenden Tabelle sind die entsprechenden Beleuchtungsmodellparameter für IRIS GL und OpenGL aufgeführt.



| Imdef-Index | glLightModel-Parameter          | Standard              | Bedeutung                                          |
|-------------|---------------------------------|----------------------|--------------------------------------------------|
| Ambient     | GL \_ LIGHT \_ MODEL \_ AMBIENT       | (0.2, 0.2, 0.2, 1.0) | Umgebungsfarbe der Szene.                          |
| Dämpfung |                                 |                      | Siehe [**glLight**](gllight-functions.md).        |
| LOCALVIEWER | GL \_ LIGHT \_ MODEL \_ LOCAL \_ VIEWER | GL \_ FALSE            | Viewer local (**TRUE**) oder infinite (**FALSE**). |
| TWOSIDE     | GL \_ LIGHTMODEL \_ TWO \_ SIDE       | GL \_ FALSE            | Verwenden Sie bei TRUE die zweiseitige **Beleuchtung.**            |



 

Wenn der erste Parameter von **Imdef** DEFLIGHT ist, ist die entsprechende OpenGL-Übersetzung die [**glLight-Funktion.**](gllight-functions.md)

In der folgenden Tabelle sind die entsprechenden Beleuchtungsparameter für IRIS GL und OpenGL aufgeführt.



| Imdef-Index           | glLight-Parameter                                                                                 | Standard                                                                             | Bedeutung                                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| Ambient               | GL \_ AMBIENTGL \_ DIFFUSE<br/> GL \_ SPECULAR<br/>                                         | (0.0, 0.0, 0.0, 1.0) (1.0, 1.0, 1.0, 1.0)<br/> (1.0, 1.0, 1.0, 1.0)<br/> | Umgebungsdichte. Diffuse Intensität.<br/> Glanzstärke.<br/> |
| LCOLOR                | Keine Entsprechung                                                                                    |                                                                                     |                                                                                |
| POSITION              | \_GL-POSITION                                                                                      | (0.0, 0.0, 1.0, 0.0)                                                                | Position des Lichts.                                                             |
| SPOTDIRECTION         | GL \_ SPOT \_ DIRECTION                                                                               | (0, 0, 1)                                                                           | Richtung des Blickpunkts.                                                        |
| Spotlight             | GL \_ SPOT \_ EXPONENTGL \_ SPOT \_ CUTOFF<br/>                                                     | 0180<br/>                                                                     | Intensitätsverteilung. Maximaler Verteilungswinkel der Lichtquelle.<br/>        |
| DEFMODEL, ATTENUATION | GL \_ CONSTANT \_ ATTENUATIONGL \_ LINEAR \_ ATTENUATION<br/> GL \_ QUADRATISCHE \_ DÄMPFUNG<br/> | (1, 0, 0)                                                                           | Dämpfungsfaktoren.                                                           |



 

 

 





