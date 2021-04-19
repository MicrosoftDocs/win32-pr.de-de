---
description: Erstellt ein Animations Controller Objekt.
ms.assetid: 771e5966-ac1a-43c2-8e81-b6d573343ff0
title: D3DXCreateAnimationController-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateAnimationController
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a61b2c42a1eafa2ed28ac98c753588181a0ccf7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353717"
---
# <a name="d3dxcreateanimationcontroller-function"></a>D3DXCreateAnimationController-Funktion

Erstellt ein Animations Controller Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateAnimationController(
  _In_  UINT                      MaxNumAnimationOutputs,
  _In_  UINT                      MaxNumAnimationSets,
  _In_  UINT                      MaxNumTracks,
  _In_  UINT                      MaxNumEvents,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Maxnumanimationoutputs* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Maximale Anzahl von Animations Ausgaben, die der Controller unterstützen kann.

</dd> <dt>

*Maxnumanimationsets* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Maximale Anzahl der Animations Sätze, die gemischt werden können.

</dd> <dt>

*Maxnumtracks* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Maximale Anzahl von Animations Sätzen, die gleichzeitig gemischt werden können.

</dd> <dt>

*Maxnumevents* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Maximale Anzahl ausstehender Ereignisse, die vom Controller unterstützt werden.

</dd> <dt>

*ppanimcontroller* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Zeiger auf das erstellte Animations Controller Objekt. Siehe [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Ein Animations Controller steuert einen Animations-Mixer. Der Controller fügt Methoden hinzu, um Mischungs Parameter im Zeitverlauf zu ändern, um reibungslose Übergänge zu ermöglichen

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Animations Funktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
