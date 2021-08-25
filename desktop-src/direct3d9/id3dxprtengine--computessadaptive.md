---
description: Berechnet einen Übertragungsvektor, der die Quellfläche zuordnt, um die Ausmusterung zu beenden, die sich aus der Subsurface-Punktung ergibt. Dabei werden adaptive Stichproben und Materialeigenschaften verwendet, die von ID3DXPRTEngine::SetMeshMaterials festgelegt werden.
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: ID3DXPRTEngine::ComputeSSAdaptive-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a602566c4d0e5b3cb5c68b2f983b6c56a9d9f596ee673db97a72e6054837759b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847380"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a>ID3DXPRTEngine::ComputeSSAdaptive-Methode

Berechnet einen Übertragungsvektor, der die Quellfläche zu einer Ausgangsfläche zuordnt, die sich aus der Subsurface-Punktung ergibt. Dabei werden die adaptive Stichprobenentnahme und die von [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)festgelegten Materialeigenschaften verwendet. Die -Methode generiert neue Scheitelzeichen und Gesichter im Gitternetz, um das PRT-Signal (Precomputed Radiance Transfer) genauer zu ungefähren. Diese Methode kann nur für Materialien verwendet werden, die pro Scheitelpunkt in einem Gittermodellobjekt definiert sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeSSAdaptive(
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

Zeiger auf ein [**EINGABE-ID3DXPRTBuffer-Objekt,**](id3dxprtbuffer.md) das das 3D-Objekt aus dem vorherigen Lichtsprung darstellt. Für diesen Eingabepuffer muss die richtige Anzahl von Farbkanälen für die Simulation zugeordnet sein.

</dd> <dt>

*AdaptiveThresh* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Schwellenwert für den PRT-Vektor, der für die Unterteilung von Gitternetzvertices und Gesichtern verwendet werden soll. Wenn kleiner als 1e-6f, wird der Standardwert 1e-6f angegeben.

</dd> <dt>

*MinEdgeLength* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Minimale Länge des Gesichtsrands, die bei adaptiver Stichprobenentnahme generiert wird. Wenn die -Methode feststellt, dass der Wert zu klein ist, wird ein modellabhängiger Wert angegeben.

</dd> <dt>

*MaxSubdiv* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Maximale Unterteilung eines Gesichts, das bei der adaptiven Stichprobenentnahme verwendet wird. Wenn 0 (null) ist, wird der Standardwert 4 angegeben.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**AUSGABE-ID3DXPRTBuffer-Objekt,**](id3dxprtbuffer.md) das einen einzelnen Bounce des im Unteroberflächen-Punktdiagramm angezeigten Lichts modelliert. Für diesen Ausgabepuffer muss die richtige Anzahl von Farbkanälen für die Simulation zugeordnet sein.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein optionales [**ID3DXPRTBuffer-Objekt,**](id3dxprtbuffer.md) das die laufende Summe aller vorherigen pDataOut-Ausgaben ist. Kann NULL **sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode für jeden lichten Bounce auf, nachdem eine [**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive-Methode**](id3dxprtengine--computedirectlightingshadaptive.md) aufgerufen wurde, um die Subsurface-Punktung zu modellieren.

Die Ausgabe dieser Methode enthält kein Albedo, und nur eingehendes Licht ist in den Simulator integriert. Wenn Sie den Albedo nicht multiplizieren, können Sie albedo-Variationen in einer feineren Skala als die Quellleistung modellieren und so genauere Ergebnisse aus der Komprimierung erzielen.

Rufen [**Sie ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) auf, um jeden PRT-Vektor mit dem Albedo zu multiplizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounce**](id3dxprtengine--computebounce.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeSS**](id3dxprtengine--computess.md)
</dt> </dl>

 

 
