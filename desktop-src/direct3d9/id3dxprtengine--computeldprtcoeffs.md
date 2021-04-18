---
description: Berechnet lokal Aufzähl Bare (ldprt-) Koeffizienten (ldprt)-Koeffizienten in Relation zu pro-Sample-normal Vektoren, um den Fehler der geringsten Quadrate in Bezug auf Eingabe ID3DXPRTBuffer Daten zu minimieren.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'ID3DXPRTEngine:: computeldprtcoeffs-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 351ecb8022e06b1a5a24abad8fa8541798d13ba0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365869"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a>ID3DXPRTEngine:: computeldprtcoeffs-Methode

Berechnet lokal Aufzähl Bare (ldprt-) Koeffizienten (ldprt)-Koeffizienten in Relation zu pro-Sample-normal Vektoren, um den Fehler der geringsten Quadrate in Bezug auf Eingabe [**ID3DXPRTBuffer**](id3dxprtbuffer.md) Daten zu minimieren. Diese Koeffizienten können mit häufenden oder transformierten normalen Vektoren verwendet werden, um globale Effekte auf dynamische Objekte zu modellieren.

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

*pdatain* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf das PRT-Datenobjekt (input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) Kugel harmonisch (SH) (SH).

</dd> <dt>

*Reihenfolge* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Reihenfolge der SH-Evaluierung. Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen. Die Auswertung generiert die Koeffizienten der Bestellung. Der Bewertungs Grad ist Order-1.

</dd> <dt>

*pnormout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Optionales Vektor Array, das mit shaderoptimalen normalen Vektoren gefüllt werden soll, für die ldprt-Koeffizienten optimiert werden. Dieses Array muss dieselbe Größe wie die Anzahl der Samplings in pdatain aufweisen. Wenn der Wert **null** ist, werden Oberflächen normale Vektoren verwendet.

</dd> <dt>

*pdataout* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das die Reihenfolge der harmonischen Koeffizient pro Farbkanal pro Beispiel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Lösungen für Schattierungs normale Vektoren können mit dieser Methode optional abgerufen werden. Diese normalen Vektoren können zusammen mit den ldprt-Koeffizienten das PRT-Signal genauer darstellen. In diesem Fall stellen die Koeffizienten zonale Oberschwingungen dar, die in normaler Richtung ausgerichtet sind.

Diese Methode kann nicht mit Ergebnissen aus [**ID3DXPRTEngine:: computesurf samplesbounce**](id3dxprtengine--computesurfsamplesbounce.md) oder [**ID3DXPRTEngine:: computesurf samplesdirectsh**](id3dxprtengine--computesurfsamplesdirectsh.md)verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
