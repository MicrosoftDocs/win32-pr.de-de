---
title: Quadleserlaneat-Funktion
description: Gibt den angegebenen Quellwert aus der durch die Lane-ID im aktuellen Quad identifizierten Spur zurück.
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- Quada-Funktion (HLSL)
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddc772c2dca66873891483431eab14ad504da77e
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474644"
---
# <a name="quadreadlaneat-function"></a>Quadleserlaneat-Funktion

Gibt den angegebenen Quellwert aus der durch die Lane-ID im aktuellen Quad identifizierten Spur zurück.

## <a name="syntax"></a>Syntax


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Quellwert* 
</dt> <dd>

Der angeforderte Typ.

</dd> <dt>

*quadlaneid* 
</dt> <dd>

Die Lane-ID; Dabei handelt es sich um einen Wert zwischen 0 und 3.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der angegebene Quellwert. Das Ergebnis dieser Funktion ist für das Vierfache einheitlich. Wenn der Quellpfad inaktiv ist, sind die Ergebnisse nicht definiert.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu den Quads finden Sie unter [Übersicht über Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Diese Funktion wird vom Shader-Modell 6,0 nur in Pixel-und Compute-Shadern unterstützt.



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




