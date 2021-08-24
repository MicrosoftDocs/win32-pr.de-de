---
description: Legt einen Ereignisschlüssel fest, der die Ortszeit einer Animationsspur ändert.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: ID3DXAnimationController::KeyTrackPosition-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9e66bac7b5aaa8da87b0cb88e3bfd12469d8aa8b6ec755eaa47268c70da5eadf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791230"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a>ID3DXAnimationController::KeyTrackPosition-Methode

Legt einen Ereignisschlüssel fest, der die Ortszeit einer Animationsspur ändert.

## <a name="syntax"></a>Syntax


```C++
D3DXEVENTHANDLE KeyTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE NewPosition,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Nachverfolgen* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Bezeichner der zu ändernden Spur.

</dd> <dt>

*NewPosition* \[ In\]
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Neue Ortszeit der Animationsspur.

</dd> <dt>

*StartTime* \[ In\]
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Globaler Zeitschlüssel. Gibt die globale Zeit an, zu der die Änderung erfolgt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignishandle für das Prioritätsmischungsereignis. **NULL** wird zurückgegeben, wenn Track ungültig ist oder wenn kein kostenloses Ereignis verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
