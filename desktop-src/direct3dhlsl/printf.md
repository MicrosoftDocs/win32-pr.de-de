---
title: printf-Funktion
description: Übermittelt eine benutzerdefinierte shadernachricht an die Informations Warteschlange.
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
ms.openlocfilehash: 74492cc613e22f335eace684300f0380e5751a95
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948254"
---
# <a name="printf-function"></a>printf-Funktion

Übermittelt eine benutzerdefinierte shadernachricht an die Informations Warteschlange.

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

 

 




