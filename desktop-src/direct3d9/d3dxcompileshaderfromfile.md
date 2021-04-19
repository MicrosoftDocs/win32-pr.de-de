---
description: Kompilieren Sie eine Shader-Datei.
ms.assetid: 2ad6042f-3601-4f4a-9624-6319a3372355
title: D3DXCompileShaderFromFile-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 865241142fa13ec9d34826bfe334c30b38ca78d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353371"
---
# <a name="d3dxcompileshaderfromfile-function"></a>D3DXCompileShaderFromFile-Funktion

Kompilieren Sie eine Shader-Datei.

> [!Note]  
> Anstatt diese Legacy Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mit dem Fxc.exe-Befehlszeilen Compiler oder der [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) -API verwenden.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCompileShaderFromFile(
  _In_        LPCTSTR             pSrcFile,
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

*psrcfile* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.

</dd> <dt>

*pdefinitionen* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***

Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen. Dieser Wert kann **null** sein.

</dd> <dt>

*pinclude* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# . Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.

</dd> <dt>

*pfunctionname* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger zur Funktion des Shader-Einstiegs Punkts, bei dem die Ausführung beginnt.

</dd> <dt>

*pprofile* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf ein Shader-Profil, das den Shader-Anweisungs Satz bestimmt. Eine Liste der verfügbaren Profile finden Sie unter [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) oder [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden. Der Direct3D 10 HLSL-Compiler ist nun der Standard. Weitere Informationen finden Sie unter [D3DXSHADER-Flags](d3dxshader-flags.md) .

</dd> <dt>

*ppshader* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Puffer zurück, der den erstellten Shader enthält. Dieser Puffer enthält den kompilierten Shader-Code sowie alle eingebetteten Debug-und Symboltabellen Informationen.

</dd> <dt>

*pperrormsgs* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Puffer zurück, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung gefunden wurden. Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird. Dieser Wert kann **null** sein.

</dd> <dt>

*ppconstanbar* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Gibt eine [**ID3DXConstantTable**](id3dxconstanttable.md) -Schnittstelle zurück, die für den Zugriff auf shaderkonstanten verwendet werden kann. Dieser Wert kann **null** sein. Wenn Sie die Anwendung als große Adressen unterstützen (d. h. mit der/LARGEADDRESSAWARE-Linkeroption, um Adressen zu verarbeiten, die größer als 2 GB sind), können Sie diesen Parameter nicht verwenden und müssen ihn auf **null** festlegen. Stattdessen müssen Sie die [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) -Funktion verwenden, um die in den Shader eingebettete Shader-Konstante Tabelle abzurufen. In diesem **D3DXGetShaderConstantTableEx** -Aufruf müssen Sie das Flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** an den *Flags* -Parameter übergeben, um anzugeben, dass auf bis zu 4 GB virtuellen Adressraum zugegriffen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, e \_ notimpl, e \_ outo fmemory.

E \_ notimpl wird zurückgegeben, wenn Sie 1,1 Shader (vs \_ 1 \_ 1 und PS \_ 1 \_ 1) verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[**D3DXCompileShader**](d3dxcompileshader.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
