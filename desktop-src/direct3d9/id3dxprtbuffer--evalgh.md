---
description: Wendet gespeicherte Textur-Gutterdaten auf einen ID3DXPRTBuffer-Texturpuffer an.
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: ID3DXPRTBuffer::EvalGH-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.EvalGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c01eee9659bc650c6e914f17932fd12dca703150d69908511c37b4d7e0a41cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493030"
---
# <a name="id3dxprtbufferevalgh-method"></a>ID3DXPRTBuffer::EvalGH-Methode

Wendet gespeicherte Textur-Gutterdaten auf einen [**ID3DXPRTBuffer-Texturpuffer**](id3dxprtbuffer.md) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode führt einen internen Aufruf von [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) aus, um Textur-Gutterdaten abzurufen und anzuwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




