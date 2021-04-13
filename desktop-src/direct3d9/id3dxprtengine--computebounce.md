---
description: Berechnet den Quell Strahl, der sich aus einem einzelnen Sprung der interreflektierten hell ergibt. Diese Methode kann für jede beleuchtete Szene verwendet werden, einschließlich eines auf einer kugelförmigen Harmonika (SH) basierenden PRT-Modells.
ms.assetid: 91a6b503-acd2-459b-9d60-de68c879c61b
title: 'ID3DXPRTEngine:: computebounce-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d40d4b2686087864cad17df0feb99dbc890033b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355706"
---
# <a name="id3dxprtenginecomputebounce-method"></a>ID3DXPRTEngine:: computebounce-Methode

Berechnet den Quell Strahl, der sich aus einem einzelnen Sprung der interreflektierten hell ergibt. Diese Methode kann für jede beleuchtete Szene verwendet werden, einschließlich eines auf einer kugelförmigen Harmonika (SH) basierenden PRT-Modells.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeBounce(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdatain* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Eingabe Objekt, das das 3D-Objekt aus dem vorherigen Licht Sprung darstellt. Dieser Eingabepuffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.

</dd> <dt>

*pdataout* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das einen einzelnen Sprung des interreflektierten Lichts modelliert. Dieser Ausgabepuffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.

</dd> <dt>

*pdatatotal* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein optionales [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, bei dem es sich um die laufende Summe aller vorherigen pdataout-Ausgaben handelt. Kann **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die folgende Aufruf Sequenz, um mehrere Licht Sprünge mit direkter Beleuchtung zu modellieren.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;

ComputeDirectLightingSH( SHOrder, pDataA );
// The accumulation buffer, pDataC, needs to be 
// initialized to the direct lighting result.

pDataC->AddBuffer( pDataA );
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // first bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // second bounce
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // third bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // fourth bounce
```



Verwenden Sie die folgende Aufruf Sequenz, um mehrere Licht Sprünge mit unter Oberflächendaten zu modellieren.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
ComputeDirectLightingSH( SHOrder, pDataA );

// *pDataC should be set to zero. The ComputeSS call will add together     
// the direct lighting results from pDataA for non-subsurface scattering 
// elements and subsurface scattering results for the subsurface scattering
// elements. Perform proper error handling for each call.
    
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // first bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // second bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
```



Die Ausgabe dieser Methode enthält nicht "Albedo", und nur das eingehende Licht ist in den Simulator integriert. Indem Sie Albedo nicht multiplizieren, können Sie Albedo-Variation in einer präziseren Skalierung als die Quell Strahlung modellieren und dadurch genauere Ergebnisse aus der Komprimierung erzielen.

[**ID3DXPRTEngine:: multiplyalbedo**](id3dxprtengine--multiplyalbedo.md) aufzurufen, um jeden PRT-Vektor von Albedo zu multiplizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: computess**](id3dxprtengine--computess.md)
</dt> </dl>

 

 




