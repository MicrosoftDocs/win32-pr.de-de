---
description: Disassembliert einen Shader.
ms.assetid: 30159223-8f88-4929-8ef1-7a6acc13f485
title: D3DXDisassembleShader-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6192b77c190ed73dc6e5038c9119152836eca375
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353362"
---
# <a name="d3dxdisassembleshader-function"></a>D3DXDisassembleShader-Funktion

Disassembliert einen Shader.

> [!Note]  
> Anstatt diese Legacy Funktion zu verwenden, empfiehlt es sich, die [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) -API zu verwenden.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXDisassembleShader(
  _In_  const DWORD        *pShader,
  _In_        BOOL         EnableColorCode,
  _In_        LPCSTR       pComments,
  _Out_       LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pshader* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf einen Arbeitsspeicher Puffer, der die Shader-Daten enthält.

</dd> <dt>

*Enablecolorcode* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Aktivieren Sie Farbcode, um die Disassembly leichter lesbar zu machen.

</dd> <dt>

*pcomments* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine optionale, auf NULL endenden Kommentar Zeichenfolge. Dieser Wert kann **null** sein.

</dd> <dt>

*ppdisassembly* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Puffer zurück, der den disassemblierten Shader enthält. Siehe [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
