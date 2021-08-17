---
description: Die Umgebungszuordnung ist eine Technik, die stark reflektierende Oberflächen simuliert, ohne die Ray-Ablaufverfolgung zu verwenden.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Umgebungszuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a07d53028e200d273206f149ea12c07afa6dbc4ad47f8232e64cddf7582a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122222"
---
# <a name="environment-mapping-direct3d-9"></a>Umgebungszuordnung (Direct3D 9)

Die Umgebungszuordnung ist eine Technik, die stark reflektierende Oberflächen simuliert, ohne die Ray-Ablaufverfolgung zu verwenden. In der Praxis wendet die Umgebungszuordnung eine spezielle Texturkarte an, die ein Bild der Szene um ein Objekt enthält, auf das Objekt selbst. Das Ergebnis entspricht der Darstellung einer reflektierenden Oberfläche, die nah genug ist, um das Auge zu verleugnen, ohne dass eine der komplexen Berechnungen für die Ray-Ablaufverfolgung erforderlich ist.

Die folgende Abbildung veranschaulicht eine Art von Umgebungszuordnung, die als pherische Umgebungszuordnung bezeichnet wird. Weitere Informationen finden Sie unter [Pherical Environment Mapping](spherical-environment-mapping.md).

![Abbildung einer Teekanne mit einer angewendeten Textur, die die Umgebung widerspiegelt](images/spheremapped-teapot.png)

Die Teekanne in diesem Bild scheint ihre Umgebung widerzu spiegeln. dies ist tatsächlich eine Textur, die auf das -Objekt angewendet wird. Da die Umgebungszuordnung eine Textur in Kombination mit speziell berechneten Texturkoordinaten verwendet, kann sie in Echtzeit ausgeführt werden.

Dieser Abschnitt enthält Informationen zum Ausführen von zwei gängigen Typen von Umgebungszuordnungen mit Direct3D. Es gibt viele Arten von Umgebungszuordnungen, die in der gesamten Grafikbranche verwendet werden, aber die folgenden Themen zielen auf die beiden häufigsten Formen ab: kubische Umgebungszuordnung und pherische Umgebungszuordnung.

-   [Kubische Umgebungszuordnung](cubic-environment-mapping.md)
-   [Pherical Environment Mapping (pherische Umgebungszuordnung)](spherical-environment-mapping.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelpipeline](pixel-pipeline.md)
</dt> </dl>

 

 



