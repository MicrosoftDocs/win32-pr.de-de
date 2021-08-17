---
description: Transformiert Animationen in einem Animationssatz in ein komprimiertes Format und gibt einen Zeiger auf den Puffer zurück, in dem die komprimierten Daten gespeichert werden.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: ID3DXKeyframedAnimationSet::Compress-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d444ffde525677715f64bd9641cc8fb3cf9513e2c8805a6be28b280aaa12e015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802387"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a>ID3DXKeyframedAnimationSet::Compress-Methode

Transformiert Animationen in einem Animationssatz in ein komprimiertes Format und gibt einen Zeiger auf den Puffer zurück, in dem die komprimierten Daten gespeichert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Einer der [**D3DXCOMPRESSION \_ FLAGS-Werte,**](./d3dxcompression-flags.md) der den Komprimierungsmodus definiert, der zum Speichern komprimierter Animationssatzdaten verwendet wird. D3DXCOMPRESS \_ DEFAULT ist der einzige derzeit unterstützte Wert.

</dd> <dt>

*Verlust* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gewünschtes Komprimierungsverlustverhältnis im Bereich von 0 bis 1.

</dd> <dt>

*pHierarchy* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**

Zeiger auf eine [**D3DXFRAME-Transformationsrahmenhierarchie.**](d3dxframe.md) Kann **NULL** sein.

</dd> <dt>

*ppCompressedData* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf den komprimierten [**Animationssatz ID3DXBuffer.**](id3dxbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
