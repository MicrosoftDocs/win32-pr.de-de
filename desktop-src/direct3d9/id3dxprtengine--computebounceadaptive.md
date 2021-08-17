---
description: Berechnet mithilfe der adaptiven Stichprobenentnahme die Quellleistung, die sich aus einem einzelnen Sprung von lichtverschiedenem Licht ergibt.
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: ID3DXPRTEngine::ComputeButnceAdaptive-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: efe983a0160d46910e7b8d1e29d0042d801275ef70aef30f6050e0538b6f9927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729749"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a>ID3DXPRTEngine::ComputeBounceAdaptive-Methode

Berechnet mithilfe der adaptiven Stichprobenentnahme die Quellleistung, die sich aus einem einzelnen Sprung von lichtverschiedenem Licht ergibt. Diese Methode generiert neue Scheitelpunkte und Gesichter im Netz, um das PRT-Signal (Precomputed Radiance Transfer) genauer anzunähern. Diese Methode kann für jede beleuchtete Szene verwendet werden, einschließlich eines SH-basierten PRT-Modells (SphericalLassing).

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeBounceAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDataIn* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**EINGABE-ID3DXPRTBuffer-Objekt,**](id3dxprtbuffer.md) das das 3D-Objekt aus dem vorherigen lichten Hüpfen darstellt. Diesem Eingabepuffer muss die richtige Anzahl von Farbkanälen für die Simulation zugeordnet sein.

</dd> <dt>

*AdaptiveThresh* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Schwellenwert für den PRT-Vektor, der zum Unterteilen von Gitternetzvertices und Gesichtern verwendet werden soll. Wenn kleiner als 1e-6f ist, wird der Standardwert 1e-6f angegeben.

</dd> <dt>

*MinEdgeLength* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Minimale Länge des Gesichtsrands, die bei der adaptiven Stichprobenentnahme generiert wird. Wenn die -Methode feststellt, dass der Wert zu klein ist, wird ein modellabhängiger Wert angegeben. Bei 0 (null) wird der Standardwert 4 angegeben.

</dd> <dt>

*MaxSubdiv* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Maximale Unterteilungsebene eines Gesichts, die bei der adaptiven Stichprobenentnahme verwendet wird.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer-Ausgabeobjekt.**](id3dxprtbuffer.md) Diesem Ausgabepuffer muss die richtige Anzahl von Farbkanälen für die Simulation zugeordnet sein.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein optionales [**ID3DXPRTBuffer-Objekt,**](id3dxprtbuffer.md) das eine laufende Summe von pDataOut bei jeder Light Bounce-Berechnung beihält. Kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
