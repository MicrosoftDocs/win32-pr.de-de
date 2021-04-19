---
description: Legt einen Ereignis Schlüssel fest, der die Geschwindigkeit eines Animations Titels ändert.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: 'ID3DXAnimationController:: keytrackspeed-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 09705dd03e7767e94b1508cf4951186a509a3c5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355238"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a>ID3DXAnimationController:: keytrackspeed-Methode

Legt einen Ereignis Schlüssel fest, der die Geschwindigkeit eines Animations Titels ändert.

## <a name="syntax"></a>Syntax


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
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

*Neugeschwindigkeit* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Neue Geschwindigkeit des Animations Titels.

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

Gibt den für den Übergang zwischen Geschwindigkeiten verwendeten transitionstyp an. Siehe [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignis Handle für das Priority Blend-Ereignis. **Null** wird zurückgegeben, wenn mindestens ein Eingabeparameter ungültig ist oder kein freies Ereignis verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
