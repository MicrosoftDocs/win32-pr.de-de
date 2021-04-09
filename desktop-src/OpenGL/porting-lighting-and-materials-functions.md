---
title: Portieren von Beleuchtungs-und Material Funktionen
description: Die OpenGL-Funktionen für Beleuchtung und Material unterscheiden sich erheblich von den Iris GL-Funktionen. Anders als IRIS GL bietet OpenGL separate Funktionen für das Festlegen von Lichtern, hellen Modellen und Materialien.
ms.assetid: de57d041-1ea1-46d0-b584-009608625ea5
keywords:
- IRIS GL portieren, Beleuchtung
- Portieren von IRIS GL, Beleuchtung
- Portieren auf OpenGL von IRIS GL, Beleuchtung
- OpenGL-Portierung von IRIS GL, Beleuchtung
- IRIS GL portieren, Materialien
- Portieren von IRIS GL, Material
- Portieren auf OpenGL von IRIS GL, Material
- OpenGL-Portierung von IRIS GL, Material
- Belichtung
- Werk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c775670b7ae49e41fed35c192385c72e72e880b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856536"
---
# <a name="porting-lighting-and-materials-functions"></a>Portieren von Beleuchtungs-und Material Funktionen

Die OpenGL-Funktionen für Beleuchtung und Material unterscheiden sich erheblich von den Iris GL-Funktionen. Anders als IRIS GL bietet OpenGL separate Funktionen für das Festlegen von Lichtern, hellen Modellen und Materialien.

Beachten Sie beim Portieren von Beleuchtungs-und Material Funktionen die folgenden Punkte:

-   OpenGL hat keine Tabelle mit gespeicherten Definitionen. Mithilfe von Anzeigelisten können Sie den Iris GL-DEF-/Bindungsmechanismus imitieren. Weitere Informationen zu defs und Bindungen finden Sie unter [Portieren von defs, Bindungen und Sets](porting-defs--binds--and-sets.md).
-   Bei OpenGL ist die Dämpfung mit den einzelnen Lichtquellen und nicht mit dem Gesamt Beleuchtungsmodell verknüpft.
-   Diffuse und Glanz Komponenten werden in OpenGL-Lichtquellen getrennt.
-   OpenGL-Lichtquellen verfügen über eine Alpha-Komponente. Wenn Sie den Iris GL-Code portieren, legen Sie diese Alpha Komponente auf 1,0 fest, um 100% nicht transparent anzugeben. Die Alpha Werte werden dann nur von der Alpha Komponente ihrer Materialien bestimmt, sodass die Objekte in Ihrer Szene genauso aussehen wie in IRIS GL.

In der folgenden Tabelle sind die Funktionen von IRIS GL, Beleuchtung und Material sowie die entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion                 | OpenGL-Funktion                               | Bedeutung                                                       |
|----------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| **Imdef (deflight**,... **)**    | [gllight](gllight-functions.md)              | Definieren Sie eine Lichtquelle.                                        |
| **Imdef (deflmodel**,... **)**   | [gllightmodel](gllightmodel-functions.md)    | Definieren eines Beleuchtungs Modells.                                      |
| **Bindung aufheben**                       | [**glEnable**](glenable.md) (GL \_ Light *i*) | Light *i* aktivieren.                                             |
| **Bindung aufheben**                       | **glEnable**(GL- \_ Beleuchtung)                  | Aktivieren der Beleuchtung.                                              |
| **Imdef (defmaterial**,... **)** | [**glmaterial**](glmaterial-functions.md)    | Definieren Sie ein Material.                                            |
| **Imcolor**                      | [**glcolormaterial**](glcolormaterial.md)    | Ändern Sie die Auswirkung von Farb Befehlen, während die Beleuchtung aktiv ist. |
|                                  | [**glgetmaterial**](glgetmaterial.md)        | Erhalten von Materialparametern.                                      |



 

In der folgenden Tabelle werden verschiedene Materialparameter von IRIS GL und ihre entsprechenden OpenGL-Parameter aufgelistet.



