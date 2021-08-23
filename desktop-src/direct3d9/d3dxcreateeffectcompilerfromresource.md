---
description: Erstellt einen ID3DXEffectCompiler aus einer ASCII-Effektbeschreibung.
ms.assetid: 041e0a3f-3dc6-4cc3-8380-d4a79a3f647a
title: D3DXCreateEffectCompilerFromResource-Funktion (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8f781137e6da118392f8b4e17addd92123b75ecd994191a86ab74d46f3dde6f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045168"
---
# <a name="d3dxcreateeffectcompilerfromresource-function"></a>D3DXCreateEffectCompilerFromResource-Funktion

Erstellt einen [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) aus einer ASCII-Effektbeschreibung.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateEffectCompilerFromResource(
  _In_        HMODULE              hSrcModule,
  _In_        LPCTSTR              pSrcResource,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSrcModule* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle für ein Modul, das die Beschreibung des Effekts enthält. Wenn dieser Parameter **NULL** ist, wird das aktuelle Modul verwendet.

</dd> <dt>

*pSrcResource* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf die Ressource. Dieser Parameter unterstützt sowohl Unicode- als auch ANSI-Zeichenfolgen. Siehe Hinweise.

</dd> <dt>

*pDefine* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***

Ein optionales NULL-terminiertes Array von [**D3DXMACRO-Strukturen,**](d3dxmacro.md) die Präprozessordefinitionen beschreiben. Dieser Wert kann **NULL** sein.

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von \# Includedirektiven verwendet werden soll. Wenn dieser Wert **NULL** ist, \# wird includes entweder beim Kompilieren aus einer Datei berücksichtigt oder verursacht bei der Kompilierung aus einer Ressource oder aus dem Arbeitsspeicher einen Fehler.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Durch verschiedene Flags identifizierte Kompilierungsoptionen (siehe [D3DXSHADER-Flags).](d3dxshader-flags.md) Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung. Weitere Informationen finden Sie [unter Effektcompilertool.](../direct3dtools/fxc.md)

</dd> <dt>

*ppEffectCompiler* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***

Adresse eines Zeigers auf eine [**ID3DXEffectCompiler-Schnittstelle,**](id3dxeffectcompiler.md) die den Effektcompiler enthält.

</dd> <dt>

*ppParseErrors* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle,**](id3dxbuffer.md) die alle Fehlermeldungen enthält, die während der Kompilierung aufgetreten sind. Dieser Parameter kann auf **NULL** festgelegt werden, um Fehlermeldungen zu ignorieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der LPCTSTR-Datentyp in LPCSTR aufgelöst.

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateEffectCompilerFromResourceW aufgelöst. Andernfalls wird der Funktionsaufruf in D3DXCreateEffectCompilerFromResourceA aufgelöst, da ANSI-Zeichenfolgen verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effect-Funktionen](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> </dl>

 

 
