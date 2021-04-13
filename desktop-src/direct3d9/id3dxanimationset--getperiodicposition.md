---
description: Gibt die Uhrzeit Position im lokalen Zeitrahmen eines Animations Satzes zurück.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'ID3DXAnimationSet:: GetPeriodicPosition-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3c4f2e8e57efdfe0681b8ae691e0b5de42624e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355936"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a>ID3DXAnimationSet:: GetPeriodicPosition-Methode

Gibt die Uhrzeit Position im lokalen Zeitrahmen eines Animations Satzes zurück.

## <a name="syntax"></a>Syntax


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Position* \[ in\]
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Lokale Zeit des Animations Satzes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Die Zeit Position, gemessen im Zeitrahmen des Animations Satzes. Dieser Wert wird durch den Zeitraum des Animations Satzes begrenzt.

## <a name="remarks"></a>Bemerkungen

Die von dieser Methode zurückgegebene Zeit Position kann als PeriodicPosition-Parameter von [**ID3DXAnimationSet:: gezrt**](id3dxanimationset--getsrt.md)verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
