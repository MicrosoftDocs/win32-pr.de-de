---
description: Kompiliert einen Shader aus einem Effekt, der eine oder mehrere Funktionen enthält.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: ID3DXEffectCompiler::CompileShader-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3e8d1d72fccd5c4ad47d21d05ee46013860a7743
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343625"
---
# <a name="id3dxeffectcompilercompileshader-method"></a>ID3DXEffectCompiler::CompileShader-Methode

Kompiliert einen Shader aus einem Effekt, der eine oder mehrere Funktionen enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFunction* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für die zu kompilierende Funktion. Dieser Wert darf nicht **NULL** sein. Siehe [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pTarget* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf ein Shaderprofil, das den Shader-Anweisungssatz bestimmt. Eine Liste der verfügbaren Profile finden Sie unter [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) oder [**D3DXGetPixelShaderProfile.**](d3dxgetpixelshaderprofile.md)

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden. Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung. Weitere Informationen finden Sie unter [D3DXSHADER-Flags.](d3dxshader-flags.md)

</dd> <dt>

*ppShader* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puffer, der den kompilierten Shader enthält. Der Compiler-Shader ist ein Array von DWORDs. Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppErrorMsgs* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puffer, der mindestens die erste aufgetretene Kompilierfehlermeldung enthält. Dies schließt Auswirkungencompilerfehler und Fehler bei der Sprachcompilierung auf hoher Ebene ein. Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppConstantTable* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Gibt eine [**ID3DXConstantTable-Schnittstelle**](id3dxconstanttable.md) zurück, die für den Zugriff auf Shaderkonstanten verwendet werden kann. Dieser Wert kann NULL **sein.** Wenn Sie Ihre Anwendung als große Adressierung kompilieren (d. h., Sie verwenden die Linkeroption /LARGEADDRESSAWARE, um Adressen zu verarbeiten, die größer als 2 GB sind), können Sie diesen Parameter nicht verwenden und müssen ihn auf **NULL festlegen.** Stattdessen müssen Sie die [**D3DXGetShaderConstantTableEx-Funktion**](d3dxgetshaderconstanttableex.md) verwenden, um die shaderkonstante Tabelle abzurufen, die in den Shader eingebettet ist. In diesem **D3DXGetShaderConstantTableEx-Aufruf** müssen Sie das **D3DXCONSTTABLE \_ LARGEADDRESSAWARE-Flag** an den *Flags-Parameter* übergeben, um den Zugriff auf bis zu 4 GB virtuellen Adressraum anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK.

Wenn die Argumente ungültig sind, gibt die Methode D3DERR \_ INVALIDCALL zurück.

Wenn bei der Methode ein Fehler auftritt, ist der Rückgabewert E \_ FAIL.

## <a name="remarks"></a>Hinweise

Ziele können für Vertex-Shader, Pixel-Shader und Texturfüllfunktionen angegeben werden.



| Ziele                      | Functions                                                                      |
|-----------------------|-----------------------------------------------------------------------|
| Vertex-Shaderziele | Vs \_ 1 \_ 1, vs \_ 2 \_ 0, vs \_ 2 \_ sw, vs \_ 3 \_ 0                               |
| Pixel-Shaderziele  | ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4, ps \_ 2 \_ 0, ps \_ 2 \_ sw, ps \_ 3 \_ 0 |
| Texturfüllziele  | tx \_ 0, tx \_ 1                                                          |



 

Diese Methode kompiliert einen Shader aus einer Funktion, die in einer C-ähnlichen Sprache geschrieben ist. Weitere Informationen finden Sie unter [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
