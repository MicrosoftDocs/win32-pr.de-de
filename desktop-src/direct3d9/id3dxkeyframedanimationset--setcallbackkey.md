---
description: Legt Informationen zu einem bestimmten Rückruf im Animations Satz fest.
ms.assetid: 899f3a85-c878-4eeb-8bda-fc4e9083bd1f
title: 'ID3DXKeyframedAnimationSet:: setcallbackkey-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49d3373e0ab0fa221e707ca6eda9ac9bb468a5a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219679"
---
# <a name="id3dxkeyframedanimationsetsetcallbackkey-method"></a>ID3DXKeyframedAnimationSet:: setcallbackkey-Methode

Legt Informationen zu einem bestimmten Rückruf im Animations Satz fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Animation* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Animations Index.

</dd> <dt>

*pcallbackkeys* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXKEY- \_ Rückruf**](d3dxkey-callback.md)**

Zeiger auf die [**Rückruffunktion**](d3dxkey-callback.md).

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
</dt> </dl>

 

 
