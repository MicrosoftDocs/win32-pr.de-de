---
title: Rendering von einfachen Oberflächen
description: Die glu-Bibliothek enthält eine Reihe von Funktionen zum Zeichnen verschiedener einfacher Oberflächen (Bereiche, Zylinder, Datenträger und Teile von Datenträgern) in einer Vielzahl von Stilen und Ausrichtungen. Diese Funktionen werden im OpenGL-Referenzhandbuch ausführlich beschrieben.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- OpenGL-Hilfsprogramm (GLU), einfache Oberflächen
- GLU (OpenGL-Hilfsprogramm), einfache Oberflächen
- einfache Oberflächen OpenGL
- OpenGL-Hilfsprogramm (GLU), Sphären
- GLU (OpenGL-Hilfsprogramm), Sphären
- Sphären OpenGL
- OpenGL-Hilfsprogramm (GLU), Zylinder
- GLU (OpenGL-Hilfsprogramm), Zylinder
- Zylinder OpenGL
- OpenGL-Hilfsprogramm (GLU), Datenträger
- GLU (OpenGL-Hilfsprogramm), Datenträger
- Datenträger OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab766c661f89cbdec30b3295dfef8dc85b59f7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388784"
---
# <a name="rendering-simple-surfaces"></a>Rendering von einfachen Oberflächen

Die glu-Bibliothek enthält eine Reihe von Funktionen zum Zeichnen verschiedener einfacher Oberflächen (Bereiche, Zylinder, Datenträger und Teile von Datenträgern) in einer Vielzahl von Stilen und Ausrichtungen. Diese Funktionen werden im *OpenGL-Referenzhandbuch* ausführlich beschrieben.

**So erzeugen Sie einfache Oberflächen**

1.  Erstellen Sie ein Quadric-Objekt mit " [**glunewquadric**](glunewquadric.md)".

    Um dieses Objekt zu zerstören, wenn Sie damit fertig sind, verwenden Sie " [**gludeletequadric**](gludeletequadric.md)".

2.  Geben Sie den gewünschten Renderingstil wie unten aufgeführt mit der entsprechenden Funktion an (es sei denn, Sie sind mit den Standardwerten zufrieden):
    -   Gibt an, ob Oberflächen normale generiert werden sollen, und wenn dies der Fall ist, ob eine normale pro Scheitelpunkt oder ein normales pro Gesicht vorhanden sein sollte: [ **gluquadricnormals**](gluquadricnormals.md)
    -   Gibt an, ob Texturkoordinaten generiert werden sollen: " [ **gluquadrictexture** "](gluquadrictexture.md)
    -   Welche Seite des quadrands sollte als außen betrachtet werden, und in der-Komponente: " [ **gluquadricorientation** "](gluquadricorientation.md)
    -   Gibt an, ob das Quadric als Satz von Polygonen, Linien oder Punkten gezeichnet werden soll: [ **gluquadricdrawstyle**](gluquadricdrawstyle.md)
3.  Nachdem Sie den Renderingstil angegeben haben, rufen Sie die-Renderingfunktion für den gewünschten Typ des Quadric-Objekts auf: " [**glusphere**](glusphere.md)", " [**gluzylinder**](glucylinder.md)", " [**gludisk**](gludisk.md) [**" oder "**](glupartialdisk.md)

    Wenn während des Renderings ein Fehler auftritt, wird die Fehler Behandlungs Funktion aufgerufen, die Sie mit " [*gluvierccallback*](gluquadric.md) " angegeben haben.

Verwenden Sie die Werte *\* RADIUS*, *height* und ähnliche Argumente anstelle der Funktion [**glscale**](glscale.md) , um die viercs zu skalieren, sodass Sie keine normalisierten Einheiten Längen renormalisieren müssen, die generiert werden. Um Beleuchtungsberechnungen mit einer präziserer Granularität zu erzwingen, insbesondere, wenn die Material Spekulation hoch ist, legen Sie die *Schleifen* -und *Stapel* Argumente auf andere Werte als 1 fest.

 

 




