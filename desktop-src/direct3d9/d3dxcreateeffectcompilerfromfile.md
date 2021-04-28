---
description: 'D3DXCreateEffectCompilerFromFile-Funktion: Erstellt einen Effektcompiler aus einer ASCII-Effektbeschreibung.'
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: D3DXCreateEffectCompilerFromFile-Funktion (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0c054b31b1ab70d1378c794be13058204b994ee2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087978"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a>D3DXCreateEffectCompilerFromFile-Funktion

Erstellt einen Effektcompiler aus einer ASCII-Effektbeschreibung.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateEffectCompilerFromFile(
  _In_        LPCTSTR              pSrcFile,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Dateinamen. Dieser Parameter unterstützt sowohl Unicode- als auch ANSI-Zeichenfolgen. Siehe Hinweise.

</dd> <dt>

*pDefdefine* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***

Ein optionales **auf NULL** beendetes Array [**von D3DXMACRO-Strukturen,**](d3dxmacro.md) die Präprozessordefinitionen beschreiben. Dieser Wert kann NULL **sein.**

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von Include-Direktiven \# verwendet werden soll. Wenn dieser Wert **NULL ist,** wird includes entweder beim Kompilieren aus einer Datei oder beim Kompilieren aus einer Ressource oder einem Arbeitsspeicher \# zu einem Fehler führen.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden (siehe [D3DXSHADER-Flags](d3dxshader-flags.md)). Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung. Weitere [Informationen finden Sie unter Effect-Compiler Tool](../direct3dtools/fxc.md) .

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

## <a name="remarks"></a>Bemerkungen

Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der LPCTSTR-Datentyp in LPCSTR aufgelöst.

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateEffectCompilerFromFileW aufgelöst. Andernfalls wird der Funktionsaufruf in D3DXCreateEffectCompilerFromFileA aufgelöst, da ANSI-Zeichenfolgen verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effect-Funktionen](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
