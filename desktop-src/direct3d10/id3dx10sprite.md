---
description: Die ID3DX10Sprite-Schnittstelle stellt eine Reihe von Methoden bereit, die das Zeichnen von Sprites mithilfe von Microsoft Direct3D vereinfachen. Diese Schnittstelle kann für eine Reihe von Sprites verwendet werden.
ms.assetid: 3703f272-f631-41c0-a0d5-e7cf2d4ae145
title: ID3DX10Sprite-Schnittstelle (d3dx10. h)
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
ms.openlocfilehash: 7b21cab26ac0929882727028775849329ac10db7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351991"
---
# <a name="id3dx10sprite-interface"></a>ID3DX10Sprite-Schnittstelle

Die ID3DX10Sprite-Schnittstelle stellt eine Reihe von Methoden bereit, die das Zeichnen von Sprites mithilfe von Microsoft Direct3D vereinfachen. Diese Schnittstelle kann für eine Reihe von Sprites verwendet werden.

## <a name="members"></a>Member

Die **ID3DX10Sprite** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DX10Sprite** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10Sprite** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Starten**](id3dx10sprite-begin.md)                                   | Bereiten Sie ein Gerät zum Zeichnen von Sprites vor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Drawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md)       | Fügen Sie dem Batch von Sprites, die gerendert werden sollen, ein Array von Sprites hinzu. Dies muss zwischen Aufrufen von [**ID3DX10Sprite:: begin**](id3dx10sprite-begin.md) und [**ID3DX10Sprite:: End**](id3dx10sprite-end.md)aufgerufen werden, und [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) muss vor Ende aufgerufen werden, um alle Batch Sprites zum Rendering an das Gerät zu senden. Diese Draw-Methode ist besonders nützlich, wenn Sie eine kleine Anzahl von Sprites zeichnen möchten, die Sie in einem großen Batch, wie z. b. Schriftarten, gepuffert werden<br/>                                                                                                                                                                              |
| [**Drawspritesimvermittler**](id3dx10sprite-drawspritesimmediate.md)     | Zeichnen Sie ein Array von Sprites. Dadurch werden die Sprites sofort zum Rendern an das Gerät gesendet. Dies unterscheidet sich von [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) , das nur ein Array von Sprites zu einem Batch von Sprites hinzufügt, die gerendert werden, wenn [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) aufgerufen wird. Diese Draw-Methode ist besonders nützlich, wenn eine große Anzahl von Sprites gezeichnet wird, die bereits auf der CPU sortiert wurden (oder nicht sortiert werden müssen), z. b. in einem Partikelsystem. Dies muss zwischen Aufrufen von [**ID3DX10Sprite:: begin**](id3dx10sprite-begin.md) und [**ID3DX10Sprite:: End**](id3dx10sprite-end.md)aufgerufen werden.<br/> |
| [**ENDE**](id3dx10sprite-end.md)                                       | Nennen Sie dies nach ID3DX10Sprite:: Flush. Wenn \_ beim Aufruf von \_ \_ ID3DX10Sprite:: Begin der d3dx10 Sprite-Speicher Zustand angegeben wurde, stellt diese API den Gerätezustand vor dem Aufruf von ID3DX10Sprite:: begin wieder her.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Leerung**](id3dx10sprite-flush.md)                                   | Erzwingen, dass alle Batch-Sprites an das Gerät übermittelt werden. Gerätezustände verbleiben nach dem letzten ID3DX10Sprite:: begin-Rückruf. Die Liste der im Batch verarbeiteten Sprites wird dann gelöscht.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**GetDevice**](id3dx10sprite-getdevice.md)                           | Rufen Sie das Gerät ab, das dem Sprite-Objekt zugeordnet ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Getprojectiontransform**](id3dx10sprite-getprojectiontransform.md) | Holen Sie sich die Sprite-Projektions Matrix, die auf alle Sprites angewendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**GetViewTransform**](id3dx10sprite-getviewtransform.md)             | Hiermit wird die Ansichts Transformation für alle Sprites angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**Setprojectiontransform**](id3dx10sprite-setprojectiontransform.md) | Legen Sie die Projektions Matrix für alle Sprites fest.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**SetViewTransform**](id3dx10sprite-setviewtransform.md)             | Legen Sie die Ansichts Transformation fest, die für alle Sprites gilt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Bemerkungen

Die ID3DX10Sprite-Schnittstelle wird durch Aufrufen der [**D3DX10CreateSprite**](d3dx10createsprite.md) -Funktion abgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
