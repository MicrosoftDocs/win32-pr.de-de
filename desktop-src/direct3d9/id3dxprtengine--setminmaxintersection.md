---
description: Legt den minimalen und maximalen Abstand der Schnittmenge zwischen 3D-Objekten fest.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: ID3DXPRTEngine::SetMinMaxIntersection-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2182714588e5d408c6928a677433e68dac44f09abf5ec6bd4cb4d6df7e4acf02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629060"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a>ID3DXPRTEngine::SetMinMaxIntersection-Methode

Legt den minimalen und maximalen Abstand der Schnittmenge zwischen 3D-Objekten fest. Diese Entfernungswerte können verwendet werden, um den minimalen oder maximalen Abstand zu steuern, den Objekte überschatten oder lichtreflektionen können. Beispielsweise kann die -Methode verwendet werden, um das Schatten von Features in der Nähe eines 3D-Modells einzuschränken.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fMin* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Minimaler Schnittmengenabstand. Muss positiv und kleiner als fMax sein.

</dd> <dt>

*fMax* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Maximaler Schnittmengenabstand. Bei 0,0f wird der vorherige Wert verwendet. andernfalls muss größer als fMin sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Methode kann nicht in prt-Simulationen (Precomputed Radiance Transfer) verwendet werden, die in der GPU ausgeführt werden. Siehe [**ID3DXPRTEngine::ComputeDirectLightingSWSPU**](id3dxprtengine--computedirectlightingshgpu.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
