---
description: Legt ein Array von Gleit Komma Zahlen fest.
ms.assetid: 8e64b569-a6bf-4925-9d21-4df0b6661ee2
title: 'ID3DXTextureShader:: setfloatarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5dbd39e8a4acfa004fb623d578e5922d477884fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219539"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a>ID3DXTextureShader:: setfloatarray-Methode

Legt ein Array von Gleit Komma Zahlen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hconstant* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für das Array von Konstanten. Siehe [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*PF* \[ in\]
</dt> <dd>

Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***

Array von Gleit Komma Zahlen.

</dd> <dt>

*Anzahl* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl von Gleit Komma Werten im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
