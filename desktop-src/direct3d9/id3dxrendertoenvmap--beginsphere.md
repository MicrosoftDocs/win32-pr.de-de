---
description: Initiieren Sie das Rendering einer sphärischen Umgebungszuordnung.
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: ID3DXRenderToEnvMap::BeginSphere-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f8bc555e3ea4f4fbb895c42f5c7a407cea88aedeacb9604ad1e78c7003bdf34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801290"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a>ID3DXRenderToEnvMap::BeginSphere-Methode

Initiieren Sie das Rendering einer sphärischen Umgebungszuordnung.

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTex* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf eine [**IDirect3DTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) die die Textur darstellt, in der gerendert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL. E \_ FAIL

## <a name="remarks"></a>Hinweise

Informationen zum Zeichnen des Gesichts finden Sie unter [**ID3DXRenderToEnvMap::Face.**](id3dxrendertoenvmap--face.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap::End**](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
