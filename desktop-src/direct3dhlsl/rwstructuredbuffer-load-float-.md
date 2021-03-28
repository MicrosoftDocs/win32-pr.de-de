---
title: 'Rwstructuredbuffer:: Load (int)-Funktion'
description: 'Liest Puffer Daten. | Rwstructuredbuffer:: Load (int)-Funktion'
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
keywords:
- Ladefunktion HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c20998faef8f5a018aaf95571be3c9d64730c436
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995366"
---
# <a name="rwstructuredbufferloadint-function"></a>Rwstructuredbuffer:: Load (int)-Funktion

Liest Puffer Daten.

## <a name="syntax"></a>Syntax


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Speicherort* \[ in\]
</dt> <dd>

Typ: **int**

Der Speicherort des Puffers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ:

Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**rwstructuredbuffer**](sm5-object-rwstructuredbuffer.md) -Objekt.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Lade Methoden](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




