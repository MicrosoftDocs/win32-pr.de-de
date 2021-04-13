---
description: Legt Mischungs Ereignis Schlüssel für den angegebenen Animations Titel fest.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'ID3DXAnimationController:: keypriorityblend-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31778da9b26ddd79b5f05c69c822ed62a5b5281e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354257"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a>ID3DXAnimationController:: keypriorityblend-Methode

Legt Mischungs Ereignis Schlüssel für den angegebenen Animations Titel fest.

## <a name="syntax"></a>Syntax


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Newblendweight* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die Zahl zwischen 0 und 1, die zum Kombinieren von Spuren verwendet wird.

</dd> <dt>

*StartTime* \[ in\]
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Die globale Zeit zum Starten von Blend.

</dd> <dt>

*Dauer* \[ in\]
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Die globale Zeitspanne der Mischung.

</dd> <dt>

*Übergang* \[ in\]
</dt> <dd>

Type: **[ **D3DXTRANSITION- \_ Typ**](./d3dxtransition-type.md)**

Gibt den für die Dauer der Blend verwendeten umgangstyp an. Siehe [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignis Handle für das Priority Blend-Ereignis. **Null** wird zurückgegeben, wenn mindestens ein Eingabeparameter ungültig ist oder kein freies Ereignis verfügbar ist.

## <a name="remarks"></a>Bemerkungen

Der Animations Controller wird in drei Phasen gemischt: Titel mit niedriger Priorität werden zuerst gemischt, Titel mit hoher Priorität werden als zweites gemischt angezeigt, und dann werden die Ergebnisse beider Komponenten gemischt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**Setpriorityblend**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
