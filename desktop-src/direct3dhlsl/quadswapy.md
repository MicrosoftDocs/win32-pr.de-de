---
title: QuadReadAcrossY-Funktion
description: Gibt den angegebenen Quellwert zurück, der von der anderen Fahrspur in diesem Quader in Y-Richtung gelesen wird.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- QuadReadAcrossY-Funktion HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f761a3588759e0c27143d16bd8fac5f674f05ae1819a0cdcebc55d6b4bdc6e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672400"
---
# <a name="quadreadacrossy-function"></a>QuadReadAcrossY-Funktion

Gibt den angegebenen Quellwert zurück, der von der anderen Fahrspur in diesem Quader in Y-Richtung gelesen wird.

## <a name="syntax"></a>Syntax

``` syntax
<type> QuadReadAcrossY(
   <type> localValue
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*localValue* 
</dt> <dd>

Der angeforderte Typ.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der angegebene Quellwert. Wenn die Quellspur inaktiv ist, sind die Ergebnisse nicht definiert.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Quads finden Sie unter [Übersicht über Shadermodell 6.](hlsl-shader-model-6-0-features-for-direct3d-12.md)

Diese Funktion wird vom Shadermodell 6.0 nur in Pixel- und Compute-Shadern unterstützt.



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




