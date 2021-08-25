---
description: Ruft ein Array von BOOL-Werten ab.
ms.assetid: 4a5e2f48-fa82-47dc-a388-02a8679585d2
title: ID3DXBaseEffect::GetBoolArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 230970e1328737339f236776c1405b7a950ea97c07a04d60d9ce26d9226168e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848780"
---
# <a name="id3dxbaseeffectgetboolarray-method"></a>ID3DXBaseEffect::GetBoolArray-Methode

Ruft ein Array von BOOL-Werten ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBoolArray(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pB,
  [in]  UINT       Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Siehe [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pB* \[ out\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)\***

Gibt ein Array boolescher Werte zurück.

</dd> <dt>

*Anzahl* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der booleschen Werte im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetBoolArray**](id3dxbaseeffect--setboolarray.md)
</dt> </dl>

 

 
