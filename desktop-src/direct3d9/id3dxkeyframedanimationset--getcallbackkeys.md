---
description: 'ID3DXKeyframedAnimationSet::GetCallbackKeys-Methode: Füllt ein Array mit Rückrufschlüsseldaten auf, die für die Keyframeanimation verwendet werden.'
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: ID3DXKeyframedAnimationSet::GetCallbackKeys-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f3bdb7049de3b5d6aad10b5ff5100d01d05e3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093718"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a>ID3DXKeyframedAnimationSet::GetCallbackKeys-Methode

Füllt ein Array mit Rückrufschlüsseldaten, die für die Keyframe-Animation verwendet werden.

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

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




