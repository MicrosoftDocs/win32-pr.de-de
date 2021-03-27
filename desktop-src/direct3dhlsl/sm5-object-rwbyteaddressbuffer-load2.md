---
title: 'Rwbyteaddressbuffer:: Load2 (uint)-Funktion'
description: 'Ruft zwei Werte ab. | Rwbyteaddressbuffer:: Load2 (uint)-Funktion'
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
keywords:
- Load2-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7595477448deb087b94664100710690a6f386a94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982029"
---
# <a name="rwbyteaddressbufferload2uint-function"></a>Rwbyteaddressbuffer:: Load2 (uint)-Funktion

Ruft zwei Werte ab.

## <a name="syntax"></a>Syntax

``` syntax
uint2 Load2(
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

Typ: **uint2**

Zwei-Werte.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Load2-Methoden](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




