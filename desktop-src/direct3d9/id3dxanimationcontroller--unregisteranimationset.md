---
description: Entfernt einen Animationssatz aus dem Animationscontroller.
ms.assetid: 2ca99651-8249-44c2-9560-b3cfaa930862
title: ID3DXAnimationController::UnregisterAnimationSet-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnregisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b2065ee9928291812b614b42137e130a7986402b25234537fc9b84fafa6f714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522349"
---
# <a name="id3dxanimationcontrollerunregisteranimationset-method"></a>ID3DXAnimationController::UnregisterAnimationSet-Methode

Entfernt einen Animationssatz aus dem Animationscontroller.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnregisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAnimSet* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Zeiger auf die zu entfernende [**ID3DXAnimationSet-Animation.**](id3dxanimationset.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DERR \_ NOTFOUND.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




