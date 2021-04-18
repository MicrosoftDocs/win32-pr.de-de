---
description: Kompiliert einen Shader aus einem Effekt, der eine oder mehrere Funktionen enthält.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: 'ID3DXEffectCompiler:: compileshader-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: 375646202e102623053c179398329ad2286e6c1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371927"
---
# <a name="id3dxeffectcompilercompileshader-method"></a>ID3DXEffectCompiler:: compileshader-Methode

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

*hfunction* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für die Funktion, die kompiliert werden soll. Dieser Wert darf nicht **null** sein. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pTARGET* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf ein Shader-Profil, das den Shader-Anweisungs Satz bestimmt. Eine Liste der verfügbaren Profile finden Sie unter [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) oder [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden. Der Direct3D 10 HLSL-Compiler ist nun der Standard. Weitere Informationen finden Sie unter [D3DXSHADER-Flags](d3dxshader-flags.md) .

</dd> <dt>

*ppshader* \[ Out, retval\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Der Puffer, der den kompilierten Shader enthält. Der compilershader ist ein Array von DWORDs. Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*pperrormsgs* \[ Out, retval\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puffer, der mindestens die erste Kompilierungs Fehlermeldung enthält, die aufgetreten ist. Dies schließt Compilerfehler und allgemeine sprach Kompilierungsfehler ein. Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppconstanbar* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Gibt eine [**ID3DXConstantTable**](id3dxconstanttable.md) -Schnittstelle zurück, die für den Zugriff auf shaderkonstanten verwendet werden kann. Dieser Wert kann **null** sein. Wenn Sie die Anwendung als große Adressen unterstützen (d. h. mit der/LARGEADDRESSAWARE-Linkeroption, um Adressen zu verarbeiten, die größer als 2 GB sind), können Sie diesen Parameter nicht verwenden und müssen ihn auf **null** festlegen. Stattdessen müssen Sie die [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) -Funktion verwenden, um die in den Shader eingebettete Shader-Konstante Tabelle abzurufen. In diesem **D3DXGetShaderConstantTableEx** -Aufruf müssen Sie das Flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** an den *Flags* -Parameter übergeben, um anzugeben, dass auf bis zu 4 GB virtuellen Adressraum zugegriffen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.

Wenn die Argumente ungültig sind, gibt die Methode D3DERR \_ invalidcallzurück.

Wenn die Methode fehlschlägt, lautet der Rückgabewert E \_ Fail.

## <a name="remarks"></a>Bemerkungen

Ziele können für Vertex-Shader, Pixel-Shader und Textur Füll Funktionen angegeben werden.



|                       |                                                                       |
|-----------------------|-----------------------------------------------------------------------|
| Vertex-Shader-Ziele | vs \_ 1 \_ 1, vs \_ 2 \_ 0, vs \_ 2 \_ SW, vs \_ 3 \_ 0                               |
| Pixel-Shader-Ziele  | PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4, PS \_ 2 \_ 0, PS \_ 2 \_ SW, PS \_ 3 \_ 0 |
| Textur Füll Ziele  | TX \_ 0, TX \_ 1                                                          |



 

Diese Methode kompiliert einen Shader aus einer Funktion, die in einer C-ähnlichen Sprache geschrieben ist. Weitere Informationen finden Sie unter [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
