---
description: Verknüpft ein ID3DXTextureGutterHelper-Objekt mit dem ID3DXPRTBuffer-Objekt.
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: 'ID3DXPRTBuffer:: attachgh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba5afa238107d60620291b50b8f184eb4e5d361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353744"
---
# <a name="id3dxprtbufferattachgh-method"></a>ID3DXPRTBuffer:: attachgh-Methode

Verknüpft ein [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekt mit dem [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pgh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

Ein Zeiger auf die [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Schnittstelle eines Objekts, das Textur Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Bemerkungen

Der Verweis Zähler des [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekts wird automatisch um 1 erhöht. Vorhandene **ID3DXTextureGutterHelper** -Zeiger werden freigegeben.

Sie müssen sicherstellen, dass die Anzahl von **ID3DXPRTBuffer:: attachgh** -aufrufen mit der Anzahl von [**ID3DXPRTBuffer:: releasegh**](id3dxprtbuffer--releasegh.md) -aufrufen übereinstimmt. Nach dem Aufruf von **ID3DXPRTBuffer:: releasegh** sollte der von **ID3DXPRTBuffer:: attachgh** zurückgegebene pgh-Zeiger nicht mehr verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer:: releasegh**](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 




