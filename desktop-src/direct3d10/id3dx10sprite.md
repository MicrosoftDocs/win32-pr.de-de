---
description: Die ID3DX10Sprite-Schnittstelle stellt eine Reihe von Methoden bereit, die das Zeichnen von Sprites mithilfe von Microsoft Direct3D vereinfachen. Diese Schnittstelle kann für eine Reihe von Sprites verwendet werden.
ms.assetid: 3703f272-f631-41c0-a0d5-e7cf2d4ae145
title: ID3DX10Sprite-Schnittstelle (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8495d967d0f512e16a06506e73ac1a35bf5fa380924cdbe6513b06a43502b137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301928"
---
# <a name="id3dx10sprite-interface"></a>ID3DX10Sprite-Schnittstelle

Die ID3DX10Sprite-Schnittstelle stellt eine Reihe von Methoden bereit, die das Zeichnen von Sprites mithilfe von Microsoft Direct3D vereinfachen. Diese Schnittstelle kann für eine Reihe von Sprites verwendet werden.

## <a name="members"></a>Member

Die **ID3DX10Sprite-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10Sprite** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10Sprite-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Starten**](id3dx10sprite-begin.md)                                   | Bereiten Sie ein Gerät für das Zeichnen von Sprites vor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md)       | Fügen Sie dem Zu rendernden Sprites-Batch ein Array von Sprites hinzu. Dieser muss zwischen Aufrufen von [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) und [**ID3DX10Sprite::End**](id3dx10sprite-end.md)aufgerufen werden, und [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) muss vor End aufgerufen werden, um alle Batch-Sprites zum Rendern an das Gerät zu senden. Diese Zeichnen-Methode ist besonders nützlich, wenn Sie eine kleine Anzahl von Sprites zeichnen, die in einen großen Batch gepuffert werden soll, z. B. Schriftarten.<br/>                                                                                                                                                                              |
| [**DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md)     | Zeichnen sie ein Array von Sprites. Dadurch werden die Sprites sofort zum Rendern an das Gerät gesendet, was sich von [**ID3DX10Sprite::D rawSpritesBuffered abzeichnet,**](id3dx10sprite-drawspritesbuffered.md) das nur einem Batch von Sprites ein Array von Sprites hinzufügt, die gerendert werden, wenn [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) aufgerufen wird. Diese Zeichnen-Methode ist besonders nützlich, wenn eine große Anzahl von Sprites gezeichnunget wird, die bereits auf der CPU sortiert wurden (oder nicht sortiert werden müssen), z. B. in einem Partikelsystem. Diese muss zwischen Aufrufen von [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) und [**ID3DX10Sprite::End aufgerufen werden.**](id3dx10sprite-end.md)<br/> |
| [**Ende**](id3dx10sprite-end.md)                                       | Rufen Sie dies nach ID3DX10Sprite::Flush auf. Wenn D3DX10 SPRITE SAVE STATE angegeben wurde, als ID3DX10Sprite::Begin aufgerufen wurde, stellt diese API den Gerätestatus wie vor dem Aufruf von \_ \_ \_ ID3DX10Sprite::Begin wieder bereit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Leerung**](id3dx10sprite-flush.md)                                   | Erzwingen Sie, dass alle Sprites in Batches an das Gerät übermittelt werden. Gerätezustände bleiben nach dem letzten Aufruf von ID3DX10Sprite::Begin unverändert. Die Liste der Sprites in Batches wird dann wieder löschen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**GetDevice**](id3dx10sprite-getdevice.md)                           | Rufen Sie das Gerät ab, das dem Sprite-Objekt zugeordnet ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**GetProjectionTransform**](id3dx10sprite-getprojectiontransform.md) | Erhalten Sie die Sprite-Projektionsmatrix, die auf alle Sprites angewendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**GetViewTransform**](id3dx10sprite-getviewtransform.md)             | Hier erhalten Sie die Ansichtstransformation, die für alle Sprites gilt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**SetProjectionTransform**](id3dx10sprite-setprojectiontransform.md) | Legen Sie die Projektionsmatrix für alle Sprites fest.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**SetViewTransform**](id3dx10sprite-setviewtransform.md)             | Legen Sie die Ansichtstransformation fest, die für alle Sprites gilt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Hinweise

Die ID3DX10Sprite-Schnittstelle wird durch Aufrufen der [**D3DX10CreateSprite-Funktion**](d3dx10createsprite.md) ermittelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
