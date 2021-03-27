---
title: 'RWTexture1D:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | RWTexture1D:: GetDimensions-Funktion'
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
ms.openlocfilehash: b65f0113ecf2c91786e45c35f5e8e832744bc952
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981080"
---
# <a name="rwtexture1dgetdimensions-function"></a>RWTexture1D:: GetDimensions-Funktion

Gibt die Dimensionen der Ressource zurück.

## <a name="syntax"></a>Syntax

``` syntax
void GetDimensions(
  out UINT Width
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Breite* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Ressourcen Breite in Texels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nichts

## <a name="remarks"></a>Bemerkungen

Dies ist eine Liste der überladenen Versionen dieser Methode.


```
void GetDimensions (out UINT Width);

void GetDimensions(out float Width);
```



Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[RWTexture1D](sm5-object-rwtexture1d.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
