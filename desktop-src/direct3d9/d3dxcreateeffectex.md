---
description: Erstellt einen Effekt aus einer ASCII- oder binären Effektbeschreibung. Diese Funktion ist eine erweiterte Version von D3DXCreateEffect, mit der eine Anwendung steuern kann, welche Parameter vom Effektsystem ignoriert werden.
ms.assetid: b08f727e-6061-4e78-8243-08c4ccab342d
title: D3DXCreateEffectEx-Funktion (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 19321dde9f44a2262ee3875d40bd5822e65eff9b84d1fc01656993ea584a8dc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988650"
---
# <a name="d3dxcreateeffectex-function"></a>D3DXCreateEffectEx-Funktion

Erstellt einen Effekt aus einer ASCII- oder binären Effektbeschreibung. Diese Funktion ist eine erweiterte Version von [**D3DXCreateEffect,**](d3dxcreateeffect.md) mit der eine Anwendung steuern kann, welche Parameter vom Effektsystem ignoriert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateEffectEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
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

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf einen Puffer, der eine Effektbeschreibung enthält.

</dd> <dt>

*SrcDataLen* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Länge der Effektdaten in Bytes.

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

*pSkipConstants* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge von Effektparametern, die vom Effektsystem ignoriert werden. Die Zeichenfolge  muss NULL-terminiert sein und den Namen jeder von der Anwendung verwalteten Konstante enthalten, die durch ein Semikolon getrennt ist.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Wenn *pSrcData* einen Texteffekt enthält, können Flags eine Kombination aus [D3DXSHADER-Flags](d3dxshader-flags.md) und [D3DXFX-Flags](d3dxfx.md) sein. Andernfalls enthält *pSrcData* einen binären Effekt, und die einzigen berücksichtigten Flags sind D3DXFX-Flags. Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung. Weitere Informationen finden Sie [unter Effektcompilertool.](../direct3dtools/fxc.md)

</dd> <dt>

*pPool* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Zeiger auf ein [**ID3DXEffectPool-Objekt,**](id3dxeffectpool.md) das für freigegebene Parameter verwendet werden soll. Wenn dieser Wert **NULL** ist, werden keine Parameter freigegeben.

</dd> <dt>

*ppEffect* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Gibt einen Zeiger auf eine [**ID3DXEffect-Schnittstelle**](id3dxeffect.md) zurück.

</dd> <dt>

*ppCompilationErrors* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Puffer zurück, der eine Liste von Kompilierungsfehlern enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Funktion ist eine erweiterte Version von [**D3DXCreateEffect,**](d3dxcreateeffect.md) mit der eine Anwendung angeben kann, welche Effektkonstanten von der Anwendung verwaltet werden. Eine Konstante, die von der Anwendung verwaltet wird, wird vom Effektsystem ignoriert. Das heißt, die Anwendung ist für die Initialisierung der Konstante sowie für das Speichern und Wiederherstellen ihres Zustands verantwortlich, sofern dies angemessen ist.

Diese Funktion überprüft jede Konstante in pSkipConstants, um Dies zu überprüfen:

-   Sie ist an ein Konstantenregister gebunden.
-   Sie wird nur im HLSL-Shadercode verwendet.

Wenn eine Konstante in der Zeichenfolge benannt wird, die im Effekt nicht vorhanden ist, wird sie ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effect-Funktionen](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectFromFileEx**](d3dxcreateeffectfromfileex.md)
</dt> <dt>

[**D3DXCreateEffectFromResourceEx**](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
