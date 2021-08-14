---
description: Ruft den Zeitraum des Animationssatzes ab.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: ID3DXAnimationSet::GetPeriod-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d8e984d1593fbbd79561bbb15fb27b62a9961c1830c42465ed529f08c374e180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522329"
---
# <a name="id3dxanimationsetgetperiod-method"></a>ID3DXAnimationSet::GetPeriod-Methode

Ruft den Zeitraum des Animationssatzes ab.

## <a name="syntax"></a>Syntax


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Zeitraum des Animationssatzes.

## <a name="remarks"></a>Hinweise

Der Zeitraum ist der Zeitraum, in dem die Animationsschlüsselrahmen gültig sind. Bei Schleifenanimationen ist dies der Zeitraum der Schleife. Die Zeiteinheiten, in denen die Keyframes angegeben werden (z. B. Sekunden), werden von der Anwendung bestimmt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
