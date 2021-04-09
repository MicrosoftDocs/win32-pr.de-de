---
description: Berechnet das pro-Dreieck-IMT aus einer Textur, die einem Mesh zugeordnet ist, um optional als Eingabe für die D3DX uvatlas-Funktionen verwendet zu werden.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: D3DXComputeIMTFromTexture-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050906"
---
# <a name="d3dxcomputeimtfromtexture-function"></a>D3DXComputeIMTFromTexture-Funktion

Berechnet das pro-Dreieck-IMT aus einer Textur, die einem Mesh zugeordnet ist, um optional als Eingabe für die D3DX [uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)verwendet zu werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ein Zeiger auf ein Eingabe Gitter (siehe [**ID3DXMesh**](id3dxmesh.md)), das die Objekt Geometrie zum Berechnen des IMTS enthält.

</dd> <dt>

*ptexture* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ein Zeiger auf die Textur (siehe [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)), die dem Mesh zugeordnet ist.

</dd> <dt>

*dwtextureindex* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

NULL basierter Texturkoordinaten Index, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Textur Umbruch Optionen. Dies ist eine Kombination aus einem oder mehreren [**D3DXIMT-Flags**](./d3dximt-flags.md).

</dd> <dt>

*pstatus Callback* 
</dt> <dd>

Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Ein Zeiger auf eine Rückruffunktion zum Überwachen des Fortschritts der IMT-Berechnung.

</dd> <dt>

*pusercontext* 
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ein Zeiger auf eine benutzerdefinierte Variable, die an die Status Rückruffunktion übermittelt wird. Wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.

</dd> <dt>

*ppimtdata* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ein Zeiger auf den Puffer (siehe [**ID3DXBuffer**](id3dxbuffer.md)), der das zurückgegebene IMT-Array enthält. Dieses Array kann als Eingabe für die D3DX [uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md) bereitgestellt werden, um die Zuordnung des Textur Raums in der Textur Parametrisierung zu priorisieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK; andernfalls ist der Wert D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Wenn eine Textur über der Oberfläche des Mesh zugeordnet ist, berechnet der Algorithmus den IMT für jedes Gesicht. Dies führt dazu, dass Dreiecke, die Signaldaten niedriger Frequenz enthalten, bei der Parametrisierung mit den uvatlas-Funktionen weniger Speicherplatz im endgültigen Textur Atlas benötigt. Es wird davon ausgegangen, dass die Textur über das Mesh bilinear interpoliert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Verwenden von uvatlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
