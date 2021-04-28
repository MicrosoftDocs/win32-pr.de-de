---
description: 'D3DX10ComputeNormalMap-Funktion: Konvertiert eine Höhenkarte in eine normale Karte. Die (x,y,z)-Komponenten jeder Normalen werden den (r,g,b) Kanälen der Ausgabetextur zugeordnet.'
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: D3DX10ComputeNormalMap-Funktion (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 173a8e0c1b3130a399152187eb52288a0306051c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105318"
---
# <a name="d3dx10computenormalmap-function"></a>D3DX10ComputeNormalMap-Funktion

Konvertiert eine Höhenkarte in eine normale Karte. Die (x,y,z)-Komponenten jeder Normalen werden den (r,g,b) Kanälen der Ausgabetextur zugeordnet.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcTexture* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Zeiger auf eine ID3D10Texture2D-Schnittstelle, die die Quelltextur der Höhenzuordnung darstellt.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Mindestens ein D3DX \_ NORMALMAP-Flag, das die Generierung normaler Zuordnungen steuert.

</dd> <dt>

*Kanal* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein \_ D3DX-KANALflag, das die Quelle der Höheninformationen angibt.

</dd> <dt>

*Amplitude* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Konstanter Wertmultiplikator, der die Werte in der normalen Zuordnung erhöht (oder verringert). Höhere Werte machen Bumps in der Regel sichtbarer, niedrigere Werte machen Bumps in der Regel weniger sichtbar.

</dd> <dt>

*pDestTexture* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Zeiger auf eine ID3D10Texture2D-Schnittstelle, die die Zieltextur darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert folgender Wert sein: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Bemerkungen

Diese Methode berechnet den Normalwert, indem der zentrale Unterschied mit einer Kernelgröße von 3 x 3 verwendet wird. RGB-Kanäle im Ziel enthalten verzerrte (x,y,z)-Komponenten des Normals. Der zentrale Unterscheidende Nenner ist auf 2,0 hartcodiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
