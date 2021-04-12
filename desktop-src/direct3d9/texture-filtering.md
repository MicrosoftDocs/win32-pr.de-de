---
description: Wenn Direct3D ein primitiv rendert, ordnet es den 3D-primitiv einem 2D-Bildschirm zu.
ms.assetid: vs|directx_sdk|~\texture_filtering.htm
title: Textur Filterung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faeeb83e1a3bc7fc03534771b15b6076aeb48f8c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482038"
---
# <a name="texture-filtering-direct3d-9"></a>Textur Filterung (Direct3D 9)

Wenn Direct3D ein primitiv rendert, ordnet es den 3D-primitiv einem 2D-Bildschirm zu. Wenn das primitiv eine Textur hat, muss Direct3D diese Textur verwenden, um für jedes Pixel im 2D-gerenderten Bild des primitiven eine Farbe zu schaffen. Für jedes Pixel im Bildschirm Bild des primitiven muss ein Farbwert aus der Textur abgerufen werden. Dieser Vorgang wird als Textur Filterung bezeichnet.

Wenn ein Textur Filter Vorgang durchgeführt wird, wird die verwendete Textur in der Regel auch vergrößert oder minimiert. Das heißt, Sie wird einem primitiven Bild zugeordnet, das größer oder kleiner als sich selbst ist. Die Vergrößerung einer Textur kann dazu führen, dass viele Pixel einem textextset zugeordnet werden. Das Ergebnis kann eine segmentierte Darstellung sein. Die Minimierung einer Textur bedeutet häufig, dass ein einzelnes Pixel vielen texeln zugeordnet wird. Das resultierende Bild kann verschwommen oder Alias sein. Um diese Probleme zu beheben, müssen Sie eine Mischung der texelfarben durchführen, um eine Farbe für das Pixel zu erhalten.

Direct3D vereinfacht den komplexen Prozess der Textur Filterung. Sie bietet drei Typen von Textur filtern: lineare Filterung, anisotrope Filterung und MipMap-Filterung. Wenn Sie keine Textur Filterung auswählen, verwendet Direct3D eine Technik, die als "Next-Point Sampling" bezeichnet wird.

Jeder Typ der Textur Filterung hat vor-und Nachteile. Beispielsweise kann die lineare Textur Filterung verzweigte Kanten oder eine segmentierte Darstellung im endgültigen Bild verursachen. Dabei handelt es sich jedoch um eine Berechnungsmethode mit geringem Aufwand für die Textur Filterung. Das Filtern mit Mipmaps erzeugt in der Regel die besten Ergebnisse, insbesondere in Kombination mit der anisotrope Filterung. Allerdings ist es erforderlich, dass die von Direct3D unterstützten Techniken den meisten Speicherplatz benötigen.

Anwendungen, die Textur Schnittstellen Zeiger verwenden, müssen die aktuelle Textur Filterungs Methode durch Aufrufen der [**IDirect3DDevice9:: setsamplerstate**](/windows/desktop/api) -Methode festlegen. Legen Sie den Wert des ersten Parameters auf die ganzzahlige Indexnummer (0-7) der Textur fest, für die Sie eine Textur Filterungs Methode auswählen. Übergeben \_ Sie D3DSAMP MagFilter, D3DSAMP \_ MinFilter oder D3DSAMP \_ MipFilter für den zweiten Parameter, um den Filter für die Vergrößerung, minifizierung oder den Mipmapping-Filter festzulegen. Übergeben Sie einen Member des [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) -enumerierten Typs als Wert im dritten Parameter.

In diesem Abschnitt werden die von Direct3D unterstützten Textur Filter Methoden vorgestellt. Es ist in die folgenden Themen unterteilt.

-   [Stichprobenentnahme am nächsten Punkt (Direct3D 9)](nearest-point-sampling.md)
-   [Lineare Textur Filterung (Direct3D 9)](linear-texture-filtering.md)
-   [Bilineare Textur Filterung (Direct3D 9)](bilinear-texture-filtering.md)
-   [Anisotrope Textur Filterung (Direct3D 9)](anisotropic-texture-filtering.md)
-   [Textur Filterung mit Mipmaps (Direct3D 9)](texture-filtering-with-mipmaps.md)

> [!Note]  
> Obwohl die im [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) -Enumerationstyp enthaltenen renderzustände für die Textur Filterung durch den Text der Textur Stufen abgelöst werden, schlägt [**IDirect3DDevice9:: seetrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)nicht fehl, wenn Sie versuchen, Sie zu verwenden. Stattdessen ordnet das System die Auswirkungen dieser renderzustände der ersten Phase in der Multitextur Cascade, Phase 0 zu. Anwendungen sollten die Legacy-Rendering-Zustände nicht mit den entsprechenden Textur Stufen Zuständen vermischen, da unvorhersehbare Ergebnisse auftreten können.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
