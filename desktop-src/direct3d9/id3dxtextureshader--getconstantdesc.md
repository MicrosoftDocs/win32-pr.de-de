---
description: Ruft einen Zeiger auf das Array von Konstanten in der Konstanten Tabelle ab.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: 'ID3DXTextureShader:: getconstantdesc-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: 22898880e5cef5669defae89cda4f7d9818f9f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364384"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a>ID3DXTextureShader:: getconstantdesc-Methode

Ruft einen Zeiger auf das Array von Konstanten in der Konstanten Tabelle ab.

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

*hconstant* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für eine Konstante. Siehe [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*PDE SC* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***

Gibt einen Zeiger auf ein Array von Beschreibungen zurück. Weitere Informationen finden Sie unter [**D3DXCONSTANT \_**](d3dxconstant-desc.md).

</dd> <dt>

*pcount* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Die angegebene Eingabe muss die maximale Größe des Arrays sein. Bei der Ausgabe handelt es sich um die Anzahl der Elemente, die im Array aufgefüllt werden, wenn die Funktion zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Samplers können mehr als einmal in einer Konstanten Tabelle vorkommen. Daher kann diese Methode ein Array von Beschreibungen mit jeweils einem anderen Register Index zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> <dt>

[**ID3DXTextureShader:: getdebug**](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
