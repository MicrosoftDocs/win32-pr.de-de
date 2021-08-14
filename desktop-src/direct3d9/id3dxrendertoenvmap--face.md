---
description: Initiieren sie das Zeichnen der einzelnen Gesichtserkennungen einer Umgebungskarte.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: ID3DXRenderToEnvMap::Face-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1190e033f9aa83b13f327fcb8a8b530be17132bfd330c9be6b9cc6d87d5e35a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801219"
---
# <a name="id3dxrendertoenvmapface-method"></a>ID3DXRenderToEnvMap::Face-Methode

Initiieren sie das Zeichnen der einzelnen Gesichtserkennungen einer Umgebungskarte.

## <a name="syntax"></a>Syntax


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gesicht* \[ In\]
</dt> <dd>

Typ: **[ **D3DCUBEMAP \_ FACES**](./d3dcubemap-faces.md)**

Das erste Gesicht der Umgebungscubekarte. Siehe [**D3DCUBEMAP \_ FACES**](./d3dcubemap-faces.md).

</dd> <dt>

*MipFilter* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine gültige Kombination aus mindestens einem [D3DX \_ FILTER-Flag.](d3dx-filter.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Diese Methode muss einmal für jeden Typ von Umgebungszuordnung aufgerufen werden. Die einzige Ausnahme ist eine kubische Umgebungskarte, die erfordert, dass diese Methode sechsmal aufgerufen wird, einmal für jedes Gesicht in D3DCUBEMAP \_ FACES. Weitere Informationen finden Sie unter [Umgebungszuordnung (Direct3D 9).](environment-mapping.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
