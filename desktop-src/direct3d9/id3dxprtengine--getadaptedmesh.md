---
description: Gibt ein Gitternetz mit Änderungen zurück, die sich aus adaptiver räumlicher Stichprobenentnahme ergeben. Das zurückgegebene Gitternetz enthält nur Positionen, Normalstellen und Texturkoordinaten (sofern definiert).
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: ID3DXPRTEngine::GetAdaptedMesh-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: e5e38937628bc36f49059bcb3e798a6d13e538c572c1c5fb6ef20865ed05385d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747670"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a>ID3DXPRTEngine::GetAdaptedMesh-Methode

Gibt ein Gitternetz mit Änderungen zurück, die sich aus adaptiver räumlicher Stichprobenentnahme ergeben. Das zurückgegebene Gitternetz enthält nur Positionen, Normalstellen und Texturkoordinaten (sofern definiert).

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

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf ein [**IDirect3DDevice9-Gerät,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das zum Erstellen des Ausgabegitters verwendet wird.

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf das ursprüngliche Gitternetz, das geteilt wurde, um das aktuelle Gesicht zu generieren.

</dd> <dt>

*pVertRemap* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf ein Zielarray, das die drei ursprünglichen Gitternetz-Scheitelpunkte enthält, die die über-Elemente des aktuellen Scheitelpunkts sind.

</dd> <dt>

*pfVertWeights* \[ in, out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf ein Zielarray, das Blendingfaktoren für die Scheitelpunkte pVertRemap enthält.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Zeiger auf das [**Ausgabe-ID3DXMesh-Gittermodellobjekt.**](id3dxmesh.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

pVertRemap und pfVertWeights können verwendet werden, um jeden Scheitelpunktwert über das Gitternetz zu interpolieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
