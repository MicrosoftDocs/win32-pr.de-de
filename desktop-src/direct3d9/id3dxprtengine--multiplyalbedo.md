---
description: Multipliziert jeden vorausbesetzten PRT-Vektor (Radiance Transfer) mit dem Pro-Vertex-Albedo.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: ID3DXPRTEngine::MultiplyAlbedo-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: c2989ce2a662be5a1ec53c961b8fafa072862fc2b43b6003b04f6b887ef3c077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790540"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a>ID3DXPRTEngine::MultiplyAlbedo-Methode

Multipliziert jeden vorausbesetzten PRT-Vektor (Radiance Transfer) mit dem Pro-Vertex-Albedo.

## <a name="syntax"></a>Syntax


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer-Ausgabeobjekt,**](id3dxprtbuffer.md) das PRT-Vektoren enthält, multipliziert mit dem Pro-Scheitelpunkt-Albedo. Wenn dieser Ausgabepuffer ein Texturobjekt ist, muss darauf achten, das Albedo der Textur mit der gleichen Auflösung wie der Simulationspuffer zu speichern. Sie können die richtige Auflösung für das Albedo mit [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)festlegen und dabei texturierte Bundstenregionen anwenden, falls zutreffend.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die ID3DXPRTEngine::Computexxx-Methoden berechnen Ausgabepuffer, in denen das Lichtsignal nicht mit albedo multipliziert wurde. Wenn Sie die Albedo nicht multiplizieren, können Sie Albedo-Variationen mit einer feineren Skala als die Quellbreite modellieren, wodurch genauere Ergebnisse der Komprimierung erzielt werden.

Um Albedo in das Modell mit gerenderten Licht zu verwenden, rufen Sie diese Methode nach einer der Computexxx-Methoden auf.

[**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) sollte aufgerufen werden, bevor diese Methode aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




