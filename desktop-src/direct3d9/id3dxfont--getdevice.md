---
description: Ruft das Direct3D-Gerät ab, das dem Schriftartobjekt zugeordnet ist.
ms.assetid: c713cbe2-6e6e-476b-a995-14fa149cb088
title: ID3DXFont::GetDevice-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e0f89594f77044db20bade062b245ccabe072a0ccae1fb5fa76f23bb18a8db0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121147"
---
# <a name="id3dxfontgetdevice-method"></a>ID3DXFont::GetDevice-Methode

Ruft das Direct3D-Gerät ab, das dem Schriftartobjekt zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDevice* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

Adresse eines Zeigers auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Direct3D-Geräteobjekt darstellt, das dem Schriftartobjekt zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Wenn Sie diese Methode aufrufen, erhöht sich der interne Verweiszähler für die [**IDirect3DDevice9-Schnittstelle.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) Rufen Sie [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) auf, wenn Sie mit der Verwendung dieser **IDirect3DDevice9-Schnittstelle** fertig sind oder ein Speicherverlust vorkommt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
