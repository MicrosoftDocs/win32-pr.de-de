---
title: Waveactiveallequal-Funktion
description: Gibt true zurück, wenn der Ausdruck für jede aktive Strecke in der aktuellen Wave identisch ist (und somit einheitlich ist).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- Waveactiveallequal-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34745e428fcd4453ce7274fc2a5accc6185f5b10
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734800"
---
# <a name="waveactiveallequal-function"></a>Waveactiveallequal-Funktion

Gibt true zurück, wenn der Ausdruck für jede aktive Strecke in der aktuellen Wave identisch ist (und somit einheitlich ist).

## <a name="syntax"></a>Syntax


``` syntax
bool WaveActiveAllEqual(
   <type> expr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*expr* 
</dt> <dd>

Der auszuwertende Ausdruck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

True, wenn der Ausdruck für jede aktive Strecke in der aktuellen Wave gleich ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




