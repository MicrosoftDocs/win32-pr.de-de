---
description: Wenn Direct3D einen Primitiven rendert, wird der 3D-Primitiv einem 2D-Bildschirm zugeordnet.
ms.assetid: vs|directx_sdk|~\texture_filtering.htm
title: Texturfilterung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758ee51df65ffa4dddf793db83fe618107886cd4c20497f0e8090373a1415beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291175"
---
# <a name="texture-filtering-direct3d-9"></a>Texturfilterung (Direct3D 9)

Wenn Direct3D einen Primitiven rendert, wird der 3D-Primitiv einem 2D-Bildschirm zugeordnet. Wenn das Primitiv über eine Textur verfügt, muss Direct3D diese Textur verwenden, um eine Farbe für jedes Pixel im gerenderten 2D-Bild des Primitiven zu erzeugen. Für jedes Pixel im Bild des Primitiven auf dem Bildschirm muss es einen Farbwert aus der Textur abrufen. Dieser Prozess wird als Texturfilterung bezeichnet.

Wenn ein Texturfiltervorgang ausgeführt wird, wird die verwendete Textur in der Regel ebenfalls vergrößert oder verknöpft. Anders ausgedrückt: Es wird einem primitiven Bild zugeordnet, das größer oder kleiner als selbst ist. Die Vergrößerung einer Textur kann dazu führen, dass viele Pixel einem Texel zugeordnet werden. Das Ergebnis kann eine segmentige Darstellung sein. Die Minifizierung einer Textur bedeutet häufig, dass vielen Texel ein einzelnes Pixel zugeordnet wird. Das resultierende Bild kann unscharf oder mit einem Alias dargestellt werden. Um diese Probleme zu beheben, müssen einige Mischungen der Texelfarben durchgeführt werden, um eine Farbe für das Pixel zu erhalten.

Direct3D vereinfacht den komplexen Prozess der Texturfilterung. Sie bietet drei Arten der Texturfilterung: lineare Filterung, Anisotrope Filterung und Mipmapfilterung. Wenn Sie keine Texturfilterung auswählen, verwendet Direct3D eine Technik namens Nearest-Point Sampling.

Jede Art von Texturfilterung hat Vor- und Nachteile. Die lineare Texturfilterung kann z. B. verzweigte Kanten oder eine segmentierte Darstellung im endgültigen Bild erzeugen. Es handelt sich jedoch um eine Methode mit geringem Rechenaufwand für die Texturfilterung. Das Filtern mit Mipmaps liefert in der Regel die besten Ergebnisse, insbesondere in Kombination mit anisotroper Filterung. Es ist jedoch der größte Arbeitsspeicher der Von Direct3D unterstützten Techniken erforderlich.

Anwendungen, die Texturschnittstellenzeiger verwenden, sollten die aktuelle Texturfiltermethode festlegen, indem sie die [**IDirect3DDevice9::SetSamplerState-Methode**](/windows/desktop/api) aufrufen. Legen Sie den Wert des ersten Parameters auf die ganzzahlige Indexnummer (0-7) der Textur fest, für die Sie eine Texturfilterungsmethode auswählen. Übergeben Sie D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER oder D3DSAMP \_ MIPFILTER für den zweiten Parameter, um den Filter für Vergrößerung, Vergrößerung oder Mipmapping festzulegen. Übergeben Sie einen Member des [**enumerationierten D3DTEXTUREFILTERTYPE-Typs**](./d3dtexturefiltertype.md) als Wert im dritten Parameter.

In diesem Abschnitt werden die Texturfiltermethoden vorgestellt, die Direct3D unterstützt. Sie ist in die folgenden Themen unterteilt.

-   [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md)
-   [Lineare Texturfilterung (Direct3D 9)](linear-texture-filtering.md)
-   [Bilineare Texturfilterung (Direct3D 9)](bilinear-texture-filtering.md)
-   [Anisotrope Texturfilterung (Direct3D 9)](anisotropic-texture-filtering.md)
-   [Texturfilterung mit Mipmaps (Direct3D 9)](texture-filtering-with-mipmaps.md)

> [!Note]  
> Obwohl die Renderzustände der Texturfilterung, die im [**D3DRENDERSTATETYPE-Enumerationstyp**](./d3drenderstatetype.md) vorhanden sind, durch Texturphasenzustände ersetzt werden, schlägt [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)im Gegensatz zur IDirect3DDevice2-Version nicht fehl, wenn Sie versuchen, sie zu verwenden. Stattdessen ordnet das System die Auswirkungen dieser Renderzustände der ersten Stufe in der Multitexture-Kaskadierung , Phase 0, zu. Anwendungen sollten die Legacyrenderzustände nicht mit den entsprechenden Texturphasenzuständen kombinieren, da unvorhersehbare Ergebnisse auftreten können.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
