---
description: Berechnet lokal deformierbare precomputed radiance transfer (LDPRT)-Koeffizienten relativ zu normalen Vektoren pro Stichprobe, um den Fehler der geringsten Quadrate in Bezug auf id3DXPRTBuffer-Eingabedaten zu minimieren.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: ID3DXPRTEngine::ComputeLDPRTCoeffs-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a432f1df1ad905ca3200789aa6245212cc180d4c7ef5a8723cf02695aeeb7454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294036"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a>ID3DXPRTEngine::ComputeLDPRTCoeffs-Methode

Berechnet lokal deformierbare precomputed radiance transfer (LDPRT)-Koeffizienten relativ zu normalen Vektoren pro Stichprobe, um den Fehler mit den geringsten Quadraten in Bezug auf eingabebasierte [**ID3DXPRTBuffer-Daten**](id3dxprtbuffer.md) zu minimieren. Diese Koeffizienten können mit skinnierten oder transformierten normalen Vektoren verwendet werden, um globale Effekte auf dynamische Objekte zu modellieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDataIn* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**EINGABE-ID3DXPRTBuffer-SH-Datenobjekt**](id3dxprtbuffer.md) (Precomputed Radiance Transfer).

</dd> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order Koeffizienten. Der Grad der Auswertung ist Order - 1.

</dd> <dt>

*pNormOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Optionales Vektorarray, das mit shaderoptimierten normalen Vektoren gefüllt werden soll, für die LDPRT-Koeffizienten optimiert sind. Dieses Array muss die gleiche Größe wie die Anzahl der Stichproben in pDataIn haben. Wenn **NULL,** werden normale Oberflächenvektoren verwendet.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer-Ausgabeobjekt,**](id3dxprtbuffer.md) das zonale Order-Koeffizienten pro Farbkanal pro Stichprobe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Lösungen für die Schattierung normaler Vektoren können optional mit dieser Methode ermittelt werden. Diese normalen Vektoren können zusammen mit den LDPRT-Koeffizienten das PRT-Signal genauer darstellen. In diesem Fall stellen die Koeffizienten zonale Direktionen dar, die in normaler Richtung ausgerichtet sind.

Diese Methode kann nicht mit Ergebnissen von [**ID3DXPRTEngine::ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) oder [**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
