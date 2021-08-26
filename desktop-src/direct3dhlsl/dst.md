---
title: dst-Funktion
description: Berechnet einen Entfernungsvektor. | dst-Funktion
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- dst-Funktion HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b0d8112902486102e6a4338445a2526b23cab8dafb2ea8b7d68b87d5b803af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068340"
---
# <a name="dst-function"></a>dst-Funktion

Berechnet einen Entfernungsvektor.

## <a name="syntax"></a>Syntax

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*src0* \[ In\]
</dt> <dd>

Typ: **[fVector](dx-graphics-hlsl-vector.md)**

Der erste Vektor.

</dd> <dt>

*src1* \[ In\]
</dt> <dd>

Typ: **[fVector](dx-graphics-hlsl-vector.md)**

Der zweite Vektor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[fVector](dx-graphics-hlsl-vector.md)**

Der berechnete Entfernungsvektor.

## <a name="remarks"></a>Hinweise

Diese systeminterne Funktion bietet die gleiche Funktionalität wie die Vertex-Shaderanweisung [dst](dst---vs.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




