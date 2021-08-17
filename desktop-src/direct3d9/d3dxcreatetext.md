---
description: Erstellt ein Netz mit dem angegebenen Text unter Verwendung der Schriftart, die dem Gerätekontext zugeordnet ist.
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: D3DXCreateText-Funktion (D3dx9shape.h)
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
ms.openlocfilehash: 9db7cc6fa89f8f102cabccdebd14852a50f60576b6135ae52e4cc9fada494812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732294"
---
# <a name="d3dxcreatetext-function"></a>D3DXCreateText-Funktion

Erstellt ein Netz mit dem angegebenen Text unter Verwendung der Schriftart, die dem Gerätekontext zugeordnet ist.

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

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf das Gerät, das das Gitternetz erstellt hat.

</dd> <dt>

*hDC* \[ In\]
</dt> <dd>

Typ: **HDC**

Gerätekontext, der die Schriftart für die Ausgabe enthält. Die vom Gerätekontext ausgewählte Schriftart muss eine TrueType-Schriftart sein.

</dd> <dt>

*pText* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den zu generierenden Text angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen. Siehe Hinweise.

</dd> <dt>

*Abweichung* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Maximale Chordalabweichung von TrueType-Schriftartgliederungen.

</dd> <dt>

*Extrusion* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Betrag, um den Text in negativer Z-Richtung gepresst werden soll.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Zeiger auf das zurückgegebene Netz.

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf einen Puffer, der Adjazienzinformationen enthält. Kann NULL **sein.**

</dd> <dt>

*pGlyphMetrics* \[ out\]
</dt> <dd>

Typ: **[ **LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**

Zeiger auf ein Array von [**GLYPHMETRICSFLOAT-Strukturen,**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) die die Glyphenmetrikdaten enthalten. Jedes Element enthält Informationen über die Position und Ausrichtung des entsprechenden Glyphen in der Zeichenfolge. Die Anzahl der Elemente im Array sollte der Anzahl der Zeichen in der Zeichenfolge entspricht. Beachten Sie, dass der Ursprung in jeder -Struktur nicht relativ zur gesamten Zeichenfolge, sondern relativ zu dieser Zeichenzelle ist. Um das gesamte Begrenzungsfeld zu berechnen, fügen Sie das Inkrement für jedes Glyphen hinzu, während Sie die Zeichenfolge durchlaufen. Wenn Sie sich nicht um die Glyphengrößen sorgen, legen Sie diesen Parameter auf **NULL fest.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateTextW auflösen. Andernfalls wird der Funktionsaufruf in D3DXCreateTextA auflösen, da ANSI-Zeichenfolgen verwendet werden.

Diese Funktion erstellt ein Gitternetz mit der Erstellungsoption D3DXMESH MANAGED und dem flexiblen \_ Vertexformat (FVF) [ \_ \| D3DFVF XYZ D3DFVF \_ NORMAL.](d3dfvf.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9shape.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Formzeichnungsfunktionen](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
