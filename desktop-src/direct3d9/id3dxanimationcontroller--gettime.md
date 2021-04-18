---
description: Ruft die globale Animations Zeit ab.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: 'ID3DXAnimationController:: getTime-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bfc3c2c1d5bb0bbbb3c364b47f22f0790f8d102
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355030"
---
# <a name="id3dxanimationcontrollergettime-method"></a>ID3DXAnimationController:: getTime-Methode

Ruft die globale Animations Zeit ab.

## <a name="syntax"></a>Syntax


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Gibt die globale Animations Zeit zurück.

## <a name="remarks"></a>Bemerkungen

Animationen werden mithilfe einer lokalen Animations Zeit entwickelt und in der globalen Zeit mit [**AdvanceTime**](id3dxanimationcontroller--advancetime.md)gemischt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
