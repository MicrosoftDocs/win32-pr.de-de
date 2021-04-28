---
description: 'D3DXCreateEffectFromFile-Funktion: Erstellt einen Effekt aus einer ASCII- oder Binäreffektbeschreibung.'
ms.assetid: b5868ba3-0869-46f7-804f-3103358a3ef5
title: D3DXCreateEffectFromFile-Funktion (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d8b2afdd1e8008bc8e03efa670e5a4b37b6dc9f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094318"
---
# <a name="d3dxcreateeffectfromfile-function"></a>D3DXCreateEffectFromFile-Funktion

Erstellen Sie einen Effekt aus einer ASCII- oder binären Effektbeschreibung.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateEffectFromFile(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf das Gerät, das den Effekt erstellt. Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> <dt>

*pSrcFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Dateinamen. Dieser Parameter unterstützt sowohl Unicode- als auch ANSI-Zeichenfolgen. Siehe Hinweise.

</dd> <dt>

*pDefdefine* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***

Optionales auf NULL beendetes Array von Präprozessormakrodefinitionen. Siehe [**D3DXMACRO**](d3dxmacro.md).

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von Include-Direktiven \# verwendet werden soll. Wenn dieser Wert **NULL ist,** wird includes entweder beim Kompilieren aus einer Datei oder beim Kompilieren aus einer Ressource oder einem Arbeitsspeicher \# zu einem Fehler führen.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Wenn *pSrcFile* einen Texteffekt enthält, können Flags eine Kombination aus [D3DXSHADER-Flags](d3dxshader-flags.md) und [D3DXFX-Flags](d3dxfx.md) sein. Andernfalls enthält *pSrcFile* einen binären Effekt, und die einzigen berücksichtigten Flags sind D3DXFX-Flags. Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung. Weitere Informationen finden Sie unter [Effektcompilertool.](../direct3dtools/fxc.md)

</dd> <dt>

*pPool* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Zeiger auf ein [**ID3DXEffectPool-Objekt,**](id3dxeffectpool.md) das für freigegebene Parameter verwendet werden soll. Wenn dieser Wert **NULL** ist, werden keine Parameter freigegeben.

</dd> <dt>

*ppEffect* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Gibt einen Zeiger auf einen Puffer zurück, der den kompilierten Effekt enthält. Siehe [**ID3DXEffect**](id3dxeffect.md).

</dd> <dt>

*ppCompilationErrors* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Zeiger auf einen Puffer zurück, der eine Auflistung von Kompilierungsfehlern enthält. Siehe [**ID3DXBuffer.**](id3dxbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Bemerkungen

Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der LPCTSTR-Datentyp in LPCSTR auflösen.

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateEffectFromFileW auflösen. Andernfalls wird der Funktionsaufruf in D3DXCreateEffectFromFileA auflösen, da ANSI-Zeichenfolgen verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effect-Funktionen](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCompileShader**](d3dxcompileshader.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
