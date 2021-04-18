---
description: Löschen Sie einen Parameter Block.
ms.assetid: 5502dabc-1703-481b-a69d-f6bd8fd01d20
title: ID3DXEffect::D eleteparameterblock-Methode (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.DeleteParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 483b09ebf308b8cdfa14d714bc74786e5fcb1f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351952"
---
# <a name="id3dxeffectdeleteparameterblock-method"></a>ID3DXEffect::D eleteparameterblock-Methode

Löschen Sie einen Parameter Block.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

 *hparameterblock* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Ein Handle für den Parameter Block. Dies ist das Handle, das von [**ID3DXEffect:: endparameterblock**](id3dxeffect--endparameterblock.md)zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Parameter Blöcke sind Blöcke von Effekt Zuständen. Verwenden Sie einen Parameter Block zum Aufzeichnen von Zustandsänderungen, sodass Sie später mit einem einzigen API-Befehl angewendet werden können. Löschen Sie den Parameter Block, wenn er nicht mehr benötigt wird, um die Speicherauslastung zu reduzieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: beginparameterblock**](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[**ID3DXEffect:: endparameterblock**](id3dxeffect--endparameterblock.md)
</dt> </dl>

 

 




