---
description: Erstellt einen prt-Puffer (Precomputed Radiance Transfer), der von einem Simulator komprimiert oder gefüllt werden kann. Diese Funktion sollte verwendet werden, um Puffer pro Pixel zu erstellen.
ms.assetid: 41e65674-e5e1-4df9-aab8-1530ebf85f25
title: D3DXCreatePRTBufferTex-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBufferTex
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44bddffded189ce747491a4c3d9c08195c9817cfb1a578136f9c025231760cde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299265"
---
# <a name="d3dxcreateprtbuffertex-function"></a>D3DXCreatePRTBufferTex-Funktion

Erstellt einen prt-Puffer (Precomputed Radiance Transfer), der von einem Simulator komprimiert oder gefüllt werden kann. Diese Funktion sollte verwendet werden, um Puffer pro Pixel zu erstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreatePRTBufferTex(
  _In_    UINT            Width,
  _In_    UINT            Height,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Breite* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Breite der Textur in Pixel.

</dd> <dt>

*Höhe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Höhe der Textur in Pixel.

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

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

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

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> </dl>

 

 
