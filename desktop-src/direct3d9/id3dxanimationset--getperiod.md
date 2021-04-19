---
description: Ruft den Zeitraum des Animations Satzes ab.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'ID3DXAnimationSet:: GetPeriod-Methode (D3dx9anim. h)'
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
ms.openlocfilehash: 5f6eafbfe802afc8ff3084c49acf31addca66cef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367494"
---
# <a name="id3dxanimationsetgetperiod-method"></a>ID3DXAnimationSet:: GetPeriod-Methode

Ruft den Zeitraum des Animations Satzes ab.

## <a name="syntax"></a>Syntax


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Zeitraum des Animations Satzes.

## <a name="remarks"></a>Bemerkungen

Der Zeitraum ist der Zeitraum, in dem die Animations Schlüsselframes gültig sind. Bei Schleifen Animationen ist dies der Zeitraum der Schleife. Die Zeiteinheiten, in denen die Keyframes angegeben werden (z. b. Sekunden), werden von der Anwendung bestimmt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
