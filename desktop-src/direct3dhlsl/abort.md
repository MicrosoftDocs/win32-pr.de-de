---
title: abort-Funktion (Corecrt \_ terminate.h)
description: Übermittelt eine Fehlermeldung an die Informationswarteschlange und beendet den aktuellen Draw- oder Dispatch-Aufruf, der ausgeführt wird.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- abort-Funktion HLSL
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
ms.openlocfilehash: 4a708d2893a19369d2db42f4551e3fafa4a1ff7a4680bf8676de32f79764289b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795524"
---
# <a name="abort-function"></a>abort-Funktion

Übermittelt eine Fehlermeldung an die Informationswarteschlange und beendet den aktuellen Draw- oder Dispatch-Aufruf, der ausgeführt wird.

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

## <a name="remarks"></a>Hinweise

Dieser Vorgang führt keine Aktion für Rasterizer aus, die sie nicht unterstützen.

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [ShaderModell 4 (DirectX HLSL) oder höher.](dx-graphics-hlsl-sm3.md) | Ja       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Corecrt \_ terminate.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





