---
title: D3DX11CompileFromMemory-Funktion (D3DX11async.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Hinweis Anstatt diese Funktion zu verwenden, empfiehlt es sich, offline mit dem Fxc.exe Befehlszeilencompiler zu kompilieren oder eine der HLSL-Kompilierungs-APIs wie die D3DCompile-API zu verwenden. Kompilieren Sie einen Shader oder einen Effekt, der in den Arbeitsspeicher geladen wird.
ms.assetid: 3396560f-f411-4c66-9f22-03c0050c74b0
keywords:
- D3DX11CompileFromMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 055fa070eb698298716abef11090a8c178cb4ef85f46bc6733df037a5778e4d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536819"
---
# <a name="d3dx11compilefrommemory-function"></a>D3DX11CompileFromMemory-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, empfiehlt es sich, offline mit dem Fxc.exe Befehlszeilencompiler zu kompilieren oder eine der HLSL-Kompilierungs-APIs wie die [**D3DCompile-API**](/windows/desktop/direct3dhlsl/d3dcompile) zu verwenden.

 

Kompilieren Sie einen Shader oder einen Effekt, der in den Arbeitsspeicher geladen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Zeiger auf den Shader im Arbeitsspeicher.

</dd> <dt>

*SrcDataLen* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Größe des Shaders im Arbeitsspeicher.

</dd> <dt>

*pFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name der Datei, die den Shadercode enthält.

</dd> <dt>

*pDefine* \[ In\]
</dt> <dd>

Typ: **const [**D3D10 \_ SHADER \_ MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Optional. Zeiger auf ein Array von Makrodefinitionen (siehe [**D3D10 \_ SHADER \_ MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). Die letzte Struktur im Array dient als Abschlusszeichen und muss alle Member auf 0 festgelegt haben. Wenn sie nicht verwendet wird, legen Sie *pDefine* auf **NULL** fest.

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Optional. Zeiger auf eine Schnittstelle für die Behandlung von Includedateien. Wenn sie auf **NULL** festgelegt wird, tritt ein Kompilierungsfehler auf, wenn ein Shader ein \# Include enthält.

</dd> <dt>

*pFunctionName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Name der Shader-Einstiegspunktfunktion, bei der die Shaderausführung beginnt. Wenn Sie einen Effekt kompilieren, ignoriert **D3DX11CompileFromMemory** *pFunctionName*; Es wird empfohlen, *pFunctionName* auf **NULL** festzulegen, da es sich bei der Programmierung empfiehlt, einen Zeigerparameter auf **NULL** festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*pProfile* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Eine Zeichenfolge, die das Shadermodell angibt. kann ein beliebiges Profil in Shadermodell 2, Shadermodell 3, Shadermodell 4 oder Shadermodell 5 sein. Das Profil kann auch für den Effekttyp (z. B. fx \_ 4 \_ 1) sein.

</dd> <dt>

*Flags1* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

[**Shaderkompilierungsflags.**](/windows/desktop/direct3dhlsl/d3dcompile-constants)

</dd> <dt>

*Flags2* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

[**Effektkompilierungsflags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants). Wenn Sie einen Shader und keine Effektdatei kompilieren, ignoriert **D3DX11CompileFromMemory** *Flags2*; Es wird empfohlen, *Flags2* auf 0 (null) festzulegen, da es sich bei der Programmierung empfiehlt, einen Nichtpunkterparameter auf 0 (null) festzulegen, wenn er von der aufgerufenen Funktion nicht verwendet wird.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Ein Zeiger auf eine Threadpumpschnittstelle (siehe [**ID3DX11ThreadPump-Schnittstelle).**](id3dx11threadpump.md) Geben Sie mit **NULL** an, dass diese Funktion erst zurückgegeben werden soll, wenn sie abgeschlossen ist.

</dd> <dt>

*ppShader* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf den Arbeitsspeicher, der den kompilierten Shader sowie alle eingebetteten Debug- und Symboltabelleninformationen enthält.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf den Arbeitsspeicher, der eine Liste von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind. Diese Fehler und Warnungen sind mit der Debugausgabe eines Debuggers identisch.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann **NULL** sein. Wenn *pPump* nicht **NULL** ist, muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 11-Rückgabecodes aufgeführten](d3d11-graphics-reference-returnvalues.md)Werte.

**D3DX11CompileFromMemory** gibt E \_ INVALIDARG zurück, wenn Sie nicht **NULL** für den *pHResult-Parameter* angeben, wenn Sie **NULL** für den *pPump-Parameter* angeben. Weitere Informationen zu dieser Situation finden Sie unter Hinweise.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu **D3DX11CompileFromMemory** finden Sie unter [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).

Sie müssen **null** für den *pHResult-Parameter* angeben, wenn Sie auch **NULL** für den *pPump-Parameter* angeben. Andernfalls können Sie anschließend keinen Shader erstellen, indem Sie den kompilierten Shadercode verwenden, auf den **D3DX11CompileFromMemory** im Arbeitsspeicher zurückgibt, auf den der *ppShader-Parameter* zeigt. Um einen Shader aus verzerrbarem Shadercode zu erstellen, rufen Sie eine der folgenden [**ID3D11Device-Schnittstellenmethoden**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) auf:

-   [**CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**CreatePixelShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Wenn Sie bei der Bereitstellung von **NULL** für *pPump* einen Wert ungleich **NULL** für *pHResult* bereitstellen, gibt **D3DX11CompileFromMemory** außerdem den E \_ INVALIDARG-Fehlercode zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

