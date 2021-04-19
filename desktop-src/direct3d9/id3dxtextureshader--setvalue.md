---
description: Legt die Konstante Tabelle mit den Daten im Puffer fest.
ms.assetid: 55cf5456-8f23-405d-9329-8ff737c5c139
title: 'ID3DXTextureShader:: SetValue-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2f18902c73f44bc4294e5152f8da5ea3e37f27ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363965"
---
# <a name="id3dxtextureshadersetvalue-method"></a>ID3DXTextureShader:: SetValue-Methode

Legt die Konstante Tabelle mit den Daten im Puffer fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hConstant,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hconstant* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für eine Konstante. Siehe [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Ein Zeiger auf einen Puffer, der die Konstanten Daten enthält.

</dd> <dt>

*Bytes* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Größe des Puffers in Bytes.

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

 

 
