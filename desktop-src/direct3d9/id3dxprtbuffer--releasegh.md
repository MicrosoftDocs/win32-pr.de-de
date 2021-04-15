---
description: Hebt die Zuordnung eines angefügten ID3DXTextureGutterHelper-Objekts zum ID3DXPRTBuffer-Objekt auf.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'ID3DXPRTBuffer:: releasegh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9fb7a68f11d21065d6b4911b9ee7f58920aeb25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394258"
---
# <a name="id3dxprtbufferreleasegh-method"></a>ID3DXPRTBuffer:: releasegh-Methode

Hebt die Zuordnung eines angefügten [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekts zum [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt den Zeiger auf die [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Schnittstelle frei.

Sie müssen sicherstellen, dass die Anzahl von [**ID3DXPRTBuffer:: attachgh**](id3dxprtbuffer--attachgh.md) -aufrufen mit der Anzahl von **ID3DXPRTBuffer:: releasegh** -aufrufen übereinstimmt. Nach dem Aufruf von **ID3DXPRTBuffer:: releasegh** sollte der von **ID3DXPRTBuffer:: attachgh** zurückgegebene pgh-Zeiger nicht mehr verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer:: attachgh**](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 




