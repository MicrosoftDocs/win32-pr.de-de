---
description: Ruft eine Passbeschreibung ab.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: ID3DXBaseEffect::GetPassDesc-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 74106bc38367e13cd70af94d0ad12016165aaae24693f19386e69ebe1d7a5cb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987750"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a>ID3DXBaseEffect::GetPassDesc-Methode

Ruft eine Passbeschreibung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPass* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Passhand handle. Siehe [Handles (Direct3D 9).](handles.md)

</dd> <dt>

*pDesc* \[ out\]
</dt> <dd>

Typ: **[ **D3DXPASS \_ DESC**](d3dxpass-desc.md)\***

Gibt eine Beschreibung des angegebenen Durchgangs zurück. Siehe [**D3DXPASS \_ DESC**](d3dxpass-desc.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Wenn ein Effekt mit [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md)erstellt wird, gibt diese Methode **NULL-Zeiger** (in [**D3DXPASS \_ DESC)**](d3dxpass-desc.md)an die Shaderfunktionen zurück.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




