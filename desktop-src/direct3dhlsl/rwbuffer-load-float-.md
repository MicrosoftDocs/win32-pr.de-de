---
title: RWBuffer::Load(int)-Funktion
description: Liest Pufferdaten. | RWBuffer::Load(int)-Funktion
ms.assetid: 3066E244-DE56-4F0D-8443-018B9EFEC1FF
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
ms.openlocfilehash: d3e3f9c9714cb4cc7f0f29bfa801e767b468d526836a7bd09f0f9823d9ff8868
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118300"
---
# <a name="rwbufferloadint-function"></a>RWBuffer::Load(int)-Funktion

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

Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**RWBuffer-Objekt.**](sm5-object-rwbuffer.md)

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Laden von Methoden](rwbuffer-load.md)
</dt> </dl>

 

 




