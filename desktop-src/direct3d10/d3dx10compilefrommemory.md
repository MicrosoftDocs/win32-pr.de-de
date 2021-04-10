---
description: Hinweis Wenn Sie diese Legacy Funktion nicht verwenden, empfiehlt es sich, die Offline Kompilierung mit dem Fxc.exe-Befehlszeilen Compiler oder der D3DCompile-API zu verwenden. Kompilieren Sie einen Shader oder einen Effekt, der in den Arbeitsspeicher geladen wird.
ms.assetid: c6458d82-a649-402c-8180-5b7320f9fdb0
title: D3DX10CompileFromMemory-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: fbb4a716df4a893ea122e7badfd6faad536aacce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961725"
---
# <a name="d3dx10compilefrommemory-function"></a>D3DX10CompileFromMemory-Funktion

> [!Note]  
> Anstatt diese Legacy Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mit dem Fxc.exe-Befehlszeilen Compiler oder der [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) -API verwenden.

 

Kompilieren Sie einen Shader oder einen Effekt, der in den Arbeitsspeicher geladen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Shader im Arbeitsspeicher.

</dd> <dt>

*Srcdatalen* \[ in\]
</dt> <dd>

Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**

Größe des Shaders im Arbeitsspeicher.

</dd> <dt>

*pfilename* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der Name der Datei, die den Shader-Code enthält.

</dd> <dt>

*pdefinitionen* \[ in\]
</dt> <dd>

Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Dies ist optional. Zeiger auf ein Array von Makro Definitionen (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). Die letzte Struktur im Array fungiert als Abschluss Zeichen und muss alle Elemente auf 0 (null) festlegen. Wenn Sie nicht verwendet wird, legen Sie *pdefinitionen* auf **null** fest.

</dd> <dt>

*pinclude* \[ in\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Dies ist optional. Zeiger auf eine [**ID3D10Include-Schnittstellen**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) Schnittstelle zur Behandlung von Includedateien. Wenn dieser Wert auf **null** festgelegt wird, wird ein Kompilierungsfehler verursacht, wenn ein Shader eine include-Datei \#

</dd> <dt>

*pfunctionname* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der Name der Shader-Einstiegspunkt Funktion, bei der die Shader-Ausführung beginnt. Wenn Sie einen Effekt kompilieren,  ignoriert D3DX10CompileFromMemory *pfunctionname*;. Es wird empfohlen, *pfunctionname* auf **null** festzulegen, da es eine gute Programmierpraxis ist, einen Zeiger Parameter auf **null** festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*pprofile* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die das Shadermodell angibt. kann ein beliebiges Profil in [Shader Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)oder [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md)sein.

</dd> <dt>

*Flags1* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

[Shader-Kompilierungs Flags](d3d10-shader.md).

</dd> <dt>

*Flags2* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

[Effekt Kompilierungs Flags](d3d10-graphics-reference-effect-constants.md). Wenn Sie einen Shader und keine Effekt Datei kompilieren, ignoriert **D3DX10CompileFromMemory** *Flags2*; Es wird empfohlen, *Flags2* auf NULL festzulegen, da es eine gute Programmierpraxis ist, einen Typ-Parameter auf 0 (null) festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*ppump* \[ in\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)). Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.

</dd> <dt>

*ppshader* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf eine [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , die den kompilierten Shader sowie alle eingebetteten Debug-und Symboltabellen Informationen enthält.

</dd> <dt>

*pperrormsgs* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf eine [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , die eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind. Diese Fehler und Warnungen sind identisch mit der Debugausgabe eines Debuggers.

</dd> <dt>

*phresult* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann **null** sein. Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
