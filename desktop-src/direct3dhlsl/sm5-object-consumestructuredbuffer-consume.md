---
title: ConsumeStructuredBuffer::Consume-Funktion
description: Entfernt einen Wert vom Ende des Puffers.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Nutzen der HLSL-Funktion
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a76f8c27ed50c7d7eab1b37cd5c60257691b8db5e5af412f5b3bfe678c283bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486700"
---
# <a name="consume-function"></a>Consume-Funktion

Entfernt einen Wert vom Ende des Puffers.

## <a name="syntax"></a>Syntax

``` syntax
T Consume(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **T**

Der entfernte Wert (kann eine -Struktur sein).

## <a name="remarks"></a>Hinweise

T kann ein beliebiger Datentyp sein, einschließlich einer -Struktur.

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




