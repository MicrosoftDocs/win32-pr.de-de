---
description: Berechnet Einheitennormle für jeden Scheitelpunkt in einem Gitternetz. Wird zur Unterstützung von Legacyanwendungen bereitgestellt. Verwenden Sie D3DXComputeTangentFrameEx, um bessere Ergebnisse zu erzielen.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: D3DXComputeNormals-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d136e7c3d01b595273127c500ccc52cd310357df2147f3df5d97df9dbd38d38d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069310"
---
# <a name="d3dxcomputenormals-function"></a>D3DXComputeNormals-Funktion

Berechnet Einheitennormle für jeden Scheitelpunkt in einem Gitternetz. Wird zur Unterstützung von Legacyanwendungen bereitgestellt. Verwenden [**Sie D3DXComputeTangentFrameEx,**](d3dxcomputetangentframeex.md) um bessere Ergebnisse zu erzielen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMesh* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Zeiger auf eine [**ID3DXBaseMesh-Schnittstelle,**](id3dxbasemesh.md) die das normalisierte Gittermodellobjekt darstellt.

</dd> <dt>

*pAdjacency* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im erstellten progressiven Gitter angeben. Dieser Parameter ist optional und sollte auf **NULL festgelegt werden,** wenn er nicht verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Für das Eingabegitternetz muss das [Flag D3DFVF \_ NORMAL](d3dfvf.md) im flexiblen Scheitelpunktformat (Flexible Vertex Format, FVF) angegeben sein.

Ein Normalwert für einen Scheitelpunkt wird generiert, indem die Normaldaten aller Gesichter, die diesen Scheitelpunkt gemeinsam haben, durchschnittlich abschn.

Wenn Adjacency bereitgestellt wird, werden replizierte Scheitelungen ignoriert und "geglättet". Wenn keine Adjacency bereitgestellt wird, weisen replizierte Scheitelpunktwerte normal aus, die nur von den Gesichtern gemittelt werden, die explizit auf sie verweisen.

Diese Funktion ruft einfach [**D3DXComputeTangentFrameEx mit**](d3dxcomputetangentframeex.md) den folgenden Eingabeparametern auf:


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
