---
title: Portieren von Beleuchtungs- und Materialfunktionen
description: OpenGL-Funktionen für Beleuchtung und Materialien unterscheiden sich erheblich von den IRIS GL-Funktionen. Im Gegensatz zu IRIS GL verfügt OpenGL über separate Funktionen zum Festlegen von Licht, Lichtmodellen und Materialien.
ms.assetid: de57d041-1ea1-46d0-b584-009608625ea5
keywords:
- IRIS GL-Portierung, Beleuchtung
- Portieren von IRIS GL, Beleuchtung
- Portieren zu OpenGL von IRIS GL, Beleuchtung
- OpenGL-Portierung von IRIS GL, Beleuchtung
- IRIS GL-Portierung, Materialien
- Portieren von IRIS GL, Materialien
- Portieren zu OpenGL von IRIS GL, Materials
- OpenGL-Portierung von IRIS GL, Materialien
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

Beachten Sie beim Portieren von Beleuchtungs- und Materialfunktionen die folgenden Punkte:

-   OpenGL enthält keine Tabelle mit gespeicherten Definitionen. Sie können Anzeigelisten verwenden, um den IRIS GL-Def/Bind-Mechanismus zu imitieren. Weitere Informationen zu Defs und Bindungen finden Sie unter [Portieren von Defs, Binds und Sets.](porting-defs--binds--and-sets.md)
-   Bei OpenGL ist die Dämpfung nicht dem gesamten Beleuchtungsmodell, sondern jeder Lichtquelle zugeordnet.
-   Diffuse und Glanzkomponenten werden in OpenGL-Lichtquellen getrennt.
-   OpenGL-Lichtquellen verfügen über eine Alphakomponente. Legen Sie beim Portieren Ihres IRIS GL-Codes diese Alphakomponente auf 1,0 fest, was 100 % nicht transparent angibt. Die Alphawerte werden dann nur von der Alphakomponente Ihrer Materialien bestimmt, sodass die Objekte in Ihrer Szene genauso aussehen wie in IRIS GL.

In der folgenden Tabelle sind die IRIS GL-Beleuchtungs- und Materialfunktionen und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion                 | OpenGL-Funktion                               | Bedeutung                                                       |
|----------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| **Imdef(DEFLIGHT**, ... **)**    | [glLight](gllight-functions.md)              | Definieren Sie eine Lichtquelle.                                        |
| **Imdef(DEFLMODEL,**... **)**   | [glLightModel](gllightmodel-functions.md)    | Definieren sie ein Beleuchtungsmodell.                                      |
| **Imbind**                       | [**glEnable**](glenable.md) ( GL \_ LIGHT *i*) | Aktivieren Sie light *i*.                                             |
| **Imbind**                       | **glEnable**( GL \_ LIGHTING )                  | Aktivieren Sie die Beleuchtung.                                              |
| **Imdef(DEFMATERIAL**, ... **)** | [**glMaterial**](glmaterial-functions.md)    | Definieren Sie ein Material.                                            |
| **Imcolor**                      | [**glColorMaterial**](glcolormaterial.md)    | Ändern Sie die Auswirkung von Farbbefehlen, während die Beleuchtung aktiv ist. |
|                                  | [**glGetMaterial**](glgetmaterial.md)        | Abrufen von Materialparametern.                                      |



 

In der folgenden Tabelle sind verschiedene IRIS GL-Materialparameter und die entsprechenden OpenGL-Parameter aufgeführt.



