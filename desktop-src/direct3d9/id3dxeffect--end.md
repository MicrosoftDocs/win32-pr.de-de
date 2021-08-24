---
description: Beendet eine aktive Technik.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: ID3DXEffect::End-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6c93dc98febe2f5e539d3be678322860fe14069c2f8bf6b75cc42864b922e1f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748660"
---
# <a name="id3dxeffectend-method"></a>ID3DXEffect::End-Methode

Beendet eine aktive Technik.

## <a name="syntax"></a>Syntax


```C++
HRESULT End();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Diese Methode gibt immer den Wert S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Das gesamte Rendering in einem Effekt erfolgt innerhalb eines übereinstimmenden Paars von [**ID3DXEffect::Begin-**](id3dxeffect--begin.md) und **ID3DXEffect::End-Aufrufen.** Nachdem alle Durchläufe gerendert wurden, muss **ID3DXEffect::End** aufgerufen werden, um die aktive Technik zu beenden. Das Effektsystem reagiert mithilfe des Zustandsblocks, der beim Aufruf von **ID3DXEffect::Begin** erstellt wurde, um den Pipelinezustand automatisch vor **ID3DXEffect::Begin** wiederherzustellen.

Standardmäßig übernimmt das Effektsystem das Speichern des Zustands vor einer Technik und das Wiederherstellen des Zustands nach einer Technik. Wenn Sie diese Speicher- und Wiederherstellungsfunktion deaktivieren möchten, finden Sie weitere Informationen unter [D3DXFX \_ DONOTSAVESAMPLERSTATE.](d3dxfx.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




