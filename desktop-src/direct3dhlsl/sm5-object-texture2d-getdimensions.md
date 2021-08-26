---
title: Texture2D::GetDimensions-Funktion
description: Gibt die Dimensionen der Ressource zurück. | Texture2D::GetDimensions-Funktion
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
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
ms.openlocfilehash: 46eb5101dc119d2779f60d2e2b39a42c695933a5bffd477b407fea56c930038c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067700"
---
# <a name="texture2dgetdimensions-function"></a>Texture2D::GetDimensions-Funktion

Gibt die Dimensionen der Ressource zurück.

## <a name="syntax"></a>Syntax

``` syntax
void GetDimensions(
  in  
            uint MipLevel,
  out 
            uint Width,
  out uint Height,
  out 
            uint NumberOfLevels
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*MipLevel* \[ In\]
</dt> <dd>

Typ: **uint**

Optional. Die Mipmapebene (muss angegeben werden, wenn *NumberOfLevels* verwendet wird).

</dd> <dt>

*Breite* \[ out\]
</dt> <dd>

Typ: **uint**

Die Ressourcenbreite in Texeln.

</dd> <dt>

*Höhe* \[ out\]
</dt> <dd>

Typ: **uint**

Die Ressourcenhöhe in Texeln.

</dd> <dt>

*NumberOfLevels* \[ out\]
</dt> <dd>

Typ: **uint**

Die Anzahl der Mipmap-Ebenen (erfordert *auch MipLevel).*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nichts

## <a name="remarks"></a>Hinweise

Dies ist eine Liste der überladenen Versionen dieser Methode.


```
void GetDimensions(uint MipLevel, 
  out uint Width,
  out uint Height,
  out uint NumberOfLevels);

void GetDimensions (out uint Width,
  out uint Height);

void GetDimensions(uint MipLevel,
  out float Width,
  out float Height,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height);
```



Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




