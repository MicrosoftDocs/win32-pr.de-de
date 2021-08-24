---
description: Berechnet die Quellspiegelung, die sich aus einem einzelnen Bounce des gespiegelten Lichts ergibt. Diese Methode kann für jede litierte Szene verwendet werden, einschließlich eines SH-basierten PRT-Modells (Precomputed Radiance Transfer).
ms.assetid: 91a6b503-acd2-459b-9d60-de68c879c61b
title: ID3DXPRTEngine::ComputeBounce-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: cc4f362555c8cc86857733ecc3e75279dc68cc6b339f641f70c592f0e3576a96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847420"
---
# <a name="id3dxprtenginecomputebounce-method"></a>ID3DXPRTEngine::ComputeBounce-Methode

Berechnet die Quellspiegelung, die sich aus einem einzelnen Bounce des gespiegelten Lichts ergibt. Diese Methode kann für jede litierte Szene verwendet werden, einschließlich eines SH-basierten PRT-Modells (Precomputed Radiance Transfer).

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

*pDataIn* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**EINGABE-ID3DXPRTBuffer-Objekt,**](id3dxprtbuffer.md) das das 3D-Objekt aus dem vorherigen Lichtsprung darstellt. Für diesen Eingabepuffer muss die richtige Anzahl von Farbkanälen für die Simulation zugeordnet sein.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer-Ausgabeobjekt,**](id3dxprtbuffer.md) das einen einzelnen Bounce des gespiegelten Lichts modelliert. Für diesen Ausgabepuffer muss die richtige Anzahl von Farbkanälen für die Simulation zugeordnet sein.

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

Verwenden Sie die folgende Aufrufsequenz, um mehrere Lichtabsprungseffekte mit direkter Beleuchtung zu modellieren.


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



Verwenden Sie die folgende Aufrufsequenz, um mehrere lichte Bounces mit Unteroberflächen-Punktung zu modellieren.


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



Die Ausgabe dieser Methode enthält kein Albedo, und nur eingehendes Licht ist in den Simulator integriert. Wenn Sie die Albedo nicht multiplizieren, können Sie Albedo-Variationen mit einer feineren Skala als die Quellbreite modellieren, wodurch genauere Ergebnisse der Komprimierung erzielt werden.

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

[**ID3DXPRTEngine::ComputeSS**](id3dxprtengine--computess.md)
</dt> </dl>

 

 




