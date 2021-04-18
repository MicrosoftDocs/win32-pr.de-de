---
description: Konvertiert eine Höhen Zuordnung in eine normale Karte. Die Komponenten (x, y, z) der einzelnen normalen werden den Kanälen (r, g, b) der Ausgabe Textur zugeordnet.
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: D3DX10ComputeNormalMap-Funktion (D3DX10Tex. h)
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
ms.openlocfilehash: 1d7318e6d00d921ba0d573eb6fb696eed6c6a58d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365319"
---
# <a name="d3dx10computenormalmap-function"></a>D3DX10ComputeNormalMap-Funktion

Konvertiert eine Höhen Zuordnung in eine normale Karte. Die Komponenten (x, y, z) der einzelnen normalen werden den Kanälen (r, g, b) der Ausgabe Textur zugeordnet.

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

*psrctexture* \[ in\]
</dt> <dd>

Typ: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Ein Zeiger auf eine ID3D10Texture2D-Schnittstelle, die die Textur der Quell Höhe darstellt.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein oder mehrere D3DX \_ normalmap-Flags, die die Generierung normaler Karten steuern.

</dd> <dt>

*Channel* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein D3DX- \_ kanalflag, das die Quelle der Höheninformationen angibt.

</dd> <dt>

*Amplitude* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Konstanter Wert Multiplikator, der die Werte in der normalen Zuordnung vergrößert (oder verringert). Höhere Werte machen in der Regel zu Leistungseinbußen, niedrigere Werte werden in der Regel weniger sichtbar.

</dd> <dt>

*pdesttexture* \[ in\]
</dt> <dd>

Typ: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Zeiger auf eine ID3D10Texture2D-Schnittstelle, die die Ziel Textur darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Wert sein: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Diese Methode berechnet die normale, indem der zentrale Unterschied mit einer Kernel Größe von 3X3 verwendet wird. RGB-Kanäle im Ziel enthalten unausgewogene (x, y, z) Komponenten der normalen. Der zentrale Differenzierungs Nenner ist hart codiert in 2,0.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
