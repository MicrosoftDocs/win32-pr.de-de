---
description: 'ID3DXKeyframedAnimationSet::GetCallbackKey-Methode: Ruft Informationen zu einem bestimmten Rückruf im Animationssatz ab.'
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: ID3DXKeyframedAnimationSet::GetCallbackKey-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5036ca9e00da3231677fe41e179bb9c27d1a4bbbd145f3e15bc6e4160902e9b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295170"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a>ID3DXKeyframedAnimationSet::GetCallbackKey-Methode

Ruft Informationen zu einem bestimmten Rückruf im Animationssatz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Animation* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Animationsindex.

</dd> <dt>

*pCallbackKeys* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXKEY \_ CALLBACK**](d3dxkey-callback.md)**

Zeiger auf die [**Rückruffunktion**](d3dxkey-callback.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
