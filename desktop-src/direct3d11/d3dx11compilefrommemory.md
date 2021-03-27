---
title: D3DX11CompileFromMemory-Funktion (D3DX11async. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Hinweis statt diese Funktion zu verwenden, wird empfohlen, die Offline Kompilierung mithilfe des Befehlszeilen Compilers Fxc.exe oder eine der HLSL-Kompilierungs-APIs wie die D3DCompile-API zu verwenden. Kompilieren Sie einen Shader oder einen Effekt, der in den Arbeitsspeicher geladen wird.
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
ms.openlocfilehash: 2e10590c3db458a23bf4d52b6507146884630087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982359"
---
# <a name="d3dx11compilefrommemory-function"></a>D3DX11CompileFromMemory-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mithilfe des Befehlszeilen Compilers Fxc.exe oder eine der HLSL-Kompilierungs-APIs wie die [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) -API verwenden.

 

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

*pSrcData* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Zeiger auf den Shader im Arbeitsspeicher.

</dd> <dt>

*Srcdatalen* \[ in\]
</dt> <dd>

Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**

Größe des Shaders im Arbeitsspeicher.

</dd> <dt>

*pfilename* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name der Datei, die den Shader-Code enthält.

</dd> <dt>

*pdefinitionen* \[ in\]
</dt> <dd>

Type: **Konstanten [**d3d10 \_ Shader- \_ Makro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Optional. Zeiger auf ein Array von Makro Definitionen (siehe [**d3d10 \_ Shader \_ Macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). Die letzte Struktur im Array fungiert als Abschluss Zeichen und muss alle Elemente auf 0 (null) festlegen. Wenn Sie nicht verwendet wird, legen Sie *pdefinitionen* auf **null** fest.

</dd> <dt>

*pinclude* \[ in\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Optional. Zeiger auf eine-Schnittstelle zum Verarbeiten von Includedateien. Wenn dieser Wert auf **null** festgelegt wird, wird ein Kompilierungsfehler verursacht, wenn ein Shader eine include-Datei \#

</dd> <dt>

*pfunctionname* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name der Shader-Einstiegspunkt Funktion, bei der die Shader-Ausführung beginnt. Wenn Sie einen Effekt kompilieren,  ignoriert D3DX11CompileFromMemory *pfunctionname*;. Es wird empfohlen, *pfunctionname* auf **null** festzulegen, da es eine gute Programmierpraxis ist, einen Zeiger Parameter auf **null** festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*pprofile* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Eine Zeichenfolge, die das Shadermodell angibt. kann ein beliebiges Profil in Shader Model 2, Shader Model 3, Shader Model 4 oder Shader Model 5 sein. Das Profil kann auch für den Typ "Effect" (z \_ . b. FX 4 \_ 1) sein.

</dd> <dt>

*Flags1* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Shader- [**Kompilierungs Flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).

</dd> <dt>

*Flags2* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Effekt [**Kompilierungs Flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants). Wenn Sie einen Shader und keine Effekt Datei kompilieren, ignoriert **D3DX11CompileFromMemory** *Flags2*; Es wird empfohlen, *Flags2* auf NULL festzulegen, da es eine gute Programmierpraxis ist, einen Typ-Parameter auf 0 (null) festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*ppump* \[ in\]
</dt> <dd>

Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)). Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.

</dd> <dt>

*ppshader* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf den Arbeitsspeicher, der den kompilierten Shader sowie alle eingebetteten Debug-und Symbol Tabelleninformationen enthält.

</dd> <dt>

*pperrormsgs* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf den Arbeitsspeicher, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind. Diese Fehler und Warnungen sind identisch mit der Debugausgabe eines Debuggers.

</dd> <dt>

*phresult* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann **null** sein. Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.

**D3DX11CompileFromMemory** gibt E \_ invalidArg zurück, wenn Sie einen Wert ungleich **null** für den Parameter " *phresult* " angeben, wenn Sie **null** für den *ppump* -Parameter angeben. Weitere Informationen zu dieser Situation finden Sie unter "Hinweise".

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu **D3DX11CompileFromMemory** finden Sie unter [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).

Sie müssen **null** für den Parameter " *phresult* " angeben, wenn Sie auch **null** für den *ppump* -Parameter angeben. Andernfalls können Sie später keinen Shader erstellen, indem Sie den kompilierten shadercode verwenden, den **D3DX11CompileFromMemory** im Speicher zurückgibt, auf den der *ppshader* -Parameter verweist. Zum Erstellen eines Shaders aus dem eingehenden Shader-Code Rufen Sie eine der folgenden [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Schnittstellen Methoden auf:

-   [**"Kreatecomputeshader"**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [**"Kreatedomainshader"**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**"Kreategeometryshader"**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**"Kreategeometryshaderwithstreamoutput"**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**"Kreatehullshader"**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**"Kreatepixelshader"**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [**"Kreatevertexshader"**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Wenn Sie einen Wert ungleich **null** *bei der Angabe* von **null** für *ppump* angeben, gibt **D3DX11CompileFromMemory** den E \_ invalidArg-Fehlercode zurück.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Bibliothek d3dx11. lib</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

