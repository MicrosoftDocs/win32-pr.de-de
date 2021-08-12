---
description: Fügt dem Animationscontroller einen Animationssatz hinzu.
ms.assetid: 93351d61-b7f4-4bd1-a5bf-313911cf6b61
title: ID3DXAnimationController::RegisterAnimationSet-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c6572b4a09967f2a911ffb3b147f3786aae75d71650d4d77d0564c1dbefc5f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296980"
---
# <a name="id3dxanimationcontrollerregisteranimationset-method"></a>ID3DXAnimationController::RegisterAnimationSet-Methode

Fügt dem Animationscontroller einen Animationssatz hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAnimSet* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Zeiger auf die hinzuzufügende [**ID3DXAnimationSet-Animation.**](id3dxanimationset.md)

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

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




