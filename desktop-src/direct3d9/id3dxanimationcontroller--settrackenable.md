---
description: Aktiviert oder deaktiviert eine Spur im Animationscontroller.
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: ID3DXAnimationController::SetTrackEnable-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61078a40e13ee1422c29de091e1758444e2bafa1586bb443e763e50d57457ad5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026580"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a>ID3DXAnimationController::SetTrackEnable-Methode

Aktiviert oder deaktiviert eine Spur im Animationscontroller.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Nachverfolgen* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Bezeichner der zu mischenden Spur.

</dd> <dt>

*Aktivieren* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Wert aktivieren. Legen Sie auf **TRUE** fest, um diese Spur im Controller zu aktivieren, oder auf **FALSE,** um zu verhindern, dass sie gemischt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Um eine Spur mit anderen Spuren zu kombinieren, muss das Enable-Flag auf **TRUE** festgelegt werden. Umgekehrt verhindert das Festlegen des Flags auf **FALSE,** dass die Spur mit anderen Spuren gemischt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
