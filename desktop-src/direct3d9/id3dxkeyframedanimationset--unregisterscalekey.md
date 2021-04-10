---
description: Entfernt die Skalierungs Daten am angegebenen Keyframe.
ms.assetid: b0bf5665-ccfb-4b87-8e88-9a717ef57955
title: 'ID3DXKeyframedAnimationSet:: unregisterscalekey-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d1ac3f500b80d8922646fddff9f05d8c91d9c48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961742"
---
# <a name="id3dxkeyframedanimationsetunregisterscalekey-method"></a>ID3DXKeyframedAnimationSet:: unregisterscalekey-Methode

Entfernt die Skalierungs Daten am angegebenen Keyframe.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnregisterScaleKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Animation* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Animations Bezeichner.

</dd> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Keyframe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist langsam und sollte nicht verwendet werden, nachdem die Wiedergabe einer Animation begonnen hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
