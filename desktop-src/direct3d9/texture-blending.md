---
description: Direct3D kann bis zu acht Texturen in einem einzigen Durchlauf in Primitive einfügen.
ms.assetid: vs|directx_sdk|~\texture_blending.htm
title: Texturmischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688be4c80fb87d0d96f8f930ed85c9cc934fc4392151196ec0c510a4cbe482bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291604"
---
# <a name="texture-blending-direct3d-9"></a>Texturmischung (Direct3D 9)

Direct3D kann bis zu acht Texturen in einem einzigen Durchlauf in Primitive einfügen. Die Verwendung mehrerer Texturmischungen kann die Bildfrequenz einer Direct3D-Anwendung erheblich erhöhen. Eine Anwendung verwendet mehrere Texturmischungen, um Texturen, Schatten, Glanzlicht, diffuse Beleuchtung und andere Spezielle Effekte in einem einzigen Durchlauf anzuwenden.

Um Texturmischung zu verwenden, sollte Ihre Anwendung zunächst überprüfen, ob die Hardware des Benutzers dies unterstützt. Diese Informationen finden Sie im TextureCaps-Member der [**D3DCAPS9-Struktur.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) Ausführliche Informationen zum Abfragen der Hardware des Benutzers nach Texturmischungsfunktionen finden Sie unter [**IDirect3DDevice9::GetDeviceCaps.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)

## <a name="texture-stages-and-the-texture-blending-cascade"></a>Texturstufen und die Texturblending Cascade

Direct3D unterstützt die Mehrfachmischung mehrerer Texturen mit nur einem Durchlauf durch die Verwendung von Texturstufen. Eine Texturphase verwendet zwei Argumente und führt eine Mischungsoperation für sie aus, wobei das Ergebnis zur weiteren Verarbeitung oder zur Rasterung übergeben wird. Sie können eine Texturphase wie im folgenden Diagramm dargestellt visualisieren.

![Diagramm einer Texturphase](images/texstg.png)

Wie das obige Diagramm zeigt, mischen Texturstufen zwei Argumente mithilfe eines angegebenen Operators. Zu den gängigen Vorgängen zählen einfache Operationen oder das Hinzufügen der Farb- oder Alphakomponenten der Argumente, aber mehr als zwei Dutzend Vorgänge werden unterstützt. Die Argumente für eine Stufe können eine zugeordnete Textur, die durchlaufene Farbe oder alpha (während der Gouraud-Schattierung durchlaufen), beliebige Farbe und Alpha oder das Ergebnis der vorherigen Texturphase sein. Weitere Informationen finden Sie unter [Texturmischungsvorgänge und -argumente (Direct3D 9).](texture-blending-operations-and-arguments.md)

> [!Note]  
> Direct3D unterscheidet die Farbmischung von der Alphablending. Anwendungen legen Blendingvorgänge und Argumente für Farbe und Alpha einzeln fest, und die Ergebnisse dieser Einstellungen sind voneinander unabhängig.

 

Die Kombination aus Argumenten und Vorgängen, die von mehreren Überblendungsphasen verwendet werden, definiert eine einfache flussbasierte Mischungssprache. Die Ergebnisse von einer Phase fließen in eine andere Phase, von dieser Phase zur nächsten usw. Das Konzept der Ergebnisse, die von Phase zu Phase fließen, um schließlich auf einem Polygon gerastert zu werden, wird häufig als Texturmischung kaskadiert bezeichnet. Das folgende Diagramm zeigt, wie einzelne Texturstufen die Texturmischung kaskadieren.

![Diagramm der Texturstufen in der Texturmischung kaskadiert](images/tcascade.png)

Jede Phase eines Geräts verfügt über einen nullbasierten Index. Direct3D ermöglicht bis zu acht Blendingstufen, obwohl Sie die Gerätefunktionen immer überprüfen sollten, um zu bestimmen, wie viele Phasen die aktuelle Hardware unterstützt. Die erste Mischungsphase befindet sich bei Index 0, die zweite bei 1 usw. bis index 7. Das System kombiniert Phasen in zunehmender Indexreihenfolge.

Verwenden Sie nur die Anzahl der benötigten Phasen. Die nicht verwendeten Blendingstufen sind standardmäßig deaktiviert. Wenn Ihre Anwendung also nur die ersten beiden Phasen verwendet, müssen sie nur Vorgänge und Argumente für Phase 0 und 1 festlegen. Das System kombiniert die beiden Phasen und ignoriert die deaktivierten Phasen.

> [!Note]  
> Wenn Ihre Anwendung die Anzahl von Phasen variiert, die sie für verschiedene Situationen verwendet – z. B. vier Phasen für einige Objekte und nur zwei für andere –, müssen Sie nicht alle zuvor verwendeten Phasen explizit deaktivieren. Eine Möglichkeit besteht darin, den Farbvorgang für die erste nicht verwendete Phase zu deaktivieren, dann werden nicht alle Phasen mit einem höheren Index angewendet. Eine weitere Möglichkeit besteht darin, die Texturzuordnung vollständig zu deaktivieren, indem Sie den Farbvorgang für die erste Texturstufe (Stufe 0) auf D3DTOP \_ DISABLE festlegen. Eine dritte Option ist, wenn eine Texturphase D3DTSS \_ COLORARG1 gleich D3DTA TEXTURE hat \_ und der Texturzeiger für die Stufe **NULL** ist, diese Phase und alle Phasen, nachdem sie nicht verarbeitet wurden.

 

Weitere Informationen finden Sie in den folgenden Themen.

-   [Texturmischungsvorgänge und -argumente (Direct3D 9)](texture-blending-operations-and-arguments.md)
-   [Zuweisen der aktuellen Texturen (Direct3D 9)](assigning-the-current-textures.md)
-   [Erstellen von Blendingstufen (Direct3D 9)](creating-blending-stages.md)
-   [Alphatexturmischung (Direct3D 9)](alpha-texture-blending.md)
-   [Multipass-Texturmischung (Direct3D 9)](multipass-texture-blending.md)
-   [Lichtzuordnung mit Texturen (Direct3D 9)](light-mapping-with-textures.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
