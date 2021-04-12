---
description: Legt einen Ereignis Schlüssel fest, mit dem die Ortszeit eines Animations Titels geändert wird.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: 'ID3DXAnimationController:: keytrackposition-Methode (D3dx9anim. h)'
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
ms.openlocfilehash: d027069efa9fb49cad3d2344da593eae4c3c844c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355507"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a>ID3DXAnimationController:: keytrackposition-Methode

Legt einen Ereignis Schlüssel fest, mit dem die Ortszeit eines Animations Titels geändert wird.

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

Nach *verfolgen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Bezeichner des zu ändernden Titels.

</dd> <dt>

*Neuposition* \[ in\]
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Neue lokale Zeit des Animations Titels.

</dd> <dt>

*StartTime* \[ in\]
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Globaler Zeit Schlüssel. Gibt die globale Zeit an, zu der die Änderung stattfindet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignis Handle für das Priority Blend-Ereignis. **Null** wird zurückgegeben, wenn Track ungültig ist, oder, wenn kein freies Ereignis verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
