---
description: Aktivieren oder deaktivieren Sie Debugmeldungen.
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: D3DX10DebugMute-Funktion (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DebugMute
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f4cd6a7ade60bc59cb1e6cbd9d3a447fac5cb7364db1ca85dcf704acedaa645c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128382"
---
# <a name="d3dx10debugmute-function"></a>D3DX10DebugMute-Funktion

Aktivieren oder deaktivieren Sie Debugmeldungen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Stummschalten* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Legen Sie diese Einstellung auf **TRUE** fest, um Debugmeldungen zu aktivieren. legen Sie auf **FALSE** fest, um Debugmeldungen zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Funktion, um Fehlermeldungen für D3DX10-APIs während des Debuggens zu deaktivieren. Die Verwendung dieser Funktion sollte durch den D3D10 \_ DEBUG-Compilerschalter geschützt werden.


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



Der Standardzustand ist **TRUE** für einen Debugbuild.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
