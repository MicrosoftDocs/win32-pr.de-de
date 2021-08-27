---
description: Erstellen Sie einen Effekt aus einer ASCII- oder binären Effektbeschreibung. Dies ist eine erweiterte Version von D3DXCreateEffectFromResource, mit der eine Anwendung steuern kann, welche Parameter vom Effektsystem ignoriert werden.
ms.assetid: 5937bdb1-750a-41f8-a49d-3643427f3e3c
title: D3DXCreateEffectFromResourceEx-Funktion (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResourceEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b72e17e648360a535f8090dc28323a3762a5cec0517f07ae78e9bb6d88045969
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096250"
---
# <a name="d3dxcreateeffectfromresourceex-function"></a>D3DXCreateEffectFromResourceEx-Funktion

Erstellen Sie einen Effekt aus einer ASCII- oder binären Effektbeschreibung. Dies ist eine erweiterte Version von [**D3DXCreateEffectFromResource,**](d3dxcreateeffectfromresource.md) mit der eine Anwendung steuern kann, welche Parameter vom Effektsystem ignoriert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateEffectFromResourceEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
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

Zeiger auf das Gerät.

</dd> <dt>

*hSrcModule* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle für ein Modul, das die Beschreibung des Effekts enthält. Wenn dieser Parameter **NULL ist,** wird das aktuelle Modul verwendet.

</dd> <dt>

*pSrcResource* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf die Ressource. Dieser Parameter unterstützt sowohl Unicode- als auch ANSI-Zeichenfolgen. Siehe Hinweise.

</dd> <dt>

*pDefdefine* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***

Ein **optionales, mit NULL** beendetes Array [**von D3DXMACRO-Strukturen,**](d3dxmacro.md) die Präprozessordefinitionen beschreiben. Dieser Wert kann NULL **sein.**

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von Include-Direktiven \# verwendet werden soll. Wenn dieser Wert **NULL ist,** wird includes entweder beim Kompilieren aus einer Datei oder beim Kompilieren aus einer Ressource oder einem Arbeitsspeicher \# zu einem Fehler führen.

</dd> <dt>

*pSkipConstants* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge von Effektparametern, die vom Effektsystem ignoriert werden. Die Zeichenfolge  muss NULL-terminiert sein und muss den Namen jeder von der Anwendung verwalteten Konstante enthalten, die durch ein Semikolon getrennt ist.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Wenn *pSrcResource* einen Texteffekt enthält, können Flags eine Kombination aus [D3DXSHADER-Flags](d3dxshader-flags.md) und [D3DXFX-Flags](d3dxfx.md) sein. *Andernfalls enthält pSrcResource* einen binären Effekt, und die einzigen flags werden als D3DXFX-Flags verwendet. Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung. Weitere [Informationen finden Sie unter Effect-Compiler Tool](../direct3dtools/fxc.md) .

</dd> <dt>

*pPool* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Zeiger auf ein [**ID3DXEffectPool-Objekt,**](id3dxeffectpool.md) das für freigegebene Parameter verwendet werden soll. Wenn dieser Wert **NULL ist,** werden keine Parameter freigegeben.

</dd> <dt>

*ppEffect* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Gibt einen Puffer zurück, der den kompilierten Effekt enthält.

</dd> <dt>

*ppCompilationErrors* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Puffer zurück, der eine Auflistung von Kompilierungsfehlern enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Funktion ist eine erweiterte Version von [**D3DXCreateEffectFromResource,**](d3dxcreateeffectfromresource.md) mit der eine Anwendung angeben kann, welche Effektkonst constants von der Anwendung verwaltet werden. Eine Konstante, die von der Anwendung verwaltet wird, wird vom Effektsystem ignoriert. Das heißt, die Anwendung ist für die Initialisierung der Konstante sowie für das Speichern und Wiederherstellen des Zustands verantwortlich, wenn dies erforderlich ist.

Diese Funktion überprüft jede Konstante in pSkipConstants, um Dies zu sehen:

-   Sie ist an ein konstantes Register gebunden.
-   Sie wird nur im HLSL-Shadercode verwendet.

Wenn eine Konstante in der Zeichenfolge benannt wird, die im Effekt nicht vorhanden ist, wird sie ignoriert.

Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der LPCTSTR-Datentyp in LPCSTR auflösen.

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateEffectFromResourceW auflösen. Andernfalls wird der Funktionsaufruf in D3DXCreateEffectFromResourceA auflösen, da ANSI-Zeichenfolgen verwendet werden.

D3DXCreateEffectFromResource lädt Daten aus einer Ressource vom Typ RT \_ RCDATA. Weitere Informationen zu Ressourcen finden Sie Windows MSDN.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effect-Funktionen](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectEx**](d3dxcreateeffectex.md)
</dt> <dt>

[**D3DXCreateEffectFromFileEx**](d3dxcreateeffectfromfileex.md)
</dt> </dl>

 

 
