---
description: Das Hinzufügen von Nebel zu einer 3D-Szene kann den Realismus verbessern, Ambiente bereitstellen oder einen Stimmungs Wert festlegen
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Nebel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b9ed234bef0f3dea76baa98390f25e9b2003a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341095"
---
# <a name="fog-direct3d-9"></a>Nebel (Direct3D 9)

Das Hinzufügen von Nebel zu einer 3D-Szene kann den Realismus verbessern, Ambiente bereitstellen oder einen Stimmungs Wert festlegen Direct3D unterstützt zwei Nebel Modelle, Pixel Nebel und Scheitelpunkt Nebel, jeweils mit eigenen Features und Programmierschnittstellen.

Im Wesentlichen wird Nebel implementiert, indem die Farbe von Objekten in einer Szene mit einer ausgewählten Nebelfarbe auf der Grundlage der Tiefe eines Objekts in einer Szene oder der Entfernung vom Standpunkt kombiniert wird. Wenn Objekte weiter entfernt werden, werden Ihre ursprüngliche Farbe mehr und mehr mit der ausgewählten Nebelfarbe kombiniert. Dadurch wird die Illusion erstellt, dass das Objekt zunehmend von kleinen, in der Szene gleitenden Partikeln verdeckt wird. Die folgende Abbildung zeigt eine Szene, die ohne Nebel gerendert wird

![Darstellung der gleichen Szene mit und ohne Nebel](images/fogcomp.png)

In dieser Abbildung hat die Szene auf der linken Seite einen klaren Horizont, über den keine Landschaft sichtbar ist, auch wenn Sie in der realen Welt sichtbar wäre. Die Szene auf der rechten Seite verdeckt den Horizont, indem eine mit der Hintergrundfarbe identische Nebelfarbe verwendet wird, sodass Polygone in den Abstand eingeblendet werden. Durch die Kombination von diskreten Nebeleffekten mit dem Design der kreativen Szene können Sie Stimmungs Werte hinzufügen und die Farbe von Objekten in einer Szene weich gestalten.

Direct3D bietet zwei Möglichkeiten zum Hinzufügen von Nebel zu einer Szene: Pixel Nebel und Scheitelpunkt Nebel, die für die Anwendung der Nebeleffekte benannt werden. Weitere Informationen finden Sie unter [Pixel Nebel (Direct3D 9)](pixel-fog.md) und [Scheitelpunkt Nebel (Direct3D 9)](vertex-fog.md). Kurz gesagt: Pixel Nebel, auch als "Tabellen Nebel" bezeichnet, wird im Gerätetreiber implementiert, und der Scheitelpunkt Nebel wird in der Direct3D-Beleuchtungs-Engine implementiert. Eine Anwendung kann Nebel mit einem Vertexshader implementieren und ggf. Pixel Nebel gleichzeitig.

> [!Note]  
> Unabhängig davon, ob Sie Pixel oder Scheitelpunkt Nebel verwenden, muss die Anwendung eine konforme Projektions Matrix bereitstellen, um sicherzustellen, dass Nebeleffekte ordnungsgemäß angewendet werden. Diese Einschränkung gilt auch für Anwendungen, die nicht die Direct3D-Transformation und Beleuchtungs-Engine verwenden. Weitere Details dazu, wie Sie eine geeignete Matrix bereitstellen können, finden Sie unter [Projektions Transformation (Direct3D 9)](projection-transform.md).

 

In den folgenden Themen werden Nebel und Informationen zur Verwendung verschiedener Nebel Features in Direct3D-Anwendungen vorgestellt.

-   [Nebel Formeln (Direct3D 9)](fog-formulas.md)
-   [Nebel Parameter (Direct3D 9)](fog-parameters.md)
-   [Nebel Mischung (Direct3D 9)](fog-blending.md)
-   [Nebelfarbe (Direct3D 9)](fog-color.md)
-   [Scheitelpunkt Nebel (Direct3D 9)](vertex-fog.md)
-   [Pixel Nebel (Direct3D 9)](pixel-fog.md)

Nebel Mischung wird durch Rendering-Zustände gesteuert. Sie ist nicht Teil der programmierbaren Pixel Pipeline.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Rendering](direct3d-rendering.md)
</dt> </dl>

 

 



