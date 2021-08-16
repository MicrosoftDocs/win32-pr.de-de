---
description: Legt die Spurgeschwindigkeit fest. Die Spurgeschwindigkeit ähnelt einem Multiplikator, der verwendet wird, um die Wiedergabe der Spur zu beschleunigen oder zu verlangsamen.
ms.assetid: b3946b61-0676-4690-9844-639fabd8fd7c
title: ID3DXAnimationController::SetTrackSpeed-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 62cd882dd95446c92dd4192528322ed54708496183a3557aa89d53bc5dac138b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522359"
---
# <a name="id3dxanimationcontrollersettrackspeed-method"></a>ID3DXAnimationController::SetTrackSpeed-Methode

Legt die Spurgeschwindigkeit fest. Die Spurgeschwindigkeit ähnelt einem Multiplikator, der verwendet wird, um die Wiedergabe der Spur zu beschleunigen oder zu verlangsamen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTrackSpeed(
  [in] UINT  Track,
  [in] FLOAT Speed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Nachverfolgen* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Bezeichner der Spur, für die die Geschwindigkeit festgelegt werden soll.

</dd> <dt>

*Geschwindigkeit* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Neue Geschwindigkeit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