| Imdef-Index  | glMaterial-Parameter                              | Standard              | Bedeutung                                                                                       |
|--------------|---------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------|
| ALPHA        | GL \_ DIFFUSE                                       |                      | Der vierte Wert im GL \_ DIFFUSE-Parameter gibt den Alphawert an.                      |
| Ambient      | GL \_ AMBIENT                                       | (0.2, 0.2, 0.2, 1.0) | Umgebungsfarbe.                                                                                |
| Diffuse      | GL \_ DIFFUSE                                       | (0.8, 0.8, 0.8, 1.0) | Diffuse Farbe.                                                                                |
| Specular     | GL \_ SPECULAR                                      | (0.0, 0.0, 0.0, 1.0) | Freizügige Farbe.                                                                               |
| INESS (BESCHWENKUNG    | \_GLINESSGL \_ AMBIENT UND \_ \_ DIFFUSE<br/> | 0,0                  | Specular exponent. Entspricht dem zweimalen Aufrufen von **glMaterial** mit den gleichen Werten.<br/> |
| COLORINDEXES | GL \_ COLOR \_ INDEXES                                |                      | Farbindizes für Umgebungs-, Diffuse- und Glanzlicht.                                    |



 

Wenn der erste **Imdef-Parameter** DEFMODEL ist, ist die entsprechende OpenGL-Übersetzung die Funktion [**glLightModel.**](gllightmodel-functions.md) Die Ausnahme ist, wenn der Parameter nach DEFMODEL ATTENUATION ist: Die entsprechende OpenGL-Funktion ist [**glLight.**](gllight-functions.md)

In der folgenden Tabelle sind die entsprechenden Beleuchtungsmodellparameter für IRIS GL und OpenGL aufgeführt.



| Imdef-Index | glLightModel-Parameter          | Standard              | Bedeutung                                          |
|-------------|---------------------------------|----------------------|--------------------------------------------------|
| Ambient     | GL \_ LIGHT \_ MODEL \_ AMBIENT       | (0.2, 0.2, 0.2, 1.0) | Umgebungsfarbe der Szene.                          |
| Dämpfung |                                 |                      | Weitere Informationen finden Sie [**unter glLight**](gllight-functions.md).        |
| LOCALVIEWER | GL \_ LIGHT \_ MODEL \_ LOCAL \_ VIEWER | GL \_ FALSE            | Viewer local (**TRUE**) oder infinite (**FALSE**). |
| TWOSIDE     | GL \_ LIGHTMODEL \_ TWO \_ SIDE       | GL \_ FALSE            | Verwenden Sie bei **TRUE** die zweiseitige Beleuchtung.            |



 

Wenn der erste **Imdef-Parameter** DEFLIGHT ist, ist die entsprechende OpenGL-Übersetzung die [**glLight-Funktion.**](gllight-functions.md)

In der folgenden Tabelle sind die entsprechenden Beleuchtungsparameter für IRIS GL und OpenGL aufgeführt.



| Imdef-Index           | glLight-Parameter                                                                                 | Standard                                                                             | Bedeutung                                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| Ambient               | GL \_ AMBIENTGL \_ DIFFUSE<br/> GL \_ SPECULAR<br/>                                         | (0.0, 0.0, 0.0, 1.0) (1.0, 1.0, 1.0, 1.0)<br/> (1.0, 1.0, 1.0, 1.0)<br/> | Umgebungsdichte. Diffuse Intensität.<br/> Glanzstärke.<br/> |
| LCOLOR                | Keine Entsprechung                                                                                    |                                                                                     |                                                                                |
| POSITION              | \_GL-POSITION                                                                                      | (0.0, 0.0, 1.0, 0.0)                                                                | Position des Lichts.                                                             |
| SPOTDIRECTION         | GL \_ SPOT \_ DIRECTION                                                                               | (0, 0, 1)                                                                           | Richtung des Blickpunkts.                                                        |
| Spotlight             | GL \_ SPOT \_ EXPONENTGL \_ SPOT \_ CUTOFF<br/>                                                     | 0180<br/>                                                                     | Intensitätsverteilung. Maximaler Verteilungswinkel der Lichtquelle.<br/>        |
| DEFMODEL, ATTENUATION | GL \_ CONSTANT \_ ATTENUATIONGL \_ LINEAR \_ ATTENUATION<br/> GL \_ QUADRATIC \_ ATTENUATION<br/> | (1, 0, 0)                                                                           | Dämpfungsfaktoren.                                                           |



 

 

 





