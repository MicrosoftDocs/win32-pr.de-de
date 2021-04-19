---
description: Multipliziert jeden PRT-Vektor (preberechneten Radiance Transfer) mit dem pro-Vertex-Albedo.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'ID3DXPRTEngine:: multiplyalbedo-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a282605789644382f39fd8fff9ce8bb47d6dfc7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350726"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a>ID3DXPRTEngine:: multiplyalbedo-Methode

Multipliziert jeden PRT-Vektor (preberechneten Radiance Transfer) mit dem pro-Vertex-Albedo.

## <a name="syntax"></a>Syntax


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdataout* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das PRT-Vektoren enthält, multipliziert mit der pro-Vertex-Albedo. Wenn dieser Ausgabepuffer ein Textur Objekt ist, muss darauf geachtet werden, dass die Albedo-Struktur der Textur mit derselben Auflösung wie der Simulations Puffer gespeichert wird. Sie können die richtige Auflösung für Albedo mit [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)festlegen und ggf. Textur bundbereiche anwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Die ID3DXPRTEngine:: computexxx-Methoden berechnen Ausgabepuffer, in denen das Lichtsignal nicht mit Albedo multipliziert wurde. Indem Sie Albedo nicht multiplizieren, können Sie Albedo-Variation in einer präziseren Skalierung als die Quell Strahlung modellieren und dadurch genauere Ergebnisse aus der Komprimierung erzielen.

Um Albedo im gerenderten lichtmodell einzuschließen, müssen Sie diese Methode nach einer der computexxx-Methoden aufrufen.

[**ID3DXPRTEngine:: settmeschmaterials**](id3dxprtengine--setmeshmaterials.md) sollte vor dem Aufruf dieser Methode aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: computedirectlightingsh**](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




