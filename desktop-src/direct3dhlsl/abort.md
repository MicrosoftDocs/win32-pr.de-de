---
title: Abbruch-Funktion (corecrt \_ beenden. h)
description: Sendet eine Fehlermeldung an die Informations Warteschlange und beendet den aktuellen Draw-oder Dispatch-Befehl, der ausgeführt wird.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- Abbruch-Funktion HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982636"
---
# <a name="abort-function"></a>abort-Funktion

Sendet eine Fehlermeldung an die Informations Warteschlange und beendet den aktuellen Draw-oder Dispatch-Befehl, der ausgeführt wird.

## <a name="syntax"></a>Syntax

``` syntax
void abort(
    
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

 
</dt> <dd>

Keine

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Bei diesem Vorgang werden keine Rasterizer unterstützt, die dies nicht unterstützen.

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) oder höher.](dx-graphics-hlsl-sm3.md) | ja       |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Corecrt \_ beenden. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





