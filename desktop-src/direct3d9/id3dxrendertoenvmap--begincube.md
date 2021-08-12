---
description: Initiieren Sie das Rendering einer kubischen Umgebungskarte.
ms.assetid: 0f02b2e2-8132-4994-ab07-c79a1b7821dd
title: ID3DXRenderToEnvMap::BeginCube-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginCube
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 081e96425a7928cb1cd4a5a3ee48479d562c5c30a2f9017665acd32ffb539244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293274"
---
# <a name="id3dxrendertoenvmapbegincube-method"></a>ID3DXRenderToEnvMap::BeginCube-Methode

Initiieren Sie das Rendering einer kubischen Umgebungskarte.

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginCube(
  [in] LPDIRECT3DCUBETEXTURE9 pCubeTex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCubeTex* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Zeiger auf eine [**IDirect3DCubeTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) die die Cubetextur darstellt, in der gerendert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Informationen zum Zeichnen der sechs Gesichter finden Sie unter [**ID3DXRenderToEnvMap::Face.**](id3dxrendertoenvmap--face.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap::End**](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
