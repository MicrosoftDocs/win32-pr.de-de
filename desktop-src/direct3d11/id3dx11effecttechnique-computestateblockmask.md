---
title: ID3DX11EffectTechnique ComputeStateBlockMask-Methode (D3dx11effect.h)
description: Berechnen Sie eine Zustandsblockmaske, um Zustandsänderungen zu ermöglichen bzw. zu verhindern.
ms.assetid: 4fd6061d-6ca5-4e3f-b031-fae98f3de057
keywords:
- ComputeStateBlockMask-Methode Direct3D 11
- ComputeStateBlockMask-Methode Direct3D 11, ID3DX11EffectTechnique-Schnittstelle
- ID3DX11EffectTechnique-Schnittstelle Direct3D 11, ComputeStateBlockMask-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf7a221cd685eb31b068ae6144514adb70ffa42c654d9e1a3249db5302e0aa6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894760"
---
# <a name="id3dx11effecttechniquecomputestateblockmask-method"></a>ID3DX11EffectTechnique::ComputeStateBlockMask-Methode

Berechnen Sie eine Zustandsblockmaske, um Zustandsänderungen zu ermöglichen bzw. zu verhindern.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStateBlockMask* 
</dt> <dd>

Typ: **[ **D3DX11 \_ STATE \_ BLOCK \_ MASK**](d3dx11-state-block-mask.md)\***

Ein Zeiger auf eine Zustandsblockmaske (siehe [**D3DX11 \_ STATE \_ BLOCK \_ MASK**](d3dx11-state-block-mask.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

 





