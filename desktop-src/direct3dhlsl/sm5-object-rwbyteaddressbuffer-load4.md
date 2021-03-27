---
title: 'Rwbyteaddressbuffer:: Load4 (uint)-Funktion'
description: 'Ruft vier Werte ab. | Rwbyteaddressbuffer:: Load4 (uint)-Funktion'
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
keywords:
- Load4-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2bdc5adf3b3d95c68871a14c9382891a59ad52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982048"
---
# <a name="rwbyteaddressbufferload4uint-function"></a>Rwbyteaddressbuffer:: Load4 (uint)-Funktion

Ruft vier Werte ab.

## <a name="syntax"></a>Syntax

``` syntax
uint4 Load4(
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

Typ: **uint4**

Vier Werte.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Load4-Methoden](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




