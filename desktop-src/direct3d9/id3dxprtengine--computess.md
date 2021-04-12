---
description: 'Berechnet mithilfe von Materialeigenschaften, die von ID3DXPRTEngine:: setmeschmaterials festgelegt wurden, die Quell Strahlung, die sich aus der unter Oberflächenstruktur ergibt. Diese Methode kann nur für Materialien verwendet werden, die pro-Vertex in einem Mesh-Objekt definiert sind.'
ms.assetid: cdf0d9c1-70e3-44d5-b97a-0521e6739daf
title: 'ID3DXPRTEngine:: computess-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 89a69be6cc946ff6695d234b8bfb82532385526e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356066"
---
# <a name="id3dxprtenginecomputess-method"></a>ID3DXPRTEngine:: computess-Methode

Berechnet mithilfe von Materialeigenschaften, die von [**ID3DXPRTEngine:: setmeschmaterials**](id3dxprtengine--setmeshmaterials.md)festgelegt wurden, die Quell Strahlung, die sich aus der unter Oberflächenstruktur ergibt. Diese Methode kann nur für Materialien verwendet werden, die pro-Vertex in einem Mesh-Objekt definiert sind.

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

*pdatain* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Eingabe Objekt, das das 3D-Objekt aus dem vorherigen Licht Sprung darstellt. Dieser Eingabepuffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.

</dd> <dt>

*pdataout* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ein Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das einen einzelnen Sprung der unter Oberfläche durch verstreut-Licht modelliert. Dieser Ausgabepuffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.

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

Um die unter Surface-Struktur zu modellieren, wird diese Methode für jeden Licht Sprung aufgerufen, nachdem eine ID3DXPRTEngine:: computedirectlighting-Methode aufgerufen wurde.

Verwenden Sie die folgende Aufruf Sequenz, um die unter Oberflächenstruktur zu modellieren.


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



Die Ausgabe dieser Methode enthält nicht "Albedo", und nur das eingehende Licht ist in den Simulator integriert. Indem Sie Albedo nicht multiplizieren, können Sie Albedo-Variation in einer präziseren Skalierung als die Quell Strahlung modellieren und dadurch genauere Ergebnisse aus der Komprimierung erzielen.

Rufen Sie [**ID3DXPRTEngine:: multiplyalbedo**](id3dxprtengine--multiplyalbedo.md) auf, um jeden PRT-Vektor (preberechneten Radiance Transfer) von Albedo zu multiplizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: computebounce**](id3dxprtengine--computebounce.md)
</dt> </dl>

 

 




