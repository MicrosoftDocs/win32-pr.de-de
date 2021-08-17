---
description: Gibt die Zeitposition im lokalen Zeitrahmen eines Animationssets zurück.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: ID3DXAnimationSet::GetPeriodicPosition-Methode (D3dx9anim.h)
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
ms.openlocfilehash: 8451e3332b61d7e6e993de7df0832a78c0c45c0240633fd5f421998816f7f26f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122061"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a>ID3DXAnimationSet::GetPeriodicPosition-Methode

Gibt die Zeitposition im lokalen Zeitrahmen eines Animationssets zurück.

## <a name="syntax"></a>Syntax


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Position* \[ In\]
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Ortszeit des Animationssets.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Die Zeitposition, die im Zeitrahmen des Animationssets gemessen wird. Dieser Wert wird durch den Zeitraum des Animationssets gebunden.

## <a name="remarks"></a>Hinweise

Die von dieser Methode zurückgegebene Zeitposition kann als PeriodicPosition-Parameter von [**ID3DXAnimationSet::GetSRT verwendet werden.**](id3dxanimationset--getsrt.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
