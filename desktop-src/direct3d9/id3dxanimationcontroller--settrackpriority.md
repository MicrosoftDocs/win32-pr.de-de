---
description: Legt die Prioritätsmischungsgewichtung für die angegebene Animationsspur fest.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: ID3DXAnimationController::SetTrackPriority-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: be294710fcd6ec2d8e72c7d7c9437623d29a2729a52144d4edfdc91e5be7eea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848970"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a>ID3DXAnimationController::SetTrackPriority-Methode

Legt die Prioritätsmischungsgewichtung für die angegebene Animationsspur fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Nachverfolgen* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Nachverfolgungsbezeichner.

</dd> <dt>

*Priorität* \[ In\]
</dt> <dd>

Typ: **[ **D3DXPRIORITY \_ TYPE**](./d3dxpriority-type.md)**

Nachverfolgungspriorität. Dieser Parameter sollte auf eine der Konstanten von [**D3DXPRIORITY \_ TYPE**](./d3dxpriority-type.md)festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