| Imdef-Index  | glmaterial-Parameter                              | Standard              | Bedeutung                                                                                       |
|--------------|---------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------|
| ALPHA        | GL- \_ diffuses                                       |                      | Der vierte Wert im GL- \_ diffusen Parameter gibt den Alpha-Wert an.                      |
| AMBIENT      | GL- \_ AMBIENT                                       | (0,2, 0,2, 0,2, 1,0) | Umgebungs Farbe.                                                                                |
| User      | GL- \_ diffuses                                       | (0,8, 0,8, 0,8, 1,0) | Diffuse Farbe.                                                                                |
| Glanz     | GL \_ Glanz                                      | (0,0, 0,0, 0,0, 1,0) | Emissive-Farbe.                                                                               |
| Glanz    | GL \_ shininess GL \_ AMBIENT \_ und \_ diffuse<br/> | 0,0                  | Glanz Exponent. Äquivalent zum doppelten Aufrufen von **glmaterial** mit denselben Werten.<br/> |
| Colorindexes | GL- \_ Farb \_ Indizes                                |                      | Farbindizes für Ambient, diffuse und Glanz Beleuchtung.                                    |



 

Wenn der erste Parameter von **imdef** "defmodel" ist, ist die entsprechende OpenGL-Übersetzung die Funktion " [**gllightmodel**](gllightmodel-functions.md)". Die Ausnahme ist, wenn der Parameter "defmodel" auf "Dämpfung" folgt: die entsprechende OpenGL-Funktion ist " [**gllight**](gllight-functions.md)".

In der folgenden Tabelle sind die entsprechenden Beleuchtungsmodell Parameter für Iris GL und OpenGL aufgeführt.



| Imdef-Index | gllightmodel-Parameter          | Standard              | Bedeutung                                          |
|-------------|---------------------------------|----------------------|--------------------------------------------------|
| AMBIENT     | GL- \_ Light- \_ Modell \_ AMBIENT       | (0,2, 0,2, 0,2, 1,0) | Umgebungs Farbe der Szene.                          |
| Dämpfung |                                 |                      | Siehe [**gllight**](gllight-functions.md).        |
| Localviewer | \_ \_ \_ lokaler \_ Viewer für GL-Light-Modell | GL \_ false            | Viewer local (**true**) oder Infinite (**false**). |
| Twoside     | GL \_ lightmodel \_ zwei \_ seitig       | GL \_ false            | Verwenden Sie die zweiseitige Beleuchtung, wenn **true**.            |



 

Wenn der erste Parameter von **imdef** deflight ist, ist die entsprechende OpenGL-Übersetzung die [**gllight**](gllight-functions.md) -Funktion.

In der folgenden Tabelle sind die entsprechenden Beleuchtungs Parameter für Iris GL und OpenGL aufgeführt.



| Imdef-Index           | gllight-Parameter                                                                                 | Standard                                                                             | Bedeutung                                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| AMBIENT               | "GL \_ ambientgl \_ diffuse"<br/> GL \_ Glanz<br/>                                         | (0,0, 0,0, 0,0, 1,0) (1,0, 1,0, 1,0, 1,0)<br/> (1,0, 1,0, 1,0, 1,0)<br/> | Umgebungs Intensität. Diffuse Intensität.<br/> Glanz Intensität.<br/> |
| Lcolor                | Keine Entsprechung                                                                                    |                                                                                     |                                                                                |
| POSITION              | GL- \_ Position                                                                                      | (0,0, 0,0, 1,0, 0,0)                                                                | Die Position des Lichts.                                                             |
| Spotdirection         | GL- \_ Spot- \_ Richtung                                                                               | (0,0)                                                                           | Richtung des Spotlight.                                                        |
| Gerückt             | GL- \_ Spot \_ exponentgl-Spot-Umstellungs \_ Punkt \_<br/>                                                     | 0180<br/>                                                                     | Intensität Verteilung. Der maximale verteilte Winkel der Lichtquelle.<br/>        |
| defmodel, Dämpfung | GL- \_ Konstante \_ Dämpfung, \_ lineare \_ Dämpfung<br/> GL. \_ quadratische \_ Dämpfung<br/> | (1, 0, 0)                                                                           | Dämpfungsfaktoren.                                                           |



 

 

 





