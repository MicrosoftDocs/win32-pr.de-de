---
title: DST-Funktion
description: Berechnet einen Entfernungs Vektor. | DST-Funktion
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- DST-Funktion HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58ce243cf9a9f3e6118763368445e5bcf26ba4cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869724"
---
# <a name="dst-function"></a>DST-Funktion

Berechnet einen Entfernungs Vektor.

## <a name="syntax"></a>Syntax

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*src0* \[ in\]
</dt> <dd>

Type: " **[atvector](dx-graphics-hlsl-vector.md) "**

Der erste Vektor.

</dd> <dt>

*Quelle1* \[ in\]
</dt> <dd>

Type: " **[atvector](dx-graphics-hlsl-vector.md) "**

Der zweite Vektor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: " **[atvector](dx-graphics-hlsl-vector.md) "**

Der berechnete Entfernungs Vektor.

## <a name="remarks"></a>Bemerkungen

Diese intrinsische Funktion bietet die gleiche Funktionalität wie die Vertex-Shader-Anweisung [DST](dst---vs.md).

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




