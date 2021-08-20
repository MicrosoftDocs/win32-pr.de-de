---
title: RWTexture1D::GetDimensions-Funktion
description: Gibt die Dimensionen der Ressource zurück. | RWTexture1D::GetDimensions-Funktion
ms.assetid: 1bbd53ed-9396-4e8e-b2f3-3bd85f6e1a90
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
ms.openlocfilehash: eb779d071f471abe92b18ef456a2a016536a5231ccf327f8ebd175be8e5ff224
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509292"
---
# <a name="rwtexture1dgetdimensions-function"></a>RWTexture1D::GetDimensions-Funktion

Gibt die Dimensionen der Ressource zurück.

## <a name="syntax"></a>Syntax

``` syntax
void GetDimensions(
  out UINT Width
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Breite* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Ressourcenbreite in Texel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nichts

## <a name="remarks"></a>Hinweise

Dies ist eine Liste der überladenen Versionen dieser Methode.


```
void GetDimensions (out UINT Width);

void GetDimensions(out float Width);
```



Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[RWTexture1D](sm5-object-rwtexture1d.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
