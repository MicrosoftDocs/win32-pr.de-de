---
description: Wendet gespeicherte Textur Daten auf einen ID3DXPRTBuffer-Textur Puffer an.
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: 'ID3DXPRTBuffer:: evalgh-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 23896ff2514db7b5e12b164ea0c0a763b5d1d3b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373549"
---
# <a name="id3dxprtbufferevalgh-method"></a>ID3DXPRTBuffer:: evalgh-Methode

Wendet gespeicherte Textur Daten auf einen [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Textur Puffer an.

## <a name="syntax"></a>Syntax


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode führt einen internen Aufrufen von [**ID3DXTextureGutterHelper:: applyguttersfloat**](id3dxtexturegutterhelper--applyguttersfloat.md) aus, um Textur bunddaten abzurufen und anzuwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




