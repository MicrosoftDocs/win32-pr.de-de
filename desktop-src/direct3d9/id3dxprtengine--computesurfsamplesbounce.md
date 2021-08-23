---
description: Berechnet prt-Stichproben (Precomputed Radiance Transfer) für einen beliebigen Punkt (und normalen Vektor).
ms.assetid: 862a9067-5c5e-4428-86f4-ebef653411b9
title: ID3DXPRTEngine::ComputeMultiSamplesBounce-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 925b5da620ae665e0fa863527c196b65a5dfcb17dd81de1c25a23b907cb88ba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492710"
---
# <a name="id3dxprtenginecomputesurfsamplesbounce-method"></a>ID3DXPRTEngine::ComputeKapselSamplesBounce-Methode

Berechnet prt-Stichproben (Precomputed Radiance Transfer) für einen beliebigen Punkt (und normalen Vektor).

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeSurfSamplesBounce(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut,
  [in, out]       LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDataIn* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**EINGABE-ID3DXPRTBuffer-Objekt,**](id3dxprtbuffer.md) das die Quellleistung des 3D-Objekts darstellt. Diesem Eingabepuffer muss die richtige Anzahl von Farbkanälen für die Simulation zugeordnet sein.

</dd> <dt>

*NumSamples* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl von Beispielspeicherorten.

</dd> <dt>

*pSampleLocs* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Position für jedes Beispiel.

</dd> <dt>

*pSampleNorms* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Normaler Vektor für jede Beispielposition.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer-Ausgabeobjekt,**](id3dxprtbuffer.md) das den direkten Beleuchtungsbeitrag an den Punkt modelliert, wobei die Sphärische Gleichung (SH) verwendet wird.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein optionales [**ID3DXPRTBuffer-Objekt,**](id3dxprtbuffer.md) das die laufende Summe aller vorherigen pDataOut-Ausgaben ist. Kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeBatsamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)
</dt> </dl>

 

 
