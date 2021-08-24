---
description: Das Hinzufügen einer 3D-Szene zu einer 3D-Szene kann den Realismus verbessern, Mehrdeutigheit bieten oder eine Stimmung festlegen und Artefakte verdecken, die manchmal verursacht werden, wenn entfernte Geometrie in Sicht kommt.
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Soll (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f06f9ff25c132feaed4ada291e7f063fcbfb3f4f1129cf934b43795b79b20aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026934"
---
# <a name="fog-direct3d-9"></a>Soll (Direct3D 9)

Das Hinzufügen einer 3D-Szene zu einer 3D-Szene kann den Realismus verbessern, Mehrdeutigheit bieten oder eine Stimmung festlegen und Artefakte verdecken, die manchmal verursacht werden, wenn entfernte Geometrie in Sicht kommt. Direct3D unterstützt zwei Modellmodelle, Pixelpixel und Scheitelpunkt, die jeweils über eigene Features und Programmierschnittstellen verfügt.

Im Wesentlichen wird die Farbe von Objekten in einer Szene mit einer ausgewählten Farbe basierend auf der Tiefe eines Objekts in einer Szene oder der Entfernung vom Blickpunkt implementiert. Wenn Objekte entfernter werden, wird ihre ursprüngliche Farbe immer mehr mit der ausgewählten Farbe kombiniert, wodurch die Täuschung entstehen, dass das Objekt zunehmend von kleinen, in der Szene schwebenden Partikeln verdeckt wird. Die folgende Abbildung zeigt eine Szene, die ohne Schwenk gerendert wurde, und eine ähnliche Szene, die mit aktivierter -Darstellung gerendert wird.

![Abbildung der gleichen Szene mit und ohne Ungn](images/fogcomp.png)

In dieser Abbildung hat die Szene auf der linken Seite einen klaren Horizont, ab dem keineRlei sichtbar ist, obwohl sie in der realen Welt sichtbar wäre. Die Szene auf der rechten Seite verdeckt den Horizont, indem sie eine mit der Hintergrundfarbe identische Farbe verwendet, wodurch Polygone in der Entfernung zu verblassen scheinen. Durch die Kombination von diskreten Effekten mit dem Entwurf einer kreativer Szene können Sie Stimmungen hinzufügen und die Farbe von Objekten in einer Szene weich machen.

Direct3D bietet zwei Möglichkeiten zum Hinzufügen von Ziege zu einer Szene: Pixelpixel und Scheitelpunkt, benannt nach der Anwendung der Effekten. Weitere Informationen finden Sie unter [Pixel Pixel (Direct3D 9)](pixel-fog.md) und [VertexFormat (Direct3D 9).](vertex-fog.md) Kurz gesagt: Pixelpixel – auch als Tabellen-Tafeln bezeichnet – werden im Gerätetreiber implementiert, und Scheitelpunkt-Tafeln werden im Direct3D-Beleuchtungsmodul implementiert. Eine Anwendung kann mit einem Scheitelpunkt-Shader und bei Wunsch Pixelpixel gleichzeitig implementieren.

> [!Note]  
> Unabhängig davon, ob Sie Pixel- oder Scheitelpunkt-Scheitelpunkte verwenden, muss Ihre Anwendung eine konforme Projektionsmatrix bereitstellen, um sicherzustellen, dass Die Effekten richtig angewendet werden. Diese Einschränkung gilt auch für Anwendungen, die nicht die Direct3D-Transformation und das Beleuchtungsmodul verwenden. Weitere Informationen dazu, wie Sie eine geeignete Matrix bereitstellen können, finden Sie unter [Projektionstransformation (Direct3D 9).](projection-transform.md)

 

In den folgenden Themen werden Unterschiedliche Features in Direct3D-Anwendungen behandelt.

-   [Formeln für Formeln (Direct3D 9)](fog-formulas.md)
-   [Parameter von "Parameters" (Direct3D 9)](fog-parameters.md)
-   [Blending für Überblendung (Direct3D 9)](fog-blending.md)
-   [Farbton (Direct3D 9)](fog-color.md)
-   [Scheitelpunkt(Direct3D 9)](vertex-fog.md)
-   [Pixelpixel (Direct3D 9)](pixel-fog.md)

Das Blending von Blending wird durch Renderzustände gesteuert. sie ist nicht Teil der programmierbaren Pixelpipeline.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Rendering](direct3d-rendering.md)
</dt> </dl>

 

 



