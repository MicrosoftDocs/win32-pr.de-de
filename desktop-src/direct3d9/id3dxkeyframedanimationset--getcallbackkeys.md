---
description: Füllt ein Array mit Rückruf Schlüsseldaten, die für die Keyframe-Animation verwendet werden.
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: 'ID3DXKeyframedAnimationSet:: getcallbackkeys-Methode (D3dx9anim. h)'
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
ms.openlocfilehash: d3f8dbc771fcdde6d1c07a1bf810b322b0a70a30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219457"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a>ID3DXKeyframedAnimationSet:: getcallbackkeys-Methode

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

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet:: getnumcallbackkeys**](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




