---
description: Gibt ein Mesh mit Änderungen zurück, die sich aus der Adaptive räumlichen Stichprobe ergeben Das zurückgegebene Mesh enthält nur Positionen, normale und Texturkoordinaten (sofern definiert).
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: 'ID3DXPRTEngine:: getadaptedmesh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetAdaptedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d012344a5dfbc1bc17780cb4ab9a53820fe34f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355696"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a>ID3DXPRTEngine:: getadaptedmesh-Methode

Gibt ein Mesh mit Änderungen zurück, die sich aus der Adaptive räumlichen Stichprobe ergeben Das zurückgegebene Mesh enthält nur Positionen, normale und Texturkoordinaten (sofern definiert).

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAdaptedMesh(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in, out] UINT              *pFaceRemap,
  [in, out] UINT              *pVertRemap,
  [in, out] FLOAT             *pfVertWeights,
  [out]     LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf ein [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Gerät, das zum Erstellen des Ausgabe Netzes verwendet wird.

</dd> <dt>

*pfakeremap* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Zeiger auf das ursprüngliche Gitter Gesicht, das geteilt wurde, um die aktuelle Seite zu generieren.

</dd> <dt>

*pvertremap* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Ein Zeiger auf ein Ziel Array, das die drei ursprünglichen Gitter Scheitel Punkte enthält, die die übergeordneten Elemente des aktuellen Scheitel Punkts sind.

</dd> <dt>

*pfvertgewichtungen* \[ in, out\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Ein Zeiger auf ein Ziel Array, das die Mischungs Faktoren für die pvertremap-Vertices enthält.

</dd> <dt>

*ppmesh* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Zeiger auf das Ausgabe [**ID3DXMesh**](id3dxmesh.md) Mesh-Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall

## <a name="remarks"></a>Bemerkungen

pvertremap und pfvertgewichtungen können verwendet werden, um einen beliebigen pro-Vertex-Wert über das Mesh zu interpolieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
