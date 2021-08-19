---
title: RWTexture3D::GetDimensions-Funktion
description: Gibt die Dimensionen der Ressource zurück. | RWTexture3D::GetDimensions-Funktion
ms.assetid: ba70b955-1e80-4f27-84f1-fc9d26a1f1ab
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
ms.openlocfilehash: 2fcd1f5e5fb1ab87193c2946e68a8144f34a7275c9ad90e87e9cc7e960336e14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509208"
---
# <a name="rwtexture3dgetdimensions-function"></a>RWTexture3D::GetDimensions-Funktion

Gibt die Dimensionen der Ressource zurück.

## <a name="syntax"></a>Syntax

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Depth
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Breite* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Ressourcenbreite in Texel.

</dd> <dt>

*Höhe* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Ressourcenhöhe in Texel.

</dd> <dt>

*Tiefe* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Ressourcentiefe in Texel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dies ist eine Liste der überladenen Versionen dieser Methode.


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[RWTexture3D](sm5-object-rwtexture3d.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
