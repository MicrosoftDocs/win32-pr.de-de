---
description: Berechnen Sie imT-Werte pro Dreieck aus Daten pro Texel. Diese Funktion ähnelt D3DXComputeIMTFromTexture, verwendet jedoch ein float-Array, um die Daten zu übergeben, und sie kann höhere dimensionale Werte als 4 berechnen.
ms.assetid: 4a151184-e67e-41e9-83c6-63da72f262fa
title: D3DXComputeIMTFromPerTexelSignal-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerTexelSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 48053a238806c223067742b62675f1c0b8bc5a53e8bdf05f78f3fc56520b8388
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299889"
---
# <a name="d3dxcomputeimtfrompertexelsignal-function"></a>D3DXComputeIMTFromPerTexelSignal-Funktion

Berechnen Sie imT-Werte pro Dreieck aus Daten pro Texel. Diese Funktion ähnelt [**D3DXComputeIMTFromTexture,**](d3dxcomputeimtfromtexture.md)verwendet jedoch ein float-Array, um die Daten zu übergeben, und sie kann höhere dimensionale Werte als 4 berechnen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeIMTFromPerTexelSignal(
  _In_  LPD3DXMESH      pMesh,
  _In_  DWORD           dwTextureIndex,
  _In_  FLOAT           *pfTexelSignal,
  _In_  UINT            uWidth,
  _In_  UINT            uHeight,
  _In_  UINT            uSignalDimension,
  _In_  UINT            uComponents,
  _In_  DWORD           dwOptions,
        LPD3DXUVATLASCB pStatusCallback,
        LPVOID          pUserContext,
  _Out_ LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ein Zeiger auf ein Eingabegittermodell (siehe [**ID3DXMesh),**](id3dxmesh.md)das die Objektgeometrie zum Berechnen des IMT enthält.

</dd> <dt>

*dwTextureIndex* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Nullbasierter Texturkoordinatenindex, der an identifiziert, welche Texturkoordinaten verwendet werden.

</dd> <dt>

*pfTexelSignal* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ein Zeiger auf ein Array von Eingabe-Texeln, aus denen IMT berechnet wird. Die Arraygröße ist uWidth \* uHeight \* uComponents.

</dd> <dt>

*uWidth* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Texturbreite in Pixel.

</dd> <dt>

*uHeight* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Texturhöhe in Pixel.

</dd> <dt>

*uSignalDimension* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Gleitkommazahlen pro Komponente in jedem Element des Signalarrays.

</dd> <dt>

*uComponents* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Komponenten in jedem Texel.

</dd> <dt>

*dwOptions* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Texturumbruchoptionen. Dies ist eine Kombination aus mindestens einem [**D3DXIMT-FLAGS.**](./d3dximt-flags.md)

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Ein Zeiger auf eine Rückruffunktion zum Überwachen des IMT-Berechnungsfortschritts.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ein Zeiger auf eine benutzerdefinierte Variable, die an die Statusrückruffunktion übergeben wird. Wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion enthält.

</dd> <dt>

*ppIMTData* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ein Zeiger auf den Puffer (siehe [**ID3DXBuffer),**](id3dxbuffer.md)der das zurückgegebene IMT-Array enthält. Dieses Array kann als Eingabe für die D3DX [UVAtlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md) bereitgestellt werden, um die Texturraumzuordnung in der Texturparameterisierung zu priorisieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D OK, andernfalls ist der Wert \_ D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[UVAtlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Verwenden von UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
