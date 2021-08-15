---
description: Ruft das Direct3D-Gerät ab, das der Renderoberfläche zugeordnet ist.
ms.assetid: 579cf7da-b8e0-4d9f-93b8-b1f47c3d5654
title: ID3DXRenderToSurface::GetDevice-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b7b8ea6887eb1b18b1e2eb28a811f05f10e9df4614ddb8dbc02371acc176c866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729604"
---
# <a name="id3dxrendertosurfacegetdevice-method"></a>ID3DXRenderToSurface::GetDevice-Methode

Ruft das Direct3D-Gerät ab, das der Renderoberfläche zugeordnet ist.

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

Adresse eines Zeigers auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Direct3D-Geräteobjekt darstellt, das der Renderoberfläche zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein. Durch aufrufen dieser Methode wird die interne Verweisanzahl für die [**IDirect3DDevice9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) erhöht. Rufen Sie [**IUnknown auf,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) wenn Sie diese **IDirect3DDevice9-Schnittstelle** nicht mehr verwenden, oder es kommt zu einem Arbeitsspeicherverlust.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 
