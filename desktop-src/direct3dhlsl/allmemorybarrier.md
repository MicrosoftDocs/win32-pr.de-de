---
title: Allmemorybarrier-Funktion
description: Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Speicherzugriffe abgeschlossen sind.
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- Allmemorybarrier-Funktion HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3252389da64b74e07853069c71315b290a2ba6d5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389324"
---
# <a name="allmemorybarrier-function"></a>Allmemorybarrier-Funktion

Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Speicherzugriffe abgeschlossen sind.

## <a name="syntax"></a>Syntax

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine Arbeitsspeicher Barriere gewährleistet, dass ausstehende Speichervorgänge abgeschlossen wurden. Threads werden bei groupsync-Barrieren synchronisiert. Dies kann einen Thread oder Threads blockieren, wenn Arbeitsspeicher Vorgänge ausgeführt werden.

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




