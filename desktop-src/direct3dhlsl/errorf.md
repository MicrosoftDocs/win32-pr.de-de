---
title: errorf-Funktion
description: Übermittelt eine Fehlermeldung an die Informationswarteschlange.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- errorf-Funktion HLSL
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0651a27419a369721806e9aa4717a20088f8f5fbbaa0063628d2feb69648c7cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562680"
---
# <a name="errorf-function"></a>errorf-Funktion

Übermittelt eine Fehlermeldung an die Informationswarteschlange.

## <a name="syntax"></a>Syntax

``` syntax
void errorf(
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

Dieser Vorgang führt auf Geräten, die ihn nicht unterstützen, keine Aktion aus.

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [ShaderModell 4 (DirectX HLSL) oder höher.](dx-graphics-hlsl-sm3.md) | Ja       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




