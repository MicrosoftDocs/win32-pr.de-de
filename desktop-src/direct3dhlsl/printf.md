---
title: printf-Funktion
description: Sendet eine benutzerdefinierte Shadernachricht an die Informationswarteschlange.
ms.assetid: 0c6c15fc-1da5-4a26-ade0-5a0489e4f564
keywords:
- printf-Funktion HLSL
topic_type:
- apiref
api_name:
- printf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47131cacef436572f519b394a02b4aaa357a426dd80a192868712cb3d7779e24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672520"
---
# <a name="printf-function"></a>printf-Funktion

Sendet eine benutzerdefinierte Shadernachricht an die Informationswarteschlange.

## <a name="syntax"></a>Syntax

``` syntax
void printf(
   string format,
    argument ...
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*format* 
</dt> <dd>

Die Formatzeichenfolge.

</dd> <dt>

*Argument...* 
</dt> <dd>

Optionale Argumente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieser Vorgang wird auf Geräten, die ihn nicht unterstützen, nicht durchgeführt.

### <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shadermodell 4 (DirectX HLSL) oder höher.](dx-graphics-hlsl-sm3.md) | Ja       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




