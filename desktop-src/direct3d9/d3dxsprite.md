---
description: 'Die folgenden Flags werden verwendet, um Sprite-Renderingoptionen für den flags-Parameter in der Begin-Methode anzugeben:'
ms.assetid: 195ee969-30e8-4828-a0be-f0d2a82e247c
title: D3DXSPRITE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e2247f414636039906277f882fb9dfc95f6b6b33aa29de2ac51a722c045901
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749760"
---
# <a name="d3dxsprite"></a>D3DXSPRITE

Die folgenden Flags werden verwendet, um Sprite-Renderingoptionen für den flags-Parameter in der [**Begin-Methode**](id3dxsprite--begin.md) anzugeben:



| \#Definieren                             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXSPRITE \_ DONOTSAVESTATE           | Der Gerätestatus darf nicht gespeichert oder wiederhergestellt werden, wenn [**Begin**](id3dxsprite--begin.md) oder [**End**](id3dxsprite--end.md) aufgerufen wird.                                                                                                                                                                                                                                                                                            |
| D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE | Der Renderzustand des Geräts darf nicht geändert werden, wenn [**Begin**](id3dxsprite--begin.md) aufgerufen wird. Es wird davon ausgegangen, dass sich das Gerät in einem gültigen Zustand befindet, um Scheitelzeichen zu zeichnen, die UsageIndex = 0 in den COLOR-Daten D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ TEXCOORD und D3DDECLUSAGE \_ enthalten.                                                                                                                                                     |
| D3DXSPRITE \_ OBJECTSPACE              | Die Welt-, Ansichts- und Projektionstransformationen werden nicht geändert. Die derzeit auf das Gerät festgelegten Transformationen werden verwendet, um die Sprites zu transformieren, wenn die Sprites in Batches gezeichnet werden (wenn [**Flush**](id3dxsprite--flush.md) oder [**End**](id3dxsprite--end.md) aufgerufen wird). Wenn dieses Flag nicht angegeben wird, werden Die Transformationen für Welt, Ansicht und Projektion so geändert, dass Sprites in Bildschirmraumkoordinaten gezeichnet werden.              |
| D3DXSPRITE \_ PLAYLIST                | Jedes Sprite wird um seinen Mittelpunkt gedreht, sodass er dem Betrachter angezeigt wird. [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) oder [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) muss zuerst aufgerufen werden.                                                                                                                                                                                                                |
| D3DXSPRITE \_ ALPHABLEND               | Aktiviert alpha blending mit D3DRS ALPHATESTENABLE, das auf TRUE festgelegt ist \_ (für Alpha ungleich null).  D3DBLEND SRCALPHA ist der Quellmischungszustand, und \_ D3DBLEND INVSRCALPHA ist der Zielmischungszustand in Aufrufen von \_ [**SetRenderState.**](/windows/desktop/api) Siehe [AlphaBlending State (Direct3D 9)](alpha-blending-state.md). [**ID3DXFont erwartet,**](id3dxfont.md) dass dieses Flag beim Zeichnen von Text festgelegt wird. |
| D3DXSPRITE \_ SORT \_ TEXTURE            | Sortieren Sie Sprites vor dem Zeichnen nach Textur. Dies kann die Leistung beim Zeichnen nicht überlappender Sprites mit einheitlicher Tiefe verbessern. Sie können auch D3DXSPRITE SORT TEXTURE mit \_ \_ D3DXSPRITE \_ SORT \_ DEPTH \_ FRONTTOBACK oder D3DXSPRITE \_ SORT DEPTH \_ \_ BACKTOFRONT kombinieren. Dadurch wird die Liste der Sprites nach Tiefe zuerst und Textur an zweiter Stelle sortiert.<br/>                                                                           |
| D3DXSPRITE \_ SORT \_ DEPTH \_ FRONTTOBACK | Sprites werden vor dem Zeichnen nach Tiefe in der Reihenfolge von vorne nach zurück sortiert. Dieses Verfahren wird empfohlen, wenn opake Sprites mit unterschiedlicher Tiefe gezeichnunget werden. Sie können D3DXSPRITE \_ SORT \_ DEPTH FRONTTOBACK mit \_ D3DXSPRITE SORT TEXTURE kombinieren, um zuerst nach Tiefe und zweitens nach \_ \_ Textur zu sortieren.<br/>                                                                                                                                   |
| D3DXSPRITE \_ SORT \_ DEPTH \_ BACKTOFRONT | Sprites werden vor dem Zeichnen nach Tiefe in der Back-to-Front-Reihenfolge sortiert. Dieses Verfahren wird empfohlen, wenn Transparente Sprites mit unterschiedlicher Tiefe gezeichnunget werden. Sie können D3DXSPRITE \_ SORT \_ DEPTH BACKTOFRONT mit \_ D3DXSPRITE SORT TEXTURE kombinieren, um zuerst nach Tiefe und zweitens nach \_ \_ Textur zu sortieren.<br/>                                                                                                                              |
| D3DXSPRITE \_ NICHT \_ \_ HINZUFÜGENREF-TEXTUR \_ | Deaktiviert den Aufruf von AddRef() bei jedem Zeichnen und Release() für Flush(), um die Leistung zu verbessern.                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="constant-information"></a>Konstante Informationen



| Anforderung                         | Wert            |
|--------------------------|-------------|
| Header                   | d3dx9core.h |
| Mindestbetriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX-Konstanten](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




