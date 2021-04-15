---
description: 'Die folgenden Flags werden verwendet, um Sprite-Renderingoptionen für den flags-Parameter in der Begin-Methode anzugeben:'
ms.assetid: 195ee969-30e8-4828-a0be-f0d2a82e247c
title: D3DXSPRITE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c394d2606584ec5f56aa28661a2da286f000a66d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520379"
---
# <a name="d3dxsprite"></a>D3DXSPRITE

Die folgenden Flags werden verwendet, um Sprite-Renderingoptionen für den flags-Parameter in der [**Begin**](id3dxsprite--begin.md) -Methode anzugeben:



|                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definieren                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                       |
| D3DXSPRITE \_ DoNotSaveState           | Wenn [**Begin**](id3dxsprite--begin.md) oder [**End**](id3dxsprite--end.md) aufgerufen wird, muss der Gerätestatus nicht gespeichert oder wieder hergestellt werden.                                                                                                                                                                                                                                                                                            |
| D3DXSPRITE \_ donotmodify \_ renderstate | Der Zustand des Geräte Rendering muss nicht geändert werden, wenn [**Begin**](id3dxsprite--begin.md) aufgerufen wird. Es wird angenommen, dass sich das Gerät in einem gültigen Zustand befindet, um Vertices mit usageindex = 0 in den \_ Farbdaten D3DDECLUSAGE Position, D3DDECLUSAGE \_ texcoord und D3DDECLUSAGE zu zeichnen \_ .                                                                                                                                                     |
| D3DXSPRITE \_ ObjectSpace              | Die Transformationen "World", "View" und "Projection" werden nicht geändert. Die Transformationen, die derzeit auf das Gerät festgelegt sind, werden verwendet, um die Sprites zu transformieren, wenn die Batch Sprites gezeichnet werden (wenn das [**leeren oder das**](id3dxsprite--flush.md) [**Ende**](id3dxsprite--end.md) aufgerufen wird). Wenn dieses Flag nicht angegeben wird, werden globale, Ansichts-und Projektions Transformationen so geändert, dass Sprites in Bildschirmraum Koordinaten gezeichnet werden.              |
| D3DXSPRITE- \_ Billboard                | Jeder Sprite wird um seine Mitte gedreht, sodass er dem Viewer angezeigt wird. [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) oder [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) muss zuerst aufgerufen werden.                                                                                                                                                                                                                |
| D3DXSPRITE \_ AlphaBlend               | Ermöglicht Alpha Blending mit D3DRS Alpha \_ atestenable auf **true** (bei einem Alpha-Wert ungleich null). D3DBLEND \_ srcalpha ist der Quell-Blend-Status, und D3DBLEND \_ invsrcalpha ist der Ziel-Blend-Status in [](/windows/desktop/api)Aufrufen von "*". Siehe [Alpha Blending State (Direct3D 9)](alpha-blending-state.md). [**ID3DXFont**](id3dxfont.md) erwartet, dass dieses Flag beim Zeichnen von Text festgelegt wird. |
| D3DXSPRITE \_ Sortier \_ Textur            | Sortieren Sie Sprites nach Textur vor dem zeichnen. Dies kann die Leistung verbessern, wenn sich nicht überlappende Sprites mit einheitlicher Tiefe zeichnen. Sie können auch D3DXSPRITE \_ Sort \_ Texture entweder mit D3DXSPRITE \_ Sort \_ Tiefe \_ frontbackback oder D3DXSPRITE \_ Sort \_ Tiefe \_ backbackfront kombinieren. Dadurch wird die Liste der Sprites nach Tiefe und Textur Sekunde sortiert.<br/>                                                                           |
| D3DXSPRITE \_ - \_ Detail- \_ frontbackback | Sprites werden vor dem zeichnen nach Tiefe in der Reihenfolge vor dem Zeichnen sortiert. Diese Vorgehensweise wird empfohlen, wenn Sie transparente Sprites mit unterschiedlichen Tiefen zeichnen. Sie können D3DXSPRITE \_ Sort \_ Tiefe \_ frontbackback mit D3DXSPRITE \_ Sort Texture kombinieren \_ , um zuerst nach Tiefe zu sortieren, und zweitens nach Textur.<br/>                                                                                                                                   |
| D3DXSPRITE \_ Sortier \_ Tiefe zurück \_ wechseln | Sprites werden vor dem zeichnen nach Tiefe in der Back-to-Front-Reihenfolge sortiert. Diese Vorgehensweise wird empfohlen, wenn transparente Sprites mit unterschiedlichen Tiefen gezeichnet werden. Sie können D3DXSPRITE \_ Sort \_ Tiefe \_ backbackfront mit D3DXSPRITE \_ Sort Texture kombinieren \_ , um zuerst nach Tiefe zu sortieren, und zweitens nach Textur.<br/>                                                                                                                              |
| D3DXSPRITE \_ - \_ \_ Textur nicht Adressier \_ | Deaktiviert das Aufrufen von adressf () bei jedem Zeichnen und Release () bei Flush (), um die Leistung zu verbessern.                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="constant-information"></a>Konstante Informationen



|                          |             |
|--------------------------|-------------|
| Header                   | d3dx9core. h |
| Mindestens Betriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX-Konstanten](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




