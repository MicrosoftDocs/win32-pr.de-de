---
description: Ruft das Direct3D-Gerät ab, das der Umgebungszuordnung zugeordnet ist.
ms.assetid: 15f342c5-7665-443a-b7b8-32cc67034c41
title: ID3DXRenderToEnvMap::GetDevice-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d7534efefdba4622fdab559d2e8210b05e21cc6fb1169bc44934a9189099ba2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293123"
---
# <a name="id3dxrendertoenvmapgetdevice-method"></a>ID3DXRenderToEnvMap::GetDevice-Methode

Ruft das Direct3D-Gerät ab, das der Umgebungszuordnung zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDevice* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

Adresse eines Zeigers auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Direct3D-Geräteobjekt darstellt, das der Umgebungszuordnung zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein. Durch aufrufen dieser Methode wird die interne Verweisanzahl für die [**IDirect3DDevice9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) erhöht. Rufen Sie [**IUnknown auf,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) wenn Sie diese **IDirect3DDevice9-Schnittstelle** nicht mehr verwenden, oder es kommt zu einem Arbeitsspeicherverlust.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
