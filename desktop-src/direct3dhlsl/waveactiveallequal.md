---
title: WaveActiveAllEqual-Funktion
description: Gibt TRUE zurück, wenn der Ausdruck für jede aktive Spur in der aktuellen Welle identisch ist (und somit einheitlich darüber ist).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- WaveActiveAllEqual-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f62493a1bf08b85e95acad319bac2d022c30a53d43c28a87d0f5f603e78d300f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786110"
---
# <a name="waveactiveallequal-function"></a>WaveActiveAllEqual-Funktion

Gibt TRUE zurück, wenn der Ausdruck für jede aktive Spur in der aktuellen Welle identisch ist (und somit einheitlich darüber ist).

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

TRUE, wenn der Ausdruck für jede aktive Spur in der aktuellen Welle identisch ist.

## <a name="remarks"></a>Hinweise

Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




