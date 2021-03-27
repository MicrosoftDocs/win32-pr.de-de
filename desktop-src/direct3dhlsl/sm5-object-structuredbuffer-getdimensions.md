---
title: 'Structuredbuffer:: GetDimensions-Funktion'
description: 'Ruft die Ressourcen Dimensionen ab. | Structuredbuffer:: GetDimensions-Funktion'
ms.assetid: 423ea79c-4440-4837-b637-95180a1d5019
keywords:
- GetDimensions-Funktion HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b3d7c879c77386ddee80a63053711b8ae34ee8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352959"
---
# <a name="structuredbuffergetdimensions-function"></a>Structuredbuffer:: GetDimensions-Funktion

Ruft die Ressourcen Dimensionen ab.

## <a name="syntax"></a>Syntax

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*numstructs* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Die Anzahl der Strukturen in der Ressource.

</dd> <dt>

*Stride* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Der Schritt (in Byte) der einzelnen Strukturelemente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Structuredbuffer](sm5-object-structuredbuffer.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




