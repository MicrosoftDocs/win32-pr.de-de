---
description: 'ID3DXCompressedAnimationSet::GetCallbackKeys-Methode: Füllt ein Array mit Rückrufschlüsseldaten auf, die für die Keyframeanimation verwendet werden.'
ms.assetid: 0dc30c1f-9ffb-42ec-8074-84293f16c344
title: ID3DXCompressedAnimationSet::GetCallbackKeys-Methode (D3dx9anim.h)
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
ms.openlocfilehash: a4889f0292cf9e97b74db5c1d35f2bc8242acdadb608db2404bda5dcff1a62b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296143"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a>ID3DXCompressedAnimationSet::GetCallbackKeys-Methode

Füllt ein Array mit Rückrufschlüsseldaten, die für die Keyframeanimation verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCallbackKeys* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXKEY \_ CALLBACK**](d3dxkey-callback.md)**

Zeiger auf ein vom Benutzer zugewiesenes Array von [**D3DXKEY \_ CALLBACK-Strukturen,**](d3dxkey-callback.md) die von der -Methode mit Rückrufdaten auffüllt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet::GetNumCallbackKeys**](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




