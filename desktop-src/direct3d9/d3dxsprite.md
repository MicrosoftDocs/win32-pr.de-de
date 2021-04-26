---
description: 'Die folgenden Flags werden verwendet, um Sprite-Renderingoptionen für den flags-Parameter in der Begin-Methode anzugeben:'
ms.assetid: 195ee969-30e8-4828-a0be-f0d2a82e247c
title: D3DXSPRITE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4dbf3e80e7cf6f7884d778860f9de61f5193f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997317"
---
# <a name="d3dxsprite"></a>D3DXSPRITE

Die folgenden Flags werden verwendet, um Sprite-Renderingoptionen für den flags-Parameter in der [**Begin-Methode**](id3dxsprite--begin.md) anzugeben:



| \#Definieren                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXSPRITE \_ DONOTSAVESTATE           | Der Gerätestatus darf nicht gespeichert oder wiederhergestellt werden, wenn [**Begin**](id3dxsprite--begin.md) oder [**End**](id3dxsprite--end.md) aufgerufen wird.                                                                                                                                                                                                                                                                                            |
| D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE | Der Renderzustand des Geräts darf nicht geändert werden, wenn [**Begin**](id3dxsprite--begin.md) aufgerufen wird. Es wird davon ausgegangen, dass sich das Gerät in einem gültigen Zustand befindet, um Scheitelzeichen mit UsageIndex = 0 in den Farbdaten D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ TEXCOORD und D3DDECLUSAGE \_ COLOR zu zeichnen.                                                                                                                                                     |
| D3DXSPRITE \_ OBJECTSPACE              | Die Welt-, Ansichts- und Projektionstransformationen werden nicht geändert. Die derzeit auf das Gerät festgelegten Transformationen werden verwendet, um die Sprites zu transformieren, wenn die Batch-Sprites gezeichnet werden (wenn [**Flush**](id3dxsprite--flush.md) oder [**End**](id3dxsprite--end.md) aufgerufen wird). Wenn dieses Flag nicht angegeben wird, werden Die Transformationen für Welt, Ansicht und Projektion so geändert, dass Sprites in Bildschirmraumkoordinaten gezeichnet werden.              |
| D3DXSPRITE \_ PLAYLIST                | Jedes Sprite wird um seinen Mittelpunkt gedreht, sodass er dem Betrachter angezeigt wird. [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) oder [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) muss zuerst aufgerufen werden.                                                                                                                                                                                                                |
| D3DXSPRITE \_ ALPHABLEND               | Aktiviert alpha blending mit D3DRS \_ ALPHATESTENABLE, das auf TRUE festgelegt **ist** (für Alpha ungleich 0 (null). D3DBLEND SRCALPHA ist der Quellmischungszustand, und \_ D3DBLEND INVSRCALPHA ist der Zielmischungszustand in Aufrufen von \_ [**SetRenderState.**](/windows/desktop/api) Weitere Informationen finden Sie unter [Alpha Blending State (Direct3D 9) (Alphamischungszustand (Direct3D 9)).](alpha-blending-state.md) [**ID3DXFont**](id3dxfont.md) erwartet, dass dieses Flag beim Zeichnen von Text festgelegt wird. |
| D3DXSPRITE \_ SORT \_ TEXTURE            | Sortieren Sie Sprites vor dem Zeichnen nach Textur. Dies kann die Leistung beim Zeichnen nicht überlappender Sprites mit einheitlicher Tiefe verbessern. Sie können auch D3DXSPRITE \_ SORT \_ TEXTURE mit D3DXSPRITE \_ SORT DEPTH \_ \_ FRONTTOBACK oder D3DXSPRITE \_ SORT DEPTH \_ \_ BACKTOFRONT kombinieren. Dadurch wird die Liste der Sprites nach Tiefe zuerst und Textur zweite sortiert.<br/>                                                                           |
| D3DXSPRITE \_ SORT \_ DEPTH \_ FRONTTOBACK | Sprites werden vor dem Zeichnen nach Tiefe in Der-Rück-Reihenfolge sortiert. Dieses Verfahren wird empfohlen, wenn Sie nicht transparente Sprites unterschiedlicher Tiefe zeichnen. Sie können D3DXSPRITE \_ SORT \_ DEPTH \_ FRONTTOBACK mit D3DXSPRITE \_ SORT TEXTURE \_ kombinieren, um zuerst nach Tiefe und dann nach Textur zu sortieren.<br/>                                                                                                                                   |
| D3DXSPRITE \_ SORT \_ DEPTH \_ BACKTOFRONT | Sprites werden vor dem Zeichnen nach Tiefe in der Reihenfolge von vorn sortiert. Dieses Verfahren wird empfohlen, wenn Transparente Sprites unterschiedlicher Tiefe gezeichnet werden. Sie können D3DXSPRITE \_ SORT \_ DEPTH \_ BACKTOFRONT mit D3DXSPRITE \_ SORT TEXTURE \_ kombinieren, um zuerst nach Tiefe und dann nach Textur zu sortieren.<br/>                                                                                                                              |
| D3DXSPRITE \_ DO \_ NOT \_ ADDREF \_ TEXTURE | Deaktiviert den Aufruf von AddRef() bei jedem Zeichnen und Release() für Flush(), um eine bessere Leistung zu erzielen.                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="constant-information"></a>Konstanteninformationen



|                          |             |
|--------------------------|-------------|
| Header                   | d3dx9core.h |
| Mindestbetriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX-Konstanten](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




