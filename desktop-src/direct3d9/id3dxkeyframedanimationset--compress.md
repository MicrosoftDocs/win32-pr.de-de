---
description: Wandelt Animationen in einem Animations Satz in ein komprimiertes Format um und gibt einen Zeiger auf den Puffer zurück, in dem die komprimierten Daten gespeichert werden.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'ID3DXKeyframedAnimationSet:: compress-Methode (D3dx9anim. h)'
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
ms.openlocfilehash: cd3a278760f2598df52d251a9e3558a72f954ceb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370469"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a>ID3DXKeyframedAnimationSet:: compress-Methode

Wandelt Animationen in einem Animations Satz in ein komprimiertes Format um und gibt einen Zeiger auf den Puffer zurück, in dem die komprimierten Daten gespeichert werden.

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

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Einer der [**D3DXCOMPRESSION \_ Flags**](./d3dxcompression-flags.md) -Werte, die den Komprimierungs Modus definieren, der zum Speichern komprimierter Animations Satz Daten verwendet wird. D3DXCOMPRESS \_ Default ist der einzige derzeit unterstützte Wert.

</dd> <dt>

*Verlust* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Das Verhältnis der gewünschten Komprimierungs Verluste liegt im Bereich von 0 bis 1.

</dd> <dt>

*phierarchie* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**

Zeiger auf eine [**D3DXFRAME**](d3dxframe.md) -Transformations Frame Hierarchie. Kann **null** sein.

</dd> <dt>

*ppcompresseddata* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf den komprimierten [**ID3DXBuffer**](id3dxbuffer.md) -Animations Satz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
