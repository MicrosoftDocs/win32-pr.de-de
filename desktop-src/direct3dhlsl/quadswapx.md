---
title: Quad-acrossx-Funktion
description: Gibt den angegebenen lokalen Wert zurück, der von der anderen Strecke in diesem Quad in der X-Richtung gelesen wird.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- Quads-acrossx-Funktion (HLSL)
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd41b0bd84861d23153f02ba6328d17b70287866
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102554"
---
# <a name="quadreadacrossx-function"></a>Quad-acrossx-Funktion

Gibt den angegebenen lokalen Wert zurück, der von der anderen Strecke in diesem Quad in der X-Richtung gelesen wird.

## <a name="syntax"></a>Syntax

``` syntax
<type> QuadReadAcrossX(
   <type> localValue
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*localvalue* 
</dt> <dd>

Der angeforderte Typ.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der angegebene lokale Wert. Wenn der Quellpfad inaktiv ist, sind die Ergebnisse nicht definiert.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu den Quads finden Sie unter [Übersicht über Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Diese Funktion wird vom Shader-Modell 6,0 nur in Pixel-und Compute-Shadern unterstützt.



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




