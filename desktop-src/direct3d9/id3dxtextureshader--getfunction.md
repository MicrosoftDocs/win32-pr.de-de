---
description: Ruft einen Zeiger auf die Funktion DWORD-Stream ab.
ms.assetid: a051b51a-185c-4a9e-a8b9-4096615e2634
title: 'ID3DXTextureShader:: GetFunction-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetFunction
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80e504e65e4c8437247b2935794025e1b693433a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355046"
---
# <a name="id3dxtextureshadergetfunction-method"></a>ID3DXTextureShader:: GetFunction-Methode

Ruft einen Zeiger auf die Funktion DWORD-Stream ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFunction(
  [in] LPD3DXBUFFER *ppFunction
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppfunction* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ein Zeiger auf die Funktion DWORD-Stream. Siehe [**ID3DXBuffer**](id3dxbuffer.md).

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

 

 




