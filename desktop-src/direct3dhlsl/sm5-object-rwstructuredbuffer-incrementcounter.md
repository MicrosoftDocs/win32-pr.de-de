---
title: 'Rwstructuredbuffer:: incrementcounter-Funktion (httpserv. h)'
description: Erhöht den ausgeblendeten Wert des Objekts.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- Incrementcounter-Funktion HLSL
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
ms.openlocfilehash: c0002f82873de1c56ce5a7d79c9adb13bdf7ebc0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355496"
---
# <a name="incrementcounter-function"></a>Incrementcounter-Funktion

Erhöht den ausgeblendeten Wert des Objekts.

## <a name="syntax"></a>Syntax

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint**

Der Wert des vorab inkrementierten Zählers.

## <a name="remarks"></a>Bemerkungen

Für die gebundene Ansicht für ungeordnete Zugriffe muss bei der Erstellung der [**D3D11 \_ buffer \_ UAV- \_ Flag \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) -Wert festgelegt sein, damit diese Methode funktioniert.

Eine strukturierte Ressource kann basierend auf den Komponentennamen der Strukturen weiter indiziert werden.

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Httpserv. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Rwstructuredbuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

