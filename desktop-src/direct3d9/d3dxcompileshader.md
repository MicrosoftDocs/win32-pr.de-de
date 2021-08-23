---
description: 'D3DXCompileShader-Funktion: Kompiliert eine Shaderdatei.'
ms.assetid: 9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8
title: D3DXCompileShader-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c6441e000422c113521803924d7c1fc746cd2c96591463d33677425a49f7edfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988690"
---
# <a name="d3dxcompileshader-function"></a>D3DXCompileShader-Funktion

Kompilieren Sie eine Shaderdatei.

> [!Note]  
> Anstatt diese Legacyfunktion zu verwenden, empfiehlt es sich, offline zu kompilieren, indem Fxc.exe Befehlszeilencompiler oder die [**D3DCompile-API verwendet**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) wird.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCompileShader(
  _In_        LPCSTR              pSrcData,
  _In_        UINT                srcDataLen,
  _In_  const D3DXMACRO           *pDefines,
  _In_        LPD3DXINCLUDE       pInclude,
  _In_        LPCSTR              pFunctionName,
  _In_        LPCSTR              pProfile,
  _In_        DWORD               Flags,
  _Out_       LPD3DXBUFFER        *ppShader,
  _Out_       LPD3DXBUFFER        *ppErrorMsgs,
  _Out_       LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Shader enthält.

</dd> <dt>

*srcDataLen* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Länge der Daten in Bytes.

</dd> <dt>

*pDefdefine* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***

Ein optionales **null-terminiertes** Array [**von D3DXMACRO-Strukturen.**](d3dxmacro.md) Dieser Wert kann NULL **sein.**

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von Include-Direktiven \# verwendet werden soll. Wenn dieser Wert **NULL ist,** wird includes entweder beim Kompilieren aus einer Datei oder beim Kompilieren aus einer Ressource oder einem Arbeitsspeicher \# zu einem Fehler führen.

</dd> <dt>

*pFunctionName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Namen der Shadereinstiegspunktfunktion enthält, an der die Ausführung beginnt.

</dd> <dt>

*pProfile* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf ein Shaderprofil, das den Shaderanweisungssatz bestimmt. Eine Liste der verfügbaren Profile finden Sie unter [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) oder [**D3DXGetPixelShaderProfile.**](d3dxgetpixelshaderprofile.md)

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden. Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung. Weitere Informationen finden Sie unter [D3DXSHADER-Flags.](d3dxshader-flags.md)

</dd> <dt>

*ppShader* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Puffer zurück, der den erstellten Shader enthält. Dieser Puffer enthält den kompilierten Shadercode sowie alle eingebetteten Debug- und Symboltabelleninformationen.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Puffer zurück, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind. Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird. Dieser Wert kann NULL **sein.**

</dd> <dt>

*ppConstantTable* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Gibt eine [**ID3DXConstantTable-Schnittstelle**](id3dxconstanttable.md) zurück, die für den Zugriff auf Shaderkonstanten verwendet werden kann. Dieser Wert kann NULL **sein.** Wenn Sie Ihre Anwendung als große Adressierung kompilieren (d. h., Sie verwenden die Linkeroption /LARGEADDRESSAWARE, um Adressen zu verarbeiten, die größer als 2 GB sind), können Sie diesen Parameter nicht verwenden und müssen ihn auf **NULL festlegen.** Stattdessen müssen Sie die [**D3DXGetShaderConstantTableEx-Funktion**](d3dxgetshaderconstanttableex.md) verwenden, um die shaderkonstante Tabelle abzurufen, die in den Shader eingebettet ist. In diesem **D3DXGetShaderConstantTableEx-Aufruf** müssen Sie das **D3DXCONSTTABLE \_ LARGEADDRESSAWARE-Flag** an den *Flags-Parameter* übergeben, um den Zugriff auf bis zu 4 GB virtuellen Adressraum anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
