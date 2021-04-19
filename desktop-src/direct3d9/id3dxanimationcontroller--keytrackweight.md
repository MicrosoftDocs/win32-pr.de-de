---
description: Legt einen Ereignis Schlüssel fest, mit dem die Gewichtung eines Animations Titels geändert wird. Die Gewichtung wird als Multiplikator verwendet, wenn mehrere Titel zusammen kombiniert werden.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: 'ID3DXAnimationController:: keytrackweight-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74f5e38392f6b4ac192f02b9d85421c8357a16ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363169"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a>ID3DXAnimationController:: keytrackweight-Methode

Legt einen Ereignis Schlüssel fest, mit dem die Gewichtung eines Animations Titels geändert wird. Die Gewichtung wird als Multiplikator verwendet, wenn mehrere Titel zusammen kombiniert werden.

## <a name="syntax"></a>Syntax


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Nach *verfolgen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Bezeichner des zu ändernden Titels.

</dd> <dt>

*Newweight* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Neue Gewichtung des Titels.

</dd> <dt>

*StartTime* \[ in\]
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Globaler Zeit Schlüssel. Gibt die globale Zeit an, zu der die Änderung stattfindet.

</dd> <dt>

*Dauer* \[ in\]
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Übergangszeit, die angibt, wie lange der reibungslose Übergang dauert.

</dd> <dt>

*Übergang* \[ in\]
</dt> <dd>

Type: **[ **D3DXTRANSITION- \_ Typ**](./d3dxtransition-type.md)**

Gibt den für den Übergang zwischen Gewichtungen verwendeten transitionstyp an. Siehe [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignis Handle für das Priority Blend-Ereignis. **Null** wird zurückgegeben, wenn mindestens ein Eingabeparameter ungültig ist oder kein freies Ereignis verfügbar ist.

## <a name="remarks"></a>Bemerkungen

Die Gewichtung wird wie ein Multiplikator verwendet, um zu bestimmen, wie viel von dieser Spur mit anderen Spuren verknüpft werden muss.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
