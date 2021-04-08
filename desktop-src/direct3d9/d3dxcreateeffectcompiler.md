---
description: Erstellt einen Effekt Compiler aus einer Beschreibung des ASCII-Effekts.
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: D3DXCreateEffectCompiler-Funktion (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompiler
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 513b11ba12abe05126c122f8bc9bfcfa978df3fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762282"
---
# <a name="d3dxcreateeffectcompiler-function"></a>D3DXCreateEffectCompiler-Funktion

Erstellt einen Effekt Compiler aus einer Beschreibung des ASCII-Effekts.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateEffectCompiler(
  _In_        LPCSTR               pSrcData,
  _In_        UINT                 SrcDataLen,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf einen Puffer, der eine Beschreibung des Effekts enthält.

</dd> <dt>

*Srcdatalen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Länge in Byte der Effekt Daten.

</dd> <dt>

*pdefinitionen* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***

Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen, die Präprozessordefinitionen beschreiben. Dieser Wert kann **null** sein.

</dd> <dt>

*pinclude* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# . Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden (siehe [D3DXSHADER Flags](d3dxshader-flags.md)). Der Direct3D 10 HLSL-Compiler ist nun der Standard. Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .

</dd> <dt>

*ppeer-ectcompiler* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***

Adresse eines Zeigers auf eine [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) -Schnittstelle, die den Effekt Compiler enthält.

</dd> <dt>

*ppparsererrors* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die Fehlermeldungen enthält, die während der Kompilierung aufgetreten sind. Dieser Parameter kann auf **null** festgelegt werden, um Fehlermeldungen zu ignorieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Funktionen](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
