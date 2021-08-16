---
title: AllMemoryBarrier-Funktion
description: Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Speicherzugriffe abgeschlossen sind.
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- AllMemoryBarrier-Funktion HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fc5d22c36d67aa0e8df8352ba8fa6f2d579ddabd4825e6508499420a56bd0ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626750"
---
# <a name="allmemorybarrier-function"></a>AllMemoryBarrier-Funktion

Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Speicherzugriffe abgeschlossen sind.

## <a name="syntax"></a>Syntax

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Eine Speicherbarriere garantiert, dass ausstehende Speichervorgänge abgeschlossen wurden. Threads werden über GroupSync-Barrieren synchronisiert. Dies kann einen Thread oder Threads blockieren, wenn Arbeitsspeichervorgänge ausgeführt werden.

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




