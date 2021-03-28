---
title: Quadread acrossy-Funktion
description: Gibt den angegebenen Quellwert zurück, der von der anderen Strecke in diesem Quad in der Y-Richtung gelesen wird.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- Quada-Funktion (HLSL)
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72b5ede0df733e60ba4b1bcc01a04f1daaedc708
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104976880"
---
# <a name="quadreadacrossy-function"></a>Quadread acrossy-Funktion

Gibt den angegebenen Quellwert zurück, der von der anderen Strecke in diesem Quad in der Y-Richtung gelesen wird.

## <a name="syntax"></a>Syntax

``` syntax
<type> QuadReadAcrossY(
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

Der angegebene Quellwert. Wenn der Quellpfad inaktiv ist, sind die Ergebnisse nicht definiert.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu den Quads finden Sie unter [Übersicht über Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Diese Funktion wird vom Shader-Modell 6,0 nur in Pixel-und Compute-Shadern unterstützt.



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




