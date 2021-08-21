---
title: RWTexture1DArray::GetDimensions-Funktion
description: Gibt die Dimensionen der Ressource zurück. | RWTexture1DArray::GetDimensions-Funktion
ms.assetid: 64f2757e-c03c-4f72-b081-1c57656d6e95
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
ms.openlocfilehash: 7a522fe31a62619134e86b2ed98da54570d693d1360ede1a8c0d41d28975b367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986020"
---
# <a name="rwtexture1darraygetdimensions-function"></a>RWTexture1DArray::GetDimensions-Funktion

Gibt die Dimensionen der Ressource zurück.

## <a name="syntax"></a>Syntax

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Elements
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Breite* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Ressourcenbreite in Texeln.

</dd> <dt>

*Elemente* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dies ist eine Liste der überladenen Versionen dieser Methode.


```
void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(out float Width,
  out UINT Elements);
```



Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[RWTexture1DArray](sm5-object-rwtexture1darray.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
