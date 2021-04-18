---
description: Füllt ein Array mit Rückruf Schlüsseldaten, die für die Keyframe-Animation verwendet werden.
ms.assetid: 0dc30c1f-9ffb-42ec-8074-84293f16c344
title: 'ID3DXCompressedAnimationSet:: getcallbackkeys-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fe56a3dbdd7d019deb5d7111fa592470bffd244d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365103"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a>ID3DXCompressedAnimationSet:: getcallbackkeys-Methode

Füllt ein Array mit Rückruf Schlüsseldaten, die für die Keyframe-Animation verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcallbackkeys* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXKEY- \_ Rückruf**](d3dxkey-callback.md)**

Zeiger auf ein vom Benutzer zugeordneter Array von [**D3DXKEY- \_ Rückruf**](d3dxkey-callback.md) Strukturen, die die Methode mit Rückruf Daten ausfüllen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet:: getnumcallbackkeys**](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




