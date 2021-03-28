---
title: 'Texture2D:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | Texture2D:: GetDimensions-Funktion'
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
ms.openlocfilehash: ba1fa832b51e86b5df3193895caa293bb006d82a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995630"
---
# <a name="texture2dgetdimensions-function"></a>Texture2D:: GetDimensions-Funktion

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

*Miplevel* \[ in\]
</dt> <dd>

Typ: **uint**

Optional. Die MipMap-Ebene (muss angegeben werden, wenn " *numoflevels* " verwendet wird).

</dd> <dt>

*Breite* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Die Ressourcen Breite in Texels.

</dd> <dt>

*Höhe* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Die Ressourcen Höhe in Texels.

</dd> <dt>

*Nummerige* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Die Anzahl von MipMap-Ebenen (erfordert auch *miplevel* ).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nichts

## <a name="remarks"></a>Bemerkungen

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



Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




