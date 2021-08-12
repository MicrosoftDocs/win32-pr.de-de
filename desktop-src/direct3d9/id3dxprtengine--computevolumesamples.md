---
description: Berechnet eine Projektion der direkten Beleuchtung aus dem vorherigen Lichtprall in SH-Basisvektoren (Spherical Vector), die die Strahlkraft von Vorfällen an angegebenen Stellen darstellen.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: ID3DXPRTEngine::ComputeVolumeSamples-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edc13e8b6f0e5c725e957be22f1b297f825a4f3b622ced68adf19b34a0b64b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293501"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a>ID3DXPRTEngine::ComputeVolumeSamples-Methode

Berechnet eine Projektion der direkten Beleuchtung aus dem vorherigen Lichtprall in SH-Basisvektoren (Spherical Vector), die die Strahlkraft von Vorfällen an angegebenen Stellen darstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDataIn* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**EINGABE-ID3DXPRTBuffer-Objekt,**](id3dxprtbuffer.md) das das 3D-Objekt aus dem vorherigen lichten Hüpfen darstellt.

</dd> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order²-Koeffizienten. Der Grad der Auswertung ist "Order - 1".

</dd> <dt>

*NumVolSamples.xml* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl von Beispielspeicherorten.

</dd> <dt>

*pSampleLocs* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Position für jedes Beispiel. Wenn pSampleLocs **NULL** ist, berechnet ComputeVolumeSamples Übertragungsmatrizen an jedem Gittervertex. Wenn pSampleLocs jedoch nicht **NULL** ist, müssen Sie eine Stichprobe für eine Kugel erstellen (legen Sie UseSphere = **TRUE** und UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo fest).**](id3dxprtengine--setsamplinginfo.md) Andernfalls gibt ComputeVolumeSamples D3DERR \_ INVALIDCALL zurück.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer-Ausgabeobjekt,**](id3dxprtbuffer.md) das die direkte Beleuchtung des vorherigen Lichts projiziert, springt in SH-Basisvektoren. Diesem Puffer muss die richtige Anzahl von Farbkanälen für die Simulation zugeordnet sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Methode berechnet, wie das Licht aus der Quellstrahlfunktion von der Oberfläche reflektiert wird, die die Szene darstellt (pDataIn) und an jedem Punkt im durch pSampleLocs angegebenen Raum eingeht. Die SH-Koeffizienten stellen an jedem pSampleLocs-Punkt die Zuordnung des Quellstrahls zum übertragenen Vorfallsmaß dar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
