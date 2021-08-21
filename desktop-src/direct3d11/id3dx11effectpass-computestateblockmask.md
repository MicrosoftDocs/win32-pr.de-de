---
title: ID3DX11EffectPass ComputeStateBlockMask-Methode (D3dx11effect.h)
description: Generieren Sie eine Maske zum Zulassen/Verhindern von Zustandsänderungen.
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- ComputeStateBlockMask-Methode Direct3D 11
- ComputeStateBlockMask-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11, ComputeStateBlockMask-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17198c076d200631142207189059ada425e9ec1ddf6e3c8a8d40499e40aa21a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535056"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a>ID3DX11EffectPass::ComputeStateBlockMask-Methode

Generieren Sie eine Maske zum Zulassen/Verhindern von Zustandsänderungen.

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





