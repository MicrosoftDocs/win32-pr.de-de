---
description: Berechnet die Quellleistung, die sich aus der Streuung der Unterfläche ergibt, mithilfe von Materialeigenschaften, die von ID3DXPRTEngine::SetMeshMaterials festgelegt wurden. Diese Methode kann nur für Materialien verwendet werden, die pro Scheitelpunkt in einem Gittermodellobjekt definiert sind.
ms.assetid: cdf0d9c1-70e3-44d5-b97a-0521e6739daf
title: ID3DXPRTEngine::ComputeSS-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSS
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b34561bf96983506cbb0f484f273de9a5e0f0b6138db2e1ddbb92b19c8bcd18f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294020"
---
# <a name="id3dxprtenginecomputess-method"></a>ID3DXPRTEngine::ComputeSS-Methode

Berechnet die Quellleistung, die sich aus der Streuung der Unterfläche ergibt, mithilfe von Materialeigenschaften, die von [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)festgelegt wurden. Diese Methode kann nur für Materialien verwendet werden, die pro Scheitelpunkt in einem Gittermodellobjekt definiert sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeSS(
  [in]      LPD3DXPRTBUFFER pDataIn,
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

*pDataOut* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer-Ausgabeobjekt,**](id3dxprtbuffer.md) das eine einzelne Abprallfläche des Lichts mit Streufläche modelliert. Diesem Ausgabepuffer muss die richtige Anzahl von Farbkanälen für die Simulation zugeordnet sein.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein optionales [**ID3DXPRTBuffer-Objekt,**](id3dxprtbuffer.md) das die laufende Summe aller vorherigen pDataOut-Ausgaben ist. Kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode für jede Lichtprellung auf, nachdem eine ID3DXPRTEngine::ComputeDirectLighting-Methode aufgerufen wurde, um das Streudiagramm der Unterfläche zu modellieren.

Verwenden Sie die folgende aufrufende Sequenz, um die Streuung von Unterflächen zu modellieren.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
    
hr = m_pPRTEngine->ComputeDirectLightingSH( SHOrder, pDataA );
    
// *pDataC should be set to zero. The ComputeSS call will add together the    
// direct lighting results from pDataA for non-subsurface scattering elements   
// and subsurface scattering results for the subsurface scattering elements.
    
hr = m_pPRTEngine->ComputeSS( pDataA, pDataB, pDataC );
if ( FAILED( hr ) ) goto Exit;
```



Die Ausgabe dieser Methode enthält nicht albedo, und nur eingehendes Licht ist in den Simulator integriert. Indem Sie den Albedo nicht multiplizieren, können Sie die Albedo-Variation in einer feineren Skala als die Quellleistung modellieren und so genauere Ergebnisse der Komprimierung erzielen.

Rufen Sie [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) auf, um jeden voraus berechneten PRT-Vektor (Radiance Transfer) mit dem Albedo zu multiplizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeButnce**](id3dxprtengine--computebounce.md)
</dt> </dl>

 

 




