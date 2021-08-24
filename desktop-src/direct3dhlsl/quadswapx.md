---
title: QuadReadAcrossX-Funktion
description: Gibt den angegebenen lokalen Wert zurück, der von der anderen Spur in diesem Quad in X-Richtung gelesen wird.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- QuadReadAcrossX-Funktion HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86a2f525a79fa2458e4f7e0ef44379053e03128782d2625e1bdceb23ec518b16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672440"
---
# <a name="quadreadacrossx-function"></a>QuadReadAcrossX-Funktion

Gibt den angegebenen lokalen Wert zurück, der von der anderen Spur in diesem Quad in X-Richtung gelesen wird.

## <a name="syntax"></a>Syntax

``` syntax
<type> QuadReadAcrossX(
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

Der angegebene lokale Wert. Wenn die Quellspur inaktiv ist, sind die Ergebnisse nicht definiert.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Quads finden Sie unter [Übersicht über Shadermodell 6.](hlsl-shader-model-6-0-features-for-direct3d-12.md)

Diese Funktion wird von Shadermodell 6.0 nur in Pixel- und Compute-Shadern unterstützt.



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




