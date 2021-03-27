---
title: Rwstructuredbuffer::D ecrementcounter-Funktion (httpserv. h)
description: Dekremente den ausgeblendeten Wert des Objekts.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- Decrementcounter-Funktion HLSL
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
ms.openlocfilehash: a56641054bb4e9ed4b1865d00c662b0de2afa1a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982389"
---
# <a name="decrementcounter-function"></a>Decrementcounter-Funktion

Dekremente den ausgeblendeten Wert des Objekts.

## <a name="syntax"></a>Syntax

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint**

Der Wert des postdekrementierten Leistungs Zählers.

## <a name="remarks"></a>Bemerkungen

Für die gebundene Ansicht für ungeordnete Zugriffe muss ein [**D3D11 \_ buffer \_ UAV- \_ Flag \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) -Wert festgelegt sein, der während der Ausführung für diese Methode festgelegt wird.

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

 

