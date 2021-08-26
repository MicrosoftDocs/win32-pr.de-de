---
title: QuadReadAcrossDiagonal-Funktion
description: Gibt den angegebenen lokalen Wert zurück, der von der diagonal gegenüberliegenden Fahrspur in diesem Quader gelesen wird.
ms.assetid: 2914F1F9-5CE2-437A-ADDB-4955D2C1490B
keywords:
- QuadReadAcrossDiagonal-Funktion HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossDiagonal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53066864ec87528406b20d5503f4e47497cb3aa80e44f01e279845fdc2674339
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981930"
---
# <a name="quadreadacrossdiagonal-function"></a>QuadReadAcrossDiagonal-Funktion

Gibt den angegebenen lokalen Wert zurück, der von der diagonal gegenüberliegenden Fahrspur in diesem Quader gelesen wird.

## <a name="syntax"></a>Syntax


``` syntax
<type> QuadReadAcrossDiagonal(
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

Der angegebene lokale Wert, der von der diagonal gegenüberliegenden Kurve in diesem Quader gelesen wird.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Quads finden Sie unter [Übersicht über Shadermodell 6.](hlsl-shader-model-6-0-features-for-direct3d-12.md)

Diese Funktion wird vom Shadermodell 6.0 nur in Pixel- und Compute-Shadern unterstützt.



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




