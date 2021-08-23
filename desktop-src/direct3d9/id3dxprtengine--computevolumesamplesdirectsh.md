---
description: Berechnet eine Projektion entfernter Beleuchtung in SH-Basisvektoren (Spherical Vector), die die Strahlkraft von Vorfällen an angegebenen Stellen darstellen.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: ID3DXPRTEngine::ComputeVolumeSamplesDirectSH-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3aaa8f9332a80e35ffde43d145be1ed885caeaca6d61e4eb9190baba09b73ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747760"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a>ID3DXPRTEngine::ComputeVolumeSamplesDirectSH-Methode

Berechnet eine Projektion entfernter Beleuchtung in SH-Basisvektoren (Spherical Vector), die die Strahlkraft von Vorfällen an angegebenen Stellen darstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OrderIn* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Darstellung entfernter Beleuchtung. Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Der Grad der Auswertung ist OrderIn - 1.

</dd> <dt>

*OrderOut* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Darstellung der lokalen Beleuchtung. Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Der Grad der Auswertung ist OrderOut - 1.

</dd> <dt>

*NumVolSamples.xml* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl von Beispielspeicherorten.

</dd> <dt>

*pSampleLocs* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Position für jedes Beispiel.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**Id3DXPRTBuffer-Ausgabeobjekt,**](id3dxprtbuffer.md) das die entfernte Beleuchtung in SH-Basisvektoren projiziert. Diesem Puffer muss die richtige Anzahl von Farbkanälen für die Simulation zugeordnet sein. Diese Methode generiert OrderInlimit \* OrderOut"skalare Skalar pro Kanal an jedem Beispielspeicherort.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Methode berechnet, wie Licht aus einer entfernten Quelle an jedem Punkt im durch pSampleLocs angegebenen Raum eintrifft. Die SH-Koeffizienten stellen an jedem pSampleLocs-Punkt die Zuordnung des Quellstrahls zum übertragenen Vorfallsmaß dar.

Um diese Methode erfolgreich zu verwenden, müssen Sie die Stichprobenentnahme für eine Kugel mit UseSphere = **TRUE** und UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)festlegen. Andernfalls gibt diese Methode einen Fehler mit D3DERR \_ INVALIDCALL zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
