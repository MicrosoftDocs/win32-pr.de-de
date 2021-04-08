---
description: Wendet die-Guster auf ein ID3DXPRTBuffer-Puffer Objekt an.
ms.assetid: db09aa50-3175-4588-8433-dad6bd37cf0c
title: 'ID3DXTextureGutterHelper:: applyguttersprt-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersPRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5a99d0cb5d54207d292398468e16b6c35deb4562
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762120"
---
# <a name="id3dxtexturegutterhelperapplyguttersprt-method"></a>ID3DXTextureGutterHelper:: applyguttersprt-Methode

Wendet die-Guster auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Puffer Objekt an.

## <a name="syntax"></a>Syntax


```C++
HRESULT ApplyGuttersPRT(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbuffer* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Puffer Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall

## <a name="remarks"></a>Bemerkungen

[**Class 2 texeln**](id3dxtexturegutterhelper.md) werden durch das erneute Sampling von Class 1 und 4 texeln generiert.

Breite und Höhe der Textur müssen mit den von [**ID3DXTextureGutterHelper:: getWidth**](id3dxtexturegutterhelper--getwidth.md) und [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md)zurückgegebenen Zeichen identisch sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




