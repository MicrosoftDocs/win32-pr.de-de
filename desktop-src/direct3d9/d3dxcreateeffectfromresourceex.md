---
description: Erstellen eines Effekts aus einer Beschreibung des ASCII-oder binären Effekts. Dies ist eine erweiterte Version von D3DXCreateEffectFromResource, mit der eine Anwendung steuern kann, welche Parameter vom Effects-System ignoriert werden.
ms.assetid: 5937bdb1-750a-41f8-a49d-3643427f3e3c
title: D3DXCreateEffectFromResourceEx-Funktion (D3DX9Effect. h)
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
ms.openlocfilehash: d0ae7a0ee43f93019f3c4c1f6145b3d8aa0e4367
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363996"
---
# <a name="d3dxcreateeffectfromresourceex-function"></a>D3DXCreateEffectFromResourceEx-Funktion

Erstellen eines Effekts aus einer Beschreibung des ASCII-oder binären Effekts. Dies ist eine erweiterte Version von [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) , mit der eine Anwendung steuern kann, welche Parameter vom Effects-System ignoriert werden.

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

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf das Gerät.

</dd> <dt>

*hsrcmodule* \[ in\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle für ein Modul, das die Beschreibung des Effekts enthält. Wenn dieser Parameter **null** ist, wird das aktuelle Modul verwendet.

</dd> <dt>

*psrkresource* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ein Zeiger auf die Ressource. Dieser Parameter unterstützt Unicode-und ANSI-Zeichen folgen. Siehe Hinweise.

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

*pskipkonstanten* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge von Effekt Parametern, die vom Effektsystem ignoriert werden. Die Zeichenfolge muss **null** sein und muss den Namen jeder von der Anwendung verwalteten Konstante enthalten, die durch ein Semikolon getrennt ist.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Wenn *psrkresource* einen Text Effekt enthält, können Flags eine Kombination aus [D3DXSHADER-Flags](d3dxshader-flags.md) und [D3DXFX](d3dxfx.md) -Flags sein. Andernfalls enthält *psrkresource* einen binären Effekt, und die einzigen Flags, die berücksichtigt werden, sind D3DXFX-Flags. Der Direct3D 10 HLSL-Compiler ist nun der Standard. Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .

</dd> <dt>

*ppool* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Zeiger auf ein [**ID3DXEffectPool**](id3dxeffectpool.md) -Objekt, das für freigegebene Parameter verwendet werden soll. Wenn dieser Wert **null** ist, werden keine Parameter freigegeben.

</dd> <dt>

*ppeer-ect* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Gibt einen Puffer zurück, der den kompilierten Effekt enthält.

</dd> <dt>

*ppcompilationerrors* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Puffer zurück, der eine Auflistung der Kompilierungsfehler enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist eine erweiterte Version von [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) , mit der eine Anwendung angeben kann, welche Effekt Konstanten von der Anwendung verwaltet werden. Eine Konstante, die von der Anwendung verwaltet wird, wird vom Effects-System ignoriert. Das heißt, die Anwendung ist dafür verantwortlich, die Konstante zu initialisieren und ihren Zustand zu speichern und wiederherzustellen, wenn dies angemessen ist.

Diese Funktion überprüft jede Konstante in pskipkonstanten, um Folgendes anzuzeigen:

-   Er ist an ein konstantes Register gebunden.
-   Sie wird nur im HLSL-Shader-Code verwendet.

Wenn eine Konstante in der Zeichenfolge benannt wird, die nicht in der Auswirkung vorhanden ist, wird Sie ignoriert.

Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der LPCTSTR-Datentyp in LPCSTR aufgelöst.

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateEffectFromResourceW aufgelöst. Andernfalls wird der Funktions Aufruhe in D3DXCreateEffectFromResourceA aufgelöst, da ANSI-Zeichen folgen verwendet werden.

D3DXCreateEffectFromResource lädt Daten aus einer Ressource vom Typ RT \_ RCDATA. Weitere Informationen zu Windows-Ressourcen finden Sie in der MSDN-Website.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Funktionen](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectEx**](d3dxcreateeffectex.md)
</dt> <dt>

[**D3DXCreateEffectFromFileEx**](d3dxcreateeffectfromfileex.md)
</dt> </dl>

 

 
