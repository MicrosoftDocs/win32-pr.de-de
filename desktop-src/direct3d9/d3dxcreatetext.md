---
description: Erstellt ein Mesh mit dem angegebenen Text unter Verwendung der Schriftart, die dem Gerätekontext zugeordnet ist.
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: D3DXCreateText-Funktion (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f6202a534dde727e21b6513ad30077f2e3b3e52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366467"
---
# <a name="d3dxcreatetext-function"></a>D3DXCreateText-Funktion

Erstellt ein Mesh mit dem angegebenen Text unter Verwendung der Schriftart, die dem Gerätekontext zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf das Gerät, das das Mesh erstellt hat.

</dd> <dt>

*hdc* \[ in\]
</dt> <dd>

Typ: **hdc**

Gerätekontext, der die Schriftart für die Ausgabe enthält. Die vom Gerätekontext ausgewählte Schriftart muss eine TrueType-Schriftart sein.

</dd> <dt>

*ptext* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den zu Generier Text angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der String-Datentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*Abweichung* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Maximale Zeichen Abweichung von TrueType-Schriftart umrissen.

</dd> <dt>

*Extrusion* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Betrag, um den Text in der negativen z-Richtung zu extrudieren.

</dd> <dt>

*ppmesh* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Zeiger auf das zurückgegebene Mesh.

</dd> <dt>

*ppency* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf einen Puffer, der Informationen zu Informationen enthält. Kann **null** sein.

</dd> <dt>

*pglyphmetrics* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **lpglyphmetricsfloat**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**

Zeiger auf ein Array von [**glyphmetricsfloat**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) -Strukturen, die die Glyphe-Metrikdaten enthalten. Jedes-Element enthält Informationen zur Position und Ausrichtung des entsprechenden Symbols in der Zeichenfolge. Die Anzahl der Elemente im Array sollte gleich der Anzahl der Zeichen in der Zeichenfolge sein. Beachten Sie, dass der Ursprung in jeder Struktur nicht relativ zur gesamten Zeichenfolge ist, sondern relativ zu dieser Zeichen Zelle ist. Fügen Sie das Inkrement für jedes Symbol beim Durchlaufen der Zeichenfolge hinzu, um das gesamte umgebende Feld zu berechnen. Wenn Sie sich nicht mit den Symbolgrößen beschäftigen, legen Sie diesen Parameter auf **null** fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateTextW aufgelöst. Andernfalls wird der Funktions Aufruhe in D3DXCreateTextA aufgelöst, da ANSI-Zeichen folgen verwendet werden.

Diese Funktion erstellt ein Mesh mit der D3DXMESH \_ Managed Creation-Option und [D3DFVF \_ XYZ \| D3DFVF \_ Normal](d3dfvf.md) flexibles Scheitelpunkt Format (FVF).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9shape. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Formen Zeichnungsfunktionen](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
