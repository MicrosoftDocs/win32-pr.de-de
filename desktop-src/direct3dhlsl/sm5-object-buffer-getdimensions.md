---
title: 'Buffer:: GetDimensions-Funktion'
description: 'Ruft die Länge des Puffers ab. | Buffer:: GetDimensions-Funktion'
ms.assetid: 704890e8-43e4-4e72-b7e2-eeef331bef1c
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
ms.openlocfilehash: c7f1ad1da7600e65d7442c1b2431535e2fdcf38c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981089"
---
# <a name="buffergetdimensions-function"></a>Buffer:: GetDimensions-Funktion

Ruft die Länge des Puffers ab.

## <a name="syntax"></a>Syntax

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

 \[ Abblenden\]
</dt> <dd>

Typ: **uint**

Die Länge des Puffers in Bytes.

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

[Buffer](sm5-object-buffer.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




