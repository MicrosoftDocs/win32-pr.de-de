---
title: "\"errorf\"-Funktion"
description: Sendet eine Fehlermeldung an die Informations Warteschlange.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- "\"errorf\"-Funktion HLSL"
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76c8fbcd9b6cb15dbbb735296a3aada8f5e568cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037850"
---
# <a name="errorf-function"></a>"errorf"-Funktion

Sendet eine Fehlermeldung an die Informations Warteschlange.

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

## <a name="remarks"></a>Bemerkungen

Bei Geräten, die den Vorgang nicht unterstützen, wird dieser Vorgang nicht unterstützt.

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) oder höher.](dx-graphics-hlsl-sm3.md) | ja       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




