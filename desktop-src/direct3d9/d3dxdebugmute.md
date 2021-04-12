---
description: Schaltet alle D3DX-Debugausgaben ein bzw. aus.
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: D3DXDebugMute-Funktion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDebugMute
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9259fa43a6a64829e42cbaa661aa7223a958f22d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219519"
---
# <a name="d3dxdebugmute-function"></a>D3DXDebugMute-Funktion

Schaltet alle D3DX-Debugausgaben ein bzw. aus.

## <a name="syntax"></a>Syntax


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Stumm schalten* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

**True** gibt an, dass die Debugger-Ausgabe angehalten wird. **false** gibt an, dass die Debugausgabe aktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Gibt den vorherigen Wert von "stumm" zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
