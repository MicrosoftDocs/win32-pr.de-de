---
description: Erstellt ein Sprite-Objekt, das einem bestimmten Gerät zugeordnet ist. Sprite-Objekte werden verwendet, um 2D-Bilder auf den Bildschirm zu zeichnen.
ms.assetid: 1611073f-0590-415a-8ea5-dc1d224f20b9
title: D3DXCreateSprite-Funktion (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSprite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8fe6d4897a581302f27544217c3caf5b6c723ce2ff4aed611b40a21cd7b0d35f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027740"
---
# <a name="d3dxcreatesprite-function"></a>D3DXCreateSprite-Funktion

Erstellt ein Sprite-Objekt, das einem bestimmten Gerät zugeordnet ist. Sprite-Objekte werden verwendet, um 2D-Bilder auf den Bildschirm zu zeichnen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateSprite(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXSPRITE      *ppSprite
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das Gerät, das dem Sprite zugeordnet werden soll.

</dd> <dt>

*ppSprite* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXSPRITE**](id3dxsprite.md)\***

Adresse eines Zeigers auf eine [**ID3DXSprite-Schnittstelle.**](id3dxsprite.md) Diese Schnittstelle ermöglicht dem Benutzer den Zugriff auf Sprite-Funktionen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Schnittstelle kann verwendet werden, um zweidimensionale Bilder im Bildschirmbereich des zugeordneten Geräts zu zeichnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
