---
description: Initiieren des Renderings einer kugelförmigen Umgebungs Zuordnung.
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: 'ID3DXRenderToEnvMap:: beginsphere-Methode (D3dx9core. h)'
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
ms.openlocfilehash: 872aa06734ae818ef248b03fbc14dcd1c33fe815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354567"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a>ID3DXRenderToEnvMap:: beginsphere-Methode

Initiieren des Renderings einer kugelförmigen Umgebungs Zuordnung.

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptex* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die die Textur darstellt, in die gerbt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall. E \_ fehlschlagen

## <a name="remarks"></a>Bemerkungen

Siehe [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) , um das Gesicht zu zeichnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap:: End**](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
