---
title: RWStructuredBuffer::Load(int)-Funktion
description: Liest Pufferdaten. | RWStructuredBuffer::Load(int)-Funktion
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
keywords:
- Load-Funktion HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cc8fbd0cfa18f2ac6c5d7109e8690d829bbde2175e8808865e68e29e63c955
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067756"
---
# <a name="rwstructuredbufferloadint-function"></a>RWStructuredBuffer::Load(int)-Funktion

Liest Pufferdaten.

## <a name="syntax"></a>Syntax


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Standort* \[ In\]
</dt> <dd>

Typ: **int**

Die Position des Puffers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ:

Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**RWStructuredBuffer-Objekt.**](sm5-object-rwstructuredbuffer.md)

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Laden von Methoden](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




