---
description: Einen Zeiger auf die Konstante Tabelle erhalten.
ms.assetid: 5d836d99-783f-41e1-b7bf-d874d09a4892
title: 'ID3DXTextureShader:: getconstantbuffer-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c83a723dde56fc80f643d7209c56fc05ad6cce5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354497"
---
# <a name="id3dxtextureshadergetconstantbuffer-method"></a>ID3DXTextureShader:: getconstantbuffer-Methode

Einen Zeiger auf die Konstante Tabelle erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConstantBuffer(
  [out] LPD3DXBUFFER *ppConstantBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppconstantbuffer* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die die Konstanten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 




