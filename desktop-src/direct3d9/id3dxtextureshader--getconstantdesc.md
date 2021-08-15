---
description: Ruft einen Zeiger auf das Array von Konstanten in der konstanten Tabelle ab.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: ID3DXTextureShader::GetConstantDesc-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f8c7f65c9f2096339e0131d5d54c2fd65fb7e52849219f06f6a60fd44c518751
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095670"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a>ID3DXTextureShader::GetConstantDesc-Methode

Ruft einen Zeiger auf das Array von Konstanten in der konstanten Tabelle ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hConstant* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für eine Konstante. Siehe [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pDesc* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***

Gibt einen Zeiger auf ein Array von Beschreibungen zurück. Siehe [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md).

</dd> <dt>

*pCount* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Die bereitgestellte Eingabe muss die maximale Größe des Arrays sein. Die Ausgabe ist die Anzahl der Elemente, die im Array aufgefüllt werden, wenn die Funktion zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Sampler können in einer konstanten Tabelle mehr als einmal angezeigt werden. Daher kann diese Methode ein Array von Beschreibungen mit jeweils einem anderen Registerindex zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> <dt>

[**ID3DXTextureShader::GetDesc**](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
