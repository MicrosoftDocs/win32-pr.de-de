---
title: RWStructuredBuffer::IncrementCounter-Funktion (Httpserv.h)
description: Erhöht den ausgeblendeten Zähler des Objekts.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- IncrementCounter-Funktion HLSL
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39a857fc9a7a108cea05060caf86ce61479a382c5160f4f051c11423bc6a5d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095170"
---
# <a name="incrementcounter-function"></a>IncrementCounter-Funktion

Erhöht den ausgeblendeten Zähler des Objekts.

## <a name="syntax"></a>Syntax

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint**

Der vorab inkrementierte Indikatorwert.

## <a name="remarks"></a>Hinweise

Für die gebundene ungeordnete Zugriffsansicht muss [**D3D11 \_ BUFFER \_ UAV \_ FLAG \_ COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) während der Erstellung festgelegt sein, damit diese Methode funktioniert.

Eine strukturierte Ressource kann basierend auf den Komponentennamen der Strukturen weiter indiziert werden.

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Httpserv.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

