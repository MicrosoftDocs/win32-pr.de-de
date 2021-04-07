---
description: Direct3D kann in einem einzelnen Durchlauf beliebig viele bis acht Texturen in primitive kombinieren.
ms.assetid: vs|directx_sdk|~\texture_blending.htm
title: Textur Mischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a89a87160bb85c1f62339380d46fa4b39736609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747617"
---
# <a name="texture-blending-direct3d-9"></a>Textur Mischung (Direct3D 9)

Direct3D kann in einem einzelnen Durchlauf beliebig viele bis acht Texturen in primitive kombinieren. Die Verwendung mehrerer Textur Mischungs Möglichkeiten kann die Framerate einer Direct3D-Anwendung erheblich erhöhen. Eine Anwendung verwendet mehrere Textur Mischungs Zeichen, um Texturen, Schatten, Glanzlichter, diffuse Beleuchtung und andere besondere Effekte in einem einzigen Durchlauf anzuwenden.

Zur Verwendung von Textur Mischungen sollte Ihre Anwendung zunächst überprüfen, ob Sie von der Hardware des Benutzers unterstützt wird. Diese Informationen finden Sie im TextureCaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur. Ausführliche Informationen zum Abfragen der Hardware des Benutzers für Textur Mischungs Funktionen finden Sie unter [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).

## <a name="texture-stages-and-the-texture-blending-cascade"></a>Textur Stufen und die Textur Mischungs kaskadieren

Direct3D unterstützt durch die Verwendung von Textur Stufen eine multidurchlauf-Mischung mehrerer Textur. Eine Textur Phase nimmt zwei Argumente an und führt einen Mischungs Vorgang für Sie durch, um das Ergebnis zur weiteren Verarbeitung oder für die rasterisierung zu übergeben. Sie können eine Textur Phase visualisieren, wie in der folgenden Abbildung dargestellt.

![Diagramm einer Textur Phase](images/texstg.png)

Wie das obige Diagramm zeigt, mischen Textur Stufen zwei Argumente mit einem angegebenen Operator. Häufige Vorgänge umfassen eine einfache Modulation oder Addition der Farb-oder Alpha Komponenten der Argumente, es werden jedoch mehr als zwei Dutzend Vorgänge unterstützt. Die Argumente für eine Stufe können eine zugeordnete Textur, die Iterierte Farbe oder Alpha (iteriert während der Schattierung von Gouraud), beliebige Farbe und Alpha oder das Ergebnis aus der vorherigen Textur Phase sein. Weitere Informationen finden Sie unter [Textur Mischungs Vorgänge und Argumente (Direct3D 9)](texture-blending-operations-and-arguments.md).

> [!Note]  
> Direct3D unterscheidet Farbmischung aus Alpha Blending. Anwendungen legen Mischungs Vorgänge und Argumente für Farbe und Alpha einzeln fest, und die Ergebnisse dieser Einstellungen sind voneinander unabhängig.

 

Die Kombination von Argumenten und Vorgängen, die von mehreren Mischungs Stufen verwendet werden, definiert eine einfache, Fluss basierte Mischungs Sprache. Die Ergebnisse aus einer Stufe werden in eine andere Phase übertragen, von dieser Phase bis zum nächsten, usw. Das Konzept der Ergebnisse, das von Phase zu Phase fließt und schließlich auf einem Polygon gerengt wird, wird häufig als Textur Mischungs Cascade bezeichnet. Das folgende Diagramm zeigt, wie einzelne Textur Stufen die Textur Mischungs Cascade bilden.

![Diagramm der Textur Stufen in der Textur Mischungs Cascade](images/tcascade.png)

Jede Stufe in einem Gerät weist einen NULL basierten Index auf. Direct3D ermöglicht bis zu acht Mischungs Phasen, aber Sie sollten immer Gerätefunktionen überprüfen, um zu bestimmen, wie viele Stufen die aktuelle Hardware unterstützt. Die erste Mischungs Stufe ist am Index 0, die zweite auf 1 usw. bis zu Index 7. Das System kombiniert Phasen in zunehmender Index Reihenfolge.

Verwenden Sie nur die Anzahl der Stufen, die Sie benötigen. die nicht verwendeten Mischungs Stufen sind standardmäßig deaktiviert. Wenn die Anwendung also nur die ersten beiden Stufen verwendet, müssen nur Vorgänge und Argumente für Phase 0 und 1 festgelegt werden. Das System kombiniert die beiden Stufen und ignoriert die deaktivierten Phasen.

> [!Note]  
> Wenn Ihre Anwendung die Anzahl der Phasen variiert, die für verschiedene Situationen verwendet werden, z. b. vier Phasen für einige Objekte und nur zwei für andere, müssen Sie nicht alle zuvor verwendeten Phasen explizit deaktivieren. Eine Möglichkeit besteht darin, den Farb Vorgang für die erste nicht verwendete Phase zu deaktivieren, dann werden nicht alle Phasen mit einem höheren Index angewendet. Eine andere Möglichkeit besteht darin, die Textur Zuordnung vollständig zu deaktivieren, indem Sie den Farb Vorgang für die erste Textur Phase (Phase 0) auf D3DTOP \_ deaktivieren festlegen. Eine dritte Möglichkeit besteht darin, dass für eine Textur Phase D3DTSS \_ COLORARG1 gleich \_ der D3DTA-Textur und der Textur Zeiger für die Stufe **null** ist, wenn diese Phase und alle Phasen nach der Verarbeitung nicht verarbeitet werden.

 

Weitere Informationen finden Sie in den folgenden Themen.

-   [Textur Mischungs Vorgänge und Argumente (Direct3D 9)](texture-blending-operations-and-arguments.md)
-   [Zuweisen der aktuellen Texturen (Direct3D 9)](assigning-the-current-textures.md)
-   [Erstellen von Mischungs Stufen (Direct3D 9)](creating-blending-stages.md)
-   [Alpha Textur Mischung (Direct3D 9)](alpha-texture-blending.md)
-   [Multipass-Textur Mischung (Direct3D 9)](multipass-texture-blending.md)
-   [Einfache Zuordnung mit Texturen (Direct3D 9)](light-mapping-with-textures.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
