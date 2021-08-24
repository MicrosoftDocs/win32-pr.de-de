---
description: 'D3DX10ComputeNormalMap-Funktion: Konvertiert eine Höhenkarte in eine normale Karte. Die (x,y,z)-Komponenten jeder Normalen werden den (r,g,b)-Kanälen der Ausgabetextur zugeordnet.'
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
ms.openlocfilehash: b719e1b40c3e8cd04ca0750e69c68bbd4a0a59394c3334818f091900606311af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634780"
---
# <a name="d3dx10computenormalmap-function"></a>D3DX10ComputeNormalMap-Funktion

Konvertiert eine Höhenkarte in eine normale Karte. Die (x,y,z)-Komponenten jeder Normalen werden den (r,g,b)-Kanälen der Ausgabetextur zugeordnet.

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

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Mindestens ein D3DX \_ NORMALMAP-Flag, das die Generierung normaler Zuordnungen steuert.

</dd> <dt>

*Kanal* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein D3DX \_ CHANNEL-Flag, das die Quelle der Höheninformationen angibt.

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

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Wert sein: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Diese Methode berechnet die Normalität mithilfe des zentralen Unterschieds mit einer Kernelgröße von 3x3. RGB-Kanäle im Ziel enthalten voreingenommene (x,y,z)-Komponenten der Normalen. Der zentrale differenzierende Nenner ist hartcodiert auf 2.0.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texturfunktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
