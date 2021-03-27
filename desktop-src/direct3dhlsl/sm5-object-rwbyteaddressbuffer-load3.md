---
title: 'Rwbyteaddressbuffer:: Load3 (uint)-Funktion'
description: 'Ruft drei Werte ab. | Rwbyteaddressbuffer:: Load3 (uint)-Funktion'
ms.assetid: cf8c4c5d-4748-43d7-896e-33ed07c94b9e
keywords:
- Load3-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6658b4929f09aa7296a284de1fdbf39c7c4f038
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982059"
---
# <a name="rwbyteaddressbufferload3uint-function"></a>Rwbyteaddressbuffer:: Load3 (uint)-Funktion

Ruft drei Werte ab.

## <a name="syntax"></a>Syntax

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Adresse* \[ in\]
</dt> <dd>

Typ: **uint**

Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint3**

Drei Werte.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Load3-Methoden](rwbyteaddressbuffer-load3.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




