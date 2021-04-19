---
description: Legt die vom Animations Controller verwendete Prioritäts Mischungs Gewichtung fest.
ms.assetid: b053024b-f219-48b3-906e-161d9cf47556
title: 'ID3DXAnimationController:: setpriorityblend-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4c820858041c730f971ce2821698f86e6ff2c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366675"
---
# <a name="id3dxanimationcontrollersetpriorityblend-method"></a>ID3DXAnimationController:: setpriorityblend-Methode

Legt die vom Animations Controller verwendete Prioritäts Mischungs Gewichtung fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPriorityBlend(
  [in] FLOAT BlendWeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Blendweight* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Das vom Animations Controller verwendete Gewicht für die Prioritäts Mischung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Die Blend-Gewichtung wird verwendet, um nachverfolgen mit hoher und niedriger Priorität zu kombinieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**Getpriorityblend**](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
