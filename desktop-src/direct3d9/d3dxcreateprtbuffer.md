---
description: Erstellt einen prt-Puffer (Precomputed Radiance Transfer), der von einem Simulator komprimiert oder gefüllt werden kann. Diese Funktion sollte zum Erstellen von Pro-Scheitelpunkt- oder Volumepuffern verwendet werden.
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: D3DXCreatePRTBuffer-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ff7293fd866bed8ef5bea46fd783b27672c4c53ee61786f75146ea45efd8a509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299275"
---
# <a name="d3dxcreateprtbuffer-function"></a>D3DXCreatePRTBuffer-Funktion

Erstellt einen prt-Puffer (Precomputed Radiance Transfer), der von einem Simulator komprimiert oder gefüllt werden kann. Diese Funktion sollte zum Erstellen von Pro-Scheitelpunkt- oder Volumepuffern verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreatePRTBuffer(
  _In_    UINT            NumSamples,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NumSamples* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Scheitelpunkte (oder Texel), die als Stichprobe entnommen wurden.

</dd> <dt>

*NumCoeffs* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Koeffizienten pro Stichprobenspeicherort. Bei Verwendung von SH-PRT (Spherical Splyting) sollte die Anzahl der Koeffizienten Orderevaluation sein, wobei Order die Reihenfolge der SH-Auswertung ist. Die Reihenfolge muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Der Grad der Auswertung ist "Order - 1".

</dd> <dt>

*NumChannels* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Farbkanäle, die im Gitternetz festgelegt werden sollen. Legen Sie auf 1 fest, um graue Materialien anzugeben (R = G = B) oder 3, um Farbunterdärkungseffekte zu ermöglichen.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***

Adresse eines Zeigers auf das erstellte [**ID3DXPRTBuffer-Objekt.**](id3dxprtbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Wenn der Puffer erstellt wird, werden alle Werte mit 0 (null) initialisiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorausberechnen von Übertragungsfunktionen für Die Radiance](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
