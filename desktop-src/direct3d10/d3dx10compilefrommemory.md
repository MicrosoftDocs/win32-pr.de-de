---
description: Hinweis Anstatt diese Legacyfunktion zu verwenden, empfiehlt es sich, offline zu kompilieren, indem Sie den Fxc.exe Befehlszeilencompiler oder die D3DCompile-API verwenden. Kompilieren Sie einen Shader oder einen Effekt, der in den Arbeitsspeicher geladen wird.
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
ms.openlocfilehash: f5cd6772079f872fe575a3a2f49fee536b89dab00f29a62dba151842dbc99b45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119281710"
---
# <a name="d3dx10compilefrommemory-function"></a>D3DX10CompileFromMemory-Funktion

> [!Note]  
> Anstatt diese Legacyfunktion zu verwenden, empfiehlt es sich, offline mit dem Fxc.exe Befehlszeilencompiler zu kompilieren oder die [**D3DCompile-API**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) zu verwenden.

 

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

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Shader im Arbeitsspeicher.

</dd> <dt>

*SrcDataLen* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Größe des Shaders im Arbeitsspeicher.

</dd> <dt>

*pFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der Name der Datei, die den Shadercode enthält.

</dd> <dt>

*pDefine* \[ In\]
</dt> <dd>

Typ: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Optional. Zeiger auf ein Array von Makrodefinitionen (siehe [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). Die letzte Struktur im Array dient als Abschlusszeichen und muss alle Member auf 0 festgelegt haben. Wenn sie nicht verwendet wird, legen Sie *pDefine* auf **NULL** fest.

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Optional. Zeiger auf eine [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) für die Behandlung von Includedateien. Wenn sie auf **NULL** festgelegt wird, tritt ein Kompilierungsfehler auf, wenn ein Shader ein \# Include enthält.

</dd> <dt>

*pFunctionName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Name der Shader-Einstiegspunktfunktion, bei der die Shaderausführung beginnt. Wenn Sie einen Effekt kompilieren, ignoriert **D3DX10CompileFromMemory** *pFunctionName*; Es wird empfohlen, *pFunctionName* auf **NULL** festzulegen, da es sich bei der Programmierung empfiehlt, einen Zeigerparameter auf **NULL** festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*pProfile* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die das Shadermodell angibt. kann ein beliebiges Profil in [Shadermodell 2,](../direct3dhlsl/dx-graphics-hlsl-sm2.md) [Shadermodell 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)oder [Shadermodell 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md)sein.

</dd> <dt>

*Flags1* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

[Shaderkompilierungsflags.](d3d10-shader.md)

</dd> <dt>

*Flags2* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

[Effektkompilierungsflags](d3d10-graphics-reference-effect-constants.md). Wenn Sie einen Shader und keine Effektdatei kompilieren, ignoriert **D3DX10CompileFromMemory** *Flags2*. Es wird empfohlen, *Flags2* auf 0 (null) festzulegen, da es sich bei der Programmierung empfiehlt, einen Nichtpunkterparameter auf 0 (null) festzulegen, wenn er von der aufgerufenen Funktion nicht verwendet wird.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Ein Zeiger auf eine Threadpumpschnittstelle (siehe [**ID3DX10ThreadPump-Schnittstelle).**](id3dx10threadpump.md) Geben Sie mit **NULL** an, dass diese Funktion erst zurückgegeben werden soll, wenn sie abgeschlossen ist.

</dd> <dt>

*ppShader* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf eine [**ID3D10Blob-Schnittstelle,**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) die den kompilierten Shader sowie alle eingebetteten Debug- und Symboltabelleninformationen enthält.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf eine [**ID3D10Blob-Schnittstelle,**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) die eine Liste von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind. Diese Fehler und Warnungen sind mit der Debugausgabe eines Debuggers identisch.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann **NULL** sein. Wenn *pPump* nicht **NULL** ist, muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
