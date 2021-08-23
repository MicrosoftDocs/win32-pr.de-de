---
title: RWStructuredBuffer::D ecrementCounter-Funktion (Httpserv.h)
description: Dekrement wird der ausgeblendete Zähler des Objekts.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- DecrementCounter-Funktion HLSL
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8302f31cd07b81f4f78abe6a0a1fbcb2e6a1028f6153da69e55e0fb34977b585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671390"
---
# <a name="decrementcounter-function"></a>DecrementCounter-Funktion

Dekrement wird der ausgeblendete Zähler des Objekts.

## <a name="syntax"></a>Syntax

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint**

Der nachdekrementierte Indikatorwert.

## <a name="remarks"></a>Hinweise

Für die gebundene ungeordnete Zugriffsansicht muss [**D3D11 \_ BUFFER \_ UAV \_ FLAG \_ COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) während der Erstellung festgelegt sein, damit diese Methode funktioniert.

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Httpserv.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

