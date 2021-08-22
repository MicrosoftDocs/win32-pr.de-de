---
description: Berechnet den direkten Beleuchtungsbeitrag zu 3D-Objekten, bei denen die Quellausmaßung durch eine Sphärische Gleichung (SH) dargestellt wird, wobei adaptive Stichprobenentnahme verwendet wird.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: ID3DXPRTEngine::ComputeDirectLightingSHAdaptive-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 991337b31b10c39cccb622c2838bd53bcb25ad534ae8f896b6ec8f4842072de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801280"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a>ID3DXPRTEngine::ComputeDirectLightingSHAdaptive-Methode

Berechnet den direkten Beleuchtungsbeitrag zu 3D-Objekten, bei denen die Quellausmaßung durch eine Sphärische Gleichung (SH) dargestellt wird, wobei adaptive Stichprobenentnahme verwendet wird. Diese Methode generiert neue Scheitelpunkte und Gesichter im Netz, um das PRT-Signal (Precomputed Radiance Transfer) genauer anzunähern.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order²-Koeffizienten. Der Grad der Auswertung ist "Order - 1".

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

Zeiger auf ein [**ID3DXPRTBuffer-Ausgabeobjekt.**](id3dxprtbuffer.md) Diesem Puffer muss die richtige Anzahl von Farbkanälen für die Simulation zugeordnet sein.

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

 

 
