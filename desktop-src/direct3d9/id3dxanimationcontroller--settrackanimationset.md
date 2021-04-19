---
description: Wendet den Animations Satz auf den angegebenen Titel an.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'ID3DXAnimationController:: settrackanimationset-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dce979e48ed118dc257c147b27615f7bbc89231
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361234"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a>ID3DXAnimationController:: settrackanimationset-Methode

Wendet den Animations Satz auf den angegebenen Titel an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Nach *verfolgen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Bezeichner des Titels, auf den der Animations Satz angewendet wird.

</dd> <dt>

*panimset* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Zeiger auf den [**ID3DXAnimationSet**](id3dxanimationset.md) -Animations Satz, der der Spur hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Diese Methode legt den Animations Satz auf den angegebenen Titel für die Mischung fest. Der Animations Satz für jede Spur wird entsprechend der Last und Geschwindigkeit des Titels gemischt, wenn [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
