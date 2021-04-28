---
description: 'ID3DXCompressedAnimationSet::GetCallbackKeys-Methode: Füllt ein Array mit Rückrufschlüsseldaten aus, die für die Keyframe-Animation verwendet werden.'
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
ms.openlocfilehash: d7c430358b5ba7f66c5a79b08ae01925141e659f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115328"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a>ID3DXCompressedAnimationSet::GetCallbackKeys-Methode

Füllt ein Array mit Rückrufschlüsseldaten aus, die für die Keyframe-Animation verwendet werden.

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

Zeiger auf ein vom Benutzer zugeordnetes Array von [**D3DXKEY \_ CALLBACK-Strukturen,**](d3dxkey-callback.md) das die Methode mit Rückrufdaten füllen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet::GetNumCallbackKeys**](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




