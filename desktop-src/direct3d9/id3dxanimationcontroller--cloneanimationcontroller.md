---
description: Klont oder kopiert einen Animationscontroller.
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: ID3DXAnimationController::CloneAnimationController-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5afb99126967163318c82bac6b8cac655fec65e8a28e4cdb349c7f2b1c679435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522781"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a>ID3DXAnimationController::CloneAnimationController-Methode

Klont oder kopiert einen Animationscontroller.

## <a name="syntax"></a>Syntax


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MaxNumAnimationOutputs* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Maximale Anzahl von Animationsausgabe, die der Controller unterstützen kann.

</dd> <dt>

*MaxNumAnimationSets* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Maximale Anzahl von Animationssätzen, die der Controller unterstützen kann.

</dd> <dt>

*MaxNumTracks* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Maximale Anzahl von Spuren, die der Controller unterstützen kann.

</dd> <dt>

*MaxNumEvents* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Maximale Anzahl von Ereignissen, die der Controller unterstützen kann.

</dd> <dt>

*ppAnimController* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Adresse eines Zeigers auf den geklonten [**ID3DXAnimationController-Animationscontroller.**](id3dxanimationcontroller.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
