---
title: 'Byteaddressbuffer:: Load4 (uint)-Funktion'
description: 'Ruft vier Werte ab. | Byteaddressbuffer:: Load4 (uint)-Funktion'
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
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
ms.openlocfilehash: 18ce27e7d02a414165aab169e40a6ab14cdd8c4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981928"
---
# <a name="byteaddressbufferload4uint-function"></a>Byteaddressbuffer:: Load4 (uint)-Funktion

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
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Load4-Methoden](byteaddressbuffer-load4.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




