---
description: Aktiviert oder deaktiviert alle D3DX-Debugausgabe.
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: D3DXDebugMute-Funktion (D3dx9core.h)
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
ms.openlocfilehash: c2bde5446e6e41568c1f9d6aa8408dacc276ab82112a176cf8a038536dd4d992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045078"
---
# <a name="d3dxdebugmute-function"></a>D3DXDebugMute-Funktion

Aktiviert oder deaktiviert alle D3DX-Debugausgabe.

## <a name="syntax"></a>Syntax


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Stummschalten* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

True **gibt an,** dass die Debuggerausgabe angehalten wird. false **gibt an,** dass die Debugausgabe aktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Gibt den vorherigen Wert von Mute zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
