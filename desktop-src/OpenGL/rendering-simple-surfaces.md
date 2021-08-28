---
title: Rendern einfacher Oberflächen
description: Die GLU-Bibliothek enthält eine Reihe von Funktionen zum Zeichnen verschiedener einfacher Oberflächen (Kugeln, Zylinder, Datenträger und Teile von Datenträgern) in einer Vielzahl von Stilen und Ausrichtungen. Diese Funktionen werden im OpenGL-Referenzhandbuch ausführlich beschrieben.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- OpenGL-Hilfsprogramm (GLU), einfache Oberflächen
- GLU (OpenGL-Hilfsprogramm), einfache Oberflächen
- Einfache Oberflächen OpenGL
- OpenGL-Hilfsprogramm (GLU), Kugeln
- GLU (OpenGL-Hilfsprogramm), Kugeln
- Spheres OpenGL
- OpenGL-Hilfsprogramm (GLU), Zylinder
- GLU (OpenGL-Hilfsprogramm), Zylinder
- Zylinder OpenGL
- OpenGL-Hilfsprogramm (GLU), Datenträger
- GLU (OpenGL-Hilfsprogramm), Datenträger
- Disks OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4010a9cc1c0cfac58f1a99572ebae43233dce552237c17f42d66cc1c50013986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776830"
---
# <a name="rendering-simple-surfaces"></a>Rendern einfacher Oberflächen

Die GLU-Bibliothek enthält eine Reihe von Funktionen zum Zeichnen verschiedener einfacher Oberflächen (Kugeln, Zylinder, Datenträger und Teile von Datenträgern) in einer Vielzahl von Stilen und Ausrichtungen. Diese Funktionen werden im *OpenGL-Referenzhandbuch ausführlich beschrieben.*

**So rendern Sie einfache Oberflächen**

1.  Erstellen Sie mit [**gluNewQuadric ein Quadric-Objekt.**](glunewquadric.md)

    Verwenden Sie [**gluDeleteQuadric,**](gludeletequadric.md)um dieses Objekt zu zerstören, wenn Sie damit fertig sind.

2.  Geben Sie den gewünschten Renderingstil wie unten aufgeführt mit der entsprechenden Funktion an (es sei denn, Sie sind mit den Standardwerten zufrieden):
    -   Gibt an, ob Oberflächennormale generiert werden sollen, und wenn ja, ob ein Normalwert pro Scheitelpunkt oder ein Normalwert pro Gesicht verwendet werden soll: [ **gluQuadricNormals**](gluquadricnormals.md)
    -   Gibt an, ob Texturkoordinaten generiert werden sollen: [ **gluQuadricTexture**](gluquadrictexture.md)
    -   Welche Seite der Quadristik sollte als außen betrachtet werden, und welche innen: [ **gluQuadricOrientation**](gluquadricorientation.md)
    -   Gibt an, ob das Quadric als Satz von Polygonen, Linien oder Punkten gezeichnet werden soll: [ **gluQuadricDrawStyle**](gluquadricdrawstyle.md)
3.  Rufen Sie nach angabe des Renderingstils die Renderingfunktion für den gewünschten Quadric-Objekttyp auf: [**gluSphere,**](glusphere.md) [**gluCylinder,**](glucylinder.md) [**gluDisk**](gludisk.md)oder [**gluPartialDisk**](glupartialdisk.md).

    Wenn während des Renderings ein Fehler auftritt, wird die Fehlerbehandlungsfunktion aufgerufen, die Sie mit [*gluQuadricCallBack*](gluquadric.md) angegeben haben.

Verwenden Sie anstelle der [**glScale-Funktion**](glscale.md) die Argumente *\* Radius,* *Height* und ähnliche Argumente, um die Quadrrics zu skalieren, sodass Sie keine generierten Normal normaler Einheitenlänge neu normalisieren müssen. Um Beleuchtungsberechnungen mit einer feineren Granularität zu erzwingen,  insbesondere wenn  die Materialspezifikation hoch ist, legen Sie die Schleifen und Stapelargumente auf andere Werte als 1 fest.

 

 




